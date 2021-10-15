# 28/08/2020 - Transports personnels, Autopartage #1

**Participants**\
****

Nicolas Frasie (Communauto et Association des Acteurs de l’Autopartage), Gilles Kister (Citiz), Josée Sabourin (Mobility Data), Julien de Labaca (Mobility Data), Fabien Serra (MyBus), Vincent Szaleniec (Île-de-France Mobilités), Mélanie Gidel (Mairie de Paris), Patrick Pigache, (Mairie de Paris), Antoine Sarazin (Instant System), Loïc Ciprian (Instant System), Christophe Le Guern (Mobility by Colas), Martin Rueda, Miryad (transport.data.gouv.fr), Jeanne (transport.data.gouv.fr), Antoine (transport.data.gouv.fr), Nicolas (transport.data.gouv.fr),\
****

Cet atelier a été coanimé avec [l’Association des Acteurs de l’Autopartage](https://asso-autopartage.fr/about.html) (AAA) et [MobilityData](https://mobilitydata.org).  Nous collaborons avec ces deux associations afin d’établir une extension du format GBFS qui sera adapté aux données d’autopartage. 

****

1. **Obligations réglementaires pour les producteurs de données : transport.data.gouv.fr**

Les données d’autopartage font partie des données de niveau 2 (modes à la demande et transports personnels). L’échéance d’ouverture est fixée au 1er décembre 2020. 

Les informations concernées sont les suivantes 

* localisation
* disponibilité des véhicules
* modalités d'achat des billets
* caractéristiques des véhicules

**2. Zoom sur le format GBFS : MobilityData**

* Historique

Le format été créé par l’association américaine [NABSA](https://nabsa.net) pour les données des vélos partagés. Ce format est utilisé par plus de 270 opérateurs dans le monde. NABSA a contractualisé avec MobilityData pour développer et enrichir le GBFS à l'échelle mondiale. 

Le [GBFS](https://github.com/NABSA/gbfs) est un agrégat de fichiers, très proche du GTFS. Il est toutefois plus restreint que le GTFS, avec moins d'extensions et de détails.  \


Historiquement, l'objectif du GBFS n'était pas de faire de la régulation mais de l'information voyageur en renseignant les informations suivantes : 

\* Localisation des stations ; 

\* Situation des stations (pleines ou vides) ;

\* Disponibilités des vélos en temps-réel. 

Ces données peuvent être réutilisées dans des applications servant à l’information voyageur comme Lime ou GoogleMaps \


* Dernières évolutions 

Le processus de gouvernance pour le GTFS est basé sur l’itération continuelle de ce format de données afin de l’adapter aux besoins des usagers. Ces améliorations du format de données sont faites en collaboration avec les opérateurs de transport et les réutilisateurs. Pour cela, un [Github](https://github.com/NABSA/gbfs) ouvert à tous a été créé avec des : 

\* issues : pour poser des questions, relever des problèmes remarqués sur le schéma proposé etc. ; 

\* [pull requests ](https://github.com/NABSA/gbfs/pull/255): pour faire des suggestions de modification ;

Un processus de vote a également été mis en place avec 7 jours de vote afin de savoir si le schéma de données proposé est adopté ou non. 1 vote « non » met le vote en échec. La proposition est alors abandonnée ou revisitée. 

La [version 2.0](https://medium.com/@mobilitydata/du-nouveau-pour-la-version-2-0-de-gbfs-2b9996247085) est la dernière en date. Les versions GBFS 2.1 et 3.0 sont à venir avec de nouvelles fonctionnalités.\


* GBFS adapté à l'autopartage

Ce format est une bonne base pour l'autopartage : 

\* Il peut être utilisé sans station ou avec station

\* Il donne des détails sur des stations et des véhicules individuels

\* Il est intrinsèquement itératif 

\* Il renseigne des données en temps réel

Issue Github sur l'autopartage : [https://github.com/NABSA/gbfs/pull/255](https://github.com/NABSA/gbfs/pull/255)****\
****\
****

**Présentation de la version alpha du schéma de données : l’extension GBFS autopartage : AAA**

Nous nous sommes basés sur trois types d’autopartage afin d’établir ce schéma de données (issue Github : https://github.com/NABSA/gbfs/pull/255) : 

* L’Autopartage en boucle 

Une disponibilité actuelle n’a que peu de sens car les réservations se font dans le futur. Les véhicules affichés seront disponible entre maintenant et dans  3h, indifféremment de leur disponibilité future. 

* Autopartage en free-floating

Il existe des services d’autopartage en free-floating où les véhicules peuvent être emprunté ou déposé dans une ou plusieurs zones mais également dans des stations, qui offrent un nombre limité de places disponibles (exactement comme des stations de vélo en libre-service).

* Autopartage en trace direct (ou \*one-way\*)

L’autopartage en trace directe (Autolib, Bluely, Bluecub) est une exception française. Les véhicules peuvent être uniquement déposés dans des stations. L’AAA s’interroge sur la pertinence de modéliser ce type d’autopartage.\


* Retour sur les champs modifiés, rajouter dans le schéma adapté à l’autopartage et propositions d’améliorations 

vehicule_types : Décrit les différents types de véhicule proposés par le service d’autopartage 

* Car_type

Permet de préciser le type de véhicule (2 places, 4 places, …). Les valeurs proposées doivent être précisées.

* Seating_capacity
* Share_type

Puisqu’un même service d’autopartage peut inclure plusieurs types de service, il nous semble utile d’ajouter ce champ. Toutefois, ces différents types ont généralement un logo et un nom différent pour un même opérateur dans une même ville (exemple Yea ! et Citiz pour Citiz), ce qui pose la question de remonter ce champ dans system_information et dédoubler le lot de fichiers. Nous sommes intéressés d’avoir l’avis des réutilisateurs sur ce point.

* Min_fuel_level

Si le véhicule est à essence, un niveau minimum de carburant peut être demandé à la fin du trajet. Cette information peut également être remontée au system_information.

* Propulsion_type  

Complexifier un peu les valeurs pour la question de l'accès au centre-ville. Question ouverte sur la possibilité de spécifier la vignette Crit'Air qui permettrait de savoir si le véhicule peut être utilisé ou non dans certaines zones (ZFE ou pic de pollution...). 

Débat entre les participants : 

Crit'Air serait limitatif car ne concerne que la France : MobilityData est plutôt contre l'introduction de cette information trop spécifique à la zone France. 

Normes euro se cantonne à l'Union européenne mais est déjà plus inclusive comme norme que Crit'Air\*\*. Possibilité d’indiquer cette donnée en se basant sur les émissions de CO2, en faisant des tranches ? L'émission de CO2 es intéressante comme critère de choix pour les utilisateurs. Cela supposerait toutefois que l'utilisateur reconstitue l'information après. 

* user_age_condition : 

Permet de renseigner certains véhicules qui sont accessibles avant 18 ans (ex. des quadricycle à moteur type Peugeot AMIOne)

* vehicule_desc 

Donne des informations diverses propre à ce type de véhicule. Ce champ libre est libre et peut donc être personnalisé selon les usagers.  

Débat entre les participants : 

Il est demandé de prévoir une traduction en anglais. Nativement dans le GBFS, la langue des commentaires est unique pour un lot de fichiers, et indiqué dans le fichier gbfs.json.

* vehicule_accessories 

Permet d’indiquer quels sont les accessoires qui sont (ou peuvent être) fournis avec le véhicule (pneus neige, siège bébé etc.). Ces accessoires doivent être visibles dans l'application de réservation. 

* vehicle_image 

Permet d’insérer une ou plusieurs photos des véhicules. 

* is_wheelchairaccessible 

Permet de préciser si le véhiculeest accessible aux personnes en fauteuil roulant. \


free_bike_status : 

*  vehicle_plate 

Permet de saisir la plaque d'immatriculation

Débat ouvert : Ce champ permet de reconstituer les trajets du véhicule, et serait susceptible de poser un risque d’atteintes à la vie privée. Il est maintenu en option à ce stade. 

* public_id :

Permet aux utilisateurs d’identifier le véhicule. 

Débat ouvert :

Il est préférable de renseigner la plaque d'immatriculation ou plutôt le numéro d'identification public ? 

Débat ouvert : Ce champ permet de reconstituer les trajets du véhicule, et serait susceptible de poser un risque d’atteintes à la vie privée.  Il est maintenu en option à ce stade. 

* current_range\_% : 

Permet d’indiquer non pas l’autonomie mais le pourcentage de remplissage de la batterie en pourcentage. L’information « range » en km du véhicule n’est pas forcément disponible pour les opérateurs d’autopartage. Pour éviter de données une estimation qui ne soit pas cohérente avec celle affichée par le véhicule en début de trajet, les opérateurs préfèrent parfois communiqués un % de charge de la batterie. Dans certains cas, les opérateurs préfèrent ne pas indiquer l’autonomie.

Ce champ risque toutefois de devenir illisible pour l’utilisateur s’il y a différents modèles. \


station_information

* parking_hoop 

Permet de signaler que la place est strictement réservée. 

Le champ a finalement été intégré dans station_type.

* station_type 

Type de station (en voirie, en sous-sol…).

* Share_type

Type d’autopartage que peut accueillir la station. En effet, il existe des services d’autopartage en free-floating où les véhicules peuvent être emprunté ou déposé dans une ou plusieurs zones mais également dans des stations, qui offrent un nombre limité de places disponibles (exactement comme des stations de vélo en libre-service).\


* charging_capacity 

Permet de préciser la présence de points de recharge pour véhicule électrique.

* step_free_access : 

Permet d’indiquer si la station est accessible aux personnes à mobilité réduite. 

* night_light 

Permet de signaler si la station est éclairée la nuit ou non. 

* station_desc 

Pour les stations hors voiries (par exemple louées chez ZenPark),il y a besoin d'un champ libre textuel (potentiellement limité) pour indiquer à une personne que la place est au -6 entre la place 204 et 200 avec le digicode XXXX.

Débat 

Potentiellement plusieurs champs pourraient être utilisés. Attention : on parle ici de données qui seront publiques ; ne pas indiquer le code d’un digicode par exemple. Attention aussi à l'internationalisation des champs libres.

Proposition : Ajout d’un champ pedestrian_access 

* station_hours 

Permet d’indiquer les horaires d'ouverture de la station. Habituellement, ouverture 24/7, mais il peut y avoir des exceptions. 

Débat : Ce champ a été envisagé pour la location de voiture, avec l’intervention d’un agent. Il est proposé de supprimer ce champ. 

 Journée, heure de début, heure de fin 

* Proposition : Ajout d'un champ de contact de la station 

station_status 

Modifications similaires à free_bike_status.\


**3. Retours des participants **

* Le GBFS va être un modèle de données assez complet : toutes ces données doivent-elles être remplies par tous les acteurs ? 

Oui, certains champs seront obligatoires, d'autres optionnels. Les champs ne seront obligatoires que pour les données facilement mobilisables. \


* Lien entre les véhicules et les stations ? 

Pour certains systèmes on peut appeler un service pour avoir la liste des stations dans lesquelles il y a un type d’autopartage. Inversement on peut demander la liste des véhicules qui sont présents dans une station. \


* Quel temps de rafraîchissement de ces données sur le PAN ?

Le taux de rafraîchissement dépend du producteur car le PAN n'héberge par les données. \
****

**4. Publication des flux GBFS sur le PAN : transport.data.gouv.fr **

* Référencement de l'URL sur fichier gbfs.json sur data.gouv par le producteur, puis l'équipe de transport.data.gouv.fr référence l'URL sur le PAN. 
* Démonstration plus détaillée au prochain atelier

**5. Etapes à venir**

* Renvoi d’un lien Github vers le schéma avec les modifications intégrées pour que tout le monde puisse ajouter des commentaires, poser des questions etc. pendant un mois. 
* Nouvel atelier dans un mois pour approuver ou non le schéma proposé  

**Objectif d'un schéma de données final pour le mois d’octobre. **\
