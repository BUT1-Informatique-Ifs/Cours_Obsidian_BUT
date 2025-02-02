# <mark style="font-weight:bolder; color:white; background: #D2B3FFA6;">Dijkstra</mark>

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Rappel parcours en largeur</mark>

- Parcours qui utilise une file (FIFO : First In First Out)

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Le problème des distances à un sommet</mark>

- Remplacer un graphe avec des distances par un graphe avec plusieurs étapes ( des sommets intermédiaires )

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Inconvénients</mark>

- Il faut distinguer les anciens sommets et les sommets intermédiaires
- Si les distances sont grandes, on peut avoir un problème de complexité car graphe très grand
- Or le temps dépend du nombre de sommets

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Méthode sans inconvénients (l'algo de Dijkstra)</mark>

- Au début, on connait que le sommet A de distance 0 et les autres sommets sont à une distance inconnue (infini par exemple)
- On met à jour les distances vers les sommets voisins de A
- On choisit comme racine le sommet qui a la plus petite distance du sommet A et on y touche plus
- ...


| A   | B   | C   | D   | E   | F   | G   | H   | I   | J   |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 0   | X   | X   | X   | X   | X   | X   | X   | X   | X   |
| ll  | 85  | 217 | X   | 173 | X   | X   | X   | X   | X   |
| ll  | ll  | 217 | X   | 173 | 165 | X   | X   | X   | X   |
| ll  | ll  | 217 | X   | 173 | ll  | X   | X   | 415 | X   |
| ll  | ll  | 217 | X   | ll  | ll  | X   | X   | 415 | 675 |
| ll  | ll  | ll  | X   | ll  | ll  | 403 | 400 | 415 | 675 |
| ll  | ll  | ll  | 503 | ll  | ll  | 403 | ll  | 415 | 567 |
| ll  | ll  | ll  | 503 | ll  | ll  | ll  | l   | 415 | 567 |
| ll  | ll  | ll  | 503 | ll  | ll  | ll  | ll  | ll  | 499 |
| ll  | ll  | ll  | 503 | ll  | ll  | ll  | ll  | ll  | ll  |
| ll  | ll  | ll  | ll  | ll  | ll  | ll  | ll  | ll  | ll  |

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Complexité</mark>
v, un sommet

v\*v = v^2 de complexité


### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Limitation de Dijkstra</mark>

- Ne permet pas de trouver le chemin le plus court si les arêtes ont des poids négatifs
- Pour les arêtes de poids négatifs, on utilise l'algo de Bellman-Ford 
- Avec des graphes énormes, Dijkstra doit encore être optimisé