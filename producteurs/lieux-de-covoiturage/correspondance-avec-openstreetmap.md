# Correspondance avec OpenStreetMap

Cette documentation a pour objectif de faire le lien entre les champs utilisés dans OpenStreetMap pour les données de covoiturage et le [schéma national des lieux de covoiturage](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html).

#### Correspondance entre OpenStreetMap et les champs du schéma

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

[**proprio**](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html#propriete-proprio)

_Dans OpenStreetMap, l'entité publique ou privée propriétaire des infrastructures_ _est décrite au moyen du tag :  (_[operator](https://wiki.openstreetmap.org/wiki/FR:Key:operator)=\*)
