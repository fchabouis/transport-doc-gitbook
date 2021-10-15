---
description: >-
  Cette foire aux questions reprend les questions qui sont les plus couramment
  posées par la communauté concernant la production et/ou la réutilisation des
  données temps-réel.
---

# Données temps-réel des transports en commun

Cette foire à question a été élaborée à partir des questions qui ont été posées lors d'appels avec des producteurs et réutilisateurs de données temps-réel des transports en commun. \
\
Elle sera mise à jour fréquemment de sorte à répondre aux nouvelles interrogations ou difficultés rencontrées par les producteurs et réutilisateurs. 

{% hint style="info" %}
 Depuis le mois d'avril 2021, le Point d'Accès National (PAN) ne fait plus de conversion GTFS-RT vers le SIRI-Lite car ces données converties n'étaient pas réutilisées et ce format ne permet pas de répondre à la réglementation européenne. 
{% endhint %}

## Formats

#### Quels sont les formats acceptés par le Point d'Accès National pour les données temps-réel ?

Le PAN supporte deux formats standards pour les données temps-réel :\
\
\- Le** GTFS-RT **(General Transit Feed Specification - realtime)\
Ce format permet de récupérer toutes les données temps réel d’un réseau en une requête et doit être associé à un fichier théorique au format GTFS. Il peut être diffusé lorsque le producteur demande au PAN de faire proxy sur ses serveurs pendant quelques mois.\
\
\- Le SIRI (Service Interface for Realtime Information)\
Le SIRI est une norme définie par le Comité Européen de Normalisation et correspond à la norme NeTEx pour le temps réel. Elle caractérise des services temps réel et est un format autoporteur. Ce format ne peut être que référencé sur le PAN.\
\
Plus d'informations [ici](https://blog.transport.data.gouv.fr/billets/la-production-des-donn%C3%A9es-temps-r%C3%A9el-interview-avec-diff%C3%A9rents-producteurs-de-donn%C3%A9es/)

#### Quel format faut-il privilégier ?

Le GTFS-RT n'est pas un format autoporteur car il doit être associé à un fichier théorique au format GTFS pour être utilisé. Si vous produisez du GTFS pour vos données sur les horaires théoriques, nous vous recommandons de publier un flux temps-réel au format GTFS-RT. Si vous produisez du NETEX pour vos horaires théoriques, nous vous recommandons de publier un flux temps-réel au format SIRI.\
En termes de réutilisation, le format GTFS-RT est le plus sollicité. 

#### Quel flux faut il privilégier dans le format GTFS-RT ?

Dans ce format, le flux le plus utilisé par les réutilisateurs des données publiées sur transport.data.gouv.fr est le ""TripUpdate"". Ce flux fait une mise à jour pour la journée du fichier sur les horaires théoriques (GTFS). Si vous avez la possibilité de ne plus publier qu'un flux, nous vous conseillons de commencer par cette information.

#### Quelle est la différence entre le SIRI-Lite et le SIRI ?

