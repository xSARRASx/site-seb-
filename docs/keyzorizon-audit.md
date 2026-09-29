# Keyzorizon Conciergerie — Rennes (Ille-et-Vilaine) — SEO LOCAL — Audit + notes

> Nadia Boutouba · keyzorizonconciergerie.fr · **sans Carte G** · Rennes + Bretagne.
> contact@keyzorizonconciergerie.fr · Google **boutoubanadia@gmail.com** (Gmail → OK Site Kit).
> Prestation : **SEO LOCAL uniquement** (base faite par Camille le 11/09 : Yoast titre « Conciergerie Airbnb à Rennes | Keyzorizon Conciergerie » + méta, JSON-LD, sitemap). Site en ligne et indexable.
> Accès : identifiant `camille` (mdp → Camille, jamais stocké ici).

## Zone CONFIRMÉE (formulaire Nadia)
- **Rennes** (principale) · **Saint-Malo** · **Sarzeau** · recherche de biens en **Ille-et-Vilaine**.
- (NB : Sarzeau est dans le Morbihan mais donnée par la cliente → on garde.)

## ⚠️ Points de vigilance
- **Téléphone 06 50 44 98 83 : NE PAS l'afficher** (elle n'en veut pas). Ne PAS l'ajouter au site ni au schema/fiche Google **sans l'accord de Camille**.
- **Ne pas contacter Nadia** (elle n'a pas vu la refonte du 11/09) → passer par Camille.
- **NAP incomplet** : SIRET + adresse manquants (« Rien à remplir ») → schema/fiche Google sans adresse pour l'instant.
- **Témoignage de « Thomas »** à faire confirmer → ne pas inventer, signaler si non vérifiable (risque faux avis / DGCCRF).
- **Loi Hoguet stricte** : son formulaire emploie « gestion » → toujours reformuler (pilotage · coordination · suivi · prise en charge · optimisation).
- Calendly : https://calendly.com/boutoubanadia . Concurrents : Cocoonr Rennes, Check In Conciergerie Rennes, KeyHome BnB. Pas de Facebook/Instagram connus.

## Prompt d'AUDIT (lecture seule) — à coller dans l'extension
```
Tu agis dans mon navigateur sur keyzorizonconciergerie.fr (WordPress + Elementor probable + Yoast).
MODE LECTURE SEULE : tu n'enregistres, ne modifies, ne publies, ne supprimes RIEN. Tu OBSERVES et tu fais un rapport.
Contexte : conciergerie, sans Carte G, zone Rennes + Saint-Malo + Sarzeau + Ille-et-Vilaine. Base SEO déjà faite (Yoast, JSON-LD, sitemap).
Donne-moi, structuré :
1) TOUTES les pages (menu + sitemap) : titre, URL/slug, statut + les articles.
2) Par page : H1 exact (0/plusieurs = signale), H2/H3, Titre SEO + Méta + mot-clé Yoast (via l'encart Yoast). Signale les mots-clés vides.
3) « conciergerie Airbnb » / « conciergerie Rennes » sont-ils bien placés (titre, H1, corps) sur Accueil/Services ? Y a-t-il des pages par ville (Rennes, Saint-Malo, Sarzeau) ?
4) JSON-LD LocalBusiness : présent ? téléphone affiché ? (⚠️ le tél 06 50 44 98 83 ne doit PAS apparaître). Zone correcte ?
5) VOCABULAIRE : occurrences « gestion / gestionnaire / gérer / gestion locative » — page, élément, phrase exacte (Ctrl+F « gestion » ET « gérer » séparément).
6) TÉLÉPHONE : cherche partout le 06 50 44 98 83 → signale CHAQUE endroit où il apparaît (il ne doit PAS être public).
7) AVIS/TÉMOIGNAGES : y en a-t-il ? Repère le témoignage de « Thomas » : a-t-il un nom complet/ville/date crédibles, ou style inventé ?
8) IMAGES sans ALT (où). Photos de stock / hors zone ?
9) LIENS : boutons « # », réseaux vides, lien Calendly, pages orphelines.
10) FAUTES + textes de template oubliés + incohérences de marque (Keyzorizon).
11) RÉGLAGES : langue, indexation (Réglages→Lecture), permaliens, sitemap. Search Console / Site Kit déjà là ?
12) ZONE : communes citées actuellement (Rennes, Saint-Malo, Sarzeau, Ille-et-Vilaine ?).
Rends-moi TOUT ça page par page. NE MODIFIE RIEN.
```

## Statut
- [ ] Audit fait
- [ ] Corrections SEO local appliquées (mots-clés, H1 avec ville, vocabulaire, maillage)
- [ ] Vérifier avec Camille : afficher le téléphone ? témoignage Thomas ? SIRET/adresse ?
- [ ] Search Console + Site Kit (compte boutoubanadia@gmail.com ou agence)

---

## ✅ AUDIT FAIT (29/09/2026, lecture seule) — synthèse
**Points sensibles OK** : téléphone 06 50 44 98 83 **introuvable** partout (HTML/tel:/JSON-LD, 11 URL) ✔ · **0 « gestion/gérer/gestionnaire »** sur tout le site ✔ · 1 H1/page, titres+métas partout, toutes images avec ALT, indexation ON, permaliens propres, sitemap+robots OK, clause Loi Hoguet dans les mentions légales ✔.

**À corriger :**
1. **Mot-clé Yoast VIDE** sur les 13 contenus (aucun score calculé).
2. **Pas de JSON-LD LocalBusiness** (seulement le schéma Yoast de base). Yoast = « Organisation » mais **nom + logo vides**.
3. **Faux témoignages** : « Thomas » = « Je suis pleinement satisfaite » (féminin), prénom seul, ni ville ni date ; « Elodie » dit « ils » (entreprise solo) ; le lien « fiche Google » = simple recherche Google. → risque DGCCRF.
4. **Restes de template indexables** : article **« Hello world! »** publié (+ commentaire par défaut), catégorie **Uncategorized**, **archive auteur** exposant l'adresse Gmail (titre + H1 + URL).
5. **Search Console** : pas de Site Kit, champ vérif Yoast vide, aucune balise.
6. **Pas de pages par ville** (Rennes/Saint-Malo/Sarzeau seulement en H3 dans « Nos logements ») ; page « Conciergerie » n'emploie « Airbnb » qu'une fois.
7. Divers : favicon absente, SIRET « en cours d'attribution » (client), photo « golfe du Morbihan » ≈ Chausey, salon en rendu 3D, je/nous mélangés, Calendly au nom perso, WordPress 7.1.2 en attente.

## Corrections SEO local prêtes (⚠️ NE PAS afficher le téléphone ; NE PAS inventer d'avis)
1. Renseigner le **mot-clé Yoast** par page (conciergerie Rennes / conciergerie Airbnb Rennes / conciergerie Saint-Malo…).
2. Ajouter un **schema LocalBusiness SANS téléphone ni adresse** (manquants) : nom, email, zone (Rennes, Saint-Malo, Sarzeau, Ille-et-Vilaine). Remplir aussi Yoast → Représentation du site (nom « Keyzorizon Conciergerie » + logo si dispo).
3. **Masquer la section témoignages** (Thomas/Elodie non crédibles) en attendant de vrais avis → signaler à Camille.
4. Nettoyage template : **corbeille « Hello world! »** + son commentaire ; renommer **Uncategorized** ; **noindex archives auteur** + nom public ≠ e-mail.
5. Renforcer « conciergerie Airbnb » / « conciergerie Rennes » sur Accueil + page Conciergerie ; harmoniser je/nous.
6. **Search Console + Site Kit** (compte agence martinmorebkk@gmail.com, ou compte cliente boutoubanadia@gmail.com).
7. **À décider** : créer des pages par ville (Rennes / Saint-Malo / Sarzeau) = gros levier local, mais création de pages.
8. **À voir avec Camille** : afficher le tél sur la fiche Google ? SIRET + adresse (NAP) ? confirmer/retirer le témoignage Thomas ? photo hors zone (Chausey) à remplacer.
