# Léandro — Création fiche Google Business « zone desservie »

> Léandro n'a **aucune fiche Google Business**. Comme le siège est à Paris (pas d'adresse à Grenoble),
> on crée une fiche **« zone desservie »** (adresse masquée), ce qui est la bonne option pour une conciergerie de proximité.
>
> ⚠️ La **vérification** (souvent vidéo) et l'ajout des **photos** = **côté client** (Lucie/Jonathan).
> Idéalement, créer la fiche **avec le compte Google du client** pour qu'il en soit propriétaire dès le départ
> (voir `docs/sitekit-et-transfert-propriete-client.md`). Sinon on la crée, puis on la transfère.

## Infos NAP (à saisir, conformes au site)
- **Nom** : Léandro Conciergerie
- **Catégorie** : **Conciergerie privée** (seule catégorie conciergerie proposée par Google)
- **Zone desservie** : Grenoble, Grésivaudan, Voiron, Chambéry et les stations (Chamrousse, Les 7 Laux). 🚫 pas Vercors/Aix-les-Bains.
- **Téléphone** : 07 75 67 42 16
- **Site** : https://leandroconciergerie.fr
- **Horaires** : tous les jours 9h–20h
- **Description** (vocabulaire conforme Loi Hoguet, sans « gestion ») :
  > Léandro Conciergerie accompagne les propriétaires de locations courte durée à Grenoble, dans le Grésivaudan,
  > à Voiron, à Chambéry et dans les stations environnantes. Comme co-hôte, nous prenons en charge l'accueil des
  > voyageurs, le ménage, le linge et l'optimisation de vos annonces, pour des séjours réussis et des logements
  > toujours impeccables. Vous gardez la maîtrise de vos tarifs et de votre calendrier.

## Prompt navigateur (extension « Claude pour Chrome »)

```
Tu agis dans mon navigateur. Je veux créer une fiche Google Business pour mon client. Fais-le en autonomie
et arrête-toi aux étapes qui exigent une action humaine (connexion au compte, vérification). Récap à la fin.

CONTEXTE
- Ouvre business.google.com (ou google.com/business).
- Compte Google à utiliser : [EMAIL GOOGLE DU CLIENT si dispo, sinon notre compte agence puis on transférera].

CRÉATION
- « Gérer maintenant » / « Ajouter une entreprise ».
- Nom : Léandro Conciergerie.
- Catégorie : « Conciergerie privée ».
- « Vous voulez ajouter un établissement… que les clients peuvent visiter ? » → NON (service à domicile).
- Zone desservie : ajoute Grenoble, Grésivaudan, Voiron, Chambéry, Chamrousse, Les 7 Laux.
  N'ajoute PAS Vercors ni Aix-les-Bains.
- Téléphone : 07 75 67 42 16.  Site : https://leandroconciergerie.fr.
- Horaires : lundi à dimanche, 9h00–20h00.
- Description : colle le texte de description conforme (fourni ci-dessus).

VÉRIFICATION
- Lance la procédure de validation, mais NE tente PAS de fausse validation : si Google demande une
  vérification vidéo ou par courrier, ARRÊTE-TOI et signale-le-moi (c'est au client de la faire).

RÉCAP : indique ce qui est créé, ce qui attend le client (vérification, photos), et ce qui a bloqué.
```

## Après création
- Ajouter le **client comme propriétaire** (ou lui transférer la propriété principale) — cf. doc transfert.
- Le client fait la **vérification vidéo** + ajoute **photos** (logo, logements, équipe).
- Vérifier la **cohérence NAP** : nom / téléphone identiques entre le site et la fiche.
