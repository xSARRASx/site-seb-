# HANDOFF-AUTOMATISATION-SEO.md — Documentation technique du système « Suivi SEO »

> **But :** documenter précisément le système actuel du tableau « Suivi SEO » pour que ChatGPT puisse
> reprendre le projet proprement et évaluer l'automatisation du workflow (Camille ajoute un site → l'IA
> récupère la fiche → fait le SEO → met à jour statut + compte rendu).
> **Rien n'a été modifié en production.** Aucun secret, mot de passe, token ou clé n'est inclus.
> Rédigé le 27/09/2026.

---

## ⚠️ RÉSUMÉ EN UNE PHRASE (à lire en premier)
Le « Suivi SEO » est un **fichier HTML statique unique** (`index.html`), en **JavaScript vanilla**, qui stocke
les fiches dans le **localStorage du navigateur**. **Il n'y a AUCUN backend, AUCUNE base de données, AUCUNE API,
AUCUNE authentification, AUCUN temps réel, AUCUN déploiement automatisé, AUCUN webhook/cron.**
→ **En l'état, une IA externe (ChatGPT) NE PEUT PAS lire ni écrire les fiches** : elles vivent uniquement dans le
navigateur de la personne qui les a saisies. **Automatiser le workflow demandé nécessite d'ajouter un backend**
(voir §13). Ce document décrit l'existant tel qu'il est, sans rien changer.

---

## 1. Repo, branche, dernier commit
- **Repo GitHub :** `https://github.com/xSARRASx/site-seb-`
- **Branche actuelle :** `claude/friendly-shannon-e3fr6a`
- **Dernier commit pertinent (avant ce doc) :** `7b059b3` — « Ajout doc handoff complet (tout le savoir SEO + methode + 8 sites) ».
- Le dépôt ne contient PAS de branche `main`/`master` active dans cette session : tout le travail est sur `claude/friendly-shannon-e3fr6a`.

## 2. Fichiers qui font fonctionner le tableau « Suivi SEO »
Contenu réel du dépôt (à la racine) :
| Fichier | Rôle |
|---|---|
| **`index.html`** | **LE tableau « Suivi SEO » en entier** : HTML + CSS + JavaScript, tout dans ce seul fichier (~22 Ko, ~495 lignes). C'est lui, et lui seul, qui fait fonctionner l'app. |
| `SEO.md` | Dossier maître (connaissances SEO, méthode, 8 sites). Documentation, pas de code. |
| `docs/` | Docs par site + templates de prompts (markdown). Documentation. |
| `guide-dortranquille.html` | Page-guide interactive (autre livrable statique, indépendant du tableau). |
| `recap-camille.html` | Page récap statique (indépendante du tableau). |

> ⚠️ **`seo.html` n'existe pas** dans le dépôt. Le tableau s'appelle **`index.html`**.
> ⚠️ **Divergence à clarifier (voir §11)** : les « fiches » que Camille produit (celles collées en conversation)
> contiennent des champs **absents de `index.html`** : `Mot de passe`, `Lien admin`, `Google My Business`,
> `Lien Drive`. → Soit une **version plus complète** du tableau existe **hors de ce dépôt**, soit Camille utilise
> un **autre outil / gabarit**. Le présent doc décrit `index.html` tel qu'il est dans ce repo.

## 3. Stack technique
- **Frontend :** HTML5 + CSS (inline dans `<style>`) + **JavaScript vanilla** (aucun framework, aucune dépendance, aucun build, aucun `package.json`).
- **Backend :** **AUCUN.**
- **Base de données :** **AUCUNE.** Persistance = **`window.localStorage`** du navigateur.
- **Hébergement / déploiement :** **AUCUN pipeline.** Le fichier s'ouvre localement (double-clic) ou peut être servi en statique (GitHub Pages, Hostinger, etc.) mais **aucune config de déploiement n'existe dans le repo** (pas de `.github/workflows`, pas de `netlify.toml`/`vercel.json`, pas de `Procfile`).

