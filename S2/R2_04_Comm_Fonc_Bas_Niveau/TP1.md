B.

Exercice : expliquer brievement
- ADD R0, R1, #42 : Additionne 42 à la valeur du registre R1 et stocke le résultat dans le registre R
- LDR R5, 98 : Place la valeur stockée à l'adresse mémoire 98 dans le registre R5
- CMP R4, #18 : Compare la valeur stockée dans le registre R4 et la valeur 18
- BGT 77 : La prochaine instruction à exécuter se trouve à l'adresse mémoire 77  si la valeur stockée dans le registre R4 est plus grande que 18 (se référer avec CMP avant)
- STR R0, 15 : Place la valeur stockée dans le registre R0 en mémoire vive à l'adresse 15
- B 100 : Structure de rupture de séquence : la prochaine instruction à exécuter se situe en mémoire vive à l'adresse 100

Exercice : Ecrire les instructions en assembleur

- « Additionne la valeur stockée dans le registre R0 et la valeur stockée dans le registre R1, le résultat est stocké dans le registre R5 » : ADD R5, R0, R1
- « Place la valeur stockée à l'adresse mémoire 878 dans le registre R0 » : LDR R0, 878
- « Place le contenu du registre R0 en mémoire vive à l'adresse 124 » : STR R0, 124
- « La prochaine instruction à exécuter se situe en mémoire vive à l'adresse 478 » : B 478
- « Si la valeur stockée dans le registre R0 est égale 42 alors la prochaine instruction à exécuter se situe à l'adresse mémoire 85 » : 
	- CMP R0, #42
	- BEQ 85


Question :
- Identifiez la valeur 42 dans la mémoire ? Ce sont les 8 derniers bits de R0

Question :
- À quoi sert la ligne B endif ? A faire une rupture de sequence et exécuter l'instruction au label endif
- À quoi correspondent les adresses mémoires 23, 75 et 30 : 
	- 23 : stocke temporairement la valeur 6 (z)
	- 75 : stocke temporairement la valeur 9 (y)
	- 30 : stocke temporairement la valeur de x