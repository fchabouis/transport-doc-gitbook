# Zones à Faibles Emissions

transport.data.gouv.fr propose un schéma de données pour favoriser la diffusion de l'information concernant les Zones à Faibles Emissions en France par leur intégration dans les applications de mobilité. 

## Documentation

### Fonctionnement du modèle de données

Les données concernant les Zones à Faibles Emissions repose sur deux fichiers au format GeoJSON. 

* Le premier jeu de données précise les règles sur des _aires_ de la ZFE d'un territoire
* Un second jeu de données précise les règles particulières et les exceptions sur certains _tronçons routiers_. 

Les mêmes informations sont attendues sur les deux fichiers, néanmoins la modélisation géographique est différente : Polygone ou Multi-Polygone pour les _aires _et Linestring et MultiLinestring pour les _tronçons routiers_.



### Représentation géographique

#### Aires couvertes par une Zone à Faibles Emissions

Les arrêtés mettant en place des Zones à Faibles Emissions précisent des aires administratives sur lesquelles s'appliquent une réglementation spécifique. Les géométries des aires couvertes correspondent donc généralement à des zones administratives : communes ou EPCI.

Ces géométries prennent pour référentiel le Référentiel Grande Echelle de l'IGN. AdminExpress peut être utilisé pour sélectionner les géométries de ces zones. 

Les géométries utilisent le système de projection WGS84. 

Si des zones spécifiques sont précisées par un arrêtés (centre-ville, bois...) alors le producteur de données doit modéliser aussi précisément que possible la géométrie de la zone.

#### Voies exceptionnelles

Les arrêtés précisent également régulièrement des voies spéciales où les règles de la ZFE s'appliquent différemment. 

Les géométries de ces tronçons routiers prennent pour référentiel la couche TRONCON_DE_ROUTE de la BD Topo de l'IGN.

Les géométries utilisent le système de projection WGS84.

### Granularité

#### Aires couvertes par une Zone à Faibles Emissions

Pour les aires, chaque ligne ou objet correspond à :

* une aire géographique
* décrite par un arrêté
* où la réglementation est homogène (hormis axes exceptionnels)

Aussi :

* si sur une même commune où un arrêté précise des réglementations différentes sur plusieurs zones on utilise plusieurs lignes/objets pour décrire la ZFE
* si les règles sont homogènes sur tout un EPCI mais que les arrêtés sont limités à chaque commune, on utilise autant de lignes/objets pour décrire chaque commune. 
* si les règles sont différentes pour les personnes morales et les personnes physiques on décrit la réglementation dans deux lignes/objets différentes.

#### Voies exceptionnelles

La granularité des voies exceptionnelles est la même que les tronçons routiers de la BD Topo de l'IGN. [La documentation de la BD Topo ](https://geoservices.ign.fr/ressources_documentaires/Espace_documentaire/BASES_VECTORIELLES/BDTOPO/DC_BDTOPO\_3-0.pdf)précise qu'un tronçon de routes est une _portion de voie de communication destinée aux automobiles, aux piétons, aux cycles ou aux animaux, homogène pour l'ensemble des attributs et des relations qui la concernent_.

Le découpage d'une voie en tronçon est précisé dans la documentation de la BD Topo.

### Attributs

