# <mark class="hltr-purple format">CM6 Réseaux</mark>

## <mark class="hltr-green format">Construction de la table de routage</mark>
1. Indiquer les réseaux auxquels la machine est connectée
2. Indiquer la route par défaut
3. Indiquer tous les autres réseaux que je ne peux pas joindre avec les 2 étapes précédentes
4. Indiquer l'adresse de la passerelle de mon réseau

### <mark class="hltr-pink format">Synthèse pour la construction de la table de routage</mark>
	Doit contenir plusieurs lignes par défaut
 - premiere ligne : passerelle vers la sortie du réseau ou vers internet
 - deuxième ligne : adresse de boucle local
 - troisième et + : adresse des réseaux connectés
## <mark class="hltr-green format">Protocole ARP</mark>

### <mark class="hltr-pink format">Problème</mark>
- la couche 2 utilise les adresses MAC
- la couche 3 utilise les adresses IP

### <mark class="hltr-pink format">Comment faire pour faire correspondre les adresses MAC et IP ?</mark>
- Le protocole ARP permet d'obtenir une adresse MAC en fonction d'une adresse IP

#### <mark class="hltr-blue format">Procédés</mark>
- On envoie sur le broadcast quel est l'adresse MAC de l'IP X.X.X.X
- Toutes les machines vont recevoir la requête mais seule la machine concerné va répondre
- Pour éviter de surcharger le réseau, on utilise le principe de cache local : on va stocker pendant un certain temps la correspondance entre l'IP et l'adresse MAC d'une machine après une requête ARP (souvent quelques minutes de stockage).
- D'ailleurs, le fonctionnement de l'ARP exige de vérifier dans le cache avant de communiquer sur le broadcast

## <mark class="hltr-green format">L'interconnexion</mark>

- Un réseau local sert à interconnecter les ordinateurs d'une organisation.
- Sur deux réseaux de même type, il suffit de faire passer les trames de l'un sur l'autre.
### <mark class="hltr-pink format">Les équipements d'interconnexion</mark>
- répéteurs : permettent de régénérer un signal
- concentrateurs (hubs) : permettent de connecter entre eux plusieurs hôtes
- ponts (bridges) : permettent de relier des réseaux locaux de même type
- commutateurs (switches) : permettent de relier divers éléments tout en segmentant le réseau
- passerelles (gateways) : permettent de relier des réseaux locaux de types différents
- routeurs : permettent de relier bcp de réseaux locaux pour permettre la circulation de donnée entre ces derniers
- B-routeurs : associe les fonctionnalités d'un routeur et d'un pont
