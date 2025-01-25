# <mark class="hltr-blue" style="font-size:50px;">Les processus</mark>

# <mark class="hltr-orange">Intro</mark>

	Programme
	Processus (instance d'un prog en cours d'exec)
Le programme est chargé dans la mémoire vive, ses instructions sont exec par le processeur.
L'OS lui fourni un espace d'adressage

	Un OS multitache doit pouvoir traiter plusieurs processus en même temps

	ps -aux [| grep nom_processus]
# <mark class="hltr-orange">Ordonnanceur et les états possibles</mark>

	Partie du noyau qui chjoisit quel processus doit s'exécuter à un moment donné