## 4. Où sont stockées les fiches + schéma des données
- **Stockage :** `localStorage`, sous **une seule clé** : **`mdw_seo_sites`**.
- **Format :** un tableau JSON d'objets « site », sérialisé (`JSON.stringify`). Lu par `load()`, écrit par `save()`.
- **Les fichiers joints** (captures, PDF) sont convertis en **base64 (dataURL)** via `FileReader` et stockés **dans le même localStorage** (⚠️ gonfle vite le quota ~5 Mo → voir §11).

**Schéma d'un objet « site » (champs réellement gérés par `index.html`) :**
| Champ | Type | Valeurs / notes |
|---|---|---|
| `id` | string | généré par `uid()` = `Date.now().toString(36)+random` |
| `name` | string | nom du client (obligatoire) |
| `url` | string | URL du site |
| `activity` | string | « Conciergerie » / « Sous-location » / « Conciergerie + sous-location » |
| `city` | string | ville / zone |
| `prestation` | string | `complet` / `local` |
| `zoneok` | string | `ok` (confirmée) / `tbc` (à confirmer) |
| `cg` | string | `no` / `yes` (Carte G) |
| `status` | string | **`todo` / `doing` / `done`** |
| `email` | string | e-mail client |
| `phone` | string | téléphone |
| `gmail` | string | compte Google du client (pour Site Kit) |
| `gbp` | string | `none` / `exists` (fiche Google Business) |
| `address` | string | adresse |
| `socials` | string | URLs réseaux sociaux |
| `note` | string | note libre / compte rendu |
| `files` | array | `[{ name, type, dataUrl(base64) }]` |

> ⚠️ Il n'existe **PAS** de champ dédié `password` / `admin_url` / `drive_url` / `gmb_url` dans `index.html`
> (contrairement aux fiches de Camille — cf. §2 divergence). Le seul « fourre-tout » est `note`.

