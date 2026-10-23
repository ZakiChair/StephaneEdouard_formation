# Sources publiques et veille — comment le corpus continue de grossir

Détail opérationnel de la section 9 du SKILL.md. La procédure générique (énumérer,
mesurer le delta, scraper, normaliser, réintégrer) est dans la compétence
`live-source-harvesting`. Ici : le cas concret de cette source.

## 1. Ce que le catalogue public porte

`mat-consulting.fr/catalogue/` n'est pas une page unique : le catalogue complet
passe par les pages de catégorie (`/categorie/<cat>/page/N/`). Sur la seule page
d'accueil, on voit une fraction du catalogue.

Chaque page produit porte des blocs structurés et réguliers :

| Bloc | Contenu | Usage autorisé |
|---|---|---|
| `La tracklist` | le déroulé séance par séance | le **programme** d'une formation |
| `Ce que vous apprendrez` | les objectifs pédagogiques | ce que l'auteur **promet** |
| `Mes postulats` | les postulats de l'auteur | les **hypothèses** de l'auteur |
| `AU PROGRAMME` | le plan d'ensemble | l'**architecture** du séminaire |
| `Écouter l'extrait gratuit` | un lien YouTube | le **pont** vers l'oral |

Piège de provenance, à répéter : une tracklist autorise *cette formation couvre X, Y, Z*. Elle n'autorise pas *cette formation explique X*. Ces pages sont de
la **copie éditoriale du vendeur**, pas de la parole de Stéphane. Ne jamais les
citer comme parole de l'auteur.

## 2. Le pont vers l'oral

Le bouton `Écouter l'extrait gratuit` pointe vers une vidéo YouTube **distincte**
des transcripts déjà collectés. C'est le mécanisme qui rend la couche web utile :
la tracklist donne le programme, l'extrait vidéo donne l'oral.

Une page produit peut en pointer plusieurs : les liens observés sur un
catalogue dense couvrent des extraits de séminaires distincts. Collecter les
métadonnées de chaque extrait (titre, description, date) séparément de la page
produit — ce sont deux objets, pas un.

## 3. Les transcripts YouTube — la seule voie qui marche

| Endpoint | Résultat observé |
|---|---|
| `timedtext` (API captions) | 200, corps vide |
| InnerTube `/youtubei/v1/get_transcript` | 400, ou `LOGIN_REQUIRED` |
| `noembed` / oEmbed | titre et auteur seuls — pas de caption, pas de description |
| **Scraper de rendu sur la page `watch`** | **le transcript, en markdown, segmenté par timestamp** |

→ Passez par le panneau Transcript rendu par la page watch. C'est du contenu
côté client : le scraper doit attendre l'élément transcript, pas seulement le
chargement de la page.

**Budget de débit** : 3 workers maximum, au-delà le 429 s'enchaîne. Backoff
exponentiel + jitter, en honorant `Retry-After`. Cache disque par URL : une course
en cache est gratuite, et une récolte interrompue reprend sans re-dépenser.

## 4. Le piège de l'identifiant — l'erreur qui a faussé tout un plan

Un ID YouTube fait 11 caractères dans `[A-Za-z0-9_-]` et **peut commencer par `-`
ou `_`**.

Conséquence mesurée : une récolte a annoncé **92 nouveaux** transcripts alors
qu'il n'y en avait que **19** d'absents. Les 73 autres avaient été mal parsés —
`split('_')[0]` renvoie la chaîne vide pour tout ID commençant par `_`, ce qui les
écrase tous dans le même seau. Le nombre de mots « neufs » était gonflé d'environ
quatre fois, et le plan de travail a été dimensionné dessus.

```python
import re
YT_ID = re.compile(r"([A-Za-z0-9_-]{11})-transcript\.md$")
```

Garde-fou obligatoire, à poser avant toute écriture :

```python
assert len(set(ids)) == len(set(files))   # un id par fichier
assert all(len(i) == 11 for i in ids)      # longueur de l'id
```

Un écart = bug de parsing → arrêter la course, ne rien écrire.

**Interroger le corpus avec la même extraction que la récolte.** Comparer un delta
extrait par une méthode à un corpus indexé par une autre méthode est comparer
deux listes de tailles différentes : c'est ainsi qu'on fabrique un delta.

## 5. Normalisation des captions

Les captions brutes arrivent en fragments non ponctués. Les fichiers du corpus, eux,
sont des blocs de prose reflowés et ponctués. Mélanger les deux fausse toutes les
mesures de style : phrase médiane, densité de ponctuation, registre.

Normaliser, et **garder la copie brute à côté** — sans elle, impossible de prouver
que la normalisation n'a rien ajouté.

Reflow + ponctuation finale + majuscule initiale suffisent. **Ne pas** corriger la
grammaire de l'orateur : c'est de l'éditorialisation, et ça casse la provenance de
toute citation tirée du fichier.

## 6. Recompter après intégration

Chaque intégration change le dénominateur de toutes les mesures. Rejouer :

- le ratio vous/tu **par registre** (oral / écrit / rédigé) ;
- la phrase médiane ;
- les tics par k mots ;
- le nombre de transcripts et de mots ;
- la taille du lot « sans contenu » (les 147 d'abord, puis **137** après la reprise
  des 10 fiches dont le verbatim était masqué par un préfixe de numéro de ligne).

Puis **ré-auditer les livrables dérivés** : un nouveau transcript peut rendre
ambiguë une citation qui était vérifiée (une seconde occurrence de la même
formulation change l'ordre de résolution) et il peut introduire des affirmations
non sourcées.

## 7. Format du rapport de veille

Le rapport doit dire **ce qui est nouveau** (IDs, titres, compte), pas redécrire
l'état du corpus. Un rapport qui ré-énumère tout le corpus à chaque tick est
illisible dès la troisième notification — et c'est ainsi qu'une veille se fait
couper.

Le sentinel doit être **déterministe** : aucun timestamp, aucun compteur variable,
liste triée. Si la sortie varie entre deux runs identiques, le planificateur
réveille un agent à chaque tick et la veille devient du bruit.
