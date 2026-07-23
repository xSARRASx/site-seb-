# TEMPLATE — Prompt maître pour l'extension « Claude pour Chrome »

> **Comment l'utiliser :**
> 1. Je (Claude) remplis les champs `[ENTRE CROCHETS]` avec les infos du site + les corrections repérées sur les captures.
> 2. Tu ouvres un onglet Chrome sur `.../wp-admin` (connecté).
> 3. Tu colles TOUT le bloc ci-dessous dans le panneau latéral Claude.
> 4. Mode **autonome** : il déroule tout seul et te fait un récap à la fin. (Tu peux désactiver « Demander avant d'agir » pour qu'il n'attende pas — ou le garder si tu préfères confirmer.)
>
> ⚠️ C'est un Claude *navigateur* (claude.ai), pas Claude Code. Sur Elementor c'est lent → normal.

---

```
Tu es mon assistant pour appliquer une optimisation SEO sur un site WordPress (Elementor + Yoast).
Tu agis DANS mon navigateur, sur l'onglet ouvert. Suis ce protocole À LA LETTRE.

########## CONTEXTE ##########
- Site : [URL DU SITE]
- Client / marque : [NOM]
- Activité : [conciergerie / sous-location]
- Ville / zone ciblée : [VILLE]
- Carte G : [OUI / NON]

########## RÈGLES ABSOLUES (à respecter en permanence) ##########
1. TRAVAILLE PAGE PAR PAGE, DANS L'ORDRE indiqué plus bas.
2. AVANCE DE FAÇON AUTONOME : enregistre (« Mettre à jour » / « Sauvegarder » / « Save ») 
   au fur et à mesure, SANS me demander à chaque fois. Ne t'arrête QUE si tu es réellement bloqué.
3. Ne touche QU'À ce qui est listé. Ne modifie NI le design, NI la mise en page, NI les couleurs.
4. FAUX AVIS / témoignages inventés : ne les invente jamais, ne les crée jamais ; signale-les-moi dans le récap final (risque légal).
5. LOI HOGUET (si Carte G = NON) : le site ne doit contenir AUCUN de ces mots :
   « gestion », « gestionnaire », « gérer », « gestion locative », « gestion Airbnb ».
   Remplacements autorisés : prise en charge · coordination · suivi · accompagnement · optimisation.

########## MÉTHODE ELEMENTOR (mémorise) ##########
- Pour modifier un TEXTE : clique UNE fois sur le bloc → panneau de GAUCHE (onglet « Contenu ») → édite le champ. (PAS de double-clic sur la page.)
- Blocs « Icon Box » JKit (cartes avec icône) : le titre ET la description sont des champs dans le panneau de gauche.
- Pour changer une BALISE de titre (H1/H2/H3) : clique le titre → panneau gauche → réglage « Balise HTML » (HTML Tag) → choisis la balise.
- Le PIED DE PAGE est un modèle global : Elementor → « Theme Builder » → « Footer » (à éditer UNE seule fois).

########## MÉTHODE YOAST (mémorise) ##########
- Ouvre la page en ÉDITEUR NORMAL (pas Elementor) → clique l'icône « Y » colorée en haut à droite → section « Apparence de recherche ».
- Colle : Titre SEO, Méta-description (vise 120-155 caractères = barre VERTE), et le Mot-clé principal.
- « Limace » = slug = fin de l'URL : n'y touche pas si elle est déjà propre.

===================================================================
ÉTAPE 0 — RÉGLAGES GLOBAUX (une seule fois)
===================================================================
0.1 Settings → General → « Site Language » = Français (pour avoir og:locale = fr_FR).
0.2 Settings → Reading → décoche « Discourage search engines from indexing this site ». Save.
0.3 Settings → Permalinks → choisis « Post name ». Save.
0.4 Vérifie que le plugin « Yoast SEO » est installé et activé (sinon : Plugins → Add New → Yoast SEO → Install → Activate).

===================================================================
ÉTAPE 1 — CORRIGER LES TEXTES INTERDITS (Loi Hoguet)
===================================================================
Sur CHAQUE page, repère et remplace tout « gestion » / « gérer ».
Corrections précises repérées sur ce site :
[LISTE DES REMPLACEMENTS PAR PAGE — ex :
 - Accueil, sur-titre : « Une Gestion Sereine… » → « Un Accompagnement Serein… »
 - Services, carte : « Gestion Du Linge » → « Coordination Du Linge »
 - Footer : « …et gérer votre location… » → « …et prendre soin de votre location… »
 ...]

===================================================================
ÉTAPE 2 — BALISES H1 (1 seul H1 par page)
===================================================================
Pour chaque page, le grand titre du héros doit être en H1 avec le mot-clé. 
[H1 PAR PAGE — ex :
 - Accueil : « [H1 ACCUEIL] »
 - À propos : « [H1 À PROPOS] »
 - Services : « [H1 SERVICES] »
 - Contact : « [H1 CONTACT] »
 - Blog : « [H1 BLOG] »]

===================================================================
ÉTAPE 3 — YOAST : TITRE + MÉTA + MOT-CLÉ (par page)
===================================================================
[PAR PAGE :
 --- [PAGE] ---
 Mot-clé principal : [MOT-CLÉ]
 Titre SEO : [TITRE]
 Méta-description : [MÉTA]
 ...]

===================================================================
ÉTAPE 4 — LIENS & PETITS DÉFAUTS
===================================================================
4.1 Boutons/CTA qui pointent vers « # » (lien vide) → fais-les pointer vers la page Contact.
4.2 Lien Facebook qui pointe vers « facebook.com » tout court → mets la vraie page, ou signale-le moi si tu n'en as pas.
4.3 Titres contenant des « ** » parasites → enlève les « ** ».
4.4 Champs de formulaire mal orthographiés (ex : « Sujette » → « Sujet ») → corrige.
4.5 FAUX AVIS / témoignages inventés : NE LES PUBLIE PAS et SIGNALE-les-moi (risque légal). Ne les invente jamais.

===================================================================
ÉTAPE 5 — IMAGES (ALT)
===================================================================
Remplis les attributs ALT VIDES des images principales avec une description contenant le mot-clé + la ville.
Exemples : « conciergerie Airbnb [VILLE] », « ménage location courte durée [VILLE] », « check-in voyageurs [VILLE] ».
Ne renomme PAS les fichiers, ne remplace PAS les photos (c'est au client).

===================================================================
ÉTAPE 6 — GOOGLE (indexation)
===================================================================
6.1 Vérifie que le sitemap existe : [URL]/sitemap_index.xml
6.2 Dans Google Search Console : VÉRIFIE d'abord que tu es sur la BONNE propriété ([URL]).
    Puis Sitemaps → envoie « sitemap_index.xml ».
6.3 Inspection d'URL → pour chaque page, colle l'adresse → « Demander une indexation ».

===================================================================
VÉRIFICATION FINALE
===================================================================
- Sur chaque page publiée : Ctrl+F « gestion » PUIS « gérer » → il doit y avoir 0 résultat.
- Chaque page a bien 1 seul H1.
- Les barres Titre + Méta sont vertes dans Yoast.
- Donne-moi un RÉCAP page par page de tout ce que tu as modifié.

Commence par l'ÉTAPE 0 et déroule TOUT jusqu'à la vérification finale, de façon autonome, 
en enregistrant au fur et à mesure. Ne t'arrête que si tu es réellement bloqué. 
À la fin, donne-moi le récap complet page par page + la liste des faux avis repérés.
```

---

## Notes pour moi (Claude Code) quand je remplis ce template
- Remplir tous les `[…]` à partir du formulaire + des captures.
- Étapes 1, 2, 3 : lister explicitement par page (l'agent navigateur ne devine pas).
- Si le site a beaucoup de pages, découper : donner une ÉTAPE à la fois.

## Infos à demander au client pour chaque nouveau site
Avant de remplir le template, je pose systématiquement les questions dont j'ai besoin, notamment :
1. **URL du site** + accès (ou captures de chaque page).
2. **Carte G : OUI ou NON ?** (détermine tout le vocabulaire autorisé).
3. **Ville / zone** exacte ciblée (+ communes voisines éventuelles).
4. **Activité** : conciergerie ou sous-location ?
5. **Nom exact de la marque** (orthographe à uniformiser).
6. **Téléphone, e-mail, adresse** (NAP pour la fiche Google).
7. **Réseaux sociaux** réels (vraie page Facebook ? sinon on retire le lien).
8. **Fiche Google Business** : existe déjà ou à créer ? accès partagé ?
9. Points de décision : **témoignages** (vrais/faux/à masquer), **blog** (au client).
→ Ne jamais deviner : si une info manque, la demander.
