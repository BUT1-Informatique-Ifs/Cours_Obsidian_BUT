# <mark class="hltr-purple hltr-bold">Découverte de Java</mark>

## <mark class="hltr-green hltr-bold">Pourquoi programmer en POO</mark>

- Besoins de types plus complexes
- Regroupement sémantique/logique
- Protection des données (pas de modif directe sur les attributs)
- Soutien/exige la programmation modulaire
## <mark class="hltr-green hltr-bold">Pourquoi Java</mark>

- Très facile à utiliser des composants déjà écrits
- Manipulation de référence (pointeur) simple
- Gestion de la mémoire dynamique automatique (il a un garbage collector) :
	- pas d'accès direct à la mémoire
- Maintenabilité du code facilitée
- Portabilité des codes sources et des applications :
	- multi-plateformes
- Existe depuis 29 ans

## <mark class="hltr-green hltr-bold">Utiliser le Java</mark>
### <mark class="hltr-pink hltr-bold">Les types primitifs</mark>
- boolean : codé sur 1 bit (0 ou 1)
- char : codé sur 8 bits
- byte : codé sur 8 bits (2^8)
- short : codé sur 16 bits
- int : codé sur 32/64 bits
- long : codé sur 64/128 bits
- float : codé sur 32/64 bits
- double : codé sur 64/128 bits

### <mark class="hltr-pink hltr-bold">Les chaînes de caractères</mark>
- On l'utilise avec : String
- String n'est pas un type primitif mais peut être utilisé de la même manière
- On peut faire des opérations : + - etc.. (comme un type primitif)
- Il y a beaucoup de méthodes utiles :
	- substring()
	- split()
	- toLowerCase()/toUpperCase()
	- ...
- Majuscule au début car c'est un type complexe (chaque type primitif a un type complexe (qui est une classe))
### <mark class="hltr-pink hltr-bold">Syntaxe</mark>
- Déclaration des variables : `Double racine;` <-- Stocke une adresse
- Convention de nommage : String nomDeFamille;
- Transtypage des variables : ... = (int) ..
- Opérateurs binaires et unaires :  * et & n'existent pas
- Incrémentation : i++ ; ++i
- etc..

### <mark class="hltr-pink hltr-bold">Les classes</mark>
- Pour instancier une classe, on utilise le mot clé <mark class="hltr-red hltr-bold">new</mark>
##### <mark class="hltr-grey hltr-bold">Exemple</mark>
Cercle c;
c = new Cercle();

#### <mark class="hltr-blue hltr-bold">La visibilité</mark>
- public : visibilité publique, déconseillé car on peut accéder à cet attribut dans n'importe quelle autre classe
- private : visibilité privée, non accessible par les autres classes sans utiliser un getter/setter
- static : c'est une variable de classe, partagée par toutes les instances
- final : constante qui peut être initialisé dès la déclaration ou plus tard mais une seule fois (similaire à #define en C)

#### <mark class="hltr-blue hltr-bold">Vocabulaire</mark>
- Classe : schéma / moule
- Instance : avec new, on instancie la classe, la mémoire est réservée
- Référence : variable dont le type est une classe, l'adresse mémoire est stockée; si l'adresse n'est plus stocké dans une variable, l'adresse est supp par le garbage collector

### <mark class="hltr-pink hltr-bold">System.out.println()</mark>
- System : c'est une classe
- out : c'est une variable de classe
- println : c'est une méthode

### <mark class="hltr-pink hltr-bold">Les tableaux</mark>
- Regroupement de variables du même type
- Accès avec indice
- On n'est pas obligé de spécifier la taille du tableau
- Ce n'est pas obligatoire d'avoir un tableau rectangulaire
##### <mark class="hltr-grey hltr-bold">Exemple</mark>
`int [] t = {5, 4, 1}`

#### <mark class="hltr-blue hltr-bold">Plusieurs manières de déclarer un tableau</mark>
- C'est la même chose :
`int [] MonTableau;`
`int MonTableau[];`
`int MonTableau[] = {1, 2, 3}`

- On peut utiliser new pour créer un tableau :
	- `int t[] = new int[nbDeValeur];`

- Pour afficher la taille d'un tableau :
	- `System.out.println(MonTableau.length);`

#### <mark class="hltr-blue hltr-bold">Erreur si on sort du tableau</mark>
- java.lang.ArrayIndexOutOfBoundsException

