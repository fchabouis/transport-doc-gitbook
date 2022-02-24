# Qualité de données

## Pourquoi est-ce important ?

Pour maintenir une information voyageur de qualité, les réutilisateurs de données d’information voyageur ont besoin de sources fiables. Si les données ne sont pas de bonne qualité, l'information donnée à l'utilisateur ne sera pas bonne.

De plus, un jeu de données qui ne respecte pas les spécifications ne sera pas forcément complètement inutile, mais sa réutilisation sera conditionnée à un traitement manuel. Ce traitement manuel peut être plus ou moins compliqué et nécessiter que les réutilisateurs modifient les données, avec le risque de mal corriger ces erreurs.

Certains réutilisateurs ont mis en place des moyens plus ou moins automatiques pour corriger les données.

## Les validateurs

Toutes les données GTFS, GBFS ou basées sur un schéma élaboré par transport.data.gouv.fr et déposés sur la plateforme sont analysées. Un rapport de validation détaillant les erreurs que peuvent contenir les ressources est mis à disposition et est accessible en cliquant sur le nombre d'erreurs détectés.&#x20;

Ce rapport permet :

* aux réutilisateurs de connaître facilement le niveau de qualité du jeu de données ;
* aux producteurs d'avoir des pistes d'amélioration du jeu de données.

Exemple d'un rapport d'erreur d'un GTFS

![](<../.gitbook/assets/image (178).png>)

![](<../.gitbook/assets/image (171).png>)

Exemple d'un rapport d'erreur d'un GBFS

![](<../.gitbook/assets/image (177).png>)

![](<../.gitbook/assets/image (181).png>)

Exemple d'un rapport d'erreur d'une ressource associée à un schéma&#x20;

![](<../.gitbook/assets/image (169).png>)\
![](<../.gitbook/assets/image (170).png>)



Les producteurs et réutilisateurs ont également la possibilité de valider ces données avant qu'elles soient publiées à partir de l'onglet "Outils" de la plateforme [en téléchargeant le fichier](https://transport.data.gouv.fr/validation) et en sélectionnant le type de fichier à évaluer dans la liste déroulante&#x20;

![](<../.gitbook/assets/image (172).png>)

ou [en renseignant une URL gbfs.json](https://transport.data.gouv.fr/tools/gbfs/analyze).&#x20;

![](<../.gitbook/assets/image (180).png>)

### Le validateur GTFS

Les erreurs sont caractérisées suivant leur niveau d'importance :

* "**Échec irrécupérable**" : les données ne respectent pas la spécification [GTFS](https://gtfs.org/reference/static), les réutilisations automatiques de ces données vont être sérieusement compromises ;
* "**Erreur**" : les données contiennent des erreurs (coordonnées de stations non valides, identifiant manquants,...). La réutilisation de ces données risque d’être compliqué.
* "**Avertissement**" : Ce ne sont pas forcément des erreurs, mais plutôt des éléments qui méritent d'être analysés. Cela peut être des temps de trajet d'un bus nuls, des stations en doublons, des coordonnées manquantes, ...
* "**Information**" : de simples informations sur le jeu de données. Cela peut etre une vitesse de bus qui semble trop rapide, des stations inutilisées, ....

Pour faciliter la réutilisation des données, il est primordial de ne pas avoir ni “Échecs irrécupérables” ni “Erreurs”. Les “Avertissements” ne sont pas forcément rédhibitoires pour des données de bonne qualité, si leur nombre reste limité.

{% hint style="info" %}
Le code de ce validateur est [ouvert](https://github.com/etalab/transport-validator/), n’hésitez pas à demander des précisions ou à participer à l’ajout de nouvelles règles.
{% endhint %}

