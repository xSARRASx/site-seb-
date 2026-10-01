# CasaNova Conciergerie — Sartrouville (78) — SEO COMPLET — Audit + notes

> Imen Siboly · conciergeriecasanova.com · **sans Carte G**. Prestation : **SEO COMPLET** (Yoast installé mais NON réglé : titre « Accueil - CasaNova », pas de méta, pas de Search Console/Site Kit).
> NAP complet : **06 48 56 73 55** · contact@conciergeriecasanova.com · **8 rue Gustave Flaubert, 78500 Sartrouville** · SIRET 105 866 230 00011.
> Google : compte marque **conciergerie.casanova@gmail.com** (hébergement) ; perso **m.siboly@gmail.com**. Accès : identifiant `camille` (mdp → Camille).

## ⚠️ BLOCAGE AVANT CORRECTIONS
- **En-tête + pied de page CasaNova (Theme Builder) PAS encore activés** → le site affiche ceux **par défaut du thème**. **Camille doit les activer d'abord.**
- → Audit lecture seule OK maintenant ; mais **ne PAS appliquer les corrections touchant header/footer** (schema, liens footer, NAP) tant que les vrais modèles ne sont pas activés.

## Zone CONFIRMÉE (formulaire Imen)
- **Cœur (rayon 5 km)** : Houilles, Carrières-sur-Seine, Sartrouville. **+** Maisons-Laffitte, Montesson, Bezons, Argenteuil, Cormeilles-en-Parisis.

## Mots-clés visés
- conciergerie Airbnb Houilles · conciergerie Sartrouville · conciergerie Carrières-sur-Seine · location courte durée.
- Concurrents : La Conciergerie Ovilloise, Click-Chic Conciergerie.

## Points de vigilance
- **Loi Hoguet** (sans Carte G) : elle emploie « gestion » dans ses réponses → **toujours reformuler** (pilotage · coordination · prestataire · suivi · optimisation).
- **Aucun témoignage** → ne rien inventer.
- **Réseaux** : Facebook/Instagram/LinkedIn cochés dans son formulaire mais **URLs jamais fournies** → ne rien brancher sans les vraies URL.
- **Fiche Google Business** : à optimiser, accès à demander à Imen.

## Prompt d'AUDIT (lecture seule) — à coller dans l'extension
```
Tu agis dans mon navigateur sur conciergeriecasanova.com (WordPress + Elementor + Yoast installé mais non réglé).
MODE LECTURE SEULE : tu n'enregistres, ne modifies, ne publies, ne supprimes RIEN. Tu OBSERVES et tu fais un rapport.
Contexte : conciergerie, sans Carte G, zone Houilles/Carrières-sur-Seine/Sartrouville + Maisons-Laffitte/Montesson/Bezons/Argenteuil/Cormeilles-en-Parisis.
NB : l'en-tête et le pied de page CasaNova (Theme Builder) ne sont peut-être pas activés (thème par défaut affiché) → signale ce que tu vois.
Donne-moi, structuré :
1) TOUTES les pages (menu + sitemap) : titre, URL/slug, statut + articles.
2) Par page : H1 exact (0/plusieurs = signale), H2/H3, Titre SEO + Méta + mot-clé Yoast (encart Yoast). Signale les vides.
3) « conciergerie Airbnb » / « conciergerie Houilles » / « conciergerie Sartrouville » placés (titre, H1, corps) ? Pages par ville ?
4) VOCABULAIRE : occurrences « gestion / gestionnaire / gérer / gestion locative » — page, élément, phrase exacte (Ctrl+F « gestion » ET « gérer » séparément).
5) JSON-LD / schema : présent ? LocalBusiness ? tél 06 48 56 73 55 + adresse 8 rue Gustave Flaubert ?
6) IMAGES sans ALT (où). Photos de stock / hors zone ?
7) LIENS : boutons « # », réseaux vides, lien téléphone (format tel:), pages orphelines. Header/footer = ceux du thème ou les modèles CasaNova ?
8) AVIS/TÉMOIGNAGES : présents ? (normalement aucun) réels ou inventés ?
9) FAUTES + textes de template oubliés (« Hello world! », Uncategorized, archives auteur exposant l'e-mail) + incohérences de marque (CasaNova).
10) RÉGLAGES : langue (fr ?), indexation (Réglages→Lecture), permaliens, sitemap. Search Console / Site Kit déjà là ? Yoast : titre par défaut « Accueil - CasaNova » ?
11) ZONE : communes citées actuellement.
Rends-moi TOUT ça page par page. NE MODIFIE RIEN.
```

