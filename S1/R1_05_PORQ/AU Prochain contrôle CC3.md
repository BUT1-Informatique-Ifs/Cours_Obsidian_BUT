utiliser trim si le type est char
Correction 2.5) c la copie de table


1.
Clé étrangère au prochain contrôle :
	- pointent sur des clés primaires
ALTER TABLE table ADD
(
	CONSTRAINT fk_NomCleEtrang
		FOREIGN KEY (colonne)
			REFERENCES table (colonne));
VAUDRA 6 points

2.
=> Insertion de valeur avec col obligatoire seulement

3.
Pour update, delete ou autre si la col est pas dans la table à modifier :
update table set col = val where col = (sous-requête);

Pour faire un apostrophe, mettre un autre apostrophe avant

4.
round au prochain contrôle