# Les 137 formations sans contenu — reconstitution depuis les contenus gratuits

> **Le constat.** Sur les **369 fiches** de formation du corpus, **232** portent un contenu
> exploitable (verbatim de couche 1, citation de l'auteur, ou doctrine de couche 2) et
> **137 n'en portent pas** : le contenu de la session est derrière le paiement.
> C'est **la seule zone du corpus qui ne soit pas exploitable** — et c'est exactement la
> zone que la persona ne peut pas documenter.

> **Ce que ce document apporte.** Pour chacune des 137 formations : le thème, la
> formation jumelle qui porte la doctrine, et le contenu gratuit de substitution
> (citations **vérifiées mot pour mot**, concepts, sections). Plus une liste explicite
> de ce qui **n'est pas** reconstituable.

> **Ce que ce document ne prétend pas faire.** Il ne reconstitue pas le cours payant.
> Une formation reconstituée doit toujours être citée avec l'identifiant de sa fiche
> jumelle (`C###`), jamais avec le sien propre.

> **Critère de « fiche vide » (explicite, reproductible).** Une fiche est vide si elle ne
> porte **ni** verbatim de couche 1 (section `## Contenu complet` réelle, ≥ 25 mots,
> hors message de paywall), **ni** citation d'auteur (section `## Citations de Stéphane`
> non vide). La doctrine de couche 2, rédigée par un LLM, n'est **pas** la voix de
> l'auteur : elle ne rend pas une fiche exploitable comme source d'une citation.

> **Seuil d'appariement.** Une substitution thématique n'est retenue qu'au-dessus d'une
> ressemblance de **0.5**. En dessous, la formation est déclarée **non
> reconstituable** plutôt que comblée par une approximation.

> **Correction du 2026-10-23.** Ce document a été régénéré après la réparation du
> corpus : 18 fiches portaient un préfixe de numéros de ligne (`1|# Titre`) qui rendait
> leur titre et leur section « Contenu complet » invisibles à toute extraction par regex.
> 10 d'entre elles portaient en réalité un verbatim de couche 1 ou des citations : elles
> sortent donc de la liste des vides. D'où **137** et non 147.

> **Ce qui n'a pas changé** : le critère de « fiche vide » (ni verbatim de couche 1
> exploitable, ni citation d'auteur) et le seuil d'appariement thématique (0.5).

**Source** : `/root/migration-docker-stephane/Bartilabas/formation/StephaneEdouard/formations/`
(369 fiches).

**Identifiants** : `C###` = index canonique des fiches (369 entrées) — voir `20-index-canonique-fiches.md`.

---

## 1. La clé de reconstitution

Chaque fiche porte une URL de catalogue unique. Deux lectures complémentaires permettent
de rattacher une formation vide à une formation qui, elle, a du contenu.

| | Ce qu'on exploite | Résultat |
|---|---|---|
| **A. Base d'URL** | le suffixe `-matin` / `-apres-midi` encode la **session**, pas le thème | **53** fiches |
| **B. Jumeau thématique** | même thème, session différente, ressemblance ≥ 0.5 | **66** fiches |
| **C. Sans jumeau fiable** | aucune fiche du corpus ne porte ce thème de façon assez proche | **18** fiches |

→ **119 des 137** formations vides sont reconstituables
à partir du corpus déjà analysé.

---

## 2. Vue d'ensemble

