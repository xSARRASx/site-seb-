# 🚀 MÉGA PROMPT SEO — one-shot (tout en une passe)

> **Principe :** l'extension AUDITE chaque page ELLE-MÊME et CORRIGE dans la foulée, applique les
> titres/métas Yoast, fait la Search Console — le tout en autonomie, en un seul prompt.
> **Claude remplit les `[CROCHETS]`** (à partir du formulaire + de la fiche du site) ; le client colle UNE fois.
>
> Onglet **[URL]/wp-admin connecté** au premier plan + extension Claude pour Chrome active. Sur Elementor c'est lent → normal.

```
Tu es mon assistant SEO. Tu agis dans mon navigateur (WordPress + Elementor + Yoast + Google Search Console),
je suis connecté à /wp-admin et à Search Console. Fais TOUT ce qui suit EN AUTONOMIE, page par page,
enregistre au fur et à mesure, ne casse pas le design, et donne-moi un RÉCAP FINAL détaillé.

########## CONTEXTE ##########
- Site : [URL]        - Client/marque : [NOM]
- Activité : conciergerie (ou sous-location) — Carte G : [OUI/NON]
- Ville/zone : [VILLE + communes voisines]
- Tél : [TEL]  ·  E-mail : [EMAIL]

########## RÈGLE ABSOLUE (Loi Hoguet, si Carte G = NON) ##########
Zéro « gestion » / « gestionnaire » / « gérer » nulle part (contenu, footer, avis, cartes, pages légales).
Remplace par : prise en charge · coordination · suivi · accompagnement · optimisation.

########## MÉTHODE (mémorise) ##########
- Elementor : modifier un texte = clic UNE fois sur le bloc → panneau de gauche (Contenu). Pas de double-clic.
- Blocs JKit « Icon Box » : titre + description = champs à gauche.
- Changer une balise : clique le titre → « Balise HTML » → H1/H2/H3.
- Footer/Header = Theme Builder (édités une seule fois).
- Yoast : page en éditeur normal → icône « Y » en haut à droite → « Apparence de recherche » → Titre + Méta (120-155 car.) + Mot-clé.

===== ÉTAPE 0 — RÉGLAGES GLOBAUX =====
- Settings → General → Site Language = Français (→ og:locale fr_FR).
- Settings → Reading → décoche « Discourage search engines ».
- Settings → Permalinks → « Post name ».
- Vérifie Yoast SEO installé/actif.

===== ÉTAPE 1 — AUDIT + CORRECTION, PAGE PAR PAGE =====
Pour CHAQUE page (menu + sitemap), LIS la page puis CORRIGE :
- Remplace tout « gestion » / « gérer » (voir règle).
- 1 SEUL H1 par page : si le titre du héros est en H2, passe-le en H1 (avec mot-clé + ville). Signale les H1 manquants corrigés.
- Enlève les « ** » parasites dans les titres.
- Remplis les attributs ALT VIDES (sujet + ville, ex « ménage location courte durée [VILLE] »).
- Liens : boutons « # » → page Contact ; icônes réseaux sans lien → mets les vraies URL (ou signale) ; tel: → format tel:+33XXXXXXXXX.
- Footer : rends les services cliquables vers /services/, les villes vers /contact/ ; ajoute les pages orphelines au footer.
- Corrige les fautes visibles (ex : « English speacking » → « English speaking », doubles espaces, casse).
- FAUX AVIS (noms/dates absents, style template) : NE les invente jamais → MASQUE la section et signale-les.

===== ÉTAPE 2 — YOAST : TITRE + MÉTA + MOT-CLÉ (par page) =====
[REMPLIR PAR CLAUDE — une entrée par page :
 [PAGE] : Titre SEO « … » | Méta « … » (120-155 car.) | Mot-clé « … »]

===== ÉTAPE 3 — RÉGLAGES =====
- Passe les pages légales (mentions légales, politique de confidentialité) en NOINDEX (Yoast → Avancé).
- Utilisateurs → profil auteur : nom public = « [PRÉNOM NOM] » (jamais une adresse e-mail).

===== ÉTAPE 4 — GOOGLE SEARCH CONSOLE =====
- Ouvre search.google.com/search-console. Si la propriété [URL] N'EXISTE PAS :
  « Ajouter une propriété » → « PRÉFIXE DE L'URL » → https://[URL] → « Balise HTML » → copie le code →
  wp-admin → Yoast → Réglages → « Connexions du site » → champ Google → colle → Enregistre → reviens → « Valider ».
- Sitemaps → envoie « sitemap_index.xml ».
- Inspection de l'URL → pour CHAQUE page → « Demander une indexation ».

===== VÉRIFICATION FINALE =====
Sur chaque page publiée : Ctrl+F « gestion » ET « gérer » = 0 · 1 seul H1 · titres/métas verts · légales en noindex.
Donne-moi le récap page par page + la liste des faux avis / liens cassés / points à trancher.
```

---

## Ce que Claude remplit avant de te l'envoyer
- Le **CONTEXTE** (URL, nom, Carte G, ville, tél, e-mail).
- L'**ÉTAPE 2** : Titre + Méta + Mot-clé pour **chaque page** (basé sur les mots-clés de la zone).
- Le nom public d'auteur (ÉTAPE 3).

## Ce qui reste TOUJOURS à la main (hors prompt)
- **Fiche Google Business** : création (prompt séparé) + **vérification vidéo** + **photos** = côté client.
- **Vrais avis**, **articles de blog**, **pages locales par ville** = côté client / projet à part.
