# <mark class="hltr-purple format">CM4 - CPU</mark>

## <mark class="hltr-green format">Processeur</mark>
- C'est le coeur de l'ordinateur
- Contient des coeurs physiques et logiques
- Différents fabricants (AMD/Intel, ..)
### <mark class="hltr-pink format">Fonctionnement</mark>

- Les registres : permettent de mémoriser les informations/instructions
- l'ALU : Exécute tout les calculs que le proc peut réaliser
- l'Unité de Commande permet d'exécuter les instructions (les programmes) (Important pour la rapidité du proc)

Le proc embarque un cache interne pour éviter d'aller chercher les données redondantes dans la RAM. Cela permet d'accélérer les traitements.

La communication avec les périphériques plus lent se fait à travers le chipset.

### <mark class="hltr-pink format">Le BUS</mark>

- Ensemble de fils qui va transférer des données entre les différents composants électroniques de l'ordinateur et le CPU

Il existe 3 grands BUS :
- le bus d'adresse
- le bus de données
- le bus de contrôle (spécifie le type d'action)

### <mark class="hltr-pink format">Architecture du CPU</mark>

2 architectures de processeur :
- Harvard : La mémoire est intégré avec l'ALU et l'U
- Von Neumann : La mémoire est séparé de l'ALU et de l'Unité de Commande

<mark class="hltr-red format">accumulateur : registre permettant de stocker les résultats intermédiaires lors d'un calcul</mark>

### <mark class="hltr-pink format">Le jeu d'instruction</mark>
- Les plus connus : 32 bits et 64 bits (qui peuvent être traité en même temps par le proc)
- Différents types d'instructions :
	- x86
	- AMD64
	- ARM
	- ..
C'est pour cela que une compilation n'est pas universelle car elle diffère selon le jeu d'instruction du proc.

<mark class="hltr-red format">socket : endroit où le proc vient s'insérer sur la carte mère</mark>

### <mark class="hltr-pink format">Les composants du proc</mark>

#### <mark class="hltr-blue format">L'horloge</mark>
- Fournit un signal électrique régulier pour synchroniser le proc. Exprimée en GHz (3 GHz = 3 milliards d'opérations par seconde)
- Le proc possède une fréquence de base et à cette fréquence, on applique un coeff multiplicateur CPU.
- Pour augmenter la fréquence du proc, on peut augmenter le coeff multiplicateur du CPU, c'est l'overclocking.

Depuis 2006, la fréquence d'horloge n'augmente presque plus car cela fait beaucoup chauffer. Les constructeurs visent alors à augmenter le nombre de cœurs du CPU.

#### <mark class="hltr-blue format">Les coeurs (ou cores)</mark>
- Possède une UAL, des registres et une unité de commande. C'est un "mini processeur".
- Un cœur peut exécuter un prog de façon autonome.
- Pour bénéficier des performances des processeurs multicœurs, il faut que les programmes aient été conçu pour optimiser leur fonctionnement avec plusieurs cœurs.
- Pour obtenir la fréquence d'horloge de chaque cœur, on divise la fréquence du CPU par le nb de cœurs physiques.
#### <mark class="hltr-blue format">Les cœurs logiques</mark>
- C'est un découpage d'un cœur physique en deux par la technologie (SMT chez AMD et HyperThreading chez Intel)
- Il peut donc gérer 2 files d'attente au lieu d'une seule.
- Le but est que chaque cœur soit utilisé au maximum pour optimiser l'utilisation du proc

#### <mark class="hltr-blue format">La mémoire tampon</mark>
- C'est la mémoire cache interne au proc.
- Permet d'éviter les accès mémoires aux RAM
- Mémoire cache > RAM (en vitesse)

#### <mark class="hltr-blue format">Les niveaux de mémoire cache</mark>
- Cache L1 (premier niveau) : 
	- très rapide
	- séparés en 2 parties :
		- cache d'instructions
		- cache de données
- Cache L2 (second niveau) : 
	- moins rapide que cache L1
	- va contenir des données
- Cache L3 (troisième niveau) :
	- encore moins rapide mais plus grande capacité

Tous les cœurs du CPU partagent le même cache L3

### <mark class="hltr-pink format">UAL du processeur</mark>

- Effectue des opérations arithmétiques sur des nombres entiers et logiques au niveau du bit.

### <mark class="hltr-pink format">Les registres</mark>

- Case mémoires internes rapides aux proc
- Permet de stocker des info intermédiaires ou utiles comme les données traités par l'UAL, 
Certains registres particuliers :
- registre accumulateur
- registre unité de commande

## <mark class="hltr-green format">Le langage assembleur</mark>

- langage bas niveau
- lié à l'architecture du proc
- différentes instructions (LDR ; STR ; ADD ; SUB ; MOV ; B; ....)

## <mark class="hltr-green format">Les registres 16bits du proc</mark>

Ce sont les registres du processeur Intel 8086, un ancien proc.