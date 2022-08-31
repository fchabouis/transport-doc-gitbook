---
description: Spécifications pour publication d'un flux temps-réel sur le PAN
---

# Les données temps réel

### Exigences juridiques&#x20;

L’[arrêté du 4 mars 2022](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000045382208) relatif aux spécifications techniques de mise à disposition des données de mobilités vise le site [https://normes.transport.data.gouv.fr](https://normes.transport.data.gouv.fr), qui référence les profils France officiels des normes européennes (NeTex & SIRI), et d’éventuels schémas de données non couverts par ces normes.

Pour les données horaires en temps réel des services réguliers, les exigences juridiques correspondent ainsi au profil France de la norme SIRI. L’ouverture des données doit ainsi être conforme aux spécifications de ce profil, qui peut être exprimé en SIRI ou SIRI Lite.

Le PAN recommande et incite par ailleurs à ce que les producteurs de données ouvrent également leurs données horaires en temps réel au format GTFS-RT. Ce format est en effet aujourd’hui majoritairement utilisé par l’écosystème de l’information voyageurs, permettant donc de faciliter et maximiser l’intégration de données dans des services numériques d’information voyageurs.



### Récapitulatif des conditions de publication de données temps-réel sur le PAN

Pour être publié sur transport.data.gouv.fr, un jeu de données temps-réel de lignes régulières doit respecter **toutes** les conditions suivantes :

* Horaires théoriques disponibles,
* Une API Siri-lite ou une API SIRI conforme au profil France de la norme SIRI, et un flux au format GTFS-RT (au minimum avec trip updates),
* Données utilisables selon les conditions de la licence ouverte (l’application d’une autre licence s’effectue sous réserve de modalités techniques ou juridiques le justifiant),
* Pas d’authentification pour accéder aux données (sous réserve de modalités techniques ou juridiques le justifiant),&#x20;
* Pas de restriction de requêtage (sous réserve de modalités techniques ou juridiques le justifiant).



{% hint style="info" %}
Les jeux de données temps-réel qui ne correspondent pas à l'ensemble de ces critères sont listés pour référence [sur cette page](https://transport.data.gouv.fr/real\_time).
{% endhint %}

### S'y retrouver : GTFS-RT, SIRI, SIRI-Lite, API ?

#### Différents types de temps réel

L’information en temps réel se décline habituellement en quatre variantes :

* Avance/retard des véhicules
  * Dans le standard GTFS-RT : _Trip updates_
  * Dans la norme SIRI : _Estimated Timetable (ET)_
* Prochains passages
  * Dans le standard GTFS-RT : _Trip updates_
  * Dans la norme SIRI : _Stop Monitoring (SM)_
* Position des véhicules&#x20;
  * Dans le standard GTFS-RT : _Vehicle positions_
  * Dans la norme SIRI : _Vehicle Monitoring (VM)_
* Messages d’information et d’alerte
  * Dans le standard GTFS-RT : _Service alerts_
  * _Dans la norme SIRI : General Messaging (GM), Situation Exchange (SX)_

Ces quatre approches sont complémentaires et aucune n’est suffisante par elle même : par exemple, l’avance-retard permet de proposer des itinéraires adaptés à la situation réelle… La position des véhicules permet de rassurer l’usager qui a tendance à ne pas faire confiance aux projections et de donner une information en cas de situation très perturbée. Enfin, les messages d’alerte permettent de gérer de grandes perturbations (chute de neige, gros évènement sportif…) ou de donner des informations non temporelles (panne d’un ascenseur…).

#### Deux moyens de diffusion

* Un fichier unique « photographie » de l’ensemble du réseau à un instant _t_ (et donc un seul fichier à télécharger toutes les 30 secondes) : format GTFS-RT,
* Une API SIRI ou Siri-Lite.



SIRI ou SIRI-Lite ? SIRI répond initialement à des problématiques d'interopérabilité « intersystèmes ». SIRI-Lite est dérivé du SIRI « pour aller vers la diffusion vers les terminaux utilisateurs et l’open-data » (C. Duquesne).

Concrètement, **SIRI-Lite** utilise le même modèle de représentation que **SIRI** mais l’interrogation des serveurs se fait en[ REST](https://fr.wikipedia.org/wiki/Representational\_state\_transfer) et non pas en[ SOAP](https://fr.wikipedia.org/wiki/SOAP).

Toutes les API pourront être référencées (« listées ») mais pas hébergées par le PAN. **Le PAN peut en particulier assumer la charge de requêtes potentiellement nombreuses uniquement pour le GTFS-RT (voir plus bas pour l'aspect serveur proxy)**.\
****Pour toutes mises à disposition de données via une API SIRI ou SIRI Lite, nous vous recommandons de contacter notre équipe qui effectue actuellement des développements en lien avec ces formats.

### Spécifications pour le GTFS-RT sur le PAN

{% hint style="info" %}
[Documentation officielle du GTFS-RT ici.](https://developers.google.com/transit/gtfs-realtime/index?hl=fr)
{% endhint %}

Le GTFS-RT s'appuie nécessairement sur un fichier GTFS décrivant les lignes et horaires théoriques, car il indique la différence observée par rapport à ces horaires prévus. Les identifiants doivent être les mêmes entre le GTFS et le GTFS-RT.&#x20;

Certains producteurs proposent [toutes les informations pouvant être diffusées dans du GTFS-RT](https://doc.transport.data.gouv.fr/producteurs/operateurs-de-transport-regulier-de-personnes/temps-reel-des-transports-en-commun#sy-retrouver-gtfs-rt-siri-siri-lite-api) dans un seul flux, comme [Zenbus](https://transport.data.gouv.fr/datasets?\_utf8=%E2%9C%93\&q=zenbus), tandis que d’autres préfèrent avoir un flux par type d’information. C’est le cas pour la RATPdev avec les données du réseau [Bibus de Brest](https://transport.data.gouv.fr/datasets/horaires-theoriques-et-temps-reel-des-bus-et-tramways-circulant-sur-le-territoire-de-brest-metropole/) qui ont été publiées avec un flux pour `TripUpdates`un autre pour `ServiceAlerts` et un autre pour `VehiclePositions`&#x20;

Plus d'informations dans notre [article de blog sur la production et la diffusion des données temps réel pour les transports en commun](https://blog.transport.data.gouv.fr/billets/la-production-des-donn%C3%A9es-temps-r%C3%A9el-interview-avec-diff%C3%A9rents-producteurs-de-donn%C3%A9es/).

### Spécifications pour le SIRI-Lite sur le PAN

{% hint style="info" %}
Documentation _en cours de publication_ pour le SIRI-Lite&#x20;
{% endhint %}

Parmi les services proposés par SIRI-Lite, pour satisfaire les obligation de mise à disposition du temps réel, **pour publication sur le PAN, il est obligatoire d’exposer **_**EstimatedTimetable**_ car c’est le seul qui permet de s’approcher d’une diffusion en « photographie ».

Les autres services _StopMonitoring,  GeneralMessage, VehicleMonitoring, StopDiscovery, LineDiscovery_ sont recommandés en sus.

### Pourquoi ces exigences de la part du PAN ?

Le Point d'Accès National a pour mission exclusive d'améliorer l'information voyageur à travers la France et cela passe par favoriser la réutilisation de la donnée de transport.

Pour cela, l'équipe du PAN est en contact permanent avec les réutilisateurs de données. Il ressort de nombreuses concertations que :

* Les réutilisateurs ont besoin de flux de données standardisés, sous peine, au mieux, d'importants travaux d'intégration des flux, et au pire la non-exploitation de ces flux.\

* Les fournisseurs de services de calcul d'itinéraires et de mobilité privilégient le téléchargement de l'intégralité du réseau en une seule requête (paramètres _Mises à jour du réseau/Trip Update_ en GTFS-RT, _EstimatedTimetable_ en SIRI-Lite) plutôt qu'une multitude d'appels arrêt par arrêt.\

* Il est possible de reconstituer la donnée pour un point d'arrêt à partir de l'ensemble du réseau, mais pas l'inverse.\

* L'identification préalable à l'accès aux données est un frein à leur réutilisation. Elle impose des démarches individualisées pour chaque réseau.\

* Le GTFS-RT est le format le plus publié en opendata et le plus réutilisé actuellement.&#x20;

### Le PAN comme serveur proxy pour assumer la charge-serveurs

Face à la crainte que ces données temps réel génèrent une charge intense sur les serveurs et donc des frais de mise à disposition importants, le PAN peut se placer temporairement comme serveur-proxy. Dans ce cas, le PAN récupère les données à une fréquence qui sera déterminée entre le producteur et l'équipe de [transport.data.gouv.fr](https://transport.data.gouv.fr/). Par défaut, cette fréquence est de 10 secondes pour les flux `Alerts` et `TripUpdate` et de 5 secondes pour le flux `VehiculePositions`. Ces données sont stockées sur les serveurs du PAN et servies aux réutilisateurs depuis les serveurs du PAN. Ainsi, quel que soit le volume réel de réutilisation de ces données, l'AOM ou son prestataire ne connait qu'une seule requête.

Pour faire une demande de proxy, nous vous invitons à envoyer l'URL vers votre flux temps-réel à l'adresse  [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr). Nous reviendrons ensuite vers vous avec un lien personnalisé que vous pourrez renseigner sur votre compte data.gouv.fr.&#x20;

Pour des contraintes techniques, **ce schéma du PAN comme serveur-proxy n'est possible qu'avec une diffusion au format GTFS-RT.**&#x20;
