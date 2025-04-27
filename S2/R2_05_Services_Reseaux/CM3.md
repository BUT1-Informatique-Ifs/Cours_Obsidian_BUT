## <mark class="hltr-green format">Suite DNS</mark>

### <mark class="hltr-pink format">Fonctionnement côté client</mark>
- Le client doit trouver son adresse IP à partir de son hôte
- Le client vérifie si une adresse IP correspondant au nom d'hôte est présente dans le cache de noms DNS.
	- Le cache de noms DNS contient tous les nom d'hôte / adresse IP qui ont été précédemment résolus.
	- Il est stocké en mémoire vive

### <mark class="hltr-pink format">Différents types de requêtes sur un serveur DNS</mark>

- Requête récursive : le serveur doit donner la réponse la plus complète possible. Le serveur DNS doit donc souvent joindre d'autres serveurs de noms dans le but de trouver la réponse exacte
- Requête itérative : le serveur renvoie la meilleure réponse qu'il peut donner sans contacter d'autres serveurs DNS

Lorsqu'une machine cliente envoie une requête à un serveur DNS, elle est par défaut de type récursive.

### <mark class="hltr-pink format">La requête vers les redirecteurs</mark>

- Lorsque le serveur DNS ne peut pas répondre à la requête récursive d'un client, ce dernier va d'abord contacter ses redirecteurs. Si le serveur est paramétré pour utiliser des redirecteurs, alors il envoie une requête récursive au premier serveur DNS configuré dans la liste. Mais s'il n'a pas de redirecteurs, il va envoyer une requête itérative au premier serveur DNS situé dans la liste de serveur DNS racine.


### <mark class="hltr-pink format">Détails du protocole</mark>

- DNS utilise en général le protocole UDP avec le port 53.
- La taille maximale des paquets est de 512 octets.
	- Si la taille du paquet est supérieure, le protocole prévoit de rediriger ce paquet sur le port TCP 53
	- Note : Les firewalls bloquent souvent le port TCP 53

### <mark class="hltr-pink format">Les commandes</mark>

nslookup : renvoie l'adresse IP correspondante et indique si la réponse fait ou non autorité sur le domaine

## <mark class="hltr-green format">Service NAT</mark>
	Network Address Translation

- Mécanisme de translation d'adresses qui a été mis au point afin de répondre à la pénurie d'adresses IP avec le protocole IPv4.
- Principe : consiste à utiliser une passerelle de connexion à internet possédant au moins une interface réseau connectée sur le réseau interne et au moins une interface réseau connectée à internet (possédant une adresse IP routable) pour connecter toutes les machines du réseau
- En bref : on traduit une adresse IP vers une autre. Permet de gagner en sécurité.

### <mark class="hltr-pink format">Translation d'adresses</mark>

- Chaque machine du réseau nécessitant d'accéder à internet est configurée pour utiliser la passerelle NAT.
- Lorsqu'une machine du réseau effectue une requête vers Internet, la passerelle effectue la requête à sa place, reçoit la réponse, puis la transmet à la machine ayant fait la demande.

Plages disponibles :
- Classe A : de 10.0.0.0 à 10.255.255.255
- Classe B : de 172.16.0.0 à 172.31.255.255
- Classe C : de 192.168.0.0 à 192.168.255.255

### <mark class="hltr-pink format">Translation statique</mark>
	Consiste à associer une adresse IP publique à une adresse privée interne au réseau.

- Permet ainsi de connecter des machines du réseau interne à internet de manière transparente mais ne résout pas le problème de la pénurie d'adresse dans la mesure où n adresses IP routables sont nécessaires pour connecter n machines du réseau interne

### <mark class="hltr-pink format">Service NAT dynamique</mark>

- Va lier une/des adresses IP à d'autres adresses IP externes de façon dynamique. La ou les adresses vont utiliser un pool d'adresses IP défini.
- Permet de partager une adresse IP routable entre plusieurs machines en adressage privé. Ainsi, toutes les machines possèdent virtuellement la même adresse IP.
- La différence avec le NAT statique est que le PC ne va pas tjr sortir sur la même adresse IP externe.

### <mark class="hltr-pink format">Définition de PAT</mark>

- pas compris dsl (le CM est pas bien écrit)

### <mark class="hltr-pink format">Port Forwarding</mark>

- Ne permet de relayer que des requêtes provenant du réseau interne vers le réseau externe

### <mark class="hltr-pink format">Port Triggering</mark>

- La plupart des app client-serveur effectuent une requête sur un hôte distant sur un port donné et ouvrent un port en retour pour récup des données
### <mark class="hltr-pink format">Différences clés entre NAT et PAT</mark>

- NAT traduit les adresses locales internes en adresses publiques similaires tandis que le PAT convertit les adresses IP non enregistrées privées en adresses IP publiques enregistrées, mais à la différence de NAT, il utilise également des numéros de port source et plusieurs hôtes peuvent être affectés avec la même adresse IP ayant des numéros de port différents

## <mark class="hltr-green format">Le VPN : Réseau privé</mark>

- Repose sur un protocole appelé "tunneling", un protocole permettant aux données passant d'une extrémité du VPN à l'autre d'être sécurisées par des algo de cryptographie

### <mark class="hltr-pink format">Protocoles de tunnelisation</mark>
	Les principaux protocoles de tunneling sont les
	suivants

- PPTP : protocole de niveau 2
- L2F : protocole de niveau 2 (quasi-obsolète)
- L2TP : protocole qui vise à converger les fonctionnalités de PPTP et L2F. Protocole de niveau 2
- IPSec : protocole de niveau 3, permet de transporter des données chiffrées pour les réseaux IP.

### <mark class="hltr-pink format">PPTP</mark>

- Permet de créer des trames sous le protocole PP et de les encapsuler dans un datagramme IP
- Les données sont encapsulées dans un message PPP, qui est lui-même encapsulé dans un message IP

### <mark class="hltr-pink format">L2TP</mark>

- Encapsule des trames protocole PPP, encapsulant elles-mêmes d'autres protocoles (IP, IPX, NetBIOS, ..)
### <mark class="hltr-pink format">IPSec</mark>

- Défini par l'IETF
- Permet de sécuriser les échanges au niveau de la couche réseau
- Protocole apportant des améliorations au niveau de la sécurité au protocole IP afin de garantir la confidentialité, l'intégrité et l'authentification des échanges

Basé sur 3 modules :
- IP Authentification Header (AH) concernant l'intégrité, l'authentification et la protection contre le rejeu des paquets à encapsuler
- Encapsulating Security Payload (ESP) définissant le chiffrement de paquets. ESP fournit la confidentialité, l'intégrité, l'auth et la protection contre le rejeu.
- Security Association (SA) définissant l'échange des clés et des paramètres de sécurité
## <mark class="hltr-green format">Notions des qualités de services (QoS)</mark>
	Désigne la capacité à fournir un service

- En temps de réponse
- En bande passante
- A garantir un niveau acceptable de perte de données pour un usage donné