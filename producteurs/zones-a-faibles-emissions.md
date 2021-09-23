# Zones à Faibles Emissions

transport.data.gouv.fr propose un schéma de données pour favoriser la diffusion de l'information concernant les Zones à Faibles Emissions en France par leur intégration dans les applications de mobilité. 

## Documentation

### Fonctionnement du modèle de données

Les données concernant les Zones à Faibles Emissions repose sur deux fichiers au format GeoJSON. 

* Le premier jeu de données précise les règles sur des _aires_ de la ZFE d'un territoire
* Un second jeu de données précise les règles particulières et les exceptions sur certains _tronçons routiers_. 

Les mêmes informations sont attendues sur les deux fichiers, néanmoins la modélisation géographique est différente : Polygone ou Multi-Polygone pour les _aires_ et Linestring et MultiLinestring pour les _tronçons routiers_.



### Représentation géographique

#### Aires couvertes par une Zone à Faibles Emissions

Les arrêtés mettant en place des Zones à Faibles Emissions précisent des aires administratives sur lesquelles s'appliquent une réglementation spécifique. Les géométries des aires couvertes correspondent donc généralement à des zones administratives : communes ou EPCI.

Ces géométries prennent pour référentiel le Référentiel Grande Echelle de l'IGN. AdminExpress peut être utilisé pour sélectionner les géométries de ces zones. 

Les géométries utilisent le système de projection WGS84. 

Si des zones spécifiques sont précisées par un arrêtés \(centre-ville, bois...\) alors le producteur de données doit modéliser aussi précisément que possible la géométrie de la zone.

#### Voies exceptionnelles

Les arrêtés précisent également régulièrement des voies spéciales où les règles de la ZFE s'appliquent différemment. 

Les géométries de ces tronçons routiers prennent pour référentiel la couche TRONCON\_DE\_ROUTE de la BD Topo de l'IGN.

Les géométries utilisent le système de projection WGS84.

### Granularité

#### Aires couvertes par une Zone à Faibles Emissions

Pour les aires, chaque ligne ou objet correspond à :

* une aire géographique
* décrite par un arrêté
* où la réglementation est homogène \(hormis axes exceptionnels\)

Aussi :

* si sur une même commune où un arrêté précise des réglementations différentes sur plusieurs zones on utilise plusieurs lignes/objets pour décrire la ZFE
* si les règles sont homogènes sur tout un EPCI mais que les arrêtés sont limités à chaque commune, on utilise autant de lignes/objets pour décrire chaque commune. 
* si les règles sont différentes pour les personnes morales et les personnes physiques on décrit la réglementation dans deux lignes/objets différentes.

#### Voies exceptionnelles

La granularité des voies exceptionnelles est la même que les tronçons routiers de la BD Topo de l'IGN. [La documentation de la BD Topo ](https://geoservices.ign.fr/ressources_documentaires/Espace_documentaire/BASES_VECTORIELLES/BDTOPO/DC_BDTOPO_3-0.pdf)précise qu'un tronçon de routes est une _portion de voie de communication destinée aux automobiles, aux piétons, aux cycles ou aux animaux, homogène pour l'ensemble des attributs et des relations qui la concernent_.

Le découpage d'une voie en tronçon est précisé dans la documentation de la BD Topo.

### Attributs

