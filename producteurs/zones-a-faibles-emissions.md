# Zones à Faibles Emissions

Transport.data.gouv.fr propose [un schéma de données pour favoriser la diffusion de l'information concernant les Zones à Faibles Emissions](https://schema.data.gouv.fr/etalab/schema-zfe/) en France par leur intégration dans les applications de mobilité.&#x20;

## Documentation

### Fonctionnement du modèle de données

Les données concernant les Zones à Faibles Emissions repose sur deux fichiers au format GeoJSON.&#x20;

* Le premier jeu de données précise les règles sur des _aires_ de la ZFE d'un territoire
* Un second jeu de données précise les règles particulières et les exceptions sur certains _tronçons routiers_.&#x20;

Les mêmes informations sont attendues sur les deux fichiers, néanmoins la modélisation géographique est différente : Polygone ou Multi-Polygone pour les _aires_ et Linestring et MultiLinestring pour les _tronçons routiers_.



### Représentation géographique

#### Aires couvertes par une Zone à Faibles Emissions

Les arrêtés mettant en place des Zones à Faibles Emissions précisent des aires administratives sur lesquelles s'appliquent une réglementation spécifique. Les géométries des aires couvertes correspondent donc généralement à des zones administratives : communes ou EPCI.

Ces géométries prennent pour référentiel le Référentiel Grande Echelle de l'IGN. AdminExpress peut être utilisé pour sélectionner les géométries de ces zones.&#x20;

Les géométries utilisent le système de projection WGS84.&#x20;

Si des zones spécifiques sont précisées par un arrêtés (centre-ville, bois...) alors le producteur de données doit modéliser aussi précisément que possible la géométrie de la zone.

#### Voies exceptionnelles

Les arrêtés précisent également régulièrement des voies spéciales où les règles de la ZFE s'appliquent différemment.&#x20;

Les géométries de ces tronçons routiers prennent pour référentiel la couche TRONCON\_DE\_ROUTE de la BD Topo de l'IGN.

Les géométries utilisent le système de projection WGS84.

### Granularité

#### Aires couvertes par une Zone à Faibles Emissions

Pour les aires, chaque ligne ou objet correspond à :

* une aire géographique
* décrite par un arrêté
* où la réglementation est homogène (hormis axes exceptionnels)

Aussi :

* si sur une même commune où un arrêté précise des réglementations différentes sur plusieurs zones on utilise plusieurs lignes/objets pour décrire la ZFE
* si les règles sont homogènes sur tout un EPCI mais que les arrêtés sont limités à chaque commune, on utilise autant de lignes/objets pour décrire chaque commune.&#x20;
* si les règles sont différentes pour les personnes morales et les personnes physiques on décrit la réglementation dans deux lignes/objets différentes.

#### Voies exceptionnelles

La granularité des voies exceptionnelles est la même que les tronçons routiers de la BD Topo de l'IGN. [La documentation de la BD Topo ](https://geoservices.ign.fr/ressources\_documentaires/Espace\_documentaire/BASES\_VECTORIELLES/BDTOPO/DC\_BDTOPO\_3-0.pdf)précise qu'un tronçon de routes est une _portion de voie de communication destinée aux automobiles, aux piétons, aux cycles ou aux animaux, homogène pour l'ensemble des attributs et des relations qui la concernent_.

Le découpage d'une voie en tronçon est précisé dans la documentation de la BD Topo.

### Attributs

Les aires réglementées et les voies exceptionnelles sont décrits par les mêmes attributs. Ces attributs sont essentiellement des éléments structurés extraits de la réglementation (véhicules dont la circulation est interdite, horaires d'application...).

<table data-header-hidden><thead><tr><th width="150">Attribut</th><th width="258">Description</th><th width="150">Format</th><th width="150">Oblig
atoire</th><th>Exemple</th></tr></thead><tbody><tr><td>Attribut</td><td>Description</td><td>Format</td><td>Obligatoire</td><td>Exemple</td></tr><tr><td>id</td><td><p><strong>Si l'objet est une aire règlementée :</strong> </p><p>Identifiant unique de l'aire réglementée (il y a donc autant d'identifiants que d'aires réglementées dans la ZFE)</p><p>Pour construire l'identifiant on utilise cette formule : <code>'Code SIREN de l'entité administrative englobant la zone' - ZFE - XXX</code> </p><p><em>NB : généralement, XXX reprend une numérotation incrémentale 001, 002, 003 etc.</em> </p><p></p><p><strong>Si l'objet est une voie spéciale :</strong> </p><p>Identifiant unique cleabs du tronçon routier issu de la couche <code>TRONCON_DE_ROUTE</code> de la BD Topo produite par l'IGN</p></td><td>string</td><td>Oui</td><td><em><strong>Identifiants d'aires :</strong>  200046977-ZFE-001, 200046977-ZFE-002, 200046977-ZFE-003</em><br><br><em><strong>Identifiant d'un tronçon :</strong> TRONROUT0000002003832789</em></td></tr><tr><td>date_debut</td><td>Date d'entrée en vigueur de la réglementation au format AAAA-MM-JJ.</td><td>string</td><td>Oui</td><td>2019-07-01</td></tr><tr><td>date_fin</td><td>Date de fin de la réglementation</td><td>string</td><td>Non</td><td>2023-07-01</td></tr><tr><td>vp_critair</td><td><strong>Véhicules particuliers :</strong> Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler. <br><br>L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. <br><br><em>EL correspond aux véhicules électriques et NC aux véhicules sans vignette.</em></td><td>string</td><td>Non</td><td>V4</td></tr><tr><td>vp_horaires</td><td><strong>Véhicules particuliers</strong> : jours et horaires de restriction au format <code>opening hours</code> d'OpenStreetMap : <a href="https://wiki.openstreetmap.org/wiki/Key:opening_hours">https://wiki.openstreetmap.org/wiki/Key:opening_hours</a></td><td>string</td><td>Non</td><td>Mo-Fr 08:00-20:00; PH off, <br>24/7</td></tr><tr><td>vul_critair</td><td><strong>Véhicules utilitaires légers</strong> : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. <br><em>Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler.</em> <br><br>L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. <br><br>EL correspond aux véhicules électriques et NC aux véhicules sans vignette.</td><td>string</td><td>Non</td><td>V4</td></tr><tr><td>vul_horaires</td><td><strong>Véhicules utilitaires légers :</strong> jours et horaires de restriction au format <code>opening hours</code> d'OpenStreetMap : <a href="https://wiki.openstreetmap.org/wiki/Key:opening_hours">https://wiki.openstreetmap.org/wiki/Key:opening_hours</a></td><td>string</td><td>Non</td><td>Mo-Fr 08:00-20:00; PH off, <br>24/7</td></tr><tr><td>pl_critair</td><td><strong>Poids lourds</strong> : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. <br><em>Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler.</em> <br><br>L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. <br><br>EL correspond aux véhicules électriques et NC aux véhicules sans vignette.</td><td>string</td><td>Non</td><td>V4</td></tr><tr><td>pl_horaires</td><td><strong>Poids lourds</strong> : jours et horaires de restriction au format <code>opening hours</code> d'OpenStreetMap : <a href="https://wiki.openstreetmap.org/wiki/Key:opening_hours">https://wiki.openstreetmap.org/wiki/Key:opening_hours</a></td><td>string</td><td>Non</td><td><p>Mo-Fr 08:00-20:00; PH off,</p><p>24/7</p></td></tr><tr><td>autobus_autocars_critair</td><td><strong>Autobus et autocars :</strong> Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. <br><em>Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler.</em> <br><br>L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. <br><br>EL correspond aux véhicules électriques et NC aux véhicules sans vignette.</td><td>string</td><td>Non</td><td>V4</td></tr><tr><td>autobus_autocars_horaires</td><td><strong>Autobus et autocars</strong> : jours et horaires de restriction au format <code>opening hours</code> d'OpenStreetMap : <a href="https://wiki.openstreetmap.org/wiki/Key:opening_hours">https://wiki.openstreetmap.org/wiki/Key:opening_hours</a></td><td>string</td><td>Non</td><td><p>Mo-Fr 08:00-20:00; PH off,</p><p>24/7</p></td></tr><tr><td>deux_rm_critair</td><td><strong>Deux roues, tricycles et quadricycles à moteu</strong>r : Vignette CRITAIR à partir de laquelle la circulation n'est pas autorisée. <br><em>Par exemple V4 signifie que les véhicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autorisés à circuler.</em> <br><br>L'ordre des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. <br><br>EL correspond aux véhicules électriques et NC aux véhicules sans vignette.</td><td>string</td><td>Non</td><td>V4</td></tr><tr><td>deux_rm_horaires</td><td><strong>Deux roues, tricycles et quadricycles à moteur</strong> : jours et horaires de restriction au format <code>opening hours</code> d'OpenStreetMap : <a href="https://wiki.openstreetmap.org/wiki/Key:opening_hours">https://wiki.openstreetmap.org/wiki/Key:opening_hours</a></td><td>string</td><td>Non</td><td><p>Mo-Fr 08:00-20:00; PH off,</p><p>24/7</p></td></tr><tr><td>url_arrete</td><td>Lien de l'arrêté administratif précisant la réglementation sur la zone ou sur le tronçon de route.</td><td>string (uri)</td><td>Non</td><td>https://cdn.paris.fr/paris/2021/05/28/23fb2b69cfa451a4e517f1bc6e3001b7.pdf</td></tr><tr><td>url_site_information</td><td>Page web décrivant le dispositif et précisant la réglementation sur la zone ou sur le tronçon de route.</td><td>string (uri)</td><td>Non</td><td>https://www.metropolegrandparis.fr/fr/ZFE</td></tr></tbody></table>

## Publication des données

### Espace de publication

Les données devront être publiées sur data.gouv.fr. Pour ce faire deux méthodes sont possibles :&#x20;

* utiliser l'interface [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-zfe). Cela simplifie et accélère le processus de publication des données sur data.gouv.fr
* assurer que les données publiées sur le portail local sont bien moissonnées.

Dans tous les cas il sera nécessaire d'associer le mot-clef "zfe" au jeu de données pour qu'il puisse être intégré à la Base Nationale.

### **Qualité des données**&#x20;

Avant de publier les données, nous recommandons aux producteurs d'évaluer la qualité de leurs ressources en utilisant le validateur de fichier disponible dans l'onglet "Outils" > "Evaluer la qualité d'un fichier"> "Zone à Faibles Emissions" de la page d'accueil de transport.data.gouv.fr : [https://transport.data.gouv.fr/validation?type=etalab%2Fschema-zfe](https://transport.data.gouv.fr/validation?type=etalab%2Fschema-zfe)\
\
![](<../.gitbook/assets/image (174) (1).png>)

### Fichiers multiples

Comme présenté ici, une ZFE peut être décrite par un fichier décrivant les aires et un fichier décrivant les tronçons routiers spéciaux. Idéalement ces deux ressources devraient être publiées dans un même jeu de données sur data.gouv.fr. Cependant il est possible qu'il soit complexe pour certains producteurs (notamment utilisateurs de la solution OpenDataSoft) de rassembler des géométries de nature différente. C'est pourquoi il est autorisé de publier les deux fichiers (aires et tronçons) dans deux jeux de données différents.&#x20;

### Consolidation et Base Nationale

Les données publiées localement seront consolidées et regroupées dans une Base Nationale publiées sur data.gouv.fr et référencées sur transport.data.gouv.fr. Cette base sera composée de deux fichiers de données : un fichier des aires réglementées et un fichier des tronçons routiers spéciaux.&#x20;



