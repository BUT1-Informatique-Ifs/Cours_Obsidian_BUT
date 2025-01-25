# <mark style="font-weight:bolder; color:white; background: #D2B3FFA6;">Les méthodes</mark>
- Appeler une méthode d'un objet : `referenceObjet.nomDeLaMethode(listeParam);`
- S'il n'y a pas d'instance (de référence) de l'objet crée, alors on a un `NullPointerException`

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Get et Set</mark>
- On n'accède pas directement aux propriétés d'un objet
- A la place, on utilise des méthodes get pour récupérer un attribut et set pour changer la valeur d'un attribut

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Mot clé this</mark>
- Fait référence à l'objet courant (celui qu'on est entrain de modifier)
- Pour accéder à une méthode de l'objet sur lequel on est entrain de créer/modifier, on fait :
	`this.nomDeLaMethode();`

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Modifier l'état des attributs</mark>
- On est pas obliger d'utiliser des setter pour modifier la valeur d'un attribut (propriété)


## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">print et println</mark>
- System.out.print() // pas de passage à la ligne
- System.out.println() // passe à la ligne


## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Comparaison d'instances</mark>
- == compare les adresses mémoires des deux instances de l'objet
- Utiliser la méthode `instance1.equals(instance2)` et il faut la redéfinir car par défaut :
	- equals utilise == (donc compare juste les adresses)

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Copie d'objets</mark>
- Utiliser la méthode `MaClasse p2 = p1.Clone()` et il faut également la redéfinir

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Surchage des méthodes</mark>
- On peut redéfinir une méthode plusieurs fois avec le même nom mais il faut soit :
	- ne pas avoir le même nombre de paramètres
	- un type différent entre les 2 méthodes de même noms
	- ou encore changer l'ordre de paramètres


## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Méthodes statiques</mark>
- pas de this dans une méthode statique