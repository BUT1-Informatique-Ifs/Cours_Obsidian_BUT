# <mark class="hltr-purple hltr-bold">Arbres recouvrants de poids minimal</mark>
- 2 sommets quelconques d'un arbre sont reliés par une unique chaine
- enlever une arête quelconque à un arbre le déconnecte
- ajouter une arête quelconque à un arbre crée un cycle
	Si on a les 3 propriétés, alors on a un arbre

## <mark class="hltr-green hltr-bold">Les arbres</mark>
### <mark class="hltr-pink hltr-bold">Construction récursive</mark>
	Un graphe avec un seul sommet et zéro arête est un arbre
- A partir d'un arbre avec au moins 1 sommet
- On accroche une feuille à n'importe quel sommet
- On obtient un arbre avec un sommet et une arête de plus
#### <mark class="hltr-blue hltr-bold">Remarques</mark>
1. Un arbre à n sommets possède exactement n-1 arêtes
2. Un arbre avec au moins deux sommets a forcément au moins une feuille
	Démonstration page 42 du CM sur les arbres

### <mark class="hltr-pink hltr-bold">Propriétés caractéristiques</mark>
1. 2 sommets quelconques d'un arbre sont reliés par une unique chaîne
2. Enlever une arête quelconque à un arbre le déconnecte
	On ne parle pas ici des arêtes des feuilles
3. Ajouter une arête quelconque à un arbre crée un cycle

**Si l'arbre vérifie ces 3 propriétés, alors c'est un arbre**

## <mark class="hltr-green hltr-bold">Les arbres recouvrants</mark>

### <mark class="hltr-pink hltr-bold">Définition</mark>

Soit un graphe non orienté G
Un arbre T tel que :
- sommets : tous les sommets de G
- arêtes : certaines arêtes de G
![[graphe_arbre_T_recouvrant.png]]
<mark class="hltr-red hltr-bold">Un arbre recouvrant est un arbre qui passe par tous les sommets d'un graphe</mark>

1. Un graphe peut avoir plusieurs arbres recouvrants
2. Un arbre n'a qu'un seul arbre recouvrant, lui même
3. Un graphe qui n'est pas connexe a aucun arbre recouvrant (car on ne peut pas atteindre tous les sommets)
4. Un graphe connexe a au moins un arbre recouvrant
## <mark class="hltr-green hltr-bold">Les graphes valués</mark>

### <mark class="hltr-pink hltr-bold">Définition</mark>
- Chaque arête a un poids > 0
- Le poids d'une chaîne (du graphe) est la somme des poids des arêtes de cette dernière (la chaîne).

## <mark class="hltr-green hltr-bold">Algorithme de Kruskal</mark>
- On veut un chemin qui coûte le moins cher possible
- Tous les centres doivent pouvoir communiquer
- Il ne faut pas construire des connexions que l'on pourrait se passer

### <mark class="hltr-pink hltr-bold">Principe de l'algorithme</mark>
- On part d'une forêt d'arbres où chaque arbre est un sommet isolé du graphe
- A chaque itération de l'algorithme, on ajoute à cette forêt, l'arête de poids le plus faible qui ne crée pas de cycle avec les arêtes déjà choisies
- On stoppe l'algorithme quand on obtient un arbre

### <mark class="hltr-pink hltr-bold">Algorithme</mark>

![[algorithme_kruskal.png]]

### <mark class="hltr-pink hltr-bold">Démonstration</mark>
1. Kruskal s'arrête toujours
	L'arbre recouvrant T finit par être connexe car G est connexe, donc en parcourant (au pire) toutes les arêtes, on arrive à connecter tous les sommets du graphe
---
2. Kruskal construit un arbre recouvrant
	Sommets de T = Sommets de G
	Arêtes de $$T \subseteq G$$
	T est connexe
	T est sans cycle car on n'ajoute une arête que pour connecter deux composantes connexes, ce qui ne peut pas créer de cycle. De plus, au début de l'algorithme, T n'a pas d'arêtes, donc pas de cycles.
---
3. L'arbre recouvrant construit par Kruskal est de poids minimal
#### <mark class="hltr-blue hltr-bold">Preuve</mark>
	Voir page 93 du CM Arbres
## <mark class="hltr-green hltr-bold">Algorithme de Prim</mark>

### <mark class="hltr-pink hltr-bold">Principe de l'algorithme</mark>
- On part d'un arbre initial réduit à un seul sommet du graphe
- A chaque itération, on agrandit l'arbre en lui ajout le sommet libre accessible de plus petit poids possible
- On stoppe quand l'arbre est recouvrant
### <mark class="hltr-pink hltr-bold">Algorithme</mark>

![[algorithme_Prim.png]]

Pour les prochaines semaines, je vais noter les trucs les plus "importants" car en vrai ça sert à rien que je note les diapos que le prof nous file déjà