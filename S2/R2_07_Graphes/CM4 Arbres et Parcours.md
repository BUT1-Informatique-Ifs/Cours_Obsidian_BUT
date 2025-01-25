# <mark class="hltr-purple hltr-bold">Arbres et Parcours</mark>

Méthode :
- Si tous les voisins de S (sommet) sont déjà connus, alors on ajoute S à la zone explorée
- sinon cela veut dire qu'il est encore dans la frontière
Comment organiser une frontière : 
Méthode 1 : avec une file (parcours en largeur)
Méthode 2 : avec une pile (parcours en profondeur)

## <mark class="hltr-green hltr-bold">Parcours en largeur</mark>
- FILE
- notion de chemin le plus rapide entre 2 sommets

### <mark class="hltr-pink hltr-bold">Arbres de parcours</mark>

#### <mark class="hltr-blue hltr-bold">Théorème 1 (Distance et Niveau)</mark>
- Le niveau d'un sommet dans l'arbre est égal à la distance entre le sommet et la source
## <mark class="hltr-green hltr-bold">Parcours en profondeur</mark>
- PILE
### <mark class="hltr-pink hltr-bold">Propriétés d'un arbre de parcours</mark>
- Lorsque l'on s'éloigne de la racine, on rajoute une flèche

#### <mark class="hltr-blue hltr-bold">Théorème 2 (absence d'arc transverse)</mark>
- s'il existe une arête entre 2 sommets, il y a forcément un ancêtre ou un descendant du sommet

#### <mark class="hltr-blue hltr-bold">Théorème 3 (Début et Fin)</mark>

Pour tous sommets voisins x et y :
Debut(x) < Debut(y) =>

### <mark class="hltr-pink hltr-bold">Tri topologique</mark>
- Exemple : on veut supprimer une table qui fait référence à une autre table
