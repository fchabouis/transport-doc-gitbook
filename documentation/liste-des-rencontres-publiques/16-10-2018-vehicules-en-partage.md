# 16/10/2018 - Véhicules en partage

**Contexte** : le [règlement européen 2017/1926](https://eur-lex.europa.eu/legal-content/FR/TXT/HTML/?uri=CELEX:32017R1926\&from=EN), d'application immédiate, impose une ouverture des données à jour, de qualité, aux normes, pour tous les modes de transport. La plateforme transport.data.gouv.fr vise à référencer l’ensemble de ces données ouvertes (statiques et temps réel). L’atelier du 16 octobre 2018 marque le lancement des travaux relatifs à l'ouverture des données VLS/autopartage et autres modes partagés en station ou en freefloating.

**Objectifs de la rencontre** : lever les freins à l'ouverture des données temps réel pour améliorer l'information voyageur et faciliter les déplacements multimodaux ; comprendre le contexte du secteur et les spécificités de chaque participant pour proposer la mise en œuvre de l’obligation la plus adaptée aux besoins possible. 

**Déroulé de la réunion** : deux ateliers ont eu lieu en parallèle : les acteurs du VLS/autopartage en station d’une part, les acteurs du freefloating d’autre part.

| <p><strong>Conclusions de la réunion</strong></p><p><strong></strong></p><ul><li><p>Les chantiers suivants seront lancés de manière séparée dans les prochains mois : </p><ul><li>Chantier sur l’ouverture des données VLS en station statiques et temps réel, notamment harmonisation des données VLS (en GBFS ?) et référencement des données statiques des VLS en station déjà référencés sur data.gouv.fr ou d’autres sources ;</li><li>Chantier sur l’ouverture des données autopartage en station statiques et temps réel ;</li><li>Chantier sur l’ouverture des données de localisation des lieux de location moyenne et longue distance ;</li><li>Chantier sur l’ouverture des données des lieux de stationnement pour les vélos d’une part, pour les automobiles d’autre part.</li></ul></li><li>Concernant le freefloating, nous faisons un appel aux opérateurs pour inviter les volontaires à constituer un groupe de travail avec l’équipe transport.data.gouv.fr et mettre en oeuvre l’ouverture de leurs données relatives à la localisation et au type des véhicules disponibles en temps réel. </li><li>Les opérateurs “pilotes” sur tous ces thèmes feront bien entendu l’objet d’une communication massive auprès de la communauté transport.data.gouv.fr (l’ensemble des 330 autorités organisatrices de mobilité et près d’un millier de contacts qualifiés dans l’écosystème mobilités).</li></ul> |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |

### Atelier n°1 : VLS/autopartage en stations

#### Participants

* Opérateurs d’autopartage : Communauto, Ubeeqo, Zipcar,
* Opérateurs de VLS en stations : Keolis (Cykléo), Transdev (Véloway, Proxiway)
* Réutilisateurs : Bicyclette, Digimobee, Google, Here Technologies, Qucit
* Acteurs publics : IDF Mobilité, Mairie de Paris, Nantes Métropole
* Autres participants : Club des villes et territoires cyclables

#### Format

Une harmonisation du format pour le VLS est attendue par plusieurs participants (réutilisateurs, producteurs, AO). Le GBFS pourrait devenir un standard pour le VLS à l’image du GTFS / GTFS RT qui s’est imposé dans les transports publics. Son usage est cependant moins répandu (31 pays, inexistant en France) et cohabite avec des formats propriétaires. Le GBFS est développé par une communauté et est en constante évolution [https://github.com/NABSA/gbfs/blob/master/gbfs.md](https://github.com/NABSA/gbfs/blob/master/gbfs.md) S’il devait devenir le standard, il faudrait définir les composantes à renseigner pour les producteurs lorsque la donnée est générée (par exemple : spécificités des VLS, overflow, électrique, batterie, tarif,...).

#### Licence

A l’image du temps réel en transport public, le groupe s’interroge sur la pertinence d’une licence ODbL : a-t-elle du sens, sachant que le partage à l’identique de données périmées n’a pas grand intérêt ? Des retours de réutilisateurs sont cependant possibles pour améliorer la qualité de la donnée : par exemple si une station VLS ou une place est mal localisée, des réutilisateurs peuvent faire remonter l’information dans le module de discussion.

#### Fréquence de mise à jour

Pour les données en temps réel, une actualisation par minute semble être privilégiée car assez fiable (à la fois pour les producteurs et les réutilisateurs), bien qu’une fréquence plus soutenue pourrait améliorer l’information voyageur dans l’avenir (30s, 5s,...). En effet, le risque de frustration chez l’usager en cas de vélo ou de place non disponibles peut exister : à charge aux calculateurs d’itinéraires d’indiquer ce risque ou de mettre en place des modèles prédictifs pour le pallier. 

#### Gestion de la charge

Des craintes existent sur la gestion de la charge des requêtes, renforcées si la demande n’est pas en bulk. Le format GBFS permet notamment une gestion des requêtes en bulk, à la fois pour les producteurs et pour les réutilisateurs. Pour faire face à une éventuelle trop grande charge, transport.data.gouv.fr pourrait faire office de proxy en bulk. C’est ce que fait actuellement la Ville de Paris avec sa plateforme d’Open Data pour le VLS. 

#### Craintes sur un détournement des données

Des producteurs (VLS et autopartage) craignent une utilisation “déloyale” ou “détournée” des données par leurs concurrents (statistiques sur les retards, localisation de voitures). Une stratégie d’Open Data vise cependant à la transparence et au principe du “pot commun”, permettant une meilleure mobilité à l’usager final ; par ailleurs, les données relatives à l’information voyageur de transports publics (VLS si en DSP ou autres contractualisation) ont également vocation à être publiques. 

#### L’autopartage 

L’autopartage apparaît plus spécifique pour le groupe : la donnée en temps réel (situation du véhicule) apparaît moins utile - mais est déjà partagée par certains producteurs - que la donnée sur les disponibilités futures du véhicule (“planning du véhicule”). Plusieurs producteurs expliquent vouloir un cadre global, déterminé pour tous, pour la publication des données d’autopartage (norme, attributs, ...) afin que tous les acteurs soient alignés et que l’ouverture des données ne soit pas nivelée par le bas. La qualité de l’information est également questionnée.

#### Vélos en location moyenne et longue durée 

Le plan vélo prévoit l’ouverture des données de vélo, en particulier celles de location de vélos en courte et moyenne durée. Elles concernent des acteurs en tout genre : privé en DSP ou non, startups, associations,  etc. Ces données pourraient améliorer sensiblement la mobilité, les territoires couverts étant par ailleurs importants (environ 70 services en France). Elles concernent majoritairement le statique bien que du temps réel s’implantent par exemple sur des parkings à vélos dans certaines collectivités par exemple. Un fichier national pourrait être consolidé par transport.data.gouv.fr à l’image des bornes IRVE. 

### Atelier n°2 : freefloating

#### Participants

* Réutilisateurs : OpenAPI, Mappy
* Opérateurs : Cityscoot, Véloway, Bird, Coup, OFO, Oribiky, Mappy, Txfy, Mobike, Indigo, Lime
* Acteurs publics : Mairie de Paris
* Autres : CEREMA, SNCF, Renault

L’enthousiasme des acteurs du freefloating pour l’ouverture des données relatives à l’information voyageur (périmètre : type de véhicule, longitude, latitude et éventuellement niveau de charge pour les véhicules disponibles à la réservation) est moyen. Les opérateurs n’y voient pas de grands bénéfices à en tirer, et ne déclarent pour la plupart ne pas avoir besoin de mise en visibilité plus large. Si la plupart des acteurs ne sont pas opposés farouchement à l’ouverture, deux risques majeurs sont soulevés : 

* Concurrence : les nouveaux entrants sur le marché du freefloating bénéficieraient de l’intelligence de l’offre/demande en ayant accès aux données sur les véhicules disponibles en freefloating. (Le nouvel entrant saurait exactement où s’implanter)
* Désintermédiation : perte de la relation directe avec les clients au bénéfice des services d’informations voyageurs.

### Position des opérateurs de freefloating

Les opérateurs préfèreraient conserver une logique de contractualisation bilatérale avec des fournisseurs de services d’information sur les déplacements (ex : Citymapper) pour conserver une marge de négociation et contrôler les accès à la données. 

Le règlement européen impose cependant l’ouverture avec des conditions de réutilisation aussi peu limitées que possible. Il n’interdit cependant pas l’obligation d’identification des réutilisateurs qui auraient accès aux API ouvertes. Cette obligation d’identification est plutôt accueillie favorablement par les opérateurs. Il est demandé de vérifier si des CGU pourraient permettre aux opérateurs de couper l’accès aux données en cas d’abus (ex : exploitation intensive des données. 

### Aspects technique

Le format standard n’existe pas. La plupart des fournisseurs fournissent un rayon autour d’un point. Afin de limiter la charge lors des requêtes, l’idéal est pourtant d’obtenir un fichier décrivant l’ensemble du réseau (ou la localisation des véhicules sur un territoire donné), récupérable en une requête unique par l’usager. Il faut étudier la possibilité du GBFS, qui est un format plutôt adapté aux vélos, mais qui pourraient aussi s’appliquer aux trottinettes. [L’exemple de Washington](https://blog.mapbox.com/cities-benefit-from-open-dockless-data-bfe610b0568e) où les opérateurs de freefloating sont tenus de maintenir une API temps réel ouverte et à jour de la localisation et des types de véhicules disponibles pour les usagers, montre que le GBFS peut être utilisé pour tous les opérateurs présents autour de la table.

### Autres sujets : 

Plutôt qu’à l’ouverture des données, les opérateurs adhèrent au partage des données (information voyageur + usage) avec les opérateurs publics (notamment pour favoriser le développement des initiatives MaaS) selon des contrats qui pourraient être harmonisés pour faciliter les discussions. Du côté des collectivités, un des gros besoins identifiés est de récupérer et de visualiser plus facilement les données d’usage. Cependant, ce sujet n’est pas du ressort de l’équipe transport.data.gouv.fr.\
