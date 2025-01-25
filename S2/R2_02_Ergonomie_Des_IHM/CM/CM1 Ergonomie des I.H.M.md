# <mark class="hltr-purple hltr-bold">Ergonomie du logiciel interactif</mark>
	etymologie :
		ergon : le travail
		nomos : la loi

*Une interface utilisateur, c'est comme une blague.*
*Si vous devez l'expliquer, c'est qu'elle n'est pas si bonne*

## <mark class="hltr-green hltr-bold">Définition de l'association internationale d'ergonomie</mark>

L'ergonomie (ou l'étude des facteurs humains) est la discipline scientifique qui vise la compréhension fondamentale des interactions entre les êtres humains et les autres composantes d'un système, et la mise en oeuvre dans la conception de théories, de principes, de méthodes et de données pertinentes afin d'améliorer le bien-être des hommes et l'efficacité globale des systèmes.

## <mark class="hltr-green hltr-bold">Les concepts</mark>

- Outil classique : prolongement des organes moteurs (bras, mains, jambes)
- Logiciel interactif : prolongement du cerveau utilisant des organes moteurs (souris, clavier)

**Il faut connaître l'Homme pour concevoir ergonomiquement.**

# <mark class="hltr-purple hltr-bold">Modèle du processeur humain</mark>

## <mark class="hltr-green hltr-bold">Sous système</mark>

3 sous-systèmes :
- sensoriel
- moteur
- cognitif

Chaque sous-système comprend :
- un processeur (cycle d'horloge)
- une mémoire (capacité, type d'info retenue, temps de dégradation de l'info)

![[schema_memoire_travail_ihm.png]]

### <mark class="hltr-pink hltr-bold">Mémoire sensorielle</mark>
- stocke les stimuli sans les interpréter
- conserve l'info pendant 0.3 à 3 secondes
- cycle de base de 100ms
	- 1/10eme de seconde pour représenter un stimuli
- persistance
	- 200ms pour le système visuel
	- 1500ms pour le système auditif

### <mark class="hltr-pink hltr-bold">Mémoire à court terme</mark>

- stocke sous forme de motifs regroupés
	- taille
	- couleur ou hauteur
	- localisation
- mémorise de 5 à 9 items
- oublie après 10 à 15 secondes
- recherche séquentielle et exhaustive

### <mark class="hltr-pink hltr-bold">Mémoire à long terme</mark>

- capacité potentiellement infinie
- stockage sous forme de réseau
- accès par association
- recherche échoue si :
	- aucune association trouvée
	- plusieurs mnèmes trouvés qui interfèrent
- l'info ne disparaît pas, elle est inaccessible

### <mark class="hltr-pink hltr-bold">Système moteur</mark>

- cycle de base de 70ms
- mouvement fait de micromouvements
- durée de placement de la main
	- augmente avec l'augmentation de la distance
	- augmente avec la diminution de la taille

## <mark class="hltr-green hltr-bold">Conséquences du modèle du processeur humain</mark>

- Rendre visible à l'écran ce qui est utile et rien que ce qui est utile 
- Eviter la mémorisation entre écrans successifs
	- en limitant les enchaînements d'écrans
	- en rappelant le cheminement à l'utilisareur
	- en permettant le retour en arrière dans l'écran précédent
- Limiter les choix dans les menus (à 7 plus ou moins 2 items ou à 7 plus ou moins 2 groupes de maximul 7 plus ou moins 2 items)
---
- Utiliser
	- les formats,
	- la couleur,
	- les emplacements
	pour faciliter l'établissement de liens entre les éléments affichés
- Produire des retours d'information immédiats et évidents 
- Trouver un bon compromis entre la taille d'un élément affiché et la vitesse de sélection

# <mark class="hltr-purple hltr-bold">Modalités de dialogue</mark>

## <mark class="hltr-green hltr-bold">Entre humains</mark>
- Langage parlé
- Langage écrit
- Dessin
- Gestes ou actions

## <mark class="hltr-green hltr-bold">Humain-machine</mark>
- Langage naturel ou langage de commandes
- Dessin
- Manipulation directe (mime de l'activité)
- Touches de fonction
- Menus
- Formulaires

### <mark class="hltr-pink hltr-bold">Langage de commandes</mark>
#### <mark class="hltr-blue hltr-bold">Commande</mark>
- terme désignant l'action ou l'opération
- options éventuelles
- arguments éventuels
#### <mark class="hltr-blue hltr-bold">Défauts</mark>
- Difficultés de mémorisation
- Risque d'erreur lexicales et syntaxiques
#### <mark class="hltr-blue hltr-bold">Avantages</mark>
- Flexibles et évolutifs

### <mark class="hltr-pink hltr-bold">Menus</mark>
#### <mark class="hltr-blue hltr-bold">Ensembles d'options</mark>
- visibles ou estompées
- regroupées ou hiérarchisées

#### <mark class="hltr-blue hltr-bold">Défauts</mark>
- Difficultés d'exploration
#### <mark class="hltr-blue hltr-bold">Avantages</mark>
- Apprentissage et mémorisation limités
- Guidage important

### <mark class="hltr-pink hltr-bold">Touches de fonction</mark>
Touches dédiées du clavier

#### <mark class="hltr-blue hltr-bold">Défauts</mark>
- Plusieurs fonctions pour une seule touche
- Risque d'erreur de frappe
#### <mark class="hltr-blue hltr-bold">Avantages</mark>
- Toujours visible
- Immédiatement disponibles
- Pas d'erreur lexicale

### <mark class="hltr-pink hltr-bold">Icônes</mark>
#### <mark class="hltr-blue hltr-bold">Pictogrammes au schématisme épuré</mark>
- Peuvent représenter
	- éléments de l'environnement
	- fonctionnalités
	- aide à la reconnaissance

#### <mark class="hltr-blue hltr-bold">Avantages</mark>
- Espace réduit
- Vitesse de perception

### <mark class="hltr-pink hltr-bold">Manipulation directe</mark>
- Représentations graphiques manipulables
	- Désignation
	- Glisser-Déposer
- Application dans le domaine graphique
- Application limitée dans l'édition de texte
- Autre domaine : recours à des métaphores

### <mark class="hltr-pink hltr-bold">Hypermédia</mark>
- Ensemble organisé d'unités d'information
- Consultable de façon non linéaire
- Navigation via les liens
	- Bouton de commande
	- Mot ou texte déclencheur
- Dans les applications de gestion
	- Navigation entre entités (CIF et autres associations)