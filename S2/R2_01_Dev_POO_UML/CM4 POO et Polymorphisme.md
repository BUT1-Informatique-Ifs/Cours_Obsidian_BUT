# <mark style="font-weight:bolder; color:white; background: #D2B3FFA6;">POO et polymorphisme</mark>

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Notion d'héritage</mark>

C'est la possibilité de définir une classe comme une spécialisation d'une autre classe existante
- Cela permet de définir une hiérarchie de classes
- Chaque classe va hériter d'une autre

- On peut ajouter des méthodes et propriétés aux classes héritées d'une autre
- On peut aussi redéfinir la classe parent

	Supposons qu'on a une classe couleur avec des méthodes

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">En java</mark>

 - Pour hériter de cette classe, on utilise le mot clé `extends`
 ```java
 public class Point2DColore extends Point2D
 ```
La classe Point2DColore va hériter des propriétés et des méthodes de la classe Point2D


<mark style="font-weight:bolder; color:white; background: #FF5582A6;">Toute les classes héritent de la classe Object. C'est la classe racine</mark>

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Mot clé super</mark>

- La méthode super() permet d'appeler le constructeur de la classe parent.
- super.toString() + `laMethode` permet d'appeler une méthode de la classe parent

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Private et protected</mark>

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Private</mark>

Les attributs avec le mot clé `private` ne sont pas accessibles aux classes dérivés ni aux classes du même paquetage.
### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Protected</mark>

Les attributs avec le mot clé `protected` sont accessibles aux classes dérivés et aux classes du même paquetage.
## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Le polymorphisme</mark>

- C'est un concept puissant en POO

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Définition</mark>
C'est la possibilité de manipuler des objets sans connaître exactement la classe de ces objets, à condition de posséder :
- une super-classe commune
- des méthodes avec la même signature (héritées ou redéfinies)

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Redéfinition d'une méthode</mark>

- Il faut la réécrire en conservant la même signature et le même type de retour
- @override permet d'informer le compilateur de la redéfinition
- Pas obligatoire d'utiliser @override
##### <mark style="font-weight:bolder; color:white; background: #CACFD9A6;">Exemple</mark>

```java
public class Point2D{
	@override
	public String toString(){
		return ....
	}
}
```

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Héritage et instanceof</mark>

- Le mot clé instanceof permet de vérifier si un objet dérive bien d'une classe donnée
## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Le transtypage</mark>

- Il est possible de convertir une classe en une autre seulement si :
	- on la convertie en une sous-type ou vers une super-classe

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">En une sous-classe (Explicite)</mark>

On met la classe que l'on veut convertir entre parenthèse : MaClasse t = (MaClasse) new Point2D();

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Héritage et final</mark>

- Si on ajoute final à une classe, on ne peut pas modifier la méthode dans une sous-classe