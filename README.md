# Stéphane Édouard — les formations, reconstituées par leur matière

Les **369 formations** de Stéphane Édouard. Une fiche = un fichier.

Ce dépôt ne colle pas des citations voisines : il restitue chaque formation
telle que **l'auteur l'a lui-même décrite**, en cinq matériaux, chacun avec sa
provenance.

## Ce que contient une fiche

| Section | Ce qu'elle est | Provenance |
|---|---|---|
| **Le programme** | les chapitres du séminaire, dans l'ordre | tracklist de la page produit |
| **L'annonce du séminaire, écrite par lui** | sa prose, en sections : déroulé numéroté, listes, citations | page produit mat-consulting.fr |
| **La matière qu'il a lui-même déclarée** | ses idées fortes, son verdict final | les documents qu'il a indexés lui-même |
| **Ses développements sur le sujet** | ses passages de vidéo et de podcast | transcripts et synthèses |
| **Verbatim de l'auteur** | le texte de la section « Contenu complet » | fiche de formation |
| **Citations de l'auteur** | les formules entre guillemets | fiche de formation |
| **Reconstitution** | pour les formations payantes : la fiche jumelle, le mode, la confiance | fiche jumelle |

## Les chiffres

| | |
|---|---|
| Fiches | **369** |
| Points de programme | **2 866** (269 fiches) |
| Annonces développées | **135 097 mots** de la prose de l'auteur (221 fiches) |
| Documents de matière | **1 159** — les liens que l'auteur pose lui-même (353 fiches) |
| Idées fortes extraites | **3 506** |
| Pages de l'auteur sur son propre séminaire | **945** (228 fiches) |
| Sections d'annonce | **1 357** |
| Mots dans le dépôt | **793 782** |

### Les statuts

| Statut | Fiches | Signification |
|---|---|---|
| **voix-ecrite** | **83** | Verbatim authentique de l'auteur |
| **citations** | **83** | Citations authentiques, sans verbatim de session |
| **reconstituee** | **119** | Fiche payante, reconstituée depuis une fiche jumelle |
| **doctrine** | **62** | Doctrine reconstituée par LLM — **pas** sa voix |
| **non-reconstituable** | **17** | Fiche payante, aucune substitution fiable — assumée |
| **paywall** | **4** | Contenu de session derrière le paiement |
| **index-catalogue** | **1** | L'index du catalogue lui-même — pas une formation |

## La matière : deux sources que l'auteur a lui-même indexées

**Les pages produit mat-consulting.fr** (201 pages). Elles ne sont pas une
fiche éditoriale : l'auteur y écrit l'annonce de son séminaire, en prose, avec
le déroulé de la journée (« 12 extraits de ce que vous allez entendre pour la
première fois »), ses bénéfices, ses citations. **135 097 mots** de sa main.
Les pages des produits retirés du site ont été récupérées par la **Wayback
Machine** (97 captures) et converties.

**Les documents qui alimentent les formations** — 207 documents du corpus
(synthèses de podcasts, transcripts) portent une section « Formations et
fiches liées » qui désigne explicitement les fiches concernées : **1 159 liens**,
tous résolus vers le canon des 369 fiches. C'est l'auteur qui a indexé sa
propre matière. On en extrait ses **3 506 idées fortes** et ses verdicts.

## Comment une formation est rattachée à sa page produit

Chaque fiche porte l'**URL mat-consulting.fr** dont elle est tirée. C'est la
clé la plus fiable : elle nomme la page exacte, sans interprétation. **214
fiches** se rattachent ainsi.

Quand cette URL ne désigne plus de page — le produit a été retiré du site, ou
la capture de session est vide — on cherche la page du **même séminaire** :

- le **stem du slug** (`like-a-boss-3-...-matin` → `like-a-boss-3-...`) relie
  les captures d'une même journée ;
- à défaut, le **mot le plus distinctif** du titre, à condition qu'une seule
  page du catalogue le porte ;
- dans les deux cas, les titres doivent **désigner le même séminaire** : le
  site réutilise un slug pour un autre produit, et le seul contre-exemple
  (`L'art de la négociation` vs `L'art délicat de la connexion`) a été
  détecté par ce test.