## Statut
- [x] Audit fait (lecture seule)
- [ ] Camille active l'en-tête + pied de page CasaNova (Theme Builder) → **bloque les corrections header/footer**
- [ ] Corrections SEO complet appliquées
- [ ] Search Console + Site Kit (compte agence ou marque)
- [ ] Fiche Google Business : accès à demander à Imen

---

## ✅ AUDIT FAIT (lecture seule) — synthèse
**Points OK** : **0 « gestion/gérer/gestionnaire »** sur tout le site (Loi Hoguet clean) ✔ · toutes les images ont un ALT correct ✔ · NAP disponible dans le contenu ✔.

**À corriger :**
1. **Yoast totalement non réglé** : tous les titres = « Titre - CasaNova », **aucune méta**, **aucun mot-clé** sur 7 pages + 1 article.
2. **Pas de schema LocalBusiness** (Yoast « Organisation » coché mais **vide** : ni tél ni adresse).
3. **Restes de template indexables** : **6× « This is text element »** (3 Accueil + 3 Services, sous les cartes), article **« Hello world! »** publié + commentaire, catégorie **Uncategorized**, **archive auteur exposant l'e-mail** (`/author/conciergerie-casanovagmail-com/`, titre + H1 = l'e-mail).
4. **Sitemap** inclut les sitemaps auteur + catégorie (à noindex).
5. **Pas de Search Console / Site Kit**.
6. **Zone** présente dans le contenu mais **seulement 3 communes dans un H1**, aucune dans les titres SEO.
7. **En-tête + pied de page = thème par défaut** (modèles CasaNova publiés « Tout le site » mais pas rendus) → **blocage Camille**.
8. Divers : **saut H1→H3 sur Contact** (pas de H2), **« Reportings »** (anglicisme), Privacy Policy brouillon EN.
9. **Pas de témoignages** (normal) → ne rien inventer. **Réseaux** cochés mais **aucune URL** → ne rien brancher.

## Corrections SEO complet prêtes
1. **Régler Yoast** par page : mot-clé (`conciergerie Airbnb Houilles` / `conciergerie Sartrouville` / `conciergerie Carrières-sur-Seine` / `conciergerie Airbnb`), **Titre SEO** (50-60c, ville) + **méta** (120-155c).
2. **Représentation du site** (Yoast) : type **Organisation** = « CasaNova Conciergerie », tél **+33648567355**, adresse **8 rue Gustave Flaubert, 78500 Sartrouville**, SIRET **105 866 230 00011**.
3. **Schema LocalBusiness** (Elementor → Code perso, `<head>`, tout le site) : NAP complet + zone 8 communes. ⚠️ **à poser après activation header/footer** (cohérence NAP).
4. **Renforcer** « conciergerie Airbnb » sur Accueil + Services ; ajouter un **H2** sur Contact (corrige le saut H1→H3).
5. **Nettoyage** : supprimer les **6 « This is text element »** ; corbeille **« Hello world! »** + commentaire ; renommer **Uncategorized** (→ « Conseils ») ; **noindex archives auteur** + nom public ≠ e-mail ; corriger « Reportings ».
6. **Search Console + Site Kit** (compte agence martinmorebkk@gmail.com, ou marque conciergerie.casanova@gmail.com).
7. **Garder 0 « gestion/gérer »** ; **ne pas inventer d'avis** ; **ne pas ajouter de réseaux** (pas d'URL).

