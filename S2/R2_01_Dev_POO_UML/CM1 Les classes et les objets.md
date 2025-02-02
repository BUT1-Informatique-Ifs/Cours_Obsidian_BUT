# <mark class="hltr-purple hltr-bold">Les classes et les objets</mark>
## <mark class="hltr-green hltr-bold">POO</mark>
- Paradigme de programmation
- Fondé sur la programmation structurée
- Facilite la réutilisation de code existant
- Nouveaux concepts :
	- Objets
	- Encapsulation
	- Classes
	- Héritages et polymorphisme
- Les objets "vivent" en famille :
	- ils héritent du comportement de leurs aînés
	- tout en spécialisant leurs comportements

## <mark class="hltr-green hltr-bold">Le paradigme objet</mark>
- Objets : des entités uniques dans les programmes
- Classes qui les définissent
- Communication entre objets : passer de messages (appels de méthodes)
### <mark class="hltr-pink hltr-bold">Objets</mark>
- N'importe quel entité
##### <mark class="hltr-grey hltr-bold">Exemple</mark>
- Une entreprise
- Un cercle
- ..

### <mark class="hltr-pink hltr-bold">Attributs</mark>
- Les objets ont des attributs
##### <mark class="hltr-grey hltr-bold">Exemple</mark>
- Cercle :
	- Coordonnée x
	- Coordonnée y
	- ..

### <mark class="hltr-pink hltr-bold">Principe d'encapsulation des données</mark>
- Encapsulation en POO
	- la modif des données d'un objet n'est pas directement possible
	- seules les méthodes permettent de modifier les attributs de l'objet
- Communication entre objets : pas besoin de connaître quels sont les structures de données utilisés par ces différents objets 
#### <mark class="hltr-blue hltr-bold">Avantages de l'encapsulation</mark>
- Simplification de l'utilisation des objets
- Meilleur robustesse du programme
- Simplification de la maintenance de l'application

## <mark class="hltr-green hltr-bold">Notions de base en POO en Java</mark>
### <mark class="hltr-pink hltr-bold">Composition d'une classe</mark>
- La partie privée
- La partie publique
- Un constructeur :
	- l'instanciation d'une classe : fabrication des objets tout en conformité avec le schéma
	- un objet est une instance d'une classe

- Nommage de classes :
	- PascalCase
	- pas de verbe

#### <mark class="hltr-blue hltr-bold">Attributs et Méthodes</mark>
- camelCase
- Verbe pour les méthodes

### <mark class="hltr-pink hltr-bold">Visibilité</mark>
- public : accessible hors de la classe
- protected : accessible dans toutes les classes du package et ses dérivées
- (Si on met rien) : accessible dans toutes classes du package
- private : accessible uniquement dans la classe
	- Les méthodes ne sont appelables que par d'autres méthodes définies dans la classe
	- Les attributs ne sont pas accessibles que par des méthodes définies dans la classe

### <mark class="hltr-pink hltr-bold">Mot clé final</mark>
- final : sert à définir une variable à laquelle on peut affecter une valeur qu'une seule fois (une constante)

### <mark class="hltr-pink hltr-bold">Mot clé static</mark>
- Un attribut static est un attribut de classe, il est commun à l'ensemble des instances de la classe
### <mark class="hltr-pink hltr-bold">Les constructeurs</mark>
- Méthode spéciale qui est appelée lorsque l'objet est crée
- La classe peut avoir plusieurs constructeurs (pour par exemple, avoir des valeurs de défaut si la classe est instancié sans paramètres et un constructeur avec des paramètres si la classe est instancié avec des paramètres)
- Il y a un constructeur par défaut
- Toujours public et sans type de retour
- Souvent, il est appelé dans une autre classe (pas dans la même classe)
### <mark class="hltr-pink hltr-bold">Destruction d'un objet</mark>
- Lorsque la référence est perdue, le garbache collector supprime l'objet
- La destruction est asynchrone (géré dans un thread de basse priorité)
- Si l'objet possède la méthode finalize(), elle est appelé lorsque l'objet est détruit