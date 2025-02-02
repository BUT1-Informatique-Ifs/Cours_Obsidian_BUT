# <mark style="font-weight:bolder; color:white; background: #D2B3FFA6;">Paquetages</mark>

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Quoi ?</mark>
- Collection de :
	- Classes
	- Interfaces
	- Enumérations
- Mot clé `package`
	- a utiliser avant la déclaration de la classe
	- Par convention : nom en minuscule

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Pourquoi ?</mark>
- Dans un projet Java, on peut avoir 2 classes Rectangle
	- La première définit les méthodes géométriques
	- La deuxième gère l'affichage graphique

Cela permet de rendre l'application modulaire

- Pour un code souvent réutilisé :
	- Le placer dans un paquetage stocké dans une location centrale
	- Permet que le code soit changé que dans le paquetage où il est

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Création</mark>
- Physiquement, cela crée un dossier avec le nom du paquetage (dans /src et dans la pile)
- Au plus haut niveau, on ne peut pas déclarer un paquetage `private` ou `protected`

- Pour créer un sous-paquetage, le nom du fichier doit avoir un préfixe `nom.nomPaquetage`

## <mark style="font-weight:bolder; color:white; background: #BBFABBA6;">Utiliser un paquetage</mark>

1. mot clé `import` après la déclaration du paquetage et avant la déclaration de la classe
2. utiliser tout le nom du paquetage pour accéder à une méthode `nomPaquetage.laMethode()`


