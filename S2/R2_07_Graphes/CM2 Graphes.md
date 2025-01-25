# <mark class="hltr-purple hltr-bold">Graphes Premiers résultats</mark>

## <mark class="hltr-green hltr-bold">Lemme des poignées de main</mark>

### <mark class="hltr-pink hltr-bold">Théorème</mark>
La somme des degrés des sommets est égale au double du nombre d'arêtes

### <mark class="hltr-pink hltr-bold">Preuve</mark>
Comptons les extrémités de 2 façons :
- en regardant les arêtes (A) : 1 arête = 2 extrémités => total : il y a 2*|A| extrémités
- en regardant les sommets (S) : il y a deg S extrémités pour S => total : Somme deg(S)
### <mark class="hltr-pink hltr-bold">Application</mark>

![[preuve_graphes.jpeg]]

## <mark class="hltr-green hltr-bold">Parcours Eulérien</mark>

### <mark class="hltr-pink hltr-bold">Cycle eulérien</mark>
	C'est un cycle qui passe une fois et une seule par toutes les
	arêtes du graphes
#### <mark class="hltr-blue hltr-bold">Théorème</mark>
Un graphe connexe a un cycle eulérien si et seulement si chaque
sommet a un degré pair
### <mark class="hltr-pink hltr-bold">Chaîne eulérienne</mark>
	C'est une chaîne qui passe une fois et une seule par toutes les
	arêtes du graphe
#### <mark class="hltr-blue hltr-bold">Théorème</mark>
Un graphe connexe a une chaîne eulérienne qui n'est pas un cycle si et seulement si chaque sommet a un degré pair, sauf exactement 2
### <mark class="hltr-pink hltr-bold">Algorithme de Fleury :</mark>

#### <mark class="hltr-blue hltr-bold">Complexité de la recherche de parcours eulérien</mark>
O(n) = A (A, le nombre d'arêtes)

## <mark class="hltr-green hltr-bold">Parcours Hamiltonien (Culture G)</mark>

### <mark class="hltr-pink hltr-bold">Cycle hamiltonien</mark>
Il faut faire du bruteforce. Grosse complexité d'algorithme
