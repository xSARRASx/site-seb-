# 📗 SEO.md — Dossier maître (Maison du Web)

> **But de ce fichier :** tout ce qu'on a construit pour le référencement (SEO) des sites
> des élèves/clients, au même endroit. Si une conversation expire, on repart d'ici.
> Dernière grosse mise à jour : session « premier site D'Or Tranquille » + lancement Valse de Lin.

---

## 1. C'est quoi cette prestation
On fait le **référencement naturel (SEO) local** de sites de conciergerie / sous-location
(sites WordPress + Elementor + Yoast). Objectif : que le client ressorte sur Google sur
« conciergerie + sa ville ».

**Rôles :**
- **Camille** = collecte les infos client + applique les changements dans WordPress.
- **Claude** = analyse, prépare les mots-clés / titres / corrections + les prompts.
- **Seb** = valide et contrôle.

---

## 2. ⚖️ LA RÈGLE D'OR — Loi Hoguet
Client **sans Carte G** → le site ne doit **JAMAIS** contenir :
**gestion · gestionnaire · gérer · gestion locative · gestion Airbnb**.
Remplacer par : **prise en charge · coordination · suivi · accompagnement · optimisation**.
Vocabulaire autorisé : **conciergerie · location courte durée · location saisonnière · sous-location**.
👉 Vérif finale : **Ctrl+F « gestion » ET « gérer »** sur chaque page = 0 résultat.

---

## 3. Le processus (par site)
1. **Cadrage** : URL, **Carte G oui/non**, ville/zone, activité, accès WP, formulaire.
2. **Récupération du contenu** : soit captures des pages, soit **audit par l'extension** (voir §5).
3. **Analyse** (Claude) : mots-clés, Titres/métas, structure Hn, liste des corrections.
4. **Application** dans WordPress : soit à la main, soit via l'**extension Claude pour Chrome**.
5. **Technique + Google** : indexation, sitemap, Search Console, fiche Google Business.
6. **Vérif + reporting** → passer le site en « Terminé » dans le tableau de bord.

---

## 4. Les mots-clés (comment on les choisit)
- **Formule** : activité + ville → « conciergerie [ville] », « conciergerie Airbnb [ville] ».
- **Prioriser les villes qui ont du trafic** (stations touristiques) plutôt que les petits villages.
- Mettre les **2 orthographes** si besoin (ex : « Les 2 Alpes » / « Les Deux Alpes »).
- Variantes : location courte durée [ville] · location saisonnière [ville] · conciergerie chalet/appartement [ville] · optimisation des annonces Airbnb [ville].
- Un **mot-clé principal par page** (à mettre dans Yoast).

---

## 5. ⭐ La méthode « extension Claude pour Chrome » (recommandée)
L'extension (sur **claude.ai**, pas Claude Code) pilote le navigateur → elle peut **lire ET modifier** le site.
Comme le site bloque souvent la lecture externe (403), c'est **elle** qui fait l'audit.

**On procède en 2 temps :**
1. **PROMPT D'AUDIT** (lecture seule) → l'extension explore tout le site et renvoie un récap
   (pages, titres, H1 manquants, « gestion », ALT vides, liens cassés, fautes, faux avis…).
   → On copie ce récap à Claude.
2. **PROMPT DE MODIFICATION** (sur-mesure) → Claude le prépare à partir du récap réel,
   l'extension applique tout en autonomie et fait un récap final.

📄 Templates prêts : `docs/TEMPLATE-prompt-navigateur-SEO.md` et `docs/prompt-pilotage-navigateur.md`.

> ⚠️ L'extension agit sur **l'onglet actif** → ouvrir le site (idéalement `/wp-admin` connecté) au premier plan.
> Sur Elementor c'est **lent** → normal.

---

## 6. La structure SEO d'une page (rappel)
- **1 seul H1 par page** = le grand titre du héros (avec mot-clé + ville). ⚠️ Souvent en H2 par défaut → à passer en H1.
- **H2** = sections · **H3** = sous-blocs/cartes.
- **Titre SEO** 55-60 car. (mot-clé + ville en début) · **Méta** 120-155 car. (barre verte Yoast).
- ALT sur les images (avec mot-clé + ville) · maillage interne.

