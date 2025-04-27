## <mark class="hltr-green format">IPV6</mark>

- 128 bits
- 2^128  adresses possibles
- Permet plusieurs interfaces par hôte
- Plusieurs adresses par interface
- Différents types d'adresses :
	- Unicast
	- Multicast
	- Anycast
- Des adresses par fournisseur d'accès
- Une partie de l'IPV6 peut être l'adresse MAC (en générant l'IP avec l'adresse MAC)


### <mark class="hltr-pink format">Décomposition d'une IPV6</mark>

- Une partie Réseau
- Une partie Hôte
- 64 premiers bits pour la partie réseau
- 64 derniers bits pour la machine hôte

### <mark class="hltr-pink format">Conversion IPv6 en IPv4</mark>

80 bits | 16 bits (FFFF) | 32 bits (adresse IPv4) => Devient une IPv4 mappée

### <mark class="hltr-pink format">Unique Local Address (ULA) : Adresse IPv6 unicast</mark>

- Uniquement utilisées pour les communications locales (IP privée en IPv4)
- 64 bits sont réservés pour l'adresse de l'hôte (on utilise l'adresse MAC pour remplir ce champ et on rajoute ff:fe pour avoir les 64 bits)

### <mark class="hltr-pink format">Adresse de l'interface ID : adresse MAC</mark>
- numéro unique au monde qui est attribué à toute interface réseau
- constituée de 48 bits ou de 64 bits
#### <mark class="hltr-blue format">Composition</mark>

 - 1 bit I/G : indique si l'adresse est individuelle
	 - 0 : (pour une machine unique/unicast)
	 - 1 : pour un groupe (multicast/broadcast)
- 1 bit U/L : indique si l'adresse est
	- 0 : universelle
	- 1 : adresse administrée localement
- 22 bits réservés
	- tous les bits sont à 0 pour une adresse locale
	- sinon, ils contiennent l'adresse du constructeur
- 24 bits (40 bits) : adresse unique (pour différencier les différentes cartes réseaux d'un même constructeur)
### <mark class="hltr-pink format">Conversion de l'interface ID en adresse IPv6</mark>

- On inverse le bit "u" des 64 bits
### <mark class="hltr-pink format">Adresse IPv6 unicast : Link-Local (ULL)</mark>
- Non routable, appartiennent que au réseau dans lequel on est
- Désignent une et une seule machine
- Comportent une partie réseau "préfixe" et une partie hôte "suffixe"
- La partie préfixe est codée sur 64 bits : les 48 bits publics et les 16 bits de site définissant le sous réseau
- La partie suffixe est aussi codée sur 64 bits à partir de l'adresse MAC

### <mark class="hltr-pink format">Adresse IPv6 multicast</mark>
- spécifie un groupe d'interfaces appartenant à un groupe de diffusion
- peut être permanente (T=0) ou temporaire (T=1).
- Les 3 premiers bits sont nuls (réservés)

### <mark class="hltr-pink format">Adresse IPv6 anycast</mark>
- c'est une adresse multicast mais le paquet émis ne sera remis qu'à un seul membre du groupe, même si plusieurs interfaces ont répondu au message de sollicitation des voisins d'ICMPv6.

### <mark class="hltr-pink format">Adresse IPv6 Globales unicast</mark>

- Les adresses qui commencent par 2001 sont déléguées aux FAI
- Les préfixes fournis aux FAI ont un préfixe d'une longueur de 32
- Tout client peut obtenir de son FAI un préfixe d'une longueur de 48

## <mark class="hltr-green format">Protocole SMTP</mark>

### <mark class="hltr-pink format">Ce que c'est</mark>

- protocole de communication utilisé pour les transferts d'emails sur un réseau
- de type client/serveur
- les échanges se font sur un serveur de messagerie via des ports (un port pour le serveur) et le protocole SMTP écoute, par défaut le port 25 avec pour objectif de router les messages

### <mark class="hltr-pink format">Fonctionnement</mark>
- port serveur : 25
- port client : 587
- ne permet pas d'identifier l'expéditeur des mails et ne permet pas de lutter contre le spam

### <mark class="hltr-pink format">Les agents de transferts (MTA)</mark>

- ce sont les programmes qui permettent le transfert des courriers entre les serveurs.
- les mails peuvent être relayé entre plusieurs MTA
- il est possible de connaître tous les MTA par lesquels le mail est passé en affichant la source du message

## <mark class="hltr-green format">Protocole POP3</mark>

- Protocole standaard qui permet la récupération des mails sur un serveur distant
- Avantage : permettre la consultation de sa messagerie en mode "hors connexion", sans avoir besoin d'une connexion internet permanente.
- Inconvénient : pas adapté aux supports mobiles et que les msg nne sont pas synchro en permanence avec le serv
- permet aux utilisateurs de pouvoir consulter les mails sans qu'on soit connectés.
- Ce protocole permet d'identifier l'expéditeur.
- Problème : les mdps ne sont pas cryptés