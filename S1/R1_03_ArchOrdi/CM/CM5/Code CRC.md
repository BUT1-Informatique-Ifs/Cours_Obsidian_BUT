# <mark class="hltr-blue hltr-bold">Code CRC (Cyclic Redundancy Check)</mark>

## <mark class="hltr-purple hltr-bold">Définitions</mark>

	Code de redondance cyclique

	Fait partie des codes polynomiaux (utilisent donc l'arithmétique des
	polynômes)

### <mark class="hltr-green hltr-bold">Représentation</mark>

	On utilise la représentation polynomiale d'un nombre binaire :

Soit un mot binaire (groupe de bits) ($b_{n-1} \; b_{n-2} \; ... \; b_{1} \; b_{0}$) de longueur $\textcolor{red}n$. On représente ce nombre par un polynôme $P(X)$ de variable $X$ et de degré $(\textcolor{red}{n}-1)$ dont les coefficients binaires sont :
	$P(X)=b_{0}+b_{1}X +b_{2}X^2 \; ... \; b_{n-1}X^{n-1}$

##### <mark class="hltr-grey hltr-bold">Exemple avec</mark> $10111_{2}$

=> $1*X^4+0*X^3+1*X^2+1*X^1+1*X^0$

#### <mark class="hltr-pink hltr-bold">Les polynômes normalisés</mark>

	Pour avoir une bonne capacité de détection, des codes ont été 
	étudiés et normalisés :

- CRC-8 : $G(X) = X^8+X^2+X+1$
- CRC-10 : $G(X) = X^{10}+X^9+X^5+X^4+X+1$
- CRC-12 : $G(X) = X^{12}+X^{11}+X^3+X^2+X+1$
- CRC-16 : $G(X) = X^{16}+X^{15}+X^2+X^2+1$
- CRC-CCITT : $G(X) = X^{16}+X^{12}+X^5+1$
- CRC-32 : $G(X) = X^{32}+X^{26}+X^{23}+X^{22}+X^{16}+X^{}+1$
ERREUR CRC-32

## <mark class="hltr-purple hltr-bold">Polynômes nécessaires</mark>

	Pour faire le calcul du code CRC, on a besoin de plusieurs polynômes

1. $M(X)$ : le polynôme du message binaire de $\textcolor{red}m$ bits à transmettre (degré $\textcolor{red}{m}-1$)
2. $M'(X)$ : le polynôme du message binaire de $\textcolor{red}m$ bits reçus (degré $\textcolor{red}{m}-1$)
3. $G(X)$ : le polynôme générateur de $\textcolor{blue}g$ bits (degré $\textcolor{blue}{g} - 1$)
4. $R(X)$ : le polynôme de contrôle de $\textcolor{magenta}r$ bits (degré $\textcolor{magenta}{r}>=\textcolor{blue}{g}$ )
5. $T(X)$ : le polynôme du message binaire transmis avec le CRC (degré $\textcolor{red}{m} + \textcolor{blue}g-1$)
6. $T'(X)$ : le polynôme du message binaire reçu avec le CRC (degré $\textcolor{red}{m}+\textcolor{blue}{g}-1$)

## <mark class="hltr-purple hltr-bold">Méthode de calcul</mark>

1. On choisit le polynôme générateur $G(X)$ car c'est lui qui définit les caractéristiques du code
2. En fin de message de $M(X)$ (le polynôme du message binaire à transmettre), on ajoute $\textcolor{blue}{g}-1$ zéros. On obtient
	- $M(X)*2^{\textcolor{blue}{(g}-1)}$  ($*2$ car on travaille en base 2, donc on va décaler de $\textcolor{blue}{g}-1$ les bits pour avoir $\textcolor{blue}{g}-1$ zéros )
3. On effectue la division euclidienne (OUEX) de $M(X)*2^{\textcolor{blue}{(g}-1)}/G(X)$
4. On obtient $Q(X)$ le quotient et $R(X)$ le reste (c'est le polynôme de contrôle)
5. <mark class="hltr-red hltr-bold">VOIR AVEC PROF</mark>
6. On obtient $T(X)$, le polynôme du message binaire transmis avec le CRC
7. A la réception, on reçoit $T'(X)$ (qui est identique à $T(X)$ s'il n'y a pas eu d'erreurs de transmission)
8. Pour vérifier le message, on fait la division euclidienne de $T'(X) / G(X)$
9. On obtient $Q'(X)$ le quotient et $R'(X)$ le reste
10. Selon $R'(X)$ :
	- Si $R'(X) = 0$, le message reçu est identique à celui qui a été transmis
	- Si $R'(X) \neq 0$, le message contient une ou plusieurs erreurs, il faut donc demander la ré-émission du message
11. Pour obtenir $M'(X)$, on enlève $\textcolor{blue}{g}-1$ bits à droite de $T'(X)$

## <mark class="hltr-purple hltr-bold">Émission du message</mark>

	Pour émettre le message, on utilise donc l'équation :

- $M(X)*2^{\textcolor{blue}{(g}-1)} / G(X) = Q(X)$ avec un reste égal à $R(X)$
	<mark class="hltr-red hltr-bold">Le LSB</mark> de $\textcolor{red}{R(X)}$ <mark class="hltr-red hltr-bold">doit toujours valoir 1 !</mark>

##### <mark class="hltr-grey hltr-bold">Exemple</mark>

	On veut envoyer 101101 en base 2

