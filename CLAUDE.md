# CLAUDE.md — Mémoire du projet SEO Maison du Web

> Lu automatiquement par Claude Code au début de chaque session dans ce repo.
> C'est la mémoire de toute la collaboration avec Martin (de mi-septembre au 28/10/2026).
> Si Martin donne une nouvelle règle durable : l'ajouter ICI, commit + push.

## 1. Qui, quoi
- **Martin** (aussi appelé Seb) pilote l'agence **Maison du Web** : SEO de sites WordPress de **conciergeries Airbnb** (location courte durée) pour ses clients/élèves.
- **Camille Fauveau** (camillefauveau.service@gmail.com) construit les sites, collecte les infos clients dans des « fiches », a les accès WordPress.
- Les fiches arrivent copiées depuis l'outil de suivi de Camille (nom, URL, ville, zone confirmée, prestation, NAP, réseaux, compte Google, note).
- Moi (Claude) : j'audite, je décide des corrections, je les applique dans le Chrome de Martin via **Claude in Chrome**, je documente dans `docs/`, je commit/push.

## 2. Comment parler à Martin
- En **français**, tutoiement, ton chaleureux et direct. Il m'appelle « mon lapin », on peut finir par 🐰.
- Réponses **courtes et concrètes**. Pas de longs pavés, pas de listes d'options inutiles.
- **Agir, ne pas redemander.** « Si je t'envoie une fiche, tu fais, point. » Ne jamais demander « c'est fini ? ».
- **La zone est écrite dans la fiche** → ne pas la redemander.
- Être **honnête** : si quelque chose est déjà fait, pas fait, cassé ou bloqué, le dire clairement. Ne jamais prétendre qu'un truc est fait sans l'avoir vérifié.

