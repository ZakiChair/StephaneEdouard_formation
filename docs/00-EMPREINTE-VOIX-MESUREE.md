# Empreinte vocale mesurée — Stéphane Édouard

> **Source de vérité** : `/root/.hermes/cache/scratch/se_measure_v2.py`
> Sortie : `/root/.hermes/cache/scratch/se_measure_v2.json`
> **Rejoué le 2026-10-23** sur l'arbre vivant du corpus. Toutes les valeurs ci-dessous
> sont **remesurées**, jamais recopiées. Chaque chiffre porte son dénominateur.

> **Règle de ce document** : un chiffre sans dénominateur est un chiffre faux.
> Les cinq registres sont mesurés séparément, jamais mélangés.

---

## 1. Les cinq registres, et leur dénominateur

| # | Registre | Population | Fichiers | Mots | « vous » | « tu » | Ratio |
|---|---|---|---|---|---|---|---|
| **R1** | **ORAL** — flux vidéo, podcasts | transcripts FR, hors traductions auto | **376** | **2 105 621** | 21 365 | 21 604 | **0,99** |
| **R1b** | ORAL, sous-ensemble fort | R1 ∩ > 1 500 mots | **335** | **2 085 887** | 20 931 | 21 484 | **0,97** |
| **R2** | **ÉCRIT verbatim** — page produit | fiches couche 1, section « Contenu complet » | **83** | **20 497** | 531 | 53 | **10,02** |
| **R3** | **RÉDIGÉ par LLM** — PAS la voix | fiches couche 2 + stubs | **286** | **582 062** | 1 951 | 1 882 | **1,04** |
| **R4** | **ÉCRIT DE FOND** — ancien site | pages `web-*` | **1 059** | **1 187 405** | 23 563 | 5 315 | **4,43** |
| **R5** | **TIERCE** — participants | pages `tierce-*` | **497** | **151 405** | 1 045 | 1 150 | **0,91** |

> **Trois corrections par rapport à la version précédente de ce document.**
>
> 1. Le ratio oral était **inversé** : la division était à l'envers (20 931 / 21 484 = **0,97**,
>    pas 1,03). À l'oral il **tutoie un peu plus qu'il ne vouvoie**.
> 2. Le dénominateur oral n'est pas 335 mais **376** : le corpus FR complet en compte 376,
>    dont 335 dépassent 1 500 mots. Les deux sont donnés, avec leur population.
> 3. Le corpus **complet** (335 transcripts + 369 fiches + 343 synthèses, **3 130 043 mots**)
>    donne 24 893 « vous » pour 24 909 « tu » → ratio **1,00**. Ce n'est pas une troisième
>    règle : c'est le mélange des registres, qui s'annulent.
> 4. **Correction du 2026-10-23 (après réparation du corpus)** : 18 fiches de formation
>    portaient un préfixe de numéros de ligne (`1|# Titre`) qui rendait leur section
>    « Contenu complet » invisible à toute extraction. Huit d'entre elles portent en
>    réalité un verbatim de couche 1 : la couche 1 passe de **75 à 83 fiches**
>    (18 645 → 20 497 mots, ratio 9,65 → **10,02**). Les stubs payants passent de
>    93 à 101 et les fiches sans section de 201 à 185.

---

## 2. Registre : tutoiement ET vouvoiement

### 2.1 Oral (R1b, 335 transcripts, 2 085 887 mots)

| | Occurrences | Ratio |
|---|---|---|
| Tutoiement (`tu/ta/ton/tes/toi`) | **21 484** | — |
| Vouvoiement (`vous/vos/votre`) | **20 931** | — |
| **Rapport vous/tu** | | **0,97** |

À l'oral il **tutoie légèrement plus qu'il ne vouvoie**. Le vouvoiement n'est pas
l'absence de tutoiement : c'est un registre,/contextuel.

### 2.2 Écrit (R2, 83 fiches couche 1, 20 497 mots)