| # | FORMATION SANS CONTENU | CATÉGORIE | JUMELLE | MODE |
|---|---|---|---|---|
| 1 | Enfer du salariat (apres-midi) | Carriere Leadership | `C005` — Enfer du salariat (matin) | base-URL |
| 2 | Like a boss, 1: Devenir INDISPENSABLE au travail (apres-midi) | Carriere Leadership | `C007` — Like a boss, 1 : Devenir INDISPENSABLE | theme |
| 3 | Like a boss, 1: Devenir INDISPENSABLE au travail (matin) | Carriere Leadership | `C007` — Like a boss, 1 : Devenir INDISPENSABLE | theme |
| 4 | Like a boss, 2: Des presentations (ecrites et orales) qui TUENT (après midi) | Carriere Leadership | `C016` — Like a boss, 2 : des presentations (éc | theme |
| 5 | Like a boss, 2: Des presentations (ecrites et orales) qui TUENT (matin) | Carriere Leadership | `C016` — Like a boss, 2 : des presentations (éc | theme |
| 6 | Like a boss, 3: Seduire et fideliser ses clients A VIE (après midi) | Carriere Leadership | **—** | none |
| 7 | Like a boss, 3: Seduire et fideliser ses clients A VIE (matin) | Carriere Leadership | `C006` — Like a boss, 3 : Séduire et fidéliser  | theme |
| 8 | Ameliorer sa voix (avec une chanteuse professionnelle) (apres-midi) | Communication | **—** | none |
| 9 | Ameliorer sa voix (avec une chanteuse professionnelle) (matin) | Communication | **—** | none |
| 10 | 100 jours pour la rendre amoureuse (apres-midi) | Couple Relations Longues | `C026` — 100 jours pour la rendre amoureuse | theme |
| 11 | 100 jours pour la rendre amoureuse (matin) | Couple Relations Longues | `C026` — 100 jours pour la rendre amoureuse | theme |
| 12 | Les couples ne fonctionnent plus – matin | Couple Relations Longues | `C003` — Le couple « à l'ancienne », c'est du p | base-URL |
| 13 | Les couples ne fonctionnent plus – après-midi | Couple Relations Longues | **—** | none |
| 14 | Survivre à la ROUTINE du couple (après midi) | Couple Relations Longues | `C025` — Survivre à la ROUTINE du couple | theme |
| 15 | Survivre à la ROUTINE du couple (matin) | Couple Relations Longues | `C025` — Survivre à la ROUTINE du couple | theme |
| 16 | Rester seduisant en couple (apres-midi) | Couple Relations Longues | `C034` — Rester seduisant en couple | theme |
| 17 | Rester seduisant en couple (matin) | Couple Relations Longues | `C034` — Rester seduisant en couple | theme |
| 18 | Le bonheur – matin | Developpement Personnel | `C038` — Le bonheur : 7 techniques pour être he | base-URL |
| 19 | Fabriquer sa chance (apres-midi) | Developpement Personnel | **—** | none |
| 20 | Fabriquer sa chance (matin) | Developpement Personnel | **—** | none |
| 21 | L'amant idéal, 2 (après-midi) | Developpement Personnel | `C042` — L'amant, 2 | base-URL |
| 22 | Développe ta force mentale (après-midi) | Developpement Personnel | `C239` — Développe ta force mentale (matin) | base-URL |
| 23 | Développe ta force mentale (matin) | Developpement Personnel | `C239` — Développe ta force mentale (matin) | base-URL |
| 24 | Le bonheur – après-midi | Developpement Personnel | `C071` — Intelligence relationnelle, 2: Les sec | theme |
| 25 | À mort la procrastination (après-midi) | Developpement Personnel | `C190` — À mort la procrastination | theme |
| 26 | À mort la procrastination (matin) | Developpement Personnel | `C190` — À mort la procrastination | theme |
| 27 | Une motivation en beton (apres-midi) | Developpement Personnel | `C047` — Une motivation en béton | theme |
| 28 | Une motivation en beton (matin) | Developpement Personnel | `C047` — Une motivation en béton | theme |
| 29 | Comprendre les gens, 2 (après-midi) | Intelligence Sociale | `C057` — Comprendre les gens, 2 | theme |
| 30 | Comprendre les gens, 2 (matin) | Intelligence Sociale | `C057` — Comprendre les gens, 2 | theme |
| 31 | Comment avoir du charisme (apres-midi) | Intelligence Sociale | `C066` — Comment avoir du charisme | theme |
| 32 | Comment avoir du charisme (matin) | Intelligence Sociale | `C066` — Comment avoir du charisme | theme |
| 33 | Comprendre les gens (apres-midi) Rattrapage de sociologie pour ceux qui ont pris maths a l ecole | Intelligence Sociale | `C073` — Comprendre les gens. Rattrapage de soc | theme |
| 34 | Comprendre les gens (matin) Rattrapage de sociologie pour ceux qui ont pris maths à l'école | Intelligence Sociale | `C073` — Comprendre les gens. Rattrapage de soc | theme |
| 35 | Confiance en soi (apres-midi) | Intelligence Sociale | `C064` — Confiance en soi | base-URL |
| 36 | Confiance en soi (matin) | Intelligence Sociale | `C064` — Confiance en soi | base-URL |
| 37 | Discernement – après-midi | Intelligence Sociale | `C071` — Intelligence relationnelle, 2: Les sec | theme |
| 38 | Discernement – matin | Intelligence Sociale | `C069` — Survivre aux mensonges du nouveau mond | base-URL |
| 39 | Formations — Stéphane Édouard | Non catégorisé | **—** | none |
| 40 | Logique de l'Homme (après-midi) | Relations H-F | `C084` — Logique des hommes – le côté obscur de | base-URL |
| 41 | Logique de l'Homme (matin) | Relations H-F | `C084` — Logique des hommes – le côté obscur de | base-URL |
| 42 | L'amant idéal, 2 : faire jouir une femme (matin) | Relations H-F | `C042` — L'amant, 2 | base-URL |
| 43 | Les jeunes filles, 1: Decoder les attentes feminines (apres-midi) | Relations H-F | **—** | none |
| 44 | Les jeunes filles, 1: Decoder les attentes feminines (matin) | Relations H-F | **—** | none |
| 45 | Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (après midi) | Relations H-F | **—** | none |
| 46 | Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (matin) | Relations H-F | **—** | none |
| 47 | Logique des femmes (apres-midi) | Relations H-F | `C081` — Logique des femmes | theme |
| 48 | Logique des femmes II (apres-midi) | Relations H-F | `C081` — Logique des femmes | theme |
| 49 | Logique des femmes II (matin) | Relations H-F | `C081` — Logique des femmes | theme |
| 50 | Logique des femmes (matin) | Relations H-F | `C081` — Logique des femmes | theme |
| 51 | Au secours, mon chef est une femme (/un homme) – apres-midi | Relations H-F | `C100` — Au secours, mon chef est une femme (/u | base-URL |
| 52 | Au secours, mon chef est une femme (/un homme) – matin | Relations H-F | `C100` — Au secours, mon chef est une femme (/u | base-URL |
| 53 | Premier rendez-vous (apres-midi)10 scenarii parfaits | Relations H-F | `C101` — Premier rendez-vous 10 scenarii parfai | theme |
| 54 | Premier rendez-vous (matin) 10 scenarii parfaits | Relations H-F | `C101` — Premier rendez-vous 10 scenarii parfai | theme |
| 55 | Rencontre (enfin) une fille bien ! (après-midi) | Relations H-F | `C106` — Où / quand / comment rencontrer une fi | base-URL |
| 56 | Rencontre (enfin) une fille bien ! (matin) | Relations H-F | `C106` — Où / quand / comment rencontrer une fi | base-URL |
| 57 | Intelligence relationnelle, 1: Doubler son RESEAU (après-midi) | Reseau Influence | `C071` — Intelligence relationnelle, 2: Les sec | theme |
| 58 | Intelligence relationnelle, 1: Doubler son RESEAU (matin) | Reseau Influence | `C071` — Intelligence relationnelle, 2: Les sec | theme |
| 59 | Intelligence sociale online (apres-midi) Internet, reseaux, applications | Reseau Influence | `C113` — Intelligence sociale III : Internet, r | theme |
| 60 | Intelligence sociale online (matin) Internet, reseaux, applications | Reseau Influence | `C113` — Intelligence sociale III : Internet, r | theme |
| 61 | L art delicat de la connexion (apres-midi) | Reseau Influence | `C112` — L'art delicat de la connexion | theme |
| 62 | L art delicat de la connexion (matin) | Reseau Influence | `C112` — L'art delicat de la connexion | theme |
| 63 | La santé mentale – après-midi | Sante Mentale | `C269` — La santé mentale – après-midi | base-URL |
| 64 | La santé mentale – matin | Sante Mentale | `C126` — Sauver sa santé mentale | theme |
| 65 | Entouré pour réussir (après-midi) | Sedirection Rencontres | `C121` — S'entourer pour réussir, ou le secret  | theme |
| 66 | Entouré pour réussir (matin) | Sedirection Rencontres | `C121` — S'entourer pour réussir, ou le secret  | theme |
| 67 | Briser la glace (apres-midi) | Sedirection Rencontres | `C127` — Briser la glace | theme |
| 68 | Briser la glace (matin) | Sedirection Rencontres | `C127` — Briser la glace | theme |
| 69 | Ce que vos parents auraient du vous apprendre (apres-midi) | Sedirection Rencontres | `C139` — Ce que vos parents auraient dû vous ap | theme |
| 70 | Ce que vos parents auraient du vous apprendre (matin) | Sedirection Rencontres | `C139` — Ce que vos parents auraient dû vous ap | theme |
| 71 | Développement personnel, 1: Decupler sa CREATIVITE (après midi) | Sedirection Rencontres | `C240` — Développement personnel 1 : décupler s | base-URL |
| 72 | Développement personnel, 1: Decupler sa CREATIVITE (matin) | Sedirection Rencontres | `C240` — Développement personnel 1 : décupler s | base-URL |
| 73 | Développement personnel, 2: Tenacite: apprendre a ne RIEN LACHER | Sedirection Rencontres | `C163` — Développement personnel, 2 : ON – NE – | theme |
| 74 | Ebook et audio | Sedirection Rencontres | **—** | none |
| 75 | Ebook seul | Sedirection Rencontres | **—** | none |
| 76 | Ce qu'il est URGENT d'apprendre à vos (futurs ?) enfants – après-midi | Sedirection Rencontres | `C148` — Ce qu'il est URGENT d'apprendre à vos  | base-URL |
| 77 | Ce qu'il est URGENT d'apprendre à vos (futurs ?) enfants – matin | Sedirection Rencontres | `C148` — Ce qu'il est URGENT d'apprendre à vos  | base-URL |
| 78 | Get a life (apres-midi) | Sedirection Rencontres | `C137` — Get a life | theme |
| 79 | Get a life (matin) | Sedirection Rencontres | `C137` — Get a life | theme |
| 80 | La peur (apres-midi) La supporter, l affronter, la vaincre | Sedirection Rencontres | `C184` — La peur : La supporter, l'affronter, l | theme |
| 81 | La peur (matin) La supporter, l affronter, la vaincre | Sedirection Rencontres | `C184` — La peur : La supporter, l'affronter, l | theme |
| 82 | Briller en ligne (après-midi) | Sedirection Rencontres | `C183` — Briller en ligne, le charme discret du | theme |
| 83 | Briller en ligne (matin) | Sedirection Rencontres | `C183` — Briller en ligne, le charme discret du | theme |
| 84 | Se construire une garde robe complete (apres-midi) | Sedirection Rencontres | `C138` — Se construire une garde-robe complete | theme |
| 85 | Se construire une garde robe complete (matin) | Sedirection Rencontres | `C138` — Se construire une garde-robe complete | theme |
| 86 | Se reconstruire apres une blessure (ce qui ne te tue pas te rend plus fort) (apres-midi) | Sedirection Rencontres | `C170` — Se reconstruire apres une blessure (ce | theme |
| 87 | Se reconstruire apres une blessure (ce qui ne te tue pas te rend plus fort) (matin) | Sedirection Rencontres | `C170` — Se reconstruire apres une blessure (ce | theme |
| 88 | Simplifiez-vous la vie ! (webinaire court et impactant, 2h « seulement ») | Sedirection Rencontres | `C349` — Simplifiez-vous la vie ! (webinaire co | base-URL |
| 89 | Secret agenda (apres-midi) | Sedirection Rencontres | `C174` — Agenda secret / feuille de route | theme |
| 90 | Secret agenda (matin) | Sedirection Rencontres | `C174` — Agenda secret / feuille de route | theme |
| 91 | Seduire bureau – ecole (apres-midi) | Sedirection Rencontres | **—** | none |
| 92 | Seduire bureau – ecole (matin) | Sedirection Rencontres | **—** | none |
| 93 | Signes d'intérêt (après-midi) | Sedirection Rencontres | `C179` — Le décodeur ultime de signes d'intérêt | base-URL |
| 94 | Signes d'intérêt (matin) | Sedirection Rencontres | `C179` — Le décodeur ultime de signes d'intérêt | base-URL |
| 95 | Small talk (badinage) (apres-midi) | Sedirection Rencontres | `C182` — Small talk (badinage) | theme |
| 96 | Small talk (badinage) (matin) | Sedirection Rencontres | `C182` — Small talk (badinage) | theme |
| 97 | Changez d'image (apres-midi) | Style Image | `C186` — Changez d'image | theme |
| 98 | Changez d'image (matin) | Style Image | `C186` — Changez d'image | theme |
| 99 | Catalogue des Formations | Non catégorisé | **—** | none |
| 100 | Comprendre les gens, 2 (matin) | Divers | `C057` — Comprendre les gens, 2 | theme |
| 101 | Cultivez votre INTELLIGENCE ÉMOTIONNELLE | Intelligence Sociale | `C070` — Cultivez votre INTELLIGENCE ÉMOTIONNEL | base-URL |
| 102 | Développement personnel, 2 : ON – NE – LÂCHE – RIEN | Divers | `C163` — Développement personnel, 2 : ON – NE – | base-URL |
| 103 | Développement personnel, 2: Tenacite: apprendre a ne RIEN LACHER | Développement Personnel | `C163` — Développement personnel, 2 : ON – NE – | theme |
| 104 | Discernement – matin | Divers | `C069` — Survivre aux mensonges du nouveau mond | base-URL |
| 105 | DOUBLE ton RÉSEAU | Carrière & Leadership | `C123` — DOUBLE ton RÉSEAU | base-URL |
| 106 | Entouré pour réussir (matin) | Divers | `C121` — S'entourer pour réussir, ou le secret  | theme |
| 107 | Intelligence relationnelle, 1: Doubler son RESEAU (matin) | Relations H-F | `C071` — Intelligence relationnelle, 2: Les sec | theme |
| 108 | Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi) | Relations H-F | `C071` — Intelligence relationnelle, 2: Les sec | base-URL |
| 109 | Intelligence relationnelle, 2: Les secrets du POUVOIR (matin) | Relations H-F | `C071` — Intelligence relationnelle, 2: Les sec | base-URL |
| 110 | Langage des hommes | Divers | `C087` — Langage des hommes | base-URL |
| 111 | Le bonheur : 7 techniques pour être heureux et surfer la vie | Santé Mentale | `C038` — Le bonheur : 7 techniques pour être he | base-URL |
| 112 | Le bonheur – matin | Santé Mentale | `C038` — Le bonheur : 7 techniques pour être he | base-URL |
| 113 | Le couple « à l&rsquo;ancienne », c&rsquo;est du passé. Encaissez les ruptures LIKE A BOSS | Relations H-F | `C003` — Le couple « à l'ancienne », c'est du p | base-URL |
| 114 | Le décodeur ultime de signes d&rsquo;intérêts ! | Divers | `C179` — Le décodeur ultime de signes d'intérêt | base-URL |
| 115 | Les couples ne fonctionnent plus – matin | Relations H-F | `C003` — Le couple « à l'ancienne », c'est du p | base-URL |
| 116 | Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (matin) | Relations H-F | **—** | none |
| 117 | Like a boss, 2: Des presentations (ecrites et orales) qui TUENT (matin) | Carrière & Leadership | `C016` — Like a boss, 2 : des presentations (éc | theme |
| 118 | Like a boss, 2 : des presentations (écrites et orales) qui TUENT | Carrière & Leadership | `C016` — Like a boss, 2 : des presentations (éc | base-URL |
| 119 | Like a boss, 3: Seduire et fideliser ses clients A VIE (après midi) | Carrière & Leadership | **—** | none |
| 120 | Like a boss, 3: Seduire et fideliser ses clients A VIE (matin) | Carrière & Leadership | `C006` — Like a boss, 3 : Séduire et fidéliser  | theme |
| 121 | Logique de l&rsquo;Homme (matin) | Divers | `C084` — Logique des hommes – le côté obscur de | base-URL |
| 122 | Logique des hommes – le côté obscur de H pur | Divers | `C084` — Logique des hommes – le côté obscur de | base-URL |
| 123 | L&rsquo;amant, 2 | Relations H-F | `C042` — L'amant, 2 | base-URL |
| 124 | L&rsquo;amant idéal, 2 : faire jouir une femme (matin) | Relations H-F | `C042` — L'amant, 2 | base-URL |
| 125 | L&rsquo;amant idéal, 2 (après-midi) | Relations H-F | `C042` — L'amant, 2 | base-URL |
| 126 | L&rsquo;école des hommes | Divers | `C088` — L'école des hommes | base-URL |
| 127 | Où / quand / comment rencontrer une fille bien | Sédduction & Rencontres | `C106` — Où / quand / comment rencontrer une fi | base-URL |
| 128 | Plus de rencontres | Sédduction & Rencontres | `C162` — Plus de rencontres | base-URL |
| 129 | Rencontre (enfin) une fille bien ! (matin) | Sédduction & Rencontres | `C106` — Où / quand / comment rencontrer une fi | base-URL |
| 130 | Reçois ton La Furia© dédicacé ! | Divers | `C154` — Reçois ton La Furia© dédicacé ! | base-URL |
| 131 | Sauver sa santé mentale | Santé Mentale | `C126` — Sauver sa santé mentale | base-URL |
| 132 | Signes d&rsquo;intérêt (matin) | Divers | `C179` — Le décodeur ultime de signes d'intérêt | base-URL |
| 133 | Simplifiez-vous la vie ! (webinaire court et impactant, 2h « seulement ») | Divers | `C349` — Simplifiez-vous la vie ! (webinaire co | base-URL |
| 134 | S&rsquo;entourer pour réussir, ou le secret des affinités électives | Divers | `C121` — S'entourer pour réussir, ou le secret  | base-URL |
| 135 | Survivre à la ROUTINE du couple (matin) | Relations H-F | `C025` — Survivre à la ROUTINE du couple | theme |
| 136 | Survivre aux mensonges du nouveau monde (le discernement) | Intelligence Sociale | `C069` — Survivre aux mensonges du nouveau mond | base-URL |
| 137 | Vivre avec la procrastination | Développement Personnel | `C050` — Vivre avec la procrastination | base-URL |

---

## 3. Fiche par formation

### 1. Enfer du salariat (apres-midi)

- **Identifiant** : `C004` · **Catégorie** : Carriere Leadership
- **URL de catalogue** : `mat-consulting.fr/enfer-du-salariat-apres-midi`
- **Base thématique** : `enfer-du-salariat`
- **Taille de la fiche** : 1237 mots (contenu de session absent)

**Formation jumelle** : `C005` — Enfer du salariat (matin)  
*mode : base-URL · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « Le salariat moderne est un jeu où l'employeur a trois coups d'avance et où vous croyez jouer à égalité. Vous ne jouez pas à égalité — vous jouez à la roulette avec son revolver. » — `C005`
- « Un homme qui ne peut pas se passer de son salaire est un homme qui ne peut pas se permettre d'avoir une conscience. C'est ça, l'enfer moderne : pas la pauvreté, mais l'impossibilité de dire non. » — `C005`
- « Le burn-out n'est pas une maladie, c'est une démission silencieuse. Le corps et l'esprit vous disent ce que votre ego refuse d'entendre : ce système n'est pas le vôtre. » — `C005`

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel · Le salariat moderne est une cage dorée · Le statut social lié au poste est une drogue · La dépendance au salaire est le premier maillon de la chaîne d'asservissement · Le CDI est un piège temporel · L'employé modèle est l'employé corvéable · L'identité professionnelle vole l'identité personnelle · Le burn-out n'est pas un accident, c'est un signal de maturité

**Sections de la fiche jumelle** :

- Concepts enseignés
- 1. L'illusion de la sécurité
- 2. Les sept cages dorées
- 3. L'identité professionnelle comme usurpation d'identité
- 4. Le syndrome de Stockholm professionnel
- 5. Le burn-out comme signal et non comme faiblesse
- 6. Le coût d'opportunité invisible
- 7. L'inversion de la pyramide de Maslow dans le salariat
- Lien avec formations et podcasts
- Elle-voulait-le-confort,-elle-a-eu-l'ennui-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C005`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 2. Like a boss, 1: Devenir INDISPENSABLE au travail (apres-midi)

- **Identifiant** : `C009` · **Catégorie** : Carriere Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-1-devenir-indispensable-au-travail-apres-midi`
- **Base thématique** : `like-a-boss-1-devenir-indispensable-au-travail`
- **Taille de la fiche** : 1675 mots (contenu de session absent)

**Formation jumelle** : `C007` — Like a boss, 1 : Devenir INDISPENSABLE au travail  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> L’ÉCONOMIE MONDIALE VA « SECOUER »… DONC LA NÔTRE AUSSI
> Croissance mondiale ⏼France 📉Inégalités 📈Climat 🥵
> Dans un contexte aussi tendu, les entreprises ne vont pas se priver de tendre les flux, éliminer le gras… et bien entendu débaucher.
> Et vous, au milieu de ça, vous n’aurez pas 50 options, ni même 30, ni même 10. Vous n’en aurez que 2, des options: J’ai mis un petit check vert au stylo sous celle qui me paraissait être la meilleure pour vous, mais après, vous êtes libre de choisir l’autre…
> Bref, si je vous l’apprends je m’en excuse par avance, mais il est désormais à peu près certain que la « crise » (i.e la croissance nulle ou quasi nulle) soit notre paysage culturel jusqu’à la retraite,

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-hVchQj-xiOo-synthese
- Citation notable
- Formations et fiches liées
- J'achète-la-formation-d'une-influenceuse-pour-séduire-sur-les-réseaux-synthese
- Conclusion
- Formations et fiches liées
- La-techno-gréviste-est-la-révélation-de-ce-début-d’année-2023-synthese
- Video-yCgVt4zZejg-synthese
- Elle-voulait-le-confort,-elle-a-eu-l'ennui-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C007`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 3. Like a boss, 1: Devenir INDISPENSABLE au travail (matin)

- **Identifiant** : `C010` · **Catégorie** : Carriere Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-1-devenir-indispensable-au-travail-matin`
- **Base thématique** : `like-a-boss-1-devenir-indispensable-au-travail`
- **Taille de la fiche** : 1267 mots (contenu de session absent)

**Formation jumelle** : `C007` — Like a boss, 1 : Devenir INDISPENSABLE au travail  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> L’ÉCONOMIE MONDIALE VA « SECOUER »… DONC LA NÔTRE AUSSI
> Croissance mondiale ⏼France 📉Inégalités 📈Climat 🥵
> Dans un contexte aussi tendu, les entreprises ne vont pas se priver de tendre les flux, éliminer le gras… et bien entendu débaucher.
> Et vous, au milieu de ça, vous n’aurez pas 50 options, ni même 30, ni même 10. Vous n’en aurez que 2, des options: J’ai mis un petit check vert au stylo sous celle qui me paraissait être la meilleure pour vous, mais après, vous êtes libre de choisir l’autre…
> Bref, si je vous l’apprends je m’en excuse par avance, mais il est désormais à peu près certain que la « crise » (i.e la croissance nulle ou quasi nulle) soit notre paysage culturel jusqu’à la retraite,

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-hVchQj-xiOo-synthese
- Citation notable
- Formations et fiches liées
- J'achète-la-formation-d'une-influenceuse-pour-séduire-sur-les-réseaux-synthese
- Conclusion
- Formations et fiches liées
- La-techno-gréviste-est-la-révélation-de-ce-début-d’année-2023-synthese
- Video-yCgVt4zZejg-synthese
- Elle-voulait-le-confort,-elle-a-eu-l'ennui-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C007`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 4. Like a boss, 2: Des presentations (ecrites et orales) qui TUENT (après midi)

- **Identifiant** : `C011` · **Catégorie** : Carriere Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-2-des-presentations-ecrites-et-orales-qui-tuent-apres-midi`
- **Base thématique** : `like-a-boss-2-des-presentations-ecrites-et-orales-qui-tuent`
- **Taille de la fiche** : 849 mots (contenu de session absent)

**Formation jumelle** : `C016` — Like a boss, 2 : des presentations (écrites et orales) qui TUENT  
*mode : theme · confiance : 0.62*

**Contenu verbatim disponible** (couche 1) :

> Savoir et Savoir-faire sont sur un bateau…
> … qui pousse l'autre à l'eau, devient capitaine, reçoit la gloire et les honneurs
> Cette antinomie, cette fracture, cette lutte à mort entre
> – d'un côté la compétence brute, le laborieux silencieux, voire le génie autiste façon Alan Turing (l'inventeur de l'ordinateur, popularisé par un film Hollywoodien, mettant en avant son incapacité pathologique à expliquer le but de ses recherches)
> On a bien failli ne jamais avoir de tablette entre les mains, parce qu'Alan Turing ne savait pas présenter son projet : l'ordinateur
> – et de l'autre le communiquant pur, totalement improductif mais génie de l'embrouille, de la parlotte, capable de vendre du sable à cr

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C016`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 5. Like a boss, 2: Des presentations (ecrites et orales) qui TUENT (matin)

- **Identifiant** : `C012` · **Catégorie** : Carriere Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-2-des-presentations-ecrites-et-orales-qui-tuent-matin-2`
- **Base thématique** : `like-a-boss-2-des-presentations-ecrites-et-orales-qui-tuent-matin`
- **Taille de la fiche** : 1778 mots (contenu de session absent)

**Formation jumelle** : `C016` — Like a boss, 2 : des presentations (écrites et orales) qui TUENT  
*mode : theme · confiance : 0.83*

**Contenu verbatim disponible** (couche 1) :

> Savoir et Savoir-faire sont sur un bateau…
> … qui pousse l'autre à l'eau, devient capitaine, reçoit la gloire et les honneurs
> Cette antinomie, cette fracture, cette lutte à mort entre
> – d'un côté la compétence brute, le laborieux silencieux, voire le génie autiste façon Alan Turing (l'inventeur de l'ordinateur, popularisé par un film Hollywoodien, mettant en avant son incapacité pathologique à expliquer le but de ses recherches)
> On a bien failli ne jamais avoir de tablette entre les mains, parce qu'Alan Turing ne savait pas présenter son projet : l'ordinateur
> – et de l'autre le communiquant pur, totalement improductif mais génie de l'embrouille, de la parlotte, capable de vendre du sable à cr

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C016`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 6. Like a boss, 3: Seduire et fideliser ses clients A VIE (après midi)

- **Identifiant** : `C013` · **Catégorie** : Carriere Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie-apres-midi`
- **Base thématique** : `like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie`
- **Taille de la fiche** : 932 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.43) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 7. Like a boss, 3: Seduire et fideliser ses clients A VIE (matin)

- **Identifiant** : `C014` · **Catégorie** : Carriere Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie-matin`
- **Base thématique** : `like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie`
- **Taille de la fiche** : 943 mots (contenu de session absent)

**Formation jumelle** : `C006` — Like a boss, 3 : Séduire et fidéliser ses clients A VIE  
*mode : theme · confiance : 0.6*

**Contenu verbatim disponible** (couche 1) :

> Je sais pas vous, mais j'ai déjà eu l'occasion de mourir plusieurs fois. Médiatiquement parlant, s'entend. Tout a commencé dans la 17ème année du XXIème siècle de notre ère par un bien sombre article dans 20 minutes qui m'accusait de… l'inverse exact de ce que je disais en vidéo. Entreprise de diffamation relayée depuis, chaque année ou presque, par un con-frère ou une con-soeur fainéant de la presse aux ordres (pléonasme). Mais… ici, on ne lâche rien, parce que :
> Mes clients m'ont toujours sauvé la vie
> Devant l'adversité, 100 % de mes clients se montrent (encore aujourd'hui) solidaires et unis ! Ça, c'est pas une preuve de fidélité ? Ça, c'est pas une preuve de fidélité ?
> Que vous soyez ent

**Sections de la fiche jumelle** :

- Concepts enseignés
- Calin-o-thérapie-le-stage-où-les-perdants-de-la-modernité-se-réconfortent-entre-eux-synthese
- Le marché des rencontres
- Analyse des participants
- Le phénomène étudié
- Le "loopen prolétariat" des rencontres
- Katia, prof de yoga
- Réaction aux critiques
- Video-_z11PNOSbnM-synthese
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C006`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 8. Ameliorer sa voix (avec une chanteuse professionnelle) (apres-midi)

- **Identifiant** : `C018` · **Catégorie** : Communication
- **URL de catalogue** : `mat-consulting.fr/ameliorer-sa-voix-avec-une-chanteuse-professionnelle-apres-midi`
- **Base thématique** : `ameliorer-sa-voix-avec-une-chanteuse-professionnelle`
- **Taille de la fiche** : 3944 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.2) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Ameliorer sa voix (avec une chanteuse professionnelle) (apres-midi) 5.00 1 avis 195€ l’ont déjà le veulent Ajouter au panier Ajouter à ma wantlist 100% 1 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients L'avis de Valentin_Popescu Formation intéressante et pédagogique, avec des conseils concrets pour mieux maîtriser sa voix et gagner en confiance. Ajouter un Avis Ann

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 9. Ameliorer sa voix (avec une chanteuse professionnelle) (matin)

- **Identifiant** : `C019` · **Catégorie** : Communication
- **URL de catalogue** : `mat-consulting.fr/ameliorer-sa-voix-avec-une-chanteuse-professionnelle-matin`
- **Base thématique** : `ameliorer-sa-voix-avec-une-chanteuse-professionnelle`
- **Taille de la fiche** : 3813 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.2) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Ameliorer sa voix (avec une chanteuse professionnelle) (matin) 0 avis 195€ l’ont déjà le veulent Ajouter au panier Ajouter à ma wantlist 0 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients Avis Il n’y a pas encore d’avis. Soyez le premier à laisser votre avis sur “Ameliorer sa voix (avec une chanteuse professionnelle) (matin)” Annuler la réponse Vous devez être conne

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 10. 100 jours pour la rendre amoureuse (apres-midi)

- **Identifiant** : `C023` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/100-jours-pour-la-rendre-amoureuse-apres-midi`
- **Base thématique** : `100-jours-pour-la-rendre-amoureuse`
- **Taille de la fiche** : 2474 mots (contenu de session absent)

**Formation jumelle** : `C026` — 100 jours pour la rendre amoureuse  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Quand vous « improvisez » vos débuts de relation, il se passe quoi ?
> J’ai donné des centaines d'études de cas, à l’issue desquelles je puis affirmer une chose avec certitude : la plupart des problèmes (souvent irrattrapables et insurmontables) dans lesquels vous vous mettez viennent du fait que vous n’avez pas su « cadrer » les choses dans les 3 premiers mois.
> Si j’étais un webmarketeur (ou un voleur, ce qui revient à peu près au même), je vous vendrais un pilule magique pour résoudre ce problème instantanément, ou bien je vous vendrais un ebook de 47 pages du style « casé en 1 semaine »… Mais aujourd’hui, se caser avec la première femme disponible n’ai rien de compliqué, n’importe quel con 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C026`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 11. 100 jours pour la rendre amoureuse (matin)

- **Identifiant** : `C024` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/100-jours-pour-la-rendre-amoureuse-matin`
- **Base thématique** : `100-jours-pour-la-rendre-amoureuse`
- **Taille de la fiche** : 2451 mots (contenu de session absent)

**Formation jumelle** : `C026` — 100 jours pour la rendre amoureuse  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Quand vous « improvisez » vos débuts de relation, il se passe quoi ?
> J’ai donné des centaines d'études de cas, à l’issue desquelles je puis affirmer une chose avec certitude : la plupart des problèmes (souvent irrattrapables et insurmontables) dans lesquels vous vous mettez viennent du fait que vous n’avez pas su « cadrer » les choses dans les 3 premiers mois.
> Si j’étais un webmarketeur (ou un voleur, ce qui revient à peu près au même), je vous vendrais un pilule magique pour résoudre ce problème instantanément, ou bien je vous vendrais un ebook de 47 pages du style « casé en 1 semaine »… Mais aujourd’hui, se caser avec la première femme disponible n’ai rien de compliqué, n’importe quel con 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C026`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 12. Les couples ne fonctionnent plus – matin

- **Identifiant** : `C027` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/couple-rupture-difficile-matin`
- **Base thématique** : `couple-rupture-difficile`
- **Taille de la fiche** : 2644 mots (contenu de session absent)

**Formation jumelle** : `C003` — Le couple « à l'ancienne », c'est du passé. Encaissez les ruptures LIKE A BOSS  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon, vous l'aurez remarqué, les couples ne fonctionnent plus (d'où le sous-titre du séminaire : encaissez les ruptures). C'est pas une vue de l'esprit, ni l'expression de mon fatalisme patent. Les gens restent ensemble de moins en moins longtemps, c'est universel en occident. Et si vous habitez une métropole, vous pouvez encore diviser votre « espérance de survie du couple » par 2, voire par 3. Vous voulez des chiffres ? entre 93 et 96, il y avait en moyenne chaque année 155 000 séparations. Ce chiffre est passé, en 15 ans à peine, à 253 000 ( ! ) par an (+63 % !!)
> Dans les années 80, 70 % des adultes en couple, âgés de 20 à 31 ans, vivaient au moins 15 ans ensemble. Cette statistique a perd

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- Pour-surmonter-une-rupture,-n'imite-pas-cette-youtubeuse-synthese
- Conclusion
- Formations et fiches liées
- Video-L_O9dPuT_jE-synthese
- Le trio magique de l'obsession
- La logique des sentiments
- La reconquête
- Chiale-encore-un-coup,-c'est-bon-pour-l'audimat-synthese
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C003`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 13. Les couples ne fonctionnent plus – après-midi

- **Identifiant** : `C028` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/couples-ne-fonctionnent-plus-apres-midi`
- **Base thématique** : `couples-ne-fonctionnent-plus`
- **Taille de la fiche** : 1994 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.4) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 14. Survivre à la ROUTINE du couple (après midi)

- **Identifiant** : `C029` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-3-audace-scenarii-oses-pour-rencontres-memorables-apres-midi`
- **Base thématique** : `les-jeunes-filles-3-audace-scenarii-oses-pour-rencontres-memorables`
- **Taille de la fiche** : 1894 mots (contenu de session absent)

**Formation jumelle** : `C025` — Survivre à la ROUTINE du couple  
*mode : theme · confiance : 0.6*

**Contenu verbatim disponible** (couche 1) :

> Vous avez remarqué ? Désormais tout le monde est devenu sociologue, tout le monde est anthropologue, tout le monde est expert en sciences cognitives, tout le monde est [insérer la spécialité de votre choix] depuis qu'ils ont visionné 3 ou 4 vidéos sur Youtube sur le sujet. Sic. Mais vous savez quoi ? Laissons-les dire, laissons-les faire : il faut que jeunesse se passe…
> Et pourtant…
> Les hommes ne savent (toujours) pas QUOI FAIRE avec les femmes
> Oui, j'ose le répéter : les hommes ne savent pas quoi faire avec les femmes. Au risque de simplifier un peu, c'est vrai et je l'ai vérifié à des centaines, à des milliers de reprises : vous voulez une/des femme(s) dans votre vie, vous mettez en place 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Combien-de-fois-A.Buzyn-a-t-elle-menti-à-la-commission-d'enquête-synthese
- Méthodologie
- Score de mentir
- Points critiques relevés
- Citation du Professeur Raoult
- Vidéoscopie-–-Analyse-de-propos-sur-les-femmes-et-la-négociation-salariale-synthese
- La-résilience-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C025`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 15. Survivre à la ROUTINE du couple (matin)

- **Identifiant** : `C030` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-3-audace-scenarii-oses-pour-rencontres-memorables-matin`
- **Base thématique** : `les-jeunes-filles-3-audace-scenarii-oses-pour-rencontres-memorables`
- **Taille de la fiche** : 1679 mots (contenu de session absent)

**Formation jumelle** : `C025` — Survivre à la ROUTINE du couple  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous avez remarqué ? Désormais tout le monde est devenu sociologue, tout le monde est anthropologue, tout le monde est expert en sciences cognitives, tout le monde est [insérer la spécialité de votre choix] depuis qu'ils ont visionné 3 ou 4 vidéos sur Youtube sur le sujet. Sic. Mais vous savez quoi ? Laissons-les dire, laissons-les faire : il faut que jeunesse se passe…
> Et pourtant…
> Les hommes ne savent (toujours) pas QUOI FAIRE avec les femmes
> Oui, j'ose le répéter : les hommes ne savent pas quoi faire avec les femmes. Au risque de simplifier un peu, c'est vrai et je l'ai vérifié à des centaines, à des milliers de reprises : vous voulez une/des femme(s) dans votre vie, vous mettez en place 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Combien-de-fois-A.Buzyn-a-t-elle-menti-à-la-commission-d'enquête-synthese
- Méthodologie
- Score de mentir
- Points critiques relevés
- Citation du Professeur Raoult
- Vidéoscopie-–-Analyse-de-propos-sur-les-femmes-et-la-négociation-salariale-synthese
- La-résilience-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C025`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 16. Rester seduisant en couple (apres-midi)

- **Identifiant** : `C032` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/rester-seduisant-en-couple-apres-midi`
- **Base thématique** : `rester-seduisant-en-couple`
- **Taille de la fiche** : 2155 mots (contenu de session absent)

**Formation jumelle** : `C034` — Rester seduisant en couple  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> AVANT VS APRÈS CETTE JOURNÉE
> Avant : Flashback
> Le couple et les rencontres, statistiquement, ça se passe comme ça : vous vous imaginez la manière dont vous allez rencontrer quelqu’un (sur internet / dans la rue / au bureau / au sport / etc.)
> rien ne se déroule exactement comme prévu
> vous finissez par rencontrer quelqu’un d’une manière complètement inattendue (souvent, vous la connaissiez déjà avant d’avoir « commencé »)
> vous oubliez 80 % des fondamentaux. Normal, ça ne sert à rien, la personne est acquise (du moins le croyez-vous). Elle habite peut-être même chez vous
> un certain nombre de comportements s’insinuent en vous, d’autant plus insidieux qu’ils sont globalement indétectables. Under 

**Concepts enseignés** :

Le Mythe des 7% · L'Économie du Couple vs la Romantique · Le Marché Immobilier au Cœur des Dynamiques de Séparation · Le Dilemme du Prisonnier Appliqué au Couple

**Sections de la fiche jumelle** :

- Concepts enseignés
- Vidéoscopie-–-Analyse-de-propos-sur-les-femmes-et-la-négociation-salariale-synthese
- L'un-de-ces-deux-protagonistes-me-provoque-un-réel-malaise-🤢,-mais-lequel-synthese
- Formations et fiches liées
- Provoc'-Bill-Cosby,-ce-père-modèle-😅-synthese
- Citation notable
- Video-4JcaTyVg9_4-synthese
- Exemples développés
- Citation clé
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C034`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 17. Rester seduisant en couple (matin)

- **Identifiant** : `C033` · **Catégorie** : Couple Relations Longues
- **URL de catalogue** : `mat-consulting.fr/rester-seduisant-en-couple-matin`
- **Base thématique** : `rester-seduisant-en-couple`
- **Taille de la fiche** : 2317 mots (contenu de session absent)

**Formation jumelle** : `C034` — Rester seduisant en couple  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> AVANT VS APRÈS CETTE JOURNÉE
> Avant : Flashback
> Le couple et les rencontres, statistiquement, ça se passe comme ça : vous vous imaginez la manière dont vous allez rencontrer quelqu’un (sur internet / dans la rue / au bureau / au sport / etc.)
> rien ne se déroule exactement comme prévu
> vous finissez par rencontrer quelqu’un d’une manière complètement inattendue (souvent, vous la connaissiez déjà avant d’avoir « commencé »)
> vous oubliez 80 % des fondamentaux. Normal, ça ne sert à rien, la personne est acquise (du moins le croyez-vous). Elle habite peut-être même chez vous
> un certain nombre de comportements s’insinuent en vous, d’autant plus insidieux qu’ils sont globalement indétectables. Under 

**Concepts enseignés** :

Le Mythe des 7% · L'Économie du Couple vs la Romantique · Le Marché Immobilier au Cœur des Dynamiques de Séparation · Le Dilemme du Prisonnier Appliqué au Couple

**Sections de la fiche jumelle** :

- Concepts enseignés
- Vidéoscopie-–-Analyse-de-propos-sur-les-femmes-et-la-négociation-salariale-synthese
- L'un-de-ces-deux-protagonistes-me-provoque-un-réel-malaise-🤢,-mais-lequel-synthese
- Formations et fiches liées
- Provoc'-Bill-Cosby,-ce-père-modèle-😅-synthese
- Citation notable
- Video-4JcaTyVg9_4-synthese
- Exemples développés
- Citation clé
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C034`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 18. Le bonheur – matin

- **Identifiant** : `C037` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/bonheur-matin`
- **Base thématique** : `bonheur`
- **Taille de la fiche** : 1262 mots (contenu de session absent)

**Formation jumelle** : `C038` — Le bonheur : 7 techniques pour être heureux et surfer la vie  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Tout a peut-être été déjà été dit sur le bonheur (et encore que, cela reste à vérifier), et alors : êtes-vous en mesure de me définir exactement ce que c'est ? Essayez d'en formuler une définition claire en 30 secondes sans recourir à une aide électronique dont le nom commencerait par wiki
> dans quelles conditions se manifeste t-il ?
> avez-vous le sentiment d'avoir une prise quelconque sur votre état d'esprit ? Why is our generation so unhappy?
> — 🌸🌸 (@Graciethebrand) March 23, 2024 Pourquoi être heureux est important
> Je dois vraiment vous le dire ? Bon, allez : La solitude tue. Or être malheureux, c'est (à terme) être seul
> Les gens heureux ont plus d'amis…
> … et de partenaires sexuels (slurp)
> L

**Sections de la fiche jumelle** :

- Concepts enseignés
- Le-bonheur-7-techniques-pour-être-heureux-et-surfer-la-vie-synthese
- Video-HjrJlmCJT3Y-synthese
- Formations et fiches liées
- Video-OPtQxFnZFX4-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C038`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 19. Fabriquer sa chance (apres-midi)

- **Identifiant** : `C039` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/fabriquer-sa-chance-apres-midi`
- **Base thématique** : `fabriquer-sa-chance`
- **Taille de la fiche** : 2649 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.0) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Fabriquer sa chance (apres-midi) 1 avis 195€ l’ont déjà le veulent Ajouter au panier Ajouter à ma wantlist 0 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients L'avis de Clément Touba (client confirmé) Commandé le 21-12-2020  (et téléchargé à  21:03:59) « Toujours au top » Ajouter un Avis Annuler la réponse Vous devez être connecté pour publier un avis. Tonton Stéphan

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 20. Fabriquer sa chance (matin)

- **Identifiant** : `C040` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/fabriquer-sa-chance-matin`
- **Base thématique** : `fabriquer-sa-chance`
- **Taille de la fiche** : 1754 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.0) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Fabriquer sa chance (matin) 0 avis 195€ l’ont déjà le veulent Ajouter au panier Ajouter à ma wantlist 0 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients Avis Il n’y a pas encore d’avis. Soyez le premier à laisser votre avis sur “Fabriquer sa chance (matin)” Annuler la réponse Vous devez être connecté pour publier un avis. Tonton Stéphane te recommande Get a life Mes

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 21. L'amant idéal, 2 (après-midi)

- **Identifiant** : `C041` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/faire-lamour-a-une-femme-apres-midi`
- **Base thématique** : `faire-lamour-a-une-femme`
- **Taille de la fiche** : 1057 mots (contenu de session absent)

**Formation jumelle** : `C042` — L'amant, 2  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon. Je vais faire simple. Pour une grande, pour une immense majorité d'hétéros binaires de base, l'acte sexuel unissant un homme et une femme se réduit à remorquer une F (consentante) sur une app' de rencontre
> essuyer avec grâce – et un semblant de détachement – une addition au restaurant plus ou moins salée
> un enchaînement plus ou moins hésitant et foireux pour prolonger la soirée chez l'un ou chez l'autre, sous couvert d'un prétexte risible
> un effeuillage penaud conclu par une pénétration vigoureuse et empressée avant le réglementaire repos du guerrier Voilà, pliez bagage, y'a plus à rien à voir, ron-ron dit celui qui se met à ronfler, et « merci pour ce moment » dit celle qui s'échappe s

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C042`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 22. Développe ta force mentale (après-midi)

- **Identifiant** : `C044` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/gestion-crise-apres-midi`
- **Base thématique** : `gestion-crise`
- **Taille de la fiche** : 1133 mots (contenu de session absent)

**Formation jumelle** : `C239` — Développe ta force mentale (matin)  
*mode : base-URL · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « La vraie résilience, c'est pas de balancer des punchlines sur les réseaux sociaux et de faire des cœurs juste avant de se filmer pour avoir un bicep bump. La vraie résilience, c'est : qu'est-ce que tu as fait quand tu as été écarté, licencié, quand tu t'es retrouvé devant un juge, quand tu as eu un souci de santé ? » — `C239`
- « La force mentale se forge dans l'action — dans le sport, dans l'effort soutenu, dans la gestion de la douleur. » — `C239`
- « L'homme qui a une mission externalisée est moins vulnérable à la dépression. » — `C239`

**Sections de la fiche jumelle** :

- Concepts enseignés
- La force vitale / H-pur
- Résilience authentique vs résilience de façade
- L'endurance et la tolérance à la douleur
- La canalisation des pulsions
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- La-résilience-synthese
- La-santé-mentale-synthese
- Positionnement dans l'écosystème MAT Consulting
- Ressources liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C239`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 23. Développe ta force mentale (matin)

- **Identifiant** : `C045` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/gestion-crise-matin`
- **Base thématique** : `gestion-crise`
- **Taille de la fiche** : 718 mots (contenu de session absent)

**Formation jumelle** : `C239` — Développe ta force mentale (matin)  
*mode : base-URL · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « La vraie résilience, c'est pas de balancer des punchlines sur les réseaux sociaux et de faire des cœurs juste avant de se filmer pour avoir un bicep bump. La vraie résilience, c'est : qu'est-ce que tu as fait quand tu as été écarté, licencié, quand tu t'es retrouvé devant un juge, quand tu as eu un souci de santé ? » — `C239`
- « La force mentale se forge dans l'action — dans le sport, dans l'effort soutenu, dans la gestion de la douleur. » — `C239`
- « L'homme qui a une mission externalisée est moins vulnérable à la dépression. » — `C239`

**Sections de la fiche jumelle** :

- Concepts enseignés
- La force vitale / H-pur
- Résilience authentique vs résilience de façade
- L'endurance et la tolérance à la douleur
- La canalisation des pulsions
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- La-résilience-synthese
- La-santé-mentale-synthese
- Positionnement dans l'écosystème MAT Consulting
- Ressources liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C239`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 24. Le bonheur – après-midi

- **Identifiant** : `C046` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/le-bonheur-apres-midi`
- **Base thématique** : `le-bonheur`
- **Taille de la fiche** : 1260 mots (contenu de session absent)

**Formation jumelle** : `C071` — Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)  
*mode : theme · confiance : 0.67*

**Sections de la fiche jumelle** :

- Concepts enseignés
- The-brilliant-idea-from-the-creators-of-#Metoo-to-save-the-movement-synthese
- Video-p1WU4JiuIzQ-synthese
- L'intelligence-relationnelle-2-synthese
- Video-tiDHbY0rQKQ-synthese
- L'intelligence-relationnelle-1-synthese
- Video-x2zvDhh2yu4-synthese
- This-case-would-be-front-page-news-if-only-the-murderer-were-a-man,-but...-🤫-synthese
- This-government-campaign-was-so-successful-that-you've-(probably)-never-seen-it.-synthese
- Fiche transcrite par Bartilabas

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C071`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 25. À mort la procrastination (après-midi)

- **Identifiant** : `C048` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/procrastination-apres-midi`
- **Base thématique** : `procrastination`
- **Taille de la fiche** : 1416 mots (contenu de session absent)

**Formation jumelle** : `C190` — À mort la procrastination  
*mode : theme · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « La procrastination n'est pas un problème de temps — c'est un problème émotionnel. Vous ne reportez pas parce que vous manquez de temps, vous reportez parce que quelque chose en vous veut éviter cette tâche. » — `C190`
- « L'homme qui agit malgré la peur développe un avantage compétitif que l'homme qui attend de se sentir prêt n'aura jamais. » — `C190`
- « Le perfectionnisme est une forme sophistiquée de procrastination — vous restez immobile en prétendant vouloir faire les choses parfaitement. » — `C190`

**Sections de la fiche jumelle** :

- Concepts enseignés
- La neuroscience de la procrastination
- Les trois types de procrastinateurs
- La logique masculine face à la procrastination
- La structure comme solution
- Vaincre-la-peur-synthese
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- Ressources liées
- Note de Bartilabas (post-enrichissement)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C190`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 26. À mort la procrastination (matin)

- **Identifiant** : `C049` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/procrastination-matin`
- **Base thématique** : `procrastination`
- **Taille de la fiche** : 1262 mots (contenu de session absent)

**Formation jumelle** : `C190` — À mort la procrastination  
*mode : theme · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « La procrastination n'est pas un problème de temps — c'est un problème émotionnel. Vous ne reportez pas parce que vous manquez de temps, vous reportez parce que quelque chose en vous veut éviter cette tâche. » — `C190`
- « L'homme qui agit malgré la peur développe un avantage compétitif que l'homme qui attend de se sentir prêt n'aura jamais. » — `C190`
- « Le perfectionnisme est une forme sophistiquée de procrastination — vous restez immobile en prétendant vouloir faire les choses parfaitement. » — `C190`

**Sections de la fiche jumelle** :

- Concepts enseignés
- La neuroscience de la procrastination
- Les trois types de procrastinateurs
- La logique masculine face à la procrastination
- La structure comme solution
- Vaincre-la-peur-synthese
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- Ressources liées
- Note de Bartilabas (post-enrichissement)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C190`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 27. Une motivation en beton (apres-midi)

- **Identifiant** : `C053` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/une-motivation-en-beton-apres-midi`
- **Base thématique** : `une-motivation-en-beton`
- **Taille de la fiche** : 2007 mots (contenu de session absent)

**Formation jumelle** : `C047` — Une motivation en béton  
*mode : theme · confiance : 0.5*

**Contenu verbatim disponible** (couche 1) :

> MES 10 CITATIONS PERSONNELLES PRÉFÉRÉES SUR LA MOTIVATION
> Citations sur la motivation connues…
> 1. “Le succès c’est d’aller d’échec en échec sans perdre son enthousiasme” ~ Winston Churchill
> 2. “La motivation vous sert de démarreur, mais c’est l’habitude qui fait continuer” ~ Jim Ryun
> 3. « Si tu rencontres un mur, ne repars pas en arrière: cherche comment escalader, traverser ou contourner le problème » ~ Michael Jordan …et moins connues…
> 4. “Le plus long chemin consiste à aller de 0 à 1, pas de 1 à 2, 3, 4…” ~ Danis Tanovic
> 5. “Motiver, c’est inverser le sens de l’énergie » ~ François Proust
> 6. “L’angoisse me motive. Si elle disparaissait, ça ne serait pas bon signe” ~ Joaquin Phoenix …et me

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Émettre-une-critique-constructive-synthese
- Analyse-de-cas-multiples-couples,-trahisons,-et-philosophie-de-vie-synthese
- Titre
- Citation
- Le concept de "trois naissances"
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C047`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 28. Une motivation en beton (matin)

- **Identifiant** : `C054` · **Catégorie** : Developpement Personnel
- **URL de catalogue** : `mat-consulting.fr/une-motivation-en-beton-matin`
- **Base thématique** : `une-motivation-en-beton`
- **Taille de la fiche** : 1915 mots (contenu de session absent)

**Formation jumelle** : `C047` — Une motivation en béton  
*mode : theme · confiance : 0.5*

**Contenu verbatim disponible** (couche 1) :

> MES 10 CITATIONS PERSONNELLES PRÉFÉRÉES SUR LA MOTIVATION
> Citations sur la motivation connues…
> 1. “Le succès c’est d’aller d’échec en échec sans perdre son enthousiasme” ~ Winston Churchill
> 2. “La motivation vous sert de démarreur, mais c’est l’habitude qui fait continuer” ~ Jim Ryun
> 3. « Si tu rencontres un mur, ne repars pas en arrière: cherche comment escalader, traverser ou contourner le problème » ~ Michael Jordan …et moins connues…
> 4. “Le plus long chemin consiste à aller de 0 à 1, pas de 1 à 2, 3, 4…” ~ Danis Tanovic
> 5. “Motiver, c’est inverser le sens de l’énergie » ~ François Proust
> 6. “L’angoisse me motive. Si elle disparaissait, ça ne serait pas bon signe” ~ Joaquin Phoenix …et me

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Émettre-une-critique-constructive-synthese
- Analyse-de-cas-multiples-couples,-trahisons,-et-philosophie-de-vie-synthese
- Titre
- Citation
- Le concept de "trois naissances"
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C047`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 29. Comprendre les gens, 2 (après-midi)

- **Identifiant** : `C055` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/analyser-gens-apres-midi`
- **Base thématique** : `analyser-gens`
- **Taille de la fiche** : 3143 mots (contenu de session absent)

**Formation jumelle** : `C057` — Comprendre les gens, 2  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Je ne vais pas y aller par quatre chemins : vous vous croyez peut-être très intelligents, mais tant que vous ne saurez pas analyser les gens, vous êtes complètement cons.
> L'oeil intelligent, selon les termes des psychologues de la perception, ne se borne pas à analyser les formes et les mouvements des individus qui sont devant nous. Il devine aussi leur pensées et leurs intentions en remarquant comment ils regardent, approchent, évitent, aident ou empêchent d'agir les autres objets et les autres individus ~ Steven Pinker, comprendre la nature humaine
> Nous sous estimons l'importance de l'intelligence sociale, de l'intelligence émotionnelle, et plus globalement de la faculté à comprendre les g

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'intelligence-relationnelle-1-synthese
- L'intelligence-relationnelle-2-synthese
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese
- 1. Le postulat de départ du livre
- 2. La mère de Stéphane comme témoin
- 3. Ce que l'homme attend vs. ce que la femme fait
- Cultive-ta-confiance-en-toi-synthese
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C057`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 30. Comprendre les gens, 2 (matin)

- **Identifiant** : `C056` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/analyser-gens-matin`
- **Base thématique** : `analyser-gens`
- **Taille de la fiche** : 1259 mots (contenu de session absent)

**Formation jumelle** : `C057` — Comprendre les gens, 2  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Je ne vais pas y aller par quatre chemins : vous vous croyez peut-être très intelligents, mais tant que vous ne saurez pas analyser les gens, vous êtes complètement cons.
> L'oeil intelligent, selon les termes des psychologues de la perception, ne se borne pas à analyser les formes et les mouvements des individus qui sont devant nous. Il devine aussi leur pensées et leurs intentions en remarquant comment ils regardent, approchent, évitent, aident ou empêchent d'agir les autres objets et les autres individus ~ Steven Pinker, comprendre la nature humaine
> Nous sous estimons l'importance de l'intelligence sociale, de l'intelligence émotionnelle, et plus globalement de la faculté à comprendre les g

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'intelligence-relationnelle-1-synthese
- L'intelligence-relationnelle-2-synthese
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese
- 1. Le postulat de départ du livre
- 2. La mère de Stéphane comme témoin
- 3. Ce que l'homme attend vs. ce que la femme fait
- Cultive-ta-confiance-en-toi-synthese
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C057`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 31. Comment avoir du charisme (apres-midi)

- **Identifiant** : `C058` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/comment-avoir-du-charisme-apres-midi`
- **Base thématique** : `comment-avoir-du-charisme`
- **Taille de la fiche** : 1972 mots (contenu de session absent)

**Formation jumelle** : `C066` — Comment avoir du charisme  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Si je devais me remémorer le Top3 des questions que j’ai le plus entendues depuis mes débuts (hormis le fameux comment briser la glace), cela ressemblerait probablement à ceci : « comment avoir du charisme ? »
> « Quelle est le secret / la recette du charisme ? »
> « A quand un séminaire sur le charisme ? » Et vous voulez savoir ce qu’étaient mes réponses ?
> #1 – « Ouh la »
> #2 – « A ma connaissance, personne n’a encore trouvé »
> #3 – « Je ne me sens pas encore prêt (pas légitime) »
> Le déclic est venu à l’issue de la journée « apprenez à négocier »
> J’avais acheté, lu et étudié en détail l’intégralité des livres publiés par les « experts » du sujet, y compris la fameuse méthode enseignée à Harvard.
> 

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'affaire-Elisabeth-Holmes-Theranos-est-une-parodie-du-XXIème-siècle-synthese
- L'ampleur du phénomène
- Les 7 points de la logique start-up
- Cultive-ta-confiance-en-toi-synthese
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- L'intelligence-relationnelle-2-synthese
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C066`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 32. Comment avoir du charisme (matin)

- **Identifiant** : `C059` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/comment-avoir-du-charisme-matin-2`
- **Base thématique** : `comment-avoir-du-charisme-matin`
- **Taille de la fiche** : 1700 mots (contenu de session absent)

**Formation jumelle** : `C066` — Comment avoir du charisme  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Si je devais me remémorer le Top3 des questions que j’ai le plus entendues depuis mes débuts (hormis le fameux comment briser la glace), cela ressemblerait probablement à ceci : « comment avoir du charisme ? »
> « Quelle est le secret / la recette du charisme ? »
> « A quand un séminaire sur le charisme ? » Et vous voulez savoir ce qu’étaient mes réponses ?
> #1 – « Ouh la »
> #2 – « A ma connaissance, personne n’a encore trouvé »
> #3 – « Je ne me sens pas encore prêt (pas légitime) »
> Le déclic est venu à l’issue de la journée « apprenez à négocier »
> J’avais acheté, lu et étudié en détail l’intégralité des livres publiés par les « experts » du sujet, y compris la fameuse méthode enseignée à Harvard.
> 

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'affaire-Elisabeth-Holmes-Theranos-est-une-parodie-du-XXIème-siècle-synthese
- L'ampleur du phénomène
- Les 7 points de la logique start-up
- Cultive-ta-confiance-en-toi-synthese
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- L'intelligence-relationnelle-2-synthese
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C066`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 33. Comprendre les gens (apres-midi) Rattrapage de sociologie pour ceux qui ont pris maths a l ecole

- **Identifiant** : `C060` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/comprendre-les-gens-apres-midirattrapage-de-sociologie-pour-ceux-qui-ont-pris-maths-a-l-ecole`
- **Base thématique** : `comprendre-les-gens-apres-midirattrapage-de-sociologie-pour-ceux-qui-ont-pris-maths-a-l-ecole`
- **Taille de la fiche** : 1407 mots (contenu de session absent)

**Formation jumelle** : `C073` — Comprendre les gens. Rattrapage de sociologie pour ceux qui ont pris maths à l'école  
*mode : theme · confiance : 0.89*

**Contenu verbatim disponible** (couche 1) :

> « L’humanité est ainsi, il ne s’agit pas de la changer, mais de la connaître. » – Flaubert
> IMMERSION DANS LE MONDE PASSIONNANT DE LA PSYCHO-SOCIOLOGIE !
> Axiome 1
> Vous avez ingéré des milliers d'informations à l’école, au collège, au lycée, à la faculté, en « grande école », en école d’art, ou ailleurs. Sur ces milliers, voire ces dizaines de milliers, combien concernaient la compréhension de l’être humain ?
> Réponse : une poignée, peut-être même moins. Zéro ?
> Axiome 2
> La plupart des gens s’estiment « au dessus de ça ». Ils estiment ne pas avoir besoin d’apprendre les mécanismes qui les régissent : Parce que, justement, ils refusent l’idée d’être régis par un autre mécanisme qu’eux-mêmes (c’es

**Concepts enseignés** :

La Théorie vs la Pratique — L'Absence de Profondeur · Le Retard Conceptuel — Le Recycling d'Idées · L'Anthropologie basée sur les Séries TV · La Forme comme Indicateur du Malaise · L'Identité des Feministes

**Sections de la fiche jumelle** :

- Concepts enseignés
- #IslamoGauchisme-let's-start-by-closing-the-sociology-faculties-synthese
- Contexte
- Les 5 temps de l'analyse
- 1. Origines du terme
- 2. octobre 2020 - Blanc-Mantecao frappe
- 3. Les alliés de Mélenchon
- Cette-école-en-Afrique-me-donne-envie-d'y-retourner-synthese
- Le-phénomène-des-profs-tiktokeuses-synthese
- Le profil

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C073`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 34. Comprendre les gens (matin) Rattrapage de sociologie pour ceux qui ont pris maths à l'école

- **Identifiant** : `C061` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/comprendre-les-gens-matinrattrapage-de-sociologie-pour-ceux-qui-ont-pris-maths-a-l-ecole`
- **Base thématique** : `comprendre-les-gens-matinrattrapage-de-sociologie-pour-ceux-qui-ont-pris-maths-a-l-ecole`
- **Taille de la fiche** : 2467 mots (contenu de session absent)

**Formation jumelle** : `C073` — Comprendre les gens. Rattrapage de sociologie pour ceux qui ont pris maths à l'école  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> « L’humanité est ainsi, il ne s’agit pas de la changer, mais de la connaître. » – Flaubert
> IMMERSION DANS LE MONDE PASSIONNANT DE LA PSYCHO-SOCIOLOGIE !
> Axiome 1
> Vous avez ingéré des milliers d'informations à l’école, au collège, au lycée, à la faculté, en « grande école », en école d’art, ou ailleurs. Sur ces milliers, voire ces dizaines de milliers, combien concernaient la compréhension de l’être humain ?
> Réponse : une poignée, peut-être même moins. Zéro ?
> Axiome 2
> La plupart des gens s’estiment « au dessus de ça ». Ils estiment ne pas avoir besoin d’apprendre les mécanismes qui les régissent : Parce que, justement, ils refusent l’idée d’être régis par un autre mécanisme qu’eux-mêmes (c’es

**Concepts enseignés** :

La Théorie vs la Pratique — L'Absence de Profondeur · Le Retard Conceptuel — Le Recycling d'Idées · L'Anthropologie basée sur les Séries TV · La Forme comme Indicateur du Malaise · L'Identité des Feministes

**Sections de la fiche jumelle** :

- Concepts enseignés
- #IslamoGauchisme-let's-start-by-closing-the-sociology-faculties-synthese
- Contexte
- Les 5 temps de l'analyse
- 1. Origines du terme
- 2. octobre 2020 - Blanc-Mantecao frappe
- 3. Les alliés de Mélenchon
- Cette-école-en-Afrique-me-donne-envie-d'y-retourner-synthese
- Le-phénomène-des-profs-tiktokeuses-synthese
- Le profil

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C073`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 35. Confiance en soi (apres-midi)

- **Identifiant** : `C062` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/confiance-en-soi-apres-midi`
- **Base thématique** : `confiance-en-soi`
- **Taille de la fiche** : 1604 mots (contenu de session absent)

**Formation jumelle** : `C064` — Confiance en soi  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Un proverbe africain dit de se méfier d’un homme qui vous vend des chemises torse nu. Je ne connais pas beaucoup de proverbes africains. C’est même le seul, à vrai dire (j’ai attendu des années, de pouvoir le placer à bon escient !). Méfiez-vous des vendeurs de confiance en soi, vérifiez qu’ils ne soient pas torse nu. JE L’AVAIS DÉJÀ ÉCRIT DANS L’HOMME IDÉAL
> « À en croire l’expression populaire, la confiance en soi s’utiliserait en doses, la fameuse « bonne dose de confiance en soi ». Comme la levure ou le sucre vanillé, on pourrait donc la stocker (date de péremption à l’appui), et en sortir du placard, aussi souvent que nécessaire, la quantité demandée par la vie (…). Mais stockez tant que

**Sections de la fiche jumelle** :

- Concepts enseignés
- Cultive-ta-confiance-en-toi-synthese
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Gaslighting-cette-drôle-manière-d'abréger-les-femmes-synthese
- 1. Le témoignage analyzed
- 2. Les techniques de gaslighting
- 3. L'effet sur la victime

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C064`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 36. Confiance en soi (matin)

- **Identifiant** : `C063` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/confiance-en-soi-matin`
- **Base thématique** : `confiance-en-soi`
- **Taille de la fiche** : 2161 mots (contenu de session absent)

**Formation jumelle** : `C064` — Confiance en soi  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Un proverbe africain dit de se méfier d’un homme qui vous vend des chemises torse nu. Je ne connais pas beaucoup de proverbes africains. C’est même le seul, à vrai dire (j’ai attendu des années, de pouvoir le placer à bon escient !). Méfiez-vous des vendeurs de confiance en soi, vérifiez qu’ils ne soient pas torse nu. JE L’AVAIS DÉJÀ ÉCRIT DANS L’HOMME IDÉAL
> « À en croire l’expression populaire, la confiance en soi s’utiliserait en doses, la fameuse « bonne dose de confiance en soi ». Comme la levure ou le sucre vanillé, on pourrait donc la stocker (date de péremption à l’appui), et en sortir du placard, aussi souvent que nécessaire, la quantité demandée par la vie (…). Mais stockez tant que

**Sections de la fiche jumelle** :

- Concepts enseignés
- Cultive-ta-confiance-en-toi-synthese
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Gaslighting-cette-drôle-manière-d'abréger-les-femmes-synthese
- 1. Le témoignage analyzed
- 2. Les techniques de gaslighting
- 3. L'effet sur la victime

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C064`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 37. Discernement – après-midi

- **Identifiant** : `C067` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/discenement-apres-midi`
- **Base thématique** : `discenement`
- **Taille de la fiche** : 1446 mots (contenu de session absent)

**Formation jumelle** : `C071` — Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)  
*mode : theme · confiance : 0.67*

**Sections de la fiche jumelle** :

- Concepts enseignés
- The-brilliant-idea-from-the-creators-of-#Metoo-to-save-the-movement-synthese
- Video-p1WU4JiuIzQ-synthese
- L'intelligence-relationnelle-2-synthese
- Video-tiDHbY0rQKQ-synthese
- L'intelligence-relationnelle-1-synthese
- Video-x2zvDhh2yu4-synthese
- This-case-would-be-front-page-news-if-only-the-murderer-were-a-man,-but...-🤫-synthese
- This-government-campaign-was-so-successful-that-you've-(probably)-never-seen-it.-synthese
- Fiche transcrite par Bartilabas

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C071`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 38. Discernement – matin

- **Identifiant** : `C068` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/discernement-matin`
- **Base thématique** : `discernement`
- **Taille de la fiche** : 1129 mots (contenu de session absent)

**Formation jumelle** : `C069` — Survivre aux mensonges du nouveau monde (le discernement)  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Malheureusement nous manquons de discernement et d'indépendance dans nos choix ; nous ne distinguons pas entre l'idole de la veille, devenue méprisable aujourd'hui, et celle qui mérite tous nos sacrifices ~ Astolphe de Custine (1790-1857)
> On ne meurt pas impunément le soir de l'anniversaire des gens. Je l'ai découvert à l'occasion de la disparition de celui qui m'aura appris – sinon « tout » – du moins à respirer, à écouter et à m'exprimer ; ce qui, vous en conviendrez, n'est pas quantité négligeable dans une vie en communauté (non, ça n'est pas Pierre Bénichou). Tintin est pénible pic.twitter.com/gO5rcW2djG
> — Tweetinão (@tintinades) March 13, 2024 L'échelle des vertus Qu'y a t-il au-dessus 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- L'intelligence-relationnelle-1-synthese
- Combien-de-fois-A.Buzyn-a-t-elle-menti-à-la-commission-d'enquête-synthese
- Méthodologie
- Score de mentir
- Points critiques relevés
- Citation du Professeur Raoult
- Video-py5soTfXpxQ-synthese
- Un-monde-sans-hommes-cette-nouvelle-lubie-des-séries-cache-un-projet-eugéniste-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C069`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 39. Formations — Stéphane Édouard

- **Identifiant** : `C078` · **Catégorie** : Non catégorisé
- **URL** : —
- **Base** : —
- **Taille de la fiche** : 2613 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.33) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 40. Logique de l'Homme (après-midi)

- **Identifiant** : `C082` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/comprendre-les-hommes-apres-midi`
- **Base thématique** : `comprendre-les-hommes`
- **Taille de la fiche** : 1194 mots (contenu de session absent)

**Formation jumelle** : `C084` — Logique des hommes – le côté obscur de H pur  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Expliquer le langage des femmes, leur logique, comment elles voient le monde : c'est ma spécialité, j'aime ça et je suis le meilleur. Mais si vous ne réussissez pas à comprendre les hommes, alors tout ceci ne sert à rien ! Voir cette publication sur Instagram Une publication partagée par Nora & Khalid (@noraandkhalid) La relation homme-femme, c'est un puzzle, une histoire de compatibilité, il faut comprendre les penchants des uns et des autres pour tenter de s'emboiter au mieux.
> Comprendre les hommes, c'est simple…
> …encore faut-il avoir la bonne paire de lunettes
> Car nous (les hommes) sommes aussi bourrés de biais cognitifs que les femmes, nous n'en avons tout simplement pas conscience.
> Nous

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-santé-mentale-synthese
- La-résilience-synthese
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese
- 1. Le postulat de départ du livre
- 2. La mère de Stéphane comme témoin
- 3. Ce que l'homme attend vs. ce que la femme fait
- Ne-soyez-plus-les-esclaves-des-femmes-synthese
- 1. La gratification indirecte (Le "mini-Darmanin")
- 2. Le refus de faire le travail à la place (La logique de l'autonomie)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C084`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 41. Logique de l'Homme (matin)

- **Identifiant** : `C083` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/comprendre-les-hommes-matin`
- **Base thématique** : `comprendre-les-hommes`
- **Taille de la fiche** : 1044 mots (contenu de session absent)

**Formation jumelle** : `C084` — Logique des hommes – le côté obscur de H pur  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Expliquer le langage des femmes, leur logique, comment elles voient le monde : c'est ma spécialité, j'aime ça et je suis le meilleur. Mais si vous ne réussissez pas à comprendre les hommes, alors tout ceci ne sert à rien ! Voir cette publication sur Instagram Une publication partagée par Nora & Khalid (@noraandkhalid) La relation homme-femme, c'est un puzzle, une histoire de compatibilité, il faut comprendre les penchants des uns et des autres pour tenter de s'emboiter au mieux.
> Comprendre les hommes, c'est simple…
> …encore faut-il avoir la bonne paire de lunettes
> Car nous (les hommes) sommes aussi bourrés de biais cognitifs que les femmes, nous n'en avons tout simplement pas conscience.
> Nous

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-santé-mentale-synthese
- La-résilience-synthese
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese
- 1. Le postulat de départ du livre
- 2. La mère de Stéphane comme témoin
- 3. Ce que l'homme attend vs. ce que la femme fait
- Ne-soyez-plus-les-esclaves-des-femmes-synthese
- 1. La gratification indirecte (Le "mini-Darmanin")
- 2. Le refus de faire le travail à la place (La logique de l'autonomie)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C084`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 42. L'amant idéal, 2 : faire jouir une femme (matin)

- **Identifiant** : `C086` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/faire-lamour-a-une-femme-matin`
- **Base thématique** : `faire-lamour-a-une-femme`
- **Taille de la fiche** : 1214 mots (contenu de session absent)

**Formation jumelle** : `C042` — L'amant, 2  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon. Je vais faire simple. Pour une grande, pour une immense majorité d'hétéros binaires de base, l'acte sexuel unissant un homme et une femme se réduit à remorquer une F (consentante) sur une app' de rencontre
> essuyer avec grâce – et un semblant de détachement – une addition au restaurant plus ou moins salée
> un enchaînement plus ou moins hésitant et foireux pour prolonger la soirée chez l'un ou chez l'autre, sous couvert d'un prétexte risible
> un effeuillage penaud conclu par une pénétration vigoureuse et empressée avant le réglementaire repos du guerrier Voilà, pliez bagage, y'a plus à rien à voir, ron-ron dit celui qui se met à ronfler, et « merci pour ce moment » dit celle qui s'échappe s

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C042`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 43. Les jeunes filles, 1: Decoder les attentes feminines (apres-midi)

- **Identifiant** : `C089` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-1-decoder-les-attentes-feminines-apres-midi`
- **Base thématique** : `les-jeunes-filles-1-decoder-les-attentes-feminines`
- **Taille de la fiche** : 2448 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.2) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 44. Les jeunes filles, 1: Decoder les attentes feminines (matin)

- **Identifiant** : `C090` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-1-decoder-les-attentes-feminines-matin`
- **Base thématique** : `les-jeunes-filles-1-decoder-les-attentes-feminines`
- **Taille de la fiche** : 1274 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.2) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 45. Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (après midi)

- **Identifiant** : `C091` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-2-plus-de-rencontres-maintenant-apres-midi`
- **Base thématique** : `les-jeunes-filles-2-plus-de-rencontres-maintenant`
- **Taille de la fiche** : 1326 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.29) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 46. Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (matin)

- **Identifiant** : `C092` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-2-plus-de-rencontres-maintenant-matin`
- **Base thématique** : `les-jeunes-filles-2-plus-de-rencontres-maintenant`
- **Taille de la fiche** : 1416 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.4) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 47. Logique des femmes (apres-midi)

- **Identifiant** : `C093` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/logique-des-femmes-apres-midi`
- **Base thématique** : `logique-des-femmes`
- **Taille de la fiche** : 1149 mots (contenu de session absent)

**Formation jumelle** : `C081` — Logique des femmes  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous êtes-vous déjà fait l’une des réflexions suivantes : Comment ne peut-elle pas voir ce que je vois
> Cette fille là ne devrait pas (ne peut pas) être avec ce type là !
> Comment a t-elle pu me dire X à moi et, dans la minute, qui suit Y à quelqu’un d’autre (meilleure amie, confident)
> Pourquoi dit elle A alors que c’est manifestement B qui est devant ses/nos yeux ?
> Pourquoi l’amitié homme-femme finit-elle toujours mal, à quelle échéance, et comment ?
> Comment peut-elle prendre une décision aussi importante, basée uniquement sur […]
> Comment une femme peut être la « femme de la vie » de 2 hommes totalement différents, et leur « correspondre » totalement à chacun ?
> Pourquoi une femme peut se savo

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C081`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 48. Logique des femmes II (apres-midi)

- **Identifiant** : `C094` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/logique-des-femmes-ii-apres-midi`
- **Base thématique** : `logique-des-femmes-ii`
- **Taille de la fiche** : 1150 mots (contenu de session absent)

**Formation jumelle** : `C081` — Logique des femmes  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous êtes-vous déjà fait l’une des réflexions suivantes : Comment ne peut-elle pas voir ce que je vois
> Cette fille là ne devrait pas (ne peut pas) être avec ce type là !
> Comment a t-elle pu me dire X à moi et, dans la minute, qui suit Y à quelqu’un d’autre (meilleure amie, confident)
> Pourquoi dit elle A alors que c’est manifestement B qui est devant ses/nos yeux ?
> Pourquoi l’amitié homme-femme finit-elle toujours mal, à quelle échéance, et comment ?
> Comment peut-elle prendre une décision aussi importante, basée uniquement sur […]
> Comment une femme peut être la « femme de la vie » de 2 hommes totalement différents, et leur « correspondre » totalement à chacun ?
> Pourquoi une femme peut se savo

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C081`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 49. Logique des femmes II (matin)

- **Identifiant** : `C095` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/logique-des-femmes-ii-matin`
- **Base thématique** : `logique-des-femmes-ii`
- **Taille de la fiche** : 1413 mots (contenu de session absent)

**Formation jumelle** : `C081` — Logique des femmes  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous êtes-vous déjà fait l’une des réflexions suivantes : Comment ne peut-elle pas voir ce que je vois
> Cette fille là ne devrait pas (ne peut pas) être avec ce type là !
> Comment a t-elle pu me dire X à moi et, dans la minute, qui suit Y à quelqu’un d’autre (meilleure amie, confident)
> Pourquoi dit elle A alors que c’est manifestement B qui est devant ses/nos yeux ?
> Pourquoi l’amitié homme-femme finit-elle toujours mal, à quelle échéance, et comment ?
> Comment peut-elle prendre une décision aussi importante, basée uniquement sur […]
> Comment une femme peut être la « femme de la vie » de 2 hommes totalement différents, et leur « correspondre » totalement à chacun ?
> Pourquoi une femme peut se savo

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C081`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 50. Logique des femmes (matin)

- **Identifiant** : `C096` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/logique-des-femmes-matin`
- **Base thématique** : `logique-des-femmes`
- **Taille de la fiche** : 1412 mots (contenu de session absent)

**Formation jumelle** : `C081` — Logique des femmes  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous êtes-vous déjà fait l’une des réflexions suivantes : Comment ne peut-elle pas voir ce que je vois
> Cette fille là ne devrait pas (ne peut pas) être avec ce type là !
> Comment a t-elle pu me dire X à moi et, dans la minute, qui suit Y à quelqu’un d’autre (meilleure amie, confident)
> Pourquoi dit elle A alors que c’est manifestement B qui est devant ses/nos yeux ?
> Pourquoi l’amitié homme-femme finit-elle toujours mal, à quelle échéance, et comment ?
> Comment peut-elle prendre une décision aussi importante, basée uniquement sur […]
> Comment une femme peut être la « femme de la vie » de 2 hommes totalement différents, et leur « correspondre » totalement à chacun ?
> Pourquoi une femme peut se savo

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C081`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 51. Au secours, mon chef est une femme (/un homme) – apres-midi

- **Identifiant** : `C098` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/manager-equipe-femmes-apresmidi`
- **Base thématique** : `manager-equipe-femmes`
- **Taille de la fiche** : 3590 mots (contenu de session absent)

**Formation jumelle** : `C100` — Au secours, mon chef est une femme (/un homme) ?  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Niveau management au féminin, femmes et pouvoir, j'ai commencé mon expérience à la dure, comme en témoigne mon dernier relevé d'appréciation chez Sofres en 2005 :
> Le texte manuscrit émane d'une femme, en l'occurence la n+1 d'Alain Imbert
> 3 exemples de biais H/F (parmi plusieurs centaines) Les hommes et les femmes, bien que disposant d'une intelligence moyenne similaire, ne recourent pas aux mêmes stratégies pour asseoir leur autorité dans l'entreprise
> Les subordonnées femmes, à productivité globale équivalente, ne réagissent pas à l'autorité comme leurs homologues masculins, ayant plus tendance à fomenter et comploter dans leurs dos hors des évaluations frontales
> Les femmes, dans leur grande

**Sections de la fiche jumelle** :

- Concepts enseignés
- Les-femmes-ont-tout-inventé-(source-une-femme)-synthese
- 1. Le "starter pack" idéologique du féminisme
- 2. L'invention du jeu vidéo : les Faits
- 3. Le biais du survivant comme méthode
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance
- 2. La stratégie de survie : s'entourer d'hommes
- 3. Le "sixième sens" féminin
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C100`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 52. Au secours, mon chef est une femme (/un homme) – matin

- **Identifiant** : `C099` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/manager-equipe-femmes-matin`
- **Base thématique** : `manager-equipe-femmes`
- **Taille de la fiche** : 1517 mots (contenu de session absent)

**Formation jumelle** : `C100` — Au secours, mon chef est une femme (/un homme) ?  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Niveau management au féminin, femmes et pouvoir, j'ai commencé mon expérience à la dure, comme en témoigne mon dernier relevé d'appréciation chez Sofres en 2005 :
> Le texte manuscrit émane d'une femme, en l'occurence la n+1 d'Alain Imbert
> 3 exemples de biais H/F (parmi plusieurs centaines) Les hommes et les femmes, bien que disposant d'une intelligence moyenne similaire, ne recourent pas aux mêmes stratégies pour asseoir leur autorité dans l'entreprise
> Les subordonnées femmes, à productivité globale équivalente, ne réagissent pas à l'autorité comme leurs homologues masculins, ayant plus tendance à fomenter et comploter dans leurs dos hors des évaluations frontales
> Les femmes, dans leur grande

**Sections de la fiche jumelle** :

- Concepts enseignés
- Les-femmes-ont-tout-inventé-(source-une-femme)-synthese
- 1. Le "starter pack" idéologique du féminisme
- 2. L'invention du jeu vidéo : les Faits
- 3. Le biais du survivant comme méthode
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance
- 2. La stratégie de survie : s'entourer d'hommes
- 3. Le "sixième sens" féminin
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C100`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 53. Premier rendez-vous (apres-midi)10 scenarii parfaits

- **Identifiant** : `C102` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/premier-rendez-vous-apres-midi10-scenarii-parfaits`
- **Base thématique** : `premier-rendez-vous-apres-midi10-scenarii-parfaits`
- **Taille de la fiche** : 1146 mots (contenu de session absent)

**Formation jumelle** : `C101` — Premier rendez-vous 10 scenarii parfaits  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Version courte La séquence technologique de ces dernières années a profondément changé la façon de communiquer au quotidien.
> Les femmes sont les premières utilisatrices de leur smartphone et des applications à vocation sociale/tchat.
> Les premiers rendez-vous doivent donc voir leur scenarii évoluer en fonction, pour leur redonner un vraie valeur ajoutée Version longue
> « Le monde déteste le changement, c’est pourtant la seule chose qui lui a permis de progresser. » – Charles F. Kettering
> Le séminaire 100 jours (parmi nos meilleures ventes toutes catégories confondues) conceptualisait la révolution numérique des rencontres, sous l’angle des principales applications de dialogue, tchat, etc. qui 

**Concepts enseignés** :

Le Mythe du TOP 1% Déconstruit par les Chiffres · La Sélectivité Masculine vs Féminine · Le Capital Triple (Physique, Intellectuel, Économique) · Le Dilemme du Virtuel vs In Vivo

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-qA7bQ-TfQoQ-synthese
- 🎙️ Thème central
- 🔑 Points clés
- 📊 Analyse
- Tinder-on-croyait-que-les-femmes-ne-matchaient-que-le-TOP-1%...-Révélation-c'est-BIEN-MOINS-!-synthese
- J'ai-oublié-comment-draguer-;-heureusement-ces-trois-là-sont-là-pour-me-le-rappeler-synthese
- Gaslighting-cette-drôle-manière-d’abréger-les-femmes-synthese
- #Zemmour2022,-ép.2-L.Salamé-et-L.Ruquier-vomissent-sur-lui-(et-appellent-ça-une-interview)-synthese
- 1. Le quadruple enjeu

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C101`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 54. Premier rendez-vous (matin) 10 scenarii parfaits

- **Identifiant** : `C103` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/premier-rendez-vous-matin10-scenarii-parfaits`
- **Base thématique** : `premier-rendez-vous-matin10-scenarii-parfaits`
- **Taille de la fiche** : 1159 mots (contenu de session absent)

**Formation jumelle** : `C101` — Premier rendez-vous 10 scenarii parfaits  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Version courte La séquence technologique de ces dernières années a profondément changé la façon de communiquer au quotidien.
> Les femmes sont les premières utilisatrices de leur smartphone et des applications à vocation sociale/tchat.
> Les premiers rendez-vous doivent donc voir leur scenarii évoluer en fonction, pour leur redonner un vraie valeur ajoutée Version longue
> « Le monde déteste le changement, c’est pourtant la seule chose qui lui a permis de progresser. » – Charles F. Kettering
> Le séminaire 100 jours (parmi nos meilleures ventes toutes catégories confondues) conceptualisait la révolution numérique des rencontres, sous l’angle des principales applications de dialogue, tchat, etc. qui 

**Concepts enseignés** :

Le Mythe du TOP 1% Déconstruit par les Chiffres · La Sélectivité Masculine vs Féminine · Le Capital Triple (Physique, Intellectuel, Économique) · Le Dilemme du Virtuel vs In Vivo

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-qA7bQ-TfQoQ-synthese
- 🎙️ Thème central
- 🔑 Points clés
- 📊 Analyse
- Tinder-on-croyait-que-les-femmes-ne-matchaient-que-le-TOP-1%...-Révélation-c'est-BIEN-MOINS-!-synthese
- J'ai-oublié-comment-draguer-;-heureusement-ces-trois-là-sont-là-pour-me-le-rappeler-synthese
- Gaslighting-cette-drôle-manière-d’abréger-les-femmes-synthese
- #Zemmour2022,-ép.2-L.Salamé-et-L.Ruquier-vomissent-sur-lui-(et-appellent-ça-une-interview)-synthese
- 1. Le quadruple enjeu

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C101`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 55. Rencontre (enfin) une fille bien ! (après-midi)

- **Identifiant** : `C104` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/rencontrer-une-fille-bien-apres-midi`
- **Base thématique** : `rencontrer-une-fille-bien`
- **Taille de la fiche** : 2299 mots (contenu de session absent)

**Formation jumelle** : `C106` — Où / quand / comment rencontrer une fille bien  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> D'après toi, rencontrer une fille bien, ça s'attend
> se mérite
> se provoque ? Réponse : la 3. Problème : la plupart des gens déploient plus d'énergie, de réflexion, de comparaison, de benchmark à choisir une maison, un crédit, une auto, voire un ordinateur, qu'à réfléchir à la personne avec qui ils devront (théoriquement) passer le reste de leur vie. Pourquoi ? Voir cette publication sur Instagram Une publication partagée par Eliott & Lilian 🦈 (@eliottlilian_off) La plupart des hommes n'ont aucune idée de ce qu'est une fille bien
> Empêtrés par le reste de son oedipe mal digéré, et incapable d'articuler dialectiquement la maman et la putain, l'homme hétérosexuel « normal » a beau émettre le vagu

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'un-de-ces-deux-protagonistes-me-provoque-un-réel-malaise-🤢,-mais-lequel-synthese
- Formations et fiches liées
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Si-seulement-ce-pouvait-être-la-dernière-fois-🕯-(Affaire-Lola)-synthese
- Applications pratiques
- Video-q5jirxsgC5Q-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C106`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 56. Rencontre (enfin) une fille bien ! (matin)

- **Identifiant** : `C105` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/rencontrer-une-fille-bien-matin`
- **Base thématique** : `rencontrer-une-fille-bien`
- **Taille de la fiche** : 2481 mots (contenu de session absent)

**Formation jumelle** : `C106` — Où / quand / comment rencontrer une fille bien  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> D'après toi, rencontrer une fille bien, ça s'attend
> se mérite
> se provoque ? Réponse : la 3. Problème : la plupart des gens déploient plus d'énergie, de réflexion, de comparaison, de benchmark à choisir une maison, un crédit, une auto, voire un ordinateur, qu'à réfléchir à la personne avec qui ils devront (théoriquement) passer le reste de leur vie. Pourquoi ? Voir cette publication sur Instagram Une publication partagée par Eliott & Lilian 🦈 (@eliottlilian_off) La plupart des hommes n'ont aucune idée de ce qu'est une fille bien
> Empêtrés par le reste de son oedipe mal digéré, et incapable d'articuler dialectiquement la maman et la putain, l'homme hétérosexuel « normal » a beau émettre le vagu

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'un-de-ces-deux-protagonistes-me-provoque-un-réel-malaise-🤢,-mais-lequel-synthese
- Formations et fiches liées
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Si-seulement-ce-pouvait-être-la-dernière-fois-🕯-(Affaire-Lola)-synthese
- Applications pratiques
- Video-q5jirxsgC5Q-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C106`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 57. Intelligence relationnelle, 1: Doubler son RESEAU (après-midi)

- **Identifiant** : `C114` · **Catégorie** : Reseau Influence
- **URL de catalogue** : `mat-consulting.fr/intelligence-relationnelle-1-doubler-son-reseau-apres-midi`
- **Base thématique** : `intelligence-relationnelle-1-doubler-son-reseau`
- **Taille de la fiche** : 3001 mots (contenu de session absent)

**Formation jumelle** : `C071` — Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)  
*mode : theme · confiance : 0.5*