Les aires réglementées et les voies exceptionnelles sont décrits par les mêmes attributs. Ces attributs sont essentiellement des éléments structurés extraits de la réglementation \(véhicules dont la circulation est interdite, horaires d'application...\).

<table>
  <thead>
    <tr>
      <th style="text-align:left">Attribut</th>
      <th style="text-align:left">Description</th>
      <th style="text-align:left">Format</th>
      <th style="text-align:left">Oblig
        <br />atoire</th>
      <th style="text-align:left">Exemple</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">id</td>
      <td style="text-align:left">
        <p><em>Si l&apos;objet est une aire reglement&#xE9;e :</em> Identifiant unique
          de l&apos;aire r&#xE9;glement&#xE9;e. Pour construire l&apos;identifiant
          on utilise cette formule : &apos;Code SIREN de l&apos;entit&#xE9; administrative
          englobant la zone&apos; - ZFE - XXX.</p>
        <p><em>Si l&apos;objet est une voie sp&#xE9;ciale : </em>Identifiant unique
          cleabs du tron&#xE7;on routier issu de la couche TRONCON_DE_ROUTE de la
          BD Topo produite par l&apos;IGN&quot;</p>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Oui</td>
      <td style="text-align:left">200046977-ZFE-001,
        <br />TRONROUT0000002003832789</td>
    </tr>
    <tr>
      <td style="text-align:left">date_debut</td>
      <td style="text-align:left">Date d&apos;entr&#xE9;e en vigueur de la r&#xE9;glementation au format
        AAAA-MM-JJ.</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Oui</td>
      <td style="text-align:left">2019-07-01</td>
    </tr>
    <tr>
      <td style="text-align:left">date_fin</td>
      <td style="text-align:left">Date de fin de la r&#xE9;glementation</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Non</td>
      <td style="text-align:left">2023-07-01</td>
    </tr>
    <tr>
      <td style="text-align:left">vp_critair</td>
      <td style="text-align:left">V&#xE9;hicules particuliers : Vignette CRITAIR &#xE0; partir de laquelle
        la circulation n&apos;est pas autoris&#xE9;e. Par exemple V4 signifie que
        les v&#xE9;hicules CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autoris&#xE9;s
        &#xE0; circuler. L&apos;ordre des vignettes est le suivant : EL, V1, V2,
        V3, V4, V5, NC. EL correspond aux v&#xE9;hicules &#xE9;lectriques et NC
        aux v&#xE9;hicules sans vignette.</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Non</td>
      <td style="text-align:left">V4</td>
    </tr>
    <tr>
      <td style="text-align:left">vp_horaires</td>
      <td style="text-align:left">V&#xE9;hicules particuliers : jours et horaires de restriction au format
        &apos;opening hours&apos; d&apos;OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">Non</td>
        <td style="text-align:left">Mo-Fr 08:00-20:00; PH off,
          <br />24/7</td>
    </tr>
    <tr>
      <td style="text-align:left">vul_critair</td>
      <td style="text-align:left">V&#xE9;hicules utilitaires l&#xE9;gers : Vignette CRITAIR &#xE0; partir
        de laquelle la circulation n&apos;est pas autoris&#xE9;e. Par exemple V4
        signifie que les v&#xE9;hicules CRITAIR 4, CRITAIR 5 et sans vignettes
        ne sont pas autoris&#xE9;s &#xE0; circuler. L&apos;ordre des vignettes
        est le suivant : EL, V1, V2, V3, V4, V5, NC. EL correspond aux v&#xE9;hicules
        &#xE9;lectriques et NC aux v&#xE9;hicules sans vignette.</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Non</td>
      <td style="text-align:left">V4</td>
    </tr>
    <tr>
      <td style="text-align:left">vul_horaires</td>
      <td style="text-align:left">V&#xE9;hicules utilitaires l&#xE9;gers : jours et horaires de restriction
        au format &apos;opening hours&apos; d&apos;OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">Non</td>
        <td style="text-align:left">Mo-Fr 08:00-20:00; PH off,
          <br />24/7</td>
    </tr>
    <tr>
      <td style="text-align:left">pl_critair</td>
      <td style="text-align:left">Poids lourds : Vignette CRITAIR &#xE0; partir de laquelle la circulation
        n&apos;est pas autoris&#xE9;e. Par exemple V4 signifie que les v&#xE9;hicules
        CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autoris&#xE9;s &#xE0;
        circuler. L&apos;ordre des vignettes est le suivant : EL, V1, V2, V3, V4,
        V5, NC. EL correspond aux v&#xE9;hicules &#xE9;lectriques et NC aux v&#xE9;hicules
        sans vignette.</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Non</td>
      <td style="text-align:left">V4</td>
    </tr>
    <tr>
      <td style="text-align:left">pl_horaires</td>
      <td style="text-align:left">Poids lourds : jours et horaires de restriction au format &apos;opening
        hours&apos; d&apos;OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">Non</td>
        <td style="text-align:left">
          <p>Mo-Fr 08:00-20:00; PH off,</p>
          <p>24/7</p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">autobus_autocars_critair</td>
      <td style="text-align:left">Autobus et autocars : Vignette CRITAIR &#xE0; partir de laquelle la circulation
        n&apos;est pas autoris&#xE9;e. Par exemple V4 signifie que les v&#xE9;hicules
        CRITAIR 4, CRITAIR 5 et sans vignettes ne sont pas autoris&#xE9;s &#xE0;
        circuler. L&apos;ordre des vignettes est le suivant : EL, V1, V2, V3, V4,
        V5, NC. EL correspond aux v&#xE9;hicules &#xE9;lectriques et NC aux v&#xE9;hicules
        sans vignette.</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Non</td>
      <td style="text-align:left">V4</td>
    </tr>
    <tr>
      <td style="text-align:left">autobus_autocars_horaires</td>
      <td style="text-align:left">Autobus et autocars : jours et horaires de restriction au format &apos;opening
        hours&apos; d&apos;OpenStreetMap : https://wiki.openstreetmap.org/wiki/Key:opening_hours</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">Non</td>
        <td style="text-align:left">
          <p>Mo-Fr 08:00-20:00; PH off,</p>
          <p>24/7</p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">deux_rm_critair</td>
      <td style="text-align:left">Deux roues, tricycles et quadricycles &#xE0; moteur : Vignette CRITAIR
        &#xE0; partir de laquelle la circulation n&apos;est pas autoris&#xE9;e.
        Par exemple V4 signifie que les v&#xE9;hicules CRITAIR 4, CRITAIR 5 et
        sans vignettes ne sont pas autoris&#xE9;s &#xE0; circuler. L&apos;ordre
        des vignettes est le suivant : EL, V1, V2, V3, V4, V5, NC. EL correspond
        aux v&#xE9;hicules &#xE9;lectriques et NC aux v&#xE9;hicules sans vignette.</td>
      <td
      style="text-align:left">string</td>
        <td style="text-align:left">Non</td>
        <td style="text-align:left">V4</td>
    </tr>
    <tr>
      <td style="text-align:left">deux_rm_horaires</td>
      <td style="text-align:left">Deux roues, tricycles et quadricycles &#xE0; moteur : jours et horaires
        de restriction au format &apos;opening hours&apos; d&apos;OpenStreetMap
        : https://wiki.openstreetmap.org/wiki/Key:opening_hours</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">Non</td>
      <td style="text-align:left">
        <p>Mo-Fr 08:00-20:00; PH off,</p>
        <p>24/7</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">url_arrete</td>
      <td style="text-align:left">Lien de l&apos;arr&#xEA;t&#xE9; administratif pr&#xE9;cisant la r&#xE9;glementation
        sur la zone ou sur le tron&#xE7;on de route.</td>
      <td style="text-align:left">string (uri)</td>
      <td style="text-align:left">Oui</td>
      <td style="text-align:left">https://cdn.paris.fr/paris/2021/05/28/23fb2b69cfa451a4e517f1bc6e3001b7.pdf</td>
    </tr>
    <tr>
      <td style="text-align:left">url_site_information</td>
      <td style="text-align:left">Page web d&#xE9;crivant le dispositif et pr&#xE9;cisant la r&#xE9;glementation
        sur la zone ou sur le tron&#xE7;on de route.</td>
      <td style="text-align:left">string (uri)</td>
      <td style="text-align:left">Non</td>
      <td style="text-align:left">https://www.metropolegrandparis.fr/fr/ZFE</td>
    </tr>
  </tbody>
</table>

## Publication des données

### Espace de publication

Les données devront être publiées sur data.gouv.fr. Pour ce faire deux méthodes sont possibles : 

* utiliser l'interface [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-zfe). Cela simplifie et accélère le processus de publication des données sur data.gouv.fr
* assurer que les données publiées sur le portail local sont bien moissonnées.

Dans tous les cas il sera nécessaire d'associer le mot-clef "zfe" au jeu de données pour qu'il puisse être intégré à la Base Nationale.

### Fichiers multiples

Comme présenté ici, une ZFE peut être décrite par un fichier décrivant les aires et un fichier décrivant les tronçons routiers spéciaux. Idéalement ces deux ressources devraient être publiées dans un même jeu de données sur data.gouv.fr. Cependant il est possible qu'il soit complexe pour certains producteurs \(notamment utilisateurs de la solution OpenDataSoft\) de rassembler des géométries de nature différente. C'est pourquoi il est autorisé de publier les deux fichiers \(aires et tronçons\) dans deux jeux de données différents. 

### Consolidation et Base Nationale

Les données publiées localement seront consolidées et regroupées dans une Base Nationale publiées sur data.gouv.fr et référencées sur transport.data.gouv.fr. Cette base sera composée de deux fichiers de données : un fichier des aires réglementées et un fichier des tronçons routiers spéciaux. 





