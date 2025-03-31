## <mark class="hltr-green format">Le DHCP</mark>
	Dynamic Host Configuration
	Protocol

- Service TCP/IP qu'on installe en général sur une machine serveur mais aussi parfois sur un routeur
- Permet d'automatiser la configuration réseau des équipements d'une infrastructure
- But : évite aux admins de configurer manuellement tous les postes de travail un par un
- C'est une attribution dynamique d'adresse IP

### <mark class="hltr-pink format">Avantages</mark>

- Attribution dynamique d'adresse IP
- Gestion de l'adressage IP de l'environnement est automatisée et centralisée
- Si l'adresse de l'adresse du serveur DNS change, il faudra juste déclarer la nouvelle IP au service DHCP
- Diminution du risque de conflit d'adresses IP dans l'infrastructure car pas d'intervention humaine

### <mark class="hltr-pink format">Le service DHCP</mark>

- Lorsque le client démarre, il n'a aucune connaissance du réseau
- Il envoie donc une trame DHCP DISCOVER pour trouver le serveur DHCP (il envoie en broadcast).
- Le serveur DHCP qui a reçu la trame va répondre par un DHCP OFFER (avec la proposition du bail, adresse mac du client et l'adresse ip du serveur).
- Le client répond par un DHCP REQUEST à tous les serveurs (en broadcast pour indiquer quelle offre il accepte)
- Le serveur DHCP choisi répond par DHCP ACK pour confirmer le bail.

## <mark class="hltr-green format">DNS</mark>
	Adresse IP en nom
- C'est une base de données distribuée qui fait correspondre le nom à une adresse IP (et d'autres infos)
	- administration partagée
	- charge partagée
	- robustesse avec la réplication
	- système de cache
	- faille critique possible de l'infrastructure internet