**Sections de la fiche jumelle** :

- Concepts enseignés
- The-brilliant-idea-from-the-creators-of-#Metoo-to-save-the-movement-synthese
- Video-p1WU4JiuIzQ-synthese
- L'intelligence-relationnelle-2-synthese
- Video-tiDHbY0rQKQ-synthese
- L'intelligence-relationnelle-1-synthese
- Video-x2zvDhh2yu4-synthese
- This-case-would-be-front-page-news-if-only-the-murderer-were-a-man,-but...-🤫-synthese
- This-government-campaign-was-so-successful-that-you've-(probably)-never-seen-it.-synthese
- Fiche transcrite par Bartilabas

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C071`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 58. Intelligence relationnelle, 1: Doubler son RESEAU (matin)

- **Identifiant** : `C115` · **Catégorie** : Reseau Influence
- **URL de catalogue** : `mat-consulting.fr/intelligence-relationnelle-1-doubler-son-reseau-matin`
- **Base thématique** : `intelligence-relationnelle-1-doubler-son-reseau`
- **Taille de la fiche** : 1010 mots (contenu de session absent)

**Formation jumelle** : `C071` — Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)  
*mode : theme · confiance : 0.5*

**Sections de la fiche jumelle** :

- Concepts enseignés
- The-brilliant-idea-from-the-creators-of-#Metoo-to-save-the-movement-synthese
- Video-p1WU4JiuIzQ-synthese
- L'intelligence-relationnelle-2-synthese
- Video-tiDHbY0rQKQ-synthese
- L'intelligence-relationnelle-1-synthese
- Video-x2zvDhh2yu4-synthese
- This-case-would-be-front-page-news-if-only-the-murderer-were-a-man,-but...-🤫-synthese
- This-government-campaign-was-so-successful-that-you've-(probably)-never-seen-it.-synthese
- Fiche transcrite par Bartilabas

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C071`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 59. Intelligence sociale online (apres-midi) Internet, reseaux, applications

