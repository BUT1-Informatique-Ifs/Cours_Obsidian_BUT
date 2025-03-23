## <mark class="hltr-green format">Programmation événementielle</mark>

	Les événements imposent l'ordre d'exécution
	On explique en code comment la machine réagit quand certains événements
	sont déclenchés

### <mark class="hltr-pink format">En JavaFX</mark>
Différents événements :
- ActionEvent
- DialogEvent
- InputEvent
- WebEvent
- ...

### <mark class="hltr-pink format">Les fonctions Lambda</mark>

En Java, on peut écrire des fonctions sans nom.
Les fonctions lambdas peuvent utiliser :
- des variables statiques
- des variables d'instance
- des variables locales "effectively final"

### <mark class="hltr-pink format">Références de fonctions</mark>
- On peut utiliser des références de fonctions :
	- statiques
	- dynamiques
## <mark class="hltr-green format">Patron MVC</mark>*

- La vue connait le modèle
- La vue connait le contrôleur
- Le contrôleur connait la vue
- Le contrôleur connait le modèle
- Le modèle ne connait pas la vue
- Le modèle ne connait pas le contrôleur