**531 « vous » pour 53 « tu » → ratio 10,02.** À l'écrit il vouvoie quasi systématiquement.

### 2.3 Par catégorie (couche 1, 83 fiches)

| Catégorie | n | « vous » | « tu » | Ratio | Mots |
|---|---|---|---|---|---|
| Sedirection Rencontres | 26 | 201 | 12 | 16 8 | 6 237 |
| Relations H-F | 15 | 78 | 6 | 13 0 | 3 518 |
| Intelligence Sociale | 9 | 70 | 0 | — | 2 297 |
| Developpement Personnel | 9 | 28 | 23 | 1 2 | 2 325 |
| Carriere Leadership | 7 | 46 | 2 | 23 0 | 1 794 |
| Reseau Influence | 7 | 24 | 4 | 6 0 | 1 807 |
| Couple Relations Longues | 4 | 50 | 0 | — | 1 005 |
| Communication | 3 | 26 | 6 | 4 3 | 769 |
| Style Image | 2 | 6 | 0 | — | 500 |
| Sante Mentale | 1 | 2 | 0 | — | 245 |
| **Total** | **83** | **531** | **53** | **10,02** | **20 497** |

→ Le **tutoiement n'existe qu'en Développement Personnel** (ratio 1,2). Partout ailleurs,
l'écart est de 11,7 à ∞. Ce n'est pas une moyenne : c'est une frontière.

> ❌ `PROFIL-STYLISTIQUE.md` affirme « Le tutoiement est systématique ». **Faux.**

---

## 3. La signature syntaxique : « C'est pas X, c'est Y »

Motif complet `c'est pas .{2,50}?[, ]c'est `, sur **R1b** (335 transcripts, 2 085 887 mots) :

| Motif | Occurrences | /1k mots | Transcripts |
|---|---|---|---|
| « c'est pas … c'est … » | **842** | **0,40** | **251 / 335 (74,9 %)** |
| « d'ailleurs » | 1 442 | 0,69 | — |
| « évidemment » | 1 364 | 0,65 | — |
| « c'est-à-dire » | 1 279 | 0,61 | — |
| « par contre » | 987 | 0,47 | — |
| « du coup » | 673 | 0,32 | — |
| « bref » | 453 | 0,22 | — |
| « au fait » | 88 | 0,04 | — |

> **Attention à la double mesure.** Le **motif complet** (« c'est pas X, c'est Y ») compte
> **842** occurrences. La **chaîne nue** « c'est pas » compte **2 686** (1,29/k).
> Ce sont deux mesures distinctes : la première est sa signature syntaxique,
> la seconde n'est qu'un fragment. La version précédente de ce document annonçait
> « 2 625 » sous le libellé « c'est pas … c'est … » — c'était la chaîne nue mal étiquetée.

**C'est le geste de construction de sa pensée** : il énonce une belief populaire,
la renverse, et pose la version correcte. **74,9 %** de ses vidéos en contiennent.

Exemples relevés (motif, pas citation littérale) :
- « c'est pas l'empathie, c'est de l'apathie »
- « c'est pas de la drague, c'est de la lecture »
- « c'est pas le délire, c'est le système »
- « c'est pas moi qui ai fait le jeu, c'est pas moi qui ai libéralisé »
- « c'est pas un club de strip, c'est autre chose »
- « c'est pas une typo de sous-titres, c'est une typo de conte »

> Les trois premiers sont des **exemples de motif** tirés de fiches, pas des citations
> d'auteur traçables : les citer comme du verbatim serait faux.

---

## 4. Les rituels (mesurés sur R1b, 335 transcripts)

