# <mark class="hltr-purple hltr-bold">Introduction aux Graphes</mark>

<mark class="hltr-red hltr-bold">Un graphe : couple de 2 ensembles (sommets et arêtes)</mark>

<mark class="hltr-red hltr-bold">Sommets : souvent représenté par des points</mark>
Arêtes : associées à 2 sommets minimum, peuvent être orientées, avoir une valeur


**Parcourir toutes les arêtes une fois et une seule** => <mark class="hltr-red hltr-bold">Parcours eulérien</mark>
**Parcourir tous les sommets une fois et une seule** => <mark class="hltr-red hltr-bold">Parcours hamiltonien</mark>

## <mark class="hltr-green hltr-bold">Définitions</mark>

### <mark class="hltr-pink hltr-bold">Représentation d'un graphe en machine</mark>
	avec des listes, avec des matrices, ..
Pour un graphe non orienté, on prends la liste des voisins du sommet

<mark class="hltr-red hltr-bold">Logiciel pour faire un graphe : DiGraph en python (jupyterNotebook)</mark>

=> pas facile de vérifier que 2 graphes sont les mêmes (il y a des algo pour cela).

Tips : Une matrice à la puissance n => connaitre le nombre de possibilité d'aller à un sommet en n étapes.

## <mark class="hltr-green hltr-bold">Graphes non orientés</mark>
### <mark class="hltr-pink hltr-bold">Graphe complet ou Clique</mark>
Tous les sommets sont reliés entre eux (ils sont tous voisins)

### <mark class="hltr-pink hltr-bold">Graphe biparti complet</mark> 
Un graphe avec 2 ensembles différents qui ont des connexions entre eux

### <mark class="hltr-pink hltr-bold">Chaîne</mark> 
Un graphe en forme de ligne

### <mark class="hltr-pink hltr-bold">Connexité</mark>
Si pour 2 sommets distincts, ils ont un chemin entre eux, alors le graphe est connexe

### <mark class="hltr-pink hltr-bold">Cycle</mark>
Un graphe "bouclé"

### <mark class="hltr-pink hltr-bold">Arbre</mark>
C'est un graphe connexe sans cycle

### <mark class="hltr-pink hltr-bold">Une forêt</mark>
C'est un graphe sans cycle

## <mark class="hltr-green hltr-bold">Graphes orientés</mark>

Def : 
	on remplace arête par arc
	on remplace chaîne par chemin
	on remplace cycle par circuit

Fortement connexe :


## Réseaux et flots


## <mark class="hltr-green hltr-bold">Vocab</mark>

<mark class="hltr-red hltr-bold">Degré d'un sommet : nb d'arêtes qui sort du sommet</mark>