Résultat : **322 fiches rattachées à leur page, 12 dont le séminaire a été
renommé par l'auteur** (« À mort la procrastination » est devenu « Vivre avec
la procrastination »), **0 appariement douteux**, 47 formations sans page
d(product aujourd'hui retirée du site, sans archive).

## Les six sources d'une fiche

Chaque formation est reconstituée à partir de ce que l'auteur a **lui-même**
produit. Les sources sont presented separement, jamais melangees :

| Source | Ce qu'elle est | Fiches |
|---|---|---|
| **Le programme** | la tracklist de la page produit : les chapitres du seminaire, dans l'ordre, avec ses mots | 269 |
| **L'annonce du séminaire** | sa prose sur son seminaire, decoupee en sections, avec le deroule numerote, les listes et les citations | 257 |
| **La matière qu'il a lui-même déclarée** | ses idées fortes et son verdict, extraits des 1 159 documents où il a lui-meme écrit quels fiches ils alimentent | 353 |
| **Ce qu'il a écrit sur son propre séminaire** | les pages de son propre site retrouvé **par le nom du seminaire** — « Devenez intéressant, mod. 3 : passez maitre en story-telling » | 228 |
| **Ce que la fiche dit de ce séminaire** | sa doctrine : points clés, concepts enseignés, exercices, citations | 331 |
| **Verbatim et citations** | le texte de la section « Contenu complet », et les formules entre guillemets | 83 |

Les sources ne se recouvrent pas : **la page de l'auteur sur son propre
séminaire** est un matériau différent de l'annonce de la page produit. La
première est un article ou une actualité qu'il a écrit sur son séminaire ;
la seconde est la fiche de vente de la journée.

**367 des 369 formations** portent au moins une source. Les deux exceptions
sont dites dans leur fichier.

## La règle qui compte : verbatim ou reconstitution## La règle qui compte : verbatim ou reconstitution

Trois statuts ne se valent pas. Confondre les deux, c'est attribuer à l'auteur
des phrases qu'il n'a pas écrites.

- **voix-ecrite** — le verbatim est de l'auteur. On le cite comme citation,
  avec l'identifiant de la fiche.
- **citations** — les formules entre guillemets sont authentiques et vérifiées
  mot pour mot. Le reste est de la doctrine.
- **doctrine** — rédigée par un LLM à partir des sources publiques. Elle décrit
  sa pensée, mais **ce n'est pas sa voix** : elle ne se cite jamais comme
  citation d'auteur.

Et pour les formations payantes :

- **reconstituee** — le contenu vient d'une *autre* fiche. On cite **la fiche
  jumelle**, jamais la fiche vide.
- **non-reconstituable** — aucune fiche du corpus ne porte ce thème de façon
  assez proche. Une substitution serait une invention.

```
C013 « Like a boss, 3 : Séduire et fidéliser ses clients A VIE (après midi) »
  → reconstituée depuis C006
  → citer : C006, en annonçant « reconstitution depuis C006 »
```

## Fiabilité

Contrôles passés sur l'ensemble du dépôt :

- **3 506 / 3 506** idées fortes retrouvées **mot pour mot** dans le document
  que la fiche cite.
- **947 / 947** sections d'annonce retrouvées dans leur page produit.
- **1 285 / 1 285** passages de développement retrouvés mot pour mot dans la page d'archive qu'elle nomme.
- **1 776 / 1 776** blocs de doctrine retrouvés mot pour mot dans la fiche d'origine.
- **257 / 257** citations de fiche vérifiées mot pour mot.
- **0** fichier contenant du déchet de page (widgets YouTube, navigation).
- **0** secret dans l'arbre.

## Les doublons

Le corpus contient **98 groupes de fiches au même titre** (275 fiches au total) :
sessions différentes, scrapings successifs, et parfois la même formation
répartie dans deux catégories. **Aucune fiche n'est supprimée** — le
dédoublonnage n'est pas fait, il est documenté dans `data/doublons-titre.json`.
Les catégories ont été normalisées en 14 catégories canoniques ; la valeur brute
reste dans le front-matter (`categorie_brute`).

## Structure

```
INDEX.md                        table des 369 fiches, avec lien vers chaque fichier
formations/<categorie>/         un fichier .md par fiche
data/
  index-canonique.json          les 369 fiches : id, chemin, catégorie, titre, taille
  reconstitution.json            programme, annonce et matière de chaque formation
  reconstitutions.json           les 137 fiches vides et leur jumelle
  doublons-titre.json           les 98 groupes de fiches au même titre
  mesures.json                  les mesures du corpus (registres, couches, comptes)
docs/                           les 20 livrables d'analyse
```

## Source

Corpus local : `/root/migration-docker-stephane/Bartilabas/formation/StephaneEdouard/`
— pages produit mat-consulting.fr, podcasts, vidéos, archive du site de l'auteur.
Analyse complète dans `docs/`.