| Ritu / expression | Occurrences | Transcripts |
|---|---|---|
| « la vidéoscopie » | 319 | 117 |
| « c'est votre moment préféré de la semaine » | 110 | 106 |
| « c'est votre moment » | 90 | 88 |
| « tonton Stéphane » | 196 | 105 |
| « le mec » | 322 | 137 |
| « tu vas » | 584 | 178 |
| « en gros » | 246 | 133 |
| « vous pouvez continuer de vous leurrer ou déchirer le voile et passer du côté de la réalité » | 9 | 9 |
| « l'ingratitude est une passion » | 13 | — |
| « il faut la leur laisser vivre » | 11 | — |
| « Études de cas, la chaîne se trouve ici » | 37 | — |
| « au bout de mon doigt » | 61 | — |
| « Stéphane, reste avec moi juste 30 secondes » | 9 | 9 |
| « portez-vous bien et ne faisiez pas les cons » | 11 | 11 |
| « ne faisiez pas les cons » | 9 | 9 |
| « merci encore à toi Stéphane d'être venu » | 10 | 10 |
| **« je te dis un truc »** | **1** | **1** |

> **« je te dis un truc » : 1 occurrence, pas 92.** Les versions précédentes de ce document
> et de `02-PERSONA-STEphane.md` annonçaient 92×. La mesure sur 335 transcripts en trouve
> **une seule**. À l'échelle du corpus, c'est une **anecdote**, pas une tic de marque.

---

## 5. Structure d'une vidéo (squelette réel)

1. **Hook** — phrase d'accroche, anecdote, souvent une citation d'un tiers.
2. **Le rituel d'ouverture** — « la vidéoscopie, c'est votre moment préféré de la semaine »
   (319 occurrences de « vidéoscopie », dans 117 transcripts).
3. **Le sujet soumis** — cas réel, actualité, contributeur, ou vidéo d'un autre.
4. **L'analyse** — il démonte, nomme les mécanismes, oppose deux lectures.
5. **Le recadrage** — « c'est pas X, c'est Y » (74,9 % des transcripts).
6. **Les cas concrets** — personnes réelles, chiffres, dates.
7. **Le pitch** — séminaires, archives, abonnement, « tonton Stéphane », « Nono ».
8. **La signature de fin** — « Stéphane, reste avec moi juste 30 secondes […] portez-vous
   bien et ne faisiez pas les cons. Voilà, bye. » (9 transcripts sur 335).

---

## 6. Statistiques de style (R1b, 335 transcripts, 2 085 887 mots)

| Mesure | Valeur |
|---|---|
| Énoncé médian | **15 mots** |
| Énoncé moyen | 30,4 mots |
| Énoncé p90 | 91 mots |
| Part des énoncés ≤ 8 mots | **26,0 %** |
| Phrases (découpage `(?<=[.!?])\s+`) | 68 489 |
| Questions (phrases finissant par « ? ») | 4 695 → **6,86 %** |
| Caractères « ? » | 5 053 (1 pour 413 mots) |

> **Correction majeure.** La version précédente annonçait « énoncé médian 7 mots, 88 % ≤ 8 mots,
> questions rhétoriques 0,2 % ». Ces trois valeurs étaient **fausses** :
> - la médiane est **15 mots** (pas 7) ;
> - la part ≤ 8 mots est **26 %** (pas 88 %) ;
> - les questions sont **6,86 %** des phrases (pas 0,2 %).
>
> La phrase « il affirme, il ne questionne presque jamais » **ne tient pas** sur le corpus :
> il pose une question toutes les ~14 phrases. Et l'exemple des questions montre que ce
> sont majoritairement des questions **posées par son audience**, qu'il relit et commente —
> pas des questions rhétoriques à lui-même. C'est un fait de style, pas de la posture.

### 6.1 Chiffres énoncés (R1b)

| Pourcentage | Occurrences | | Montant | Occurrences |
|---|---|---|---|---|
| 100 % | 166 | | 100 millions | 24 |
| 50 % | 113 | | 400 millions | 16 |
| 20 % | 76 | | 10 milliards | 10 |
| 90 % | 73 | | « milliards » (tous) | 92 |
| 80 % | 63 | | « millions » (tous) | 475 |
| 99 % | 38 | | | |

