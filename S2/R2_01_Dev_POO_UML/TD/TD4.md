# TD4 - Polymorphisme

## <mark class="hltr-green format">Exercice 1 - Polymorphisme</mark>

### <mark class="hltr-pink format">Q1</mark>

La trace d'exécution est correcte. Cela veut dire que quand on affiche l'initialisation de l'instance, elle affiche le nom de la classe suivi de l'adresse mémoire. On peut déduire que toString n'a pas été faite dans la classe.

### <mark class="hltr-pink format">Q2</mark>
- Il y aura une erreur à boisson.getDegreAlcool car la classe Boisson n'a pas de méthode getDegreAlcool (erreur de compilation)
- boissonForte = boisson ne marche pas car on a classeFille = classeMere
	- pour résoudre, il faut caster : boissonForte = (BoissonAlcoolisee) boisson;
- boissonFort = eau compile mais renverra une exception car eau n'a pas de méthode getDegreAlcool()

### <mark class="hltr-pink format">Q3</mark>

```java
ArrayList<Boisson> boissons = new ArrayList<Boisson>();
```

Pour parcourir :
```java
for(int i=0; i<boissons.size(); i++){
	System.out.println(boissons.get(i).getNom();
	System.out.println(boissons.get(i).getPrix();
	if(boissons.get(i) instanceof BoissonAlcoolisee){
		System.out.println((BoissonAlcoolisee)(boissons.get(i)).getDegreAlcool());
	}
}
```

### <mark class="hltr-pink format">Q4</mark>

La trace d'exécution de la Q1 est modifié et quand on affiche jus ou porto, on aura donc la chaîne de caractère renvoyé avec toString().

Oui, on peut simplifier l'affichage en appelant toString() pour chaque instance de Boisson

## <mark class="hltr-green format">Exercice 2 - Application de l'héritage aux employés d'une entreprise</mark>

```java
class abstract Employe{
	protected String name;
	public Employe(String name){
		this.name = name;
	}

	public abstract float getSalaire();

	@Override
	public String toString(){
		return "Nom : " + this.name + " Salaire : " + this.getSalaire();
	}
}

class GoodEmploye extends Employe{
	private double nbHeures;
	private double tarifHoraire;
	private double pourcentageHeuresSupp;
	private static final double HEURESDUES = 39.0;
	
	public EmployeBetter(String name){
		super(name);
		this.nbHeures = 0;
		this.tarifHoraire = 0;
		this.pourcentageheuresSupp = 0.3;
	}
	public EmployeBetter(String name, double nbHeures, double tarifHoraire, double pourcentageHeuresSupp, boolean mieuxPaye){
		super(name);
		this.nbHeures = nbHeures;
		this.tarifHoraire = tarifHoraire;
		this.pourcentageHeuresSupp = pourcentageHeuresSupp; 
		if(mieuxPaye) this.pourcentageHeuresSupp = 0.5;
		else this.pourcentageHeuresSupp = 0.3;
	}

	public void setInfoSalaire(){
		
	}

	public float getSalaire(){
		double res 0;
		if(this.nbHeures < this.HEURESDUES) return this.nbHeures * this.tarifHoraire;
		else return (this.HEURESDUES * this.tarifHoraire + (this.nbheures - this.HEURESDUES) * (1+this.pourcentageHeuresSupp) + this.tarifHoraire);
	}
}
```