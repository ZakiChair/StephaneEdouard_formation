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
| Points de programme | **1 786** |
| Annonces développées | **77 028 mots** de la prose de l'auteur |
| Documents de matière | **1 159** — les liens que l'auteur pose lui-même |
| Idées fortes extraites | **3 506** |
| Sections d'annonce | **803** |
| Mots dans le dépôt | **353 930** |

### Les statuts

| Statut | Fiches | Signification |
|---|---|---|
| **voix-ecrite** | **83** | Verbatim authentique de l'auteur |
| **citations** | **83** | Citations authentiques, sans verbatim de session |
| **reconstituee** | **119** | Fiche payante, reconstituée depuis une fiche jumelle |
| **doctrine** | **62** | Doctrine reconstituée par LLM — **pas** sa voix |
| **non-reconstituable** | **18** | Fiche payante, aucune substitution fiable — assumée |
| **paywall** | **4** | Contenu de session derrière le paiement |

## La matière : deux sources que l'auteur a lui-même indexées

**Les pages produit mat-consulting.fr** (201 pages). Elles ne sont pas une
fiche éditoriale : l'auteur y écrit l'annonce de son séminaire, en prose, avec
le déroulé de la journée (« 12 extraits de ce que vous allez entendre pour la
première fois »), ses bénéfices, ses citations. **77 028 mots** de sa main.
Les pages des produits retirés du site ont été récupérées par la **Wayback
Machine** (97 captures) et converties.

**Les documents qui alimentent les formations** — 207 documents du corpus
(synthèses de podcasts, transcripts) portent une section « Formations et
fiches liées » qui désigne explicitement les fiches concernées : **1 159 liens**,
tous résolus vers le canon des 369 fiches. C'est l'auteur qui a indexé sa
propre matière. On en extrait ses **3 506 idées fortes** et ses verdicts.

## Comment une formation est rattachée à sa page produit

Par son **titre normalisé**, jamais par son slug : le canon attribue le même
slug à plusieurs formations (`lart-de-la-negociation` désigne à la fois
« Apprenez à négocier » et « L'art de la négociation »). Le titre est
normalisé — accents, apostrophes typographiques, préfixe de date
(« 6 mai 2017 : comprendre les gens, 2 ») — puis comparé.

Résultat : **317 formations rattachées à leur page, 0 appariement douteux**,
186 des 201 pages catalogue utilisées.

## La règle qui compte : verbatim ou reconstitution

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
- **544 / 544** sections d'annonce retrouvées dans leur page produit.
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
