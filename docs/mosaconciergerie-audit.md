# MOSA Conciergerie (Belgique) — Audit + notes

> Maxime · mosaconciergerie.be · Liège (Belgique) · conciergerie · **client BELGE** (pas Loi Hoguet française).
> maxime@mosaconciergerie.com · Tél +32 491 97 27 18 · Google **mrafetin@gmail.com** (vrai Gmail → OK Site Kit).
> Prestation : **SEO complet**. Site WordPress + Elementor Pro NEUF, bilingue **FR/EN** (/en/ en cours).

## ⚠️ Points de vigilance (à lire avant tout)
1. **Belgique** : pas de Loi Hoguet FR, MAIS l'IPI (agent immobilier belge) encadre aussi la « gestion locative » →
   par prudence on garde le réflexe : éviter « gestion locative / gestionnaire ». Moins strict qu'en France.
2. **Zone NON confirmée** : ville pressentie = Liège + agglo, mais **demander à Maxime la liste exacte des communes**
   AVANT de faire les titres/H1 locaux (site neuf → on ne peut pas la déduire).
3. **🚨 Maxime édite le site EN DIRECT** : ne PAS appliquer de corrections tant qu'il bosse dessus (risque d'écrasement).
   → 2 feux verts avant corrections : (a) liste communes de Maxime, (b) Maxime a fini d'éditer (via Camille).
4. **Bilingue FR/EN** : gérer le hreflang, ne pas mélanger FR et EN, /en/ peut être partiel.
5. Non bloquant pour le SEO : mentions légales FR/EN en brouillon (attente n° BCE), bandeau cookies absent, avis à venir.

## Accès
- Auto-login via hPanel > Partage de compte > Admin WordPress (demander à Camille). Login = mrafetin@gmail.com.

## Prompt d'AUDIT (lecture seule) — à coller dans l'extension
```
Tu agis dans mon navigateur sur mosaconciergerie.be (WordPress + Elementor Pro, site BILINGUE FR/EN).
MODE LECTURE SEULE : tu n'enregistres, ne modifies, ne publies, ne supprimes RIEN. Tu OBSERVES et tu fais un rapport.
⚠️ Le propriétaire édite peut-être le site en direct : ne verrouille rien, n'ouvre pas d'éditeur en écriture.

Fais l'inventaire complet pour préparer un SEO (conciergerie, Belgique/Liège, zone NON confirmée). Donne-moi, structuré :
1) LISTE DE TOUTES LES PAGES FR + EN (/en/) : titre, URL/slug, statut, langue.
2) POUR CHAQUE PAGE : H1 exact (0/plusieurs = signale), H2/H3, et si plugin SEO présent : Titre SEO + Méta + mot-clé. Sinon signale l'absence.
3) PLUGIN SEO (Yoast/RankMath/SEOPress) ? Plugin multilingue (WPML/Polylang/TranslatePress) ?
4) BILINGUE : hreflang FR/EN présent ? /en/ complet ou partiel ? contenu EN mélangé au FR ?
5) VOCABULAIRE : occurrences « gestion/gestionnaire/gérer/gestion locative » (FR) + « property management » (EN) — page, élément, phrase.
6) IMAGES : combien sans ALT, où. Photos de stock non locales ?
7) LIENS : boutons « # », réseaux vides/faux, tél (format), pages orphelines, liens FR↔EN.
8) AVIS : présents ? réels ou inventés ?
9) FAUTES + textes de template oubliés (souvent EN) + incohérences de marque.
10) RÉGLAGES : langue, indexation (Réglages→Lecture — site neuf souvent en « décourager les moteurs » !), permaliens, sitemap, Search Console existante ?
11) ZONE : communes belges citées actuellement.
12) ÉTAT DES TRAVAUX : sections en cours de construction (placeholders, brouillons).
Rends-moi TOUT ça page par page (FR+EN). NE MODIFIE RIEN.
```

## Statut
- [x] Accès obtenus
- [x] Audit **PARTIEL** fait (~70% — connexion Chrome perdue en cours)
- [ ] Audit à terminer (rouvrir l'onglet + « continue » à l'extension : vocabulaire, avis, fautes, ALT médiathèque, H2/H3 légales, communes Zone/FAQ)
- [ ] Zone confirmée par Maxime
- [ ] Maxime a fini d'éditer (surtout la version EN/Polylang) → feu vert corrections
- [ ] Corrections appliquées
- [ ] Search Console + Site Kit (compte mrafetin@gmail.com)

