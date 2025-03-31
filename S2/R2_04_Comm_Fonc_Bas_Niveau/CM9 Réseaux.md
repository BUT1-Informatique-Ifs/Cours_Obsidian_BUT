## <mark class="hltr-green format">Suite modèle TCP/IP</mark>

### <mark class="hltr-pink format">La couche Internet</mark>

- possède une implémentation officielle : le protocole IP


### <mark class="hltr-pink format">La couche Transport</mark>

- permettre à des entités paires de soutenir une conversation
	- a 2 implémentations :
		- protocole TCP
		- protocole UDP


### <mark class="hltr-pink format">Protocole TCP</mark>
- protocole fiable, orienté connexion qui permet l'acheminement sans erreur de paquets entre machine. Plus lent car connecté à internet mais plus fiable

### <mark class="hltr-pink format">Protocole UDP</mark>
- protocole plus simple que TCP, non fiable et sans connexion. Le protocole UDP n'a pas besoin de la conservation de l'ordre de remise des paquets. A utiliser par exemple pour la transmission vocale (conversation) car très rapide. A utiliser aussi si transfert proche (machine proche par exemple).


## <mark class="hltr-green format">Dialogue entre 2 machines</mark>
- Les adresses MAC source et destination sont modifiées à chaque passage par un routeur.