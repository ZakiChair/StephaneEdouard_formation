# Stéphane Édouard — les formations, reconstituées

Les **369 formations** de Stéphane Édouard, en un dépôt navigable : une fiche =
un fichier, avec son identifiant canonique, sa catégorie, son statut et ses
dénominateurs.

Chaque fiche porte **tout le contenu gratuit de l'auteur** rattaché à son
champ thématique, organisé par provenance et jamais mélangé.

## Ce que contient une fiche

| Section | Ce qu'elle est | Provenance |
|---|---|---|
| **Ce que l'auteur a écrit sur cette formation** | tracklist (le programme), l'annonce du séminaire écrite par lui, « ce que vous apprendrez », durée, prix, note | page produit mat-consulting.fr |
| **Verbatim de l'auteur** | le texte de la section « Contenu complet » | fiche de formation |
| **Citations de l'auteur** | les formules entre guillemets | fiche de formation |
| **Ce qu'il a dit sur ce thème (vidéoscopie)** | passages verbatim de ses vidéos | transcripts YouTube (`T###`) |
| **Ce qu'il a dit sur ce thème (podcasts)** | passages verbatim de ses podcasts | synthèses (`S###`) |
| **Ses écrits sur ce thème** | passages verbatim de son ancien site | archive `web-*` |
| **Reconstitution** | pour les formations payantes : la fiche jumelle, le mode d'appariement, la confiance | fiche jumelle |
| **La parole des participants** | forum et témoignages | archive `tierce-*` |

## Les chiffres

| | |
|---|---|
| Fiches | **369** |
| Tracklists (le programme de chaque séminaire) | **1 839 items** |
| Annonces de séminaire écrites par lui | **174 fiches** |
| Extraits verbatim rattachés | **4 308** |
| Mots dans le dépôt | **~632 000** |
| Fiches avec au moins un extrait de l'auteur | **369 / 369** |

### Statuts

| Statut | Fiches | Signification |
|---|---|---|
| **voix-ecrite** | **83** | Verbatim authentique de l'auteur |
| **citations** | **83** | Citations authentiques, sans verbatim de session |
| **reconstituee** | **119** | Fiche payante, reconstituée depuis une fiche jumelle |
| **doctrine** | **62** | Doctrine reconstituée par LLM — **pas** sa voix |
| **non-reconstituable** | **18** | Fiche payante, aucune substitution fiable — assumée |
| **paywall** | **4** | Contenu de session derrière le paiement |

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

## D'où vient le contenu

Quatre sources, quatre provenances, jamais mélangées :

1. **Les pages produit mat-consulting.fr** (201 pages) — la source la plus
   proche : elle parle *du* séminaire. Tracklist, annonce rédigée par lui,
   objectifs, extrait vidéo. Les pages des produits retirés ont été récupérées
   par la **Wayback Machine** (97 captures) et converties.
2. **Les transcripts YouTube** (407 fichiers) — sa voix, à l'oral.
3. **Les synthèses de podcasts** (343 fichiers) — résumés structurés de ses
   vidéos et podcasts.
4. **L'archive de son ancien site** (1 564 pages) — ses écrits. Les pages
   `web-*` sont de lui ; les `tierce-*` sont la parole des participants et ne
   sont **jamais** citées comme la sienne.

## Fiabilité

Contrôles passés sur l'ensemble du dépôt :

- **4 308 / 4 308** extraitsverbatim retrouvés **mot pour mot** dans le fichier
  source que la fiche cite.
- **257 / 257** citations de fiche vérifiées mot pour mot.
- **0** fichier contenant du déchet de page (widgets YouTube, navigation).
- **0** secret dans l'arbre.
- Chaque chiffre de ce README porte son dénominateur.

## Les doublons

Le corpus contient **98 groupes de fiches au même titre** (275 fiches au total) :
sessions différentes, scrapings successifs, et parfois la même formation
répartie dans deux catégories. **Aucune fiche n'est supprimée** — le dédoublonnage
n'est pas fait, il est documenté dans `data/doublons-titre.json`. Les catégories
ont été normalisées en 14 catégories canoniques ; la valeur brute reste dans le
front-matter (`categorie_brute`).

## Structure

```
INDEX.md                        table des 369 fiches, avec lien vers chaque fichier
formations/<categorie>/         un fichier .md par fiche
data/
  index-canonique.json          les 369 fiches : id, chemin, catégorie, titre, taille
  reconstitutions.json          les 137 fiches vides et leur jumelle
  pages-produit.json            les tracklists et annonces extraites des pages produit
  doublons-titre.json           les 98 groupes de fiches au même titre
  mesures.json                  les mesures du corpus (registres, couches, comptes)
docs/                           les 20 livrables d'analyse
```

## Source

Corpus local : `/root/migration-docker-stephane/Bartilabas/formation/StephaneEdouard/`
— pages produit mat-consulting.fr, podcasts, vidéos, archive du site de l'auteur.
Analyse complète dans `docs/`.
