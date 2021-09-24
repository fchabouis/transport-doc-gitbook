# 08/04/2021 - Zones à Faibles Emissions \#1

## Documents

* [Présentation](https://docs.google.com/presentation/d/1VhroWRWISD9vtkKq18-TTQZu8aZyxNEJsrBLZcH1x0g/edit#slide=id.gcebcbf8b6b_0_240)
* [Schéma](https://docs.google.com/spreadsheets/d/1ScvSWENXt20OltPCejFMCgUnjskBLzQcR-nOYamABdM/edit#gid=1796371647)

## Participants

* pour transport.data.gouv.fr : 
  * Miryad Ali
  * Nicolas Berthelot \(animateur\)
* 
  Aline   Batifol, Mappy

* Frédéric   Petit  , Grenoble Alpes Métropole
* Geoffrey Aldebert, Etalab
* Jean-Philippe Elie, Logistic Low-Carbon





* Mélanie   Gidel, Ville de Paris
* Cindie   Andrieu-Dupin, DRIEAT Île-de-France
* Patrick   Pigache, Ville de Paris
* Gaël   Pognonec, GRT Gaz 
* Cédric   Devun
* Martin   Burgat, TomTom
* Stéphane   Levesque
* Jérôme Olivet  , DREAL Occitanie
* Xavier Bourat, Total
* Jérémy   Bourreau  , Métropole de Lyon 
* Aurélie   Bayol  , Toulouse Métropole
* Jérémy   Courel, Institut Paris Région
* Priscilla   Zachée, TomTom
* Nicolas   Madignier  , Grand Poitiers
* Renan   Perault  , CEREMA



## Compte rendu

### Géométrie de la Zone à Faibles Emissions

Trois options sont proposées pour modéliser les Zones à Faibles Emissions : 

* **Option 1 :** Zones avec exclusion des axes hors ZFE

  ![](https://lh3.googleusercontent.com/KwbXCsnJ-0EI_RQyFBLtyD_z4gT3DQQxWqjIr0dP_JIrlVIgVN0avZW9dCKJQCDehum2AGCZV4BW0Ek0_H9p_oQhQJ-W3_WELTII95GF_wh7YeX_wghXchkkOWafiEZnNG9Zm52Lvso)

* **Option 2 :** Filaire routier complet représentant les tronçon concernés par la ZFE

  ![](https://lh5.googleusercontent.com/8Qd0Of9QwFaruVGqk11P11zP6AQy7RLiB-12Lbb8X7lPWrkZCgENdXR4-b49dEbzN7VBIsTi-AEQFM7h0UYu1pxeTE8DxmN9TKUnPYgmXeYX94LTsz8xZdqBdhm_lkNe6rQFZZY7BAQ)

* **Option 3 :** Zonage de la ZFE + filaire routier représentant les axes exclues de la ZFE

  ![](https://lh4.googleusercontent.com/vsTX1WgqBVoed3H51mC-Sl9CVr7phxEzUD8OSlFPG5ZcHEoaF1mayfyCYOqD7HH_ykMTu5jBOmgEbSwDFHRJSbxFwNfu1y3XkpiR8bMNhz6CzJuZiBwnZrgV7YG9v4QcyTNzhtUC31U)\_\_

_Retours des participants :_ 

N. Madignier : La base adresse qui va peut être entrer en ligne de compte car il faudra identifier des groupements de noms de rue. Faire jointure entre base adresse et filaire de voirie 



P. Pigache : la 1ère option est simple mais la complexité est la retranscription cartographique d’arrêtés qui n’ont pas été pensés pour en faire de la cartographie. Est-ce identique sur tout le territoire ? Besoin d'homogénéiser les arrêtés 

G. Pognonec : Option 1 la plus simple pour mettre en oeuvre même si ce n’est pas la plus fine. Partie de prendre en compte toute la commune et vont donc élargir la carte par rapport à la réalité de la ZFE. Lyon ils ont essayé de faire l’option 3 mais assez compliqué. Pour les geoshape ils utilisent une base de l’INSEE

P. Zachée : Aimerait avoir zone+filaire pour chaque ZFE car avoir ces 2 sources pourrait permettre de résoudre certaines problèmes dont mix/match de leur référentiel filaire et celui qui sera fourni

Ils présentent ces deux types de présentation dans leurs données : ZFE représenté par zone et sont attribués à l’axe

N.Berthelot : on pourrait envisager de faire un mix des deux:  
1/ Identifiant pour la zone avec des propriétés  
2/avoir le filaire où on met ID zone qu’on pourra affilié  

P. Pigache: l’option 3 a un gros intêrét. Veulent pas un JDD pour une même thématique mais on pourrait le faire excepetionnellement   
Ne mettre en filaire que les exceptions  
Référentiel axe routier : se baser sur l’IGN. Il faut avoir un référentiel commun  
L'option 1 va poser de gros problème notamment sur les périphériques car pas assez de précision sur les zones d’exclusion. Données aura des conséquences car il y a des amendes si pas respect de ces zones   
Le PAN pourrait proposer un exemple d’arrêté

A. Batifol : Mix&match plus simple sur l’option 2

F. Petit : L'Option 2 est compliqué si les petites collectivités n’ont pas les ressources alors que ce modèle doit être généralisable d’où la nécessité d’avoir un modèle d’arrêté précis 

P. Pigache : si toutes les métropoles produisent filaires de toutes leurs voiries &gt; va être lourd et alourdir les serveurs. Dans la production, si les arrêtés le permettent, 

J. Olivet : Montpellier a pris un arrêté selon les zones. Option 1 leur conviendrait le mieux mais comme ZFE doit être sur toute la métropole, la zone 3 sera la meilleure option car il y aura des voies exclues de la ZFE dans les ZFE

**Résultat du vote** 



| Propositions | Votes | Pourcentage |
| :--- | :--- | :--- |
| Option 1 | 2 | 11% |
| Option 2 | 0 | 0% |
| Option 3 | 7 | 39% |
| Option 1+2 | 9 | 50% |

L'option 1+2 fonctionnerait concrètement avec deux fichiers : 

* une table géométrique contenant les géométrie des zones de la ZFE \(en excluant les axes routiers hors-ZFE\) + les informations réglementaires de la ZFE + un identifiant de zone
* un fichier de géométrie de l'ensemble des tronçons routiers concernés par la ZFE avec un identifiant renvoyant à la zone dont fait partie le tronçon avec les réglementations associées.

### Identifiant de la Zone à Faibles Emissions

La proposition est de composer un identifiant à partir du code SIREN de la zone administrative englobant la ZFE. Si la ZFE se limite à une commune, on utilise le SIREN de la commune ; si la ZFE concerne une zone contenue dans un EPCI, le code SIREN de l'EPCI. Il peut y avoir avoir plusieurs zones au sein d'une même zone administrative aussi on ajoutera une valeur incrémenté pour obtenir ce type d'identifiant :   
200046977-ZFE-001

### Catégorie de véhicule 

A ce stade 5 catégories de véhicules : 

* les véhicules particuliers, 
* les véhicules utilitaires légers \(&lt;3,5 t\) 
* les poids lourds \(&gt;3,5t\)
* autobus et autocars
* 2 roues, tricycles et quadricycles à moteur

P. Zachée : Il faudrait également ajouter la catégorie "taxis"

De nombreux véhicules en fonction de leur utilisation \(urgence, covoiturage...\) échappent aux réglementations. Il semble compliqué de modéliser ces exceptions à ce stade nous nous limiterons donc à ces 5 catégories + les taxis.

### **Vignettes concernées**

Pour chaque catégorie de véhicule il est nécessaire d'associer une vignette Crit'Air nécessaire pour accéder à la zone. La méthode proposée est d'indiquer les catégories de vignettes concernées par des tirets. Par exemple si la zone  est interdite aux véhicules de vignettes Crit'air 4, 5 et sans vignettes on indiquerait 4-5-NC.

La séparateur tiret n'est pas idéal il faut donc proposer une autre solution. Un champ à choix multiple pourrait être plus efficace. 

Proposition retenue : modalités fermées :  
- CRITAIR 1 ET INFERIEUR  
- CRITAIR 2 ET INFERIEUR  
- CRITAIR 3 ET INFERIEUR  
- CRITAIR 4 ET INFERIEUR  
- CRITAIR 5 ET INFERIEUR 

### **Date d'entrée en vigueur** 

Ce champ pourrait permettre de publier en avance des réglementations.

P.Pigache : Le problème est qu'il faut toujours attendre la publication de l'arrêté qui matérialise l'entrée en vigueur. Et il et très complexe de connaître précisément son contenu avant publication.

L'attribut est conservé mais il ne sera pas utilisé pour indiquer la création de futures zones ou de nouvelles restrictions.









