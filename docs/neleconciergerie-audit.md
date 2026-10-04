# Nele Conciergerie — Le Cannet (06) — SEO LOCAL — Audit + notes

> Nele Muylle · neleconciergerie.com · **sans Carte G**. Prestation : **SEO LOCAL uniquement** (base déjà faite par Camille en juillet : Yoast titres+métas sur Accueil/À propos/Services/Contact, JSON-LD, sitemap, ALT images. Site en ligne et indexable).
> NAP : **06 20 40 32 30** · **24 avenue Lacour, 06110 Le Cannet** · SIRET **105 742 027 00011**.
> E-mail : site = **contact@neleconciergerie.com** / formulaire = **contact@neleconciergerie.fr** → ⚠️ à trancher. Accès : identifiant `camille` (mdp → Camille, jamais stocké ici).

## Zone CONFIRMÉE (formulaire Nele)
- **Cannes · Le Cannet (siège) · Mougins.**

## ⚠️ Particularités de CETTE installation (important)
- **Theme Builder PLANTE** sur ce site → en-tête + pied de page **intégrés dans chaque page**. **NE PAS utiliser le Theme Builder.**
- **Polylang installé** mais versions **NL et EN non faites** → **ne pas toucher aux langues sans Camille**.
- **Éditeur Yoast en masse ne marche pas** → régler **page par page**.
- **E-mail incohérent** : site `.com` vs formulaire `.fr` → **trancher avant la fiche Google** (cohérence NAP). Ne rien changer sans validation.

## Points de vigilance
- **Loi Hoguet** (sans Carte G) : **jamais** « gestion / gestionnaire / gérer / gestion locative ». Utiliser : conciergerie, location courte durée, location saisonnière, pilotage, coordination, prestataire, suivi, prise en charge, optimisation, accompagnement.
- **Pas de Facebook/Instagram connus** → ne rien brancher (aucune URL).
- **Gmail pour Site Kit : aucun connu** → utiliser le compte agence martinmorebkk@gmail.com, ou en demander un à Nele via Camille.
- **Ne rien inventer** (avis/témoignages).

## Reste à faire (d'après la fiche)
- Search Console, fiche Google Business, **og:image par défaut dans Yoast**, réseaux sociaux (si URLs un jour).

## Prompt d'AUDIT (lecture seule) — à coller dans l'extension
```
Tu agis dans mon navigateur sur neleconciergerie.com (WordPress + Elementor + Yoast + Polylang).
MODE LECTURE SEULE : tu n'enregistres, ne modifies, ne publies, ne supprimes RIEN. Tu OBSERVES et tu fais un rapport.
Contexte : conciergerie, sans Carte G, zone Cannes / Le Cannet (siège) / Mougins. Base SEO déjà faite (Yoast titres+métas Accueil/À propos/Services/Contact, JSON-LD, sitemap, ALT).
ATTENTION : NE touche à RIEN. En-tête/pied de page sont intégrés dans chaque page (Theme Builder plante). Polylang présent (NL/EN non faites) — ne change pas de langue.
Donne-moi, structuré :
1) TOUTES les pages (menu + sitemap) : titre, URL/slug, statut, langue + articles.
2) Par page : H1 exact (0/plusieurs = signale), H2/H3, Titre SEO + Méta + mot-clé Yoast (encart Yoast). Signale les vides.
3) « conciergerie » / « conciergerie Cannes » / « conciergerie Le Cannet » / « Airbnb » bien placés (titre, H1, corps) sur Accueil/Services ? Pages par ville (Cannes/Le Cannet/Mougins) ?
4) VOCABULAIRE : occurrences « gestion / gestionnaire / gérer / gestion locative » — page, élément, phrase exacte (Ctrl+F « gestion » PUIS « gérer » séparément).
5) JSON-LD / schema : présent ? LocalBusiness ? téléphone 06 20 40 32 30 + adresse 24 avenue Lacour affichés ? zone correcte ?
6) E-MAIL : repère partout l'adresse affichée — est-ce « .com » ou « .fr » ? Signale CHAQUE endroit (incohérence connue à trancher).
7) IMAGES sans ALT (où). Photos de stock / hors zone ? og:image par défaut réglé dans Yoast (Réglages → Réseaux sociaux) ?
8) LIENS : boutons « # », réseaux vides, lien téléphone (tel:), pages orphelines.
9) AVIS/TÉMOIGNAGES : présents ? réels ou inventés ?
10) FAUTES + textes de template oubliés (« Hello world! », Uncategorized, archives auteur exposant l'e-mail) + incohérences de marque (Nele Conciergerie).
11) RÉGLAGES : langue par défaut, indexation (Réglages→Lecture), permaliens, sitemap. Search Console / Site Kit déjà là ? Réseaux sociaux renseignés dans Yoast ?
12) ZONE : communes citées actuellement (Cannes / Le Cannet / Mougins ?).
Rends-moi TOUT ça page par page. NE MODIFIE RIEN.
```

