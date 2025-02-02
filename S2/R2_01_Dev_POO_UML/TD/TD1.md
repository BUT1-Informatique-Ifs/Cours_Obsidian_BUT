# <mark style="font-weight:bolder; color:white; background: #D2B3FFA6;">Modélisation orientée objet</mark>

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Exercice 1 - Modélisation dépend du contexte</mark>
### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 1</mark>
- Pour un éleveur :
	- numéro
	- race
	- espèce
	- poids
	- taille
	- prix
- Pour un scientifique :
	- espèce
	- race
	- ordre, famille, genre
	- taille de population
	- région
	- nom  scientifique
	- taille maximal
	- taille actuel
	- age maximal
	- nb de battement de coeur par minutes
- Pour un propriétaire d'un animal de compagnie :
	- nom
	- date de naissance
	- espèce
	- numéro puce
	- statut de vaccin
	- poids
### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 2</mark>
Pour l'éleveur (dans l'ordre des attributs ci-dessus) :
- constant
- constant
- constant
- variable
- variable
- variable
Pour un scientifique :
- constant
- constant
- constant
- variable
- constant
- constant
- variable
- variable
- variable
- variable
Pour un proprio :
- constant
- constant
- constant
- constant
- variable
- variable
## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Exercice 2 - Attribut vs méthode d'objet</mark>

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 1</mark>

Avantages avec 2 attributs :
- moins de calcul
- code plus lisible
Inconvénients avec 2 attributs :
- plus d'attributs qui peuvent être inutiles
### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 2</mark>

1. Il faudrait juste un setter pour l'aire

2. Avec la version implicite, il faudrait faire ceci pour les getter
```java
public double getAire(){
	return Math.PI * Math.pow(this.rayon, 2);
}
```

```java
public double getCirconference(){
	return 2 * Math.PI * this.rayon;
}
```

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 3</mark>


```java
public void setRayon(double rayon){
	this.rayon = rayon;
}
```

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Exercice 3 - Lire et comprendre du code</mark>

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 1</mark>

Ligne par ligne :
- Déclaration d'une instance de LireCode e
- Déclaration et initialisation de LireCode e2
- Déclaration d'une variable j

- On modifie la propriété i de l'instance LireCode e2 à 5
- j prend la valeur de la propriété i de l'instance e2 avec e2.getI()
- On affiche la propriété response de l'objet (la classe) LireCode (qui est une constante)
- On affecte l'adresse de l'instance de LireCode e2 à l'instance LireCode e
- Passe l'attribut r à true de l'instance LireCode e
- Affiche e2.r `==` e.r (True ou False)
- Passe une ligne
- Modifie l'attribut i de l'instance LireCode e en prenant la valeur i de e2 et en ajoutant 2
- Concatène la valeur i de l'instance LireCode e2 avec un + et la valeur de i de l'instance LireCode e
- Affiche la chaîne de caractère de la méthode question1 et question2

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 2</mark>

Sur la troisième ligne :
- Sachant que j est un int, c'est 0
Sur la cinquième ligne :
- j = 5 (la valeur de i de l'instance LireCode e2)

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 3</mark>

Sur la première ligne :
- C'est un pointeur null
Sur la septième ligne :
- l'adresse de l'instance LireCode e pointe cette fois ci vers e2, soit l'instance de LireCode e2

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 4</mark>

Le programme affiche
```
42
true == true

7 + 7
What do you get if you multiply six by nine ?
```

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Exercice 4 - Les types de variable et leurs visibilités</mark>

### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 1</mark>
1; 2 et 3
1. var1 est une propriété qui peut être modifié plusieurs fois mais var2 peut être modifié qu'une seule fois car c'est une constante. Les 2 propriétés sont publiques, donc accessible en dehors de la classe principale
2. var1 n'est pas accessible en dehors de la classe et var2 est une variable statique, donc si on l'a modifie, toute les instances de l'objet auront la même valeur pour var2
3. var1 et var2 sont des attributs privés. Il faut des getters pour y accéder et un setter pour var1 car c'est une constante qui n'a pas encore été initialisé comparé à var2. Ils sont statiques donc si l'on change leurs valeurs, elles s'appliqueront à toute les instances de l'objet.
4. Pour var1, c'est un tableau. Il faut un getter et un setter. Pour i, cela n'a pas de sens car i est une variable local de la méthode.



### <mark style="font-weight:bolder; color:white; background: #FFB8EBA6;">Question 2</mark>

1. C'est une méthode d'objet (de classe). Les variables visibles sont dix (type int), a, b vrai, z