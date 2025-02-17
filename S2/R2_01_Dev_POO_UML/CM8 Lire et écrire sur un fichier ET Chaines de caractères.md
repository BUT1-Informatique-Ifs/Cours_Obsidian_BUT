# <mark class="hltr-purple format">Lire et écrire sur un fichier texte</mark>
## <mark class="hltr-green format">Files</mark>
- en une seule fois : 
	- `public static byte[] readAllbytes(Path);`
	- `public static List<String> readAllLine(Path, [Charset]);`
		- charset est par défaut à UTF-8
	-  `public static Path write()`
=> c'est dans la classe Files

## <mark class="hltr-green format">Path</mark>

- c'est une interface (et une classe)
- représente des fichiers, dossiers, ..
- Pour créer des Path: 
	- `static Path of(String first, ..)`
	- `static Path of(URI uri)`

##### <mark class="hltr-grey format">Exemple</mark>
```java
Path file = Path.of("/home/brice/exemple.js");
```


## <mark class="hltr-green format">Interface OpenOption</mark>
- objets qui configurent comment ouvrir/créer un fichier
- Implémentation StandardOpenOption : énumération

## <mark class="hltr-green format">Lire un fichier texte au fur et à mesure</mark>
- Il faut utiliser un BufferedReader /BufferedWriter
- static BufferedReader newBufferedReader(Path path, String charset) / static BufferedWriter
- Il faut utiliser try catch
- la méthode write écrit dans le buffer mais pas dans le fichier. C'est quand le buffer est plein que java utilise la méthode flush() pour écrire dans le fichier
En java, une ligne est terminé soit par:
- \n
- \r
- EOF

## <mark class="hltr-green format"> Fermer les ressources</mark>
- Il faut fermer le fichier comme en C avec la méthode close() de BufferedReader/BufferedWriter

# <mark class="hltr-purple format">Lire et écrire sur un fichier non-texte</mark>
- Utiliser BufferedInputStream/BufferedOutputStram
- on récupère des bytes

# <mark class="hltr-purple format">Manipuler des chaînes de caractères</mark>

## <mark class="hltr-green format">Créer des chaînes de caractères - StringBuilder</mark>

### <mark class="hltr-pink format">Construire une chaîne au fur et à mesure</mark>
- Récupérer chaîne finale avec .toString()

- méthodes principales :
	- append(..)
	- insertAt(..)

##### <mark class="hltr-grey format">Exemple</mark>
```java
StringBuilder sb = new StringBuilder("Notes :");
```

## <mark class="hltr-green format">Rechercher dans une chaîne</mark>
	CharSequence : interface implémentée en java
- boolean contains(CharSequence)
- boolean endsWith(String)
- boolean statsWith(String)
- int indexOf(Char)/lastIndexOf(Char)
- int indexOf(String)/lastIndexOf(String)

## <mark class="hltr-green format">Modifier une chaîne</mark>

- String replace(char, char)
- ...

## <mark class="hltr-green format">Quelques exemples de RegEx</mark>
- ^a => trouve "a" au début d'une ligne, mais pas dans "ba"
- b$ => "b" à la fin d'une ligne mais pas dans "ba"
- ...

## <mark class="hltr-green format">Diviser une chaîne en parties</mark>

- Pour récupérer des sous-parties, on utilise la méthode split(String)
	- renvoie un tableau

## <mark class="hltr-green format">Sérialisation</mark>
- procédé qui permet de rendre un objet ou un graphe d'objets de la JVM (Java Virtual Machine) persistant pour stockage ou échange et vice versa
- 2 méthodes :
	- writeObject
	- readObject