- **Identifiant** : `C116` · **Catégorie** : Reseau Influence
- **URL de catalogue** : `mat-consulting.fr/intelligence-sociale-online-apres-midiinternet-reseaux-applications`
- **Base thématique** : `intelligence-sociale-online-apres-midiinternet-reseaux-applications`
- **Taille de la fiche** : 1093 mots (contenu de session absent)

**Formation jumelle** : `C113` — Intelligence sociale III : Internet, réseaux, applications  
*mode : theme · confiance : 0.67*

**Contenu verbatim disponible** (couche 1) :

> Les comédiens qui se voient décerner une récompense, plus ou moins méritée, remercient toujours (dans l’ordre ou dans le désordre) – 1 – Dieu, – 2 – leurs parents, – 3 – leurs enfants, – 4 – leur coach/mentor/professeur et – 5 – le producteur/sponsor qui a misé de l’argent sur eux etc.
> (sans oublier Harvey Weinstein, mais ça, c'était avant le drame)
> En réfléchissant sincèrement, profondément et honnêtement à tout ce qui me permet de vivre cette vie que j’adore (« vivre bien », dans le noble sens du terme, c’est-à-dire pas uniquement gagner de l’argent mais le faire en me sentant utile et nécessaire, il y a quelqu’un que je devrais remercier en tout premier lieu. Devant mes professeurs, mes p

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'intelligence-relationnelle-1-synthese
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Confiné,-il-rédige-une-ode-à-la-beauté-féminine-➡️-devinez-qui-l'agresse-synthese
- Tinder-on-croyait-que-les-femmes-ne-matchaient-que-le-TOP-1%...-Révélation-c'est-BIEN-MOINS-!-synthese
- L'intelligence-relationnelle-2-synthese
- Vidéoscopie-–-Reportage-Envoyé-Spécial-sur-les-injections-d'acide-hyaluronique-low-cost-sur-Instagra-synthese
- Formations et fiches liées
- J'achète-la-formation-d'une-influenceuse-pour-séduire-sur-les-réseaux-synthese
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C113`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 60. Intelligence sociale online (matin) Internet, reseaux, applications

- **Identifiant** : `C117` · **Catégorie** : Reseau Influence
- **URL de catalogue** : `mat-consulting.fr/intelligence-sociale-online-matininternet-reseaux-applications`
- **Base thématique** : `intelligence-sociale-online-matininternet-reseaux-applications`
- **Taille de la fiche** : 1107 mots (contenu de session absent)

**Formation jumelle** : `C113` — Intelligence sociale III : Internet, réseaux, applications  
*mode : theme · confiance : 0.67*

**Contenu verbatim disponible** (couche 1) :

> Les comédiens qui se voient décerner une récompense, plus ou moins méritée, remercient toujours (dans l’ordre ou dans le désordre) – 1 – Dieu, – 2 – leurs parents, – 3 – leurs enfants, – 4 – leur coach/mentor/professeur et – 5 – le producteur/sponsor qui a misé de l’argent sur eux etc.
> (sans oublier Harvey Weinstein, mais ça, c'était avant le drame)
> En réfléchissant sincèrement, profondément et honnêtement à tout ce qui me permet de vivre cette vie que j’adore (« vivre bien », dans le noble sens du terme, c’est-à-dire pas uniquement gagner de l’argent mais le faire en me sentant utile et nécessaire, il y a quelqu’un que je devrais remercier en tout premier lieu. Devant mes professeurs, mes p

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'intelligence-relationnelle-1-synthese
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Confiné,-il-rédige-une-ode-à-la-beauté-féminine-➡️-devinez-qui-l'agresse-synthese
- Tinder-on-croyait-que-les-femmes-ne-matchaient-que-le-TOP-1%...-Révélation-c'est-BIEN-MOINS-!-synthese
- L'intelligence-relationnelle-2-synthese
- Vidéoscopie-–-Reportage-Envoyé-Spécial-sur-les-injections-d'acide-hyaluronique-low-cost-sur-Instagra-synthese
- Formations et fiches liées
- J'achète-la-formation-d'une-influenceuse-pour-séduire-sur-les-réseaux-synthese
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C113`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 61. L art delicat de la connexion (apres-midi)

- **Identifiant** : `C119` · **Catégorie** : Reseau Influence
- **URL de catalogue** : `mat-consulting.fr/l-art-delicat-de-la-connexion-apres-midi`
- **Base thématique** : `l-art-delicat-de-la-connexion`
- **Taille de la fiche** : 1032 mots (contenu de session absent)

**Formation jumelle** : `C112` — L'art delicat de la connexion  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Tout le monde sait (« sent ») l’importance de la connexion, personne ou presque ne sait la définir, la concevoir clairement, l’exposer aisément.
> Ce que les femmes en disent :
> « C’était magique »
> « Je l’ai su tout de suite »
> « J’aurais été prête à tout pour lui »
> « Ca ne s’explique pas, ça se ressent »
> Au risque d’être toujours un peu plus iconoclaste, qu’en savent-elles, que ça ne s’explique pas ? Et à force de les entendre dire – à qui veut l’entendre – que rien ne s’explique, jamais, ça ne fait justement que décupler mon envie d’expliquer mieux.
> FAISONS SIMPLE
> Vous pouvez bien savoir briser la glace avec la terre entière, partout et tout le temps (c’est une image, évidemment que dans la ré

**Sections de la fiche jumelle** :

- Concepts enseignés
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens
- 3. L'art d'"arracher" vs. cueillir ce qui s'offre
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)
- Stratégie 2: Le tango comme porte d'entrée (~6/10)
- Stratégie 3: La carte de visite (~12/20)
- Stratégie 4: Les cadeaux (~14-15/20)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C112`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 62. L art delicat de la connexion (matin)

- **Identifiant** : `C120` · **Catégorie** : Reseau Influence
- **URL de catalogue** : `mat-consulting.fr/l-art-delicat-de-la-connexion-matin`
- **Base thématique** : `l-art-delicat-de-la-connexion`
- **Taille de la fiche** : 992 mots (contenu de session absent)

**Formation jumelle** : `C112` — L'art delicat de la connexion  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Tout le monde sait (« sent ») l’importance de la connexion, personne ou presque ne sait la définir, la concevoir clairement, l’exposer aisément.
> Ce que les femmes en disent :
> « C’était magique »
> « Je l’ai su tout de suite »
> « J’aurais été prête à tout pour lui »
> « Ca ne s’explique pas, ça se ressent »
> Au risque d’être toujours un peu plus iconoclaste, qu’en savent-elles, que ça ne s’explique pas ? Et à force de les entendre dire – à qui veut l’entendre – que rien ne s’explique, jamais, ça ne fait justement que décupler mon envie d’expliquer mieux.
> FAISONS SIMPLE
> Vous pouvez bien savoir briser la glace avec la terre entière, partout et tout le temps (c’est une image, évidemment que dans la ré

**Sections de la fiche jumelle** :

- Concepts enseignés
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens
- 3. L'art d'"arracher" vs. cueillir ce qui s'offre
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)
- Stratégie 2: Le tango comme porte d'entrée (~6/10)
- Stratégie 3: La carte de visite (~12/20)
- Stratégie 4: Les cadeaux (~14-15/20)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C112`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 63. La santé mentale – après-midi

- **Identifiant** : `C124` · **Catégorie** : Sante Mentale
- **URL de catalogue** : `mat-consulting.fr/mars-apm`
- **Base thématique** : `mars-apm`
- **Taille de la fiche** : 3050 mots (contenu de session absent)

**Formation jumelle** : `C269` — La santé mentale – après-midi  
*mode : base-URL · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « Les hommes et les femmes ne bloquent pas au même endroit. La santé mentale des hommes et des femmes présente le même point commun au stade de l'angoisse, mais diverge après. » — `C269`
- « Le terme 'santé mentale' tel qu'utilisé aujourd'hui (2001-2015+) est récent et souvent utilisé à tort. » — `C269`
- « La PSY-industrie vs l'auto-analyse pratique — le vrai travail sur soi passe par la compréhension rationnelle, pas par le dogmatisme thérapeutique. » — `C269`

**Sections de la fiche jumelle** :

- Concepts enseignés
- Le modèle XANAX
- Différences hommes/femmes dans la gestion des émotions
- Sphères de la santé
- L'investissement dans un projet significatif
- Le discernement
- La-santé-mentale-synthese
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- La-résilience-synthese
- Gaslighting-cette-drôle-manière-d'abréger-les-femmes-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C269`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 64. La santé mentale – matin

- **Identifiant** : `C125` · **Catégorie** : Sante Mentale
- **URL de catalogue** : `mat-consulting.fr/mars-matin`
- **Base thématique** : `mars`
- **Taille de la fiche** : 2883 mots (contenu de session absent)

**Formation jumelle** : `C126` — Sauver sa santé mentale  
*mode : theme · confiance : 0.67*

**Contenu verbatim disponible** (couche 1) :

> L'expression comment préserver sa santé mentale n'a jamais été aussi recherché dans le monde Je n'aborderai pas l'épineux et sérieux sujet de la dépression. Si vous pensez être en dépression, ou connaissez des gens qui en souffrent, je suis au regret de vous dire clairement, d'entrée de jeu, que je n'ai pas de solution à apporter à cette pathologie. Navré.
> Les contenus présentés au cours de cette journée n'ont évidemment pas vocation à se substituer à ceux recueillis auprès d'un professionnel de la santé. Ils ne sont que l'avis d'un pauvre ingénieur en mécanique qui s'est vu greffer un DEA en sociologie, de surcroît ex-starlette de la tv et Youtuboomeur* à ses heures. Ceci étant mainten

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-santé-mentale-synthese
- Gaslighting-cette-drôle-manière-d'abréger-les-femmes-synthese
- 1. Le témoignage analyzed
- 2. Les techniques de gaslighting
- 3. L'effet sur la victime
- Video-m54h8ZXqHO0-synthese
- Sujet
- Thèmes abordés
- Question posée

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C126`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 65. Entouré pour réussir (après-midi)

- **Identifiant** : `C130` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/bien-sentourer-apresmidi`
- **Base thématique** : `bien-sentourer`
- **Taille de la fiche** : 3654 mots (contenu de session absent)

**Formation jumelle** : `C121` — S'entourer pour réussir, ou le secret des affinités électives  
*mode : theme · confiance : 0.67*

**Contenu verbatim disponible** (couche 1) :

> « Chacun veut être autonome, mais en même temps que grandit notre liberté individuelle grandit notre besoin d'être lié aux autres (…) il y a quelques années, seuls le couple, la famille et les amis étaient des lieux d'investissement affectif » ~ JC Kaufmann (le sociologue qui ne m'aime pas)
> Les paradoxes de quiconque cherche à bien s'entourer Dans une société narcissique, on cherche inlassablement son semblable, que l'on ne trouvera jamais puisque tout est conçu pour valoriser notre unicité (« parce que JE le vaux bien« )
> Pour des millions de personnes à travers le monde, savoir bien s'entourer c'est faire des enfants et les élever. Problème : un peu partout dans le monde, des millions d'enf

**Sections de la fiche jumelle** :

- Concepts enseignés
- 30-mn-gratuites-du-séminaire-savoir-s'entourer-synthese
- Séminaires "Savoir s'entourer" – Affinités électives, groupes et réseaux
- Formations et fiches liées
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance
- 2. La stratégie de survie : s'entourer d'hommes
- 3. Le "sixième sens" féminin
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C121`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 66. Entouré pour réussir (matin)

- **Identifiant** : `C131` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/bien-sentourer-matin`
- **Base thématique** : `bien-sentourer`
- **Taille de la fiche** : 3654 mots (contenu de session absent)

**Formation jumelle** : `C121` — S'entourer pour réussir, ou le secret des affinités électives  
*mode : theme · confiance : 0.67*

**Contenu verbatim disponible** (couche 1) :

> « Chacun veut être autonome, mais en même temps que grandit notre liberté individuelle grandit notre besoin d'être lié aux autres (…) il y a quelques années, seuls le couple, la famille et les amis étaient des lieux d'investissement affectif » ~ JC Kaufmann (le sociologue qui ne m'aime pas)
> Les paradoxes de quiconque cherche à bien s'entourer Dans une société narcissique, on cherche inlassablement son semblable, que l'on ne trouvera jamais puisque tout est conçu pour valoriser notre unicité (« parce que JE le vaux bien« )
> Pour des millions de personnes à travers le monde, savoir bien s'entourer c'est faire des enfants et les élever. Problème : un peu partout dans le monde, des millions d'enf

**Sections de la fiche jumelle** :

- Concepts enseignés
- 30-mn-gratuites-du-séminaire-savoir-s'entourer-synthese
- Séminaires "Savoir s'entourer" – Affinités électives, groupes et réseaux
- Formations et fiches liées
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance
- 2. La stratégie de survie : s'entourer d'hommes
- 3. Le "sixième sens" féminin
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C121`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 67. Briser la glace (apres-midi)

- **Identifiant** : `C133` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/briser-la-glace-apres-midi`
- **Base thématique** : `briser-la-glace`
- **Taille de la fiche** : 1427 mots (contenu de session absent)

**Formation jumelle** : `C127` — Briser la glace  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> A ceux qui se demandent à quoi peut bien servi le fait de savoir briser la glace, je répondrais
> « Il serait beaucoup plus important d’apprendre à l’école l’art d’aborder les gens que d’apprendre la trigonométrie » ~ Montherlant
> Ceci va être l’annonce de séminaire la plus simple à rédiger. De tous les temps.
> Short story
> Durant la journée, je vous dirai, expliquerai, décortiquerai tout ce que j’ai compris, une vie durant, sur l’art de briser la glace avec les gens. Les femmes ET les hommes.
> Voilà.
> Vous pouvez cliquer sur ajouter au panier et grouper vos commandes pour bénéficier d’une réduction. Voir cette publication sur Instagram Une publication partagée par @cyril.meme Sinon, pour ceux qui 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-LfkvDekiWus-synthese
- Le concept de barbare
- La normalisation du vin (Americanisation)
- Émettre-une-critique-constructive-synthese
- L'ennemi-public-n°1-a-un-nouveau-portrait-robot-synthese
- Le harcèlement de rue : un problème réel mais à nuancer
- L'argumentation de Marguerite Stern
- Critique de l'excuse "Réseaux sociaux = fin de la drague"
- Signaux de disponibilité féminine

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C127`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 68. Briser la glace (matin)

- **Identifiant** : `C134` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/briser-la-glace-matin`
- **Base thématique** : `briser-la-glace`
- **Taille de la fiche** : 1325 mots (contenu de session absent)

**Formation jumelle** : `C127` — Briser la glace  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> A ceux qui se demandent à quoi peut bien servi le fait de savoir briser la glace, je répondrais
> « Il serait beaucoup plus important d’apprendre à l’école l’art d’aborder les gens que d’apprendre la trigonométrie » ~ Montherlant
> Ceci va être l’annonce de séminaire la plus simple à rédiger. De tous les temps.
> Short story
> Durant la journée, je vous dirai, expliquerai, décortiquerai tout ce que j’ai compris, une vie durant, sur l’art de briser la glace avec les gens. Les femmes ET les hommes.
> Voilà.
> Vous pouvez cliquer sur ajouter au panier et grouper vos commandes pour bénéficier d’une réduction. Voir cette publication sur Instagram Une publication partagée par @cyril.meme Sinon, pour ceux qui 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-LfkvDekiWus-synthese
- Le concept de barbare
- La normalisation du vin (Americanisation)
- Émettre-une-critique-constructive-synthese
- L'ennemi-public-n°1-a-un-nouveau-portrait-robot-synthese
- Le harcèlement de rue : un problème réel mais à nuancer
- L'argumentation de Marguerite Stern
- Critique de l'excuse "Réseaux sociaux = fin de la drague"
- Signaux de disponibilité féminine

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C127`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 69. Ce que vos parents auraient du vous apprendre (apres-midi)

- **Identifiant** : `C135` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/ce-que-vos-parents-auraient-du-vous-apprendre-apres-midi`
- **Base thématique** : `ce-que-vos-parents-auraient-du-vous-apprendre`
- **Taille de la fiche** : 3283 mots (contenu de session absent)

**Formation jumelle** : `C139` — Ce que vos parents auraient dû vous apprendre  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Rien. Non, rien de rien. Ce séminaire n’a rien de commun avec les séminaires habituels, dont vous avez été plusieurs milliers à travers les années à reconnaître la qualité et la pertinence en matière de relations hommes-femmes, mais aussi de cette relation à vous-même qu'il est convenu d'appeler développement personnel.
> Vous le savez, le bagage parental et scolaire détermine grandement vos trajectoires, que ce soit sociale, professionnelle ou affective. C'est un fait. En clair, c'est de la combinaison « maman-papa-école » que naissent beaucoup de croyances limitantes, de peurs de l'inconnu, de rationalisations, bref, de bornes que vous mettez à votre destin. Voir cette publication sur Instag

**Concepts enseignés** :

La Métonymie et la Préterition · Le Gage Inutile (Trigger Warning) · La Pseudo-Diversité qui Uniformise · La Trinité Patriarcale Universelle

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-HjrJlmCJT3Y-synthese
- Formations et fiches liées
- Confiné,-il-rédige-une-ode-à-la-beauté-féminine-➡️-devinez-qui-l'agresse-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- The-Circus-of-A-Gendered-Children-on-TV-synthese
- Citation marquant
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C139`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 70. Ce que vos parents auraient du vous apprendre (matin)

- **Identifiant** : `C136` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/ce-que-vos-parents-auraient-du-vous-apprendre-matin`
- **Base thématique** : `ce-que-vos-parents-auraient-du-vous-apprendre`
- **Taille de la fiche** : 2683 mots (contenu de session absent)

**Formation jumelle** : `C139` — Ce que vos parents auraient dû vous apprendre  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Rien. Non, rien de rien. Ce séminaire n’a rien de commun avec les séminaires habituels, dont vous avez été plusieurs milliers à travers les années à reconnaître la qualité et la pertinence en matière de relations hommes-femmes, mais aussi de cette relation à vous-même qu'il est convenu d'appeler développement personnel.
> Vous le savez, le bagage parental et scolaire détermine grandement vos trajectoires, que ce soit sociale, professionnelle ou affective. C'est un fait. En clair, c'est de la combinaison « maman-papa-école » que naissent beaucoup de croyances limitantes, de peurs de l'inconnu, de rationalisations, bref, de bornes que vous mettez à votre destin. Voir cette publication sur Instag

**Concepts enseignés** :

La Métonymie et la Préterition · Le Gage Inutile (Trigger Warning) · La Pseudo-Diversité qui Uniformise · La Trinité Patriarcale Universelle

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-HjrJlmCJT3Y-synthese
- Formations et fiches liées
- Confiné,-il-rédige-une-ode-à-la-beauté-féminine-➡️-devinez-qui-l'agresse-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- The-Circus-of-A-Gendered-Children-on-TV-synthese
- Citation marquant
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C139`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 71. Développement personnel, 1: Decupler sa CREATIVITE (après midi)

- **Identifiant** : `C140` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/developpement-personnel-1-decupler-sa-creativite-apres-midi`
- **Base thématique** : `developpement-personnel-1-decupler-sa-creativite`
- **Taille de la fiche** : 2230 mots (contenu de session absent)

**Formation jumelle** : `C240` — Développement personnel 1 : décupler sa créativité  
*mode : base-URL · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « La créativité n'est pas un talent réservé aux artistes — c'est une compétence que tout homme peut développer. » — `C240`
- « La peur du jugement est le premier tueur de créativité — il faut apprendre à proposer sans se juger. » — `C240`
- « Les contraintes boostent la créativité — le budget limité et la deadline serrée vous forcent à innover. » — `C240`

**Sections de la fiche jumelle** :

- Concepts enseignés
- La créativité comme compétence
- La pensée divergente vs convergente
- Les contraintes comme stimulateur
- La curiosité comme moteur
- L'échec comme processus
- La peur du jugement
- Vaincre-la-peur-synthese
- Je-décompte-les-affabulations-d'Oussama-Ammar...-et-là-surprise-synthese
- Les anecdotes analysées (sur 10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C240`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 72. Développement personnel, 1: Decupler sa CREATIVITE (matin)

- **Identifiant** : `C141` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/developpement-personnel-1-decupler-sa-creativite-matin`
- **Base thématique** : `developpement-personnel-1-decupler-sa-creativite`
- **Taille de la fiche** : 1859 mots (contenu de session absent)

**Formation jumelle** : `C240` — Développement personnel 1 : décupler sa créativité  
*mode : base-URL · confiance : 1.0*

**Citations de l'auteur** (vérifiées mot pour mot dans la fiche jumelle) :

- « La créativité n'est pas un talent réservé aux artistes — c'est une compétence que tout homme peut développer. » — `C240`
- « La peur du jugement est le premier tueur de créativité — il faut apprendre à proposer sans se juger. » — `C240`
- « Les contraintes boostent la créativité — le budget limité et la deadline serrée vous forcent à innover. » — `C240`

**Sections de la fiche jumelle** :

- Concepts enseignés
- La créativité comme compétence
- La pensée divergente vs convergente
- Les contraintes comme stimulateur
- La curiosité comme moteur
- L'échec comme processus
- La peur du jugement
- Vaincre-la-peur-synthese
- Je-décompte-les-affabulations-d'Oussama-Ammar...-et-là-surprise-synthese
- Les anecdotes analysées (sur 10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C240`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 73. Développement personnel, 2: Tenacite: apprendre a ne RIEN LACHER

- **Identifiant** : `C142` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/developpement-personnel-2-tenacite-apprendre-a-ne-rien-lacher-matin`
- **Base thématique** : `developpement-personnel-2-tenacite-apprendre-a-ne-rien-lacher`
- **Taille de la fiche** : 849 mots (contenu de session absent)

**Formation jumelle** : `C163` — Développement personnel, 2 : ON – NE – LÂCHE – RIEN  
*mode : theme · confiance : 0.5*

**Contenu verbatim disponible** (couche 1) :

> Objectif du séminaire
> « Le vent se lève; il faut tenter de vivre » – Paul Valéry
> Vous l'avez sans doute remarqué (et dans le cas contraire, ouvrez les journaux et intéressez-vous à l'actualité), les temps sont durs, très durs, et l'avenir ne s'annonce pas vraiment rose. Ni politiquement, ni économiquement, ni rien. Non, vraiment pas. Ça, c'est pour l'échelle macro. Le sérieux.
> « Décidément les temps – comme les oeufs – sont durs. Et la bêtise n'a pas de limite » ~ Ken
> À l'échelle micro (le frivole), ben ce n'est guère plus réjouissant. Notre situation économique personnelle est instable, nos conditions de logement se détériorent, il est de plus en plus difficile de rencontrer quelqu'un, les 

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-résilience-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C163`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 74. Ebook et audio

- **Identifiant** : `C144` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/ebook-et-audio`
- **Base thématique** : `ebook-et-audio`
- **Taille de la fiche** : 2493 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.0) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Ebook et audio 5.00 10 avis 195€ l’ont déjà le veulent Nous n'avons pas pu confirmer votre inscription. Ton inscription est confirmée. Indisponible actuellement Entre ton adresse email ci-dessous et sois recontacté(e) dès qu'il revient Préviens-moi quand il revient Ajouter à ma wantlist 100% 10 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients L'avis de Stepping up (

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 75. Ebook seul

- **Identifiant** : `C145` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/ebook-seul`
- **Base thématique** : `ebook-seul`
- **Taille de la fiche** : 2027 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.0) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Ebook seul 0 avis 195€ l’ont déjà le veulent Nous n'avons pas pu confirmer votre inscription. Ton inscription est confirmée. Indisponible actuellement Entre ton adresse email ci-dessous et sois recontacté(e) dès qu'il revient Préviens-moi quand il revient Ajouter à ma wantlist 0 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients Description Avis Il n’y a pas encore d’

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 76. Ce qu'il est URGENT d'apprendre à vos (futurs ?) enfants – après-midi

- **Identifiant** : `C146` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/education-parentale-apres-midi`
- **Base thématique** : `education-parentale`
- **Taille de la fiche** : 3330 mots (contenu de session absent)

**Formation jumelle** : `C148` — Ce qu'il est URGENT d'apprendre à vos (futurs ?) enfants  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Avec désormais une belle dizaine d'années de recul, il m'est désormais facile de dégager 3 grandes tendances en ce qui concerne l'écoulement de mes précieux séminaires (faut-il le rappeler, pour la 100ème fois : l'information se trouve dans mes séminaires, les réseaux sociaux ne me servent que de canaux de communication, j'y fais surtout le pitre et rien d'autre, vous laissant, à vous clients payants, la primeur de l'information la plus pertinente et la plus recherchée, bref la gifle de réalisme dont vous ne pouvez plus vous passer. La sociologie dissidente, c'est comme la fessée à l'âge adulte: une fois essayée, difficile de revenir en arrière) 3 types de séminaires certains atteignent des 

**Concepts enseignés** :

La Métonymie et la Préterition · Le Gage Inutile (Trigger Warning) · La Pseudo-Diversité qui Uniformise · La Trinité Patriarcale Universelle

**Sections de la fiche jumelle** :

- Concepts enseignés
- Confiné,-il-rédige-une-ode-à-la-beauté-féminine-➡️-devinez-qui-l'agresse-synthese
- Il-s’est-stérilisé.-A-priori,-ça-n’était-pas-urgent-synthese
- Video-HjrJlmCJT3Y-synthese
- Formations et fiches liées
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C148`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 77. Ce qu'il est URGENT d'apprendre à vos (futurs ?) enfants – matin

- **Identifiant** : `C147` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/education-parentale-matin`
- **Base thématique** : `education-parentale`
- **Taille de la fiche** : 2707 mots (contenu de session absent)

**Formation jumelle** : `C148` — Ce qu'il est URGENT d'apprendre à vos (futurs ?) enfants  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Avec désormais une belle dizaine d'années de recul, il m'est désormais facile de dégager 3 grandes tendances en ce qui concerne l'écoulement de mes précieux séminaires (faut-il le rappeler, pour la 100ème fois : l'information se trouve dans mes séminaires, les réseaux sociaux ne me servent que de canaux de communication, j'y fais surtout le pitre et rien d'autre, vous laissant, à vous clients payants, la primeur de l'information la plus pertinente et la plus recherchée, bref la gifle de réalisme dont vous ne pouvez plus vous passer. La sociologie dissidente, c'est comme la fessée à l'âge adulte: une fois essayée, difficile de revenir en arrière) 3 types de séminaires certains atteignent des 

**Concepts enseignés** :

La Métonymie et la Préterition · Le Gage Inutile (Trigger Warning) · La Pseudo-Diversité qui Uniformise · La Trinité Patriarcale Universelle

**Sections de la fiche jumelle** :

- Concepts enseignés
- Confiné,-il-rédige-une-ode-à-la-beauté-féminine-➡️-devinez-qui-l'agresse-synthese
- Il-s’est-stérilisé.-A-priori,-ça-n’était-pas-urgent-synthese
- Video-HjrJlmCJT3Y-synthese
- Formations et fiches liées
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C148`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 78. Get a life (apres-midi)

- **Identifiant** : `C151` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/get-a-life-apres-midi`
- **Base thématique** : `get-a-life`
- **Taille de la fiche** : 3632 mots (contenu de session absent)

**Formation jumelle** : `C137` — Get a life  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> A la manière de nos séminaires best-seller Être sexué 1 et Être sexué 2, dont le premier vous montre tout l’horizon des possibles et vous pousse à tous les dépasser, et dont le second décline les concepts du premier mais dans les contraintes du réel, Get a life est le meilleur moyen de : casser l’emprise que les habitudes ont pris sur vous
> sortir de votre zone de confort
> vous faire un cercle social de qualité
> remettre votre vie en mouvement
> redécouvrir le goût de faire des activités avec une personne qui vous plaît vraiment changer de job / ville / vie
> vivre ses rêves avant la retraite Bref, Get a life sera une gigantesque journée « coup de pied au c.. » pour tous ceux qui éprouvent la sensa

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- Drag-queens-VS-maternelle-la-vérité-sortira-t-elle-de-la-bouche-de-ces-enfants-synthese
- Thèmes principaux
- Théorie des barbares
- Durée estimée
- Formations et fiches liées
- Elle-voulait-le-confort,-elle-a-eu-l'ennui-synthese
- The-Circus-of-A-Gendered-Children-on-TV-synthese
- Citation marquant
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C137`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 79. Get a life (matin)

- **Identifiant** : `C152` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/get-a-life-matin-2`
- **Base thématique** : `get-a-life-matin`
- **Taille de la fiche** : 3793 mots (contenu de session absent)

**Formation jumelle** : `C137` — Get a life  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> A la manière de nos séminaires best-seller Être sexué 1 et Être sexué 2, dont le premier vous montre tout l’horizon des possibles et vous pousse à tous les dépasser, et dont le second décline les concepts du premier mais dans les contraintes du réel, Get a life est le meilleur moyen de : casser l’emprise que les habitudes ont pris sur vous
> sortir de votre zone de confort
> vous faire un cercle social de qualité
> remettre votre vie en mouvement
> redécouvrir le goût de faire des activités avec une personne qui vous plaît vraiment changer de job / ville / vie
> vivre ses rêves avant la retraite Bref, Get a life sera une gigantesque journée « coup de pied au c.. » pour tous ceux qui éprouvent la sensa

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- Drag-queens-VS-maternelle-la-vérité-sortira-t-elle-de-la-bouche-de-ces-enfants-synthese
- Thèmes principaux
- Théorie des barbares
- Durée estimée
- Formations et fiches liées
- Elle-voulait-le-confort,-elle-a-eu-l'ennui-synthese
- The-Circus-of-A-Gendered-Children-on-TV-synthese
- Citation marquant
- Conclusion

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C137`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 80. La peur (apres-midi) La supporter, l affronter, la vaincre

- **Identifiant** : `C155` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/la-peur-apres-midila-supporter-l-affronter-la-vaincre`
- **Base thématique** : `la-peur-apres-midila-supporter-l-affronter-la-vaincre`
- **Taille de la fiche** : 2961 mots (contenu de session absent)

**Formation jumelle** : `C184` — La peur : La supporter, l'affronter, la vaincre  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> L’anecdote du mois
> Contrairement à ce que propage la fémininisation depuis 30 ans avec ses « c’est beau un homme qui pleure », je vous déconseille sérieusement de prendre au mot cette idée reçue, au risque de passer pour une belle fiotte. Je le sais, je l’ai fait.
> Bon, j’avais mes raisons (j’étais très, très déçu de quelque chose ou plutôt de quelqu’un) mais n’empêche, j’ai été très con. Je m’en suis vertement voulu, mais de tout échec il faut tirer leçon, et c’est ce que j’ai fait.
> FLASHBACK : LA PEUR EST LA NORME DE L’ENFANT
> Quand on était enfant – même l’enfant de deux parents normaux qui vous nourrissent, vous chérissent, vous protègent et vous aiment, on avait souvent peur.
> Peur de l’ex

**Sections de la fiche jumelle** :

- Concepts enseignés
- Vaincre-la-peur-synthese
- Cultive-ta-confiance-en-toi-synthese
- The-Circus-of-A-Gendered-Children-on-TV-synthese
- Citation marquant
- Conclusion
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- Pré-requis
- Public visé
- Niveau

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C184`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 81. La peur (matin) La supporter, l affronter, la vaincre

- **Identifiant** : `C156` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/la-peur-matinla-supporter-l-affronter-la-vaincre`
- **Base thématique** : `la-peur-matinla-supporter-l-affronter-la-vaincre`
- **Taille de la fiche** : 2961 mots (contenu de session absent)

**Formation jumelle** : `C184` — La peur : La supporter, l'affronter, la vaincre  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> L’anecdote du mois
> Contrairement à ce que propage la fémininisation depuis 30 ans avec ses « c’est beau un homme qui pleure », je vous déconseille sérieusement de prendre au mot cette idée reçue, au risque de passer pour une belle fiotte. Je le sais, je l’ai fait.
> Bon, j’avais mes raisons (j’étais très, très déçu de quelque chose ou plutôt de quelqu’un) mais n’empêche, j’ai été très con. Je m’en suis vertement voulu, mais de tout échec il faut tirer leçon, et c’est ce que j’ai fait.
> FLASHBACK : LA PEUR EST LA NORME DE L’ENFANT
> Quand on était enfant – même l’enfant de deux parents normaux qui vous nourrissent, vous chérissent, vous protègent et vous aiment, on avait souvent peur.
> Peur de l’ex

**Sections de la fiche jumelle** :

- Concepts enseignés
- Vaincre-la-peur-synthese
- Cultive-ta-confiance-en-toi-synthese
- The-Circus-of-A-Gendered-Children-on-TV-synthese
- Citation marquant
- Conclusion
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- Pré-requis
- Public visé
- Niveau

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C184`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 82. Briller en ligne (après-midi)

- **Identifiant** : `C158` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/messages-drague-apres-midi`
- **Base thématique** : `messages-drague`
- **Taille de la fiche** : 3271 mots (contenu de session absent)

**Formation jumelle** : `C183` — Briller en ligne, le charme discret du texto parfait ?  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> 221 par jour
> Le nombre de fois où vous consultez votre smartphone (source). À multiplier par 2 si vous êtes une femme. Et par 4 si vous avez moins de 25 ans.
> Alors sachant que la requête n°1 à son appareil est de prendre / recevoir des nouvelles de son cercle d'amis, selon vous cette statistique : a) influe sur les stratégies relationnelles (personnelles, amoureuses et professionnelles)
> b) « je sais pas, j'en m'en fous, je suis un hétéro binaire de base, j'aime pas le téléphone et tout ce qui y est associé, j'ai un forfait 5 minutes par mois 2 sms, et je ne le termine jamais« Vous avez répondu a) =&gt; lisez la suite
> vous avez répondu b) =&gt; vous avez un problème. Ce problème, c'est que le

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-20Qx2jb_xZU-synthese
- 1. TF1 et le journalisme de complaisance
- 2. La MILF de TF1
- 3. Le mouvement masculiniste vient des USA années 70
- 4. Andrew Tate comme épouvantail
- 5. La violence vient d'où ?
- 6. Les salles de MMA
- Tu-me-manques-synthese
- Serais-tu-un-harceleur-aux-USA-12-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C183`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 83. Briller en ligne (matin)

- **Identifiant** : `C159` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/messages-drague-matin`
- **Base thématique** : `messages-drague`
- **Taille de la fiche** : 1455 mots (contenu de session absent)

**Formation jumelle** : `C183` — Briller en ligne, le charme discret du texto parfait ?  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> 221 par jour
> Le nombre de fois où vous consultez votre smartphone (source). À multiplier par 2 si vous êtes une femme. Et par 4 si vous avez moins de 25 ans.
> Alors sachant que la requête n°1 à son appareil est de prendre / recevoir des nouvelles de son cercle d'amis, selon vous cette statistique : a) influe sur les stratégies relationnelles (personnelles, amoureuses et professionnelles)
> b) « je sais pas, j'en m'en fous, je suis un hétéro binaire de base, j'aime pas le téléphone et tout ce qui y est associé, j'ai un forfait 5 minutes par mois 2 sms, et je ne le termine jamais« Vous avez répondu a) =&gt; lisez la suite
> vous avez répondu b) =&gt; vous avez un problème. Ce problème, c'est que le

