# 📗 DOSSIER COMPLET SEO — Maison du Web (handoff pour une nouvelle conversation)

> **À quoi sert ce document :** transmettre TOUT ce qu'il faut savoir pour continuer le référencement (SEO)
> des sites de nos clients conciergerie, sans rien perdre. Colle-le en entier au début d'une nouvelle
> conversation (ChatGPT ou autre) pour qu'elle reprenne exactement au même niveau.
> Dernière mise à jour : 26/09/2026. Rédigé par Claude (Maison du Web).

---

## 1. CONTEXTE & RÔLES

On est une agence (**Maison du Web**) qui fait le **SEO local** de sites de **conciergerie / sous-location**
Airbnb (location courte durée) pour des clients/élèves. Les sites sont sur **WordPress + Elementor (+ Elementor Pro) + Yoast SEO**, hébergés surtout chez **Hostinger**.

**Objectif :** que le client ressorte sur Google sur « conciergerie + sa ville » (+ location courte durée, Airbnb…).

**Rôles :**
- **Camille Fauveau** = collecte les infos client (fiches) + a les accès WordPress. Admin WP sur les sites (compte `camillefauveau.service@gmail.com` ou `camille`).
- **Seb / Martin** = valide, contrôle, pilote. C'est lui qui a le compte Google **martinmorebkk@gmail.com** (voir §5).
- **L'IA (moi)** = analyse, prépare les mots-clés / titres / métas / corrections **au mot près**, rédige les prompts.
- **L'extension « Claude pour Chrome »** = applique les changements dans le navigateur (voir §4).

---

## 2. ⚖️ LA RÈGLE D'OR — LOI HOGUET (à respecter TOUJOURS)

