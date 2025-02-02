# <mark class="hltr-purple hltr-bold">Bibliothèques statiques et dynamiques</mark>
- fichiers .h

## <mark class="hltr-green hltr-bold">Statique (.a)</mark>
Lors de la compilation :
- on inclut le code binaire des modules objets (.o) de la lib dans l'exécutable
- l'exécution peut se faire sans avoir la lib sur la machine
- l'espace disque utilisé par l'exécutable sera plus important

## <mark class="hltr-green hltr-bold">Dynamique/Partagée (.so)</mark>
- chargée une seule fois et toute entière
- gain de place en mémoire car exécutable moins gros
- nécessite la présence de cette lib sur la machine

=> gcc utilise par défaut les bibliothèques dynamiques
- pour compiler en statique, on utilise `-static`
- -ldd permet de connaître les dépendances dynamiques de l'exécutable

- .so.nb1.nb2

Si nb1 change, c'est une mise à jour majeure
Si nb2 change, c'est une mise à jour mineure
# <mark class="hltr-purple hltr-bold">Les variables et les adresses mémoires</mark>

## <mark class="hltr-green hltr-bold">Les pointeurs</mark>
- c'est un objet (Lvalue) dont la valeur est égale à l'adresse mémoire d'un autre objet.
- `%p` permet d'afficher une adresse mémoire
- si on ajoute un entier à une adresse mémoire (le pointeur), on se déplace dans la mémoire
- pointeur++ (incrémente pas de 1 mais de la taille de l'objet en mémoire)