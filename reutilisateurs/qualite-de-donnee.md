# Qualité de données

## Pourquoi est-ce important ?

Pour maintenir une information voyageur de qualité, les réutilisateurs de données d’information voyageur ont besoin de sources fiables. Si les données ne sont pas de bonne qualité, l'information donnée à l'utilisateur ne sera pas bonne.

De plus, un jeu de données qui ne respecte pas les spécifications ne sera pas forcément complètement inutile, mais sa réutilisation sera conditionnée à un traitement manuel. Ce traitement manuel peut être plus ou moins compliqué et nécessiter que les réutilisateurs modifient les données, avec le risque de mal corriger ces erreurs.

Cela étant dit, les données ne sont que très rarement parfaites, et certains réutilisateurs ont mis en place des moyens plus ou moins automatiques pour corriger les données.

## Validateur de fichiers GTFS

Tous les fichiers GTFS déposés sur la plateforme https://transport.data.gouv.fr sont analysés et un rapport de validation est mis à disposition.

Ce rapport permet :

* aux réutilisateurs de connaître facilement le niveau de qualité du jeu de données ;
* de proposer des pistes d'amélioration du jeu de données aux producteurs de données.

Les erreurs sont caractérisées suivant leur niveau d'importance :

* "**Échec irrécupérable**" : les données ne respectent pas la spécification [GTFS](https://gtfs.org/reference/static), les réutilisations automatiques de ces données vont être sérieusement compromises ;
* "**Erreur**" : les données contiennent des erreurs \(coordonnées de stations non valides, identifiant manquants,...\). La réutilisation de ces données risque d’être compliqué.
* "**Avertissement**" : Ce ne sont pas forcément des erreurs, mais plutôt des éléments qui méritent d'être analysés. Cela peut être des temps de trajet d'un bus nuls, des stations en doublons, des coordonnées manquantes, ...
* "**Information**" : de simples informations sur le jeu de données. Cela peut etre une vitesse de bus qui semble trop rapide, des stations inutilisées, ....

Pour faciliter la réutilisation des données, il est primordial de ne pas avoir ni “Échecs irrécupérables” ni “Erreurs”. Les “Avertissements” ne sont pas forcément rédhibitoires pour des données de bonne qualité, si leur nombre reste limité.

{% hint style="info" %}
Le code de ce validateur est [ouvert](https://github.com/etalab/transport-validator/), n’hésitez pas à demander des précisions ou à participer à l’ajout de nouvelles règles.
{% endhint %}



