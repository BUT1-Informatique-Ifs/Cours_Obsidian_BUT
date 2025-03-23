# <mark class="hltr-purple format">CM8 Réseaux</mark>

## <mark class="hltr-green format">Suite Modèle OSI</mark>

### <mark class="hltr-pink format">En tête Ethernet</mark>

- Adresse MAC destinataire ( qui envoie la trame )
- Adresse MAC source ( qui reçoit la trame )
- Type d'ethernet (type de protocole)
### <mark class="hltr-pink format">Dialogue entre deux machines</mark>

| @MAC A | @ MAC B | protocole sup | XXXXX | Bonjour |

### <mark class="hltr-pink format">Pourquoi une adresse alors que l'on a déjà l'adresse MAC ?</mark>

- Il faut pouvoir différencier les adresses de couche 2 et de couche 3 car elles n'ont pas les mêmes rôles.
- L'adresse MAC en couche 2 permet d'identifier une machine sur le même réseau.

### <mark class="hltr-pink format">Couche transport</mark>
Le but :
- découper des données de taille variable en paquets de taille fixe
- identifier les programmes destinataire/émetteur de la donnée
### <mark class="hltr-pink format">La segmentation des données</mark>
- C'est le protocole TCP/UDP qui s'occupe de gérer les trames de données reçues
### <mark class="hltr-pink format">L'identification des processus émetteur/récepteur</mark>
- On utilise en plus des adresses IP, les ports logiciels. 
### <mark class="hltr-pink format">Différents ports</mark>
#### <mark class="hltr-blue format">Ports dédiés</mark>
- 0 à 1023 : Ce sont des ports réservés à des fonctions précises (SSH, FTP, SMTP, ...)

#### <mark class="hltr-blue format">Ports réservés</mark>
- 1024 à 49151 : Ports réservés à des applications propriétaires

#### <mark class="hltr-blue format">Ports dynamiques</mark>
- 49152 à 65535 : Ports libres, non réservés, utilisables à la demande

### <mark class="hltr-pink format">Les pare-feu</mark>
- permettent d'interdire la communication sur certains ports et de filtrer les segments/datagrammes selon le numéro de port.
- permet donc d'éviter la réception ou l'envoi de segments/datagrammes dangereux/non souhaités.

### <mark class="hltr-pink format">Le protocole UDP</mark>
- gère les ports logiciels mais ne vérifie pas que la donnée est bien arrivée, et ne remet pas les datagrammes dans leur ordre d'envoi. Il est très adapté dans les situations où l'on se moque que les données arrivent dans l'ordre et où les pertes de données sont acceptables.

- contient plusieurs infos :
	- le port source (16 bits)
	- le port destinataire (16 bits)
	- la longueur (16 bits)
	- la somme de contrôle (16 bits)

### <mark class="hltr-pink format">Le protocole TCP</mark>

- En plus des fonctionnalités du UDP, il gère des connexions, les accusés de réception et la détection des pertes de données et gère l'ordre de réception
- Il remet les segments dans l'ordre pour reconstituer la donnée transmise.


### <mark class="hltr-pink format">Connexion TCP</mark>
- C'est un protocole en mode connecté : tout transfert de donnée doit être précédé d'une négociation entre l'émetteur et le récepteur, appelé connexion.
### <mark class="hltr-pink format">La couche session</mark>
- Permet d'établir des sessions entre les utilisateurs de machines différentes : elles stockent les tokens de synchronisation dans le cas où une session crash.
## <mark class="hltr-green format">Modèle TCP/IP</mark>

### <mark class="hltr-pink format">Différentes couches</mark>
- application
- transport
- internet
- network access