# Publier des données temps réel pour les transports publics collectifs

{% hint style="info" %}
Les données doivent d'abord être référencées sur [data.gouv.fr](https://www.data.gouv.fr/fr/). Plus d'informations [ici](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan). Une fois que ce référencement est fait, il devient possible de [mettre à jour ses données](https://doc.transport.data.gouv.fr/producteurs/mettre-a-jour-des-donnees) à partir de [transport.data.gouv.fr](https://transport.data.gouv.fr/).
{% endhint %}

## Le référencement des données SIRI ou SIRI-Lite sur transport.data.gouv.fr

Si chaque flux d'information SIRI ou SIRI-Lite est complet, il pourra être réferencé dans un jeu de données qui lui sera propre sans association à des données théoriques en suivant [une de ces méthodes de publication](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan/publier-un-jeu-de-donnees).

## Le référencement des données GTFS-RT&#x20;

**Pour associer une ressource théorique et une ressource temps-réel, il est aujourd'hui nécessaire de les regrouper dans un jeu de données.** Ces données doivent partager les mêmes identifiants, pour pouvoir être réutilisées. Les données statiques et temps-réel doivent donc être dans le même jeu de données. \
Pour cela, il vous suffit de référencer votre ressource théorique sur [data.gouv.fr](https://www.data.gouv.fr/fr/) puis de cliquer sur "Ajouter" > "\[...]fichier distant existant  > compléter les informations puis cliquer sur "Enregistrer" pour ajouter les données temps-réel. \
<img src="../../../.gitbook/assets/image (174) (2).png" alt="" data-size="line"><img src="../../../.gitbook/assets/image (176) (1) (1).png" alt="" data-size="line">

Une fois que les données seront référencées sur [transport.data.gouv.fr](https://transport.data.gouv.fr/), votre jeu de données devrait apparaître comme suit :&#x20;

![Jeu de données contenant un GTFS et un GTFS-RT ](<../../../.gitbook/assets/image (170) (2).png>)

Lors de la publication, nous recommandons de préciser dans le nom de la ressource :&#x20;

* le réseau concerné
* le type d'informations diffusées pour les données temps-réel lorsqu'il y a un flux par information

![](<../../../.gitbook/assets/image (169) (1) (1).png>)

Si il y a plusieurs informations dans un seul flux, nous recommandons de préciser cette information dans la description du jeu de données.

## **Qualité des données**&#x20;

Avant de publier les données, nous recommandons aux producteurs d'évaluer la qualité de leurs ressources en utilisant le validateur de fichier disponible dans l'onglet "Outils" > "Evaluer la qualité d'un fichier ou d'un flux"> "GTFS-RT" de la page d'accueil de transport.data.gouv.fr : [https://transport.data.gouv.fr/validation?type=gtfs-rt](https://transport.data.gouv.fr/validation?type=gtfs-rt)

![](<../../../.gitbook/assets/image (180) (1) (1).png>)

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



{% hint style="info" %}
Plus d'informations sur les formats attendus pour les données temps-réel pour le transport collectif [ici](https://doc.transport.data.gouv.fr/producteurs/operateurs-de-transport-regulier-de-personnes/temps-reel-des-transports-en-commun).
{% endhint %}

{% hint style="info" %}
Une fois les données publiées, les producteurs de données doivent par ailleurs fournir une déclaration de conformité. Plus d'informations [ici](https://doc.transport.data.gouv.fr/presentation-et-mode-demploi-du-pan/declaration-de-conformite#vous-etes-producteur-de-donnees).&#x20;
{% endhint %}
