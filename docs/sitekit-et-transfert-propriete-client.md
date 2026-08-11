# Site Kit + transfert de propriété au client — procédure réutilisable

> **But :** sur CHAQUE site, (1) installer **Google Site Kit** connecté au **compte Google du client**,
> et (2) **transférer la propriété** des outils Google (Search Console + fiche Google Business) **au client**,
> pour qu'il reste propriétaire de ses données une fois l'accompagnement terminé.
>
> À faire une fois le SEO on-page + Search Console déjà en place (étapes du process principal).

---

## ⚠️ Le point qui coince (à comprendre avant)

Pour connecter Site Kit / ajouter un propriétaire **avec l'adresse Gmail du client**, il faut être
**connecté à CE compte Google** dans le navigateur. **Nous n'avons pas le mot de passe du client.**

👉 Deux façons de faire, à choisir par site :

- **Option A — le client fait le clic Google lui-même** (recommandé, le plus propre).
  Nous installons/préparons tout ; au moment du « Se connecter avec Google », c'est le client
  (connecté à son propre Gmail) qui clique. Résultat : Site Kit et la propriété sont **directement au nom du client**.
- **Option B — on prépare sous notre compte, puis on ajoute le client comme propriétaire.**
  Utile si le client n'est pas dispo. On connecte Site Kit / on crée la propriété sous notre Google,
  puis on **ajoute l'email du client en « Propriétaire »** et on lui **transfère la propriété principale**.
  Le client reçoit une invitation à **accepter**.

> Dans les deux cas, l'**email Google du client** est indispensable. **Le demander avant** (ne jamais deviner).

---

## Infos à réunir par site (avant de lancer)

1. **URL** du site + accès `/wp-admin`.
2. **Email Google (Gmail) du client** — celui qui doit rester propriétaire.
3. Search Console : propriété déjà créée ? (oui, si le process principal a été suivi).
4. Fiche Google Business : existe ? créée sous quel compte (agence ou client) ?
5. Option **A** (client clique) ou **B** (on prépare puis on transfère) ?

---

## Partie 1 — Installer Google Site Kit

Dans `wp-admin` :
1. **Extensions → Ajouter → « Site Kit by Google »** → Installer → Activer.
2. **Site Kit → Démarrer la configuration → « Se connecter avec Google ».**
   - **Option A** : le client, connecté à SON Gmail, clique et autorise. ✅ Site Kit est à son nom.
   - **Option B** : on se connecte avec notre compte agence (celui qui possède déjà la Search Console).
3. Autoriser les accès demandés → **vérifier la propriété** (Site Kit la relie automatiquement à la Search Console).
4. Connecter **Search Console** (inclus d'office). Analytics = optionnel (à activer seulement si un compte GA4 existe).
5. Vérifier que le tableau de bord Site Kit s'affiche dans `wp-admin` (impressions / clics).

> Site Kit **n'améliore pas le SEO en soi** : il affiche les stats Google dans WordPress et confirme le lien
> avec la Search Console. Utile pour le client, mais ce n'est **pas** un substitut au travail on-page.

---

## Partie 2 — Transférer la Search Console au client

`search.google.com/search-console` → bonne propriété → **Paramètres → Utilisateurs et autorisations** :
1. **Ajouter un utilisateur** → email Google du client → autorisation **« Propriétaire »**.
2. Prévenir le client : il reçoit l'accès, il peut **confirmer**.
3. (Option A) Si le client a créé la propriété lui-même, il est **déjà** propriétaire : rien à transférer,
   éventuellement nous ajouter, nous, en « Lecteur » le temps de l'accompagnement.

> ⚠️ Toujours vérifier qu'on est sur la **BONNE propriété** (piège déjà vécu : agir sur le site d'un autre client).

---

## Partie 3 — Transférer la fiche Google Business au client

`business.google.com` (ou l'appli) → bonne fiche → **Paramètres → Personnes et accès** :
1. **Ajouter** → email Google du client → rôle **« Propriétaire »**.
2. Une fois le client accepté, **transférer la propriété principale** au client (« Faire de … le propriétaire principal »).
3. Nous pouvons **rester « Gestionnaire »** le temps de l'accompagnement, puis nous retirer.

> Rappel : la **vérification** (souvent vidéo) et l'ajout des **photos** restent **côté client**.
> Catégorie conforme : **« Conciergerie privée »**. Vocabulaire Loi Hoguet respecté (pas de « gestion » sans Carte G).

---

## Prompt navigateur (extension « Claude pour Chrome ») — à coller

> Onglet `wp-admin` du site au premier plan, connecté. **Option A** : demander au client d'être connecté
> à son Gmail sur un onglet Google avant de lancer le « Se connecter avec Google ».

```
Tu agis dans mon navigateur. Fais ceci en autonomie et donne-moi un récap final.

CONTEXTE
- Site : [URL]        - Client : [NOM]
- Email Google du client (doit rester propriétaire) : [EMAIL CLIENT]
- Mode : [A = le client cliquera lui-même le « Se connecter avec Google » / B = je prépare puis j'ajoute le client]

1) SITE KIT
- wp-admin → Extensions → Ajouter → « Site Kit by Google » → Installer → Activer.
- Site Kit → Démarrer la configuration → « Se connecter avec Google ».
  · Mode A : ARRÊTE-TOI ici et dis-moi de faire cliquer le client (connecté à [EMAIL CLIENT]).
  · Mode B : connecte-toi avec le compte agence déjà propriétaire de la Search Console.
- Termine la configuration, connecte Search Console, vérifie que le tableau de bord s'affiche.

2) SEARCH CONSOLE — ajouter le client en propriétaire
- search.google.com/search-console → VÉRIFIE que tu es sur la propriété [URL].
- Paramètres → Utilisateurs et autorisations → Ajouter un utilisateur → [EMAIL CLIENT] → « Propriétaire ».

3) FICHE GOOGLE BUSINESS (si elle existe)
- business.google.com → la bonne fiche → Paramètres → Personnes et accès → Ajouter → [EMAIL CLIENT] → « Propriétaire ».
- Si possible, transfère-lui la propriété principale.

RÉCAP : indique ce qui est fait, ce qui attend une action du client (accepter l'invitation, vérif vidéo, photos),
et ce qui est resté bloqué.
```

---

## Statut par site (à tenir à jour)

| Site | Email Google client | Site Kit | GSC → client | GMB → client |
|---|---|---|---|---|
| D'Or Tranquille | _à demander_ | — | — | — |
| Valse de Lin | _à demander_ | — | — | GMB créée (sous notre compte) → à transférer |
| Léandro | _à demander_ | — | — | pas de fiche (à créer d'abord ?) |
