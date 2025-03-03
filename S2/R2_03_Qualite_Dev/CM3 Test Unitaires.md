# <mark class="hltr-purple format">CM 3 - Les tests unitaires</mark>

4 familles de tests :
- test unitaire (seul) :
	- sur une portion de code (classe méthode, ..)
- test d'intégration (les éléments entre eux)
- test système (le tout dans différents contextes logiciels)
- test d'acceptation (recette)

Assertions en JUnit5
- assertTrue(boolean r)
- assertFalse(boolean r)
- assertEquals(Object t, Object r)
- ....


3 principes essentielles pour un code de qualité :
- lisibilité
- documentation
- tests unitaires

Les règles du test propre : FIRST
- Fast (doivent être rapide)
- Independant (pas de tests qui dépendent du résultat de d'autres tests)
- Repeatable (possibilité de le répéter)
- Self-validating (renvoie vrai ou faux)
- Timely (l'écriture du test doit être réalisé avant le code)

Test Driven Development : C'est le test qui conduit le développement =>  règles :
1. Ne pas écrire de code qui n'est pas rendu nécessaire par un test
2. Ne pas écrire plus dans un test unitaire que ce qui suffit à faire échouer le test
3. Ne pas écrire plus de code de prod que ce qui permet de passer le test