La quasi-totalité des clients sont **SANS Carte G** (carte professionnelle d'agent immobilier).
→ Le site ne doit **JAMAIS** contenir ces mots (ils sont réservés aux détenteurs de la Carte G) :
**« gestion » · « gestionnaire » · « gérer » · « gestion locative » · « gestion Airbnb » · « mandat de gestion »**.

**Remplacements autorisés :** prise en charge · coordination · suivi · accompagnement · optimisation · pilotage · prestataire · exploitation · co-hôte.

**Vocabulaire autorisé à privilégier :** conciergerie · location courte durée · location saisonnière · location moyenne durée · sous-location · loyer garanti (pour la sous-location).

**Vérification finale obligatoire :** faire **Ctrl+F « gestion »** PUIS **Ctrl+F « gérer »** (séparément — l'un ne trouve pas l'autre) sur **chaque page publique** = **0 résultat**.

**Où se cachent les « gestion / gérer » :** le footer (global), les faux témoignages, les sur-titres de section, les titres de cartes (« Gestion du Linge »), les cartes de valeurs, les FAQ, les pages légales, l'intérieur du JSON-LD, et surtout **les articles de blog**.

**Exceptions tolérées (à signaler, pas bloquantes) :**
- Les **chaînes du plugin cookies** (Complianz : « Gérer le consentement », « Gérez vos réglages »…) = ce sont des textes du plugin, pas de l'éditorial, sur des pages en noindex → risque nul (vocabulaire cookies, pas immobilier). Modifiables seulement via Complianz Premium ou Loco Translate. On les laisse en général.
- « suggestions » contient « gestion » en sous-chaîne mais n'est pas le mot interdit (par prudence on peut mettre « recommandations »).

**Cas BELGE (ex : MOSA à Liège) :** pas la Loi Hoguet française, MAIS la Belgique a l'**IPI** (agent immobilier) qui encadre aussi la « gestion locative » → **on garde le même réflexe par prudence** (éviter « gestion locative », « property management » en anglais → dire « conciergerie / concierge service »).

---

## 3. LE PROCESSUS PAR SITE (résumé)

1. **Cadrage** (fiche client) : URL + accès WP · **Carte G oui/non** · ville/zone **confirmée par le client** · activité (conciergerie / sous-location / moyenne durée) · prestation (SEO complet ou SEO local seul) · nom exact de la marque · téléphone + adresse (NAP) · réseaux sociaux réels · compte Google (Gmail) du client · fiche Google Business existe/à créer.
2. **Audit** (extension, LECTURE SEULE) → rapport page par page.
3. **Analyse** (IA) : mots-clés, titres/métas, structure Hn, liste des corrections exactes.
4. **Application** (extension, mode autonome) → correction + récap.
5. **Google** : Search Console (propriété + sitemap + indexation) + Site Kit + fiche Google Business.
6. **Vérif finale** + passer le site en « Terminé » dans le tableau de bord.

**Périmètre :** ✅ inclus = SEO (mots-clés, titres/métas, Hn, vocabulaire, ALT, schema, technique, Search Console, Site Kit, Google Business). ❌ NON inclus = **rédaction des articles de blog** (= au client), création de design/contenu éditorial, vrais avis. On **optimise** l'existant.

---

## 4. ⭐ L'OUTIL : « CLAUDE POUR CHROME » (l'extension qui applique)

- C'est une **extension de navigateur** (produit claude.ai) qui **pilote le vrai Chrome** de l'utilisateur, sur l'**onglet actif**. Elle peut **lire ET modifier** le site (contrairement à une IA classique qui ne peut souvent pas lire le site à cause du blocage 403 Hostinger).
- **Toujours ouvrir `.../wp-admin` connecté au premier plan** avant de coller un prompt.
- Sur Elementor c'est **LENT** → normal, la laisser tourner en autonomie.
- On travaille en **2 temps** (méthode la plus sûre, zéro erreur) :
  1. **PROMPT D'AUDIT (lecture seule)** → elle explore tout et renvoie un rapport. On le colle à l'IA.
  2. **PROMPT DE CORRECTION (au mot près)** → l'IA le prépare à partir du rapport réel ; l'extension applique tout en autonomie et fait un récap final.
- Variante rapide : **MÉGA PROMPT one-shot** (audit + correction + Yoast + Search Console en une passe) quand on veut aller vite et qu'on fait confiance.
- ⚠️ Certaines actions ne peuvent être faites QUE par l'humain (l'extension s'arrête et le signale) : **« Se connecter avec Google » (OAuth), la validation passkey/2FA, l'ajout d'un propriétaire sur une ressource Google**. → C'est à Seb de cliquer.

**⚠️ Piège Chrome :** la **traduction automatique de Chrome** sur `/wp-admin` (interface en anglais) affiche des libellés faux et peut faire **planter** l'interface Yoast/éditeur. → désactiver la traduction, ou passer la langue du profil WP en français.

---

## 5. COMPTES GOOGLE & SÉCURITÉ

- **Search Console + Site Kit** : on les crée/connecte partout sous le compte agence **martinmorebkk@gmail.com** (celui de Seb). C'est lui le propriétaire validé de toutes les propriétés.
- **Transfert de propriété au client** : possible seulement si le client a un **vrai compte Google (Gmail)**. Si son email est **Outlook/Hotmail** (ex : Léandro `luciesimonian@outlook.fr`) ou une adresse de domaine non-Google → **impossible**, on laisse sous le compte agence.
- **Mots de passe WordPress** : **jamais stockés** dans les docs. Toujours « à demander à Camille ».
- **Quota Google d'indexation** : ~10 URL/jour **par compte** (pas par site). Si « Quota dépassé » → relancer le lendemain. Pas grave : le sitemap fait la découverte de toute façon.
- **Ne jamais accepter d'offres payantes** dans Site Kit / Google Business (crédit Ads 400 €, Workspace, AdSense, Reader Revenue) → toujours « Peut-être plus tard ».

---

## 6. LA STRUCTURE SEO D'UNE PAGE (rappel technique)

- **1 seul H1 par page** = le grand titre du héros, **avec mot-clé + ville**. ⚠️ Piège fréquent : le héros est en H2 (ou H6) par défaut, la page n'a AUCUN H1 → le passer en H1.
- **H2** = sections · **H3** = sous-blocs/cartes.
- **Titre SEO Yoast** : 50-60 caractères, mot-clé + ville au début, finit par « | [Marque] ».
- **Méta description Yoast** : **120-155 caractères** (barre verte Yoast ; le français accentué compte plus large → viser ~150). Accroche + ville + service + appel à l'action.
- **Mot-clé principal (focus keyphrase)** renseigné dans Yoast sur CHAQUE page (souvent oublié = score 0).
- **ALT** sur toutes les images (description + ville).
- **Maillage interne** : pages villes ↔ services/tarifs/contact ; pas de page orpheline.
- **Slug** (« limace » dans Yoast) : court, propre ; ne pas y toucher s'il est déjà bon (changer un slug = risque de 404 → nécessite une redirection 301).

---

## 7. SEO TECHNIQUE + GOOGLE (checklist de base à chaque site)

- **Yoast SEO installé/activé** (config manuelle, pas l'assistant payant). Si absent → l'installer (c'est du « SEO complet »).
- **Langue du site = Français** (Réglages → Général → `fr_FR`) → `og:locale = fr_FR`. (Belgique : `fr_FR` ok, ou en_GB pour l'EN.)
- **Fuseau horaire = Europe/Paris** (souvent laissé sur UTC+0).
- **Indexation ON** : Réglages → Lecture, case « décourager les moteurs » **décochée** (⚠️ un site neuf est souvent bloqué).
- **Permaliens** = « Nom de l'article » (`/%postname%/`).
- **Yoast → noindex** : archives d'auteur (⚠️ elles exposent souvent le login/e-mail admin dans l'URL `/author/…`), catégories, étiquettes ; rediriger les pièces jointes. → sitemap propre.
- **Pages légales** (mentions légales, confidentialité, cookies, CGU/CGV) → **noindex**.
- **Yoast → Représentation du site** : type Organisation, nom de la marque, **logo**, (téléphone = Yoast Premium seulement → sinon dans le schema).
- **Sitemap Yoast** : `[site]/sitemap_index.xml` (existe une fois Yoast installé).
- **Schema LocalBusiness** : Yoast gratuit ne met pas le téléphone → on ajoute un **bloc JSON-LD LocalBusiness complet à part** via **Elementor → Réglages du site → Code personnalisé (Custom Code)**, emplacement `<head>`, « Dans tout le site ». (Cohabite avec le schema Yoast, `@id` distinct.) Voir modèle §9.
- **Search Console** : `search.google.com/search-console` → ⚠️ VÉRIFIER qu'on est sur la BONNE propriété → si absente : « Ajouter une propriété » → **« PRÉFIXE DE L'URL »** → `https://[site]` → méthode **« Balise HTML »** → copier le code → WordPress → **Yoast → Réglages → « Connexions du site » → champ Google** → coller → Enregistrer → revenir → « Valider ». Puis **Sitemaps** → envoyer `sitemap_index.xml`. Puis **Inspection de l'URL** → chaque page → « Demander une indexation ».
- **Site Kit by Google** (plugin WordPress) : Extensions → installer/activer → « Se connecter avec Google » (**humain**, compte martinmorebkk@gmail.com) → connecte Search Console (+ souvent PageSpeed / Analytics GA4 en bonus, on garde). Objectif du site = « Fournir des services ».
- **Fiche Google Business** : catégorie **« Conciergerie privée »** (la seule que Google propose ; « Service de conciergerie » n'existe pas). Adresse masquée (service à domicile / zone desservie) si pas d'adresse commerciale. NAP identique au site. Zone = communes confirmées. **La vérification (souvent vidéo) + les photos = TOUJOURS côté client.**

---

## 8. LES MOTS-CLÉS (comment on les choisit)

- **Formule** : activité + ville → « conciergerie [ville] », « conciergerie Airbnb [ville] ».
- **Prioriser les villes à trafic** (grandes villes / stations touristiques) plutôt que les petits villages (qui servent la fiche Google, pas le trafic). Ex : Rouen (590/mois) > Louviers (~0).
- Mots-clés génériques forts : « conciergerie Airbnb » (~5400/mois), « tarif conciergerie Airbnb » (~480), « conciergerie [grande ville] ».
- Un **mot-clé principal par page**, renseigné dans Yoast.
- **⚠️ LA ZONE = uniquement les communes RÉELLEMENT desservies, CONFIRMÉES par le client.** Ne jamais ajouter une ville voisine plus recherchée « parce qu'elle a du volume ». (Erreur vécue : Valse de Lin → on avait mis La Baule/Guérande, la cliente ne les dessert pas → tout refait. Voir §11.)

---

## 9. MODÈLE DE SCHEMA LocalBusiness (à coller dans Elementor → Code personnalisé, `<head>`)

```
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": ["ProfessionalService","LocalBusiness"],
  "@id": "https://[SITE]/#business",
  "name": "[MARQUE]",
  "description": "Conciergerie ... à [VILLE] et [ZONE].",
  "url": "https://[SITE]",
  "email": "[EMAIL]",
  "telephone": "+33[NUMERO]",
  "image": "https://[SITE]/wp-content/uploads/[LOGO].png",
  "address": { "@type": "PostalAddress", "addressLocality": "[VILLE]", "postalCode": "[CP]", "addressRegion": "[REGION]", "addressCountry": "FR" },
  "areaServed": [ {"@type":"City","name":"[VILLE1]"}, {"@type":"City","name":"[VILLE2]"} ],
  "priceRange": "€€",
  "knowsAbout": ["Conciergerie Airbnb","Location courte durée","Location saisonnière"]
}
</script>
```
> ⚠️ Vérifier que l'URL du champ `image` renvoie bien un 200 (sinon mettre le vrai chemin `/uploads/AAAA/MM/...`).

---

## 10. PROMPTS RÉUTILISABLES

### 10.a — PROMPT D'AUDIT (lecture seule)
```
Tu agis dans mon navigateur sur [SITE] (WordPress + Elementor).
MODE LECTURE SEULE : tu n'enregistres, ne modifies, ne publies, ne supprimes RIEN. Tu OBSERVES et tu fais un rapport.
Fais l'inventaire complet pour préparer un SEO (conciergerie, sans Carte G, zone [ZONE]). Donne-moi, structuré :
1) TOUTES les pages (menu + sitemap) : titre, URL/slug, statut + les articles.
2) Par page : H1 exact (0/plusieurs = signale), H2/H3, et si plugin SEO présent : Titre SEO + Méta + mot-clé. Sinon signale l'absence.
3) Plugin SEO installé (Yoast/RankMath) ? Constructeur ? Thème ?
4) VOCABULAIRE : occurrences « gestion / gestionnaire / gérer » — page, élément, phrase exacte (Ctrl+F « gestion » ET « gérer » séparément).
5) IMAGES sans ALT (où). Photos de stock / hors zone ?
6) LIENS : boutons « # », réseaux sociaux vides/faux, lien téléphone (format), pages orphelines.
7) AVIS : présents ? réels ou inventés (style template) ?
8) FAUTES + textes de template oubliés + incohérences de marque.
9) RÉGLAGES : langue, indexation (Réglages→Lecture), permaliens, sitemap. Search Console déjà là ?
10) ZONE : communes citées actuellement.
Rends-moi TOUT ça page par page. NE MODIFIE RIEN.
```

### 10.b — SQUELETTE DU PROMPT DE CORRECTION (l'IA le remplit au mot près depuis l'audit)
```
Tu es mon assistant SEO. Tu agis sur [SITE]/wp-admin (WordPress + Elementor + Yoast), je suis connecté.
Applique EXACTEMENT les corrections ci-dessous EN AUTONOMIE, enregistre au fur et à mesure, ne casse pas le design,
ne touche QU'À ce qui est listé. Purge le cache à la fin. Récap page par page.
RÈGLE (sans Carte G) : zéro « gestion / gérer / gestionnaire ». Remplacements : coordination · suivi · prise en charge · exploitation.
A — Yoast + réglages (installer si absent ; noindex auteur/catégorie/tag ; Org + logo ; fuseau Paris ; langue fr).
B — Titre + Méta + Mot-clé par page (LISTE EXACTE fournie).
C — H1 : 1 seul par page, avec ville (LISTE des corrections).
D — Loi Hoguet : remplacements EXACTS « avant → après » (LISTE).
E — Fautes / textes cassés (LISTE).
F — Images : remplir les ALT vides (description + ville). Signaler les photos hors zone.
G — Liens : tel:+33… ; réseaux (laisser « # » si pas de vraie URL) ; maillage.
H — Schema LocalBusiness (bloc JSON-LD dans Elementor → Code personnalisé, <head>).
I — Search Console : créer propriété (préfixe URL) + valider via Yoast + sitemap_index.xml + demander indexation.
VÉRIF FINALE : Ctrl+F « gestion »/« gérer » = 0 · 1 H1/page · titres/métas verts · légales noindex · schema présent. Récap.
```

### 10.c — PROMPT SITE KIT
```
Tu agis sur [SITE]/wp-admin, je suis connecté.
- Extensions → « Site Kit by Google » → Installer/Activer (ou activer s'il est déjà là).
- Kit de site → Démarrer la configuration → « Se connecter avec Google » → compte martinmorebkk@gmail.com.
  Si Google demande une validation/passkey → ARRÊTE-TOI, je le fais.
- Objectif du site → « Fournir des services ». Ignore les encarts promo (« Peut-être plus tard »). Aucune offre payante.
Récap : Search Console / Analytics / PageSpeed connectés ?
```

### 10.d — PROMPT FICHE GOOGLE BUSINESS
```
Tu agis dans mon navigateur. Crée une fiche Google Business pour [MARQUE]. Fais-le en autonomie et ARRÊTE-TOI
aux étapes humaines (connexion compte, vérification). Récap.
- business.google.com → « Ajouter une entreprise » → Nom : [MARQUE].
- Catégorie : « Conciergerie privée ». Établissement visitable ? → NON (service à domicile, adresse masquée).
- Zone desservie : [communes confirmées]. Tél : [07…]. Site : https://[SITE]. Horaires : [ … ].
- Description : [texte conforme, sans « gestion »].
- Lance la validation MAIS ne tente aucune fausse vérif : si Google demande vidéo/courrier, ARRÊTE-TOI et signale-le
  (c'est au client). N'accepte aucune offre payante.
```

---

## 11. 🧰 LEÇONS DE TERRAIN (les pièges qui font gagner un temps fou)

**Elementor :**
- Modifier un texte = **clic UNE fois** sur le bloc → panneau de gauche (onglet « Contenu »). PAS de double-clic.
- Blocs « Icon Box » (JKit/ElementsKit) : titre + description = champs à gauche.
- Changer une balise H1/H2/H3 : clique le titre → réglage **« Balise HTML »**.
- **Footer / Header = modèles globaux** : Elementor → **Theme Builder** → édités UNE fois pour tout le site.
- **Schema** = via **Elementor → Code personnalisé** (Elementor Pro), `<head>`, tout le site.
- **⚠️ Piège Elementor↔Yoast** : Yoast ne « voit » pas les widgets Heading/Image (reçus en texte brut) ni un `alt` vide de widget qui **écrase** celui de la médiathèque. → si un assessment « image / H2 / ALT » reste rouge à tort, placer le `<h2>`/`<img>` **DANS un widget Texte** (rendu public identique). Purger le cache Elementor pour voir les ALT.

**Yoast :**
- Ouvrir la page en éditeur → icône « Y » en haut à droite → « Apparence de recherche » → Titre + Méta + Mot-clé.
- « Limace » = slug. Visage rouge/orange sur pages Elementor = normal, ce qui compte = Titre + Méta verts.
- Renseigner le **mot-clé (focus keyphrase)** partout (souvent vide = score 0).

**Loi Hoguet :** Ctrl+F « gestion » ET « gérer » séparément, sur chaque page. Ils se cachent dans footer, faux avis, sur-titres, titres de cartes, FAQ, JSON-LD, articles.

**Zone géographique :** **uniquement les communes confirmées par le client.** En cas de doute → confirmer AVANT (H1, titres, fiche Google). Ne pas ajouter une ville voisine « à volume ». Retirer les villes hors zone même si elles sont déjà sur le site (ex : Dax retiré chez Ongi Etorri).

**Search Console :** toujours vérifier qu'on est sur la **BONNE propriété** (piège : agir sur le site d'un autre client). Quota ~10 URL/jour/compte. « Impossible de récupérer le sitemap » juste après l'envoi = **normal**, revérifier 24-48 h.

**Faux avis / témoignages inventés** (sans nom/date, style template) = **risque légal (DGCCRF)** → ne jamais les inventer, les masquer en attendant de vrais avis.

**Numéros de téléphone :** format `tel:+33XXXXXXXXX` (sans espaces encodés `%20`). ⚠️ Vérifier qu'un mauvais numéro (ex : n° d'agent immobilier d'une autre activité) ne traîne pas, y compris **dans la méta Yoast** (cas Les Jardins : 06 IAD dans la méta Contact, public sur Google).

**Divers :** virer les `**` markdown parasites dans les titres ; catégorie « Uncategorized » à renommer ; nom public d'auteur = le vrai nom (jamais un e-mail) ; désactiver la traduction auto de Chrome sur wp-admin.

---

## 12. 🗂️ LES 8 SITES — TOUS FINIS À 100% (au 26/09/2026)

**1. D'Or Tranquille — dortranquille.fr (Les 2 Alpes) — ✅ FINI (100%)**
Conciergerie, sans Carte G. SEO on-page + technique + fiche Google Business faits.

**2. Valse de Lin — valsedelin.fr (Sainte-Reine-de-Bretagne) — ✅ FINI (100%)**
Karine Riou, SASU, sans Carte G. **Zone : la Brière, Pontchâteau, La Roche-Bernard.** Tél 06 10 90 52 09 · accueil@valsedelin.fr. SEO on-page complet + fiche Google Business créée (catégorie « Conciergerie privée ») + Search Console.

**3. Léandro Conciergerie — leandroconciergerie.fr (Grenoble) — ✅ FINI (100%)**
Lucie & Jonathan, SAS, sans Carte G. Tél 07 75 67 42 16. **Zone : Grenoble, Grésivaudan, Voiron, Chambéry, stations — JAMAIS Vercors ni Aix-les-Bains.** SEO local + **3 pages locales créées et 100% vertes** (/conciergerie-chambery/, /conciergerie-voiron/, /conciergerie-gresivaudan/) + Search Console + Site Kit + fiche Google Business créée.

**4. Ongi Etorri Conciergerie — ongietorriconciergerie.fr (Hendaye) — ✅ FINI (100%)**
Marie Lefèvre, sans Carte G. **Zone 2 niveaux : moyenne durée** (Hendaye, Urrugne, Ciboure, Saint-Jean-de-Luz) **+ courte durée Landes** (Capbreton, Ondres, Seignosse). Tél 06 02 20 47 30. Yoast installé, Loi Hoguet 0/0, 28 ALT, schema LocalBusiness, Search Console + Site Kit connectés.

**5. MOSA Conciergerie — mosaconciergerie.be (Liège) — ✅ FINI (100%) — client BELGE**
Maxime Rafétin. **Zone : Liège, Huy, Namur.** Site bilingue FR/EN. Yoast installé, vocabulaire conforme (concierge service), schema LocalBusiness, Search Console + Site Kit connectés.

**6. Les Clefs du Rivage 85 — lesclefsdurivage85.fr (Saint-Jean-de-Monts / Vendée) — ✅ FINI (100%)**
Isabelle Fonteneau, sans Carte G. Zone : Saint-Jean-de-Monts, Notre-Dame-de-Monts, Saint-Hilaire-de-Riez, Saint-Gilles-Croix-de-Vie, Challans. Yoast installé, Loi Hoguet 0/0, 94 ALT, schema LocalBusiness, Search Console.

**7. Le Nid Mousin — lenidmousin.com (Folles / Haute-Vienne) — ✅ FINI (100%)**
Pauline & Jason, conciergerie + sous-location, sans Carte G. Zone : Folles, Haute-Vienne, Limousin, Limoges. Yoast installé, Loi Hoguet 0/0, schema LocalBusiness, Search Console + Site Kit connecté (+ Analytics GA4).

**8. Les Jardins Seine Eure — lesjardinsseineeure.fr (Louviers / Normandie) — ✅ FINI (100%)**
Loubna George, sans Carte G. **Zone : Louviers, Vernon, Évreux, Rouen, Giverny, Les Andelys (40 km).** SEO local : mots-clés Yoast, « conciergerie Airbnb » ajouté, Loi Hoguet 0/0, FAQPage sur /faq/, Eure/Normandie maillées, 5 articles publiés, Search Console + Site Kit connectés.

---

## 13. TABLEAU DE SUIVI (pour Camille)
Il existe un petit site interne (`index.html`) où Camille ajoute chaque site : nom, URL, activité, ville, **Carte G**, **prestation** (SEO complet / local), **zone confirmée oui/à confirmer**, statut, e-mail, **téléphone**, **compte Google**, **fiche Google Business**, adresse, réseaux, note, fichiers. Données stockées dans le navigateur (localStorage) — donc **pas partagé entre 2 ordis** (chantier futur si on veut une vraie base partagée).

## 14. INFOS À DEMANDER POUR CHAQUE NOUVEAU SITE
URL + accès WP · **Carte G oui/non** · **zone exacte confirmée par le client** · activité (conciergerie/sous-location/moyenne durée) · **prestation (SEO complet ou local)** · nom exact de la marque · **téléphone** (le bon !) + adresse (NAP) · **URL réelles Facebook/Instagram** · **compte Gmail** du client (pour Site Kit) · fiche Google Business (existe/à créer) · décisions témoignages. **Ne jamais deviner : demander si ça manque. Mot de passe WP jamais stocké → demander à Camille.**
```
```
FIN DU DOCUMENT — tout ce qu'il faut pour reprendre au même niveau.
```
