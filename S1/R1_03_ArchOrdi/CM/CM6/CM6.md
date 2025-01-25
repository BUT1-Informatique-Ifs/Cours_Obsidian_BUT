# Opération NON ()
	Fait le complément à 1 de la valeur de la variable
  Base 2 : 
Base 16 : chiffre jusqu'à 15, de combien ? 

# Opération Décalage à gauche (SHL)
Base 2 : 
	a=0110 1010
	a<<4 = 1010 0000
Base 16
	a=6A
	a<<4 = A0

# Opération Décalage à droite (SHR)
Base 2 : 
	a=0110 1010
	a>>3 = 0000 1101
Base 16
	a=6A
	a>>3 = 0D

# Application d'un <mark class="hltr-orange">ET</mark> avec masque de donnée

Base 2 : 
	0110 1010
% 
	0000 0011
----
0000 0010
Base 16 (passer par la base 2 pour faire l'opération)
	6A
&
	0F
----
0A

# Application d'un <mark class="hltr-orange">OU</mark> avec masque de donnée
Base 2 : 
	0110 1010
| 
	0000 0011
----
0110 1011
Base 16 (passer par la base 2 pour faire l'opération)
	6A
|
	0F
----
6F

# Application d'un <mark class="hltr-orange">OUEX</mark> avec masque de donnée
Base 2 : 
	0110 1010
| 
	0000 0011
----
0110 1001
Base 16 (passer par la base 2 pour faire l'opération)
	6A
|
	0F
----
65

# Histoire de l'info

....


...



# <mark class="hltr-blue">Le système informatique</mark>
	Matériel
	Logiciel

## Le but
	I/O (entrée clavier, etc..) et (sortie : disque, etc..)

### Structure
	Processeur
	Zone de mémoire morte (ROM, EPROM, ..)
	Zone de mémoire vive (RAM)
	Périphériques

	Bus de donnée 
		(circulation des donnéees, 
		mais aussi des instructions entre les 4 grands blocs)
	Bus d'adresse
	Bus de contrôle

### Ports I/O
	Port d'entrée (composé de tampons à 3 états (0, 1, Z)
	Port de sortie (composé de bascules D)

### Périphériques d'entrée
	Un flux de données qui peut venir :
		Du réseau
		D'une lecture d'information sur disque
		D'une saisi clavier, ..

### Périphériques de sortie
	Un signal
	Un flux de données
	Un affichage, un son..

### Périphériques d'I/O (les 2)
	Modem
	Cartes réseau
	Disque dur, carte mémoire, ..
	Imprimantes/scanners, ..


### Gestion des I/O
Par

	1. Lecture intermittente
	2. Interruptions
	3. Accès Direct à la Mémoire (DMA=> DIrect Memory Access)

### Performances
Ce qui influence : 

	Puissance du processeur
	La mémoire disponible
	Le temps consacré aux opérations I/O
_voir **swaping**_

	Charge du processeur
	Charge du dispositif I/O

Si ressources insuffisantes => Saturation
## <mark class="hltr-yellow">Architecture des Ordinateurs</mark>

8 Lois :

	Gilder
	Morris : nb de Gbits/pouce double tous les ans
	Objets Connectés : nb d'obj tagués double tous les ans
	Moore : nb de transistors d'un microprocesseur double tous les 18 mois (plus possible)

	Wirth : les prog ralentissent + vite que le matos accélère
	Koomey
	Big Data
	Metcalfe

=> Depui