## Statut
- [x] Audit fait (lecture seule)
- [x] E-mail tranché : **site 100 % `.com`**, aucun `.fr` → on garde `contact@neleconciergerie.com` (vérifier juste que cette boîte reçoit bien)
- [ ] Corrections SEO local appliquées (mots-clés, maillage, schema, nettoyage)
- [ ] Search Console + Site Kit (compte agence martinmorebkk@gmail.com)
- [ ] Fiche Google Business

---

## ✅ AUDIT FAIT (lecture seule) — synthèse
**Points OK** : **0 « gestion/gérer/gestionnaire »** (clause Loi Hoguet nickel en ML : « aucun encaissement de loyers… ») ✔ · 1 H1/page ✔ · titres+métas remplis sur 4 pages ✔ · toutes images avec ALT ✔ · tél +33620403230 partout ✔ · zone Cannes/Le Cannet/Mougins cohérente ✔ · indexation ON, permaliens propres, sitemap/robots OK ✔ · og:image par défaut réglée ✔ · **e-mail 100 % `.com`** (pas de `.fr`) ✔.

**À corriger :**
1. **Mot-clé Yoast VIDE sur 5 pages** (0/5, « expression clé non définie »).
2. **Pas de schema LocalBusiness** (seulement WebPage/Breadcrumb/WebSite). Yoast « Entité » coché mais **nom + logo vides**. → ni tél, ni adresse, ni zone dans le schéma.
3. **Archive auteur expose le Gmail** : `/author/nelemuyllegmail-com/`, title+H1 = « nelemuylle@gmail.com », indexable + dans le sitemap (nom public WP = l'e-mail).
4. **Restes de template indexables** : article **« Hello world! »** + commentaire par défaut, catégorie **Uncategorized** (install EN), brouillon **Privacy Policy** (titre EN), fil d'Ariane schéma « Home ».
5. **Mentions légales** : titre SEO + méta vides.
6. **Pas de pages par ville** ; « conciergerie » absent des 2 H1 (Accueil/Services, H1 émotionnels) ; « conciergerie Le Cannet » jamais en expression exacte.
7. **Search Console / Site Kit absents** (champ vérif Yoast vide, pas de Site Kit).
8. **À trancher** : Accueil dit « installée à Cannes / je vis à Cannes » vs À propos « installée au Cannet » (siège = Le Cannet). → cohérence lieu.
9. **4 badges langues sans lien** (FRANÇAIS/NEDERLANDS/ENGLISH/ESPAÑOL) sur À propos = liens morts trompeurs (Polylang NL/EN non faits). → **voir Camille** (ne pas toucher aux langues sans elle).
10. Mineurs : og:image Accueil = logo carré (pas idéal) ; fuseau WordPress UTC+0 (→ Paris) ; chiffres « 4,9/5 · 20+ biens · 5 ans » sans source (à faire valider par Nele, pas de faux avis) ; 10 MAJ plugins en attente.

## Corrections SEO local prêtes
1. **Mots-clés Yoast** par page + titre/méta sur Mentions légales.
2. **Schema LocalBusiness** (Elementor → Code perso, `<head>`, tout le site) : NAP complet + zone 3 communes. Remplir aussi Yoast → Représentation du site (nom « Nele Conciergerie » + logo).
3. **Archive auteur** : nom public → « Nele Conciergerie » (≠ e-mail), slug auteur hors e-mail, **noindex archives auteur + catégories/étiquettes**.
4. **Nettoyage** : corbeille « Hello world! » + commentaire ; renommer « Uncategorized » → « Conseils » ; supprimer brouillon Privacy Policy ; fil d'Ariane « Home » → « Accueil ».
5. **Renforcer** « conciergerie » + ville dans l'intro/H2 d'Accueil & Services (sans casser les H1 émotionnels), 0 « gestion/gérer ».
6. **Search Console + Site Kit** (martinmorebkk@gmail.com).
7. **Mineurs** : og:image Accueil → photo villa ; fuseau → Paris.
8. **À voir avec Camille/Nele** : « Cannes » vs « Le Cannet » (lieu) ; 4 badges langues morts ; chiffres à sourcer ; boîte `.com` reçoit bien ?

## Prompt de CORRECTION (à coller dans l'extension)
```
Tu agis dans mon navigateur sur neleconciergerie.com (WordPress + Elementor + Yoast + Polylang). Tu PEUX modifier et tu ENREGISTRES chaque changement (Mettre à jour).
INTERDICTIONS ABSOLUES : ne touche PAS au Theme Builder (il plante — en-tête/pied de page sont intégrés dans chaque page) ; ne touche PAS aux langues/Polylang (NL/EN non faites) ; reste en FRANÇAIS.
Loi Hoguet (sans Carte G) : INTERDIT « gestion / gestionnaire / gérer / gestion locative ». Utilise : conciergerie, location courte durée, location saisonnière, pilotage, coordination, prestataire, suivi, prise en charge, optimisation, accompagnement. Zone : Cannes, Le Cannet (siège), Mougins.

Fais dans l'ordre, en enregistrant à chaque fois :

1) YOAST — mot-clé principal + (si besoin) titre/méta, PAGE PAR PAGE (l'éditeur en masse ne marche pas ici) :
   - Accueil : mot-clé « conciergerie Cannes ».
   - Services : mot-clé « conciergerie Cannes ».
   - À propos : mot-clé « conciergerie Côte d'Azur ».
   - Contact : mot-clé « conciergerie Le Cannet ».
   - Mentions légales : mot-clé « mentions légales conciergerie » + Titre SEO (ex. « Mentions légales | Nele Conciergerie ») + méta courte.
   Ne laisse AUCUN mot-clé vide.

2) YOAST — Représentation du site (Réglages) : type « Entité/Organisation », Nom = « Nele Conciergerie », Logo = le logo du site (médiathèque). Dans Réglages → Réseaux sociaux : laisse vide (aucune URL connue). Image de site (og) : mets la photo « villa-terrasse-cote-azur » comme image par défaut.

3) SCHEMA LocalBusiness — Elementor → Code personnalisé (Custom Code), nom « Schema LocalBusiness », emplacement <head>, condition « Tout le site ». Colle EXACTEMENT :
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Nele Conciergerie",
  "description": "Conciergerie et location courte durée à Cannes, Le Cannet et Mougins.",
  "url": "https://neleconciergerie.com",
  "email": "contact@neleconciergerie.com",
  "telephone": "+33620403230",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "24 avenue Lacour",
    "postalCode": "06110",
    "addressLocality": "Le Cannet",
    "addressCountry": "FR"
  },
  "areaServed": ["Cannes","Le Cannet","Mougins"]
}
</script>
Vérifie qu'il n'y a pas déjà un LocalBusiness en double. (Si Custom Code indisponible, DIS-LE, ne touche pas au Theme Builder.)

4) CONTENU (sans casser les H1 existants) :
   - Accueil + Services : fais apparaître naturellement « conciergerie » + une ville (Cannes / Le Cannet) dans le 1er paragraphe et dans un H2. NE mets AUCUN « gestion/gérer ».
   - N'invente AUCUN avis ni chiffre. Ne touche pas aux chiffres existants (4,9/5, 20+, 5 ans).

5) ARCHIVE AUTEUR (expose le Gmail) :
   - Profil utilisateur : « Nom à afficher publiquement » = « Nele Conciergerie » (PAS l'e-mail). Change aussi le pseudo/slug si l'URL auteur contient l'e-mail.
   - Yoast → Réglages → Types de contenu / Archives : archives d'auteur en noindex ; catégories et étiquettes en noindex aussi.

6) NETTOYAGE TEMPLATE :
   - « Hello world! » → corbeille + supprime son commentaire par défaut.
   - Catégorie « Uncategorized » → renomme « Conseils » (slug conseils).
   - Brouillon « Privacy Policy » (titre anglais) → corbeille.
   - Yoast → Fil d'Ariane : libellé de l'accueil « Home » → « Accueil ».

7) MINEUR : Réglages → Général → Fuseau horaire = Paris.

8) SEARCH CONSOLE + SITE KIT :
   - Installe/active « Site Kit by Google », connecte-le au compte Google martinmorebkk@gmail.com, autorise Search Console, N'ACTIVE PAS Analytics.
   - Propriété https://neleconciergerie.com/ créée + sitemap sitemap_index.xml soumis.
   - Demande l'indexation de : Accueil, Services, Contact, À propos (dans la limite du quota du jour).

9) VÉRIFS FINALES : Ctrl+F « gestion » PUIS « gérer » sur chaque page = 0 occurrence. Aucun avis inventé. Aucun lien réseau social ajouté. Theme Builder et langues NON touchés.

NE touche PAS aux 4 badges langues (FRANÇAIS/NEDERLANDS/ENGLISH/ESPAÑOL) de la page À propos : on verra avec Camille. Dis-moi ce que tu as changé page par page.
```

---

## ✅ APPLIQUÉ (04/10/2026) — SEO local fait
- **Mots-clés Yoast** (5/5) : Accueil + Services = « conciergerie Cannes » ; À propos = « conciergerie Côte d'Azur » ; Contact = « conciergerie Le Cannet » ; Mentions légales = « mentions légales conciergerie » (+ titre + méta). Aucun vide.
- **Contenu** : Accueil 1er § enrichi (conciergerie + Cannes/Le Cannet/Mougins) + H2 « Une conciergerie d'exception à Cannes » ; Services 1er § + H2 « Conciergerie & intendance à Cannes ». H1 conservés.
- **Yoast Représentation** : Entité « Nele Conciergerie » + logo ; sociaux vides ; og par défaut = villa (déjà réglée).
- **Archive auteur** : nom public + pseudo « Nele Conciergerie », URL → `/author/nele-conciergerie/` (extension Edit Author Slug installée) ; noindex archives auteur + catégories + étiquettes.
- **Nettoyage** : « Hello world! » + commentaire + brouillon Privacy Policy → corbeille ; « Uncategorized » → « Conseils » (slug conseils) ; fil d'Ariane « Home » → « Accueil » ; fuseau → Paris.
- **Search Console + Site Kit** : connectés (martinmorebkk@gmail.com, sans Analytics) ; propriété https://neleconciergerie.com/ ; sitemap `sitemap_index.xml` = « Opération effectuée » (0 page découverte au contrôle = normal, site récent) ; indexation demandée Accueil/Services/Contact/À propos.
- **Vérif** : 0 « gestion » / 0 « gérer » ✔ ; aucun avis/chiffre inventé (4,9/5, 20+, 5 ans conservés) ; aucun réseau ; Theme Builder + Polylang non touchés ✔.

### ✅ Schema RÉSOLU (3e passe)
- 1re passe : `@context` + `url` **vides** (effacés au copier-coller) → invalide.
- 2e passe : URL recollées → **liens Markdown `[…](…)`** → toujours cassé.
- 3e passe (OK) : édition **à la main** + **champ `url` supprimé** (optionnel) → **`"@context": "https://schema.org"` en texte brut, JSON valide, 1 seul LocalBusiness** (vérifié sur le script HTML public ; view-source bloqué par l'outil mais contrôle fait directement). ✔
- 💡 **Leçon pour les prochains sites** : les URL dans un JSON-LD se cassent au copier-coller (vide ou Markdown). → faire **éditer le code à la main** par l'extension, et garder `url` facultatif.

## 🏁 NELE — SEO LOCAL FINI (04/10/2026)
Tout fait : mots-clés Yoast 5/5, contenu renforcé, entité+logo, schema LocalBusiness valide, archive auteur corrigée, nettoyage template, Search Console + Site Kit, indexation demandée. 0 « gestion/gérer ». Theme Builder + langues non touchés.
**Reste non-SEO (Camille/Nele)** : badges langues morts (À propos) ; « Cannes » vs « Le Cannet » (récit perso) ; boîte `.com` reçoit bien ? ; fiche Google Business (accès Nele). **Demain** : revérifier indexation Services/Contact/À propos.

### Reste (toi / Camille / Nele)
- Confirmer le **fix schema** ci-dessus.
- **Demain** : revérifier indexation Services/Contact/À propos (quota).
- **Camille/Nele** : 4 badges langues morts (À propos) ; « Cannes » vs « Le Cannet » (récit perso) ; boîte `.com` reçoit bien ?
- **Fiche Google Business** (accès Nele).
