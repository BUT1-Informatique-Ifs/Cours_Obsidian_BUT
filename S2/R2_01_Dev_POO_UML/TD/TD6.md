# <mark class="hltr-purple format">TD6</mark>

## <mark class="hltr-green format">Exercice 1</mark>
### <mark class="hltr-pink format">Q1</mark>
Il y a du code dans cette méthode alors qu'il n'en faut pas

### <mark class="hltr-pink format">Q2</mark>

Il faut retirer le code de la méthode aMethod

### <mark class="hltr-pink format">Q3</mark>

Oui, il n'y a pas de raison que cela compile pas.

### <mark class="hltr-pink format">Q4</mark>

Le nom de la méthode de l'interface A et B est le même alors que les types des arguments de `method` n'a pas changé (là il n'y a pas d'arguments).

## <mark class="hltr-green format">Exercice 2</mark>

### <mark class="hltr-pink format">Q1/Q2/Q3/Q4/Q5</mark>

```java
enum Couleur implements Melange{
	ROUGE(255, 0, 0, "rouge", "red"),
	VERT(0, 255, 0, "vert", "green"),
	BLEU(0, 0, 255, "bleu", "blue");
	MAGENTA(255, 0, 255, "magenta", "magenta");
	int rouge;
	int vert;
	int bleu;
	String fr;
	String en;
	Couleur(int r, int v, int b, String fr, String en){
		this.rouge = r;
		this.vert = v;
		this.bleu = b;
		this.fr = fr;
		this.en = en;
	}

	String getNom(String langage){
		if(langage == "en") return this.en;
		else return this.fr;
	}
	Couleur versRouge(){
		switch(this){
			case BLEU:
				return MAGENTA;
			case VERT:
				return JAUNE;
			default:
				return ROUGE;
		}
	}
	// idem pour versVert, etc..
}

public Interface Melange{
	public Couleur versRouge();
	public Couleur versVert();
	public Couleur versBleu();
}

```