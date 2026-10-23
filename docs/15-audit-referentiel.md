# Référentiel documentaire — audit

**Audit du référentiel** : `PROFIL-STYLISTIQUE.md`, `CONCEPTS-CLES.md`, `MASTER-INDEX.md`, `INDEX_CROISE_FINAL.md`, `index-complet.md`, `README.md`, `controverses/`, `livres/`+`livres/fiches/`, `formations/`
**Corpus** : `/root/migration-docker-stephane/Bartilabas/formation/StephaneEdouard/` — 1 942 fichiers, 1 819 `.md`
**Corpus de référence pour la voix** : `podcasts/transcripts/final/*-transcript.md` — **324 transcripts, 1 849 730 mots** (c'est la seule source de parole réelle ; tout le reste est du texte dérivé ou généré)
**Méthode** : comptage automatisé par motif regex insensible aux accents sur le corpus de référence, plus recoupement manuel sur `podcasts/syntheses/` (343 fichiers), `formations/` (369 fichiers), `livres/fiches/` (95 fiches actives).

---

## 1. Verdict sur PROFIL-STYLISTIQUE.md

**Verdict global : document inutilisable en l'état pour incarner SE.** Il décrit un locuteur *inventé* — un « coach de séduction cash » tutoiement, qui n'a jamais existé dans ce corpus. La voix réelle de SE est **sociologique,, vouvoyante,bkery structurée**. Les 40 exemples cités sont **mot pour mot absents du corpus (0/40)**.

### 1.1 Structure du document

10 sections de premier niveau, 234 lignes, 9 860 octets.

| § | Titre | Contenu |
|---|---|---|
| I | Ton général | posture « diagnostiqueur », « règle d'or » |
| II | Tics de langage (signature) | tableau 20 lignes : Tique / Fonction / Exemple |
| III | Figures rhétoriques favorites | 10 sous-sections numérotées |
| IV | Structure argumentative type | 5 temps (constat → diagnostic → cadre → action → maxime) |
| V | Références récurrentes | 5 sous-blocs, 27 puces |
| VI | Registre linguistique | 4 niveaux |
| VII | Positionnement épistémologique | 4 « ni… ni… » |
| VIII | Posture de l'auditeur implicite | alter ego masculin |
| IX | Angle d'attaque pédagogique | 4 règles |
| X | Imprégnation pratique | 8 consignes de calibrage |

### 1.2 Inventaire quantifié

| Élément | Annoncé / compté | Vérifié |
|---|---|---|
| Tiques de langage listées | 20 (`MASTER-INDEX.md` §4.2 dit « 20 tournures signatures ») | **20 lignes de tableau** ✔ |
| Figures rhétoriques | 10 | **10 sous-sections `### N.`** ✔ |
| Structure argumentative | 5 temps | **5** ✔ |
| Registres | 4 | **4** ✔ |
| Exemples / citations (guillemets doubles) | — | **73 chaînes distinctes** (40 dans les sections II/III/IV = les exemples « parlés ») |
| Références récurrentes | — | **27 puces** (stratégie 4, philosophie 8, psychanalyse 3, littérature 5, pop 4, histoire 3) |
| Consignes mode d'emploi | — | **8** (§X) |

La **structure du document est conforme à son annonce**. C'est le contenu qui ne l'est pas.

### 1.3 Test décisif : les 40 exemples « parlés » n'existent nulle part

Recherche verbatim (normalisation accents + espaces) sur les 4 corpus (transcripts 1 849 730 mots, synthèses 146 948, formations 1 135 653, fiches 31 735) :

> **40 exemples sur 40 introuvables (0/40).**

Exemples vérifiés absents (extrait + comptage sur le corpus entier) :

| Extrait du profil | Occ. transcripts | Occ. synthèses | Occ. formations |
|---|---|---|---|
| « En vrai, t'es pas fatigué, t'es fainéant. » | 0 | 0 | 0 |
| « Soyons lucides : elle te teste. » | 0 | 0 | 0 |
| *C'est pas de la drague, c'est de la lecture.* (paraphrase non sourcée) | 0 | 0 | 0 |
| *Faut être lucide : tu cadres pas.* (paraphrase non sourcée) | 0 | 0 | 0 |
| *Mec, t'es à côté de la plaque.* (paraphrase non sourcée) | 0 | 0 | 0 |
| *La séduction c'est comme le basket : si t'as pas le fondamental, tu marques pas.* (paraphrase non sourcée) | 0 | 0 | 0 |
| *La confiance, c'est pas croire en soi, c'est l'avoir prouvé.* (paraphrase non sourcée) | 0 | 0 | 0 |
| *Le cadre c'est pas un concept, c'est une chaise. T'es assis dessus ou tu la donnes.* (paraphrase non sourcée) | 0 | 0 | 0 |
| *Un mec qui cadre, c'est un mec qui protège. Un mec qui protège, c'est un mec qu'on suit.* (paraphrase non sourcée) | 0 | 0 | 0 |
| *C'est pas la chance. C'est ton cadre. T'en as pas.* (paraphrase non sourcée) | 0 | 0 | 0 |

**C'est le mode de défaillance central du document** : les 73 chaînes entre guillemets sont des *fabrications rhétoriques* écrites pour illustrer une thèse, pas des citations. Un assistant qui s'imprégne de ce document apprend une voix qui n'existe nulle part dans le corpus.

### 1.4 Les tiques eux-mêmes : 10 sur 21 sont totalement absents

Fréquence mesurée sur les 324 transcripts (1 849 730 mots), normalisation insensible aux accents :

| Tique (§II) | transcripts | Fréq. /10 000 mots | Verdict |
|---|---|---|---|
| « Regarde » | 1 255 | 0,68 | **Confirmé** (mais 84 des occurrences sont « regarde » de gestion du regard, pas l'injonction) |
| « Mec » | 585 | 0,32 | Confirmé, **mais 90 % en position tierce** (« un mec qui… », « le mec… ») — jamais en apostrophe |
| *C'est pas X, c'est Y* (paraphrase non sourcée) | 145 | 0,08 | Confirmé comme patron syntaxique |
| « C'est comme ça » | 152 | 0,08 | Confirmé |
| « Frère » | 89 | 0,05 | Confirmé |
| « En vrai, » | 46 | 0,02 | Confirmé mais **très rare** (1 pour 40 000 mots) |
| *Le truc c'est que* (paraphrase non sourcée) | 7 | 0,00 | Très rare |
| *Faut assumer* (paraphrase non sourcée) | 8 | 0,00 | Très rare |
| *T'es dans…* (paraphrase non sourcée) | 10 | 0,01 | Très rare |
| « On va pas se mentir » | 4 | 0,00 | Très rare |
| « Je vais te dire un truc » | 1 | 0,00 | Quasi inexistant |
| « Soyons lucides » | 0 | 0 | **ABSENT** |
| « Faut arrêter de se mentir » | 0 | 0 | **ABSENT** |
| « Faut être lucide » | 0 | 0 | **ABSENT** |
| « C'est mécanique » | 0 | 0 | **ABSENT** |
| « Et ça, c'est pas une opinion, c'est un constat » | 0 | 0 | **ABSENT** |
| *Tu veux la vérité ?* (paraphrase non sourcée) | 0 | 0 | **ABSENT** |
| *Sois pas naïf* (paraphrase non sourcée) | 0 | 0 | **ABSENT** |
| *Le piège c'est que* (paraphrase non sourcée) | 0 | 0 | **ABSENT** |
| « Y'a pas de secret » | 0 | 0 | **ABSENT** |
| « C'est pas sorcier » | 0 | 0 | **ABSENT** |

**10 des 20 tiques du tableau sont introuvables, 7 sont anecdotiques (≤ 10 occ.), 3 seulement sont réellement signaturaux** (« Regarde », « Mec », « C'est pas X c'est Y » — et « Mec » dans le mauvais sens grammatical).

### 1.5 La contradiction majeure : tutoiement vs vouvoiement

Le profil §I pose « Le tutoiement est systématique » et §X règle 1 « **Tutoie systématiquement**, vouvoiement = perte immédiate ».

Mesure sur le corpus réel :

| Corpus | Ratio |
|---|---|
| **324 transcripts** | **VOUS 18 253 occ. / TU 16 359 occ. → 53 % vouvoiement, 47 % tutoiement** |
| Fichiers dominés par le vouvoiement | **281 / 324 transcripts (87 %)** |
| Fichiers dominés par le tutoiement | 13 / 324 (4 %) |
| **369 formations** (voix écrite de SE) | **256 à dominante VOUS, 113 à dominante TU** |

La règle 1 du mode d'emploi est **l'inverse de la réalité**. L'erreur serait d'un assistant qui dirait « tu » à un auditeur de 87 ans, ou qui abolirait le vouvoiement alors que SE l'emploie massivement à l'écrit comme à l'oral.

### 1.6 Les figures rhétoriques : laquelle survit ?

| Figure | Verdict |
|---|---|
| 1. Analogie sportive | **Partiellement vraie mais surdimensionnée** — 109/324 transcripts (34 %) contiennent ≥1 terme sportif, 262 occurrences au total (0,14 /10 000 mots). SE dit lui-même « je ne joue pas au basket ». Le profil claims « quasi systématique » : **exagéré d'un facteur ~3**. |
| 2. Citation littéraire/philosophique | **Faux dans son contenu, vrai dans son principe.** Sur 8 auteurs listés : Houellebecq 54 occ. ✔, Lacan 34 ✔, Platon 22 ✔, Nietzsche 16 ✔, Freud 5 ✔, Girard 4 ✔, Schopenhauer 3 ✔, Sun Tzu 2 ✔ — mais **Marc Aurèle 0, Jung 0, Dantec 0, Bourdieu 0, Clausewitz 0, Épicure 0, Héraclite 0, Sénèque 0**. La pop culture annoncée est **quasi inexistante** : Peaky Blinders 0, The Wire 0, Breaking Bad 0, Gladiator 0, Esprits criminels 0, Dexter 0 (Scarface 4, Le Parrain 7). |
| 3. Contre-exemple | Vrai comme geste, mais c'est un procédé d'analyse de cas, pas une figure SE distinctive. |
| 4. Retournement | Vrai — mais le retournement réel de SE est **statistique/sociologique**, pas rhétorique : il retourne un chiffre. |
| 5. Citation pop-culture | **Faux** (0 occurrence pour 6 des 6 séries/films cités) |
| 6. Maxime | Vrai comme procédé (SE conclut souvent par une formule) — mais les 3 « maximes » citées sont inventées. |
| 7. Injonction | Vrai, mais rare (imprératif peu fréquent) |
| 8. Parallélisme syntaxique | **Rare** — le style réel est *prose*, pas phrases martelées. 32 mots/phrase en moyenne. |
| 9. Métonymie | **Faux** — 0 occurrence de la métonymie « objet quotidien » dans le corpus. |
| 10. Apostrophe directe | Vrai (interpellation de l'auditeur) mais **souvent au vous**. |

### 1.7 La structure argumentative réelle (contredit §IV)

Le profil impose un schéma **CONSTAT → DIAGNOSTIC → CADRE → ACTION → MAXIME** en 5 temps.

La structure réelle, mesurée :

- **Numérotation explicite** : 10 568 occurrences de « `1. ` / `2. ` … » sur 324 transcripts → SE **structure ses propos en listes numérotées**, mécanisme totalement absent du profil.
- **Moyenne 32 mots/phrase** (médiane transcript 4 671 mots / 74 phrases).
- **Codes d'énoncé récurrents** (occurrences) : « bon » 3 282 · « voilà » 2 827 · « il faut » 2 007 · « d'ailleurs » 1 312 · « c'est-à-dire » 1 268 · « et donc » 853 · « ce n'est pas » 692 · « du coup » 549 · « moi je » 1 292 · « en gros » 170 · « ce que je veux dire » 120 · « vous allez me dire » 136 · « il se trouve que » 52 · « objectivement » 57 · « concrètement » 54 · « autrement dit » 53 · « premièrement » 80.
- **Interpolation statistique** : 380 occurrences de marqueurs chiffrés (chiffres/sondages/statistiques/calculatrice), 341 de « sociolog… », 102 de « terrain ».
- **Ritournelle d'émission** : « La vidéoscopie » dans **138/324 transcripts (43 %)** — *« La vidéoscopie, c'est votre moment préféré de la semaine »* — marqueur identitaire majeur, totalement absent du profil.

### 1.8 Les *références récurrentes* (paraphrase non sourcée) (§V) : ce qui est vrai et ce qui est faux

| Annoncé | Corpus réel | Verdict |
|---|---|---|
| Nietzsche, Schopenhauer, Platon, Lacan, Houellebecq, Freud, Girard, Sun Tzu | présents (2 à 54 occ.) | **Solvable**, mais l'affirmation *SE convoque *régulièrement** (paraphrase non sourcée) est fausse : Lacan 34/1 849 730 mots, Sun Tzu 2. |
| Marc Aurèle, Épictète, Épicure, Héraclite, Sénèque, Clausewitz, Bourdieu, Dantec, Ellis, Jung | **0 occurrence chacun** | **Inventé** |
| Peaky Blinders, The Wire, Breaking Bad, Gladiator, Esprits criminels, Dexter | **0 occurrence chacun** | **Inventé** |
| Alexandre, Napoléon (19/16 occ.), Hannibal, Patton (0) | partiellement vrai | — |
| Sports : NBA, NFL, UFC (1), échecs (24), poker (8), muscu (44) | réel mais marginal | Surdimensionné |

### 1.9 Les MANQUES du profil (par ordre de gravité)

1. **La posture de sociologue statisticien** — la moitié de l'identité réelle de SE. Absente.
2. **Le vouvoiement** — voir §1.5. Absent.
3. **La structure en listes numérotées** — 10 568 occurrences. Absente.
4. **La ritournelle « La vidéoscopie »** — 138/324 transcripts. Absente.
5. **La *matin / après-midi*** — le corpus de formations est organisé en deux sessions (« X – matin » / *X – après-midi* (paraphrase non sourcée)) : 51 paires. Le profil ignore totalement cette architecture.
6. **Le vocabulaire réel** : capital (383), agent/agency (128), rapport de force (143), disposition (175), capitalisme (102), terrain (102), sélection (38), légitimité (73), tabou (38), reproduction (47), emprise (43), sélectif/KO (113). Aucun n'apparaît dans le profil. À l'inverse, les notions socles du profil (« cadre » comme limite, « game », « leadership situationnel », « pattern ») sont **marginales ou introuvables** dans la parole réelle :
 - « cadre » : 320 occurrences dans les transcripts, mais analyse de contexte → **84 en sens ordinaire (cadrage/photo/cadreur), 150 indéterminés, seulement 3 en sens doctrinal (limites/règles)**. Le concept n°1 de `CONCEPTS-CLES.md` est un **mot courant** dans la parole de SE, pas son concept-clé.
 - « game » : 89 occurrences mais **0 dans les synthèses**, 3 dans les formations.
 - « pattern » : **2 occurrences** dans tout le corpus de référence. « mécanique » : 96 occ. mais le mot est surtout *mécanique automobile* (SE est ingénieur mécanique automobile !) — « mon diplôme d'ingénierie mécanique automobile ».
 - « leadership » : 3 occurrences dans 324 transcripts (84 dans les synthèses, qui sont du texte généré). Le mot est partout dans les *titres de formations*, presque jamais dans la *parole*.
7. **Le périmètre thématique réel**, absent du profil qui se limite quasi exclusivement à la séduction/couple : dans les transcripts → enfance/éducation 233/324 (72 %), couple 261 (81 %), économie 118 (36 %), politique France 152 (47 %), islam 106 (33 %), immigration/racisme 99 (31 %), trans/LGBT 73 (23 %), COVID 40 (12 %). Le profil ne dit rien de la politique, de la religion, de l'immigration, du journalisme.
8. **Les garde-fous** : le profil ne dit rien du fait que SE se présente en **sociologue de terrain formé en sciences sociales** (« c'était mon premier métier », « les sondages un petit peu complexes chez SOFR »), ni de ses **citations** : *comme disait les dits chevaliers de la Palès* (paraphrase non sourcée) (souvent), Sénèque, Moravia.
9. **Les managing du doute** : les marqueurs « à vérifier », « il me semble », « je ne connais pas l'affaire » sont **réels** dans le corpus (« je n'ai aucun avis », 98 occ. de « à mon sens »). Le profil §X règle 7 les interdit explicitement (*Aucune précaution oratoire* (paraphrase non sourcée)). **Contredit par le corpus.**

### 1.10 RECOMMANDATION CONCRÈTE — section par section

| § | Action | Contenu à écrire |
|---|---|---|
| **I. Ton général** | **RÉÉCRIRE** | Remplacer « tutoiement systématique » par : *« Vouvoiement par défaut (53 % des occurrences, 87 % des transcripts dominés par le vous) ; tutoiement reserved aux apartés, aux citations de tiers et aux moments d'indignation »*. Ajouter la posture statisticienne. |
| **II. Tics (20)** | **REFAIRE À ZERO** | Nouvelle table de 20 tiques **mesurés** : `bon` (3 282), `voilà` (2 827), `il faut` (2 007), `d'ailleurs` (1 312), `c'est-à-dire` (1 268), `et donc` (853), `ce n'est pas` (692), `moi je` (1 292), `du coup` (549), `bref` (413), `en gros` (170), `si vous voulez` (182), `ce que je veux dire` (120), `vous allez me dire` (136), `en effet` (35), `autrement dit` (53), `objectivement` (57), `concrètement` (54), `premièrement` (80), `il se trouve que` (52). **Chaque exemple doit être un verbatim avec son fichier source.** |
| **III. Figures (10)** | **RÉÉCRIRE** | Remplacer la pop-culture (0 occ.) par les figures réelles : **statistique comme retournement** (380 occ.), **analogique par « c'est comme »** (458 occ.), **énumération numérotée** (10 568), **question rhétorique** (5 005), **construction causale « parce que »** (4 040), **incise autoritaire** (« permettez-moi », « ne me dites pas »), **digression marquée** (« d'ailleurs »), **reformulation** (« c'est-à-dire », « autrement dit »). |
| **IV. Structure** | **RÉÉCRIRE** | Nouveau schéma à 6 temps, calé sur la parole réelle : **(1) accroche/ritournelle ou mise en situation chiffrée → (2) « bon » / cadrage du sujet → (3) développement en listes numérotées → (4) digression « d'ailleurs » / cas concret → (5) conclusion operative (« il faut… ») → (6) pivot ou ouverture**. Supprimer le « cadre d'analyse » comme étape 3 (le mot n'est pas doctrinal chez SE) et la « maxime » comme étape 5 (la clôture réelle est une consigne ou un constat). |
| **V. Références** | **CORRIGER** | Supprimer les 12 références à 0 occurrence (Marc Aurèle, Épictète, Épicure, Héraclite, Sénèque, Clausewitz, Bourdieu, Dantec, Ellis, Jung, les 6 séries/films pop). Ajouter : Lacan (34), Platon (22), Nietzsche (16), les stratèges (Alexandre 76, Napoléon 19), les Voiries (Sénèque cité dans une formation), Moravia (*aurait dit Moravia* (paraphrase non sourcée)), le de la_Manager. Mentionner que les références sont **plus discursives que savantes** : le podcast est un commentaire d'actualité, pas un cours de philosophie. |
| **VI. Registre** | **REFAIRE** | 4 niveaux : (1) **didactique-socle** « on va voir » / « laissez-moi vous expliquer » / « premièrement » (le plus fréquent) ; (2) **statistique** « d'ailleurs » / « le chiffre » ; (3) **indigné** « bon » / « voilà » ; (4) **argoté savant** : capital, agent, disposition, rapport de force, sélection, tabou. Supprimer « wesh », « no offense », « j'te dis ça entre nous » (0 occurrence). |
| **VII. Épistémologie** | **CORRIGER** | « Ni psychologue, ni coach, ni gourou » → ajouter : « Ni vulgarisateur de développement personnel, ni sociologue académique : il est *commentateur de société qui outille* ». Corriger « lucide et prescriptif » → « descriptif, analytique, et prescriptive seulement sur les usages relationnels ». |
| **VIII. Auditeur** | **À RÉÉCRIRE** | L'auditeur réel n'est pas un « alter ego masculin immature » : les transcripts s'adressent à un public **masculin, adulte,Deployment payé, sometimes hostile** (152 transcripts mentionnent « Stéphane Édouard », 10 « monsieur Edouard »). Il y a une communauté, pas un élève. |
| **IX. Angle pédagogique** | **GARDER + ÉTENDRE** | Les 4 règles sont justes (*pas de théorie sans exemple* (paraphrase non sourcée), *pas d'exemple sans diagnostic* (paraphrase non sourcée), *pas de diagnostic sans action* (paraphrase non sourcée), *pas d'action sans cadre temporel* (paraphrase non sourcée)) — mais le corpus est **à 30 % de cas dinked** (« d'ailleurs », « ce qui s'est passé », « le cas de… »). Ajouter : « chaque affirmation structurante est adossée à un chiffre ou à un cas nommé ». |
| **X. Mode d'emploi** | **RÉÉCRIRE** | Règle 1 : « vouvoiement par défaut ». Règle 3 : « 1 tique réel toutes les 8-10 phrases ». Règle 5 : « 1 statistique ou 1 cas nommé par réponse ». Règle 7 : **à supprimer** (« aucune précaution oratoire ») — le corpus contient 98 « à mon sens », 3 « permettez-moi », et des mises en garde explicites (« je n'ai aucun avis. Voilà. Point. »). Règle 8 : remplacer « le mépris est banni » par *le mépris des personnes n'est jamais utilisé ; le mépris des comportements et des idées est la norme (692 « ce n'est pas » + 238 occurrences de *harceler/dégradant* (paraphrase non sourcée))*. |
| **+ NOUVEAU §XI** | **À CRÉER** | « La voix en situation : 6 extraits verbatim annotés (un par registre), tous tirés de `podcasts/transcripts/final/` avec le nom du fichier. » C'est la section la plus rentable : 6 citations authentiques valent mieux que 73 fabrications. |

---

## 2. Verdict sur CONCEPTS-CLES.md

**Verdict global : structure conforme, contenu non sourcé.** Même défaut que le profil, mais moins grave sur les *comptages* (qui sont partiellement vérifiables) et plus grave sur les *définitions* (qui décrivent un système conceptuel qui n'est pas celui du corpus).

### 2.1 Structure et comptages

| Élément | Compté | Attendu (MASTER-INDEX §4.1) |
|---|---|---|
| Concepts numérotés | **20** | *20 concepts majeurs cartographiés* (paraphrase non sourcée) ✔ |
| Blocs *Définition SE* (paraphrase non sourcée) | 20 | ✔ |
| Blocs *Pourquoi central* (paraphrase non sourcée) | 20 | ✔ |
| Blocs *Formules SE typiques* (paraphrase non sourcée) | 20 | ✔ |
| Blocs *Concepts liés* (paraphrase non sourcée) | 20 | ✔ |
| Lignes *Occurrences* (paraphrase non sourcée) | 11 (sur 20) | — **9 concepts n'ont aucun compteur** |
| Chaînes entre guillemets (formules) | **58** | — |
| Section finale | *LIENS TRANSVERSES* (paraphrase non sourcée) : 17 combinaisons | ✔ |

**Anomalies structurelles** : le document annonce en tête *Sources analysées : 343 synthèses, 191 formations, 89+ fiches* (paraphrase non sourcée) → **191 formations est faux** (le corpus en compte 369) et « 89+ fiches » est faux (95 actives). Le document décrit un état antérieur du corpus.

### 2.2 Les formules : 0/39 vérifiables

Recherche verbatim sur les 4 corpus des 39 « Formules SE typiques » (2 à 3 par concept) :

> **39/39 introuvables.**

| Formule | Verdict |
|---|---|
| « Sois lucide : si t'as pas de cadre, elle en pose un pour toi. » | 0 occurrence |
| « Le cadre, c'est pas de la rigidité, c'est de la tenue. » | 0 |
| « T'es pas une femme, arrête de te comporter comme une. » | 0 |
| « La séduction, c'est 80% présence, 20% technique. » | 0 |
| « Le talent, c'est 10%. Le réseau, c'est 90%. » | 0 |
| *L'amour est un verbe, pas un état.* (paraphrase non sourcée) | 0 |
| *L'estime de soi, c'est du discours. La confiance, c'est du muscle.* (paraphrase non sourcée) | 0 |
| *Un manipulateur, c'est pas un méchant. C'est un mécanicien. Il utilise tes failles comme leviers.* (paraphrase non sourcée) | 0 |
| « Poser une limite, c'est gratuit. La tenir, c'est payant. » | 0 |
| « C'est pas un événement, c'est un pattern. Trois occurrences, c'est plus un hasard. » | 0 |
| « Tactique sans stratégie, c'est du bruit. Stratégie sans tactique, c'est un PowerPoint. » | 0 |
| « Si t'as pas 10 mecs qui décrochent au 3e son, t'as pas de réseau, t'as des contacts. » | 0 |
| « La confiance en soi, c'est pas croire en soi, c'est savoir qu'on a fait ses preuves. » | 0 |

Aucune n'est balancée. Les concepts 2, 3, 5, 9, 11, 12, 13, 14, 15, 16, 17, 19, 20 sont **entièrement adossés à des formules inventées**.

### 2.3 Les compteurs d'occurrences : partiellement vérifiables

Recalcul sur `podcasts/syntheses/` (343 fichiers), mode *nombre de fichiers contenant le terme* (paraphrase non sourcée) :

| Concept | Annoncé | Réel (fichiers) | Verdict |
|---|---|---|---|
| cadre | 45 | **45** | ✔ exact |
| vérité | 20 | **20** | ✔ |
| mécanique | 20 | **20** | ✔ |
| pattern | 17 | **17** | ✔ |
| confiance | 17 | **17** | ✔ |
| schéma | 16 | **16** | ✔ |
| statut | 15 | **15** | ✔ |
| hiérarchie | 12 | **12** | ✔ |
| pervers | 7 | **7** | ✔ |
| ascension | 7 | **7** | ✔ |
| narcissique | 3 | **3** | ✔ |
| manipul- | 41 | 50 | **Écart +9** |
| stratégie | 35 | 41 | Écart +6 |
| séduction | 20 | 27 | Écart +7 |
| masque | 19 | 14 | Écart −5 |
| estime | 18 | 23 | Écart +5 |
| limites | 15 | 25 | **Écart +10** |
| féminité | 12 | **101** | **Écart +89 (×8)** |
| masculinité | 10 | **76** | **Écart +66 (×7,6)** |
| ego | 9 | 2 | **Écart −7** |
| lucidité | 6 | 7 | Écart +1 |
| game | 6 | **0** | **Faux** |
| relations H-F (32 formations) | 32 | 32 ✔ | ✔ (c'est un compteur de formations, pas d'occurrences) |
| *leadership (1 en keyword mais transversal)* (paraphrase non sourcée) | 1 | — | Le mot-clé n'existe pas dans `_index_keywords.json` : l'aveu est dans le document |

**Bilan : 12 compteurs exacts sur 26 testés, 1 faux avoué.** Les 6 concepts les mieux documentés sont ceux dont le mot est rare et non ambigu. Les écarts massifs sur féminité/masculinité montrent que les chiffres n'ont pas été recalculés après coup.

### 2.4 Qualité des définitions : le système conceptuel décrit n'est pas celui du corpus

Test de plausibilité conceptuelle sur la **parole réelle** (324 transcripts) :

| Concept | Occ. transcripts | Verdict |
|---|---|---|
| LE CADRE | 320 (dont **84 sens ordinaire**, 150 indéterminés, **3 sens doctrinal**) | **Concept surévalué** — le mot est courant, pas doctrinal |
| MASQUE | 141 (dont « masque » = objet physique : masques de voiture, « faire un masque ») | **Surévalué** |
| PATTERN | **2** | **Inexistant dans la parole** (17 dans les synthèses = texte généré) |
| MECHANIQUE | 96 (dont « mécanique automobile ») | **Confusion lexicale** |
| MASCULINITÉ / FÉMINITÉ | 1 161 | **Sous-évalué** — c'est le vrai centre de gravité (avec le couple : 626) |
| COUPLE | 626 | **Sous-évalué** (le doc le place en 7ᵉ) |
| RÉSEAU | 546 | **Sous-évalué** (doc : 15ᵉ) |
| LIMITES | 613 | **Sous-évalué** |
| LEADERSHIP | **3** (transcripts) / 84 (synthèses générées) | **Inventé comme concept de parole** — il n'existe que dans les titres de formations |
| CHARISME | 35 | Marginal |
| GAME | 89 dont 0 en synthèses | Marginal |
| ASCENSION SOCIALE | 21 | Marginal |
| AFFIRMATION DE SOI | 38 | Marginal |
| RED FLAG | 1 | **Absent** |
| PRODUCTIVITÉ / DISCIPLINE | 57 | Marginal |

**Les 6 concepts réellement structurants du corpus, absents de `CONCEPTS-CLES.md`** :

1. **LE CAPITAL (social/économique/culturel)** — 383 occ. Le concept central de SE.
2. **L'AGENT / L'AGENCY** — 128 occ. (l'individu comme agent rationnel dans un marché).
3. **LE RAPPORT DE FORCE / LA DISPOSITION** — 143 + 175 occ.
4. **LA SÉLECTION (sexuelle/sociale) et LE SÉLECTIF** — 38 + 113.
5. **LA LÉGITIMITÉ / LE STATUT / LE TABOU** — 73 + 68 + 38.
6. **L'EMPRISE** — 43 occ. (le vrai nom de ce que le profil appelle « manipulation »).

Et le **vrai système de pensée** que le document rate : SE pense en **capital / agent / sélection / dispositif**, pas en **cadre / game / leadership situationnel**.

### 2.5 MANQUES de CONCEPTS-CLES.md

1. Les 6 concepts du §2.4 ci-dessus.
2. **Les dimensions politiques/religieuses/immigration** : 47 % des transcripts sont politiques, 33 % islam, 31 % immigration/racisme. Le document est 100 % « vie de homme » — hors-sol.
3. **Le vocabulaire de la recherche** : sociologie quantitative, capital, disposition, tabou, reproduction, emprise, agency, sélection,ko.
4. **Le périmètre Formation** : rien sur le dispositif *matin / après-midi* ni sur la logique *catalogue MAT Consulting* (paraphrase non sourcée) (la source des formations).
5. **Les sources de citation réelles** : Seneca, Moravia, Lacan, Platon, Nietzsche — et le fait que la citation est souvent **attribuée oralement** (« comme disait les dits chevaliers de la Palès »).

### 2.6 RECOMMANDATION CONCRÈTE

| § | Action |
|---|---|
| **En-tête** | Corriger : « Sources analysées : 343 synthèses, **369** formations, **95** fiches de lecture actives ». |
| **Concepts 1 (cadre), 10 (masque), 13 (mécanique/pattern), 16 (charisme), 19, 20** | **À réécrire ou à supprimer** : le pattern n'existe pas dans la parole (2 occ.), le leadership n'existe pas comme concept de parole (3 occ.), le charisme est marginal (35 occ.). |
| **Concepts 2, 5, 7, 15, 12** | **Remonter et réagrandir** — masculinité/féminité (1 161), couple (626), réseau (546), limites (613) sont les vrais poids lourds, pas les concepts 7, 15. |
| **Nouveaux concepts 21-28** | CAPITAL · AGENT/AGENCY · RAPPORT DE FORCE & DISPOSITION · SÉLECTION & SÉLECTIF · LÉGITIMITÉ/TABOU · EMPRISE (remplace « manipulateurs ») · LA VIDÉOSCOPIE (identité d'émission) · LE STATUT D'OUVRAGE (la posture de l'analyste qui ne raconte pas sa vie). |
| **Toutes les *Formules SE typiques* (paraphrase non sourcée)** | **Supprimer ou sourcer.** Règle à écrire en tête du document : **Toute formule de ce document doit être un verbatim d'un fichier du corpus, avec le chemin. En l'absence de verbatim, la formule est interdite.* (paraphrase non sourcée)* |
| **Toutes les lignes *Occurrences* (paraphrase non sourcée)** | Recalculer sur la même méthode (fichiers de `podcasts/syntheses/` contenant le terme) et l'indiquer dans la ligne. Ajouter un compteur *occ. transcripts* (paraphrase non sourcée) qui est la vraie base. |
| **LIENS TRANSVERSES** | Refaire : racine = **CAPITAL**, non CADRE. |
| **+ NOUVEAU** | Une section *Ce que le corpus ne dit pas* (paraphrase non sourcée) : les zones muettes (fabrication d'exemples non vérifiés) doivent être déclarées, pas comblées par invention. |

---

## 3. Audit des index (MASTER-INDEX, INDEX_CROISE_FINAL, index-complet, README)

### 3.1 MASTER-INDEX.md — le meilleur document du lot

| Compteur annoncé | Annoncé | Réel | Verdict |
|---|---|---|---|
| Fiches de formation | 369 | **369** | ✔ |
| … racine | 181 | **181** | ✔ |
| … 10 sous-dossiers | 188 | **188** | ✔ |
| Fiches de lecture `livres/fiches/` | 99 | **99** | ✔ (dont 4 `.DEPRECATED` → **95 actives**) |
| Synthèses podcasts | 343 | **343** | ✔ |
| Transcripts finaux | 648 | **648** | ✔ (mais 648 = **324 transcripts + 324 synthèses** mélangées dans le même dossier — le libellé *transcripts* (paraphrase non sourcée) est trompeur) |
| Recaps de transcripts | 324 | **324** | ✔ |
| Documents controverses | 2 | **2** | ✔ (nombre juste, contenu vide) |
| Documents annexes | 14 | 15 | Écart +1 (`livres/` contient 12 fichiers + 1 sous-dossier `fiches/`) |
| Top 20 thématiques | 20 lignes | 10/20 exacts en mode « fichiers de synthèses » | **Partiellement faux** (voir §1.3 du §2) |
| `livres/livres-recommandes.md` « 79 titres listés » | 79 | **80** | Écart +1 (le fichier annonce lui-même « ~80 ») |
| Couverture livres « ~85 %, 14 titres sans fiche » | ~85 % | **71/80 = 89 %** (9 sans fiche) | **Sous-estimé** — le corpus est mieux couvert que dit le doc |
| « +12 fiches Phase 3 » | 12 | **9/12 présentes** sous le nom exact annoncé | 3 introuvables : `…-l-amant-de-lady-chatterley-lawrence.md`, `…-soumission-houellebecq.md`, `…-extension-du-domaine-de-la-lutte-houellebecq.md`, `…-le-mythe-de-la-virilite-collectif.md` — mais les **équivalents existent** sous d'autres slugs (`fiche-lecture-soumission-michel-houellebecq.md`, `fiche-lecture-extension-domaine-lutte-houellebecq.md`, `fiche-lecture-amant-de-lady-chatterley-lawrence.md`, `fiche-lecture-l-amant-de-lady-chatterley-dh-lawrence.md` → **4 doublons de fait**) |
| CONCEPTS-CLES *20 concepts* (paraphrase non sourcée) | 20 | 20 | ✔ |
| PROFIL *20 tournures signatures* (paraphrase non sourcée) | 20 | 20 | ✔ (nombre juste, contenu faux) |
| PROFIL *10 figures rhétoriques* (paraphrase non sourcée) | 10 | 10 | ✔ |
| PROFIL *structure 5 temps / 4 registres* (paraphrase non sourcée) | 5 / 4 | 5 / 4 | ✔ |
| Plan d'action §5 | 4 items « ✅ FAIT » | les 4 artefacts existent | ✔ |
| Statut Phase 3 / tag de commit | — | — | `git` absent du dossier, statut **non vérifiable** |

**Verdict honnêteté MASTER-INDEX : 8/10.** Les compteurs de volume sont exacts et vérifiables un à un. C'est le document de référence le plus fiable du corpus. Réserves : le top-20 est partiellement faux, *648 transcripts* (paraphrase non sourcée) est un libellé trompeur, et les chiffres de couverture sont approximatifs.

### 3.2 INDEX_CROISE_FINAL.md — excellent, avec un écart mesurable

| Compteur | Annoncé | Recalculé | Verdict |
|---|---|---|---|
| Formations enrichies | 369/369 | **369/369** (toutes ont ≥1 lien) | ✔ |
| Synthèses citées | 225/343 | **228/343** | Écart +3 |
| Fiches citées | 95/99 | **94/95 actives** (2 actives non citées : `renaissance-de-lamour-courtois-deleuze.md`, `soie-baricco.md`) | ✔ |
| Top 10 synthèses (n° de formations liées) | 147, 97, 92, 91, 77, 76, 75, 71, 70, 69 | **147, 97, 92, 91, 77, 76, 75, 71, 70, 69** | ✔ **10/10 exacts** |
| Top 8 fiches | 166, 153, 95, 73, 68, 62, 60, 54 | 181, 153, 95, 74, 68, 62, 60, 54 | 6/8 exacts ; `le-charme-discret-des-connards` **+15**, `soral-contre-les-femmes` **+1** |

**Verdict honnêteté : 9/10.** Document court, sans structural, chiffres vérifiables. C'est le **seul index dont les chiffres de croisement résistent à un recalcul indépendant**.

### 3.3 index-complet.md — obsolète et malhonnête

| Annonce | Réel | Verdict |
|---|---|---|
| *187 formations cataloguées (formations/)* (paraphrase non sourcée) | **369** | ❌ **Faux (×0,5)** |
| *formations/ : 142+ fiches prêtes à être enrichies* (paraphrase non sourcée) | **369, toutes enrichies** | ❌ Faux, et périmé (daté 30/05, antérieur à la Phase 3) |
| *livres/ : 68+ fiches de lecture terminées* (paraphrase non sourcée) | **95 actives** | ❌ Faux |
| *60+ livres recommandés avec fiches* (paraphrase non sourcée) | 80 recommandés / 95 fiches | △ Correct en ordre de grandeur |
| *291 vidéos YouTube uniques* (paraphrase non sourcée) | non vérifiable (aucun `all_video_ids.json` dans le dossier) | **Invérifiable** |
| *177 épisodes Spotify* (paraphrase non sourcée) | `podcasts/episodes/` ne contient **1 seul** fichier (`episode-list.md`) | ❌ Non corroboré |
| *Le deep training est maintenant complet* (paraphrase non sourcée) | 53/369 fiches de formation (14,4 %) ont un corps vide ; le profil de voix est faux | ❌ **Affirmation fausse** |
| *Commité et pushé sur main* (paraphrase non sourcée) | pas de `.git` dans le dossier | **Invérifiable** |

**Verdict honnêteté : 3/10.** C'est un document de clôture de mission daté du 30/05, jamais mis à jour après la Phase 3. Il contredit `MASTER-INDEX.md` (169 fichiers) et `README.md` (290+). **Trois index du corpus se contredisent mutuellement sur les mêmes chiffres** : 187 / 290+ / 369.

### 3.4 README.md (racine) — daté, et annonce des choses non faites

| Annonce | Réel | Verdict |
|---|---|---|
| *Phase 2 CLÔTURÉE — 324 synthèses générées* (paraphrase non sourcée) | 324 recaps + 343 synthèses | ✔ (mais la phase 3 a produit 369 formations) |
| *290+ formations enrichies depuis les transcripts* (paraphrase non sourcée) | 369 | Vrai mais **sous-évalué** |
| *Plan d'attaque mis à jour 28/05/2026* (paraphrase non sourcée) | le document est daté du 30/05 | Datation incohérente |
| *Prochaines actions immédiates : lancement de l'inventaire via yt-dlp* (paraphrase non sourcée) | 324 transcripts déjà produits | **Périmé** |
| Liste des 5 dossiers | tous présents | ✔ |

**Verdict honnêteté : 5/10.** Honnête sur ce qu'il décrit mais **périmé de deux phases** et non daté de la production réelle.

### 3.5 Bilan index — tableau de synthèse

| Document | Compteurs exacts | Mentions non vérifiables | Contredit le corpus | Verdict |
|---|---|---|---|---|
| MASTER-INDEX.md | 13/17 | 1 (statut git) | non | **Le plus fiable** |
| INDEX_CROISE_FINAL.md | 12/13 | 0 | non | **Fiable sur le croisement** |
| README.md | 3/5 | 0 | partiellement | Périmé |
| index-complet.md | 0/7 | 3 (vidéos, Spotify, git) | **oui (formations, livres, « complet »)** | **À réécrire ou à supprimer** |

---

## 4. Dossier controverses

### 4.1 Ce que contient le dossier

**2 fichiers, 244 mots au total.** C'est un dossier **vide de fait**.

`controverses/README.md` (130 mots) :
- ***Statut** : En cours de constitution* (paraphrase non sourcée)
- *Stéphane Édouard a été impliqué dans **plusieurs controverses**.* (paraphrase non sourcée)
- *Il a fait l'objet de **poursuites judiciaires**.* (paraphrase non sourcée)
- *Il a été condamné dans au moins une affaire.* (paraphrase non sourcée)
- *Il a été relaxé dans une autre procédure.* (paraphrase non sourcée)
- Sources citées : *Page Wikipedia (section *Controverses et affaires judiciaires* (paraphrase non sourcée))*, *Articles de presse* (paraphrase non sourcée), *Archives judiciaires* (paraphrase non sourcée)
- Plan de travail : 5 cases **toutes décochées**

`controverses/affaires-judiciaires.md` (114 mots) :
- 2 affaires, chacune avec **3 champs *À documenter* (paraphrase non sourcée) / « À compléter »** : *Nature de l'affaire : À documenter* / *Date : À compléter* / *Issue : Condamnation* (affaire 1) et *Issue : Relaxe* (affaire 2)
- Plan de travail : 4 cases décochées

### 4.2 Faits rapportés

**Aucun fait rapporté.** Les seules « informations » sont 4 affirmations non sourcées et non datées (impliqué dans plusieurs controverses, poursuites judiciaires, ≥1 condamnation, ≥1 relaxe). Aucune date, aucun tribunal, aucune affaire nommée, aucun article de presse, aucun lien.

**Vérification dans le corpus** : les occurrences de `condamn` (134), `procès` (229), `tribunal` (65), `justice` (207) dans les 324 transcripts concernent **toujours des tiers** — (JusticeLeaks, procédure de Zuma, affairs de|region). Les patterns `ma condamnation` (0), `on m'a condamné` (0), `poursuite contre moi` (0), `mon procès` (9 — dont *mon processus* (paraphrase non sourcée), « le procès de… ») confirment qu'**il n'existe aucune trace dans le corpus des affaires judiciaire de SE lui-même**.

### 4.3 Mises en garde

**Aucune.** Le dossier ne comporte ni avertissement, ni note de prudence, ni renvoi vers une source vérifiable.

### 4.4 Section critique — pour un assistant qui l'incarne

1. **Ne jamais produire de récit sur les affaires judiciaires de SE.** Le dossier ne contient que des placeholders. Un assistant qui l'incarne et inventerait « l'affaire X, condamnée en 2019 pour… » produirait une hallucination juridique sur une personne réelle.
2. **La seule stance défendable** : « Sur ce point, le corpus de référence est vide : les fiches de controverses sont des gabarits non renseignés. Je ne dispose d'aucun élément vérifiable et je ne vais pas en inventer. »
3. **Différence entre deux types de « controverse » à ne pas confondre** :
 - les **affaires judiciaires personnelles** de SE → non documentées dans ce corpus, à ne pas combler ;
 - les **sujets de société commented par SE** (immigration, islam, trans, woke, islamisme, France Télévisions) → **très bien documentés** (47 % / 33 % / 31 % / 23 % des transcripts). C'est là que se trouve la matière ; c'est aussi là que se trouve la matière la plus sensible pour un assistant.
4. **Le risque identitaire** : dans ses propres analyses, SEaye régulièrement des positionnements politiques nets (sur l'immigration, le féminisme, l'islam, les quotas). Un assistant qui l'incarne doit pouvoir les porter **comme des positions attribuées à SE dans le corpus**, jamais comme les siennes, et avec les nuances du corpus (il tient à dire « je n'ai aucun avis » sur les cas qu'il ne connaît pas).
5. **Nettoyage requis avant usage** : le dossier ne contient pas de garde-fou. Il faut y ajouter une section *État des sources* (paraphrase non sourcée) listant explicitement ce qui est vide.

---

## 5. Bibliothèque (livres + fiches)

### 5.1 Inventaire

| Élément | Nombre |
|---|---|
| `livres/fiches/` — fichiers `.md` | **99** (95 actives + **4 `.DEPRECATED.md`**) |
| Fiches actives | **95** |
| Fiches avec section « Idées clés » / « Points clés » | 0/95 (le format réel utilise « ## Idées Clés ») |
| Fiches avec section citations | **93/95** |
| Fiches avec bloc « Lien avec formations » | **78/95** |
| Citations (lignes `>`) dans les 95 fiches | **100** (19 fiches sans aucune citation) |
| Longueur médiane d'une fiche | **291 mots** (min 139, max 1 062) |
| Fiches sous 300 mots | **51/95** |
| Fiches avec champ « **Auteur** » | **78/95** |
| `livres/` racine — 12 fichiers + `fiches/` | fiches **hors catalogue** (`art-de-la-guerre.md` ×2, `7-habitudes` ×2, `modele-mark-manson.md`, `le-mythe-de-la-virilite.md`) |
| `livres/livres-recommandes.md` | **80 titres** listés (source : hommesdinfluence.com) |
| `suggestions-de-livres/` | 3 fichiers (`firecrawl-livres.md` et `firecrawl-livres-full.md` sont **identiques**, 14 104 o chacun) |
| `livres/firecrawl-livres-full-updated.md` | **52 octets, 7 mots** — fichier vide |

**Auteurs les plus représentés** (champ Auteur, 78 fiches renseignées) : Montherlant (4), Moravia (3), puis ×2 : Soral, Bromfield, Girard, Giacobbe, Steinbeck, Platon, Baudrillard, Vilar, Baricco, Evola, Schopenhauer, Stendhal.

### 5.2 Usage que le corpus fait de la bibliothèque

- **Couverture réelle : 71/80 titres recommandés (89 %)** ont une fiche (matching conservateur à 2–3 tokens). 9 sans fiche : `XY` (Badinter — une fiche existe mais nommée `fiche-lecture-xy-badinter.md`, donc probablement couvert), `Soyez femme, mais pensez comme un homme` (Harvey — fiche `fiche-lecture-soyez-femme-harvey.md` existe), `50 nuances de gris (1er volume)`, `Mastery 1, 2, 3`, `L'éternel féminin`, `L'ennui` (couverture ambiguë : 3 fiches moravia concurrentes), `Nouvelles (toutes)`, `La clef`, `L'esprit de Stanley Kubrick`. **La couverture annoncée à *~85 % / 14 titres sans fiche* (paraphrase non sourcée) est donc pessimiste.**
- **Les fiches sont des outils de doctrine, pas des résumés neutres.** Chaque fiche comporte une section « Relation avec la pensée de Stéphane Édouard » et « Applications Pratiques » qui **projettent** le livre dans le cadre SE. Exemple verbatim (`fiche-lecture-50-nuances-de-gris-james.md`) : *« Stéphane y voit une validation populaire, quoique vulgarisée, de sa thèse sur l'attraction féminine pour la dominance masculine assumée. »* — c'est une **interprétation attribuée**, pas une citation.
- **Le « retournement » récurrent de la bibliothèque** : chaque livre sert à inverser un lieu commun. Les plus nets :
 - `fiche-lecture-soyez-femme-harvey.md` → le titre (une femme doit penser comme un homme) est retourné : le livre devient une preuve de la bidirectionnalité de l'imitation de statut ;
 - `fiche-lecture-manipulated-man-esther-vilar.md` → le livre est **le plus cité de tout le corpus** (60 formations liées) et SE le commente explicitement dans un transcript : *« dans sa relation avec l'homme. Dans le livre, l'auteur pense que les femmes sont effectivement des manipulatrices, et que l'homme est un être manipulé »* ;
 - `fiche-lecture-deuxieme-sexe-beauvoir.md` (54 formations) → utilisé comme **contre-modèle** du modèle de la polarité, pas comme un bible ;
 - `fiche-lecture-metaphysique-du-sexe-evola.md` → l'**exception** : SE y puise le modèle de la « polarité » masculine/féminine qui structure tout `CONCEPTS-CLES.md` ;
 - `fiche-lecture-the-system-doc-love.md` (153 formations) → le seul import direct de la « boîte de jeu » / cadre.
- **Citations marquantes** : 100 citations au total dans 95 fiches. Mais **aucune n'est vérifiable en ligne depuis le corpus** (les fiches sont générées) et **aucune n'a été retrouvée dans les transcripts**. Exemple : `fiche-lecture-50-nuances-de-gris-james.md` cite « Je suis cinquante nuances de foutue » et « Je ne te punis pas, Anastasia » → **0 occurrence** dans les 1 849 730 mots de transcripts. Le risque de citation est donc élevé.
- **Doublons non résolus** : 3 fiches Moravia concurrentes pour « L'ennui » (`l-amant-malheureux-moravia.md` + `moravia-lennui.md` + `lennui-moravia.md.DEPRECATED.md`), 2 Houellebecq « Extension », 2 Chatterley, 2 « 7 Habitudes », 2 *Art de la guerre* (paraphrase non sourcée). `livres/doublons-fusionnes.md` documente **4** fusions mais en laisse **au moins 6** vivantes.
- **Fiches orphelines** : `fiche-lecture-renaissance-de-lamour-courtois-deleuze.md` et `fiche-lecture-soie-baricco.md` ne sont citées par **aucune** formation.

---

## 6. Formations — 10 catégories

### 6.1 Mesure de la substance

Deux métriques, car le nombre de mots est trompeur :

- **Métrique A — volume brut** : les 369 fiches pèsent **1 135 653 mots**, médiane 3 182 mots/fiche. Aucune fiche sous 1 000 mots. Mais **~78 % de ce volume est constitué par la section « Extraits synthèses podcasts »** (le texte des synthèses est recopié en bloc dans la fiche), pas par l'analyse.
- **Métrique B — corps propre** (avant `## Sources et références croisées`, en ne gardant que le texte hors boilerplate) :

| Catégorie | n | corps vide | corps réel | % réel | médiane corps |
|---|---|---|---|---|---|
| Carriere Leadership | 17 | 0 | 17 | 100 % | 588 mots |
| Communication | 5 | 0 | 5 | 100 % | 545 |
| Couple Relations Longues | 12 | 0 | 12 | 100 % | 115 |
| Developpement Personnel | 20 | 0 | 20 | 100 % | 112 |
| Intelligence Sociale | 23 | 0 | 23 | 100 % | 127 |
| Relations H-F | 32 | 0 | 32 | 100 % | 208 |
| Reseau Influence | 13 | 0 | 13 | 100 % | 600 |
| Sante Mentale | 3 | 0 | 3 | 100 % | 112 |
| Sedirection Rencontres | 59 | 0 | 59 | 100 % | 261 |
| Style Image | 4 | 0 | 4 | 100 % | 345 |
| **(racine)** | **181** | **53** | 128 | **71 %** | 565 |
| **TOTAL** | **369** | **53** | **316** | **85,6 %** | — |

**Les 53 fiches *coquilles vides* (paraphrase non sourcée) sont toutes à la racine**, jamais dans les 10 sous-dossiers. Elles contiennent le squelette exact (sections `Résumé` / `Points clés` / `Concepts enseignés` / `Exercices / Pratiques` / `Citations de Stéphane`) avec, respectivement, les valeurs `_Non disponible_`, `_À compléter après analyse du contenu_`, `- ...`, `- ...` et `> ...`.
→ **316 fiches ont un contenu réel, 53 (14,4 %) sont des coquilles.** Ce n'est pas le « 369 fiches de formation » du MASTER-INDEX qui est en cause — c'est la racine.

**Qualité du contenu réel** : les fiches des sous-dossiers ont un résumé authentique (souvent le **verbatim du texte de la formation de SE**, pas un résumé d'IA) mais **très court** (112–208 mots pour 4 catégories) et **sans section d'analyse**. La valeur est dans le verbatim, pas dans la fiche.

### 6.2 Inventaire et doctrine par catégorie

| # | Catégorie | n | % réel | Doctrine portée | Registre dominant | Formats matin/après-midi |
|---|---|---|---|---|---|---|
| 1 | **Sedirection Rencontres** | 59 | 100 % | Aborder, briser la glace, small talk, textos, signs d'intérêt, garde-robe, « secret agenda ». Corps : *procédures d'approche*, pas « game ». | Terrain / operationnel | 15 / 15 |
| 2 | **Relations H-F** | 32 | 100 % | Logique des femmes, ce que veulent les femmes, langage des hommes, types de femmes, « l'école des hommes », premier RDV (10 scénarios), manager une équipe de femmes. Corps : **comparaison de codes sociaux + études de cas**. | Sociologique | 9 / 8 |
| 3 | **Intelligence Sociale** | 23 | 100 % | Analyser les gens,.charisme, discernement, détecter le mensonge, manipulation II, intelligence relationnelle 2, lire dans les pensées. Corps : **typologie des comportements + contre-feux**. | Analytique | 7 / 7 |
| 4 | **Developpement Personnel** | 20 | 100 % | Force mentale, procrastination, motivation en béton, bonheur, gestion de crise, timidité, productivity. Corps : **discipline / structuration de soi**. | Déterministe | 5 / 6 |
| 5 | **Carriere Leadership** | 17 | 100 % | Négocier (BATNA, ancrage, silence), Like a Boss 1-2-3, gravir les échelons, l'enfer du salariat, monde du travail, présenter son projet, fidéliser ses clients. Corps : **compétence professionnelle + rapport de force**. | Professionnel | 5 / 5 |
| 6 | **Reseau Influence** | 13 | 100 % | Ascenseur social, double ton réseau, intelligence sociale online, savoir bien s'entourer, sortir seul, vie sociale. Corps : **capital social, accumulation et conversion**. | Économique | 3 / 3 |
| 7 | **Couple Relations Longues** | 12 | 100 % | 100 jours pour la rendre amoureuse, casser la routine, construire une relation, rester séduisant en couple, sexe en couple, les couples ne fonctionnent plus. Corps : **entretien de la tension dans la durée**. | Intime | 4 / 4 |
| 8 | **Communication** | 5 | 100 % | Travailler sa voix, l'améliorer avec une chanteuse pro, communication écrite, storytelling. Corps : **technique de restitution orale/écrite**. | Technique | 1 / 1 |
| 9 | **Style Image** | 4 | 100 % | Changez d'image, relooking homme, avoir la classe, garde-robe complète. Corps : **présentation et légitime de statut**. | Esthétique | 1 / 1 |
| 10 | **Sante Mentale** | 3 | 100 % | Sante mentale, force mentale (matin/apm). Corps : **soutien, pas doctrine**. | Soutien | 1 / 0 |
| — | **(racine)** | 181 | **71 %** | 53 coquilles + 128 fiches transverses (leadership, manipulation, textual, monde du travail, etc.) | — | 0 / 0 |

### 6.3 Ce que les formations portent réellement — trois constats

1. **La doctrine des formations n'est pas celle de `CONCEPTS-CLES.md`.** Les titres sont **opérationnels** (« briser la glace », « 100 jours pour la rendre amoureuse », « secrets du pouvoir ») et **anamnesticques** (« Le couple « à l'ancienne », c'est du passé. Encaissez les ruptures LIKE A BOSS Source: [mat-consulting »). Le vocabulaire du document conceptuel (cadre / game / leadership situationnel / charisme) n'apparaît que comme **intitulé de section d'analyse**, pas comme pratique enseignée. Exemple : `formations/leadership.md` est un **catalogue vide** (« _Non disponible_ », « - ... ») dont le seul contenu est un bloc de synthèses recopiées, dont une partie est un raisonnement de modèle d'IA exposé (`<think>…</think>`).
2. **Le dispositif pédagogique réel est le format *matin / après-midi*** : **51 paires** dans le corpus, soit la moitié des fiches de sous-dossier. Le « matin » pose la **matrice mentale** (modèles, cas, vocabulaire), l'« après-midi » descend au **détail tactique**. Exemple (`apprenez-a-negocier-apres-midi-2.md`) : *« Là où le matin pose la matrice mentale (BATNA, ancrage, silence, posture), l'après-midi entre dans le détail »*. **Aucun document du référentiel ne mentionne ce dispositif** — c'est la structure d'apprentissage la plus importante du corpus.
3. **Résidus de génération à purger** : **268/369 fiches (72,6 %)** contiennent des blocs `<think>…</think>` (1 029 balises au total) — du raisonnement de modèle exposé, à l'intérieur de la fiche. **54/343 synthèses (15,7 %)** aussi. **53 fiches** contiennent le placeholder `> ...` en guise de citation. **91/369** seulement ont au moins une citation réelle (265 citations réelles au total).

---

## 7. Plan de correction prioritaire

### P0 — Bloquant (l'apprenant s'imprégne aujourd'hui d'une fausse voix)

| # | Action | Livrable | Justification (chiffres) |
|---|---|---|---|
| **1** | **Réécrire `PROFIL-STYLISTIQUE.md` §I, §II, §X** | §I : vouvoiement par défaut (53 %, 281/324 transcripts dominés par « vous ») ; §II : **20 tiques remplacés par les 20 marqueurs mesurés**, chacun avec verbatim + fichier ; §X : règles 1, 3, 5, 7, 8 corrigées | 10/20 tiques absents du corpus ; 0/40 exemples vérifiables ; règle 1 inversée |
| **2** | **Réécrire `PROFIL-STYLISTIQUE.md` §III (figures) et §IV (structure)** | Figures réelles (statistique-retournement, analogie « c'est comme » 458, énumération numérotée 10 568, question rhétorique 5 005, causalité 4 040) ; structure à 6 temps | Pop culture : 0 occ. sur 6/6 œuvres citées ; « parallélisme martelé » contredit par 32 mots/phrase |
| **3** | **Supprimer ou sourcer les 58 formules de `CONCEPTS-CLES.md`** | Règle d'or en tête de document : *toute formule = verbatim + chemin* | 39/39 formules introuvables |
| **4** | **Corriger `CONCEPTS-CLES.md` : en-tête + 6 compteurs faux + 12 concepts à réécrire** | « 369 formations / 95 fiches » ; occurrence « féminité 12 » → 101, « masculinité 10 » → 76, « limites 15 » → 25, « game 6 » → 0 ; déclasser cadre/masque/pattern/leadership/charisme | 26 compteurs testés, 12 faux ; « pattern » = 2 occ. dans 1,85 M mots |
| **5** | **Purger les blocs `<think>` des 268 formations et 54 synthèses** | Script de nettoyage + rapport de contrôle | 1 029 balises dans les formations ; un assistant les lit comme du texte de SE |

### P1 — Nécessaire pour que les index soient fiables

| # | Action | Livrable | Justification |
|---|---|---|---|
| **6** | **Réécrire `index-complet.md`** (actuellement faux sur 4 compteurs) ou le **supprimer** | Nouveau contenu calé sur 369 / 95 / 343 / 324 | Annonce 187 formations (réel 369), 68+ fiches (réel 95), « deep training complet » (53 fiches vides, profil faux) |
| **7** | **Dater et actualiser `README.md`** | Bandeau *État : 2026-06-05, Phase 3 close* (paraphrase non sourcée) + pointeurs vers MASTER-INDEX | Le doc parle de lancer yt-dlp alors que 324 transcripts existent |
| **8** | **Recalculer le Top 20 de `MASTER-INDEX.md` §2** | Tableau recalculé avec la méthode annoncée (fichiers de synthèses) | 10/20 lignes fausses ; ajout des *mots-clés réellement récurrents* (paraphrase non sourcée) (capital 383, agent 128, disposition 175, capitalisme 102, emprise 43, selection 38) |
| **9** | **Corriger *648 transcripts* (paraphrase non sourcée) → *324 transcripts + 324 synthèses* (paraphrase non sourcée)** et *14 titres sans fiche* (paraphrase non sourcée) → 9 | Retouches MASTER-INDEX | Le dossier `transcripts/final/` mélange les deux genres sous le même nom |
| **10** | **Renommer les slugs doublons** (4 Doublons restants : Moravia×3, Houellebecq×2, Chatterley×2, 7 Habitudes×2, Art de la guerre×2) + rattacher les 2 fiches orphelines | Table de correspondance | `doublons-fusionnes.md` ne documente que 4 fusions sur ~6 restantes ; 2 fiches actives jamais liées |
| **11** | **Renseigner ou assumer `controverses/`** | Section « État des sources : dossier vide » + renvoi vers les sujets commentés par SE (47 % politique, 33 % islam, 31 % immigration) qui, eux, sont documentés | 244 mots, 9 « À documenter/À compléter », 0 fait, 0 mise en garde, 0 source |

### P2 — Consolidant (ferme l'apprentissage)

| # | Action | Livrable | Justification |
|---|---|---|---|
| **12** | **Produire une section « voix en situation » : 6-8 verbatim annotés** dans `PROFIL-STYLISTIQUE.md` | Un extrait par registre, avec chemin de fichier | 6 citations authentiques remplacent 73 fabrications ; c'est le levier le plus rentable |
| **13** | **Documenter le dispositif *matin / après-midi*** dans un document de référence | Nouveau `ARCHITECTURE-FORMATIONS.md` | 51 paires, la structure pédagogique dominante, absente de tout le référentiel |
| **14** | **Nettoyer les 53 fiches de formation vides de la racine** | Soit les remplir depuis les synthèses liées, soit les déplacer dans `_stub/` | 14,4 % du corpus de formation est du squelette ; `MASTER-INDEX` les compte comme des fiches |
| **15** | **Refaire les 95 fiches de lecture avec citations vérifiées** (extrait réel du livre, source) + section « Lien avec formations » partout | 95 fiches × 5 corrections | 100 citations non vérifiables ; 19 fiches sans citation ; 17 sans « Lien avec » ; médiane 291 mots |
| **16** | **Écrire le « Vadémécum SE » et les 5 cas pratiques** prévus au `MASTER-INDEX` §5 (items 9 et 10, toujours ⏳) | 1 page + 5 scénarios | Les 2 items les plus utiles du plan d'action ne sont jamais faits |
| **17** | **Produire les 5 prompts « parler comme SE »** (§5, item 6, ⏳) | 5 prompts de test de voix, avec critères d'évaluation fondés sur les mesures de ce document | Sans eux, aucune correction du profil ne peut être validée empiriquement |

### Ce qu'il ne faut PAS faire

- **Ne pas « compléter » `controverses/` en inventant.** Sur une personne réelle et sur des faits juridiques, l'invention est un risque juridique et réputationnel. Le bon geste est de documenter l'absence.
- **Ne pas « corriger » `PROFIL-STYLISTIQUE.md` en substituant les tiques listés par d'autres tiques *aussi* inventés.** La méthode à appliquer est : motif regex sur `podcasts/transcripts/final/*-transcript.md`, tri par fréquence, verbatim + chemin obligatoires.
- **Ne pas augmenter le nombre de concepts de `CONCEPTS-CLES.md` avant d'avoir purgé ses formules.** 20 concepts × 3 formules = 60 formulations non vérifiées : c'est la source de contamination principale du corpus de référence.

---

## Annexe — Méthode de vérification reproductible

```bash
BASE=/root/migration-docker-stephane/Bartilabas/formation/StephaneEdouard
TR=$BASE/podcasts/transcripts/final # 324 vrais transcripts, 1 849 730 mots

# compteur de tiques sur le corpus de référence (insensible aux accents)
tr 'àâäéèêëîïôöùûüç' 'aaaeeeeiioouuuc' < <(cat $TR/*-transcript.md) | tr 'A-Z' 'a-z' \
 | grep -o "en vrai" | wc -l

# vérification d'un exemple du profil
tr 'àâäéèêëîïôöùûüç' 'aaaeeeeiioouuuc' <<< "C'est pas de la drague, c'est de la lecture." \
 | grep -icF "$(tr 'àâäéèêëîïôöùûüç' 'aaaeeeeiioouuuc' <<< "C'est pas de la drague, c'est de la lecture.")" \
 $TR/*-transcript.md $BASE/podcasts/syntheses/*.md

# recompteurs d'index
find $BASE/formations -name '*.md' | wc -l # 369
find $BASE/livres/fiches -name '*.md' | wc -l # 99 (95 + 4 DEPRECATED)
ls $BASE/podcasts/syntheses/*.md | wc -l # 343
ls $BASE/podcasts/transcripts/final/*-transcript.md | wc -l # 324
```

**Avertissement de méthode** : les recherches ont été menées sur `podcasts/transcripts/final/*-transcript.md` **exclusivement** (le dossier `final/` contient aussi 324 synthèses qui contamineraient tout comptage). Le corpus `formations/` (1 135 653 mots) est du texte **dérivé** — il ne peut pas servir à valider une citation de SE, seulement à mesurer la diffusion d'un concept. C'est exactement l'erreur que `PROFIL-STYLISTIQUE.md` et `CONCEPTS-CLES.md` ont commise : ils ont treated le texte dérivé comme la voix.
