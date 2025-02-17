# <mark class="hltr-purple format">Les exceptions</mark>

## <mark class="hltr-green format">Pourquoi les exceptions</mark>

- car sans les exceptions, compliqué d'indiquer qu'il y a une erreur dans le programme (renvoyer -1 n'est pas très indicatif, ..)
- Permet de traiter efficacement les erreurs 

### <mark class="hltr-pink format">Comment ça marche</mark>

- les exceptions :
	- déroutent le programme (comme un break, return, ..)
	- redirigé vers un gestionnaire d'exceptions

### <mark class="hltr-pink format">Pour travailler avec</mark>

- utiliser try et catch
- throw pour lever volontairement une exception

Toutes les exceptions héritent de la classe **Throwable** et possède 2 classes filles :
- Error
- Exception

On peut faire plusieurs catch pour traiter différentes exceptions

##### <mark class="hltr-grey format">Exemple</mark>
```java
try{
....
} 
catch(Exception1 e){

}
catch(Exception2 e){

}
..
```
### <mark class="hltr-pink format">Quelques méthodes de la classe Throwable</mark>
- String getMessage() => retourne le message détaillé de l'exception
- ...


## <mark class="hltr-green format">Créer des d'exceptions</mark>

- Il faut définir une classe `MonException` qui hérite de la classe Exception
- throws permet de dire à une méthode qu'elle peut retourner une exception ou plusieurs exceptions

##### <mark class="hltr-grey format">Exemple</mark>

```java
static void checkAge(int age) throws ArithmeticException {}
```


## <mark class="hltr-green format">Quand lever une exception</mark>
- Si le problème a été causé localement, on le traite intérieurement
- Si le problème vient de l'extérieur, on leve une exception
## <mark class="hltr-green format">Le mot clé finally</mark>

Lorsque l'on utilise un try catch, on peut utiliser le mot clé finally qui sera toujours exécuté, qu'il y ait une exception ou non.