# Procédure SEO — Fiche de consignes collaborateur

**Maison du Web** · Procédure de référence pour le référencement des sites clients
(conciergerie / sous-location)

> **Durée cible : 1h30 à 2h par site.** Le premier site prend toujours un peu
> plus de temps, ensuite le rythme se prend. Si les mots-clés sont
> concurrentiels ou que le site a beaucoup de pages, dépasser 2h est normal.

---

> ## ⚠️ RÈGLE VOCABULAIRE — À LIRE AVANT TOUT (Loi Hoguet)
>
> **Si le client n'a PAS la Carte G**, on n'utilise JAMAIS les mots suivants,
> ni dans les Titles, ni dans les metas, ni dans les mots-clés ciblés, ni dans
> le contenu des pages, ni dans la fiche Google Business :
>
> - ❌ **gestion locative**
> - ❌ **gestionnaire**
> - ❌ **gestion** (y compris « gestion Airbnb »)
>
> **Vocabulaire AUTORISÉ et à privilégier :**
>
> - ✅ **conciergerie**
> - ✅ **location courte durée**
> - ✅ **location saisonnière**
> - ✅ **sous-location** (pour les clients sous-location)
>
> 👉 Attention : « gestion Airbnb » est un mot-clé qui ressort beaucoup dans les
> outils, donc la tentation de l'utiliser est forte. **C'est précisément ce
> qu'il ne faut pas faire.** Vérifier ce point sur les sites repris d'un ancien
> collaborateur — l'erreur a déjà été commise.

---

## 0. Accès et cadrage — 5 min

- [ ] Vérifier l'accès **WP admin**.
- [ ] Vérifier l'accès à la **fiche Google Business** (partage sur
      `service@maisonduweb.fr`).
- [ ] **Identifier l'activité : conciergerie ou sous-location.**
      → C'est ça qui détermine le vocabulaire autorisé pour toute la suite
      (voir encadré ci-dessus).

## 1. Installation et configuration de Yoast SEO — 15 min

- [ ] Installer **Yoast SEO**, lancer l'assistant de configuration.
- [ ] Renseigner : type de site, nom de l'entreprise, logo, réseaux sociaux.
- [ ] Désactiver l'indexation des pages inutiles : archives d'auteur (site
      mono-auteur), pages de pièces jointes, formats.
- [ ] Régler le séparateur et le modèle de titre par défaut.

## 2. Connexion aux outils Google — 15 min

- [ ] Ajouter et valider le site dans **Google Search Console** (balise HTML ou
      DNS).
- [ ] Soumettre le **sitemap XML** généré par Yoast : `/sitemap_index.xml`.
- [ ] Lancer l'indexation et vérifier avec `site:domaineduclient.fr`.

## 3. Recherche de mots-clés locaux — 15 à 20 min

- [ ] **Mot-clé principal = activité + ville** (ex : « conciergerie Dax »).
- [ ] Ajouter 2-3 variantes par page :
      - « conciergerie Airbnb [ville] »
      - « location courte durée [ville] »
      - « conciergerie [zone] »
- [ ] Client **sous-location** : « loyer garanti [ville] », « sous-location
      [ville] ».

> **Rappel légal :** respecter strictement l'encadré vocabulaire en tête de
> fiche. Pas de « gestion » sans Carte G.

## 4. Optimisation on-page, page par page — 30 à 40 min

> **C'est le plus gros du temps.** Pour chaque page (Accueil, services, à
> propos, zones, contact) :

- [ ] **Title** de 55-60 caractères, avec mot-clé + ville **en début**.
- [ ] **Meta description** de 140-155 caractères : accroche + ville + appel à
      l'action.
- [ ] **Un seul H1** par page, structure H2/H3 logique.
- [ ] **Slug** court et propre.
- [ ] Mot-clé présent **naturellement** dans l'introduction.
- [ ] Balises **ALT** sur toutes les images, avec mots-clés descriptifs.
- [ ] **Maillage interne** entre les pages.
- [ ] Viser le **feu vert** (ou orange acceptable) dans Yoast, **sans bourrage
      de mots-clés**.

## 5. SEO technique de base — 15 min

- [ ] Site indexable : **Réglages > Lecture**, la case « décourager les moteurs »
      doit être **décochée**.
- [ ] Permaliens en « **nom de l'article** ».
- [ ] **Cache actif** : LiteSpeed sur Hostinger, WP Rocket sur OVH / O2Switch.
- [ ] Images en **WebP** via Converter for Media.
- [ ] **HTTPS** actif, cohérence **www / non-www**, **pas de 404**.

## 6. SEO local et fiche Google Business — 15 à 20 min

- [ ] Bonne **catégorie**.
- [ ] Description avec **vocabulaire conforme** (voir encadré).
- [ ] **Zone desservie**, horaires, photos, lien vers le site.
- [ ] **NAP cohérent** : Nom, Adresse, téléphone (Phone) **identiques** entre le
      site et la fiche.

> C'est souvent ce qui fait sortir le client dans le **pack local** → à ne pas
> négliger sur ces activités de proximité.

## 7. Vérification finale et reporting — 10 min

- [ ] Re-tester l'**indexation**.
- [ ] Vérifier que les **Titles et metas** s'affichent bien dans Google.
- [ ] **Produire le rapport client** (voir `modele-reporting-client.md`).

---

### Récapitulatif des temps

| Étape | Durée |
|---|---|
| 0. Accès et cadrage | 5 min |
| 1. Yoast SEO | 15 min |
| 2. Outils Google | 15 min |
| 3. Mots-clés locaux | 15-20 min |
| 4. On-page (le gros) | 30-40 min |
| 5. SEO technique | 15 min |
| 6. SEO local / Google Business | 15-20 min |
| 7. Vérif + reporting | 10 min |
| **Total réaliste** | **1h30 – 2h** |
