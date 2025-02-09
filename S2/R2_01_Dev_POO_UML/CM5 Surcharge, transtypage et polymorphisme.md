# <mark class="hltr-purple format">Surcharge, transtypage et polymorphisme</mark>

Conversion dans l'ordre : 
- byte => int => long => float => double
## <mark class="hltr-green format">Transtypage</mark>

```java
(type)maVariable;
```

Exemple :
```java
long a = 10.1;
System.out.println((int)a);
```

## <mark class="hltr-green format">instanceOf vs getClass()</mark>
### <mark class="hltr-pink format">getClass</mark>

retourne la classe de l'objet


### <mark class="hltr-pink format">instanceOf</mark>
retourne vrai ou faux si A est une instance de B

Exemple :
```java
A a=new A();
B b=new B();

System.out.println(b instanceOf a); // VRAI
System.out.println(a instanceOf b); // faux
```

## <mark class="hltr-green format">this</mark>

On peut utiliser this : `this()` pour exploiter le constructeur de la classe.