## Findings de l'audit partiel (2026-09-18)
- **Aucun plugin SEO** (ni Yoast/RankMath/SEOPress) → 0 méta (sauf article auto 155c), titres défaut « Page – MOSA Conciergerie », pas d'OG, pas de mot-clé. → **SEO complet, Yoast à installer.**
- **Indexation OK** (case « décourager » NON cochée). Sitemap natif `/wp-sitemap.xml` expose **/author/mrafetingmail-com/** (⚠️ fuite du login admin) + catégorie + tag.
- **Search Console** : aucune (à créer).
- **Pages** : 7 FR (6 publiées + **Mentions légales en brouillon → 404** alors que le footer FR+EN y pointe) ; **2 EN seulement** (Home, Book a call) via **Polylang gratuit, assistant NON terminé** ; 1 article FR (« Conciergerie Airbnb à Liège… ») ; 5 articles + 1 page en corbeille ; template Header Elementor en brouillon.
- **H1** : `/logements/` **sans H1** ; page auteur H1 vide ; H1 accueil « Louer en toute sérénité » **coupé par un `<br>` sans espace** ; aucun mot-clé métier/géo dans H1-H2 de l'accueil.
- **Bilingue (⚠️ en construction)** : hreflang Polylang sur les 2 paires traduites, **pas de x-default**. Switcher FR/EN = lien fixe `/` et `/en/` (pas le switcher Polylang). **Home EN pointe vers des pages FR** (/logements/, /blog/, /mentions-legales/), bandeau cookies Complianz **en FR sur l'EN**, `/en/logements/` etc. répondent **200 avec le contenu FR** (duplication/mélange). → NE PAS toucher tant que Maxime construit l'EN.
- **Images/liens** : 8 pictos sans ALT (accueil FR+EN, mosa-icone-1…8) ; photos logements en **fond CSS** (pas d'`<img>` → pas d'ALT possible) ; Insta/Facebook = **liens vides** (instagram.com/, facebook.com/) ; LinkedIn = profil perso ; `tel:+32491972718` OK mais affiché « 0491… » en FR / « +32 491… » en EN ; **e-mail en .com** alors que le site est en .be ; menu = ancres de l'accueil ; politique de confidentialité orpheline.
- **Zone citée** : Liège, **Huy, Namur** (slogan), Outremeuse, Sart-Tilman, Condroz, Le Perron/Cornillon (noms de logements), Liège seul dans l'article. ⚠️ Huy/Namur = à confirmer avec Maxime (3 villes distinctes, peut-être aspirationnel).
- **Reste à auditer** (browser coupé) : vocabulaire gestion/management, témoignages, fautes/textes template, ALT médiathèque, H2/H3 légales/archives, communes « Zone d'activité » + FAQ.

---

## PLAN DE CORRECTION (prêt — à appliquer SEULEMENT après les 2 feux verts)
> Zone provisoire = **Liège (principale), Huy, Namur** (leur propre site le cite partout). ⚠️ confirmer la hiérarchie
> avec Maxime (3 villes + « Wallonie » = ambition, pas forcément zone réelle). Belgique = pas Hoguet, mais prudence IPI.

### A. Yoast + réglages (fondation, zone-indépendant)
- Installer Yoast. **NOINDEX** : archives auteur (fixe la fuite /author/mrafetingmail-com/), catégories, étiquettes ;
  rediriger les pièces jointes. Retirer auteurs/tag du sitemap.
- Yoast → Représentation du site : Organisation « MOSA Conciergerie », logo, tél +32491972718.

### B. Yoast Titres + Métas (par page) — Liège/Huy/Namur
- Accueil : « Conciergerie Airbnb à Liège, Huy & Namur | MOSA » + méta accueil voyageurs/ménage/optimisation.
- Logements / Blog / Rendez-vous / Article : idem, adaptés (voir prompt).
- Légales : noindex.

### C. H1 & structure
- **Bug `<br>` sans espace** sur les H1/H2 (« toutesérénité », « Tarificationdynamique », EN « totalserenity »…) → remettre l'espace.
- `/logements/` : **ajouter un H1** « Nos logements en conciergerie à Liège, Huy & Namur ».
- Surtitre hero « CONCIERGERIE AIRBNB EN WALLONIE » → « …À LIÈGE, HUY & NAMUR » (mot-clé + villes réelles).
- Boutons « Réserver » de /logements/ (#contact mort) → /rendez-vous/.

### D. Vocabulaire (prudence IPI + cohérence avec leurs mentions légales « n'exerce aucune activité d'agence immobilière »)
- Article : « Mandat de gestion… » (méta/extrait) → reformuler ; « gestion des réservations » → « suivi des réservations » ;
  « gérer les réservations » → « s'occuper des réservations » ; « mandat de gestion classique » → « mandat de conciergerie ».
- EN Home : « property management » → « Airbnb concierge service » ; « Booking management » → « Booking coordination » ;
  « switch property manager » → « switch concierge ».

### E. Fautes / templates
- « Combiné » → « Combinée » ; ALT « Boveri » → « Boverie » ; « Belgique Belgique » (doublon cookies) ;
  footer libellé « Facebook-f » ; jargon « LCD » → « location courte durée (LCD) ».
- Politique de cookies : texte générique e-commerce Complianz (« panier/paiement », section 6 vide) → régénérer via Complianz (config).

### F. Images ALT
- 8 pictos mosa-icone-1..8 (accueil FR+EN) → ALT descriptifs. Sur l'EN, traduire les ALT actuellement en FR (⚠️ dépend de l'EN de Maxime).

### G. Liens
- Tél : harmoniser l'affichage « +32 491 97 27 18 » partout (FR affiche « 0491… »).
- Réseaux Insta/Facebook vides → laisser (comme les autres) ou brancher si Maxime donne les URL.
- E-mail .com vs domaine .be → **à confirmer** (lequel est le bon ?).

### H. Schema LocalBusiness (Elementor → Code perso, <head>)
- name MOSA Conciergerie, tél +32491972718, adresse Rue Strivay 53, 4122 Plainevaux (Neupré), areaServed Liège/Huy/Namur, email.

### I. Search Console + Site Kit (compte mrafetin@gmail.com)
- Créer propriété + sitemap ; puis Site Kit.

### ⏸️ NE PAS TOUCHER (chantier de Maxime)
- Toute la partie **bilingue EN/Polylang** (EN partiel, /en/<slug-fr> sert du FR, cookies FR sur EN, switcher, x-default) → attendre qu'il finisse.
- Mentions légales (brouillon, BCE manquant), header template brouillon, logements (photos stock/placeholders), témoignages placeholders.

## 🙋 À demander à Maxime (via Camille)
1. **Zone exacte** : vraiment Liège + Huy + Namur à parts égales, ou **Liège en priorité** + les 2 autres en secondaire ?
2. Quand aura-t-il **fini de construire** (surtout l'EN + mentions légales + vraies photos de logements) ?
3. **E-mail** : .com ou .be ? Et a-t-il de **vrais** comptes Facebook/Instagram à brancher ?
