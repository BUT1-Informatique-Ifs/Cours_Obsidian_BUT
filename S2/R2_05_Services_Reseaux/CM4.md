## <mark class="hltr-green format">Protocole HTTP</mark>
- Protocole utilisé par les navigateurs web pour consulter les site internet
- Détermine comment la page est transmise du serveur au client
- Hypertexte : désigne le fait de mettre en lien des fichiers. Les sites internet contiennent en effet des hyperliens renvoyant à d'autres pages web

### <mark class="hltr-pink format">Fonctionnement du HTTP</mark>

- différentes requêtes (GET;POST;...)
- le navigateur traduit l'url en requête HTTP pour requêter le serveur web (et demander la page)

### <mark class="hltr-pink format">Quand utiliser HTTP</mark>

- API REST
- Serveur web
- WebDAV
- Communication de machine à machine
- Lecteurs de médias
- Accès à une BDD (CRUD=>Create;Read;Update;Delete)

### <mark class="hltr-pink format">HTTP-Pipelining</mark>
- permet au client d'envoyer la requête suivante avant d'avoir reçu la réponse de la première requête

### <mark class="hltr-pink format">Keepalive</mark>
- le client peut maintenir une connexion au-delà d'une requête (connexion persistante) en envoyant un keepalive dans l'entête de sa requête

### <mark class="hltr-pink format">Personnaliser une page d'erreur 404</mark>

- Dans le fichier .htaccess

### <mark class="hltr-pink format">Les codes de statut HTTP</mark>

- 1xx : le serveur indique au client que la requête est en cours
- 2xx : codes de succès
- 3xx : codes de redirection
- 4xx : erreurs du client
- 5xx : erreurs du serveur