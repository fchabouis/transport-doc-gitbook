---
description: >-
  Ce schéma est une traduction du schéma json des aménagements cyclables au
  format tableur. Il a pour objectif de faciliter la compréhension des champs.
---

# Schéma au format tableur

Ce schéma, sous format tableur, reprend le schéma des aménagements cyclables publié au format json sur le[ GitHub dédié à ce schéma](https://github.com/etalab/schema-amenagements-cyclables). Cette version tableur est une simplification du schéma afin d'en faciliter la compréhension. Toute personne voulant se renseigner doit se baser sur la [version json](https://github.com/etalab/schema-amenagements-cyclables/blob/master/schema\_amenagements\_cyclables.json) qui est plus détaillée et la plus à jour. &#x20;

{% hint style="warning" %}
Les coordonnées géographiques des aménagements cyclables ne correspondent pas à des points mais à des formes géographiques. Elles ne seront pas représentées dans ce tableau bien que ce champ soit obligatoire. \
Le WGS84 est le système géodésique attendu.&#x20;
{% endhint %}

{% hint style="info" %}
* Certains champs ont des valeurs pré définies dans des listes déroulantes comme les champs "reseau\_loc", "ame\_d" etc. Ces valeurs ne seront pas listées dans ce schéma. Veuillez vous reporter au [schéma json ](https://github.com/etalab/schema-amenagements-cyclables/blob/master/schema\_amenagements\_cyclables.json)pour avoir ces détails.&#x20;
* La valeur "booléen" renvoie à "true" ou "false"&#x20;
{% endhint %}

## Schéma

| nom          | description                                                                                                                               | type                 | Propriétés                                                |
| ------------ | ----------------------------------------------------------------------------------------------------------------------------------------- | -------------------- | --------------------------------------------------------- |
| id\_local    | identifant local de l'aménagement                                                                                                         | chaîne de caractères | valeur obligatoire                                        |
| reseau\_loc  | type de réseau structurant local auquel l'aménagement appartient                                                                          | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| nom\_loc     | nom et numéro des itinéraires locaux                                                                                                      | chaîne de caractères | valeur optionnelle                                        |
| id\_osm      | identifiant de l'aménagement sur OpenStreetMap (OSM)                                                                                      | chaîne de caractères | valeur optionnelle                                        |
| num\_iti     | numéro des itinéraires, des EuroVelo au schéma départementaux, auxquels le segment appartient. Séparé par « : »                           | chaîne de caractères | valeur optionnelle                                        |
| code\_com\_d | code INSEE de la commune (5 caractères alphanumériques) sur la voie de droite                                                             | chaîne de caractères | valeur obligatoire                                        |
| ame\_d       | type d'aménagement présent sur la voie de droite                                                                                          | chaîne de caractères | <p>valeur obligatoire</p><p><em>liste déroulante</em></p> |
| regime\_d    | régime présent sur la voie de droite                                                                                                      | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| sens\_d      | sens de circulation pour les cyclistes sur la voie de droite                                                                              | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| largeur\_d   | largeur hors marquage minimale utile de la voie de droite réservée au cycliste, en mètre. La largeur du marquage est exclue               | nombre               | valeur optionnelle                                        |
| local\_d     | emplacement de l'aménagement sur la voie de droite                                                                                        | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| statut\_d    | niveau de réalisation de l'infrastructure sur la voie de droite                                                                           | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| revet\_d     | type de revêtement de l'aménagement sur la voie de droite                                                                                 | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| code\_com\_g | code INSEE de la commune (5 caractères alphanumériques) sur la voie de gauche                                                             | chaîne de caractères | valeur obligatoire                                        |
| ame\_g       | type d'aménagement présent sur la voie de gauche                                                                                          | chaîne de caractères | <p>valeur obligatoire</p><p>liste <em>déroulante</em></p> |
| regime\_g    | régime présent sur la voie de gauche                                                                                                      | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| sens\_g      | sens de circulation pour les cyclistes sur la voie de gauche                                                                              | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| largeur\_g   | largeur hors marquage minimale utile de la voie de gauche réservée au cycliste, en mètre. La largeur du marquage est exclue               | nombre               | valeur optionnelle                                        |
| local\_g     | emplacement de l'aménagement sur la voie de gauche                                                                                        | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| statut\_g    | niveau de réalisation de l'infrastructure sur la voie de gauche                                                                           | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| revet\_g     | type de revêtement de l'aménagement sur la voie de gauche                                                                                 | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| access\_ame  | accessibilité des amanégements par type de véhicule à deux roues non motorisé                                                             | chaîne de caractères | <p>valeur optionnelle</p><p><em>liste déroulante</em></p> |
| date\_maj    | date de dernière mise à jour des données du segment Notation ISO 8601, format AAAA-MM-JJ                                                  | chaîne de caractères | valeur optionnelle                                        |
| trafic\_vit  | vitesse maximale autorisée pour le trafic adjacent à l'aménagement, en km/h. La vitesse 5 km/h correspond à une vitesse à l'allure du pas | nombre entier        | valeur optionnelle                                        |
| lumiere      | aménagement éclairé                                                                                                                       | chaîne de caractères | <p>valeur optionnelle</p><p><em>booléen</em> </p>         |
| d\_service   | date de mise en oeuvre de l'aménagement (AAAA)                                                                                            | nombre               | valeur optionnelle                                        |
| comm         | remarques éventuelles au sujet de l'aménagement                                                                                           | chaîne de caractères | valeur optionnelle                                        |
| source       | entité ayant fourni les données                                                                                                           | chaîne de caractères | valeur optionnelle                                        |
| project\_c   | projection cartographique utilisée                                                                                                        | chaîne de caractères | valeur optionnelle                                        |
| ref\_geo     | référentiel géographique utilisé                                                                                                          | chaîne de caractères | valeur optionnelle                                        |

## Exemple&#x20;

| id\_local | reseau\_loc | nom\_loc | id\_osm    | num\_iti       | code\_com\_d | ame\_d         | regime\_d     | sens\_d         | largeur\_d | local\_d | statut\_d  | ame\_g         | regime\_g     | sens\_g         | largeur\_g | local\_g | statut\_g  | access\_ame | date\_maj  | trafic\_vit | lumiere | d\_service | comm                      | source         | project\_c | ref\_geo |
| --------- | ----------- | -------- | ---------- | -------------- | ------------ | -------------- | ------------- | --------------- | ---------- | -------- | ---------- | -------------- | ------------- | --------------- | ---------- | -------- | ---------- | ----------- | ---------- | ----------- | ------- | ---------- | ------------------------- | -------------- | ---------- | -------- |
| 751AC     | Structurant | V1       | 7746952719 | 0001:0006:0045 | 75114        | BANDE CYCLABLE | AIRE PIETONNE | UNIDIRECTIONNEL | 3          | TROTTOIR | PROVISOIRE | BANDE CYCLABLE | AIRE PIETONNE | UNIDIRECTIONNEL | 4.1        | TROTTOIR | PROVISOIRE | VTT         | 2020-08-15 | 80          | true    | 2015       | forte pente sur 10 mètres | Ville de Paris | Peters     | Bdortho  |

##
