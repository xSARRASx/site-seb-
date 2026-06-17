# Prompt à coller dans l'autre conversation Claude (site de l'équipe)

> Copie tout le bloc ci-dessous et colle-le dans la conversation Claude qui gère
> le site de ton équipe. Joins aussi le fichier `index.html` à cette
> conversation : il contient la version de référence à intégrer.

---

Salut ! Je veux ajouter une nouvelle section **« Suivi SEO »** à notre site
d'équipe (la petite case SEO du tableau de bord). J'ai déjà un prototype
fonctionnel en un seul fichier HTML autonome (je le joins à ce message) : je veux
que tu l'intègres proprement à notre site existant, en réutilisant notre design
et notre stack actuelle (ne casse pas la mise en page existante).

**À quoi sert cette section :** c'est un outil de suivi interne. Notre
collaboratrice Camille y ajoute, site client par site client, l'avancement du
travail SEO et tout ce qu'elle doit nous transmettre.

**Pour chaque site client, on doit pouvoir saisir et afficher :**
- Nom du client
- URL du site (lien cliquable)
- Activité : « Conciergerie » ou « Sous-location »
- Ville / zone
- Carte G : Oui / Non
- Statut : « À faire » / « En cours » / « Terminé » (modifiable en un clic)
- E-mail du client (lien mailto cliquable)
- Une note libre (remarques de Camille)
- Des fichiers joints (captures, rapport, identifiants) téléchargeables

**Affichage attendu :**
- Des cartes (une par site) avec badges colorés selon le statut
- Des compteurs en haut : total / à faire / en cours / terminés
- Des filtres par statut
- Un bouton « + Ajouter un site » qui ouvre un formulaire (modal)
- Possibilité de modifier et supprimer un site
- Un bandeau de rappel affiché en haut : « Loi Hoguet — pour un client sans
  Carte G, ne jamais utiliser les mots gestion / gestionnaire / gestion locative
  (ni gestion Airbnb). Vocabulaire autorisé : conciergerie, location courte
  durée, location saisonnière, sous-location. »

**Important sur le stockage des données :**
Le prototype joint stocke les données dans le navigateur (localStorage), donc
elles ne sont PAS partagées entre Camille et moi. Pour notre usage réel, il faut
que les données soient **partagées et persistées côté serveur** : Camille saisit
depuis son poste, et nous voyons tous la même chose. Merci de :
1. Me dire quelle solution de stockage tu recommandes avec notre stack actuelle
   (base de données, API, ou service type Supabase/Firebase selon ce qu'on a
   déjà), AVANT de coder le backend.
2. Intégrer d'abord l'interface visuelle dans le site, puis brancher le stockage
   partagé.
3. Prévoir que seuls les membres de l'équipe (dont Camille) puissent ajouter /
   modifier (selon notre système d'authentification actuel).

Avant de commencer, dis-moi ce dont tu as besoin comme infos sur notre stack
(framework, base de données, auth) pour faire l'intégration la plus propre
possible.