Les aires réglementées et les voies exceptionnelles sont décrits par les mêmes attributs. Ces attributs sont essentiellement des éléments structurés extraits de la réglementation (véhicules dont la circulation est interdite, horaires d'application...).

| Attribut                  | Description                                                                                                                                                                                                                                                                                                                                                                                          | Format       | <p>Oblig<br>atoire</p> | Exemple                                                                    |
| ------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------ | ---------------------- | -------------------------------------------------------------------------- |
| id                        | <p><em>Si l'objet est une aire reglementée :</em> Identifiant unique de l'aire réglementée. Pour construire l'identifiant on utilise cette formule : 'Code SIREN de l'entité administrative englobant la zone' - ZFE - XXX. </p><p><em>Si l'objet est une voie spéciale : </em>Identifiant unique cleabs du tronçon routier issu de la couche TRONCON_DE_ROUTE de la BD Topo produite par l'IGN"</p> | string       | Oui                    | 200046977-ZFE-001,&#xD; TRONROUT0000002003832789                           |
| date_debut                | Date d'entrée en vigueur de la réglementation au format AAAA-MM-JJ.                                                                                                                                                                                                                                                                                                                                  | string       | Oui                    | 2019-07-01                                                                 |
| date_fin                  | Date de fin de la réglementation                                                                                                                                                                                                                                                                                                                                                                     | string       | Non                    | 2023-07-01                                                                 |
| vp_critair                | Véhicules particuliers : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler. L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. EL correspond aux véhicules électriques et NC aux véhicules sans vignette.                                  | string       | Non                    | V4                                                                         |
| vp_horaires               | Véhicules particuliers : jours et horaires de restriction au format 'opening hours' d'OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours                                                                                                                                                                                                                                          | string       | Non                    | <p>Mo-Fr 08:00-20:00; PH off, <br>24/7</p>                                 |
| vul_critair               | Véhicules utilitaires légers : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler. L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. EL correspond aux véhicules électriques et NC aux véhicules sans vignette.                            | string       | Non                    | V4                                                                         |
| vul_horaires              | Véhicules utilitaires légers : jours et horaires de restriction au format 'opening hours' d'OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours                                                                                                                                                                                                                                    | string       | Non                    | <p>Mo-Fr 08:00-20:00; PH off, <br>24/7</p>                                 |
| pl_critair                | Poids lourds : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler. L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. EL correspond aux véhicules électriques et NC aux véhicules sans vignette.                                            | string       | Non                    | V4                                                                         |
| pl_horaires               | Poids lourds : jours et horaires de restriction au format 'opening hours' d'OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours                                                                                                                                                                                                                                                    | string       | Non                    | <p>Mo-Fr 08:00-20:00; PH off,</p><p>24/7</p>                               |
| autobus_autocars_critair  | Autobus et autocars : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler. L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. EL correspond aux véhicules électriques et NC aux véhicules sans vignette.                                     | string       | Non                    | V4                                                                         |
| autobus_autocars_horaires | Autobus et autocars : jours et horaires de restriction au format 'opening hours' d'OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours                                                                                                                                                                                                                                             | string       | Non                    | <p>Mo-Fr 08:00-20:00; PH off,</p><p>24/7</p>                               |
| deux_rm_critair           | Deux roues, tricycles et quadricycles à moteur : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler. L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. EL correspond aux véhicules électriques et NC aux véhicules sans vignette.          | string       | Non                    | V4                                                                         |
| deux_rm_horaires          | Deux roues, tricycles et quadricycles à moteur : jours et horaires de restriction au format 'opening hours' d'OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours                                                                                                                                                                                                                  | string       | Non                    | <p>Mo-Fr 08:00-20:00; PH off,</p><p>24/7</p>                               |
| url_arrete                | Lien de l'arrêté administratif précisant la réglementation sur la zone ou sur le tronçon de route.                                                                                                                                                                                                                                                                                                   | string (uri) | Oui                    | https://cdn.paris.fr/paris/2021/05/28/23fb2b69cfa451a4e517f1bc6e3001b7.pdf |
| url_site_information      | Page web décrivant le dispositif et précisant la réglementation sur la zone ou sur le tronçon de route.                                                                                                                                                                                                                                                                                              | string (uri) | Non                    | https://www.metropolegrandparis.fr/fr/ZFE                                  |

## Publication des données

### Espace de publication

Les données devront être publiées sur data.gouv.fr. Pour ce faire deux méthodes sont possibles : 

* utiliser l'interface [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-zfe). Cela simplifie et accélère le processus de publication des données sur data.gouv.fr
* assurer que les données publiées sur le portail local sont bien moissonnées.

Dans tous les cas il sera nécessaire d'associer le mot-clef "zfe" au jeu de données pour qu'il puisse être intégré à la Base Nationale.

### Fichiers multiples

Comme présenté ici, une ZFE peut être décrite par un fichier décrivant les aires et un fichier décrivant les tronçons routiers spéciaux. Idéalement ces deux ressources devraient être publiées dans un même jeu de données sur data.gouv.fr. Cependant il est possible qu'il soit complexe pour certains producteurs (notamment utilisateurs de la solution OpenDataSoft) de rassembler des géométries de nature différente. C'est pourquoi il est autorisé de publier les deux fichiers (aires et tronçons) dans deux jeux de données différents. 

### Consolidation et Base Nationale

Les données publiées localement seront consolidées et regroupées dans une Base Nationale publiées sur data.gouv.fr et référencées sur transport.data.gouv.fr. Cette base sera composée de deux fichiers de données : un fichier des aires réglementées et un fichier des tronçons routiers spéciaux. 