**Sections de la fiche jumelle** :

- Concepts enseignés
- Video-20Qx2jb_xZU-synthese
- 1. TF1 et le journalisme de complaisance
- 2. La MILF de TF1
- 3. Le mouvement masculiniste vient des USA années 70
- 4. Andrew Tate comme épouvantail
- 5. La violence vient d'où ?
- 6. Les salles de MMA
- Tu-me-manques-synthese
- Serais-tu-un-harceleur-aux-USA-12-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C183`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 84. Se construire une garde robe complete (apres-midi)

- **Identifiant** : `C164` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/se-construire-une-garde-robe-complete-apres-midietape-par-etape`
- **Base thématique** : `se-construire-une-garde-robe-complete-apres-midietape-par-etape`
- **Taille de la fiche** : 1438 mots (contenu de session absent)

**Formation jumelle** : `C138` — Se construire une garde-robe complete  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Il fut un temps où j’écrivais sur un site de mode masculine voisin (si si), un article dont certains d’entre vous me reparlent encore aujourd’hui. Il s’agissait, en version simplissime, du « juste prix » à mettre dans chaque type de vêtements.
> Alors d’emblée, si une fille tombe sur ces lignes, elle n’y verra guère de sens. Avec 1000 €, elle a 15 chemisiers, 10 robes, 5 jeans, 5 paires de chaussures, et 50 accessoires…
> Avec la même somme, un homme a 1 manteau, 1 jean et des chaussures !
> J’exagère un peu, mais pas tant que ça… Vous voyez l’idée.
> POURQUOI UN SÉMINAIRE SUR LA GARDE-ROBE ?
> Pensez à tous les experts de l’habillement que vous pouvez imaginer / croiser / voir. Sur le net ou ailleurs

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- We-must-save-the-children-#Pélissard-synthese
- Contexte
- Analyse critique
- Le "loopen prolétariat"
- Conséquences pour les enfants
- Réponse de l'entourage
- Sans-conteste-LE-couple-progressiste-le-+-inattendu-de-2023-synthese
- Le couple progressiste inattendu : Marraine & James
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C138`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 85. Se construire une garde robe complete (matin)

- **Identifiant** : `C165` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/se-construire-une-garde-robe-complete-matinetape-par-etape`
- **Base thématique** : `se-construire-une-garde-robe-complete-matinetape-par-etape`
- **Taille de la fiche** : 1438 mots (contenu de session absent)

