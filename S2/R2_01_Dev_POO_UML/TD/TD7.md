# <mark class="hltr-purple format">TD7 - Questions d'examen</mark>

## <mark class="hltr-green format">Exercice 1</mark>

### <mark class="hltr-pink format">Question 1</mark>

1. Ne peut pas hériter d'autres classes/énumérations
2. Toutes les instances sont prédéfinies
### <mark class="hltr-pink format">Question 2</mark>

```java

// ecrire une ligne de code pour afficher le rayon de c2
System.out.println(c2.rayon);
// ecrire une ligne de code pour afficher le nombre de cercles
System.out.println(Cercle.nb);

```

### <mark class="hltr-pink format">Question 3</mark>

 ```java
 // 3.1 Quelles sont les variables accessibles ici et quelle est leur valeur ?
a=3;b=7;dix=10;vrai=true (car static) ; Autre.z ; c=42; this.dix="dix"

// 3.2 Quelles sont les variables accessibles ici et quelle est leur valeur ?
autre.y=13; Autre.z=15;vrai=true;a=3;b=7;dix="dix"; autre
```

## <mark class="hltr-green format">Exercice 2</mark>

### <mark class="hltr-pink format">Question 1 / Question 2</mark>

```java
public class Date{
	private int jour;
	private int mois;
	private int annee;

	public Date(int j, int m, int a){
		this.jour = j;
		this.mois = m;
		this.annee = a;
	}

	@Override
	public String toString(){
		return ""+this.jour+"/"+this.mois+"/"+this.annee;
	}

	@Override
	public boolean equals(Object o){
		// Identité
		if(o == this) return true;
		// Existance

		// Instance
	}
}
```