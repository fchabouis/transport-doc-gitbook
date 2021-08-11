# 24/02/2021 - Stationnement cyclable \#2

## Documents

* [Présentation](https://docs.google.com/presentation/d/1n5s2qua-n4qfDpHz5NIjq7JvL2tEMbyGdIs5wvbAzyw/edit#slide=id.gac4151b512_0_14)
* [Schéma](https://docs.google.com/spreadsheets/d/1P-SmgmR3Fos7MMq4jeWi3S4N9KSqy0v6inu8zW4pG-A/edit#gid=2092296455)

## Participants

* pour transport.data.gouv.fr : 
  * Miryad Ali
  * Nicolas Berthelot \(animateur\)
* Alexandre Chassignon, Cyclamaine
* Antoine Coué, Vélo & Territoires
* Arnaud Grenier, Montpellier Métropole
* Corentin Lemaître, Nantes Métropole
* Fabien Commeaux, Vélo & Territoires
* Fabien Ripaud, Altinnova
* Geoffray Durantet, Val d'Oise
* Heitiare Teauna
* Jean-Chripstophe Becquet, Apitux
* Léo Frachet, MobilityData
* Léonard Vassord, Brest Métropole
* Nicolas Madignier, Grand Poitiers
* Pierre Hamburger, Grenoble Alpes Métropole
* Pierre Lemasson, Copark
* Simon Réau, Géovélo
* Stéphane Mével-Viannay, GéoBretagne
* Thomas Montagne, Vélo & Territoires
* Thomas Tremblay, Altinnova
* Yohan Planche, DGITM

## Compte rendu

### Ajout du champ `lumiere`

Conformément au projet de décret sur le stationnement cyclable sécurisé, un emplacement doit être éclairé \(par un éclairage spécifique ou indirectement éclairé par un équipement urbain\) pour être considéré sécurisé.

Un champ optionnel "booléen" est donc ajouté à l'unanimité des participants.

### Ajout du champ `cargo`

Il est de plus en plus attendu par les usagers de pouvoir savoir s'ils peuvent stationner leur vélo cargo \(ou de grande taille\).

| Propositions | Votes | Pourcentage |
| :--- | :--- | :--- |
| nombre entier : nombre de places adaptées aux vélos cargos sur l'emplacement | **12** | **70,6%** |
| booléen : au moins une place adaptée au vélos cargos sur l'emplacement | 4 | 23,5 % |
| booléen : toutes les places de l'emplacement sont adaptées | 1 | 5,9% |

Le groupe de travail indique qu'il serait pertinent que cette information soit également modélisable au niveau du type de mobilier. 

| Propositions | Votes | Pourcentage |
| :--- | :--- | :--- |
| Ajouter la modalité "arceau vélo grande-taille" dans le champ `mobilier` | **8** | **57,1%** |
| Ne pas ajouter de modalité | 6 | 42,9% |

### Informations tarifaires

Une proposition de modélisation des tarifs d'accès à certains emplacements de stationnement. Le groupe de travail a manifesté sa réserve concernant cette modélisation car elle souvent très complexe et liée à de nombreuses conditions spéciales \(accès sur la base d'abonnements, réductions...\). Ce sujet devrait plutôt être abordé dans une table indépendante à laquelle on pourrait faire référence dans les données de stationnement cyclable.

| Propositions | Votes | Pourcentage |
| :--- | :--- | :--- |
| Ajouter des champs pour les informations tarifaires | **14** | **99,3%** |
| Ne pas ajouter de champs | 1 | 0,7% |

### Modification du champ `acces_libre`

Sans modélisation des informations tarifaires il est néanmoins important d'informer l'usager de pouvoir distinguer les emplacements de stationnement réservés à des usagers privés \(habitants d'un immeuble, employés d'une entreprise\) à des emplacements accessibles à des clients. 

| Propositions | Votes | Pourcentage |
| :--- | :--- | :--- |
| Passer d'un booléen à un champ à modalité : Libre/Payant/Privé | **15** | **88,2%** |
| Pas de modification | 2 | 11,8% |

### Ajout des champs `proprietaire` et `gestionnaire`

Les membres du groupe de travail indiquent qu'il est problématique de ne pas proposer aux producteurs de données de ne pas pouvoir préciser que les emplacements sont la propriétés d'une organisation et/ou gérées par une organisation. 

| Propositions | Votes | Pourcentage |
| :--- | :--- | :--- |
| Ajouter champ `proprietaire` et `gestionnaire` | **11** | **61,1%** |
| Ajouter champ `proprietaire` | 1 | 5,6% |
| Ajouter champ `gestionnaire` | 1 | 5,6% |
| Pas d'ajout de champ | 5 | 27,8% |

### 



