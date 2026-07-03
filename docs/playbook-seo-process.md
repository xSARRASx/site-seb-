# Playbook SEO — Processus répétable pour TOUS les sites élèves

Objectif : un même circuit appliqué à chaque site, pour que tous soient bien
référencés, sans rien réinventer à chaque fois.

> **Rôles :**
> - **Camille** = collecte les infos + applique les changements dans WordPress.
> - **Claude (cette conv)** = analyse, produit la fiche de corrections prête à coller.
> - **Toi (Seb)** = valides les décisions et contrôles le rendu final.

> ## 🚧 PÉRIMÈTRE DE LA PRESTATION (important, à retenir)
> La prestation = **le référencement naturel (SEO) uniquement** : mots-clés, Titles/métas,
> structure Hn, vocabulaire conforme (Loi Hoguet), technique (indexation, sitemap, Search
> Console) et fiche Google Business.
>
> ❌ **NE FONT PAS partie du périmètre** (donc on ne les rédige pas) :
> - La **rédaction des articles de blog** → c'est au **client** (ou une prestation à part).
> - La création/refonte du design ou du contenu éditorial des pages.
>
> → On **optimise** l'existant pour le SEO, on n'écrit pas le contenu à la place du client.

---

## 🔁 La boucle, étape par étape (par site)

### Étape 1 — Cadrage (Camille) · 5 min
Dans le **tableau de bord de suivi** (`index.html`), ajouter le site avec :
nom client, **URL**, **activité** (conciergerie / sous-location), **Carte G oui/non**,
**ville/zone**, accès WP, e-mail, et le **formulaire** rempli en pièce jointe.
👉 La Carte G détermine tout le vocabulaire autorisé.

### Étape 2 — Envoi à Claude (Camille → cette conv)
Coller dans la conversation :
1. Les **infos de cadrage** (ou le formulaire).
2. Les **captures de chaque page** (groupées par page : Accueil, À propos, Services, Contact, Blog).
   → 5-10 images par message, page par page.

### Étape 3 — Analyse & fiche de corrections (Claude) · automatique
Je produis pour chaque site **un document unique** (comme `seo-dortranquille-corrections-site.md`) avec :
- **Partie 1** : corrections **Loi Hoguet** (chaque « gestion / gérer » → remplacement exact)
- **Partie 2** : **Title + meta + requête cible** par page (prêts à coller dans Yoast)
- **Partie 3** : autres corrections (typos, témoignages, blog, ALT, cohérence marque)
- **Partie 4** : checklist technique + fiche Google Business
- **Récap des décisions** à valider

### Étape 4 — Application dans WordPress (Camille) · 1h-1h30
- Coller les **Title/meta/requête** dans Yoast, page par page.
- Corriger les **textes** (Hoguet + typos) dans Elementor.
- Ajouter les **ALT** images, vérifier H1/H2.
- Régler le **technique** : indexation ON, sitemap → Search Console, cache, WebP.
- Optimiser la **fiche Google Business** (NAP identique).

### Étape 5 — Vérification & reporting (Camille + toi) · 10 min
- Re-tester l'indexation + l'affichage des snippets dans Google.
- Remplir le **modèle de reporting** (`modele-reporting-client.md`) :
  mots-clés ciblés, position, date, prochaines étapes + capture.
- Passer le site en **« Terminé »** dans le tableau de bord.

---

## 📋 Checklist « bon référencement » (valable pour CHAQUE site)

**Contenu / on-page**
- [ ] Title 55-60 car. (mot-clé + ville en début) sur chaque page
- [ ] Meta description 140-155 car. (accroche + ville + CTA)
- [ ] 1 seul H1 par page, structure H2/H3 logique
- [ ] Mot-clé naturel dans l'intro, ALT sur les images
- [ ] Maillage interne entre les pages
- [ ] **Zéro vocabulaire interdit** si pas de Carte G

**Technique**
- [ ] Site indexable (case « décourager les moteurs » décochée)
- [ ] Permaliens propres, cache actif, images WebP, HTTPS, pas de 404
- [ ] Search Console + sitemap soumis

**Local**
- [ ] Fiche Google Business optimisée, NAP cohérent site ↔ fiche

---

## ⚖️ La règle qui ne bouge jamais (Loi Hoguet)

Sans Carte G : **jamais** « gestion », « gestionnaire », « gestion locative »
(ni « gestion Airbnb »). On reste sur **conciergerie, location courte durée,
location saisonnière, sous-location, optimisation, prise en charge, accompagnement**.
→ C'est la 1ʳᵉ chose à vérifier sur chaque site, y compris ceux repris d'un ancien collaborateur.

---

## 🗂️ Les outils déjà prêts (dans ce dépôt)
- `index.html` → tableau de bord de suivi des sites
- `docs/procedure-seo-collaborateur.md` → fiche de consignes détaillée
- `docs/modele-reporting-client.md` → modèle de rapport client
- `docs/seo-dortranquille-corrections-site.md` → exemple concret de fiche de corrections

---

## 🚀 Pour aller plus vite (optionnel, plus tard)
- Faire **2-3 sites ensemble** pour caler le rythme de Camille.
- Une fois le circuit rodé, on peut **standardiser les Title/meta par type d'activité**
  (gabarit « conciergerie + ville ») pour gagner du temps sur les sites suivants.
