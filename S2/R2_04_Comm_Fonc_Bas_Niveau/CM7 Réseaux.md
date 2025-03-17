# <mark class="hltr-purple format">CM7 Réseaux</mark>

## <mark class="hltr-green format">Différents câbles</mark>

### <mark class="hltr-pink format">Câble droit (straight)</mark>
- Câble UTP/STP

- Si les couleurs sont au même endroit à l'entrée et à la sortie du câble, c'est un câble droit.
### <mark class="hltr-pink format">Câble croisé (cross-over)</mark>
- Si les couleurs ne sont pas les mêmes à l'entrée et à la sortie du câble, c'est un câble croisé.

## <mark class="hltr-green format">Connexion et branchement du routeur</mark>

- Il faut brancher le câble console au routeur

- Pour s'y connecter, on peut utiliser SSH avec PuTTY, le protocole telnet ou encore "serial" pour se connecter au port physique du routeur.

## <mark class="hltr-green format">Le routage</mark>

### <mark class="hltr-pink format">Routage statique</mark>

- On peut ajouter manuellement à un routeur, les routes de notre réseau qui lui manquent avec une commande.


#### <mark class="hltr-blue format">Avantages</mark> 
- Economie de bande passante
- Sécurité
- Connaissance du chemin à l'avance
#### <mark class="hltr-blue format">Inconvénients</mark>
- La configuration du réseau de taille importante peut devenir complexe et longue
- Compliqué à faire évoluer quand le réseau s'agrandit


### <mark class="hltr-pink format">Routage dynamique</mark>
- Permet de mettre à jour de façon automatique le plan du réseau.
- Certains protocoles de routage calculent les routes en fonction :
	- de la vitesse des liens qui les relient (état des liens, ..)
	- du nombre de routeurs (nb de sauts) à passer avant d'atteindre notre destination (distance-vecteur);

#### <mark class="hltr-blue format">Protocoles</mark>
- RIP, IGRP, OSPF, IS-IS
- Ici on s'intéressera à RIP (Routing Information Protocol)
#### <mark class="hltr-blue format">Avantages</mark>
- Maintenance réduite
- Modularité et Flexibilité
- Performance

#### <mark class="hltr-blue format">Inconvénients</mark>
- Plus compliqué à mettre en place lors de son initialisation
- Consomme plus de bande passante
- Problème de sécurité
- Consomme plus de CPU et RAM


## <mark class="hltr-green format">Normalisation : Modèle OSI</mark>

- C'est une norme qui structure la communication entre les différents éléments et protocoles du réseau
- Séparé en différentes couches, chaque couche a un rôle défini
- Les données traversent différentes couches, de l'application jusqu'au média réseau, et à l'arrivée font le chemin en sens inverse
- Chaque couche ne peut communiquer qu'avec une couche adjacente (au dessous ou au dessous)

- Les couches sont séparés en 2 catégories :
	- Les couches hautes
	- Les couches matérielles
- Le nom de l'unité de données change en fonction de la couche