Le SIRI-Lite utilise le même modèle de représentation que SIRI mais l’interrogation des serveurs se fait en [REST](https://fr.wikipedia.org/wiki/Representational_state_transfer) et non pas en [SOAP](https://fr.wikipedia.org/wiki/SOAP), ce qui permet une intégration un peu plus facilitée. Pour pouvoir répondre à la réglementation européenne, les producteurs doivent diffuser un flux temps-réel au format SIRI. Le SIRI-Lite ne permet pas d'y répondre.\
Plus d'informations [ici](https://doc.transport.data.gouv.fr/producteurs/operateurs-de-transport-regulier-de-personnes/temps-reel-des-transports-en-commun)

#### Pourquoi vous ne diffusez pas d'informations temps-réel dans des formats propres aux collectivités/opérateurs ?

L'objectif du PAN est de faciliter la réutilisation des données. Diffuser des données dans des formats propres aux collectivités et opérateurs complexifierait la réutilisation des données car le réutilisateur aurait à traiter différemment chaque flux. De plus, le Réglement Européen UE 2017 1926 encadre l'ouverture des données en fixant des formats par type de données. Pour le temps-réel c'est le format SIRI qui est demandé.

## Fréquence de mise à jour

#### Quelle fréquence de mise à jour recommandez-vous ?

Nous recommandons de ne pas aller au delà de 2 min pour mettre à jour une donnée pour que l'information fournie soit considérée comme étant en temps-réel, notamment pour la position du véhicule. Plus cette information est rafraîchie, plus elle est utile. 

## Production des données 

#### Peut on sous traiter la production des données théoriques et celles des données temps-réel à deux sociétés différentes ?

Vous pouvez sous-traiter la production de ces deux types de données à des délégataires distincts. Vous devez toutefois veiller à ce que les identifiants des arrêts et le calendrier soient exactement les mêmes entre le fichier théorique et le flux temps-réel.

#### Qu'est ce que je dois mettre dans mon cahier des charges lorsque je veux que mes données temps-réel soient référencées sur le Point d'Accès National ?

Nous vous recommandons de préciser dans votre cahier des charges : le format de données, à savoir du GTFS-RT ou du SIRI la diffusion des données, selon le format, sur le Point d'Accès National (GTFS-RT) ou un portail OpenData (SIRI ou GTFS-RT) par le producteur l'hébergement de votre flux temps-réel sur les serveurs du producteurs de données si vos serveurs ne peuvent pas supporter plusieurs requêtes par minute"

## Diffusion des données 

#### Lorsqu'on délègue la production des données temps-réel : il vaut mieux que ça soit la collectivité ou le délégataire qui se charge de la publication ?

Pour faciliter la gestion de la qualité des données, nous préférons qu'il y ait les mêmes interlocuteurs pour les horaires théoriques et pour le temps-réel. Si la production de ces données est déléguée à un opérateur mais que la collectivité veut publier elle-même ses données, nous vous recommandons de donner accès à votre espace organisation de data.gouv.fr à votre délégataire et de nous transmettre ses coordonnées. Ainsi, si il y a des erreurs dans vos jeux de données ou qu'ils ne sont plus à jour, nous pourrons contacter directement le producteur en vous mettant en copie du mail.

#### Peut on publier des flux par informations ou il ne faut publier qu'un seul flux ?

Vous pouvez publier autant de flux que vous avez d'informations à transmettre. La communuaté de l'Auxerrois a par exemple publié un flux pour le "Trip Update" et un autre pour le "Vehicle position".

#### Pouvez-vous nous adresser une adresse IP fixe pour que nous puissions ensuite vous autorisez à accéder à nos données ?

Pour l'instant nous ne fournissons pas d'IP fixe, mais c'est à l'étude pour le futur, si le besoin était fort.

#### Gérez-vous la transmission des données pour lesquelles il faut une authentification pour y accéder ?

Le point d'accès national ne gère pas l'identification ou l'authentification des utilisateurs de données. Aussi, si vous exigez de telles conditions en matière d'accès à vos données, nous nous contenterons alors de référencer uniquement l'adresse ou le portail permettant d'y accéder.

#### Vous privilégiez les liens http ou https ?

Il faut préférer des liens https car ils permettent de protéger les données diffusées et garantissent mieux la vie privée des réutilisateurs (potentiellement personne seule)

#### Y a-t-il un système de compensation financière pour la diffusion de ces données ?

L'article 25 de la loi d'orientation des mobilités vous accorde en effet la possibilité de mettre en place une compensation à l'utilisation de ces données, au delà de certains seuils précisés dans son décret d'application n°2020-1753 du 28 décembre 2020. A noter toutefois que si vous faîtes le choix de saisir cette option, vous êtes chargé de mettre en place toutes les fonctionnalités nécessaires à la diffusion de ces données payantes (portail d'accès, authentification, mesure de la consommation, facturation, gestion des paiements, ...). Le point d'accès national est en effet un service gratuit qui n'a pas vocation à gérer la transmission de données soumises à compensation financière. Nous pourrons néamoins vous proposer d'assurer la diffusion des données non soumises à compensation financière (en deçà des seuils du décret susmentionné).

## Licences

#### Sous quelle.s licence.s sont publiées les données ?

Le choix de la licence est laissé à la discrétion du producteur de données. Le point d'accès national recommande toutefois l'utilisation de la licence ouverte pour les données en temps réel.