## 5. Temps réel entre Camille et Martin
**Il n'y en a pas.** `localStorage` est **strictement local à un navigateur, sur un appareil**. Ce que Camille
saisit sur son ordinateur **n'est pas visible** par Martin, et inversement. Aucune synchronisation, aucun partage,
aucun serveur central. (C'est déjà noté comme limite dans `SEO.md` §13.) Pour un vrai partage/temps réel → backend requis (§13).

## 6. Fonctions internes (il n'y a PAS d'API/endpoints — ce sont des fonctions JS locales)
Le fichier n'expose aucun endpoint réseau. Les « opérations » sont des fonctions JavaScript qui manipulent le
tableau en mémoire puis appellent `save()` (écriture localStorage) + `render()` (rafraîchissement DOM) :
| Besoin | Fonction JS (dans `index.html`) | Détail |
|---|---|---|
| Lire la liste des sites | `load()` | `JSON.parse(localStorage.getItem('mdw_seo_sites'))` → tableau. |
| Afficher / filtrer | `render()` + `setFilter(f, el)` | filtre par `status` (`all/todo/doing/done`). |
| Lire une fiche complète | `sites.find(s => s.id === id)` (via `editSite(id)` → `openModal(site)`) | ouvre la modale pré-remplie. |
| Créer une fiche | `saveSite()` avec `f-id` vide | `sites.unshift(data)` + `save()`. |
| Modifier une fiche | `saveSite()` avec `f-id` renseigné | `sites.map(...)` remplace l'objet + `save()`. |
| Changer le statut | `changeStatus(id, val)` | `{...s, status: val}` + `save()` + `render()`. |
| Notes / compte rendu | champ `note` du formulaire, écrit par `saveSite()` | pas de champ « compte rendu » séparé — c'est `note`. |
| Supprimer | `delSite(id)` | `confirm()` puis `filter` + `save()`. |
| Fichiers | `addFiles(fileList)`, `removeFile(i)`, `renderFileList()` | base64 en localStorage. |

## 7. Stockage & protection des accès WordPress clients
- **Dans ce dépôt : AUCUN accès client n'est stocké.** `index.html` n'a pas de champ mot de passe ; le code ne contient aucun identifiant.
- **Politique appliquée dans tout le projet :** les **mots de passe WordPress ne sont JAMAIS stockés** dans le repo ni dans les docs → toujours « à demander à Camille » (cf. `SEO.md`).
- **⚠️ Point de sécurité (si la version complète de Camille stocke les mots de passe) :** ils seraient alors en
  **clair dans le localStorage** du navigateur (aucun chiffrement, aucune protection) → à considérer comme un
  risque réel à corriger lors de la mise en place d'un backend (chiffrement au repos + accès restreint).
- **Aucune variable d'environnement n'existe** aujourd'hui (pas de backend). Le seul « secret » d'environnement
  connu du projet global est le compte Google agence **martinmorebkk@gmail.com** (identité, pas un secret stocké
  dans le code). Quand un backend sera créé, les secrets (ex. `SUPABASE_URL`, `SUPABASE_SERVICE_KEY`, `GITHUB_TOKEN`…)
  devront être définis **côté hébergeur (variables d'environnement du service)**, jamais dans le repo — mais **rien de tel n'existe encore**.

## 8. Authentification & rôles Martin / Camille
- **Aucune authentification** dans `index.html` : pas de login, pas de session, pas de contrôle d'accès.
- Les **rôles Martin / Camille sont uniquement organisationnels** (décrits dans `SEO.md` §1), **pas techniques** :
  n'importe qui ouvrant le fichier a un accès total à SON localStorage. Il n'y a pas de séparation de droits dans le code.

## 9. Déploiement & URL de production
- **Procédure de déploiement : AUCUNE** (pas de CI/CD, pas de config d'hébergeur dans le repo).
- **URL de production : inconnue / non déclarée dans le repo.** Le fichier fonctionne en local (`file://`) ou
  s'il est servi en statique quelque part — mais aucune trace de cet endroit dans le dépôt. **À clarifier (§11).**
- Publication du code = `git commit` + `git push origin claude/friendly-shannon-e3fr6a` (c'est tout ce qui existe).

## 10. Webhooks / cron / automatisations / services externes
- **AUCUN.** Pas de webhook, pas de cron, pas de tâche planifiée, pas de service externe (pas de Supabase/Firebase,
  pas de Google Sheets API, pas de Zapier/Make, pas d'appel réseau sortant dans le code).
- Le SEO lui-même est appliqué **manuellement** via l'extension « Claude pour Chrome » (pilotage du navigateur),
  pas via une automatisation serveur (cf. `SEO.md` / `docs/HANDOFF-COMPLET.md`).

## 11. Limites, bugs connus, points de sécurité
- **Pas de partage entre appareils** (localStorage local) → Camille et Martin ne voient pas les mêmes données. **C'est LA limite bloquante pour l'automatisation.**
- **Une IA externe ne peut pas accéder au localStorage** → impossible de « récupérer la fiche » à distance en l'état.
- **Quota localStorage ~5 Mo** : les fichiers en base64 le saturent vite → `saveSite()` a un `try/catch` qui alerte « fichiers trop volumineux ».
- **Aucune sauvegarde/backup** : vider le cache navigateur = perte des fiches.
- **Aucune authentification / chiffrement** : données (et mots de passe éventuels) en clair dans le navigateur.
- **Divergence de schéma** entre `index.html` (ce repo) et les fiches de Camille (champs password/admin/Drive/GMB en plus) → **origine à clarifier** (version hors repo ? autre outil ?).
- **URL de production inconnue** (non déclarée dans le repo).
- Données de démo : au **premier lancement** (localStorage vide), `index.html` injecte 3 sites d'exemple fictifs.

## 12. Exemple FICTIF de fiche au format JSON (schéma réel de `index.html`, aucune donnée réelle)
```json
{
  "id": "lz9k2a4b",
  "name": "Conciergerie Exemple",
  "url": "https://exemple-conciergerie.fr",
  "activity": "Conciergerie",
  "city": "Villeneuve-sur-Exemple",
  "prestation": "local",
  "zoneok": "ok",
  "cg": "no",
  "status": "todo",
  "email": "contact@exemple-conciergerie.fr",
  "phone": "06 00 00 00 00",
  "gmail": "exemple.conciergerie@gmail.com",
  "gbp": "none",
  "address": "1 rue de l'Exemple, 00000 Villeneuve-sur-Exemple",
  "socials": "https://facebook.com/exemple | https://instagram.com/exemple",
  "note": "SEO local à faire. Sans Carte G. Zone confirmée. Mot de passe WP : à demander à Camille (jamais ici).",
  "files": []
}
```
> La liste complète stockée est un **tableau** de tels objets sous la clé `mdw_seo_sites`.

## 13. La manière la plus propre pour permettre à ChatGPT d'automatiser le workflow
**Constat :** l'automatisation demandée (détecter un site `todo` → lire la fiche → passer `doing` → travailler →
écrire le compte rendu → passer `done`) est **impossible sur l'architecture actuelle** (localStorage non accessible
à distance). Il faut d'abord **externaliser les données** dans un stockage adressable par API. **Rien de tout cela
n'a été mis en place** (conformément à ta consigne : documenter, ne rien lancer). Voici les options, de la plus légère à la plus robuste :

**Option A — Google Sheet (la plus simple, non-dev).** Le tableau devient une feuille Google ; ChatGPT y accède via
un connecteur/Apps Script. Champs = colonnes du schéma §4 + `status` + `compte_rendu`. Camille remplit, ChatGPT lit/écrit.

**Option B — Backend léger (Supabase/Firebase).** Une table `sites` (schéma §4). `index.html` est adapté pour lire/écrire
via l'API REST au lieu du localStorage → partage + temps réel natifs. ChatGPT (ou un script) tape la même API :
`GET /sites?status=todo`, `GET /sites/:id`, `PATCH /sites/:id {status:'doing'}`, `PATCH /sites/:id {note:'…'}`, `PATCH /sites/:id {status:'done'}`.
Secrets côté hébergeur en variables d'env (`SUPABASE_URL`, `SUPABASE_ANON_KEY`, `SUPABASE_SERVICE_KEY`) — jamais dans le repo.

**Option C — Le repo GitHub comme base (via l'API GitHub).** Les fiches deviennent des fichiers JSON versionnés
(ex. `sites/<id>.json`). ChatGPT lit/écrit via l'API GitHub (token en variable d'env `GITHUB_TOKEN`), le statut et le
compte rendu = champs du JSON commités. Avantage : historique/versionné, cohérent avec l'existant. Inconvénient : pas de temps réel.

**Flux cible (une fois un backend en place, quelle que soit l'option) :**
1. Détecter un nouveau site : lister les fiches où `status === "todo"`.
2. Récupérer sa fiche : lire l'objet complet par `id`.
3. Passer `doing` : écrire `status = "doing"`.
4. Travailler : appliquer le SEO (via l'extension Claude pour Chrome — cf. `docs/HANDOFF-COMPLET.md`).
5. Enregistrer le compte rendu : écrire dans `note` (ou ajouter un champ dédié `compte_rendu`).
6. Passer `done` : écrire `status = "done"`.

> **Recommandation :** ne PAS coupler l'IA au localStorage. Choisir une des options A/B/C **avec Martin** avant tout
> développement. **Aucune de ces options n'est implémentée aujourd'hui** — ce document ne fait que les décrire.

---

## Points restant à clarifier (à valider avec Martin/Camille)
1. **Divergence de schéma** : d'où viennent les fiches de Camille avec `Mot de passe / Lien admin / Google My Business / Lien Drive` ? Version de `index.html` hors repo, ou autre outil ? (impacte tout le §4/§12).
2. **URL de production** réelle du tableau (est-il hébergé quelque part, ou seulement en local ?).
3. **Choix de la cible d'automatisation** : option A (Google Sheet), B (Supabase/Firebase) ou C (repo GitHub) ?
4. **Politique de stockage des mots de passe WordPress** : si on centralise, il faut du chiffrement + accès restreint (ils ne doivent jamais finir en clair ni dans le repo).
5. **Branche de travail** : rester sur `claude/friendly-shannon-e3fr6a` ou fusionner vers une branche par défaut avant de bâtir l'automatisation ?
