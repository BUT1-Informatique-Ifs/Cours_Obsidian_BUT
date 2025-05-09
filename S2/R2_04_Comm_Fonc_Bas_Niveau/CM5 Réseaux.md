## <mark class="hltr-green format">Réseaux de Données</mark>
- Réseau : ensemble d'équipements permettant à des individus/groupes de partager des info et des services d'un point à un autre

- équipements terminaux : appareils qui consomment et émettent des données
- équipements d'interconnexion : appareils entre l'émetteur et le récepteur

- nécessitent des supports de transmissions
- des protocoles de communications

### <mark class="hltr-pink format">L'objectif des réseaux de données</mark>

- transmission et consultation des données
- le partage de ressources physiques
- la sécurité des informations

### <mark class="hltr-pink format">Principales applications</mark>

- consultation de pages web
- multimédia
- transfert de fichiers
- ...

### <mark class="hltr-pink format">Classification des réseaux de données</mark>

- par le type de commutations
- type de transmission
- type de connexion
- leur débit
- par la qualité de service (fiabilité, délais, ..)
- par leur architecture interne
- ...

#### <mark class="hltr-blue format">Par le type de commutations</mark>

- Commutation de circuits : technique qui permet l'allocation de voies de transmission pendant toute la durée d'une communication.

- Commutation de messagers : ici, pas de réservation de ressources. Les messages sont traités selon l'ordre d'arrivée. C'est une file (First In First Out)

- Commutation par paquets : Technique permettant des communications où les ressources sont affectées en fonction des besoins. L'information est structurée en paquet de taille fixe pour rester en mémoires dans les commutateurs. Ce mode de transfert est celui utilisé sur internet.


#### <mark class="hltr-blue format">Par le type de transmission</mark>

- Réseaux à diffusion : possède qu'un seul canal de communication (réseaux de petites tailles)
- Point à Point : le message doit transiter par plusieurs stations intermédiaire (réseaux de grandes tailles)
- Inter-circuit : Bus : réseau de faible étendue (environ 10cm) => permet de faire transiter des données d'un circuit électronique vers un autre circuit (CAN BUS => échange de données sur une voiture)
- personnel : PAN : interconnexion d'équipements informatique dans un espace d'une dizaine de mètres. C'est le WIFI ou le Bluetooth
- locaux : LAN : dizaines/centaines de mètres. connexion entre plusieurs ordi souvent en ethernet.
- réseaux métropolitains : MAN : réseau LAN avec possibilité de connexion à des distances plus grandes (connecter Campus 1 et 3) (plusieurs LAN regroupés)
- étendus : WAN : constitué de LAN voire de MAN. étendu à des milliers de km (Internet est le plus grand WAN)

## <mark class="hltr-green format">Adressage IPV4</mark>

- Protocole : TCP/IP => système particulier d'adressage

- 3 types de trafic :
	- Unicast : communication entre un hôte source unique et un hôte destination unique
	- Multicast : communication entre un hôte source unique et un groupe d'hôtes
	- Broadcast : désigne un flux par un hôte à destination de tous les autres hôtes appartenant au même domaine de diffusion. Ce trafic ne peut exister que sur les réseaux dits de diffusion comme Ethernet. Exemple de protocole : ARP

- Distribuées par IANAN
- Codé sur 32 bits
- de 0 à 255
- privé ou publique
- aucune adresse publique dispo depuis février 2011

### <mark class="hltr-pink format">Classes d'adresse IP</mark>

- Les adresses IP sont réparties en différentes classes
- 2 premiers octets pour réseau, les autres pour l'hôte
- Le masque réseau sert à départager la partie réseau et la partie hôte.
- Notation CIDR : consiste à faire suivre l'adresse de /X, avec X = le nombre de bits à 1 du masque de sous-réseau (entre 0 et 32)
- Classes couramment utilisé : de A à C

#### <mark class="hltr-blue format">Classe A</mark>

- premier bit à 0
- masque réseau vaut : 255.0.0.0
- permettent donc de créer des réseaux (127) avec bcp de machines. On les retrouve sur des backbones

#### <mark class="hltr-blue format">Classe B</mark>

- les deux premiers bits sont à 10
- le masque réseau vaut : 255.255.0.0
#### <mark class="hltr-blue format">Classe C</mark>

- trois premiers bits sont à 110
- masque : 255.255.255.0

#### <mark class="hltr-blue format">Classe D</mark>
- quatre premiers bit sont à 1110
- classe d'adresse multidiffusion
#### <mark class="hltr-blue format">Classe E</mark>
- cinq premiers bits à 11110
- classe d'adresse réservée


### <mark class="hltr-pink format">Les adresses </mark>
- 0.0.0.0 est utilisé par les hôtes au démarrage
- les adresses IP finissant par 0 sont rattachés au réseau en cours
- pour envoyer un message à tous les hôtes, c'est 255.255.255.255

#### <mark class="hltr-blue format">Adresses privées</mark>

- plusieurs adresses sont réservées et privées
- sont utilisables en interne et ne sont pas routables
- sont prévues pour être utilisé avec un NAT (Network Address Translation) ou avec un DHCP

## <mark class="hltr-green format">Les sous réseaux (Subnetting)</mark>
- une adresse ip possède une partie réseau sur 8, 16 ou 24 bits et une partie hôte.
Un masque de sous-réseau est un nombre de la même taille que l'adresse. 


## <mark class="hltr-green format">Le routage</mark>

- La communication en IP se fait par un acheminement de paquets d'une machine source vers une machine destination B

Problème : Comment atteindre la machine B en ne connaissant que son adresse IP ?
- On va utiliser des routeurs pour faire la connexion entre des réseaux
- Routeur : c'est un dispositif réseau qui relie au moins 2 réseaux

L'IP de destination appartient elle au même réseau que l'IP de l'émetteur ?
- Oui : la remise est direct
- Non : la remise est indirect
	- on utilise l'adresse de la passerelle (Gateway) pour sortir du réseau

### <mark class="hltr-pink format">La table de routage</mark>
Elle contient : 
- les réseaux à joindre
- les interfaces de l'hôte considéré
- les masques correspondants
- les passerelles à contacter pour les joindre
- la métrique : le coût de la route
- les adresses des sous-réseaux auxquels le routeur est directement connecté
- les routes statiques (configurées par l'admin)
- les routes dynamiques (apprises dynamiquement)
- une route par défaut (0.0.0.0) pour sortir du réseau si l'adresse n'a pas été trouvée dans la table