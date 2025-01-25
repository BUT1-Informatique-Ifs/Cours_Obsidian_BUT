# <mark class="hltr-blue hltr-bold">Les codes correcteurs d'erreurs</mark>

## <mark class="hltr-purple hltr-bold">Définitions</mark>

	C'est une technique de codage basée sur la redondance.

<mark class="hltr-red hltr-bold">Permet de corriger les erreurs de transmission</mark> d'une information sur une voie de communication peu fiable.

### <mark class="hltr-green hltr-bold">Différentes familles de codes</mark>
#### <mark class="hltr-pink hltr-bold">Codes en bloc (linéaire, cycliques ou non)</mark>

Le codage/décodage d'un code <mark class="hltr-red hltr-bold">dépend uniquement des informations de 
ce bloc</mark>.

#### <mark class="hltr-pink hltr-bold">Codes en treillis (convolutifs, récursifs ou non)</mark>

	Un code convolutif s'applique sur une suite infinie de symboles et 
	produit une suite infinie.

Le codage/décodage <mark class="hltr-red hltr-bold">dépend des informations d'autres blocs</mark> (généralement de blocs précédemment transmis).


### <mark class="hltr-green hltr-bold">Différents types de codes correcteur d'erreurs</mark>

- Code de Hamming
- Code de Golay
- Code de Reed-Müller (utilisé par la NASA pour les photos de mars)
- Code de Goppa (utilisé pour la cryptographie)
- Code de Xing
- Code de Reed-Solomon (utilisé sur les CD, DVD, Satellite, ADSL, ADSL2, ..)

# <mark class="hltr-blue hltr-bold">Codes en bloc (code correcteur d'erreurs)</mark>

## <mark class="hltr-purple hltr-bold">Définitions</mark>

	Un code en bloc est un code correcteur d'erreur traitant des 
	messages de longueur fixe.
### <mark class="hltr-green hltr-bold">Pourquoi les utiliser</mark>

- Les messages ont rarement une longueur fixe. Or, il est plus simple de développer une code correcteur d'erreurs pour des messages qui ont une longueur fixe.
- On va donc segmenter le message. 
  Dans un premier temps, le cas d'un message de longueur fixe est traité et pour le cas général, on va concaténer une suite de blocs. C'est le code convolutif.
- Le codage par bloc est le plus utilisé dans les applications téléinformatiques classiques car le codage/décodage est plus simple et plus rapide.

### <mark class="hltr-green hltr-bold">Utilisation</mark>

Un code ($\textcolor{red}{k}$, $\textcolor{blue}{n}$) code $\textcolor{red}{k}$ bits d'information (longueur initiale des mots) en un bloc de $\textcolor{blue}{n}$ bits (longueur du code). Le code est redondant car $\textcolor{blue}{n}>=\textcolor{red}{k}$.
![[Pasted image 20241010210207.png]]

## <mark class="hltr-purple hltr-bold">Notions importantes</mark>
### <mark class="hltr-green hltr-bold">Le poids de Hamming</mark>

C'est <mark class="hltr-red hltr-bold">le nombre de bit à 1</mark> qu'un mot w(N) contient.

##### <mark class="hltr-grey hltr-bold">Exemple</mark>

Poids de Hamming de : w(0<mark class="hltr-grey hltr-bold">1</mark>00<mark class="hltr-grey hltr-bold">11</mark>00) = 3

### <mark class="hltr-green hltr-bold">La distance de Hamming</mark>

#### <mark class="hltr-pink hltr-bold">Entre 2 mots</mark>

C'est <mark class="hltr-red hltr-bold">le nombre de bits qui diffèrent entre 2 mots</mark> d(N1, N2) de même longueur.
On l'obtient par le poids de Hamming du OUEX binaire ($\textcolor{red}{\oplus}$) des 2 mots.

#### <mark class="hltr-pink hltr-bold">D'un code</mark>

C'est la distance minimum entre tous les mots du code, définit par :
	$d_C = min\{\forall\ i \neq j, \; d(N_i\;, N_j) \}$
En d'autres termes, c'est <mark class="hltr-red hltr-bold">le nombre de bits le plus petit qui diffèrent entre tous les mots</mark> du code.

### <mark class="hltr-green hltr-bold">Capacité de détection (de correction) du code</mark>

	Définie par les erreurs qu'il est capable de corriger.

Une erreur simple .....

##### <mark class="hltr-grey hltr-bold">Exemple</mark>

Si on a une distance de Hamming = 3,
Alors la capacité de détection est <=2,
Et la capacité de correction <=1

<mark class="hltr-red hltr-bold">Plus la distance de Hamming est grande, meilleur est le code</mark>

## <mark class="hltr-purple hltr-bold">Codage</mark>

1. On code le message sous forme de $\textcolor{red}{b}$ caractères sur $\textcolor{blue}{a}$ bits. Le bloc de données est disposé sous une forme matricielle ($k=\textcolor{blue}{a} * \textcolor{red}{b}$).

2. On ajoute une parité paire sur chaque ligne : VRC (Vertical Redundancy Check : Contrôle de parité verticale)

3. On ajoute une parité paire sur chaque colonne : LRC (Longitudinal Redundancy Check : Contrôle de parité horizontale)

4. On ajoute une parité paire croisée de la colonne VRC et de la ligne LRC

5. On obtient une matrice de taille ($\textcolor{blue}{a}+1, \textcolor{red}{b}+1$)

![[Pasted image 20241011075855.png]]

##### <mark class="hltr-grey hltr-bold">Exemple</mark>

	On veut transmettre le message : JFAnne

