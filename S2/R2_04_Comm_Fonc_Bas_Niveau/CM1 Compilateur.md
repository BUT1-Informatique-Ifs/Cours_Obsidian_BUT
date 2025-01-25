# <mark class="hltr-purple hltr-bold">Compilateur</mark>

## <mark class="hltr-green hltr-bold">Compilateur vs Interpréteur</mark>
- Compilateur : on traduit tout le fichier source en code binaire (ex : gcc pour le C)
- Interpréteur : le code du fichier est traduit en code binaire ligne à ligne, et exécuté (ex : les navigateurs web)
## <mark class="hltr-green hltr-bold">Caractéristiques du compilateur</mark>
Le compilateur traduit le fichier en code binaire selon le processeur donné. (sur Linux/MacOS/Windows, cela peut nécessiter de recompiler le fichier source)

##### <mark class="hltr-grey hltr-bold">Étape de la compilation en C</mark>
- Le préprocesseur prend les .c et les .h (les lib nécessaires) et fait un seul fichier. Il l'envoie au compilateur.
- Le code source est traduit en assembleur
- Il est traduit en binaire et stocke le binaire dans un .o
- L'éditeur de lien combine les .o et produit un fichier exécutable
- **On peut utiliser -v pour voir les différentes étapes**
**L'assembleur et le préprocesseur sont des compilateurs**

### <mark class="hltr-pink hltr-bold">Décompilateur</mark>
- C'est un compilateur particulier : il prend des fichiers binaires et produit en sortie un programme équivalent dans le langage de programmation original
- Souvent utilisé en rétroingénierie pour comprendre un programme dont le code source n'est pas disponible. Par exemple, pour essayer de trouver une backdoor ou autre.
- Certains programmes sont compilés avec des **compilateurs obfuscateurs** dont l'objectif est de rendre difficile la décompilation du code binaire. Le code source sera incompréhensible pour un humain.

### <mark class="hltr-pink hltr-bold">Structure d'un compilateur</mark>
Il doit :
- lire le code source
- vérifier sa validité
- générer le code binaire

Il effectue plusieurs analyses :
- analyse lexical
- analyse syntaxique
- analyse sémantique

#### <mark class="hltr-blue hltr-bold">Analyse lexical</mark>
- Consiste à diviser la séquence de caractères du fichier source en "jetons" (sous-séquence de caractères comme une ponctuation, etc..)
- Il y a généralement 2 types de jetons : les jetons utiles et ignorés (les espaces, etc..)

#### <mark class="hltr-blue hltr-bold">Analyse syntaxique</mark>
- Consiste à vérifier l'organisation des caractères (pour identifier les erreurs de syntaxe dans un langage)

#### <mark class="hltr-blue hltr-bold">Analyse sémantique</mark>
- Consiste par exemple à vérifier que une variable locale n'est pas utilisé avant d'être initialisée. Ou s'il y a une erreur de type.

## <mark class="hltr-green hltr-bold">Caractéristiques de l'interpréteur</mark>
- C'est un programme qui exécute du code source que ce dernier a compilé
- Certains interpréteurs sont interactifs : ils exécutent le programme ligne à ligne selon ce que l'utilisateur tape.
- Ils sont réflexifs car ils peuvent exécuter des morceaux de code source.

### <mark class="hltr-pink hltr-bold">Structure d'un interpréteur</mark>
- Le générateur de code est remplacé par un exécuteur de code (alors qu'un compilateur, c'est l'inverse)


## <mark class="hltr-green hltr-bold">Les différentes étapes du compilateur C</mark>
### <mark class="hltr-pink hltr-bold">4 Étapes</mark>
1. préprocesseur (cpp -> fichier.i -> option -E)
2. compilateur (cc1 -> fichier.s -> option -S)
3. assembleur (as -> fichier.o -> option -c)
4. éditeur de liens (ld -> fichier a.out)

Les 2 premiers fichiers sont compréhensible par l'homme.
Les 2 suivants sont en binaire.
Enfin le dernier fichier est un binaire exécutable.

GCC supprime les fichiers intermédiaires à la fin de la compilation.

### <mark class="hltr-pink hltr-bold">Les options relatives aux erreurs et warnings</mark>
- -Wall : les warnings
- -Wconversion : affiche des warnings en cas de cast implicit et de perte de précision
- -Werror : demande au compilateur de traiter les warnings affichés en tant qu'erreurs

### <mark class="hltr-pink hltr-bold">Compiler en mode debug et optimisations</mark>
- -g : pour compiler en mode debug
- -O0 : aucune optimisation demandée
- -O1 : un premier niveau d'opti qui conserve une taille de l'exécutable minimale
- -O2 : opti intermédiaire, avec un bon compromis sur la taille du fichier 
- -O3 : toutes les opti mais la taille de l'exécutable conséquent

### <mark class="hltr-pink hltr-bold">Compilation pour la production</mark>
`gcc -Wall -DNDEBUG -O2 fichier1.c fichier2.c -o nom_fichier`

### <mark class="hltr-pink hltr-bold">Le préprocesseur CPP</mark>
- Ce programme est exécuté lors de la première phase de la compilation du fichier source. Il effectue des modifications textuelles sur le fichier source.
- Introduite par #
Exemple :
- #define 
- #include
- #if, #else, #endif, #elif, #ifndef

#### <mark class="hltr-blue hltr-bold">Spécifier un symbole</mark>
`gcc -Dnomsymbole fichier.c`

### <mark class="hltr-pink hltr-bold">Débogueur ddd</mark>
- Debogueur en interface graphique
### <mark class="hltr-pink hltr-bold">Débogueur GDB</mark>
- Permet de lancer le programme et d'arrêter l'exécution à un endroit précis, d'examiner et de modifier la variable au cours de l'exécution. Il exécute aussi pas-à-pas le code.
- Il faut spécifier -g pour utiliser gdb
- Fonctionne en CLI
- Il examine le fichier core en cas d'arrêt brutal du processus.
	- il faut changer la valeur de ulimit (linux) pour augmenter les limites de ressources autorisées par le shell


#### <mark class="hltr-blue hltr-bold">Désassembler avec GDB</mark>
- Je sais plus

### <mark class="hltr-pink hltr-bold">La compilation séparée</mark>
- La commande "nm" permet de visualiser la table des symboles qui sont dans un fichier binaire. Elle affiche différentes informations
- Les symboles sont les informations qui sont réservés en mémoire par le fichier

## <mark class="hltr-green hltr-bold">Make et Makefile</mark>
### <mark class="hltr-pink hltr-bold">L'utilitaire Make</mark>
- Permet de réaliser la compilation séparée de façon automatique (quand on a bcp de fichiers par exemple).
- C'est un fichier de configuration
Forme du fichier Makefile:
	Cible : dépendances
		Commandes

- Cible : le nom du binaire exécutable par exemple
- Dépendances : les fichiers qu'on a besoin pour compiler
- Commandes : les commandes que l'on veut utiliser (gcc; etc..)

#### <mark class="hltr-blue hltr-bold">Pour faire une compilation totale</mark>
`Make all`

## <mark class="hltr-green hltr-bold">Autres outils </mark>
- gprof : outil de profilage pour savoir quel partie du code passe la plus grande partie de son temps d'exécution
- strace : outil de traçage de tous les appels systèmes effectués par le prog
- splint : recherche d'erreur sémantique
- strip : retirer les info symboliques de debogage d'un fichier
- indent : met en forme un fichier source suivant un style donné
- time : fournit trois temps machine à la fin de l'exec de la commande passé en paramètre  (temps total d'horloge, passé par le processus en mode utilisateur et système)