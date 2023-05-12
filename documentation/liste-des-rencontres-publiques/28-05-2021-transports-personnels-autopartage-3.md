# 28/05/2021 - Transports personnels, Autopartage #3

### Participants

Thibaut Barrère (transport.data.gouv.fr), Miryad Ali (transport.data.gouv.fr), Nicolas Frasie (Communauto, Association des Acteurs de l'Autopartage), Heidi Guenin (MobilityData), Josée Sabourin (MobilityData), Tu-Tho Thai (MobilityData), Pierre Trouvé (Ubeeqo), Pierrick Paul (Fluctuo), David Stoltz (Keolis Dijon Mobilités).&#x20;

Cet atelier a été coanimé avec [l’Association des Acteurs de l’Autopartage](https://asso-autopartage.fr/about.html) (AAA). [MobilityData](https://mobilitydata.org/) a encadré les échanges concernant les spécificités du GBFS.  Nous collaborons avec ces deux associations afin d’établir une extension du format GBFS qui sera adapté aux données d’autopartage.&#x20;

Vous trouverez le support de présentation[ ici ](https://docs.google.com/presentation/d/1F5r\_HDcXEwysGFC6t-Voc0psk\_OkGNUrdRfWJd4jmws/edit#slide=id.g921c24f674\_0\_234)\
L'extension GBFS, non finalisée, [ici](https://docs.google.com/document/d/1bgNsiTcTfjKxG6khGq0ro0x-vEaToihp0\_t-krGyj1o/edit?ts=606c5d87)

{% hint style="info" %}
#### Cet atelier était le dernier atelier animé par l'équipe du Point d'Accès National et l'AAA concernant l'extension GBFS pour l'autopartage
{% endhint %}

####

### 1. Objectif de l'atelier&#x20;

L'objectif de cet atelier était de présenter les modifications apportées à la version bêta de l'extension GBFS grâce aux :\
\- retours qui nous ont été fait lors du dernier atelier en novembre 2020\
\- avis des potentiels réutilisateurs sur des sujets comme la définition du modèle de véhicule \
\- conseils de MobilityData pour rendre cette extension plus "internationale" et moins spécifique au cas français.&#x20;

### 2. Présentation des modifications apportées à l'extension par fichier &#x20;

**vehicle\_types**&#x20;

Le champ `car_type` a été supprimé et remplacé par `rider _ capacity` qui renvoie au nombre de places assises et `min_cargo_capacity` qui renseigne sur la capacité minimale, en litre, du coffre du véhicule. Le champ `car_type` a été supprimé car il n'y avait pas de nomenclature commune et facilement compréhensible pour les réutilisateurs. Ces derniers ont été consultés et ont jugé les deux nouveaux champs plus pertinents pour définir le type de véhicule.

Le champ `crit_air_label`, typique à la France, a été remplacé par `eco _ sticker`. Toutes les vignettes permettant de classer les véhicules en fonction de leurs émissions polluantes peuvent ainsi être renseignées, peu importe le pays. Le champ est passé d'une énumération à un tableau (JSON) pour pouvoir mettre des correspondances entre les vignettes de plusieurs pays. Pour un véhicule qui peut passer de la France à l'Espagne, par exemple, l'opérateur pourra renseigner à la fois la vignette du véhicule en France et celle en Espagne. La liste de valeurs proposées dans ce champ est seulement indicative.&#x20;

le champ `vehicle_description` avec comme informations attendues : le constructeur et le modèle du véhicule a été supprimé car les valeurs ne pouvaient être harmonisées. Un opérateur pourrait écrire, par exemple, "Toyota" comme "toyota"  ou "TOYOTA".&#x20;

Le champ `vehicle _ desc` a été conservé et seuls 50 caractères sont autorisés.&#x20;

La description du champ `vehicle _ accessories` a été modifiée afin de faciliter la compréhension des informations attendues. Ce sont les fonctionnalités fournies par le constructeur automobile qui doivent être indiquées ici.&#x20;

la description du champ `vehicle _ image` a été modifiée pour préciser les formats autorisées, à savoir le JPEG, JPG et PNG.

le champ `wheelchair_places` a été supprimé car il est encore complexe de définir l'accessibilité au véhicule de manière homogénéiser. Par exemple, faut il définir le nombre de places accessibles aux personnes en chaise roulante dans le véhicule et/ou préciser si la personne peut accéder seule au véhicule etc. ?&#x20;

le champ `b _ license  _ required` a été supprimé car il ne permettait pas de représenter les différents cas de figure de manière harmonisée comme les voitures pouvant être réservées sans permis, celles qui sont accessibles à partir d'une certaine ancienneté de permis etc.

**station\_information**

toutes les mentions de `car sharing` dans le champ `share _ type` ont été supprimées afin de généraliser ce champ à d'autres types de véhicules. Ainsi, `one way carsharing` est devenu `one way`.\
Ce champ sera probablement déplacé vers un autre fichier. MobilityData travailler sur ce sujet et nous attendons leurs retours avant de publier cette extension sur le Github de transport.data.gouv.fr et sur [schema.data.gouv.fr.](https://schema.data.gouv.fr/)&#x20;

le champ `disable _ person _ access` a été supprimé car il est encore complexe de définir l'accessibilité d'une station pour une personne à mobilité réduite. \
Ce champ sera toutefois intégré plus tard.

le champ `station_desc` ne peut contenir que 50 caractères

la description du champ `contact _ phone` a été complétée pour préciser que le numéro de téléphone doit être fourni au format  E.164.&#x20;

**free \_ vehicle \_ status**

Le nom du fichier a été modifié passant de `free  bike  status`_à  \` free  \_vehicle_ \_ status pour généraliser l'usage de cette extension à d'autres types de véhicules.&#x20;

La description du champ `vehicle _ accessories` a été modifiée afin de faciliter la compréhension des informations attendues. Ce sont les accessoires fournies par l'opérateur qui doivent être indiquées ici. La valeur "navigation" (GPS) a été ajoutée.

toutes les mentions de `car sharing` dans le champ `share _ type` ont été supprimées afin de généraliser ce champ à d'autres types de véhicules. Ainsi, `one way carsharing` est devenu `one way`.\
Ce champ sera probablement déplacé vers un autre fichier. MobilityData travailler sur ce sujet et nous attendons leurs retours avant de publier cette extension sur le Github de transport.data.gouv.fr et sur [schema.data.gouv.fr.](https://schema.data.gouv.fr/)&#x20;

Le champ `max_timeavailability` est devenu `available _ until` afin de faciliter la compréhension des informations attendues, à savoir quand est ce que le véhicule doit être rendue. Cette information doit être renseignée au format ISO 8601 notation avec le fuseau horaires.&#x20;

### 3. Prochaines étapes&#x20;

{% hint style="info" %}
L'extension ne sera publiée que lorsque le champ "share  type" sera défini par MobilityData".\
Les prochaines étapes ne seront donc pas datées car nous n'avons pas de date précise concernant l'intégration du "share \_ type" dans le GBFS par MobilityData.&#x20;
{% endhint %}

La prochaine étape est de préciser la méthode de calcul utiliser pour définir l'émission de C02/km&#x20;

Nous publierons ensuite cette extension sur le github de transport.data.gouv.fr et sur [schema.data.gouv.fr](https://schema.data.gouv.fr/).

Puis, nous allons proposer cette extension sur le [Github NABSA GBFS](https://github.com/NABSA/gbfs/blob/master/gbfs.md), qui est le Github dédié à l'évolution de ce format afin d'avoir des retours de la "communauté". \
**Si l'extension est validée par la communauté NABSA, cette extension sera considérée comme une évolution du format GBFS.**&#x20;

Enfin, nous définirons les modalités de transmission des données par les opérateurs vers le Point d'Accès National.&#x20;













