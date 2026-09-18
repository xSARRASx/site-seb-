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