**Formation jumelle** : `C138` — Se construire une garde-robe complete  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Il fut un temps où j’écrivais sur un site de mode masculine voisin (si si), un article dont certains d’entre vous me reparlent encore aujourd’hui. Il s’agissait, en version simplissime, du « juste prix » à mettre dans chaque type de vêtements.
> Alors d’emblée, si une fille tombe sur ces lignes, elle n’y verra guère de sens. Avec 1000 €, elle a 15 chemisiers, 10 robes, 5 jeans, 5 paires de chaussures, et 50 accessoires…
> Avec la même somme, un homme a 1 manteau, 1 jean et des chaussures !
> J’exagère un peu, mais pas tant que ça… Vous voyez l’idée.
> POURQUOI UN SÉMINAIRE SUR LA GARDE-ROBE ?
> Pensez à tous les experts de l’habillement que vous pouvez imaginer / croiser / voir. Sur le net ou ailleurs

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- We-must-save-the-children-#Pélissard-synthese
- Contexte
- Analyse critique
- Le "loopen prolétariat"
- Conséquences pour les enfants
- Réponse de l'entourage
- Sans-conteste-LE-couple-progressiste-le-+-inattendu-de-2023-synthese
- Le couple progressiste inattendu : Marraine & James
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C138`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 86. Se reconstruire apres une blessure (ce qui ne te tue pas te rend plus fort) (apres-midi)

- **Identifiant** : `C168` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/se-reconstruire-apres-une-blessure-ce-qui-ne-te-tue-pas-te-rend-plus-fort-apres-midi`
- **Base thématique** : `se-reconstruire-apres-une-blessure-ce-qui-ne-te-tue-pas-te-rend-plus-fort`
- **Taille de la fiche** : 3321 mots (contenu de session absent)

**Formation jumelle** : `C170` — Se reconstruire apres une blessure (ce qui ne te tue pas te rend plus fort)  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> « Il n’y a pas que les croyances qui sont limitantes, il y a les blessures, aussi » – Stéphane
> S’il y a bien un sujet que les sites de développement personnel n’ont jamais abordé…
> … c’est celui des blessures et des traumatismes du passé disparition (ou abdication) d’un parent pendant l’enfance,
> échec personnel ou professionnel (qu’il soit avéré ou pas, peu importe, l’importance étant le ressenti : savoir qu’il y a « toujours pire ailleurs » n’a jamais aidé personne à se sentir mieux),
> rejet violent d’une personne que l’on convoitait (suivi éventuellement d’une obsession amoureuse),
> séparation douloureuse avec une personne que l’on a beaucoup aimé, qu’on ne parvient pas à oublier, et dont on 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Cultive-ta-confiance-en-toi-synthese
- #Zemmour2022,-ep.1-the-case-of-the-stolen-kiss-synthese
- Analyse du témoignage
- Comparaison Orwellienne
- Hypocrisie politique
- Vaincre-la-peur-synthese
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C170`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 87. Se reconstruire apres une blessure (ce qui ne te tue pas te rend plus fort) (matin)

- **Identifiant** : `C169` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/se-reconstruire-apres-une-blessure-ce-qui-ne-te-tue-pas-te-rend-plus-fort-matin`
- **Base thématique** : `se-reconstruire-apres-une-blessure-ce-qui-ne-te-tue-pas-te-rend-plus-fort`
- **Taille de la fiche** : 3311 mots (contenu de session absent)

**Formation jumelle** : `C170` — Se reconstruire apres une blessure (ce qui ne te tue pas te rend plus fort)  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> « Il n’y a pas que les croyances qui sont limitantes, il y a les blessures, aussi » – Stéphane
> S’il y a bien un sujet que les sites de développement personnel n’ont jamais abordé…
> … c’est celui des blessures et des traumatismes du passé disparition (ou abdication) d’un parent pendant l’enfance,
> échec personnel ou professionnel (qu’il soit avéré ou pas, peu importe, l’importance étant le ressenti : savoir qu’il y a « toujours pire ailleurs » n’a jamais aidé personne à se sentir mieux),
> rejet violent d’une personne que l’on convoitait (suivi éventuellement d’une obsession amoureuse),
> séparation douloureuse avec une personne que l’on a beaucoup aimé, qu’on ne parvient pas à oublier, et dont on 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Cultive-ta-confiance-en-toi-synthese
- #Zemmour2022,-ep.1-the-case-of-the-stolen-kiss-synthese
- Analyse du témoignage
- Comparaison Orwellienne
- Hypocrisie politique
- Vaincre-la-peur-synthese
- Développe-ta-force-mentale-et-prépare-toi-aux-combats-de-la-vie-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C170`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 88. Simplifiez-vous la vie ! (webinaire court et impactant, 2h « seulement »)

- **Identifiant** : `C171` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/se-simplifier-la-vie-webinar`
- **Base thématique** : `se-simplifier-la-vie-webinar`
- **Taille de la fiche** : 2890 mots (contenu de session absent)

**Formation jumelle** : `C349` — Simplifiez-vous la vie ! (webinaire court et impactant, 2h « seulement »)  
*mode : base-URL · confiance : 1.0*

**Sections de la fiche jumelle** :

- Concepts enseignés
- Pourquoi la simplification est difficile
- Les 4 domaines de simplification
- Le cadre de décision « Oui, Non, ou Hell Yeah »
- La simplification comme philosophie de pouvoir
- Le-bonheur-7-techniques-pour-être-heureux-et-surfer-la-vie-synthese
- Vaincre-la-peur-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C349`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 89. Secret agenda (apres-midi)

- **Identifiant** : `C172` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/secret-agenda-apres-midi-2`
- **Base thématique** : `secret-agenda-apres-midi`
- **Taille de la fiche** : 2895 mots (contenu de session absent)

**Formation jumelle** : `C174` — Agenda secret / feuille de route  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> D’après mes statistiques internes, la problématique la plus souvent abordée sur le forum ces derniers mois… le secret agenda (plan de vie, ou encore feuille de route). Hasard ? Bien sûr que non.
> Rappel : Ca n’est pas contre vous, mais une femme est physiologiquement concue pour « graver dans le marbre » une hiérarchie de priorités , même si elle ne s’en rend pas compte. Et si elle s’en rend compte, elle ne vous le dira pas. Il n’y a pas (forcément) méchanceté ou manipulation, juste de la psychologie. »
> Exemples de ces décisions/priorités Combien d’enfants elle aura,
> A quel âge,
> Avec qui (typologie d’homme),
> Où elle vivra (ville/pays, appartement/maison),
> Comment elle subsistera (salariat, en

**Sections de la fiche jumelle** :

- Concepts enseignés
- Garde-alternée-et-coup-de-boule-qui-ment-dans-ce-tribunal-synthese
- Elle-accepte-TOUS-ses-rencards-#tinder-regardez-la-se-transformer-en-temps-réel-synthese
- Formations et fiches liées
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- J'ai-rencontré-les-fameux-0,001%-synthese
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C174`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 90. Secret agenda (matin)

- **Identifiant** : `C173` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/secret-agenda-matin-2`
- **Base thématique** : `secret-agenda-matin`
- **Taille de la fiche** : 3113 mots (contenu de session absent)

**Formation jumelle** : `C174` — Agenda secret / feuille de route  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> D’après mes statistiques internes, la problématique la plus souvent abordée sur le forum ces derniers mois… le secret agenda (plan de vie, ou encore feuille de route). Hasard ? Bien sûr que non.
> Rappel : Ca n’est pas contre vous, mais une femme est physiologiquement concue pour « graver dans le marbre » une hiérarchie de priorités , même si elle ne s’en rend pas compte. Et si elle s’en rend compte, elle ne vous le dira pas. Il n’y a pas (forcément) méchanceté ou manipulation, juste de la psychologie. »
> Exemples de ces décisions/priorités Combien d’enfants elle aura,
> A quel âge,
> Avec qui (typologie d’homme),
> Où elle vivra (ville/pays, appartement/maison),
> Comment elle subsistera (salariat, en

**Sections de la fiche jumelle** :

- Concepts enseignés
- Garde-alternée-et-coup-de-boule-qui-ment-dans-ce-tribunal-synthese
- Elle-accepte-TOUS-ses-rencards-#tinder-regardez-la-se-transformer-en-temps-réel-synthese
- Formations et fiches liées
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- J'ai-rencontré-les-fameux-0,001%-synthese
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C174`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 91. Seduire bureau – ecole (apres-midi)

- **Identifiant** : `C175` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/seduire-bureau-ecole-apres-midi`
- **Base thématique** : `seduire-bureau-ecole`
- **Taille de la fiche** : 2877 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.0) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Seduire bureau – ecole (apres-midi) 4.83 6 avis 195€ l’ont déjà le veulent Ajouter au panier Ajouter à ma wantlist 6 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients L'avis de Coelus (client confirmé) Commandé le 23-07-2023  (et téléchargé à  12:09:00) Stephane demolit les idees preconcues concernant la seduction au bureau: pourquoi le dejeuner n’est absolument pas 

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 92. Seduire bureau – ecole (matin)

- **Identifiant** : `C176` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/seduire-bureau-ecole-matin-2`
- **Base thématique** : `seduire-bureau-ecole-matin`
- **Taille de la fiche** : 3404 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.0) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Page produit archivée** (contenu gratuit complémentaire) :

> Seduire bureau – ecole (matin) 4.80 5 avis 195€ l’ont déjà le veulent Ajouter au panier Ajouter à ma wantlist 5 avis clients s’expriment dans ce noble dessin. Lire tous les avis > Avis clients L'avis de Coelus (client confirmé) Commandé le 23-07-2023  (et téléchargé à  12:09:00) Stepahe demolit les idees preconcues concernant la seduction au bureau: pourquoi le dejeuner n’est absolument pas le mei

**Statut** :

- **partiellement couvert par la page produit archivée** — prix, disponibilité, avis
  clients authentifiés et recommandations croisées ; **pas** de doctrine de session
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 93. Signes d'intérêt (après-midi)

- **Identifiant** : `C177` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/signes-interet-apres-midi`
- **Base thématique** : `signes-interet`
- **Taille de la fiche** : 890 mots (contenu de session absent)

**Formation jumelle** : `C179` — Le décodeur ultime de signes d'intérêts !  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Avoue. Une fois. Au moins une (1) fois. Tu te l'es posée, la question : comment savoir si une femme est intéressée (vraiment intéressée).
> Alors tu es parti fouiller sur le web. Et tu en as trouvé, du contenu. Des tonnes de contenus, devrais-je dire. Morcelées, éparpillées, ventilées partout sur des blogs, des pages, des forums. Sans parler des vidéos Youtube ou un type sorti de nulle part, debout devant un tableau blanc, dénué de tout diplôme en sciences humaines, vient t'expliquer la psychologie féminine découverte au cours de ses deux dernières années à draguer sur les boulevards.
> Et si on arrêtait le massacre à l'information sauvage ?
> Souvent, en regardant des tutos youtube sur la psychol

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'embrayage-qui-crie-famine-depuis-des-mois-synthese
- Titre
- Citation
- Conclusion
- Formations et fiches liées
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens
- 3. L'art d'"arracher" vs. cueillir ce qui s'offre

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C179`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 94. Signes d'intérêt (matin)

- **Identifiant** : `C178` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/signes-interet-matin`
- **Base thématique** : `signes-interet`
- **Taille de la fiche** : 890 mots (contenu de session absent)

**Formation jumelle** : `C179` — Le décodeur ultime de signes d'intérêts !  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Avoue. Une fois. Au moins une (1) fois. Tu te l'es posée, la question : comment savoir si une femme est intéressée (vraiment intéressée).
> Alors tu es parti fouiller sur le web. Et tu en as trouvé, du contenu. Des tonnes de contenus, devrais-je dire. Morcelées, éparpillées, ventilées partout sur des blogs, des pages, des forums. Sans parler des vidéos Youtube ou un type sorti de nulle part, debout devant un tableau blanc, dénué de tout diplôme en sciences humaines, vient t'expliquer la psychologie féminine découverte au cours de ses deux dernières années à draguer sur les boulevards.
> Et si on arrêtait le massacre à l'information sauvage ?
> Souvent, en regardant des tutos youtube sur la psychol

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'embrayage-qui-crie-famine-depuis-des-mois-synthese
- Titre
- Citation
- Conclusion
- Formations et fiches liées
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens
- 3. L'art d'"arracher" vs. cueillir ce qui s'offre

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C179`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 95. Small talk (badinage) (apres-midi)

- **Identifiant** : `C180` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/small-talk-badinage-apres-midi`
- **Base thématique** : `small-talk-badinage`
- **Taille de la fiche** : 2171 mots (contenu de session absent)

**Formation jumelle** : `C182` — Small talk (badinage)  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous êtes-vous déjà retrouvé dans la situation suivante (ou analogue) : les gens se parlent comme s’ils se connaissaient depuis toujours, or ils se sont rencontrés il y a à peine 5 minutes. C’est inconcevable pour vous, il vous faut « bien connaître » quelqu’un avant de vous ouvrir à lui.
> vous assistez à une conversation (volontairement ou involontairement), vous en écoutez le contenu, cela vous semble vide, creux, inintéressant, il n’y a pas vraiment d’informations « importantes » échangées, et pourtant les protagonistes semblent y trouver parfaitement leur compte. Ils s’échangent leurs coordonnées avec plaisir et projettent de se revoir. Ils s’embrassent peut-être déjà bouche ouverte
> vous 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Serais-tu-un-harceleur-aux-USA-12-synthese
- 1. Le harcèlement est tyrannique (pas démocratique)
- 2. La règle du "une seule demande"
- 3. La notion de "coupe mentale"
- 4. Le profil du harceleur récurrent
- 5. Les blagues sur l'origine ethnique en contexte professionnel
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C182`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 96. Small talk (badinage) (matin)

- **Identifiant** : `C181` · **Catégorie** : Sedirection Rencontres
- **URL de catalogue** : `mat-consulting.fr/small-talk-badinage-matin`
- **Base thématique** : `small-talk-badinage`
- **Taille de la fiche** : 3493 mots (contenu de session absent)

**Formation jumelle** : `C182` — Small talk (badinage)  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous êtes-vous déjà retrouvé dans la situation suivante (ou analogue) : les gens se parlent comme s’ils se connaissaient depuis toujours, or ils se sont rencontrés il y a à peine 5 minutes. C’est inconcevable pour vous, il vous faut « bien connaître » quelqu’un avant de vous ouvrir à lui.
> vous assistez à une conversation (volontairement ou involontairement), vous en écoutez le contenu, cela vous semble vide, creux, inintéressant, il n’y a pas vraiment d’informations « importantes » échangées, et pourtant les protagonistes semblent y trouver parfaitement leur compte. Ils s’échangent leurs coordonnées avec plaisir et projettent de se revoir. Ils s’embrassent peut-être déjà bouche ouverte
> vous 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Serais-tu-un-harceleur-aux-USA-12-synthese
- 1. Le harcèlement est tyrannique (pas démocratique)
- 2. La règle du "une seule demande"
- 3. La notion de "coupe mentale"
- 4. Le profil du harceleur récurrent
- 5. Les blagues sur l'origine ethnique en contexte professionnel
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C182`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 97. Changez d'image (apres-midi)

- **Identifiant** : `C187` · **Catégorie** : Style Image
- **URL de catalogue** : `mat-consulting.fr/changez-d-image-apres-midi`
- **Base thématique** : `changez-d-image`
- **Taille de la fiche** : 1422 mots (contenu de session absent)

**Formation jumelle** : `C186` — Changez d'image  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Pourquoi si peu de contenus sur l'image dans ce catalogue de formations ? Plusieurs raisons à cela :
> 1. Une raison de hiérarchie
> Comme le montrent dans Paris les groupuscules extrémistes de modeux de ce qu’il est convenu d’appeler la semaine de la mode (fashion week), le rôle du contenant ne doit jamais dépasser celui du contenu.
> Le statut d’homme sexué et intéressant – tel que nous le concevons – s’accompagnant mal de celui d’huître creuse passant tout son temps libre à disserter sur les blogs du mercato des maisons de couture. Bref, la couture, c’est pour les filles.
> 2. Une raison de diversité
> Comme vous le savez probablement si vous suivez le site depuis un certain temps, les séminaires n

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)
- Stratégie 2: Le tango comme porte d'entrée (~6/10)
- Stratégie 3: La carte de visite (~12/20)
- Stratégie 4: Les cadeaux (~14-15/20)
- Stratégie 5: La confrontation directe (~4/10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C186`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 98. Changez d'image (matin)

- **Identifiant** : `C188` · **Catégorie** : Style Image
- **URL de catalogue** : `mat-consulting.fr/changez-d-image-matin-2`
- **Base thématique** : `changez-d-image-matin`
- **Taille de la fiche** : 1376 mots (contenu de session absent)

**Formation jumelle** : `C186` — Changez d'image  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Pourquoi si peu de contenus sur l'image dans ce catalogue de formations ? Plusieurs raisons à cela :
> 1. Une raison de hiérarchie
> Comme le montrent dans Paris les groupuscules extrémistes de modeux de ce qu’il est convenu d’appeler la semaine de la mode (fashion week), le rôle du contenant ne doit jamais dépasser celui du contenu.
> Le statut d’homme sexué et intéressant – tel que nous le concevons – s’accompagnant mal de celui d’huître creuse passant tout son temps libre à disserter sur les blogs du mercato des maisons de couture. Bref, la couture, c’est pour les filles.
> 2. Une raison de diversité
> Comme vous le savez probablement si vous suivez le site depuis un certain temps, les séminaires n

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)
- Stratégie 2: Le tango comme porte d'entrée (~6/10)
- Stratégie 3: La carte de visite (~12/20)
- Stratégie 4: Les cadeaux (~14-15/20)
- Stratégie 5: La confrontation directe (~4/10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C186`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 99. Catalogue des Formations

- **Identifiant** : `C209` · **Catégorie** : Non catégorisé
- **URL** : —
- **Base** : —
- **Taille de la fiche** : 3148 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.0) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 100. Comprendre les gens, 2 (matin)

- **Identifiant** : `C225` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/analyser-gens-matin`
- **Base thématique** : `analyser-gens`
- **Taille de la fiche** : 3398 mots (contenu de session absent)

**Formation jumelle** : `C057` — Comprendre les gens, 2  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Je ne vais pas y aller par quatre chemins : vous vous croyez peut-être très intelligents, mais tant que vous ne saurez pas analyser les gens, vous êtes complètement cons.
> L'oeil intelligent, selon les termes des psychologues de la perception, ne se borne pas à analyser les formes et les mouvements des individus qui sont devant nous. Il devine aussi leur pensées et leurs intentions en remarquant comment ils regardent, approchent, évitent, aident ou empêchent d'agir les autres objets et les autres individus ~ Steven Pinker, comprendre la nature humaine
> Nous sous estimons l'importance de l'intelligence sociale, de l'intelligence émotionnelle, et plus globalement de la faculté à comprendre les g

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'intelligence-relationnelle-1-synthese
- L'intelligence-relationnelle-2-synthese
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese
- 1. Le postulat de départ du livre
- 2. La mère de Stéphane comme témoin
- 3. Ce que l'homme attend vs. ce que la femme fait
- Cultive-ta-confiance-en-toi-synthese
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C057`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 101. Cultivez votre INTELLIGENCE ÉMOTIONNELLE

- **Identifiant** : `C234` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/intelligence-emotionnelle`
- **Base thématique** : `intelligence-emotionnelle`
- **Taille de la fiche** : 2826 mots (contenu de session absent)

**Formation jumelle** : `C070` — Cultivez votre INTELLIGENCE ÉMOTIONNELLE  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Cela fait trente ans qu'on vous bassine avec l'idée que l'intelligence émotionnelle serait « el nuvo QI ». Goleman l'a écrit en 1995, les RH l'ont récupéré sans vergogne (les RH ont rarement de la vergogne), LinkedIn l'a mu en une litanie hebdomadaire, et au bout du compte, personne ou presque n'est plus fichu de dire concrètement de quoi il s'agit, comment savoir si vous en avez, et surtout comment vivre avec. Qu'on en soit doté ou pas. Ce séminaire est ma réponse à ce vide.
> « L'intelligence émotionnelle ? Encore un truc de pleurnichards en quête de validation. Moi je gère, je suis pas une chochotte. »
> Bonne remarque. Fausse, mais bonne.
> 1. D'abord parce que c'est précisément parce que vous

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C070`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 102. Développement personnel, 2 : ON – NE – LÂCHE – RIEN

- **Identifiant** : `C241` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/resilience`
- **Base thématique** : `resilience`
- **Taille de la fiche** : 1965 mots (contenu de session absent)

**Formation jumelle** : `C163` — Développement personnel, 2 : ON – NE – LÂCHE – RIEN  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Objectif du séminaire
> « Le vent se lève; il faut tenter de vivre » – Paul Valéry
> Vous l'avez sans doute remarqué (et dans le cas contraire, ouvrez les journaux et intéressez-vous à l'actualité), les temps sont durs, très durs, et l'avenir ne s'annonce pas vraiment rose. Ni politiquement, ni économiquement, ni rien. Non, vraiment pas. Ça, c'est pour l'échelle macro. Le sérieux.
> « Décidément les temps – comme les oeufs – sont durs. Et la bêtise n'a pas de limite » ~ Ken
> À l'échelle micro (le frivole), ben ce n'est guère plus réjouissant. Notre situation économique personnelle est instable, nos conditions de logement se détériorent, il est de plus en plus difficile de rencontrer quelqu'un, les 

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-résilience-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C163`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 103. Développement personnel, 2: Tenacite: apprendre a ne RIEN LACHER

