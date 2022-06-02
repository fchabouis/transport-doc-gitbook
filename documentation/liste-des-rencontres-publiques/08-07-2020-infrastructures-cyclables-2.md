# 08/07/2020 - Infrastructures cyclables #2

**26 participants** dont 3 membres de [transport.data.gouv.fr](https://transport.data.gouv.fr/) Vélo & Territoires, Poitiers, Montpelliers, Pays-Basque, Touraine, Angers, Brest, Allons à Vélo Allons à Pied (AVAP), Grand Chambéry, région Hauts-de-France, région Bretagne, Communauté d'Agglomération Ventoux Comtat Venaissin, Ille-et-Vilaine, Communauté de communes Val d'Ille-Aubigné, Nantes métropole, Systra, OpenStreetMap (OSM), GéoVélo, MobilityData, Mon Univert, institut Paris région, l'association des citoyens du Seignanx

Cet OpenLab a été co-animé avec l’association Vélo & Territoires

## 1.     Présentation de transport.data.gouv.fr et rappel des obligations réglementaires

Présentation déroulée en séance disponible à [ce lien](https://docs.google.com/presentation/d/1q4WDQK3rIglwaeKZt4QhqJ1jJphfYZ5oEaqgKxwABjU/edit?usp=sharing).

Pour plus d’informations sur transport.data.gouv.fr, vous pouvez consulter [le guide publié ici](https://doc.transport.data.gouv.fr/).

Le règlement européen 2017/1926 impose une ouverture des données à jour, de qualité, aux normes pour tous les modes de transport. Trois catégories de modes de transport ont été identifiées :

\-          Services réguliers ;

\-          Services à la demande ;

\-          Modes personnels.

Les données d’aménagements cyclables font partie de la catégorie « modes personnels » et leur publication sur le PAN était initialement prévue en décembre 2019. Cependant, le standard de données n’a pas encore été décrété par la Direction générale européenne des mobilités et des transports (DG Move).

Un groupe de travail avait été identifié lors du premier OpenLab du 27 juin 2019 afin d’établir une proposition de schéma de publication et de standard pour les données relatives aux infrastructures cyclables. Nous avons repris l’investigation sur ces données en mars 2020 et nous nous sommes associés à Vélo & Territoires afin de continuer les travaux. Cette association avait déjà entamé des travaux de normalisation des données d’aménagements cyclables.



### **1.** **Présentation des résultats de l’enquête de Vélo & Territoires sur les données d’aménagements cyclables**

Vélo & Territoires est une association regroupant des collectivités engagées pour le développement et la promotion du vélo au niveau national et européen.

Pour plus d’informations sur Vélo & Territoires, vous pouvez consulter leur [page web](https://www.velo-territoires.org/)

L’association a mené une enquête auprès des collectivités afin de mieux comprendre leur situation, leurs pratiques quant aux données d’aménagements cyclables et leurs besoins. Cette enquête a\


également permis d’évaluer la place d’OpenStreetMap au sein des collectivités. Il y a eu 70 réponses à ce questionnaire.

Cette enquête a révélé que 73% des enquêtés disposent d’une base de données qui répertorie les aménagements cyclables de leur collectivité. En revanche, seuls 55,7% des enquêtés possèdent leur propre modèle de données, tandis que 37% n’en possèdent pas.

45,7% des structures ont des difficultés pour numériser leurs données et 48,6% pour décrire sémantiquement ces aménagements. Cela peut s’expliquer par :

\-          des difficultés d’interprétation, de conceptualisation et de modélisation de la réalité ;

\-          une dichotomie entre la législation (arrêtés) et la réalité de terrain.

Cette dichotomie pourrait provenir de la différence d’approches entre les bases de données institutionnelles et OpenStreetMap. Selon les enquêtés, OpenStreetMap répond mieux aux besoins des usagers des aménagements cyclables, tandis que des bases de données institutionnelles sont plus adaptées aux besoins des techniciens et des aménageurs ;

\-          un manque de connaissance du patrimoine disponible.

#### 80% des communautés territoriales ayant répondu au questionnaire pensent qu’un standard serait utile et faciliterait leur travail.

### **2.** **Besoins identifiés**

Les résultats de cette enquête et les entretiens que nous avons menés auprès de producteurs de données et de réutilisateurs nous ont permis de déterminer les attentes générales de l’harmonisation de ces données. Ce standard doit :

\-          permettre d’utiliser un langage commun : il faut une nomenclature sans variation entre les communes ;

\-          être simple, bien documenté, avec des définitions claires ;

\-          être accessible aux petites structures techniquement et en termes de coût ;

\-          être flexible et modulable : ce schéma doit permettre d’intégrer de nouveaux types d’aménagements ;

\-          permettre l’interopérabilité entre les collectivités françaises et à l’échelle de l’Union Européenne ;

\-          être compatible avec OpenStreetMap ;

\-          faciliter l’aide à la décision ;

\-          permettre de mieux gérer le patrimoine.

Nous nous intéressons plus particulièrement aux données servant à l’information voyageur et qui pourront donc être intégrées dans des calculateurs d’itinéraires.

Des modules complémentaires seront toutefois proposés aux collectivités pour répondre à leurs attentes communes.

### 3.     Présentation d’une version alpha d’un schéma de données et retour des participants

Après avoir identifié ces besoins et grâce au schéma d’Île-de-France mobilités (IDFM), à celui de la Fédération française des usagers de la bicyclette (FUB) et des tags OpenStreetMap, nous avons élaboré une version alpha du schéma de données

Cette    version    alpha    est    composée  de    plusieurs            champs   et         est    consultable ici : [https://docs.google.com/spreadsheets/d/153snS5uDK16hlQEvhP0qtJQVhESacf-](https://docs.google.com/spreadsheets/d/153snS5uDK16hlQEvhP0qtJQVhESacf-469KDb2X2fi4/edit#gid%3D1951087160) [469KDb2X2fi4/edit#gid=1951087160](https://docs.google.com/spreadsheets/d/153snS5uDK16hlQEvhP0qtJQVhESacf-469KDb2X2fi4/edit#gid%3D1951087160)

Une remarque a été soulevée dès le début de l’atelier : le schéma de données ne doit pas être pensé au niveau français mais à l’échelle européenne pour que les données puissent être interopérables. Il faut donc garder en tête que les données et les champs proposés doivent pouvoir être saisis par des producteurs qui ne sont pas français et être utiles à des réutilisateurs qui ne se cantonnent pas aux itinéraires cyclables français.

Nous avons ensuite passé en revue chaque champ proposé afin de valoriser les retours que nous avons eus.

_-          Identifiant unique_

Ce code sera déterminé par le PAN

\- _Identifiant OSM si passage par OSM_

Remarques de certains sur le fait que l’identifiant OSM n’est pas pérenne. Proposition de rajouter un identifiant local des collectivités.

\-          Code INSEE

\-          ~~Code EPCI~~

\-           ~~Code département~~

\-         ~~Code région~~

\-        ~~Code aménagement~~

#### Tous ces codes peuvent être redondants, il serait plus pertinent de ne garder que le code INSEE.

\-         _Type d’aménagement cyclable_

Ce champ liste les types d’aménagements qu’on retrouve dans le code de la route et ceux que l’on retrouve dans les collectivités sans qu’ils fassent partie du code de la route afin de refléter au mieux les réalités du terrain.

Une définition de chaque aménagement avec une photothèque est attendue pour faciliter la compréhension.

\-          _Avancement de l’infrastructure_

Ce champ n’est pas utile aux réutilisateurs de données, cela pourrait complexifier le schéma de données. Il peut être mis dans le module complémentaire. Le réutilisateur serait plutôt intéressé par la pérennisation des infrastructures : savoir si elles sont pérennes ou provisoires.

\-  _Date de mise en service_

Ce champ n’est pas utile aux réutilisateurs.

Þ Il peut être placé dans le module complémentaire.

\-          _Type de revêtement de la chaussée_

Même s’il est difficile de décrire cette donnée avec des catégories simples car il y a beaucoup de types de revêtement, il serait mieux de réduire les catégories pour n’en retenir que 4 au maximum.

_-          État du revêtement_

Les valeurs proposées dans ce champ sont subjectives. Il faudrait trouver d’autres indicateurs.

De plus, ce niveau de détail n’est pas utile dans le cadre d’une réutilisation numérique mais l’est pour l’entretien de voirie, ce qui correspond exclusivement aux besoins des collectivités.

Ce champ pourrait toutefois permettre de déduire la cyclabilité en le croisant avec d’autres champs.

#### &#x20;Il peut être placé dans le module complémentaire.

\-   _Sens vélo_

_-          Sens général_

\-          _Pente_

Au lieu de préciser s’il y a une pente ou non, il serait plus pertinent de définir un seuil à partir duquel on renseigne un pourcentage de pente.

\-          _Largeur et longueur de l’aménagement_

Le fait de connaître la longueur de l’aménagement n’est pas utile. Ce champ peut être remplacé par les champs largeur droite / largeur gauche ?

_-           Distance à la chaussée_

Ce champ n’a pas été jugé utile et a donc été supprimé.

\-          _Date de mise à jour du segment_

Cette information est intéressante pour les réutilisateurs de données OSM car l’identifiant OSM n’est pas pérenne dans le temps.

\- _Sécurisation_

Ce champ n’a pas été jugé utile et a donc été supprimé.

\-          _Vitesse max du trafic adjacent_

Ce champ pourrait être intéressant pour les cyclistes novices afin d’évaluer le niveau de confort. Toutefois, ce n’est pas une information indispensable. Ce champ peut donc être optionnel.

\-           _Volume de trafic routier_

Ce champ n’a pas été jugé utile et a donc été supprimé.

_-           Voie partagée_

Cette information a déjà été renseignée dans l’option « zone partagée » dans la liste des aménagements cyclables.

Ce champ a donc été supprimé

_-          Signalisation_

Le type de signalisation n’est pas évident pour les réutilisateurs et peut donc être un champ optionnel

_-          Présence ou non de luminaires_ (éclairé ou non) .

\-    _Cyclabilité_

Cette approche est assez subjective car tout le monde n’a pas le même niveau d’appréciation. C’est une information difficile à uniformiser car elle dépend du contexte : taille des pneus, confort personnel, expérience du cycliste etc. Chaque cycliste a son ressenti.

&#x20;Il faudrait trouver des critères plus objectifs.

### 4.     Zoom sur les propositions d’amélioration pour les options proposées dans les types d’aménagements cyclables.

Dans la version alpha, les types d’aménagements cyclables proposés étaient les suivants :

| Piste cyclable                                                 |
| -------------------------------------------------------------- |
| Bande cyclable                                                 |
| Double sens cyclable                                           |
| Voie verte                                                     |
| Vélo-rue                                                       |
| Chaussée à voie centrale banalisée                             |
| Couloir ouvert bus-vélo                                        |
| Couloir fermé bus-vélo                                         |
| Rampe                                                          |
| Goulotte                                                       |
| Aménagements mixtes piéton/vélo hors voie verte                |
| Cyclistes pied à terre                                         |
| <p>Trajectoire suggérée</p><p>Zones de circulation apaisée</p> |

\-          Il n’y a pas de zones d’infrastructures spéciales pour les vélos dans les zones de circulation apaisée. Cette option peut donc être retirée de la liste

\-          Le couloir bus fermé n’est pas à renseigner dans cette liste car il n’est pas accessible aux cyclistes.

\-          Dans la réglementation une zone 30 et une zone de rencontre sont des aménagements cyclables. En effet, dans la zone 30, le cycliste est prioritaire sur la voiture. Elles doivent être inclues dans la liste.

Il serait intéressant d’ajouter un champ sur les **aménagements temporaires,** les aménagements cyclables de transition.

## 5.     Quelles suites à cet atelier ?

Nous avons repris la version alpha et avons intégré les retours que nous avons eu lors de l’atelier.

La version bêta du schéma de données a été envoyée aux participants. Nous attendons un travail de hiérarchisation des champs par les collectivités et les réutilisateurs, à savoir définir quels champs sont optionnels et lesquels sont obligatoires, pour pouvoir améliorer ce schéma.
