
# Les classes abstraites

## Abstract
- Les classes abstract peuvent avoir un constructeur
- On ne peux pas faire new ClasseAbstraite()
- Pour utiliser le constructeur, il faut utiliser super dans la classe qui hérite de la classe abstraite
- Si on a définit des méthodes abstraites, il faut forcément les redéfinir dans la classe qui hérite de la classe abstraite

## Interface
- Java ne permet pas l'héritage multiple
	Une interface est une liste de méthodes (prototype) qu'une classe doit implémenter.

- Une classe java peut implémenter plusieurs interface :
	- avec le mot clé implements

Exemple :

```java
public interface Enregistrable {
	public boolean enregistreDans(Fichier f);
}
public interface Supprimable {
	public boolean supprime(Fichier f);
}

class Test implements Enregistrable, Supprimable{
	//....
}
```
### Héritage entre interface
- On peut faire de l'héritage entre interface