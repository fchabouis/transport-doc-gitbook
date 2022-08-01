# Lieux de covoiturage

La [base nationale des lieux de covoiturage](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/) (BNLC) recense les points de rencontre où les conducteurs peuvent déposer et prendre en charge des passagers en toute sécurité. Il est sous format .csv encodé en UTF8.\
Ce format a été défini en concertation avec Etalab, Open Data France, la ville de Paris et l'Agence d'aménagement et d'urbanisme de Corse. Le [schéma national des lieux de covoiturage](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/) a été publié par Etalab. Le schéma et la [BNLC](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/) sont maintenus par l'équipe de transport.data.gouv.fr.&#x20;

Ce jeu de données est sous licence ODbL : [https://doc.transport.data.gouv.fr/reutilisateurs/licence-odbl-et-conditions-de-reutilisation](https://doc.transport.data.gouv.fr/reutilisateurs/licence-odbl-et-conditions-de-reutilisation). Il est ainsi ouvert et accessible à tous.

\
Les contributeurs, peuvent transmettre directement les données relatives aux lieux qu’elles considèrent pertinents pour les covoitureurs en nous écrivant à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr) ou en utilisant l'outil d'aide à la contribution : [https://contribuer.transport.data.gouv.fr/](https://contribuer.transport.data.gouv.fr/)

\
La première base a été publiée en septembre 2019. Elle rassemblait les données publiées par [Blablacar ](https://transport.data.gouv.fr/datasets/aires-de-covoiturage-en-france/)et la [Fabrique des Mobilités](https://transport.data.gouv.fr/datasets/aires-de-covoiturage-base-de-donnees-commune-des-lieux-et/). Plusieurs départements, covoitureurs et entreprises comme [Vinci Autoroute](https://doc.transport.data.gouv.fr/notre-ecosysteme/les-facilitateurs) ou [Rézo Pouce](https://doc.transport.data.gouv.fr/notre-ecosysteme/les-facilitateurs) ont contribué à la BNLC depuis sa création.&#x20;



Cette documentation a pour objectif de définir plus précisément les valeurs autorisés de certains champs du schéma, sous la demande de producteurs et réutilisateurs.

{% hint style="info" %}
Cette documentation est amenée à évoluer avec l'intégration des définitions de nouvelles valeurs. N'hésitez pas à nous contacter à l'adresse  [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr) si vous souhaitez contribuer à ce glossaire.
{% endhint %}

### Correspondance avec OpenStreetMap

{% hint style="info" %}
Les données de covoiturage ont le tag[ amenity=car\_pooling ](https://wiki.openstreetmap.org/wiki/FR:Tag:amenity%3Dcar\_pooling)sur OpenStreetMap.
{% endhint %}

On retrouve certains champs du [schéma national des lieux de covoiturage](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/) dans le tag [ amenity=car\_pooling ](https://wiki.openstreetmap.org/wiki/FR:Tag:amenity%3Dcar\_pooling)sur OpenStreetMap (OSM). Ces champs n'ont toutefois pas le même nom. Ce tag OSM est utilisé pour représenter les stations ou lieux de covoiturage où on peut monter ou descendre de la voiture de quelqu'un ou pour aller chercher ou déposer quelqu'un.

Vous trouverez les champs qu'on retrouve à la fois dans le schéma national et sur OpenStreetMap ici :&#x20;

#### [nom\_lieu](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html#propriete-nom-lieu)

_Dans OpenStreetMap, les noms des lieux de covoiturage sont généralement décrits au moyen du tag :  (_[name](https://wiki.openstreetmap.org/wiki/FR:Key:name)=\*_)_

#### [nbre\_pl](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html#propriete-nbre-pl)

_Dans OpenStreetMap, le nombre de places réservées au stationnement disponibles est décrit au moyen du tag :  (_[capacity](https://wiki.openstreetmap.org/wiki/FR:Key:capacity)=number)

#### [duree](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html#propriete-duree)

_Dans OpenStreetMap, la durée maximale de stationnement autorisée est décrite au moyen du tag :  (_[maxstay](https://wiki.openstreetmap.org/wiki/FR:Key:maxstay)=\*)

[**proprio**](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html#propriete-proprio)****

_Dans OpenStreetMap, l'entité publique ou privée propriétaire des infrastructures_ **** _est décrite au moyen du tag :  (_[operator](https://wiki.openstreetmap.org/wiki/FR:Key:operator)=\*)

### Définitions des valeurs du champ ["type" ](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.2/documentation.html#propriete-type)

Le champ `type` permet de définir le lieu de covoiturage grâce à plusieurs valeurs :&#x20;

*   `Aire de covoiturage` qui correspond à un lieu signalisé par un panneau CE52, fléché, portant un nom et géographiquement délimité où :

    \- les conducteurs et les passagers se retrouvent, ou se trouvent, au début d’un trajet covoituré, ou

    \- le conducteur et ses passagers se séparent à la fin d’un trajet covoituré.\
    Les passagers peuvent y stationner leurs véhicules avant de prendre la route ensemble. &#x20;

    Plus d'informations[ ici](https://wiki.lafabriquedesmobilites.fr/wiki/D%C3%A9finition\_d'une\_aire\_de\_Covoiturage)&#x20;

{% hint style="info" %}
Panneau de type CE52 \
![](<../../.gitbook/assets/image (169) (1) (1) (1).png>)
{% endhint %}

* `Sortie d'autoroute` qui correspond aux plateformes et voies proches des péages d’entrée et de sortie d’autoroute
* `Parking` qui désigne un parc de stationnement
* `Supermarché` qui correspond à des places sur un parking de supermarché
* `Parking relais` qui correspond aux parkings aménagés près de transports publics et signalés par un panneau ID1b&#x20;

{% hint style="info" %}
Panneau de type ID1b\
![](<../../.gitbook/assets/image (168) (1).png>)
{% endhint %}

* `Délaissé routier` qui correspond à des parcelles qui faisaient partie du domaine public routier et qui ont été déclassées. Il peut s'agir de rue, voies ou impasses qui ne sont plus utilisées pour la circulation et qui peuvent être utilisées comme lieu de rencontre pour les covoitureurs
* `Auto-stop` qui correspond à des arrêts matérialisés et sécurisés permettant à une personne d'arrêter des automobilistes pour leur demander de les transporter gratuitement.&#x20;







Source :&#x20;

[Site de Vinci Autoroute ](https://www.vinci-autoroutes.com/fr/conseils/ecomobilite/covoiturage/)

[Wiki de la Fabrique des mobilités ](https://wiki.lafabriquedesmobilites.fr/wiki/D%C3%A9finition\_d'une\_aire\_de\_Covoiturage)
