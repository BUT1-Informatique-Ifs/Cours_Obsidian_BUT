# <mark class="hltr-purple format">TD8 - Les collections</mark>

## <mark class="hltr-green format">Exercice 1</mark>

### <mark class="hltr-pink format">Q1</mark>

#### <mark class="hltr-blue format">1.</mark>

- Le programme initialise une liste lié d'Etudiant et en ajoute 4.
- Le programme affiche les étudiants (cela marche grâce à toString redéfinie dans la classe Etudiant)
- Crée un HashSet d'étudiant avec listeDEtudiant nommé ensembleDEtudiants
- Affiche ensembleDEtudiants
- Crée une PriorityQueue d'étudiant nommé pqDEtudiants
- Affiche pqDEtudiants

#### <mark class="hltr-blue format">2.</mark>

Il y a une erreur d'exécution : 
- c'est la PriorityQueue car il faut utiliser des compareTo

#### <mark class="hltr-blue format">3.</mark>

- Le premier affiche les étudiants
- Le deuxième affiche les étudiants
- Le troisième plante avant car la PriorityQueue n'est pas bien initialisé
### <mark class="hltr-pink format">Q2</mark>


```java
public class Etudiant implements Comparable{
	public int compareTo(Etudiant etu){
		return this.ID - etu.ID;
	}
}
```

Maintenant, le 3eme System.out.println() marche et donc l'affiche sera dans l'ordre :
- Alban
- Alban
- Bert
- Sophie

### <mark class="hltr-pink format">Q3</mark>

#### <mark class="hltr-blue format">1.</mark>

```java
public class ComparateurEtudiant implements Comparator<Etudiant>{
	public int compare(Etudiant etu1, Etudiant etu2){
	
		if(etu1.getNom().compareTo(etu2.getNom()) >0) return 1;
		if(etu1.getNom().compareTo(etu2.getNom()) <0) return -1;
		if(etu1.getPrenom().compareTo(etu2.getPrenom()) >0) return 1;
		if(etu1.getPrenom().compareTo(etu2.getPrenom()) <0) return -1;
		if(etu1.getFormation().compareTo(etu2.getFormation()) >0) return 1;
		if(etu1.getFormation().compareTo(etu2.getFormation()) <0) return -1;
		return 0;
	}
}
```

#### <mark class="hltr-blue format">2.</mark>

```markdown
- Fourrier
- Fourrier
- Germain
- Herzig
- Nutter
```

#### <mark class="hltr-blue format">3.</mark>

Car on ne sait pas dans quel ordre cela sera affiché (cela dépend de l'implémentation de la PriorityQueue)


### <mark class="hltr-pink format">Q4</mark>

#### <mark class="hltr-blue format">1.</mark>

```java

public boolean equals(Object a){
	if(this == a) return true;
	if(a == null) return false;
	if(a instanceof Etudiant){
		Etudiant etu = (Etudiant) a;
		return this.formation.equals(etu.formation) && 
		this.nom.equals(etu.nom) && this.prenom.equals(etu.prenom) && 
		this.noteMoyenneUE1 == etu.noteMoyenneUE1 && this.noteMoyenneUE2 == 
		etu.noteMoyenneUE2;
	}
	return false;
}

```
#### <mark class="hltr-blue format">2.</mark>

Cela ne change rien car HashSet utilise en premier le HashCode