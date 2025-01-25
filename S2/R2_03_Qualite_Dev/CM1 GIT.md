# <mark class="hltr-purple hltr-bold">CM1 GIT</mark>

## <mark class="hltr-green hltr-bold">Gestion des versions</mark>

Pourquoi des versions :
- Partage de fichiers => travail en équipe
- Traçabilité / Historisation => permet de revenir en arrière si bug
- Branches multiples
Pourquoi un gestionnaire (git) :
- plus organisé qu'un partage de fichiers
- meilleure gestion des conflits
- il en existe plusieurs :
	- CVS
	- SVN
	- GIT

## <mark class="hltr-green hltr-bold">Les dépôts</mark>
### <mark class="hltr-pink hltr-bold">Plusieurs hébergements</mark>
- local : dépôt sur la machine 
	- git init
- github : serveur gratuit pour les projets open-source
	- compte requis
- bitbucket : serveur gratuit pour petits projets (5 comptes)
	- compte requis
- gitlab : serveur DevOps gratuit (sous conditions)
	- compte requis
	- serveur à l'université via etupass : https://git.unicaen.fr
	- image docker disponible
- forge : serveur (par ex : RedMine) pour la gestion de projet
	- serveur à l'université via etupass : https://redmine-etu.info.unicaen.fr
	- GIT ; SVN ; Gantt ; ...

### <mark class="hltr-pink hltr-bold">3 espaces à gérer</mark>
GIT repose sur 3 espaces de fichiers :
- Zone de travail : Working-Directory => nos fichiers
- Index : les fichiers à valider
- HEAD : les fichiers versionnés (branche courante)
La commande **git status** compare ces trois zones.

## <mark class="hltr-green hltr-bold">Terminologie</mark>
- un dépôt : repository, une gestion de version avec l'historique
- un dépôt nu : bare repository, un dépôt où on ne travaille pas
	- pas de Working-Directory, ni d'Index
- un commit : abus de langage pour désigner une version en particulier
- commiter : un barbarisme pour désigner l'action de créer une nouvelle version pour des fichiers de l'espace de travail
- non suivi : un fichier dans l'espace de travail, mais pas dans l'index
- modifié : un fichier présent dans l'espace de travail mais différent de la version indexée
- non modifié : un fichier présent dans l'espace de travail et cohérent avec la version indexée
- validé : un fichier cohérent dans les 3 espaces
- supprimé : dans l'index mais pas dans l'espace de travail

## <mark class="hltr-green hltr-bold">Les commandes</mark>

git remote remove : retire un dépôt distant
git checkout : permet de changer de branche ou de versions de fichiers

Outils pour visualiser git : https://git-school.github.io/visualizing-git

git commit --amend : modifie le dernier commit (non poussé) au lieu d'en créer un nouveau

git rm \<fichiers\> : supprime le/les fichiers du disque et de l'index
git rm --cached \<fichiers\> : supprime le/les fichiers de l'index mais pas du disque

git rebase HEAD : efface le dernier commit (que en local)
git restore --staged \<fichiers\> : retire les fichiers de l'index (utile quand on fait un git add par erreur)

git merge \<branche\> récupère les fichiers de la branche spécifié