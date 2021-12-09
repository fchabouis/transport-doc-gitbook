---
description: Compte-rendu de l'OpenLab "Stationnement cyclable" du 25 novembre 2020.
---

# 25/11/2020 - Stationnement cyclable #1

## Documents

* [Présentation](https://docs.google.com/presentation/d/1iFqNwBK1MvxqIevlXN5lJYvfja9X352fteV2mtP-n0U/edit?usp=sharing)
* [Schéma](https://docs.google.com/spreadsheets/d/1P-SmgmR3Fos7MMq4jeWi3S4N9KSqy0v6inu8zW4pG-A/edit?usp=sharing)

## Participants

* pour transport.data.gouv.fr :
  * Antoine Desbordes
  * Benoit Queyron
  * Miryad Ali
  * Nicolas Berthelot (animation)
* Alexia Harrang (DRIEA)
* Arnaud Grenier (Montpellier)
* Benoît Chaumeret (Ville de Paris)
* Cindie Andrieu-Dupin (DRIEA)
* Corentin Lemaitre (Nantes)
* Fabien Commeaux (Vélo & Territoire)
* Geoffrey Aldebert (Etalab, data.gouv.fr)
* Josée Sabourin (MobilityData)
* Julien de Labaca (MobilityData)
* Jérémie Valentin (Montpellier)
* Léonard Vassord (Brest métropole)
* Mathias Vadot (Droit au Vélo ADAV)
* Natacha Roger (Ministère Transition Ecologique, DGITM)
* Nicolas Madignier (Grand Poitiers)
* Olivier Asselin (Métropole Européenne de Lille)
* Quentin Paternoster (Fractale)
* Sabine Carette (SMT, Tours Métropole)
* Simon Réau (Geovelo)
* Stéphane Mével-Viannay (GéoBretagne)
* Thomas Montagne (Vélo & Territoire)
* Violette Baccou (DGITM)
* Vivien Michon (Île-de-France Mobilité)

## Compte-rendu

### Localisation de l'emplacement

> Proposition : Modélisation dans un fichier csv avec xlong ylat en projection WGS84 ; un point géolocalisé  par groupe d'accroches (plutôt que par accroche)

_Nicolas M. (Poitiers)_ : base stationnement vélo fait par groupe d'accroche > champ "nbre de place". pas utile d'identifier un point par mobilier \
_Arnaud G. (Montpellier)_ : Sur Montpellier, c'est également par groupe d'accroche. \
_Simon R. (Geovelo)_ : Par groupe d'accroche > permet d'avoir des cartes nettes \
_Léonard V. (Brest)_ : par groupe d'accroche mais sur chaque site il peut y avoir des typologies différentes (couverts/non couverts) et dans ces cas > 2 points/carte

| Propositions              | Votes  | Pourcentage |
| ------------------------- | ------ | ----------- |
| **Par groupe d'accroche** | **13** | **81,3%**   |
| Par accroche              | 1      | 6,3%        |
| Ne se prononce pas        | 2      | 13,5%       |

| Propositions       | Votes  | Pourcentage |
| ------------------ | ------ | ----------- |
| Lambert93          | 4      | 22,2%       |
| **WGS84**          | **10** | **55,6%**   |
| Ne se prononce pas | 4      | 22,2%       |

_Autres échanges sur la localisation_

Q - _Arnaud G. (Montpellier):_ "Sur OSM, le stationnement vélo est également représenté par des polygones, notamment pour les parkings de grande surface. Est-ce pris en compte dans le projet actuel ?" \
R - _Nicolas B. (transport)_ : La solution est de synthétiser le polygone en un point pour simplifier la saisie et le maintien du fichier.\
_Simon R. (Geovelo)_: réutilise données stationnement OSM sous système de point. Dans l'identifiant OSM : mettre la nature de l'objet (relation (r), noeud (n), voie (w)) pour éviter les doublons.&#x20;

Q - _Cindie A.-D. (DRIEA)_ : Dans le schéma, comment est représentée l'emprise sur la voirie d'un groupe d'accroches représenté par un point : notion de surface, longueur ? \
R - _Nicolas B. (transport)_ : on est plus sur l'équipement que sur l'occupation de la voirie > l'emprise n'est pas pris en compte dans le schéma actuel

### **Nature du mobilier**

> Proposition : Valeurs entrées en texte, types limités. Liste issue d’OSM. Champ optionnel.&#x20;

_Stéphane M.-V. (GeoBretagne)_ : La typologie peut suivre des usages. En Bretagne on distingue les équipements pour stationner de courte/longue durée. Cela permet d'avoir une stratégie prescriptive de ce qu'est un bon équipement.\
_Nicolas B. (transport)_ : on veut représenter ce qui existe sans donner de prescription

_Corentin L. (Nantes)_ : le champ sur le mobilier devrait être obligatoire

| Propositions          | Votes | Pourcentage |
| --------------------- | ----- | ----------- |
| **Champ obligatoire** | **9** | **56,3%**   |
| Champ optionnel       | 5     | 31,3%       |
| Ne se prononce pas    | 2     | 12,5%       |

_Nicolas B. (transport)_ : un champ complémentaire pourrait être proposé pour préciser la valeur "Autre"

Proposer une FAQ claire pour expliquer quel mobilier choisir.&#x20;

### Protection de l'équipement

> Proposition : champ optionnel. Valeurs autorisées : stationnement non fermé, consigne collective fermée, box individuel fermé, autre

A l'intérieur de la typologie de l'équipement mais vu que ça se recoupe avec la nature > on le rattache à l'abri Vidéo/surveillance humaine etc. > voir avec C.Duquesnes pour que ça soit cohérent avec la LOM

### Couverture de l'équipement

> Proposition : champ optionnel, booléen&#x20;

Que faire si l'équipement n'est pas parfaitement couvert (par exemple des box avec des trous) ?\
_Benoît C. (Paris)_ : C'est à la discrétion du producteur de données de préciser l'information selon ce qui lui semble pertinent.&#x20;

### Accessibilité des équipements

> Proposition : champ optionnel, Valeurs autorisées : public, privé, payant

_Benoît C. (Paris)_ : Ambigu comme valeur. Il peut y avoir des abris sécurisés mais publique car pour toute personne abonnées aux transports en commun, dans les hôpitaux où ça peut être considéré comme privé mais accessible à toute personne qui va à l'hôpital.

Plutôt utiliser un booléen : accès libre/accès restreint et préciser les conditions d'accès en commentaire et grâce au champ URL.&#x20;

### **Sécurisation de l'emplacement**

> Proposition : champ optionnel, booléen&#x20;

Il y a une différence entre un emplacement gardé par un gardien et un emplacement sous vidéo-surveillance, faudrait-il différencier ? On pourrait faire deux champs distincts mais OSM ne différencie pas ces deux aspects.&#x20;

| Propositions                              | Votes  | Pourcentage |
| ----------------------------------------- | ------ | ----------- |
| Deux champs (gardienné et vidéosurveillé) | 4      | 22,2%       |
| **Un seul champ (surveillé)**             | **11** | **61,1%**   |
| NSP                                       | 3      | 16,7%       |

### Capacité de l'emplacement &#xD;

> Proposition : champ obligatoire, on dénombre le nombre de places effectives de l'emplacement

Le champ pourrait ne pas être obligatoire.&#x20;

| Propositions          | Votes | Pourcentage |
| --------------------- | ----- | ----------- |
| **Champ obligatoire** | **8** | **47,1%**   |
| Champ optionnel       | 7     | 41,1%       |
| NSP                   | 2     | 11,8%       |

### Granularité de la base

> Proposition : une ligne par groupe d'équipements cohérents localisés au même endroit. Si au même emplacement des équipements de différentes natures sont présents, on double cette ligne.

### Métadonnées

> Certaines informations contextuelles peuvent être utiles :&#x20;
>
> * identifiant du stationnement cyclable dans la base de données source (locale ou OSM)
> * identifiant national
> * code insee de la commune de rattachement
> * état de l'équipement (en service, hors service, en projet...)
> * date de mise en place de l'équipement
> * date de mise à jour des données
> * source de la donnée
> * site web d'information sur le stationnement cyclable
> * commentaire

Remarques sur le champ état de l'équipement qui devrait se limiter à : en service / hors service.



###











>

