## <mark class="hltr-green format">Protocole IMAP</mark>

- Protocole de messagerie
- inverse du protocole POP car il a une connexion constante au serveur de messagerie
- Port : 143
- Il conserve les mails même après la déconnexion
- Permet aux utilisateurs de consulter leurs mails à divers endroits et sur des webmails différents
- Limite : la capacité de stockage du serveur
- Trie des mails directement sur le serveur
- Possible de gérer plusieurs boîtes aux lettres
- Désavantage : nécessite une connexion permanente
- Permet une synchronisation entre tous les appareils utilisés (si on met un msg non lu sur le tel, il le sera sur le pc)


## <mark class="hltr-green format">POPs et IMAPs</mark>
- Permet la sécurité car :
	- POP3 over SSL
	- IMAP over SSL

## <mark class="hltr-green format">Différents services d'un serveur de courriel</mark>
	Le serveur de messageroe est divisé en plusieurs services :
- MUA (Mail User Agent) : logiciel qui sert à lire et à envoyer les messages électroniques
- MTA (Mail Transfert Agent) : logiciel pour serveur de transmission. Il envoie les mails entre les serveurs
- MDA (Mail Delivery Agent) : logiciel de distribution du courrier électronique et représente la dernière étape de la chaîne d'envoi d'un mail. 

### <mark class="hltr-pink format">Itinéraire d'un message</mark>

- Jean envoie un message grâce à son MUA. Le message est acheminé au serveur SMTP de son domaine
- Le MTA emc.fr reçoit le msg et constate que le de destinataire n'est pas dans ses destinations. Il cherche grâce à DNS si un MTA existe pour le domaine du destinataire. S'il trouve, il envoie le msg à ce MTA
- Le serveur SMTP du destinataire reçoit le msg. Il dépose le msg avec le MDA