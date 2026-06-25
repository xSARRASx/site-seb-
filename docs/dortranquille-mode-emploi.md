# D'Or Tranquille — Mode d'emploi pas à pas (à suivre dans l'ordre)

Tout ce qu'il faut modifier sur https://dortranquille.fr, **dans l'ordre**, avec
**où cliquer** et **quoi coller**. Compter ~1h-1h30.

> ⚠️ Avant de commencer : se connecter au WP admin (dortranquille.fr/wp-admin),
> identifiant **camille**. On travaille sur le site réel : **toujours cliquer
> « Mettre à jour » après chaque page.**

---

## 🟦 BLOC 1 — Corriger les textes (avec Elementor)

Pour chaque page : ouvrir la page → cliquer **« Edit with Elementor »** (barre du haut)
→ cliquer sur le texte à corriger → le modifier dans le panneau de gauche
→ cliquer le bouton vert **« Mettre à jour »** en bas à gauche.

### Page ACCUEIL
1. Sur-titre de section — remplacer :
   - ❌ `Une Gestion Sereine Pour Votre Location Courte Durée`
   - ✅ `Un Accompagnement Serein Pour Votre Location Courte Durée`
2. Témoignage de « Miley Houdson » — remplacer :
   - ❌ `…tout au long de la gestion de notre logement.`
   - ✅ `…tout au long de l'accompagnement de notre logement.`

### Page À PROPOS
3. Paragraphe « Une Nouvelle Vie Au Cœur Des 2 Alpes » (3ᵉ paragraphe) :
   - ❌ `…dans la gestion de leur location courte durée…`
   - ✅ `…dans la prise en charge de leur location courte durée…`
4. Carte de valeur « Confiance » :
   - ❌ `Un accompagnement sérieux pour gérer votre bien sereinement.`
   - ✅ `Un accompagnement sérieux pour prendre soin de votre bien sereinement.`
5. Bandeau du bas « Confiez Votre Location Courte Durée À D'Or Tranquille » :
   - ❌ `…pour gérer votre logement aux 2 Alpes en toute sérénité.`
   - ✅ `…pour prendre soin de votre logement aux 2 Alpes en toute sérénité.`

### Page SERVICES
6. Bloc « Pourquoi Choisir D'Or Tranquille » — titre :
   - ❌ `Gestion Sérieuse`  →  ✅ `Suivi Sérieux`
7. Carte service « Gestion Du Linge » :
   - ❌ titre `Gestion Du Linge`  →  ✅ `Coordination Du Linge`
   - ❌ texte `Gestion du linge avec une attention…`  →  ✅ `Coordination du linge avec une attention…`

### Page CONTACT
8. Formulaire — champ mal orthographié :
   - ❌ `Sujette`  →  ✅ `Sujet`
   - (clic sur le champ → panneau gauche → onglet « Content » → champ « Placeholder/Label »)

### PIED DE PAGE (une seule fois, il s'applique à toutes les pages)
9. Le footer est un **modèle global**. Pour l'éditer :
   - WP admin → **Templates → Theme Builder → Footer** (ou « Modèles »), ouvrir le footer avec Elementor.
   - Texte à corriger :
     - ❌ `…pour valoriser et gérer votre location courte durée aux 2 Alpes.`
     - ✅ `…pour valoriser et prendre soin de votre location courte durée aux 2 Alpes.`

---

## 🟩 BLOC 2 — Title + Meta + mot-clé (avec Yoast)

Pour chaque page : WP admin → **Pages** → ouvrir la page → descendre **sous** l'éditeur
jusqu'au bloc **« Yoast SEO »** → cliquer **« Édition de l'extrait Google »**.
Y coller : **Titre SEO**, **Méta description**, et **Requête cible** (focus keyphrase).
Puis **« Mettre à jour »**.