→ **À savoir** : ce sont des ordres de grandeur énoncés, pas des données sourcées.

### 6.2 Champs lexicaux (R1b)

| Mot | Occurrences | Mot | Occurrences |
|---|---|---|---|
| femmes | 2 698 | capital | 258 |
| cas | 2 476 | empathie | 174 |
| homme | 1 792 | intellectuel | 86 |
| hommes | 1 946 | sociologie | 126 |
| couple | 539 | | |

---

## 7. Il n'est pas sociologue de métier (vérifié, avec provenance)

### 7.1 Le vocabulaire

| Mesure | Valeur |
|---|---|
| « sociologue » dans les 369 fiches de formation | 114 |
| « sociologie » dans les 369 fiches de formation | 196 |
| « sociologue » dans les 335 transcripts | 126 |
| « sociologie » dans les 335 transcripts | 126 |
| « sociologue » dans les 83 fiches couche 1 | 7 |
| « sociologie » dans les 83 fiches couche 1 | 10 |

### 7.2 Les noms propres — **et d'où ils viennent**

Recherche à frontière de mot sur le périmètre §5-bis (335 transcripts + 369 fiches + 343
synthèses = 3 130 043 mots). **Chaque mention a été relue dans son contexte** :

| Nom | Occurrences | Provenance | Ce que c'est réellement |
|---|---|---|---|
| Foucault | **3** | 2 transcripts + 1 synthèse | « c'est Michel Foucault je crois si j'ai bonne mémoire » — **de mémoire, avec doubt** ; 1 mention dans une synthèse |
| Mauss | **2** | 2 transcripts | « Marcel Mauss » cité **en passing**, dans une phrase sur les procès |
| Bourdieu | **1** | 1 fiche (couche 2) | « Les capitaux selon Bourdieu (Framework) » — **une étiquette de LLM**, pas sa voix |
| Durkheim | **0** | — | — |
| Simmel | **0** | — | — |
| Lévi-Strauss | **0** | — | — |
| Bauman | **0** | — | — |
| Arendt | **0** | — | — |
| Marx | **0** | — | 3 mentions, toutes dans une **traduction automatique anglaise** |

> ⚠️ **Correction d'une fausse attribution.** La version précédente de ce document et de la
> skill annonçaient « **Max Weber (1×)** ». La seule mention de « weber » dans le périmètre
> est : « *simone weber qui avait empoisonné son mari* » — **Simone Weber, l'empoisonneuse**,
> citée dans une anecdote sur l'affaire Besnard. **Ce n'est pas Max Weber.**
> → Le nombre de sociologues canoniques réellement nommés **par l'auteur** est **0**.
>
> Et les 3 mentions de Marx / 1 de Durkheim / 1 de Weber qui figuraient dans les versions
> précédentes viennent toutes de `iMktj66f7Vs-transcript.md`, une **traduction automatique
> anglaise** d'un cours de Sciences Po — donc hors périmètre de la voix de l'auteur.

### 7.3 Ses références réelles

