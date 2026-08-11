# Le Nid Mousin — MÉGA PROMPT one-shot (audit + corrections + Yoast + Search Console)

> Client : Pauline & Jason · lenidmousin.com · Folles (87250) / Haute-Vienne / Limousin.
> Conciergerie **+ sous-location**, **sans Carte G**. Site WordPress + Elementor. E-mail : hello@lenidmousin.com.
> ⚠️ Mot de passe WP à demander à Camille (jamais stocké ici). Zone à confirmer avec le client si doute.
>
> À coller UNE fois dans l'extension, onglet **lenidmousin.com/wp-admin connecté**, mode autonome.

```
Tu es mon assistant SEO. Tu agis dans mon navigateur (WordPress + Elementor + Yoast + Google Search Console),
je suis connecté à /wp-admin et à Search Console. Fais TOUT ce qui suit EN AUTONOMIE, page par page,
enregistre au fur et à mesure, ne casse pas le design, et donne-moi un RÉCAP FINAL détaillé.

########## CONTEXTE ##########
- Site : lenidmousin.com        - Client/marque : Le Nid Mousin (Pauline & Jason)
- Activité : conciergerie ET sous-location — Carte G : NON
- Zone : Folles (87250), Haute-Vienne, Limousin (+ alentours réellement desservis)
- E-mail : hello@lenidmousin.com   (Téléphone : garde celui déjà présent sur le site, n'en invente aucun)

########## RÈGLE ABSOLUE (Loi Hoguet — Carte G = NON) ##########
Zéro « gestion » / « gestionnaire » / « gérer » / « gestion locative » / « gestion Airbnb » nulle part
(contenu, footer, avis, cartes, sur-titres, pages légales, FAQ, schema).
Remplace par : prise en charge · coordination · suivi · accompagnement · optimisation · pilotage · prestataire.
Vocabulaire AUTORISÉ à privilégier : conciergerie · location courte durée · location saisonnière ·
sous-location · loyer garanti (pour la partie sous-location).
⚠️ Fais Ctrl+F « gestion » ET « gérer » séparément sur CHAQUE page (l'un ne trouve pas l'autre).

########## MÉTHODE (mémorise) ##########
- Elementor : modifier un texte = clic UNE fois sur le bloc → panneau de gauche (Contenu). Pas de double-clic.
- Blocs JKit/ElementsKit « Icon Box » : titre + description = champs à gauche.
- Changer une balise : clique le titre → « Balise HTML » → H1/H2/H3.
- Footer/Header = Theme Builder (édités une seule fois).
- Piège Elementor↔Yoast : Yoast ne « voit » pas toujours les widgets Heading/Image → si un assessment
  « image / sous-titre / mot-clé » reste rouge à tort, place le <h2>/<img> DANS un widget Texte (rendu identique).
- Yoast : page en éditeur normal → icône « Y » en haut à droite → « Apparence de recherche » →
  Titre + Méta (120-155 caractères = barre VERTE) + Mot-clé principal.

===== ÉTAPE 0 — RÉGLAGES GLOBAUX =====
- Settings → General → Site Language = Français (→ og:locale fr_FR).
- Settings → Reading → décoche « Discourage search engines ».
- Settings → Permalinks → « Post name ».
- Vérifie que Yoast SEO est installé/actif (sinon installe-le).

===== ÉTAPE 1 — AUDIT + CORRECTION, PAGE PAR PAGE =====
Pour CHAQUE page (menu + sitemap), LIS la page puis CORRIGE :
- Remplace tout « gestion » / « gérer » (voir règle).
- 1 SEUL H1 par page : si le titre du héros est en H2, passe-le en H1 (avec mot-clé + zone). Signale les H1 corrigés.
- Enlève les « ** » parasites dans les titres.
- Remplis les ALT VIDES (sujet + zone, ex : « conciergerie Airbnb Haute-Vienne », « ménage location courte durée Limousin »).
- Liens : boutons « # » → page Contact ; icônes réseaux sans lien → vraies URL (ou signale) ; tel: → format tel:+33XXXXXXXXX.
- Footer : services cliquables vers /services/, villes/zones vers /contact/ ; ajoute les pages orphelines.
- Corrige les fautes visibles (doubles espaces, casse, « English speacking » → « speaking », etc.).
- FAUX AVIS (sans nom/date, style template) : NE les invente jamais → MASQUE la section et signale-les.

===== ÉTAPE 2 — YOAST : TITRE + MÉTA + MOT-CLÉ (par page, applique ce modèle) =====
Mot-clé = « conciergerie » + zone (varie selon la page) : conciergerie Haute-Vienne / conciergerie Limousin /
conciergerie Folles / sous-location Haute-Vienne / loyer garanti Limousin.
Titre (55-60 car.) : commence par le mot-clé, finit par « | Le Nid Mousin ».
Méta (120-155 car.) : accroche + zone (Folles, Haute-Vienne, Limousin) + service + appel à l'action. Barre VERTE.
Exemples à suivre :
- ACCUEIL : Titre « Conciergerie Airbnb en Haute-Vienne & Limousin | Le Nid Mousin » |
  Méta « Le Nid Mousin, votre conciergerie de location courte durée à Folles, en Haute-Vienne et dans le Limousin : accueil voyageurs, ménage, linge et optimisation de vos annonces. » | Mot-clé « conciergerie Haute-Vienne »
- SERVICES : Titre « Services de conciergerie en Haute-Vienne | Le Nid Mousin » |
  Méta « Ménage, accueil voyageurs, linge et optimisation de vos annonces : tous les services de conciergerie du Nid Mousin à Folles, en Haute-Vienne et dans le Limousin. » | Mot-clé « services de conciergerie Haute-Vienne »
Applique le MÊME modèle à toutes les autres pages (À propos, Contact, Blog, sous-location, etc.) en adaptant la zone.

===== ÉTAPE 3 — RÉGLAGES =====
- Passe les pages légales (mentions légales, politique de confidentialité) en NOINDEX (Yoast → Avancé).
- Utilisateurs → profil auteur : nom public = « Le Nid Mousin » ou « Pauline & Jason » (jamais une adresse e-mail).

===== ÉTAPE 4 — GOOGLE SEARCH CONSOLE =====
- Ouvre search.google.com/search-console. VÉRIFIE d'abord que tu es sur la BONNE propriété (lenidmousin.com).
- Si la propriété N'EXISTE PAS : « Ajouter une propriété » → « PRÉFIXE DE L'URL » → https://lenidmousin.com →
  « Balise HTML » → copie le code → wp-admin → Yoast → Réglages → « Connexions du site » → champ Google →
  colle → Enregistre → reviens → « Valider ».
- Sitemaps → envoie « sitemap_index.xml ».
- Inspection de l'URL → pour CHAQUE page → « Demander une indexation » (si quota dépassé, signale-le, pas grave).

===== VÉRIFICATION FINALE =====
Sur chaque page publiée : Ctrl+F « gestion » ET « gérer » = 0 · 1 seul H1 · titres/métas verts · légales en noindex.
Donne-moi le récap page par page + la liste des faux avis / liens cassés / points à trancher (dont la zone exacte à confirmer).
```

## Notes
- **Téléphone** manquant sur la fiche → l'extension garde celui du site, on n'invente rien. À récupérer pour la fiche Google plus tard.
- **Zone** : la note Camille dit « Folles / Haute-Vienne / Limousin ». Si Pauline & Jason desservent des communes précises
  (Bellac, Limoges…), les confirmer AVANT d'en faire des mots-clés (leçon zone Valse de Lin).
- **Fiche Google Business** + **Site Kit** : à faire après, comme pour les autres (fiche = vérif vidéo côté client).
