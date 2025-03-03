# <mark class="hltr-purple format">CM9 Les Types Abstrait de Données (TAD) et collections</mark>


- Un TAD = une structure de données (objet structuré en mémoire) + opérations pour manipuler ces données (ex : faire un type Ensemble avec des opérations comme : ajouter, union, intersection, ..)

En java, ce sont les classes abstraites, les interfaces, ...

## <mark class="hltr-green format">Les collections</mark>

- Collection est l'interface racine de la hiérarchie de collection.
- représente un ensemble d'éléments
- plusieurs méthodes pour le manipuler :
	- add()
	- clear()
	- remove()
	- ...

### <mark class="hltr-pink format">Sous-interfaces principales</mark>

- List
	- éléments accessible par un indice
	- peut contenir des éléments dupliqués
	- préserve l'ordre d'insertion
		- il y a une spécialisation de List avec ArrayList

- Queue
	- le premier élément est lu/retiré
	- l'insertion dépend de l'implémentation
	- liste qui ne permet que de lire le premier élément
	- l'insertion dépend de l'implémentation (FILE, PILE, ..)
- Set
	- modélise la notion mathématique de l'ensemble
	- on ne peut pas avoir des éléments dupliqués (sachant que c'est un ensemble mathématique)
- Map
	- contient des paires (clé, valeur)
	- ne permet pas de clés dupliquées

### <mark class="hltr-pink format">Quand et pourquoi utiliser une ArrayList :</mark>
- taille nécessaire pas connue à l'avance
- accès rapide souhaité car => complexité O(1)
- pas beaucoup d'insertion/suppression car => complexité O(n)
- taille qui n'augmentera pas souvent (sinon utiliser ensureCapacity())

### <mark class="hltr-pink format">LinkedList, pourquoi et quand utiliser ?</mark>
- Structure de données dynamique (Exige plus de mémoire qu'une ArrayList)
- Collection d'objets arrangés dans un ordre séquentiel
	- chaque élément possède un successeur

Pourquoi et quand :
- Taille nécessaire pas connue à l'avance
- Beaucoup d'insertion/suppression à faire car => complexité O(1)
- Taille qui va augmenter souvent
- Accès rapide pas important car => complexité O(n)

### <mark class="hltr-pink format">Pourquoi utiliser une Queue</mark>
- Scénario où il y a un concept temporel/séquentiel d'ordre
	- exemple avec une file d'attente
- Pas besoin de gérer les indices concrètes
- Pourtant besoin d'un ordre séquentiel pour les éléments

### <mark class="hltr-pink format">Pourquoi utiliser une Deque</mark>
- Même argument que pour Queue
- Lire seulement de la tête/ajouter seulement à la queue trop restrictif

### <mark class="hltr-pink format">Pourquoi utiliser une PriorityQueue</mark>

 - Besoin d'un ordre
 - Ordre dynamique
 - Pas besoin d'un accès aléatoire

### <mark class="hltr-pink format">Pourquoi utiliser un Set</mark>
- Ordre n'est pas important
- Elément dupliqué doivent être évités
- Efficace