- **Identifiant** : `C242` · **Catégorie** : Développement Personnel
- **URL de catalogue** : `mat-consulting.fr/developpement-personnel-2-tenacite-apprendre-a-ne-rien-lacher-matin`
- **Base thématique** : `developpement-personnel-2-tenacite-apprendre-a-ne-rien-lacher`
- **Taille de la fiche** : 1371 mots (contenu de session absent)

**Formation jumelle** : `C163` — Développement personnel, 2 : ON – NE – LÂCHE – RIEN  
*mode : theme · confiance : 0.5*

**Contenu verbatim disponible** (couche 1) :

> Objectif du séminaire
> « Le vent se lève; il faut tenter de vivre » – Paul Valéry
> Vous l'avez sans doute remarqué (et dans le cas contraire, ouvrez les journaux et intéressez-vous à l'actualité), les temps sont durs, très durs, et l'avenir ne s'annonce pas vraiment rose. Ni politiquement, ni économiquement, ni rien. Non, vraiment pas. Ça, c'est pour l'échelle macro. Le sérieux.
> « Décidément les temps – comme les oeufs – sont durs. Et la bêtise n'a pas de limite » ~ Ken
> À l'échelle micro (le frivole), ben ce n'est guère plus réjouissant. Notre situation économique personnelle est instable, nos conditions de logement se détériorent, il est de plus en plus difficile de rencontrer quelqu'un, les 

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-résilience-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C163`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 104. Discernement – matin

- **Identifiant** : `C246` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/discernement-matin`
- **Base thématique** : `discernement`
- **Taille de la fiche** : 1375 mots (contenu de session absent)

**Formation jumelle** : `C069` — Survivre aux mensonges du nouveau monde (le discernement)  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Malheureusement nous manquons de discernement et d'indépendance dans nos choix ; nous ne distinguons pas entre l'idole de la veille, devenue méprisable aujourd'hui, et celle qui mérite tous nos sacrifices ~ Astolphe de Custine (1790-1857)
> On ne meurt pas impunément le soir de l'anniversaire des gens. Je l'ai découvert à l'occasion de la disparition de celui qui m'aura appris – sinon « tout » – du moins à respirer, à écouter et à m'exprimer ; ce qui, vous en conviendrez, n'est pas quantité négligeable dans une vie en communauté (non, ça n'est pas Pierre Bénichou). Tintin est pénible pic.twitter.com/gO5rcW2djG
> — Tweetinão (@tintinades) March 13, 2024 L'échelle des vertus Qu'y a t-il au-dessus 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- L'intelligence-relationnelle-1-synthese
- Combien-de-fois-A.Buzyn-a-t-elle-menti-à-la-commission-d'enquête-synthese
- Méthodologie
- Score de mentir
- Points critiques relevés
- Citation du Professeur Raoult
- Video-py5soTfXpxQ-synthese
- Un-monde-sans-hommes-cette-nouvelle-lubie-des-séries-cache-un-projet-eugéniste-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C069`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 105. DOUBLE ton RÉSEAU

- **Identifiant** : `C247` · **Catégorie** : Carrière & Leadership
- **URL de catalogue** : `mat-consulting.fr/vie-sociale`
- **Base thématique** : `vie-sociale`
- **Taille de la fiche** : 1625 mots (contenu de session absent)

**Formation jumelle** : `C123` — DOUBLE ton RÉSEAU  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Ta-dam, 10 conseils merdiques tirés du web pour développer son réseau : distribuez des cartes de visite
> prenez des cartes de visite
> scannez les cartes de visite qu'on te donne sur ton ordi
> publiez du contenu intéressant sur Linkedin
> il est plus facile qu'avant de se créer un bon réseau (NDLR : ah bon ?)
> écrivez à votre réseau toutes les X semaines/tous les Y mois (très naturel, l'autre va pas du tout le voir venir)
> allez rencontrer des professionnels de votre secteur au pôle emploi, à l'APEC, l'APECITA, au centre de documentation, à la chambre d'agriculture, celle des métiers, dans les sociétés d'intérim… (sos amitié bonsoir)
> lu sur Elle.fr : « votre voisine du 5ème ou le père du meilleur am

**Sections de la fiche jumelle** :

- Concepts enseignés
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)
- Stratégie 2: Le tango comme porte d'entrée (~6/10)
- Stratégie 3: La carte de visite (~12/20)
- Stratégie 4: Les cadeaux (~14-15/20)
- Stratégie 5: La confrontation directe (~4/10)
- Video-2886bTU-5Yk-synthese
- 1. Konbini et le format épileptique
- 2. "Combat d'arrière-garde"

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C123`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 106. Entouré pour réussir (matin)

- **Identifiant** : `C251` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/bien-sentourer-matin`
- **Base thématique** : `bien-sentourer`
- **Taille de la fiche** : 2686 mots (contenu de session absent)

**Formation jumelle** : `C121` — S'entourer pour réussir, ou le secret des affinités électives  
*mode : theme · confiance : 0.67*

**Contenu verbatim disponible** (couche 1) :

> « Chacun veut être autonome, mais en même temps que grandit notre liberté individuelle grandit notre besoin d'être lié aux autres (…) il y a quelques années, seuls le couple, la famille et les amis étaient des lieux d'investissement affectif » ~ JC Kaufmann (le sociologue qui ne m'aime pas)
> Les paradoxes de quiconque cherche à bien s'entourer Dans une société narcissique, on cherche inlassablement son semblable, que l'on ne trouvera jamais puisque tout est conçu pour valoriser notre unicité (« parce que JE le vaux bien« )
> Pour des millions de personnes à travers le monde, savoir bien s'entourer c'est faire des enfants et les élever. Problème : un peu partout dans le monde, des millions d'enf

**Sections de la fiche jumelle** :

- Concepts enseignés
- 30-mn-gratuites-du-séminaire-savoir-s'entourer-synthese
- Séminaires "Savoir s'entourer" – Affinités électives, groupes et réseaux
- Formations et fiches liées
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance
- 2. La stratégie de survie : s'entourer d'hommes
- 3. Le "sixième sens" féminin
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C121`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 107. Intelligence relationnelle, 1: Doubler son RESEAU (matin)

- **Identifiant** : `C260` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/intelligence-relationnelle-1-doubler-son-reseau-matin`
- **Base thématique** : `intelligence-relationnelle-1-doubler-son-reseau`
- **Taille de la fiche** : 2549 mots (contenu de session absent)

**Formation jumelle** : `C071` — Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)  
*mode : theme · confiance : 0.5*

**Sections de la fiche jumelle** :

- Concepts enseignés
- The-brilliant-idea-from-the-creators-of-#Metoo-to-save-the-movement-synthese
- Video-p1WU4JiuIzQ-synthese
- L'intelligence-relationnelle-2-synthese
- Video-tiDHbY0rQKQ-synthese
- L'intelligence-relationnelle-1-synthese
- Video-x2zvDhh2yu4-synthese
- This-case-would-be-front-page-news-if-only-the-murderer-were-a-man,-but...-🤫-synthese
- This-government-campaign-was-so-successful-that-you've-(probably)-never-seen-it.-synthese
- Fiche transcrite par Bartilabas

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C071`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 108. Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)

- **Identifiant** : `C261` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/intelligence-relationnelle-2-les-secrets-du-pouvoir-apres-midi`
- **Base thématique** : `intelligence-relationnelle-2-les-secrets-du-pouvoir`
- **Taille de la fiche** : 1238 mots (contenu de session absent)

**Formation jumelle** : `C071` — Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)  
*mode : base-URL · confiance : 1.0*

**Sections de la fiche jumelle** :

- Concepts enseignés
- The-brilliant-idea-from-the-creators-of-#Metoo-to-save-the-movement-synthese
- Video-p1WU4JiuIzQ-synthese
- L'intelligence-relationnelle-2-synthese
- Video-tiDHbY0rQKQ-synthese
- L'intelligence-relationnelle-1-synthese
- Video-x2zvDhh2yu4-synthese
- This-case-would-be-front-page-news-if-only-the-murderer-were-a-man,-but...-🤫-synthese
- This-government-campaign-was-so-successful-that-you've-(probably)-never-seen-it.-synthese
- Fiche transcrite par Bartilabas

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C071`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 109. Intelligence relationnelle, 2: Les secrets du POUVOIR (matin)

- **Identifiant** : `C262` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/intelligence-relationnelle-2-les-secrets-du-pouvoir-matin`
- **Base thématique** : `intelligence-relationnelle-2-les-secrets-du-pouvoir`
- **Taille de la fiche** : 1243 mots (contenu de session absent)

**Formation jumelle** : `C071` — Intelligence relationnelle, 2: Les secrets du POUVOIR (après midi)  
*mode : base-URL · confiance : 1.0*

**Sections de la fiche jumelle** :

- Concepts enseignés
- The-brilliant-idea-from-the-creators-of-#Metoo-to-save-the-movement-synthese
- Video-p1WU4JiuIzQ-synthese
- L'intelligence-relationnelle-2-synthese
- Video-tiDHbY0rQKQ-synthese
- L'intelligence-relationnelle-1-synthese
- Video-x2zvDhh2yu4-synthese
- This-case-would-be-front-page-news-if-only-the-murderer-were-a-man,-but...-🤫-synthese
- This-government-campaign-was-so-successful-that-you've-(probably)-never-seen-it.-synthese
- Fiche transcrite par Bartilabas

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C071`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 110. Langage des hommes

- **Identifiant** : `C270` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/langage-hommes`
- **Base thématique** : `langage-hommes`
- **Taille de la fiche** : 778 mots (contenu de session absent)

**Formation jumelle** : `C087` — Langage des hommes  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> C'est le langage qui divise
> Pascal Quignard Parce qu'on ne va pas se mentir* : à mon grand désarroi, vous ne comprenez strictement rien aux hommes, et ce quand bien même ils font l'effort de vous parler. Ce qui n'est pas toujours le cas. Les gros balourds.
> Tonton Stéphane…
> …l'homme qui murmure à l'oreille des femmes H entend mais n'écoute pas ; F écoute mais avec quoi !?
> Indice : pas avec ses oreilles, manifestement.
> Parmi les 25+ phrases que nous décoderons ensemble
> Tu es trop bien pour moi
> Comme tu veux
> Qu'est-ce que je vais faire de toi
> On verra
> Tu ferais une très bonne maman
> Je ne veux pas me prendre la tête
> Sans oublier el famoso…
> … (le silence) Voir cette publication sur Instagram Une 

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-santé-mentale-synthese
- Stéphane-Edouard-attendri-par-une-Femen-synthese
- Formations et fiches liées
- Baby-metisse-et-tweets-fétichisant-synthese
- Formations et fiches liées
- Video-p1WU4JiuIzQ-synthese
- Comment-se-construire-une-esthétique-synthese
- Applications pratiques
- Video-m54h8ZXqHO0-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C087`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 111. Le bonheur : 7 techniques pour être heureux et surfer la vie

- **Identifiant** : `C274` · **Catégorie** : Santé Mentale
- **URL de catalogue** : `mat-consulting.fr/bonheur`
- **Base thématique** : `bonheur`
- **Taille de la fiche** : 1478 mots (contenu de session absent)

**Formation jumelle** : `C038` — Le bonheur : 7 techniques pour être heureux et surfer la vie  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Tout a peut-être été déjà été dit sur le bonheur (et encore que, cela reste à vérifier), et alors : êtes-vous en mesure de me définir exactement ce que c'est ? Essayez d'en formuler une définition claire en 30 secondes sans recourir à une aide électronique dont le nom commencerait par wiki
> dans quelles conditions se manifeste t-il ?
> avez-vous le sentiment d'avoir une prise quelconque sur votre état d'esprit ? Why is our generation so unhappy?
> — 🌸🌸 (@Graciethebrand) March 23, 2024 Pourquoi être heureux est important
> Je dois vraiment vous le dire ? Bon, allez : La solitude tue. Or être malheureux, c'est (à terme) être seul
> Les gens heureux ont plus d'amis…
> … et de partenaires sexuels (slurp)
> L

**Sections de la fiche jumelle** :

- Concepts enseignés
- Le-bonheur-7-techniques-pour-être-heureux-et-surfer-la-vie-synthese
- Video-HjrJlmCJT3Y-synthese
- Formations et fiches liées
- Video-OPtQxFnZFX4-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C038`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 112. Le bonheur – matin

- **Identifiant** : `C275` · **Catégorie** : Santé Mentale
- **URL de catalogue** : `mat-consulting.fr/bonheur-matin`
- **Base thématique** : `bonheur`
- **Taille de la fiche** : 1421 mots (contenu de session absent)

**Formation jumelle** : `C038` — Le bonheur : 7 techniques pour être heureux et surfer la vie  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Tout a peut-être été déjà été dit sur le bonheur (et encore que, cela reste à vérifier), et alors : êtes-vous en mesure de me définir exactement ce que c'est ? Essayez d'en formuler une définition claire en 30 secondes sans recourir à une aide électronique dont le nom commencerait par wiki
> dans quelles conditions se manifeste t-il ?
> avez-vous le sentiment d'avoir une prise quelconque sur votre état d'esprit ? Why is our generation so unhappy?
> — 🌸🌸 (@Graciethebrand) March 23, 2024 Pourquoi être heureux est important
> Je dois vraiment vous le dire ? Bon, allez : La solitude tue. Or être malheureux, c'est (à terme) être seul
> Les gens heureux ont plus d'amis…
> … et de partenaires sexuels (slurp)
> L

**Sections de la fiche jumelle** :

- Concepts enseignés
- Le-bonheur-7-techniques-pour-être-heureux-et-surfer-la-vie-synthese
- Video-HjrJlmCJT3Y-synthese
- Formations et fiches liées
- Video-OPtQxFnZFX4-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C038`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 113. Le couple « à l&rsquo;ancienne », c&rsquo;est du passé. Encaissez les ruptures LIKE A BOSS

- **Identifiant** : `C277` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/couple-rupture-difficile`
- **Base thématique** : `couple-rupture-difficile`
- **Taille de la fiche** : 939 mots (contenu de session absent)

**Formation jumelle** : `C003` — Le couple « à l'ancienne », c'est du passé. Encaissez les ruptures LIKE A BOSS  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon, vous l'aurez remarqué, les couples ne fonctionnent plus (d'où le sous-titre du séminaire : encaissez les ruptures). C'est pas une vue de l'esprit, ni l'expression de mon fatalisme patent. Les gens restent ensemble de moins en moins longtemps, c'est universel en occident. Et si vous habitez une métropole, vous pouvez encore diviser votre « espérance de survie du couple » par 2, voire par 3. Vous voulez des chiffres ? entre 93 et 96, il y avait en moyenne chaque année 155 000 séparations. Ce chiffre est passé, en 15 ans à peine, à 253 000 ( ! ) par an (+63 % !!)
> Dans les années 80, 70 % des adultes en couple, âgés de 20 à 31 ans, vivaient au moins 15 ans ensemble. Cette statistique a perd

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- Pour-surmonter-une-rupture,-n'imite-pas-cette-youtubeuse-synthese
- Conclusion
- Formations et fiches liées
- Video-L_O9dPuT_jE-synthese
- Le trio magique de l'obsession
- La logique des sentiments
- La reconquête
- Chiale-encore-un-coup,-c'est-bon-pour-l'audimat-synthese
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C003`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 114. Le décodeur ultime de signes d&rsquo;intérêts !

- **Identifiant** : `C279` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/signes-interet`
- **Base thématique** : `signes-interet`
- **Taille de la fiche** : 894 mots (contenu de session absent)

**Formation jumelle** : `C179` — Le décodeur ultime de signes d'intérêts !  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Avoue. Une fois. Au moins une (1) fois. Tu te l'es posée, la question : comment savoir si une femme est intéressée (vraiment intéressée).
> Alors tu es parti fouiller sur le web. Et tu en as trouvé, du contenu. Des tonnes de contenus, devrais-je dire. Morcelées, éparpillées, ventilées partout sur des blogs, des pages, des forums. Sans parler des vidéos Youtube ou un type sorti de nulle part, debout devant un tableau blanc, dénué de tout diplôme en sciences humaines, vient t'expliquer la psychologie féminine découverte au cours de ses deux dernières années à draguer sur les boulevards.
> Et si on arrêtait le massacre à l'information sauvage ?
> Souvent, en regardant des tutos youtube sur la psychol

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'embrayage-qui-crie-famine-depuis-des-mois-synthese
- Titre
- Citation
- Conclusion
- Formations et fiches liées
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens
- 3. L'art d'"arracher" vs. cueillir ce qui s'offre

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C179`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 115. Les couples ne fonctionnent plus – matin

- **Identifiant** : `C286` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/couple-rupture-difficile-matin`
- **Base thématique** : `couple-rupture-difficile`
- **Taille de la fiche** : 1046 mots (contenu de session absent)

**Formation jumelle** : `C003` — Le couple « à l'ancienne », c'est du passé. Encaissez les ruptures LIKE A BOSS  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon, vous l'aurez remarqué, les couples ne fonctionnent plus (d'où le sous-titre du séminaire : encaissez les ruptures). C'est pas une vue de l'esprit, ni l'expression de mon fatalisme patent. Les gens restent ensemble de moins en moins longtemps, c'est universel en occident. Et si vous habitez une métropole, vous pouvez encore diviser votre « espérance de survie du couple » par 2, voire par 3. Vous voulez des chiffres ? entre 93 et 96, il y avait en moyenne chaque année 155 000 séparations. Ce chiffre est passé, en 15 ans à peine, à 253 000 ( ! ) par an (+63 % !!)
> Dans les années 80, 70 % des adultes en couple, âgés de 20 à 31 ans, vivaient au moins 15 ans ensemble. Cette statistique a perd

**Concepts enseignés** :

L'Abandon Consenti de Souveraineté · Devenir Maman avant de Devenir Femme · Le Confort comme Piège · L'Espérance de Vie et le Changement Structurel

**Sections de la fiche jumelle** :

- Concepts enseignés
- Pour-surmonter-une-rupture,-n'imite-pas-cette-youtubeuse-synthese
- Conclusion
- Formations et fiches liées
- Video-L_O9dPuT_jE-synthese
- Le trio magique de l'obsession
- La logique des sentiments
- La reconquête
- Chiale-encore-un-coup,-c'est-bon-pour-l'audimat-synthese
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C003`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 116. Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (matin)

- **Identifiant** : `C287` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-2-plus-de-rencontres-maintenant-matin`
- **Base thématique** : `les-jeunes-filles-2-plus-de-rencontres-maintenant`
- **Taille de la fiche** : 1387 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.4) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 117. Like a boss, 2: Des presentations (ecrites et orales) qui TUENT (matin)

- **Identifiant** : `C289` · **Catégorie** : Carrière & Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-2-des-presentations-ecrites-et-orales-qui-tuent-matin-2`
- **Base thématique** : `like-a-boss-2-des-presentations-ecrites-et-orales-qui-tuent-matin`
- **Taille de la fiche** : 1928 mots (contenu de session absent)

**Formation jumelle** : `C016` — Like a boss, 2 : des presentations (écrites et orales) qui TUENT  
*mode : theme · confiance : 0.83*

**Contenu verbatim disponible** (couche 1) :

> Savoir et Savoir-faire sont sur un bateau…
> … qui pousse l'autre à l'eau, devient capitaine, reçoit la gloire et les honneurs
> Cette antinomie, cette fracture, cette lutte à mort entre
> – d'un côté la compétence brute, le laborieux silencieux, voire le génie autiste façon Alan Turing (l'inventeur de l'ordinateur, popularisé par un film Hollywoodien, mettant en avant son incapacité pathologique à expliquer le but de ses recherches)
> On a bien failli ne jamais avoir de tablette entre les mains, parce qu'Alan Turing ne savait pas présenter son projet : l'ordinateur
> – et de l'autre le communiquant pur, totalement improductif mais génie de l'embrouille, de la parlotte, capable de vendre du sable à cr

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C016`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 118. Like a boss, 2 : des presentations (écrites et orales) qui TUENT

- **Identifiant** : `C290` · **Catégorie** : Carrière & Leadership
- **URL de catalogue** : `mat-consulting.fr/presenter-son-projet`
- **Base thématique** : `presenter-son-projet`
- **Taille de la fiche** : 863 mots (contenu de session absent)

**Formation jumelle** : `C016` — Like a boss, 2 : des presentations (écrites et orales) qui TUENT  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Savoir et Savoir-faire sont sur un bateau…
> … qui pousse l'autre à l'eau, devient capitaine, reçoit la gloire et les honneurs
> Cette antinomie, cette fracture, cette lutte à mort entre
> – d'un côté la compétence brute, le laborieux silencieux, voire le génie autiste façon Alan Turing (l'inventeur de l'ordinateur, popularisé par un film Hollywoodien, mettant en avant son incapacité pathologique à expliquer le but de ses recherches)
> On a bien failli ne jamais avoir de tablette entre les mains, parce qu'Alan Turing ne savait pas présenter son projet : l'ordinateur
> – et de l'autre le communiquant pur, totalement improductif mais génie de l'embrouille, de la parlotte, capable de vendre du sable à cr

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C016`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 119. Like a boss, 3: Seduire et fideliser ses clients A VIE (après midi)

- **Identifiant** : `C291` · **Catégorie** : Carrière & Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie-apres-midi`
- **Base thématique** : `like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie`
- **Taille de la fiche** : 2127 mots (contenu de session absent)

**Aucune fiche jumelle fiable** — la meilleure ressemblance thématique
(0.43) est sous le seuil de 0.5. Aucune substitution n'est proposée :

combler cette fiche serait inventer.

**Statut** :

- **non reconstituable** — aucun contenu de substitution dans le corpus
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 120. Like a boss, 3: Seduire et fideliser ses clients A VIE (matin)

- **Identifiant** : `C292` · **Catégorie** : Carrière & Leadership
- **URL de catalogue** : `mat-consulting.fr/like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie-matin`
- **Base thématique** : `like-a-boss-3-seduire-et-fideliser-ses-clients-a-vie`
- **Taille de la fiche** : 2111 mots (contenu de session absent)

**Formation jumelle** : `C006` — Like a boss, 3 : Séduire et fidéliser ses clients A VIE  
*mode : theme · confiance : 0.6*

**Contenu verbatim disponible** (couche 1) :

> Je sais pas vous, mais j'ai déjà eu l'occasion de mourir plusieurs fois. Médiatiquement parlant, s'entend. Tout a commencé dans la 17ème année du XXIème siècle de notre ère par un bien sombre article dans 20 minutes qui m'accusait de… l'inverse exact de ce que je disais en vidéo. Entreprise de diffamation relayée depuis, chaque année ou presque, par un con-frère ou une con-soeur fainéant de la presse aux ordres (pléonasme). Mais… ici, on ne lâche rien, parce que :
> Mes clients m'ont toujours sauvé la vie
> Devant l'adversité, 100 % de mes clients se montrent (encore aujourd'hui) solidaires et unis ! Ça, c'est pas une preuve de fidélité ? Ça, c'est pas une preuve de fidélité ?
> Que vous soyez ent

**Sections de la fiche jumelle** :

- Concepts enseignés
- Calin-o-thérapie-le-stage-où-les-perdants-de-la-modernité-se-réconfortent-entre-eux-synthese
- Le marché des rencontres
- Analyse des participants
- Le phénomène étudié
- Le "loopen prolétariat" des rencontres
- Katia, prof de yoga
- Réaction aux critiques
- Video-_z11PNOSbnM-synthese
- Formations et fiches liées

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C006`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 121. Logique de l&rsquo;Homme (matin)

- **Identifiant** : `C294` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/comprendre-les-hommes-matin`
- **Base thématique** : `comprendre-les-hommes`
- **Taille de la fiche** : 915 mots (contenu de session absent)

**Formation jumelle** : `C084` — Logique des hommes – le côté obscur de H pur  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Expliquer le langage des femmes, leur logique, comment elles voient le monde : c'est ma spécialité, j'aime ça et je suis le meilleur. Mais si vous ne réussissez pas à comprendre les hommes, alors tout ceci ne sert à rien ! Voir cette publication sur Instagram Une publication partagée par Nora & Khalid (@noraandkhalid) La relation homme-femme, c'est un puzzle, une histoire de compatibilité, il faut comprendre les penchants des uns et des autres pour tenter de s'emboiter au mieux.
> Comprendre les hommes, c'est simple…
> …encore faut-il avoir la bonne paire de lunettes
> Car nous (les hommes) sommes aussi bourrés de biais cognitifs que les femmes, nous n'en avons tout simplement pas conscience.
> Nous

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-santé-mentale-synthese
- La-résilience-synthese
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese
- 1. Le postulat de départ du livre
- 2. La mère de Stéphane comme témoin
- 3. Ce que l'homme attend vs. ce que la femme fait
- Ne-soyez-plus-les-esclaves-des-femmes-synthese
- 1. La gratification indirecte (Le "mini-Darmanin")
- 2. Le refus de faire le travail à la place (La logique de l'autonomie)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C084`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 122. Logique des hommes – le côté obscur de H pur