---

## 7. Le SEO technique + Google
- **Langue du site = Français** (Settings → General → Site Language) → pour `og:locale = fr_FR`.
- **Indexation ON** (Settings → Reading, case « décourager » décochée).
- **Permaliens** = « Post name ».
- **Sitemap** Yoast : `[site]/sitemap_index.xml`.
- **Search Console** : bonne propriété → envoyer le sitemap → « Demander une indexation » par page.
- **Fiche Google Business** : catégorie « Service de conciergerie » (jamais « gestion immobilière »),
  NAP identique au site, zone, photos, description sans « gestion ».

---

## 8. 🗂️ Sites traités

### ✅ D'Or Tranquille — dortranquille.fr (Les 2 Alpes) — TERMINÉ
- Conciergerie, sans Carte G. On-page + technique + Google Business faits.
- Détails : `docs/seo-dortranquille-les2alpes.md`, `docs/seo-dortranquille-corrections-site.md`,
  `guide-dortranquille.html`, `docs/recap-verification-dortranquille.md`.
- Restait en option : ALT images, 1er article de blog (= au client).

### ✅ Valse de Lin — valsedelin.fr (Sainte-Reine-de-Bretagne) — ON-PAGE FAIT
- Karine **Riou**, conciergerie SASU, **sans Carte G**. SIRET 107 254 401 00014.
- **Adresse** : 10 Bis rue des Sapins, 44160 Sainte-Reine-de-Bretagne.
- **Tél** : 06 10 90 52 09 (tel:+33610905209) · **E-mail** : accueil@valsedelin.fr · Horaires Lun-Ven 9h-18h30.
- **Réseaux** : Facebook (profil id) + Instagram (instagram.com/valsedelin/).
- **Zone RÉELLE (confirmée par la cliente)** : **la Brière, Pontchâteau, La Roche-Bernard et alentours**.
  ⚠️ La Baule / Guérande / Pornichet / Saint-Nazaire = **HORS secteur** (retirés le 25/07 après retour de Karine —
  ils étaient dans la liste initiale de Camille mais ce n'est pas sa zone). ✅ Recentrage appliqué en ligne
  (H1, 7 titres/métas, footer, articles, ALT). Laissé volontairement : « tribunaux de Saint-Nazaire »
  dans les mentions légales (= tribunal de rattachement, juridiquement correct, page noindex).
  À faire plus tard : renommer les fichiers images (…la-baule…), remplacer les visuels bord de mer par des photos de Brière.
- **Mot-clé principal** : « conciergerie Brière » (+ Pontchâteau / La Roche-Bernard).
- **GMB à corriger** : retirer La Baule/Guérande/Pornichet/Saint-Nazaire des zones desservies de la fiche.
- **Méthode** : audit puis correction via l'extension Claude pour Chrome (docs `valsedelin-modification-prompt.md`).
- **Fait** ✅ : titres+métas (7 pages), H1 sur toutes les pages, tous les « gestion/gérer » retirés,
  ALT sur les 42 images, noindex mentions/politique, nom d'auteur « Karine Riou », liens sociaux/footer,
  fautes corrigées, faux avis masqués, archives d'auteur désactivées, hero H1+H2.
- **Fiche Google Business** : ✅ créée (prestataire de services, adresse masquée) — catégorie
  **« Conciergerie privée »** (« Service de conciergerie » n'existe pas chez Google), 11 zones,
  tél, site, horaires, description (462/750). ⏳ **Vérification à faire par Karine** (vidéo) —
  rien de public avant. À ajouter : **logo + photos** (depuis le Drive), catégorie secondaire
  « Service de nettoyage », liste des services.
- **Search Console** : ✅ propriété https://valsedelin.fr ajoutée (Préfixe d'URL) + validée via Yoast
  (Connexions du site → code Google), sitemap `sitemap_index.xml` envoyé, 7 pages soumises à l'indexation
  (6 déjà indexées, /faq/ relancée).
- **Reste** : vérification GMB (vidéo) + photos par Karine · pages locales par ville (projet à part) · vrais avis · blog = au client.

> ⚠️ RAPPEL PROCESS : la **Search Console (ajout propriété + vérif Yoast + sitemap + demande d'indexation)**
> fait partie du process de BASE à chaque site — voir ÉTAPE 6 du template. Ne pas l'oublier.

---

### ✅✅ Léandro Conciergerie — leandroconciergerie.fr (Grenoble) — TERMINÉ
- Lucie & Jonathan, conciergerie SAS, **sans Carte G**. SIREN 107 309 882. Siège : **47 rue Vivienne, 75002 Paris** (⚠️ pas d'adresse à Grenoble → handicap local).
- **Tél** : 07 75 67 42 16 · **E-mail** : contact@leandroconciergerie.fr · Horaires 9h-20h · FB + Insta.
- **Prestation** : SEO LOCAL uniquement (base déjà faite par Camille : Yoast, titres, métas, schema, ALT).
- **Zone** : Grenoble, Grésivaudan, Voiron, Chambéry et les stations. 🚫 **JAMAIS** Vercors ni Aix-les-Bains.
- **Vocabulaire** : interdits = gestion/gérer/gestionnaire **+ « création d'annonces »** → pilotage · coordination · prestataire · optimisation.
- **Fait (extension, prompt `docs/leandro-modification-prompt.md`)** :
  - Conformité : Vercors + Aix-les-Bains retirés (Accueil FAQ+schema FAQPage, CGU, article ×2) ; « création d'annonces » → « Optimisation de vos annonces » ; « mandat de gestion » reformulé en « mandat immobilier / co-hôte » ; « gestion/gérer » corrigés dans confidentialité + mentions légales + pied de page.
  - H1 : 1 seul H1 par page (12 pages), **avec ville** sur les pages principales ; doublons corrigés (Mentions légales, article 5→1, Tarifs bandeau doublon).
  - Yoast : 6 titres+métas enrichis (Grésivaudan/Voiron/Chambéry).
  - Zone dans le contenu : barre d'en-tête + intros Services/Tarifs/À propos + bloc Contact du footer.
  - Schema LocalBusiness (Elementor → Custom Code, ID 480) : ajout telephone, openingHours Mo-Su 09:00-20:00, areaServed Chamrousse + Les 7 Laux, Facebook dans sameAs.
- **⚠️ Reste bloqué** : 6 chaînes « Gérer… » du **plugin Complianz** (bannière cookies + politique cookies UE) = chaînes de traduction du plugin → nécessitent un override **Loco Translate**. Risque faible (vocabulaire cookies, pas immobilier).
- **Search Console** ✅ : propriété créée + validée (balise Yoast), sitemap `sitemap_index.xml` soumis, 7 pages + 3 pages locales envoyées à l'indexation. Propriétaire actuel = martinmorebkk@gmail.com.
- **Pages locales** ✅✅ créées ET **100% vertes Yoast** (17 bons résultats, 0 problème) : /conciergerie-chambery/ (574), /conciergerie-voiron/ (575), /conciergerie-gresivaudan/ (576). Template Elementor Full Width, 1 H1 + 5 H2, ~310-324 mots, 1 image ALT + 1 lien sortant (office de tourisme) par page, maillées (footer + accueil). Titres en correspondance exacte : « Conciergerie [ville] : location courte durée | Léandro ». Déjà indexées (recrawl auto via sitemap lastmod).
  - ⚠️ Piège Elementor↔Yoast : Yoast ne « voit » pas les widgets Heading/Image (reçus en texte brut) → placer `<h2>` et `<img>` DANS un widget Texte pour que les assessments passent au vert (rendu public identique).
- **Site Kit** ✅ installé + connecté (compte martinmorebkk@gmail.com) — « Configuration initiale terminée ». Analytics non connecté (voulu) → cartes « Autorisations insuffisantes » = normal.
- **Propriétaire client Search Console : ABANDONNÉ** — l'email de Lucie est **luciesimonian@outlook.fr** (Outlook, PAS un compte Google) → transfert impossible. La propriété reste sous martinmorebkk@gmail.com. (Camille est admin WP via camillefauveau.service@gmail.com.)
- **Fiche Google Business : CRÉÉE** (finalement faite) — ID 01044066609826807143, sous martinmorebkk@gmail.com, état « Validation requise » / non publique. Catégorie « Conciergerie privée », adresse masquée (services à domicile), tél 07 75 67 42 16, horaires 7j/7 9h-20h, description conforme. Zones (6) : Grenoble, **Communauté de Communes Le Grésivaudan** (⚠️ « Grésivaudan » seul = Sud-Grésivaudan/Saint-Marcellin = MAUVAIS), Voiron, Chambéry, Chamrousse, **Station des Sept Laux** (l'entrée « Les 7 Laux » n'existe pas). Zéro Vercors/Aix. Offres payantes (Ads 400€, Workspace) refusées.
  - **🛑 Reste au CLIENT (Lucie/Jonathan)** : cliquer « Valider » → saisir leur **adresse postale réelle** (non publique) → choisir la vérif (vidéo/courrier/tel/email) ; puis ajouter **logo + 3-5 photos** de logements. Tant que non validé = fiche invisible.
- **À noter** : adresse iséroise absente (siège = Paris = handicap local) — non résolu, dépend du client.
- **À noter** : éditeur de blocs WordPress + page réglages Yoast **plantent** sur ce site (conflit d'extension probable) → contourner via Quick Edit / Elementor. Module « Duplication de contenu » d'ASE activé pour créer les pages.

---

### ✅ Le Nid Mousin — lenidmousin.com (Folles 87250 / Haute-Vienne / Limousin) — SEO COMPLET fait
- Pauline & Jason (Pauline Boulet-Benac EI), conciergerie **+ sous-location**, **sans Carte G**. Tél 06 41 84 03 46 · hello@lenidmousin.com.
- **Zone** : Folles, Haute-Vienne, Limousin, **Limoges** (client cible Limoges via leur article). Marque figée : **« Le Nid Mousin »** (sans apostrophe). Réseaux sociaux laissés vides (choix client).
- ⚠️ **Yoast n'était PAS installé** → SEO complet (pas juste local). Prompt : `docs/lenidmousin-correction-prompt.md`, audit : mega prompt.
- **Fait (extension, one-shot)** : Yoast installé + réglages (slogan, fuseau Paris, archives auteur off) ; **Loi Hoguet 0/0** sur 9 pages (5 remplacements : gestion→coordination/exploitation/suivi) ; 1 seul H1/page avec zone ; 7 titres+métas Yoast verts ; légales en noindex ; **27 images ALT** ; tel: corrigé (+33641840346) ; marque uniformisée ; carte CTA `#`→/services/ ; **Search Console** créée+validée + sitemap Yoast soumis (indexation quota dépassé → refaire demain).
- **⚠️ Schema** : Yoast gratuit ne met pas le téléphone (réservé Yoast Local SEO payant) → **schema LocalBusiness complet ajouté à part** (prompt de finition) avec tél + adresse Folles + areaServed.
- **Finitions (prompt 2)** ✅ : doublon H2 sous-location corrigé ; **schema LocalBusiness JSON-LD** ajouté via Elementor → Code personnalisé (ID 354, `<head>`, tout le site, cohabite avec Yoast, @id distinct) ; Blog ajouté au menu (5e position, header OK sur 1 ligne ≥1080px).
- **Micro-polish** ✅ : libellés de menu raccourcis (« Sous-location », « À propos ») → header plus aéré, tient sur 1 ligne dès 1025px. **SEO 100% terminé.**
- **⚠️ Astuce** : la **traduction auto de Chrome** sur `/wp-admin` affiche des libellés faux (« Sous-localisation », « À propos de ») alors que les vraies valeurs sont bonnes → désactiver la traduction pour éviter les fausses alertes.
- **Site Kit** ✅ installé + connecté (compte martinmorebkk@gmail.com). Le flux OAuth déjà autorisé a tout connecté d'un coup : Search Console + **Analytics GA4 créé** (compte 395592310, propriété 549568632, mesure G-DCWY8V6DY0) + PageSpeed. Gardé (stats en bonus). Objectif « Fournir des services ». Encarts promo (Reader Revenue, Sign in with Google) = ignorés.
- **Reste CLIENT / plus tard** : mentions légales incomplètes (pas de SIRET/adresse/dir. publication) ; aucun avis (à construire) ; slug /services/ (redirection = payant) ; 2 brouillons BACKUP à nettoyer ; **fiche Google Business à créer** (vérif vidéo côté client).

---

## 9. 🧰 Leçons de terrain (voir aussi `docs/procedure-seo-collaborateur.md`)
- **Elementor** : modifier un texte = **clic UNE fois** sur le bloc → panneau de gauche (pas double-clic).
- **Blocs JKit « Icon Box »** : titre + description = champs à gauche.
- **Changer une balise** H1/H2/H3 : clique le titre → réglage **« Balise HTML »**.
- **Footer** = modèle global : Elementor → **Theme Builder → Footer** (édité une fois).
- **Loi Hoguet** : chercher **« gestion » ET « gérer »** (Ctrl+F séparé). Ils se cachent dans footer,
  faux avis, sur-titres, titres de cartes, cartes de valeurs.
- **H1 manquants** = piège fréquent (héros en H2) → vérifier chaque page.
- **Yoast** : icône « Y » en haut à droite → « Apparence de recherche ». Méta verte = 120-155 car.
  « Limace » = slug. Visage rouge sur Elementor = normal.
- **Blog** : virer les `**` parasites dans les titres.
- **Search Console** : vérifier qu'on est sur la **BONNE propriété** (piège : agir sur le mauvais site).
- **Faux avis** = **risque légal** → à retirer/remplacer, ne jamais inventer.

---

## 10. 🚧 Périmètre de la prestation
- ✅ **Inclus** : SEO (mots-clés, titres/métas, Hn, vocabulaire, technique, Search Console, Google Business).
- ❌ **NON inclus** : **rédaction des articles de blog** (= au client), création de design/contenu éditorial.
- → On **optimise** l'existant, on n'écrit pas le contenu à la place du client.

---

## 11. 📁 Index des fichiers du dépôt
| Fichier | Rôle |
|---|---|
| `SEO.md` | **Ce dossier maître** (résumé de tout) |
| `index.html` | Tableau de bord de suivi des sites élèves |
| `docs/playbook-seo-process.md` | Le processus réutilisable + périmètre |
| `docs/procedure-seo-collaborateur.md` | Consignes détaillées + **leçons de terrain** |
| `docs/modele-reporting-client.md` | Modèle de rapport client |
| `docs/TEMPLATE-prompt-navigateur-SEO.md` | **Template du prompt maître** (extension, mode autonome) |
| `docs/prompt-pilotage-navigateur.md` | Exemple de prompt navigateur (D'Or Tranquille) |
| `docs/prompt-integration-seo.md` | Prompt pour intégrer le tableau de bord au site équipe |
| `guide-dortranquille.html` | Guide interactif D'Or Tranquille (copier/coller + cases) |
| `recap-camille.html` | Récap de vérification (jolie page) |
| `docs/seo-dortranquille-les2alpes.md` | Plan SEO complet D'Or Tranquille |
| `docs/seo-dortranquille-corrections-site.md` | Corrections site D'Or Tranquille |
| `docs/recap-verification-dortranquille.md` | Récap vérif D'Or Tranquille |

---

## 12. ❓ Infos à demander pour chaque nouveau site
URL + accès · **Carte G oui/non** · ville/zone · activité · nom exact de la marque ·
téléphone + adresse (NAP) · réseaux sociaux réels · fiche Google Business (existe/à créer) ·
décisions témoignages (vrais/faux/masquer). **Ne jamais deviner : demander si ça manque.**