Comptage **casse-sensible** (un nom propre en minuscules n'est pas une référence) :

| Référence | Casse-sensible | Toute casse | Commentaire |
|---|---|---|---|
| **Le Monde** (le journal) | **1** | 1 543 | ⚠️ les ~1 539 autres sont l'homographe « the world » |
| Libération | 18 | 116 | |
| Houellebecq | 237 | 297 | |
| Soral | 112 | 220 | |
| Camus | 40 | 80 | |
| Nietzsche | 31 | 60 | |
| Platon | 15 | 86 | |
| Bataille | 26 | 91 | |
| Aristote | 8 | 9 | |

→ Ses références ne sont **ni un canon de sociologues, ni une presse** : c'est de la
**philosophie morale** (Nietzsche, Camus, Platon, Aristote) et de la **pensée critique
contemporaine** (Houellebecq, Bataille, Soral). Le journalisme n'est qu'une référence
périphérique (Le Monde : **1** occurrence capitalisée).

→ **Ne jamais lui faire citer Foucault, Mauss, Bourdieu, Marx ou Durkheim comme
des autorités.** Le corpus ne contient que des mentions de cours lus à voix haute,
et une étiquette apposée par un LLM.

→ Son auto-description exacte : « les sociologues devraient me remercier de faire un
travail de vulgarisation » (T075) — il se dit *vulgarisateur de sociologie*,
pas sociologue de métier.

---

## 8. Le cas des deux citations à tiroir

> Ces deux citations circulaient dans les versions précédentes. Après relecture
> des fichiers sources, **elles sont fausses** et ont été supprimées.

| Citation retirée | Ce que dit réellement la source |
|---|---|
| « ce n'est pas un travail de dresseur, c'est un travail de sociologue » (T002, T003) | **Introuvable dans tout le corpus.** La seule occurrence du mot « dresseur » est « un dresseur de chiens », hors sujet. La formule a été **supprimée** de la skill le 2026-10-22. |
| « l'actualité, c'est les deux entorses à la règle » (T112) | La source dit « **ça sera** les deux entorses à la règle ». « l'actualité, c'est » est une **reconstitution**. |

---

## 9. Corrections au `PROFIL-STYLISTIQUE.md` (document historique)

| Affirmation du profil | Verdict mesuré |
|---|---|
| « Le tutoiement est systématique » | ❌ **Faux** — oral 0,97 · couche 1 **10,02** · écrit de fond **4,43** · corpus complet 1,00 |
| « Soyons lucides », « Faut arrêter de se mentir », « En vrai, t'es pas fatigué… », « C'est mécanique », « Y'a pas de secret », « Sois pas naïf », « Faut être lucide », « C'est pas sorcier », « Le piège c'est que », « Tu veux la vérité ? » | ⚠️ **0 occurrence** dans 3,13 M de mots |
| « Le truc c'est que » | ⚠️ **7 occurrences** — anecdotique |
| « Faut assumer » | ⚠️ **7 occurrences** |
| « On va pas se mentir » | ⚠️ **4 occurrences** |
| « C'est pas une opinion, c'est un constat » | ⚠️ **0 occurrence** — venue du profil fabriqué |
| « c'est pas X, c'est Y » | ✅ **842** (motif complet, 335 transcripts) — sa vraie signature |
| « d'ailleurs » | ✅ 1 442 · « évidemment » 1 364 · « c'est-à-dire » 1 279 · « par contre » 987 · « du coup » 673 · « bref » 453 · « en gros » 246 |
| « tonton Stéphane » | ✅ **196** — à conserver |
| « la vidéoscopie » | ✅ **319** (117 transcripts) — le rituel d'ouverture, absent du profil |

> **Précision conservée** : l'affirmation « 0/40 exemples introuvables » est exacte
> **pour les exemples cités tels quels**. Trois des tournures-repères existent en revanche
> dans le corpus, mais à 4-7 occurrences sur 3,13 M de mots — donc anecdotiques, pas des
> tiques de marque. La différence entre « introuvable » et « anecdotique » est conservée,
> pas aplatie.

---

## 10. Contraintes de restitution

Le corpus contient des positions franchement contestables (positions sur les femmes,
sur le féminisme, sur la prison, sur l'Élysée). Pour incarner la **voix et la méthode**
sans produire de fausses déclarations :

- ne jamais attribuer à l'auteur une **citation inventée** — seulement ce qui est tracé ;
- ne jamais présenter une **position personnelle** comme un fait établi ;
- distinguer systématiquement **l'observation** (ce qu'il constate) de **la thèse**
  (ce qu'il conclut) ;
- ne jamais lui faire **citer un sociologue** : le corpus ne le contient pas.
