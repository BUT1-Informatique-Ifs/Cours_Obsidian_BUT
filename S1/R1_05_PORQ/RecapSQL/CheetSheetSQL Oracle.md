# <mark class="hltr-blue hltr-bold">Spécificités d'Oracle</mark>

## <mark class="hltr-purple hltr-bold">Les schémas</mark>

	Sur Oracle, les schémas sont des utilisateurs associés à des
	collections d'objets comme des tables ou autres.
	Donc à chaque création d'utilisateur de la base, on crée un schéma.

##### <mark class="hltr-grey hltr-bold">Exemple</mark>

Dans la base de donnée de M. PORQ, `prof`est un schéma qui possède plusieurs tables, etc.. 

## <mark class="hltr-purple hltr-bold">Les types VS les autres SGBD</mark>

|                     | Oracle                                                                 | SGBD Standard               |
| ------------------- | ---------------------------------------------------------------------- | --------------------------- |
| Entier              | $\textcolor{red}{number}\textcolor{blue}{(x)}$                         | int                         |
| Réel                | $\textcolor{red}{number}(\textcolor{blue}{x}, \textcolor{magenta}{y})$ | float                       |
| Chaîne de caractère | $\textcolor{red}{varchar2}\textcolor{blue}{(x)}$                       | char($\textcolor{blue}{x}$) |
| Date                | date                                                                   | date                        |
- Entier $\textcolor{blue}{x}$ : c'est <mark class="hltr-red hltr-bold">le nombre de CHIFFRES</mark> dans le nombre
- Réel $\textcolor{blue}{x}$ : c'est <mark class="hltr-red hltr-bold">le nombre de CHIFFRES totaux</mark> dans le nombre (y compris ceux de le nombre de la virgule)
- Réel $\textcolor{magenta}{y}$ : c'est l<mark class="hltr-red hltr-bold">e nombre de CHIFFRES après la virgule</mark>
- Chaîne de caractère $\textcolor{blue}{x}$ : c'est <mark class="hltr-red hltr-bold">le nombre de caractères</mark> dans la chaîne

##### <mark class="hltr-grey hltr-bold">Exemples en Oracle</mark>

1. 45 : c'est un entier, il a 2 chiffres => number(<mark class="hltr-grey hltr-bold">2</mark>)
2. 457,345 : c'est un réel, il a 6 chiffres au total dont 3 après la virgule => number(<mark class="hltr-grey hltr-bold">6</mark>, <mark class="hltr-grey hltr-bold">3</mark>)
3. "M.Porq et le SQL" : c'est une chaîne de caractère, elle a 16 caractères => varchar2(<mark class="hltr-grey hltr-bold">16</mark>)

# <mark class="hltr-blue hltr-bold">Base de données et mots clés</mark>

## <mark class="hltr-purple hltr-bold">La création et suppression de table</mark>

	drop ; create table ; commit
### <mark class="hltr-green hltr-bold">Procédure pour créer une table</mark>

1. On supprime la potentielle table existante
	- <mark class="hltr-red hltr-bold">drop table</mark> la_table;
2. On crée notre table
	- <mark class="hltr-red hltr-bold">create table</mark> la_table(nom_colonne1 <mark class="hltr-yellow hltr-bold">type</mark>, nom_colonne2 <mark class="hltr-yellow hltr-bold">type</mark>, ..);


## <mark class="hltr-purple hltr-bold">L'insertion de valeur dans une table</mark>

	insert into ; values

### <mark class="hltr-green hltr-bold">Syntaxe pour ajouter des valeurs à la table</mark>

<mark class="hltr-red hltr-bold">insert into</mark> la_table(colonne1, ...) <mark class="hltr-red hltr-bold">values</mark>(valeur_colonne1, valeur_colonne2, ..);

## <mark class="hltr-purple hltr-bold">Les jointures</mark>

	where ; join on ; join using ; left join ; right join

### <mark class="hltr-green hltr-bold">Les équijointures</mark>

![[schema_equijointure.png]]

Il faut <mark class="hltr-red hltr-bold">TOUJOURS</mark> <mark class="hltr-red hltr-bold">associer les clés primaires communes aux 2 tables</mark>, sinon on risque d'avoir un **produit cartésien** entre les 2 tables (nombreDeLignesTable1 * nombreDeLignesTable2).

##### <mark class="hltr-pink hltr-bold">Le where</mark>

	On sépare par une virgule les tables qu'on veut lier et on associe
	leurs clés primaires dans le where.

select attribut_1, .. from <mark class="hltr-red hltr-bold">table_1, table_2</mark> 
<mark class="hltr-red hltr-bold">where</mark> <mark class="hltr-yellow hltr-bold">cle_primaire_1 = cle_primaire_2</mark> ...;
##### <mark class="hltr-pink hltr-bold">Le join on</mark>

	On sélectionne la première table et on utilise join table on et
	on associe leurs clés primaires.

select attribut_1, .. from table_1
<mark class="hltr-red hltr-bold">join</mark> table_2 <mark class="hltr-red hltr-bold">on</mark> <mark class="hltr-yellow hltr-bold">cle_primaire_1 = cle_primaire_2</mark> ...;

##### <mark class="hltr-pink hltr-bold">Le join using</mark>

	On sélectionne la première table et on utilise join table using
	et on spécifie toute les clés primaires communes aux 2 tables dans
	le using (séparés par des virgules).

select attribut_1, .. from table_1
<mark class="hltr-red hltr-bold">join</mark> table_2 <mark class="hltr-red hltr-bold">using</mark>(<mark class="hltr-yellow hltr-bold">cle_primaire_commune</mark>, ..);

### <mark class="hltr-green hltr-bold">Les jointures externes</mark>

##### <mark class="hltr-pink hltr-bold">Le left join</mark>

	On récupère tous les enregistrements présents dans la table 
	dominante et ceux communs avec la table subordonnee (table dominante
	et intersection)


select attribut_1, .. from <mark class="hltr-yellow hltr-bold">table_dominante</mark>
<mark class="hltr-red hltr-bold">left join table_subordonnee</mark> on table_dominante.cle_primaire = table_subordonnee.cle_primaire;

![[schema_leftjoin.png]]

##### <mark class="hltr-pink hltr-bold">Le right join</mark>

	On récupère tous les enregistrements présents dans la table 
	dominante (celle à droite) et ceux communs avec la table subordonnee
	(c'est un left join déguisé car seul l'emplacement des tables dans
	la requête sont changés, table dominante à droite).

select attribut_1, .. from <mark class="hltr-yellow hltr-bold">table_subordonnee</mark>
<mark class="hltr-red hltr-bold">right join table_dominante</mark> on subordonnee.cle_primaire = table_dominante.cle_primaire;

![[schema_rightjoin.png]]