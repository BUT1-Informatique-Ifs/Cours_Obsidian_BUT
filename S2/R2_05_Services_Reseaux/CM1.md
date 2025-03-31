## <mark class="hltr-green format">Transmission : ETTD et ETCD</mark>

- Une transmission de données met en oeuvre des calculateurs d'extrémité et des éléments d'adaptation du signal

ETTD :  Equipement Terminal de Traitement de Données => contrôle les communications
ETCD : de Circuit de Données => réalise l'adaptation du signal entre l'ETTD et le support de transmission

### <mark class="hltr-pink format">Organisation des échanges</mark>

Plusieurs caractéristiques :
- sens de transmission : unidirectionnelle (Simplex), à l'alternat (Half Duplex) ou bidirectionnelle (Full Duplex)
- le nombre de bits transmis en même temps : transmission parallèle ou transmission en série
- le type de synchronisation des horloges : synchrone ou asynchrone
- le mode de transmission électrique : asymétrique ou symétrique

### <mark class="hltr-pink format">Modulation d'un Signal</mark>

- La modulation peut être définie comme le processus par lequel le signal est transformé de sa forme originale en une forme adaptée au canal de transmission, par exemple en faisant varier les paramètres d'amplitude et d'argument (phase/freq) d'une onde sinusoïdale appelée.

### <mark class="hltr-pink format">Deux modes d'adaptation du signal</mark>

- La transmission en large bande translate le spectre du signal à émettre dans une bande de freq mieux admise par le système.

- La transmission en bande de base consiste à modifier légèrement (on dit transcoder) le signal émis par l'ETTD.
### <mark class="hltr-pink format">Différents types de modulations analogiques</mark>
- Modulation en Amplitude
- Modulation en Fréquence
- Modulation en Phase

Les différentes techniques de modulation peuvent être combinées.


### <mark class="hltr-pink format">Jonction ETTD/ETCD</mark>

- Définit un ensemble de règles (protocole) destinées à assurer la connectivité et le dialogue entre ETTD et ETCD, la synchronisation.

### <mark class="hltr-pink format">Deux techniques de multiplexage</mark>
- spatial et temporel

## <mark class="hltr-green format">Configuration Réseau</mark>

Quand on se connecte à une machine à un réseau en TCP/IP, la machine doit disposer :
- d'une adresse IP unique dans son réseau et appartenant au même réseau logique que toutes les autres machines du réseau en question
- un masque de sous-réseau, le même pour tous les hôtes du réseau
- l'adresse de la passerelle qui permet de sortir du réseau et d'accéder à internet
- une adresse de DNS, pour pouvoir résoudre les noms des hôtes, surtout si son réseau est connecté à internet