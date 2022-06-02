---
description: Spécifications pour publication d'un flux temps-réel sur le PAN
---

# Les données temps réel

### Récapitulatif des conditions de publication de données temps-réel sur le PAN

{% hint style="info" %}
Le point d’accès `Siri Lite` et `GTFS-RT` pour tous les jeux de données publiés sur le PAN est [tr.transport.data.gouv.fr](https://tr.transport.data.gouv.fr).
{% endhint %}

Pour être publié sur transport.data.gouv.fr, un jeu de données temps-réel de lignes régulières doit respecter **toutes** les conditions suivantes :

* Horaires théoriques disponibles,
* Horaires en temps réel (avance/retard des véhicules),
* Soit au format GTFS-RT (au minimum avec _trip updates_),\
  Soit une API Siri-lite (au minimum avec _stop monitoring_ et _stop discovery_),
* Données utilisables selon les conditions de la licence _ODbL_ ou licence ouverte,
* Pas d’authentification pour accéder aux données (sous réserve de modalités techniques le justifiant),
* Pas de restriction de requêtage (nous nous réservons le droit de couper les accès dépassant 1 requête par seconde).

{% hint style="info" %}
Les jeux de données temps-réel qui ne correspondent pas à l'ensemble de ces critères sont listés pour référence [sur cette page](https://transport.data.gouv.fr/real\_time).
{% endhint %}

### S'y retrouver : GTFS-RT, SIRI, SIRI-Lite, API ?

#### Différents types de temps réel

L’information en temps réel se décline habituellement en quatre variantes :

* Avance/retard des véhicules
  * Dans le standard GTFS-RT : _Trip updates_
  * Dans la norme SIRI : _Estimated Timetable_
* Prochains passages
  * Dans le standard GTFS-RT : _Trip updates_
  * Dans la norme SIRI : _Stop Monitoring_
* Position des véhicules&#x20;
  * Dans le standard GTFS-RT : _Vehicle positions_
  * Dans la norme SIRI : _Vehicle Monitoring_
* Messages d’information et d’alerte
  * Dans le standard GTFS-RT : _Service alerts_
  * _Dans la norme SIRI : General Messaging_

Ces quatre approches sont complémentaires et aucune n’est suffisante par elle même : par exemple, l’avance-retard permet de proposer des itinéraires adaptés à la situation réelle… La position des véhicules permet de rassurer l’usager qui a tendance à ne pas faire confiance aux projections et de donner une information en cas de situation très perturbée. Enfin, les messages d’alerte permettent de gérer de grandes perturbations (chute de neige, gros évènement sportif…) ou de donner des informations non temporelles (panne d’un ascenseur…).

#### Deux moyens de diffusion

* Un fichier unique « photographie » de l’ensemble du réseau à un instant _t_ (et donc un seul fichier à télécharger toutes les 30 secondes) : format GTFS-RT
* Une API pour requêter arrêt par arrêt (dite « unitaire » : prochains passages à cet arrêt de bus-ci) : format SIRI et Siri-Lite

L’approche d’un fichier unique permet de réduire très fortement la charge serveur (aucune intelligence à avoir, faible nombre d’appels, possibilité de mise en cache…) et permet de déduire les informations unitaires. À l’opposé, une API unitaire ne permet pas de mise en cache et génèrera beaucoup plus d’appels.&#x20;



**SIRI ou SIRI-Lite ?** SIRI répond initialement à des problématiques d'interopérabilité « _intersystèmes_ ». SIRI-Lite est dérivé du SIRI « pour aller vers la diffusion vers les terminaux utilisateurs et l’open-data » (_C. Duquesne_).

Concrètement, **SIRI-Lite** utilise le même modèle de représentation que **SIRI** mais l’interrogation des serveurs se fait en [Rest](https://fr.wikipedia.org/wiki/Representational\_state\_transfer) et non pas en [SOAP](https://fr.wikipedia.org/wiki/SOAP).

Toutes les API unitaires pourront être référencées (« listées ») mais pas hébergées par le PAN. Ainsi, **le PAN peut assumer la charge de requêtes potentiellement nombreuses uniquement pour le GTFS-RT** (voir plus bas pour l'aspect serveur proxy).

### Spécifications pour le GTFS-RT sur le PAN

{% hint style="info" %}
[Documentation officielle du GTFS-RT ici.](https://developers.google.com/transit/gtfs-realtime/index?hl=fr)
{% endhint %}

Le GTFS-RT s'appuie nécessairement sur un fichier GTFS décrivant les lignes et horaires théoriques, car il indique la différence observée par rapport à ces horaires prévus. Les identifiants doivent être les mêmes entre le GTFS et le GTFS-RT.&#x20;

### Spécifications pour le SIRI-Lite sur le PAN

{% hint style="info" %}
[Documentation non-finalisée pour le SIRI-Lite ici.](http://www.normes-donnees-tc.org/wp-content/uploads/2017/01/Proposition-Profil-SIRI-Lite-initial-v1-2.pdf)
{% endhint %}

Parmi les services proposés par SIRI-Lite, pour satisfaire les obligation de mise à disposition du temps réel, **pour publication sur le PAN, il est obligatoire d’exposer **_**EstimatedTimetable**_ car c’est le seul qui permet de s’approcher d’une diffusion en « photographie ».

Les autres services _StopMonitoring,  GeneralMessage, VehicleMonitoring, StopDiscovery, LineDiscovery_ sont recommandés en sus.

### Conditions d'accès aux données

Afin de se conformer aux standards de l'Open Data et à la Loi d'Orientation des Mobilités, il est attendu que ces flux temps-réel soient **librement accessibles, sans besoin d'identification** (sous réserve de modalités techniques le justifiant) ni approbation préalable du réutilisateur.

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