## Prompt de CORRECTION (à coller dans l'extension) — SANS header/footer
```
Tu agis dans mon navigateur sur conciergeriecasanova.com (WordPress + Elementor + Yoast). Tu PEUX modifier, mais tu ENREGISTRES chaque changement (Mettre à jour) et tu NE TOUCHES PAS à l'en-tête ni au pied de page (modèles Theme Builder pas encore activés — on verra plus tard).
Contexte : conciergerie, SANS Carte G → INTERDIT d'écrire « gestion / gestionnaire / gérer / gestion locative ». Utilise : conciergerie, location courte durée, location saisonnière, pilotage, coordination, prestataire, suivi, prise en charge, optimisation, accompagnement. Zone : Houilles, Carrières-sur-Seine, Sartrouville (cœur) + Maisons-Laffitte, Montesson, Bezons, Argenteuil, Cormeilles-en-Parisis.

Fais, dans l'ordre, en enregistrant à chaque fois :

1) YOAST — RÉGLAGES GÉNÉRAUX (Yoast → Réglages → Représentation du site) :
   - Type : Organisation. Nom : « CasaNova Conciergerie ».
   - Téléphone : +33648567355. Adresse : 8 rue Gustave Flaubert, 78500 Sartrouville. SIRET : 105 866 230 00011 (si champ dispo).

2) YOAST PAR PAGE (encart Yoast de chaque page/article) — mot-clé + Titre SEO (50-60 car.) + Méta (120-155 car.) :
   - Accueil : mot-clé « conciergerie Airbnb Houilles ». Titre ex. « Conciergerie Airbnb à Houilles & Sartrouville | CasaNova ». Méta orientée propriétaires (location courte durée, zone, contact).
   - Services : mot-clé « conciergerie Airbnb ». Titre + méta sur les prestations (accueil voyageurs, ménage, optimisation des annonces, suivi).
   - Contact : mot-clé « conciergerie Sartrouville ». Titre + méta.
   - Les autres pages (À propos, etc.) : un mot-clé pertinent + titre + méta cohérents.
   - L'article : mot-clé + titre + méta.
   NE laisse AUCUN titre « Titre - CasaNova » ni aucun mot-clé vide.

3) CONTENU :
   - Accueil + Services : renforce naturellement « conciergerie Airbnb » et les villes (Houilles, Sartrouville, Carrières-sur-Seine) dans le H1 et le 1er paragraphe, SANS « gestion/gérer ».
   - Contact : ajoute un H2 clair (ex. « Contactez votre conciergerie à Sartrouville ») pour corriger le saut H1→H3.
   - Remplace l'anglicisme « Reportings » par « Comptes rendus » (ou « Suivi »).

4) NETTOYAGE TEMPLATE :
   - Supprime les 6 blocs « This is text element » (3 sur Accueil, 3 sur Services) ou remplace-les par un vrai texte utile.
   - Mets « Hello world! » à la corbeille + supprime son commentaire par défaut.
   - Renomme la catégorie « Uncategorized » en « Conseils » (slug : conseils).

5) ARCHIVES AUTEUR (expose l'e-mail) :
   - Profil utilisateur : règle le « Nom à afficher publiquement » sur « CasaNova Conciergerie » (PAS l'e-mail).
   - Yoast → Réglages → Types de contenu / Archives : passe les archives d'auteur en noindex (et catégories/étiquettes si inutiles).

6) VÉRIFS FINALES : fais Ctrl+F « gestion » PUIS « gérer » sur chaque page → il doit y avoir 0 occurrence. N'invente aucun avis. N'ajoute aucun lien réseau social (aucune URL fournie).

NE touche PAS au schema LocalBusiness (JSON-LD) ni à l'en-tête/pied de page pour l'instant : on les fera après activation des modèles. Dis-moi ce que tu as changé page par page.
```

> **Après activation header/footer par Camille** : poser le JSON-LD LocalBusiness (NAP complet + zone 8 communes) via Elementor → Code personnalisé (`<head>`, tout le site), puis Search Console + Site Kit (martinmorebkk@gmail.com) + demander l'accès fiche Google Business à Imen.
