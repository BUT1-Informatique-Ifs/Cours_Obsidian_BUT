# <mark class="hltr-pink format">TD5 - Classes abstraites et interfaces</mark>

## <mark class="hltr-green format">Exercice 1 - Les classes abstraites</mark>

### <mark class="hltr-pink format">Q1</mark>
```java
public abstract class Vehicule{
	protected String nom;
	public Vehicule(String nom){
		this.nom=nom;
	}
	public String getNom(){return this.nom};
	public void setNom(String nom){this.nom = nom};
	public abstract String getCategorie();
	public abstract float getVitesseMaximum();
	public boolean estVitessePossible(float v){
		this.getVitesseMaximum >=v;
	}
}
```


### <mark class="hltr-pink format">Q2</mark>

```java
public class BateauARames extends Vehicule{
	protected int nbRameurs;
	public BateauARames(String nom, int nbRameurs){
		super(nom);
		this.nbRameurs = nbRameurs;
	}

	@Override
	public String getCategorie(){
		return "Bateau";
	}

	@Override
	public float getVitesseMaximum(){
		return this.nbRameurs*0.5f;
	}
}
public class Voiture extends Vehicule{
	protected int puissance;
	public Voiture(String nom, int puissance){
		super(nom);
		this.puissance = puissance;
	}

	@Override
	public String getCategorie(){
		return "Voiture";
	}

	@Override
	public float getVitesseMaximum(){
		return this.puissance*1.5f;
	}
}
```
### <mark class="hltr-pink format">Q3</mark>

```java
public class Garage{
	Vehicule[] parking;
	public static void main(){
		parking[0] = new Voiture("Porsche", 450);
		parking[1] = new Voiture("RAM", 250);
		parking[2] = new BateauARames("Voilier", 100);
		parking[3] = new BateauARames("Jsp", 180);

		for(int i=0; i<parking.length; i++){
			System.out.println("Nom : " + parking[i].getNom()+" Categ : " + parking[i].getCategorie() + " VitMax : " + parking[i].getVitesseMaximum());
		}
	}

	public boolean sup15Possible(Voiture v){
		return v.getVitesseMaximum() >= 15;
	}
}
```

## <mark class="hltr-green format">Exercice 2 - Que fait ce programme</mark>


- int valeur(){return nombre} retournera une erreur car sans spécifier, valeur() est de visibilité package-protected alors que la déclaration de la méthode valeur() de l'interface est public.
- 2eme erreur est valeurBis() car on a une collection de InterfaceValeur alors que cette méthode est pas dans l'interface.

## <mark class="hltr-green format">Exercice 3 - Animaux</mark>

```java
public class Animal{
	protected String nom;

	public Animal(String nom){
		this.nom=nom;
	}
}

public class Mammifere extends Animal{

	public Mammifere(String nom){
		super(nom);
	}

	public String toString(){
		return "Je suis un animal de nom " + this.nom + ". Je suis un mammifère.";
	}
}

interface Deplacement{
	public void seDeplacer();
}

interface Raisonnemennt{
	public void reflechir();
}


public class Chien extends Mammifere implements Deplacement{
	
}

public class Homme extends Mammifere implements Deplacement, Raisonnement{

}
```