### Accueil
- Titre SEO : `Conciergerie Airbnb Les 2 Alpes | D'Or Tranquille`
- Méta : `Conciergerie aux 2 Alpes : accueil des voyageurs, ménage, linge et optimisation de vos annonces. Confiez votre location courte durée à D'Or Tranquille.`
- Requête cible : `conciergerie Airbnb Les 2 Alpes`

### À propos
- Titre SEO : `Conciergerie Les 2 Alpes : à propos de D'Or Tranquille`
- Méta : `Découvrez D'Or Tranquille, votre conciergerie aux 2 Alpes : une reconversion passionnée, l'exigence du service et la proximité au cœur de la station.`
- Requête cible : `conciergerie Les 2 Alpes`

### Services
- Titre SEO : `Conciergerie Airbnb Les 2 Alpes : ménage, accueil & annonces`
- Méta : `Ménage, linge, check-in/out, création d'annonces et optimisation : découvrez les services de conciergerie de D'Or Tranquille aux 2 Alpes.`
- Requête cible : `services de conciergerie Les 2 Alpes`

### Contact
- Titre SEO : `Contact – Conciergerie Les 2 Alpes | D'Or Tranquille`
- Méta : `Contactez D'Or Tranquille, conciergerie aux 2 Alpes. Prenez rendez-vous en ligne ou appelez le 06 88 21 58 30. Parlons de votre location courte durée.`
- Requête cible : `conciergerie Les 2 Alpes contact`

### Blog
- Titre SEO : `Blog conciergerie & location courte durée | D'Or Tranquille`
- Méta : `Conseils et actualités pour propriétaires en location courte durée aux 2 Alpes : optimisation, accueil des voyageurs et bonnes pratiques par D'Or Tranquille.`
- (Blog vide → voir Bloc 4, point Blog.)

---

## 🟨 BLOC 3 — Images (ALT)

Pour chaque image importante : la cliquer dans Elementor → onglet **« Avancé / Image »**
ou via **Médias** → champ **« Texte alternatif »**. Exemples à utiliser :
- Accueil héro : `conciergerie Airbnb Les 2 Alpes`
- Ménage : `ménage location courte durée Les 2 Alpes`
- Linge : `coordination du linge conciergerie Les 2 Alpes`
- Check-in : `check-in voyageurs Les 2 Alpes`
- Chalets : `chalet en location courte durée Les 2 Alpes`

---

## 🟥 BLOC 4 — Technique & finitions

- [ ] **Indexation ON** : Réglages → Lecture → décocher « Demander aux moteurs… »
- [ ] **Permaliens** : Réglages → Permaliens → « Titre de la publication »
- [ ] **Search Console** : valider le site + soumettre le sitemap `/sitemap_index.xml`
- [ ] **Cache** (LiteSpeed sur Hostinger) actif + **images WebP** (Converter for Media)
- [ ] **403** : vérifier que le site est bien accessible publiquement (sinon Google ne peut pas l'indexer)
- [ ] **Blog** : on **garde la page tel quel** (un article viendra plus tard). Juste retirer les `**`
      du titre « **Nos Articles & Conseils » → « Nos Articles & Conseils » (petit défaut d'affichage).
- [ ] **Témoignages** : ✅ **on garde la section** pour l'instant. (Mais bien corriger le mot « gestion »
      dans le témoignage de Miley Houdson — voir Bloc 1, point 2.)
- [ ] **Marque** : ✅ uniformiser les **textes** en « **D'Or Tranquille** » (remplacer « D'or » par « D'Or »).
      Le logo « Dort Tranquille » reste tel quel (exception graphique assumée).
- [ ] **Fiche Google Business** : catégorie « Service de conciergerie », NAP identique au site,
      zone Les 2 Alpes, photos, description sans « gestion ».

---

## ✅ BLOC 5 — Vérification finale
- [ ] Re-tester l'affichage des titres/metas (taper `site:dortranquille.fr` dans Google).
- [ ] Vérifier qu'il ne reste **aucun** « gestion / gérer » (Ctrl+F sur chaque page publiée).
- [ ] Remplir le **reporting client** et passer le site en « Terminé » dans le tableau de bord.
