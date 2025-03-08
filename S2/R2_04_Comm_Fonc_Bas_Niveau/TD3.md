
## <mark class="hltr-green format">A. Exercice 2</mark>


| IP                           | Classe d'adresse                             | Masque        | Addr réseau   | Masque Sous réseau                                                                                              | Addr sous-réseau et num | Num machine (hote) sous réseau | Intervalles d'addr utilisables pour 3 premiers sous-réseaux |
| ---------------------------- | -------------------------------------------- | ------------- | ------------- | --------------------------------------------------------------------------------------------------------------- | ----------------------- | ------------------------------ | ----------------------------------------------------------- |
| 145.245.45.225 (60 sous-res) | B car premier octet compris entre 128 et 191 | 255.255.0.0   | 145.245.0.0   | 255.255.252.0, car on doit rajouter 6 bits car 2^6>60 donc 6 bits à 1 et le reste à 0, on trouve 11111100 = 252 |                         | Voir feuille                   |                                                             |
| 202.2.48.149 (15 sous-res)   | C car octet compris entre 192 et 223         | 255.255.255.0 | 202.2.48.0    | 255.255.255.240                                                                                                 |                         |                                |                                                             |
| 97.124.36.142 (200 sous-res) | A car octet compris entre 0 et 127           | 255.0.0.0     | 97.0.0.0      | 255.255.0.0                                                                                                     |                         |                                |                                                             |
| 172.24.245.25                | B                                            | 255.255.0.0   | 172.24.0.0    | 255.255.255.0                                                                                                   |                         |                                |                                                             |
| 212.122.148.49               | C                                            | 255.255.255.0 | 212.122.148.0 | 255.255.255.224                                                                                                 |                         |                                |                                                             |

## <mark class="hltr-green format">B. Exercice 1</mark>

Il faut 4 bits car 2^4 > 7 réseaux



| IP                | ID sous-réseau | Première machine | Dernière machine configurée | Broadcast | ID sous-réseau |
| ----------------- | -------------- | ---------------- | --------------------------- | --------- | -------------- |
| SR1 : 38 machines |                |                  |                             |           |                |
| SR2 : 33 machines |                |                  |                             |           |                |
| SR3 : 52 machines |                |                  |                             |           |                |
| SR4 : 35 machines |                |                  |                             |           |                |
| SR5 : 34 machines |                |                  |                             |           |                |
| SR6 : 37 machines |                |                  |                             |           |                |
| SR7 : 25 machines |                |                  |                             |           |                |