- **Identifiant** : `C295` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/comprendre-les-hommes`
- **Base thématique** : `comprendre-les-hommes`
- **Taille de la fiche** : 1552 mots (contenu de session absent)

**Formation jumelle** : `C084` — Logique des hommes – le côté obscur de H pur  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Expliquer le langage des femmes, leur logique, comment elles voient le monde : c'est ma spécialité, j'aime ça et je suis le meilleur. Mais si vous ne réussissez pas à comprendre les hommes, alors tout ceci ne sert à rien ! Voir cette publication sur Instagram Une publication partagée par Nora & Khalid (@noraandkhalid) La relation homme-femme, c'est un puzzle, une histoire de compatibilité, il faut comprendre les penchants des uns et des autres pour tenter de s'emboiter au mieux.
> Comprendre les hommes, c'est simple…
> …encore faut-il avoir la bonne paire de lunettes
> Car nous (les hommes) sommes aussi bourrés de biais cognitifs que les femmes, nous n'en avons tout simplement pas conscience.
> Nous

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-santé-mentale-synthese
- La-résilience-synthese
- Esther-Villard-La-manipulation-dans-les-relations-hommes-femmes-synthese
- 1. Le postulat de départ du livre
- 2. La mère de Stéphane comme témoin
- 3. Ce que l'homme attend vs. ce que la femme fait
- Ne-soyez-plus-les-esclaves-des-femmes-synthese
- 1. La gratification indirecte (Le "mini-Darmanin")
- 2. Le refus de faire le travail à la place (La logique de l'autonomie)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C084`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 123. L&rsquo;amant, 2

- **Identifiant** : `C297` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/faire-lamour-a-une-femme`
- **Base thématique** : `faire-lamour-a-une-femme`
- **Taille de la fiche** : 3246 mots (contenu de session absent)

**Formation jumelle** : `C042` — L'amant, 2  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon. Je vais faire simple. Pour une grande, pour une immense majorité d'hétéros binaires de base, l'acte sexuel unissant un homme et une femme se réduit à remorquer une F (consentante) sur une app' de rencontre
> essuyer avec grâce – et un semblant de détachement – une addition au restaurant plus ou moins salée
> un enchaînement plus ou moins hésitant et foireux pour prolonger la soirée chez l'un ou chez l'autre, sous couvert d'un prétexte risible
> un effeuillage penaud conclu par une pénétration vigoureuse et empressée avant le réglementaire repos du guerrier Voilà, pliez bagage, y'a plus à rien à voir, ron-ron dit celui qui se met à ronfler, et « merci pour ce moment » dit celle qui s'échappe s

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C042`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 124. L&rsquo;amant idéal, 2 : faire jouir une femme (matin)

- **Identifiant** : `C298` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/faire-lamour-a-une-femme-matin`
- **Base thématique** : `faire-lamour-a-une-femme`
- **Taille de la fiche** : 714 mots (contenu de session absent)

**Formation jumelle** : `C042` — L'amant, 2  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon. Je vais faire simple. Pour une grande, pour une immense majorité d'hétéros binaires de base, l'acte sexuel unissant un homme et une femme se réduit à remorquer une F (consentante) sur une app' de rencontre
> essuyer avec grâce – et un semblant de détachement – une addition au restaurant plus ou moins salée
> un enchaînement plus ou moins hésitant et foireux pour prolonger la soirée chez l'un ou chez l'autre, sous couvert d'un prétexte risible
> un effeuillage penaud conclu par une pénétration vigoureuse et empressée avant le réglementaire repos du guerrier Voilà, pliez bagage, y'a plus à rien à voir, ron-ron dit celui qui se met à ronfler, et « merci pour ce moment » dit celle qui s'échappe s

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C042`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 125. L&rsquo;amant idéal, 2 (après-midi)

- **Identifiant** : `C299` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/faire-lamour-a-une-femme-apres-midi`
- **Base thématique** : `faire-lamour-a-une-femme`
- **Taille de la fiche** : 1063 mots (contenu de session absent)

**Formation jumelle** : `C042` — L'amant, 2  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Bon. Je vais faire simple. Pour une grande, pour une immense majorité d'hétéros binaires de base, l'acte sexuel unissant un homme et une femme se réduit à remorquer une F (consentante) sur une app' de rencontre
> essuyer avec grâce – et un semblant de détachement – une addition au restaurant plus ou moins salée
> un enchaînement plus ou moins hésitant et foireux pour prolonger la soirée chez l'un ou chez l'autre, sous couvert d'un prétexte risible
> un effeuillage penaud conclu par une pénétration vigoureuse et empressée avant le réglementaire repos du guerrier Voilà, pliez bagage, y'a plus à rien à voir, ron-ron dit celui qui se met à ronfler, et « merci pour ce moment » dit celle qui s'échappe s

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese
- Stratégie 1: L'amitié comme stratégie (~6/10)

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C042`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 126. L&rsquo;école des hommes

- **Identifiant** : `C300` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/lecole-des-hommes`
- **Base thématique** : `lecole-des-hommes`
- **Taille de la fiche** : 3340 mots (contenu de session absent)

**Formation jumelle** : `C088` — L'école des hommes  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> El famoso premier livre de Stéphane Edouard, pour la première fois réédité au format numérique et à prix doux.
> Plus aucune raison de le pirater, et c’est aussi une façon de dire merci pour les centaines d’heures de contenu gratuit sur Youtube.
> L'ancienne couverture window.addEventListener('load', function() { jQuery('.duree').text('465 pages'); }); ---

**Sections de la fiche jumelle** :

- Concepts enseignés
- Fiche transcrite par Bartilabas
- Pré-requis
- Public visé
- Niveau
- Durée estimée
- Format
- Discipline > motivation
- Objectifs concrets
- Sortir de la zone de confort

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C088`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 127. Où / quand / comment rencontrer une fille bien

- **Identifiant** : `C313` · **Catégorie** : Sédduction & Rencontres
- **URL de catalogue** : `mat-consulting.fr/rencontrer-une-fille-bien`
- **Base thématique** : `rencontrer-une-fille-bien`
- **Taille de la fiche** : 762 mots (contenu de session absent)

**Formation jumelle** : `C106` — Où / quand / comment rencontrer une fille bien  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> D'après toi, rencontrer une fille bien, ça s'attend
> se mérite
> se provoque ? Réponse : la 3. Problème : la plupart des gens déploient plus d'énergie, de réflexion, de comparaison, de benchmark à choisir une maison, un crédit, une auto, voire un ordinateur, qu'à réfléchir à la personne avec qui ils devront (théoriquement) passer le reste de leur vie. Pourquoi ? Voir cette publication sur Instagram Une publication partagée par Eliott & Lilian 🦈 (@eliottlilian_off) La plupart des hommes n'ont aucune idée de ce qu'est une fille bien
> Empêtrés par le reste de son oedipe mal digéré, et incapable d'articuler dialectiquement la maman et la putain, l'homme hétérosexuel « normal » a beau émettre le vagu

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'un-de-ces-deux-protagonistes-me-provoque-un-réel-malaise-🤢,-mais-lequel-synthese
- Formations et fiches liées
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Si-seulement-ce-pouvait-être-la-dernière-fois-🕯-(Affaire-Lola)-synthese
- Applications pratiques
- Video-q5jirxsgC5Q-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C106`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 128. Plus de rencontres

- **Identifiant** : `C318` · **Catégorie** : Sédduction & Rencontres
- **URL de catalogue** : `mat-consulting.fr/rencontrer-des-femmes`
- **Base thématique** : `rencontrer-des-femmes`
- **Taille de la fiche** : 1321 mots (contenu de session absent)

**Formation jumelle** : `C162` — Plus de rencontres  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Cette journée s'adresse à tous ceux dont l'objectif est simple : ils ne cherchent ni l'âme sœur ni la future mère de leur portée (si tant est qu'elle existe), ils veulent simplement rencontrer des femmes, ils veulent plus de femmes dans leur vie. Pour être plus libres, plus épanouis, moins stressés, et globalement plus heureux. Et quand le veulent-ils ? Disons, maintenant 😉
> Je vous ai déjà livré les derniers secrets d'une enquête réalisée en exclusivité avec la tv française sur les nouvelles attentes féminines. C'était le premier volet du cycle « les jeunes filles »*.
> Tout savoir pour rencontrer des femmes
> Selon les femmes (qu'en dépit de leur double langage permanent, je continue d'écouter,

**Sections de la fiche jumelle** :

- Concepts enseignés
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Faites-toujours-confiance-aux-femmes-synthese
- 1. L'encensement comme mise à part (Règle 1)
- 2. La mendicité oratoire (Règle 2 : ne pas interrompre)
- 3. La persuasion sexuelle : une chimère (Règle 3)
- Montrer-son-intérêt-à-un-homme,-pt.22-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C162`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 129. Rencontre (enfin) une fille bien ! (matin)

- **Identifiant** : `C327` · **Catégorie** : Sédduction & Rencontres
- **URL de catalogue** : `mat-consulting.fr/rencontrer-une-fille-bien-matin`
- **Base thématique** : `rencontrer-une-fille-bien`
- **Taille de la fiche** : 429 mots (contenu de session absent)

**Formation jumelle** : `C106` — Où / quand / comment rencontrer une fille bien  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> D'après toi, rencontrer une fille bien, ça s'attend
> se mérite
> se provoque ? Réponse : la 3. Problème : la plupart des gens déploient plus d'énergie, de réflexion, de comparaison, de benchmark à choisir une maison, un crédit, une auto, voire un ordinateur, qu'à réfléchir à la personne avec qui ils devront (théoriquement) passer le reste de leur vie. Pourquoi ? Voir cette publication sur Instagram Une publication partagée par Eliott & Lilian 🦈 (@eliottlilian_off) La plupart des hommes n'ont aucune idée de ce qu'est une fille bien
> Empêtrés par le reste de son oedipe mal digéré, et incapable d'articuler dialectiquement la maman et la putain, l'homme hétérosexuel « normal » a beau émettre le vagu

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'un-de-ces-deux-protagonistes-me-provoque-un-réel-malaise-🤢,-mais-lequel-synthese
- Formations et fiches liées
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale
- 2. La métaphore des "gardes du corps"
- 3. Le mariage comme cas d'école
- Si-seulement-ce-pouvait-être-la-dernière-fois-🕯-(Affaire-Lola)-synthese
- Applications pratiques
- Video-q5jirxsgC5Q-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C106`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 130. Reçois ton La Furia© dédicacé !

- **Identifiant** : `C330` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/la-furia`
- **Base thématique** : `la-furia`
- **Taille de la fiche** : 3467 mots (contenu de session absent)

**Formation jumelle** : `C154` — Reçois ton La Furia© dédicacé !  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Tu étais où le soir du lancement de La Furia à Paris ? Chez toi ? C'est ballot, tu n'as pas pu me faire dédicacer ton exemplaire. Heureusement qu'il y a Internet : rattrape-toi vite, il m'en reste quelques-uns et je m'appliquerai même à écrire ton prénom sans (trop de) fautes.
> Index des articles par numéro Mensonges médiatiques et vérités Internet, pt.1 : fiers d'être dupes
> Mensonges médiatiques et vérités Internet, pt.2 : florilège d'impostures
> Argent et prolétariat : histoire d'une folie à deux, pt.1 : où sont les pauvres ?
> Argent et prolétariat : histoire d'une folie à deux, pt.2 : le monde festoie sur le cratère d'un volcan
> Vers la remigration, pt.1 : la Guyane
> Le Palmarès des P.P.P, pt.

**Sections de la fiche jumelle** :

- Concepts enseignés
- Ces-traits-de-caractère-insupportables-qui-étaient-décelables-en-2-mn-synthese
- Formations et fiches liées
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Elle-plaque-tout-pour-devenir-stripteaseuse-(la-suite-va-te-surprendre)-synthese
- Applications pratiques
- The-Circus-of-A-Gendered-Children-on-TV-synthese
- Citation marquant
- Conclusion
- Video-2886bTU-5Yk-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C154`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 131. Sauver sa santé mentale

- **Identifiant** : `C333` · **Catégorie** : Santé Mentale
- **URL de catalogue** : `mat-consulting.fr/sante-mentale`
- **Base thématique** : `sante-mentale`
- **Taille de la fiche** : 704 mots (contenu de session absent)

**Formation jumelle** : `C126` — Sauver sa santé mentale  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> L'expression comment préserver sa santé mentale n'a jamais été aussi recherché dans le monde Je n'aborderai pas l'épineux et sérieux sujet de la dépression. Si vous pensez être en dépression, ou connaissez des gens qui en souffrent, je suis au regret de vous dire clairement, d'entrée de jeu, que je n'ai pas de solution à apporter à cette pathologie. Navré.
> Les contenus présentés au cours de cette journée n'ont évidemment pas vocation à se substituer à ceux recueillis auprès d'un professionnel de la santé. Ils ne sont que l'avis d'un pauvre ingénieur en mécanique qui s'est vu greffer un DEA en sociologie, de surcroît ex-starlette de la tv et Youtuboomeur* à ses heures. Ceci étant mainten

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-santé-mentale-synthese
- Gaslighting-cette-drôle-manière-d'abréger-les-femmes-synthese
- 1. Le témoignage analyzed
- 2. Les techniques de gaslighting
- 3. L'effet sur la victime
- Video-m54h8ZXqHO0-synthese
- Sujet
- Thèmes abordés
- Question posée

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C126`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 132. Signes d&rsquo;intérêt (matin)

- **Identifiant** : `C345` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/signes-interet-matin`
- **Base thématique** : `signes-interet`
- **Taille de la fiche** : 988 mots (contenu de session absent)

**Formation jumelle** : `C179` — Le décodeur ultime de signes d'intérêts !  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Avoue. Une fois. Au moins une (1) fois. Tu te l'es posée, la question : comment savoir si une femme est intéressée (vraiment intéressée).
> Alors tu es parti fouiller sur le web. Et tu en as trouvé, du contenu. Des tonnes de contenus, devrais-je dire. Morcelées, éparpillées, ventilées partout sur des blogs, des pages, des forums. Sans parler des vidéos Youtube ou un type sorti de nulle part, debout devant un tableau blanc, dénué de tout diplôme en sciences humaines, vient t'expliquer la psychologie féminine découverte au cours de ses deux dernières années à draguer sur les boulevards.
> Et si on arrêtait le massacre à l'information sauvage ?
> Souvent, en regardant des tutos youtube sur la psychol

**Sections de la fiche jumelle** :

- Concepts enseignés
- L'embrayage-qui-crie-famine-depuis-des-mois-synthese
- Titre
- Citation
- Conclusion
- Formations et fiches liées
- Le-verbe-arracher-et-la-disponibilité-féminine-synthese
- 1. La formule beauté + intelligence + disponibilité = constante
- 2. La disponibilité comme concept à double sens
- 3. L'art d'"arracher" vs. cueillir ce qui s'offre

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C179`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 133. Simplifiez-vous la vie ! (webinaire court et impactant, 2h « seulement »)

- **Identifiant** : `C348` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/se-simplifier-la-vie-webinar`
- **Base thématique** : `se-simplifier-la-vie-webinar`
- **Taille de la fiche** : 2036 mots (contenu de session absent)

**Formation jumelle** : `C349` — Simplifiez-vous la vie ! (webinaire court et impactant, 2h « seulement »)  
*mode : base-URL · confiance : 1.0*

**Sections de la fiche jumelle** :

- Concepts enseignés
- Pourquoi la simplification est difficile
- Les 4 domaines de simplification
- Le cadre de décision « Oui, Non, ou Hell Yeah »
- La simplification comme philosophie de pouvoir
- Le-bonheur-7-techniques-pour-être-heureux-et-surfer-la-vie-synthese
- Vaincre-la-peur-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C349`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 134. S&rsquo;entourer pour réussir, ou le secret des affinités électives

- **Identifiant** : `C353` · **Catégorie** : Divers
- **URL de catalogue** : `mat-consulting.fr/savoir-bien-sentourer`
- **Base thématique** : `savoir-bien-sentourer`
- **Taille de la fiche** : 3512 mots (contenu de session absent)

**Formation jumelle** : `C121` — S'entourer pour réussir, ou le secret des affinités électives  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> « Chacun veut être autonome, mais en même temps que grandit notre liberté individuelle grandit notre besoin d'être lié aux autres (…) il y a quelques années, seuls le couple, la famille et les amis étaient des lieux d'investissement affectif » ~ JC Kaufmann (le sociologue qui ne m'aime pas)
> Les paradoxes de quiconque cherche à bien s'entourer Dans une société narcissique, on cherche inlassablement son semblable, que l'on ne trouvera jamais puisque tout est conçu pour valoriser notre unicité (« parce que JE le vaux bien« )
> Pour des millions de personnes à travers le monde, savoir bien s'entourer c'est faire des enfants et les élever. Problème : un peu partout dans le monde, des millions d'enf

**Sections de la fiche jumelle** :

- Concepts enseignés
- 30-mn-gratuites-du-séminaire-savoir-s'entourer-synthese
- Séminaires "Savoir s'entourer" – Affinités électives, groupes et réseaux
- Formations et fiches liées
- L'entraide-entre-femmes-un-déficit-historique-synthese
- 1. Le déficit de sororité dès l'enfance
- 2. La stratégie de survie : s'entourer d'hommes
- 3. Le "sixième sens" féminin
- Le-secret-derrière-ces-millions-de-femmes-seules-est-si-bête-que-c'en-est-gênant-synthese
- 1. La configuration spatiale fatale

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C121`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 135. Survivre à la ROUTINE du couple (matin)

- **Identifiant** : `C358` · **Catégorie** : Relations H-F
- **URL de catalogue** : `mat-consulting.fr/les-jeunes-filles-3-audace-scenarii-oses-pour-rencontres-memorables-matin`
- **Base thématique** : `les-jeunes-filles-3-audace-scenarii-oses-pour-rencontres-memorables`
- **Taille de la fiche** : 1021 mots (contenu de session absent)

**Formation jumelle** : `C025` — Survivre à la ROUTINE du couple  
*mode : theme · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Vous avez remarqué ? Désormais tout le monde est devenu sociologue, tout le monde est anthropologue, tout le monde est expert en sciences cognitives, tout le monde est [insérer la spécialité de votre choix] depuis qu'ils ont visionné 3 ou 4 vidéos sur Youtube sur le sujet. Sic. Mais vous savez quoi ? Laissons-les dire, laissons-les faire : il faut que jeunesse se passe…
> Et pourtant…
> Les hommes ne savent (toujours) pas QUOI FAIRE avec les femmes
> Oui, j'ose le répéter : les hommes ne savent pas quoi faire avec les femmes. Au risque de simplifier un peu, c'est vrai et je l'ai vérifié à des centaines, à des milliers de reprises : vous voulez une/des femme(s) dans votre vie, vous mettez en place 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- Combien-de-fois-A.Buzyn-a-t-elle-menti-à-la-commission-d'enquête-synthese
- Méthodologie
- Score de mentir
- Points critiques relevés
- Citation du Professeur Raoult
- Vidéoscopie-–-Analyse-de-propos-sur-les-femmes-et-la-négociation-salariale-synthese
- La-résilience-synthese
- La-logique-masculine-face-à-l'absence-de-motivation-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C025`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 136. Survivre aux mensonges du nouveau monde (le discernement)

- **Identifiant** : `C359` · **Catégorie** : Intelligence Sociale
- **URL de catalogue** : `mat-consulting.fr/discernement`
- **Base thématique** : `discernement`
- **Taille de la fiche** : 1586 mots (contenu de session absent)

**Formation jumelle** : `C069` — Survivre aux mensonges du nouveau monde (le discernement)  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Malheureusement nous manquons de discernement et d'indépendance dans nos choix ; nous ne distinguons pas entre l'idole de la veille, devenue méprisable aujourd'hui, et celle qui mérite tous nos sacrifices ~ Astolphe de Custine (1790-1857)
> On ne meurt pas impunément le soir de l'anniversaire des gens. Je l'ai découvert à l'occasion de la disparition de celui qui m'aura appris – sinon « tout » – du moins à respirer, à écouter et à m'exprimer ; ce qui, vous en conviendrez, n'est pas quantité négligeable dans une vie en communauté (non, ça n'est pas Pierre Bénichou). Tintin est pénible pic.twitter.com/gO5rcW2djG
> — Tweetinão (@tintinades) March 13, 2024 L'échelle des vertus Qu'y a t-il au-dessus 

**Sections de la fiche jumelle** :

- Concepts enseignés
- Survivre-aux-mensonges-du-nouveau-monde-le-discernement-synthese
- L'intelligence-relationnelle-1-synthese
- Combien-de-fois-A.Buzyn-a-t-elle-menti-à-la-commission-d'enquête-synthese
- Méthodologie
- Score de mentir
- Points critiques relevés
- Citation du Professeur Raoult
- Video-py5soTfXpxQ-synthese
- Un-monde-sans-hommes-cette-nouvelle-lubie-des-séries-cache-un-projet-eugéniste-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C069`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

### 137. Vivre avec la procrastination

- **Identifiant** : `C366` · **Catégorie** : Développement Personnel
- **URL de catalogue** : `mat-consulting.fr/procrastination-solutions`
- **Base thématique** : `procrastination-solutions`
- **Taille de la fiche** : 3207 mots (contenu de session absent)

**Formation jumelle** : `C050` — Vivre avec la procrastination  
*mode : base-URL · confiance : 1.0*

**Contenu verbatim disponible** (couche 1) :

> Procrastination : des solutions existent… oui mais lesquelles ? Il va de cesser de procrastiner comme d'arrêter de fumer : on connaît tous des gens qui y sont parvenus, et affirment la main sur le coeur ne jamais avoir été tentés de rechuter. Problème : ce sont les moins nombreux, ils sont même l'exception. Et révèlent trop rarement leurs secrets. Souvent, il s'agit d'un détail insignifiant, qui ne fonctionne pas pour nous. Bien souvent, cela n'a rien de rationnel.
> « J'étais occupée à procrastiner toute la journée, désolée »
> Procrastination : des solutions (enfin) à votre portée
> J'ai globalement de la chance. Globalement. Un certain nombre de facultés m'ont été léguées par je ne sais quel ph

**Sections de la fiche jumelle** :

- Concepts enseignés
- La-France-a-un-nouvel-intellectuel...-le-monde-entier-nous-l'envie-synthese
- Formations et fiches liées
- Marguerite-Stern-Behind-the-Scenes-of-the-Feminist-Dream-Life-synthese
- Provoc'-Bill-Cosby,-ce-père-modèle-😅-synthese
- Citation notable
- La-logique-masculine-face-à-l'absence-de-motivation-synthese
- 1. La "coquille vide" : Beauté sans substance
- 2. La logique masculine vs. la logique féminine
- Video-vvh8wAYHRBw-synthese

**Statut** :

- **reconstituable** — doctrine, citations et concepts via `C050`
- **Non couvert** : le déroulé exact de la session, les diapositives, les exercices propres à cette session.

---

## 4. Les formations non reconstituables

**18 formations** n'ont aucun équivalent fiable dans le corpus. Pour elles,
la seule ressource est le **flux oral gratuit** : les vidéos YouTube et les podcasts de
l'auteur sur le même champ thématique. Elles sont listées ici pour que l'absence soit
**assumée** plutôt que comblée par une approximation.

| ID | TITRE | CATÉGORIE | MEILLEURE RESSEMBLANCE |
|---|---|---|---|
| `C013` | Like a boss, 3: Seduire et fideliser ses clients A VIE (après midi) | Carriere Leadership | 0.43 |
| `C018` | Ameliorer sa voix (avec une chanteuse professionnelle) (apres-midi) | Communication | 0.2 |
| `C019` | Ameliorer sa voix (avec une chanteuse professionnelle) (matin) | Communication | 0.2 |
| `C028` | Les couples ne fonctionnent plus – après-midi | Couple Relations Longues | 0.4 |
| `C039` | Fabriquer sa chance (apres-midi) | Developpement Personnel | 0.0 |
| `C040` | Fabriquer sa chance (matin) | Developpement Personnel | 0.0 |
| `C078` | Formations — Stéphane Édouard | Non catégorisé | 0.33 |
| `C089` | Les jeunes filles, 1: Decoder les attentes feminines (apres-midi) | Relations H-F | 0.2 |
| `C090` | Les jeunes filles, 1: Decoder les attentes feminines (matin) | Relations H-F | 0.2 |
| `C091` | Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (après midi) | Relations H-F | 0.29 |
| `C092` | Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (matin) | Relations H-F | 0.4 |
| `C144` | Ebook et audio | Sedirection Rencontres | 0.0 |
| `C145` | Ebook seul | Sedirection Rencontres | 0.0 |
| `C175` | Seduire bureau – ecole (apres-midi) | Sedirection Rencontres | 0.0 |
| `C176` | Seduire bureau – ecole (matin) | Sedirection Rencontres | 0.0 |
| `C209` | Catalogue des Formations | Non catégorisé | 0.0 |
| `C287` | Les jeunes filles, 2: Plus de RENCONTRES, maintenant! (matin) | Relations H-F | 0.4 |
| `C291` | Like a boss, 3: Seduire et fideliser ses clients A VIE (après midi) | Carrière & Leadership | 0.43 |

## 5. Règle de restitution

```
C009  « Like a boss, 1 : Devenir INDISPENSABLE au travail »
  -> reconstituée depuis C007 (même thème, session différente)
  -> citer : C007, en signalant « reconstitution »
```

**À faire** : citer l'identifiant de la fiche **jumelle**, jamais celui de la formation vide.
**À ne pas faire** : présenter le contenu de la jumelle comme « le cours » de la formation vide,
ni fusionner les deux dans une seule référence.

| Ce qui est couvert | Ce qui ne l'est pas |
|---|---|
| la doctrine de la formation | le déroulé exact de la session |
| les citations de l'auteur (vérifiées) | les diapositives |
| les concepts enseignés | les exercices propres à cette session |
| les distinctions et oppositions | le verbatim de l'orateur de cette session |

**Statut d'ensemble** : sur 369 fiches, **232** portent un contenu de l'auteur
directement, **119** le sont par reconstitution, et
**18** restent hors d'atteinte — soit **351/369 = 95 %** du corpus exploité.