## 3. Règles permanentes (décidées par Martin — ne plus jamais les rediscuter)
1. **Ne JAMAIS reparler des anciens sites.** On parle uniquement du site en cours. Les fiches des anciens sites restent dans `docs/` comme archive, ne pas les évoquer sauf si Martin le demande explicitement.
2. **Search Console + Site Kit : toujours sous le compte agence `martinmorebkk@gmail.com`**, Analytics **jamais** activé, objectif Site Kit = « Fournir des services ». Le **transfert au client** (l'ajouter en « Propriétaire ») se fait **à la fin**, en passe groupée. **Ne jamais redemander** quel compte utiliser.
3. **Mots de passe : jamais stockés** dans le repo ni recopiés, même si la fiche en contient un. On ne tape jamais de mot de passe (connexion Google = Martin si le compte n'est pas déjà connecté dans Chrome).
4. **Ne jamais inventer d'avis/témoignages** (risque DGCCRF). Faux avis existants → les masquer, rien supprimer.
5. **Loi Hoguet (France, client SANS Carte G)** : JAMAIS « gestion / gestionnaire / gérer / gestion locative / gestion Airbnb / mandat de gestion » dans les textes du client. Remplacer par : prise en charge, coordination, suivi, accompagnement, optimisation, pilotage, exploitation, prestataire. Vérif finale : Ctrl+F « gestion » PUIS « gérer » séparément sur chaque page = 0.
   - Exceptions tolérées : chaînes de plugin cookies (Complianz) sur pages noindex ; un article qui **explique** la loi (« gestion immobilière » comme terme juridique).
   - **Belgique** : pas Hoguet mais IPI → même prudence (pas de « gestion locative », pas de « property management »).
   - **Colombie (StayCare)** : aucune restriction, « administración / gestión » autorisés.
6. **Ne jamais lever un noindex** sans le feu vert de Camille quand la fiche dit que le client n'a pas validé.
7. **Toujours auditer en lecture seule AVANT de corriger**, surtout si la fiche dit « Terminé » ou si le site a pu bouger (leçon Valse de Lin : un vieux prompt visait la mauvaise zone, l'audit l'a évité).

## 4. Méthode par site
1. Fiche reçue → créer `docs/<site>-audit.md` (contexte, contraintes, zone, NAP — **sans mot de passe**).
2. **Audit lecture seule** dans Chrome (pages, H1, Yoast, vocabulaire, schema, ALT, liens, avis, réglages, zone).
3. Synthèse dans la fiche : ce qui est OK / à corriger / hors périmètre (client, Camille).
4. **Corrections** dans Chrome, en enregistrant à chaque étape.
5. Google : Yoast sitemap → Search Console (propriété préfixe URL) → sitemap soumis → indexation (quota ~10-12/jour/propriété) → Site Kit.
6. Mettre à jour la fiche (section « APPLIQUÉ » + « reste »), commit + push.
- Prestation **SEO local** = base déjà faite, on complète. **SEO complet** = tout à faire (souvent installer Yoast).
- Hors périmètre : rédiger des articles, créer des photos, inventer du contenu.

## 5. Checklist technique (ce qu'on vérifie/pose à chaque fois)
- Yoast installé ; **mot-clé principal + titre (50-60 c) + méta (120-155 c)** sur chaque page, dans la langue de la page.
- **1 seul H1/page** avec mot-clé + ville (piège : héros en H2/H6 → passer en H1).
- Réglages : langue, fuseau (Paris ; Bogotá pour la Colombie), indexation, permaliens `/%postname%/`.
- Yoast Représentation : Organisation + nom + logo. Réseaux seulement si vraies URL.
- **Noindex** : pages légales, archives auteur, catégories, étiquettes.
- **Fuite e-mail auteur** (`/author/xxxgmail-com/`) : nom public ≠ e-mail + slug propre (plugin « Edit Author Slug ») + désactiver les archives d'auteur dans Yoast. Purger le cache LiteSpeed avant de conclure.
- Nettoyage : « Hello world! » + commentaire → corbeille ; « Uncategorized » → « Conseils » ou « Actualités ».
- Tél au format `tel:+33…`. Vérifier qu'aucun mauvais numéro ne traîne (y compris dans les métas Yoast).
- **Schema LocalBusiness** JSON-LD dans le `<head>` (1 seul par page) :
  - Elementor **Pro** → Elementor → Code personnalisé, emplacement `<head>`, tout le site.
  - Elementor **gratuit** (pas de Custom Code) → plugin **WPCode Lite**, emplacement site-wide header.
  - Si pas d'adresse connue → pas d'adresse dans le schema (ne rien inventer).

## 6. Leçons de terrain
- **Yoast gratuit** : téléphone/adresse/SIRET verrouillés « Premium » dans Représentation → les mettre dans le schema.
- **Thème Hello Elementor** peut injecter sa propre `meta description` (doublon avec Yoast) → Hello → Réglages avancés → « Désactiver la balise meta description ».
- **JSON-LD** : les URL (`@context`, `url`) se cassent quand on copie-colle un prompt entre deux fenêtres (vidées ou transformées en `[url](url)` Markdown). Toujours vérifier dans le code source que `"@context": "https://schema.org"` est en texte brut. `url` est facultatif.
- **Elementor** : modifier = clic UNE fois sur le bloc → panneau de gauche. Balise de titre → « Balise HTML ». Header/footer = Theme Builder (édité une fois pour tout le site). Certains sites ont un Theme Builder qui plante → header/footer intégrés dans chaque page.
- Yoast ne « voit » pas certains widgets Elementor (Heading/Image) → score rouge à tort ; ce qui compte = titre + méta + rendu public.
- **Search Console** : vérifier qu'on est sur la BONNE propriété. « Impossible de récupérer le sitemap » juste après l'envoi = normal, ça passe en « Opération effectuée » ensuite. « Exclue par noindex » après une levée de noindex = ancienne exploration, ça se corrige au prochain passage.
- Traduction auto de Chrome sur wp-admin = libellés faux → la désactiver.
- Si un site est bilingue (Polylang) et que le client construit lui-même la version EN : ne pas toucher à son chantier EN.

## 7. Git
- Branche de travail : **`claude/friendly-shannon-e3fr6a`**. Une fiche par site : `docs/<site>-audit.md`.
- Messages de commit sur **une seule ligne**. Si le garde-fou bloque `commit && push`, faire le commit puis le push séparément.
- `docs/HANDOFF-COMPLET.md` = ancien dossier technique général (utile pour les modèles de prompts et le schema). `docs/sitekit-et-transfert-propriete-client.md` = procédure de transfert de propriété aux clients.
- `index.html` à la racine = tableau de suivi de Camille (localStorage).

## 7 bis. Autres livrables et projets
- `rapports-clients/` : rapports SEO individuels par client (HTML, non techniques, aucun client ne voit un autre client).
- `HANDOFF-AUTOMATISATION-SEO.md` : doc technique du « Suivi SEO » (index.html statique + localStorage, pas de backend ; pistes : Google Sheet / Supabase-Firebase / repo GitHub).
- **Robot SEO** = autre repo **`xSARRASx/BUG-GL`**, branche **`claude/amazing-euler-U7YqQ`**. Demande de Martin : remplacer le stub `robot/lib/analyse.js` par une vraie analyse SEO publique en lecture seule. Contraintes : `dryRun: true`, `autoTermine: false`, `allowScheduledActive: false`, cron 15 min, aucune écriture sur WordPress, aucun OpenAI/OpenSEO payant, aucun statut « terminé » automatique, tests hors ligne, logs sans secrets (noms de variables d'environnement seulement). Lancer aucun workflow. **État : fichiers confirmés présents, rien modifié — Martin n'a jamais donné le « go ».** Ne pas commencer sans son feu vert.

## 8. SITE EN COURS : StayCare (Medellín, Colombie) — détails dans `docs/staycare-audit.md`
- Sandra Belhouari · staycare.com.co · multilingue Polylang : **ES à la racine**, `/fr/`, `/en/`, `/pt/` (7 pages par langue).
- ⚠️ **Contenu Elementor régénéré par script** (par Camille) : NE PAS toucher aux textes, H1, images, ALT, menus. Sûr : Yoast, réglages WP, WPCode, Search Console, Site Kit.
- **Fait (28/10)** : Yoast + WPCode (schema LocalBusiness) + Représentation + réseaux + fuite e-mail corrigée + fuseau Bogotá + légales/catégories noindex ; titres/métas/mots-clés sur les 28 pages ; **noindex levé** ; sitemap soumis (« Opération effectuée ») ; Site Kit connecté (martinmorebkk) ; **10 pages demandées en indexation**.
- **À faire** : demander l'indexation de `/en/our-area/` et `/pt/nossa-regiao/`, puis Nosotros / Contact / FAQ dans les 4 langues (~10 par jour).
- Côté Camille (envoyé) : ajouter « Airbnb » dans les H1/textes ES + traduire les ALT par langue ; créer `contact@staycare.com.co` ? ; fiche Google Business.
- Fin de projet : ajouter `contactostaycare@gmail.com` en propriétaire de la Search Console.
