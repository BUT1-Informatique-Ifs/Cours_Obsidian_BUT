# <mark class="hltr-purple format">Interfaces et énumérations</mark>
## <mark class="hltr-green format">Dans les interfaces</mark>

### <mark class="hltr-pink format">Variables dans interfaces</mark>
- Doivent toujours être iniatilisées

### <mark class="hltr-pink format">Méthodes dans interface</mark>

- Peuvent être déclarées avec :
	- default
	- static

## <mark class="hltr-green format">Dans les énumérations</mark>
- C'est une collection de constantes
- mot clé enum pour la déclarer
- Toutes les énumérations sont enfants implicites de java.lang.enum
- Traduit en classe pendant la compilation :
	- Suffix.java
	- Déclaration public (protected) enum
- Méthodes implicitement déclarées :
	- Exemple : public static values()

- Peut étendre d'une interface
- Ne peut pas hériter d'une autre énumération

Exemple :
```java
public enum Planet{
	MERCURE, VENUS, TERRE, MARS, NEPTUNE
}
```

- Peut avoir un constructeur, des méthodes ou encore des propriétés

