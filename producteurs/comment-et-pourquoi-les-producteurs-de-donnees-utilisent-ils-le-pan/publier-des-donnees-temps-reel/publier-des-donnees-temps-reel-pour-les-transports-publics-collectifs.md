# Publier des données temps réel pour les transports publics collectifs

L'ouverture des données temps réel pour les transports publics collectifs sur [transport.data.gouv.fr](https://transport.data.gouv.fr) peut se faire selon[ ](https://transport.data.gouv.fr):&#x20;

* le format [SIRI Profil France ](http://www.normes-donnees-tc.org/wp-content/uploads/2021/10/BNTRA-CN03-GT7\_NF-Profil-SIRI-FR\_v1.2\_20210308.pdf)
* le format [SIRI Lite ](http://www.normes-donnees-tc.org/wp-content/uploads/2017/01/Proposition-Profil-SIRI-Lite-initial-v1-2.pdf)(spécification non finalisée)
* le format [GTFS-RT ](https://github.com/google/transit/blob/master/gtfs-realtime/CHANGES.md)en complément du SIRI ou SIRI Lite (Le seul GTFS-RT est toléré si le producteur n'est pas encore en mesure de diffuser des données au format SIRI ou SIRI Lite)

L'objectif de cette documentation est de vous accompagner dans la publication de ces données selon ces formats.

{% hint style="info" %}
Les données doivent d'abord être référencées sur [data.gouv.fr](https://www.data.gouv.fr/fr/). Plus d'informations [ici](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan). Une fois que ce référencement est fait, il devient possible de [mettre à jour ses données](https://doc.transport.data.gouv.fr/producteurs/mettre-a-jour-des-donnees) à partir de [transport.data.gouv.fr](https://transport.data.gouv.fr).
{% endhint %}

## Le format SIRI Profil France

Le [règlement délégué UE n°2017-1926](https://eur-lex.europa.eu/eli/reg\_del/2017/1926/oj?locale=fr) impose la norme SIRI pour l'ouverture des données temps-réel des transports publics collectifs. Cette norme se décline en France en un profil (sous-ensemble de la norme) correspondant au format légal.

{% hint style="info" %}
Cette publication est en cours de rédaction. Elle sera prochainement complétée pour intégrer la partie "Publication des données temps réel au format SIRI".
{% endhint %}

Si un producteur n'est pas encore en mesure de produire ou diffuser des données temps-réel sous ce format, il peut les publier au format GTFS-RT en attendant de pouvoir publier ses données au format SIRI. Nous encourageons les producteurs qui produisent des données aux formats SIRI et GTFS-RT à référencer les deux formats.

Si vous produisez des données SIRI mais que vous rencontrez des difficultés à les diffuser en opendata, vous pouvez nous contacter à l'adresse : c[ontact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)

## Le format [SIRI Lite ](http://www.normes-donnees-tc.org/wp-content/uploads/2017/01/Proposition-Profil-SIRI-Lite-initial-v1-2.pdf)Profil France&#x20;

Le SIRI Lite est un sous-dérivé de SIRI qui a pour objectif d'être complètement compatible avec le SIRI profil France et Île-de-France.&#x20;

Les données sont servies via une API HTTP classique dans le format JSON, ce qui peut le rendre un peu plus facile d'accès que SIRI (SOAP/XML).

Comme le SIRI, le SIRI Lite n'a pas besoin d'être associé à des données statiques au format GTFS ou Netex pour être réutilisé. Chaque service peut véhiculer une information complète (nom de l'arrêt, de la ligne, DestinationDisplay, etc.).

### Le référencement des données SIRI Lite sur transport.data.gouv.fr

Si chaque flux d'information SIRI Lite est complet, il pourra être réferencé dans un jeu de données qui lui sera propre sans association à des données théoriques en suivant [une de ces méthodes de publication](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan/publier-un-jeu-de-donnees).

## Le format GTFS-RT

Le [GTFS-RT](https://github.com/google/transit/blob/master/gtfs-realtime/CHANGES.md) est un standard maintenu et étendu de manière communautaire sous l’égide de [MobilityData](https://mobilitydata.org).

Ce format permet de récupérer toutes les données temps réel d’un réseau en une requête.

Ce flux temps réel peut contenir trois types d’information :

* ``[`TripUpdates`](https://gtfs.mobilitydata.org/spec/trip-updates) qui correspond à la mise à jour des horaires de passage
* ``[`ServiceAlerts` ](https://gtfs.mobilitydata.org/spec/service-alerts)qui génère des alertes de service
* ``[`VehiclePositions`](https://gtfs.mobilitydata.org/spec/vehicle-positions) qui renseigne la position des véhicules\
  Plus d'informations[ ici](https://doc.transport.data.gouv.fr/producteurs/operateurs-de-transport-regulier-de-personnes/temps-reel-des-transports-en-commun).

Certains producteurs proposent toutes ces informations dans un seul flux, comme [Zenbus](https://transport.data.gouv.fr/datasets?\_utf8=%E2%9C%93\&q=zenbus), tandis que d’autres préfèrent avoir un flux par type d’information. C’est le cas pour la RATPdev avec les données du réseau [Bibus de Brest](https://transport.data.gouv.fr/datasets/horaires-theoriques-et-temps-reel-des-bus-et-tramways-circulant-sur-le-territoire-de-brest-metropole/) qui ont été publiées avec un flux pour `TripUpdates`un autre pour `ServiceAlerts` et un autre pour `VehiclePositions`&#x20;

Plus d'informations dans notre [article de blog sur la production et la diffusion des données temps réel pour les transports en commun](https://blog.transport.data.gouv.fr/billets/la-production-des-donn%C3%A9es-temps-r%C3%A9el-interview-avec-diff%C3%A9rents-producteurs-de-donn%C3%A9es/).

## Le référencement des données GTFS-RT&#x20;

**Pour associer une ressource théorique et une ressource temps-réel, il est aujourd'hui nécessaire de les regrouper dans un jeu de données.** Ces données doivent partager les mêmes identifiants, pour pouvoir être réutilisées. Les données statiques et temps-réel doivent donc être dans le même jeu de données. \
Pour cela, il vous suffit de référencer votre ressource théorique sur [data.gouv.fr](https://www.data.gouv.fr/fr/) puis de cliquer sur "Ajouter" > "\[...]fichier distant existant  > compléter les informations puis cliquer sur "Enregistrer" pour ajouter les données temps-réel. \
![](<../../../.gitbook/assets/image (174) (1).png>)![](<../../../.gitbook/assets/image (176).png>)

Une fois que les données seront référencées sur [transport.data.gouv.fr](https://transport.data.gouv.fr), votre jeu de données devrait apparaître comme suit :&#x20;

![Jeu de données contenant un GTFS et un GTFS-RT ](<../../../.gitbook/assets/image (170) (1).png>)

Lors de la publication, nous recommandons de préciser dans le nom de la ressource :&#x20;

* le réseau concerné
* le type d'informations diffusées pour les données temps-réel lorsqu'il y a un flux par information

![](<../../../.gitbook/assets/image (169) (1) (1).png>)

Si il y a plusieurs informations dans un seul flux, nous recommandons de préciser cette information dans la description du jeu de données.

## Recommandations sur la latence des données temps-réel&#x20;

{% hint style="info" %}
Cette documentation est en cours de rédaction. Elle sera prochainement complétée pour intégrer nos recommandations pour le SIRI et SIRI Lite&#x20;
{% endhint %}

Il n’y a pas d’exigence particulière concernant le niveau de service pour les données diffusées au format GTFS-RT. Il est toutefois utile aux réutilisateurs d'avoir accès à une donnée fraîche qui permet aux usagers finaux d'optimiser leur déplacement et de réduire leur temps d'attente. Nous recommandons de ne pas dépasser :&#x20;

* 1 min pour les flux `ServiceAlerts` et `TripUpdates`&#x20;
* 5 secondes pour le flux `VehiclePositions`



N'hésitez pas à consulter la [foire aux questions des données pour les transports en commun](https://doc.transport.data.gouv.fr/foire-aux-questions-1/donnees-temps-reel-des-transports-en-commun) et l'[article de blog sur la production et la diffusion des données temps réel pour les transports en commun](https://blog.transport.data.gouv.fr/billets/la-production-des-donn%C3%A9es-temps-r%C3%A9el-interview-avec-diff%C3%A9rents-producteurs-de-donn%C3%A9es/).



Vous avez des questions, des suggestions d'améliorations de cette documentation ? \
Contactez nous à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)



