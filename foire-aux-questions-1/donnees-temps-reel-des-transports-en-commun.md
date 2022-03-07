---
description: >-
  Cette foire aux questions reprend les questions qui sont les plus couramment
  posées par la communauté concernant la production et/ou la réutilisation des
  données pour les transports en commun.
---

# Données pour les transports en commun

Cette foire aux questions a été élaborée à partir des questions qui ont été posées lors d'appels avec des producteurs, réutilisateurs de données des transports en commun et lors d'ateliers. \
\
Elle sera mise à jour fréquemment de sorte à répondre aux nouvelles interrogations ou difficultés rencontrées par les producteurs et réutilisateurs.&#x20;

{% hint style="info" %}
&#x20;Depuis le mois d'avril 2021, le Point d'Accès National (PAN) ne fait plus de conversion GTFS-RT vers le SIRI-Lite car ces données converties n'étaient pas réutilisées et ce format ne permet pas de répondre à la réglementation européenne.&#x20;
{% endhint %}

## Données théoriques pour les transports en commun

### Conversion GTFS vers le Netex&#x20;

#### Sur quel profil le convertisseur GTFS to Netex est-il basé ?

Le convertisseur [GTFS vers Netex ](https://github.com/CanalTP/transit\_model/tree/master/gtfs2netexfr)produit en sortie un jeu de données selon les spécifications du profil Netex France pour les horaires.

### **Profils Netex**&#x20;

#### **Le profil Île-de-France permet-il d’être conforme à la réglementation ou toutes les autorités organisatrices des mobilités/transports devront passer du Netex profil Île-de-France au Netex profil France ?**

L’ensemble des acteurs qui ont une obligation d’ouverture de données sur des services réguliers, devront nécessairement, pour se conformer au cadre juridique en vigueur, fournir des données conformes au profil Netex France. A noter, que l’ensemble des profils des normes européennes feront l’objet d’une prochaine publication sur transport.data.gouv.fr.



## Données temps-réel pour les transports en commun

### Formats

#### Quels sont les formats acceptés par le Point d'Accès National pour les données temps-réel ?

Le PAN supporte trois formats standards pour les données temps-réel :\
\
\- Le **SIRI** (Service Interface for Realtime Information) **Profil France**\
Le SIRI est une norme définie par le Comité Européen de Normalisation et correspond à la norme NeTEx pour le temps réel. Elle caractérise des services temps réel et est un format autoporteur. Ce format ne peut être que référencé sur le PAN.

\- Le **SIRI Lite Profil France**\
Le SIRI Lite est un sous-dérivé de SIRI. Les données sont servies via une API HTTP classique dans le format JSON, ce qui peut le rendre un peu plus facile d'accès que SIRI (SOAP/XML). Ce format a pour objectif d'être complètement compatible avec le SIRI profil France et Île-de-France.

\- Le **GTFS-RT** (General Transit Feed Specification - realtime)\
Ce format permet de récupérer toutes les données temps réel d’un réseau en une requête et doit être associé à un fichier théorique au format GTFS. Il peut être diffusé lorsque le producteur demande au PAN de faire proxy sur ses serveurs pendant quelques mois.\
\
Plus d'informations [ici](https://blog.transport.data.gouv.fr/billets/la-production-des-donn%C3%A9es-temps-r%C3%A9el-interview-avec-diff%C3%A9rents-producteurs-de-donn%C3%A9es/)

#### Quel format faut-il privilégier ?

Les données temps-réel conformes au profil France aux formats SIRI et/ou SIRI Lite sont à privilégier. Le format GTFS-RT est toléré si le producteur n'est pas encore en mesure de produire des données aux formats SIRI/SIRI Lite ou en complément de ces formats. \
Le GTFS-RT n'est pas un format autoporteur car il doit être associé à un fichier théorique au format GTFS pour être utilisé. Si vous produisez du GTFS pour vos données sur les horaires théoriques, nous vous recommandons de publier un flux temps-réel au format GTFS-RT. Si vous produisez du NETEX pour vos horaires théoriques, nous vous recommandons de publier un flux temps-réel au format SIRI.

#### Quel flux faut il privilégier dans le format GTFS-RT ?

Dans ce format, le flux le plus utilisé par les réutilisateurs des données publiées sur transport.data.gouv.fr est le ""TripUpdate"". Ce flux fait une mise à jour pour la journée du fichier sur les horaires théoriques (GTFS). Si vous avez la possibilité de ne plus publier qu'un flux, nous vous conseillons de commencer par cette information.

#### Quelle est la différence entre le SIRI-Lite et le SIRI ?

Le SIRI-Lite utilise le même modèle de représentation que SIRI mais l’interrogation des serveurs se fait en [REST](https://fr.wikipedia.org/wiki/Representational\_state\_transfer) et non pas en [SOAP](https://fr.wikipedia.org/wiki/SOAP), ce qui permet une intégration un peu plus facilitée.

#### Pourquoi vous ne diffusez pas d'informations temps-réel dans des formats propres aux collectivités/opérateurs ?

L'objectif du PAN est de faciliter la réutilisation des données. Diffuser des données dans des formats propres aux collectivités et opérateurs complexifierait la réutilisation des données car le réutilisateur aurait à traiter différemment chaque flux. \
De plus, le Règlement Européen UE 2017 1926 encadre l'ouverture des données en fixant des formats par type de données. Pour le temps-réel les données doivent être conformes au Profil France de la norme SIRI ou SIRI Lite.

#### Quelles sont les exigences juridiques en matière de format pour la mise à disposition des données temps réel des transports publics collectifs?

Le règlement délégué UE 2017-1926, et l'article 25 de la loi d'orientation des mobilités, disposent de l'utilisation de la norme SIRI notamment pour les données en temps réel des transports publics collectifs. Cette norme se décline au sein de chaque Etat membre en un profil de la norme, c'est à dire un sous ensemble de la norme adapté aux spécificités de l'Etat considéré. Aussi, en France, il est ainsi attendu que ces données soient conformes avec le profil France de la norme SIRI (qui sera prochainement disponible sur la plateforme[).](https://normes.transport.data.gouv.fr/\).) A noter, l'exigence juridique porte spécifiquement sur la conformité à ce format là, quelque soit le protocole d'échange utilisé (SIRI ou SIRI Lite).

#### Peut on publier des données SIRI ou SIRI Lite au profil Île-de-France ?&#x20;

Le Profil Île-de-France est toléré si le producteur ne diffuse pas d'informations sur le suivi de fréquentation et le remplissage des véhicules. Dès lors que ces informations sont produites, les données doivent être au profil France.&#x20;

### Fréquence de mise à jour

#### Quelle fréquence de mise à jour recommandez-vous ?

Nous recommandons de ne pas aller au delà de 2 min pour mettre à jour une donnée pour que l'information fournie soit considérée comme étant en temps-réel, notamment pour la position du véhicule. Plus cette information est rafraîchie, plus elle est utile.&#x20;

#### **A terme y aura t-il un accord de niveau de service (SLA) exigeant un temps de latence maximal pour les producteurs ?**

Pour l’heure, il n’y a pas d’exigence particulière concernant le niveau de service. Il est en revanche naturel que le niveau de service proposé par les producteurs permette de fournir en temps utile les données aux réutilisateurs, et ainsi offrir aux voyageurs une information de qualité. \
Pour le flux vehicle\_position, nous recommandons par exemple de ne pas dépasser 5 secondes.&#x20;

### Production des données&#x20;

#### Peut on sous traiter la production des données théoriques et celles des données temps-réel à deux sociétés différentes ?

Vous pouvez sous-traiter la production de ces deux types de données à des délégataires distincts. Vous devez toutefois veiller à ce que les identifiants des arrêts et le calendrier soient exactement les mêmes entre le fichier théorique et le flux temps-réel.

#### Qu'est ce que je dois mettre dans mon cahier des charges lorsque je veux que mes données temps-réel soient référencées sur le Point d'Accès National ?

Nous vous recommandons de préciser dans votre cahier des charges : le format de données, à savoir du GTFS-RT ou du SIRI la diffusion des données, selon le format, sur le Point d'Accès National (GTFS-RT) ou un portail OpenData (SIRI ou GTFS-RT) par le producteur l'hébergement de votre flux temps-réel sur les serveurs du producteurs de données si vos serveurs ne peuvent pas supporter plusieurs requêtes par minute"

### Diffusion des données&#x20;

**Lorsqu'une collectivité délègue la production des données temps-réel : il vaut mieux que ça soit la collectivité, le délégataire ou le système d’aide à l’exploitation et à l’information voyageur (SAEIV) qui se charge de la publication ?**

Pour faciliter la gestion de la qualité des données, nous préférons qu'il y ait les mêmes interlocuteurs pour les horaires théoriques et pour le temps-réel. Si la collectivité délègue la production de ses données mais qu’elle veut publier elle-même ses données, nous recommandons à la collectivité de donner accès à son espace organisation de data.gouv.fr à son délégataire ou son SAEIV et de nous transmettre leurs coordonnées. Ainsi, si il y a des erreurs dans les jeux de données ou qu'ils ne sont plus à jour, nous pourrons contacter directement le producteur en mettant la collectivité en copie du mail.&#x20;

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

#### Pour diffuser des données au format SIRI, il faut un connecteur établi entre un producteur et un consommateur. Le producteur doit pouvoir reconnaître les réutilisateurs et gérer la totalité des consommateurs. Comment faire dans le cadre de la donnée ouverte et la diffusion sur transport.data.gouv.fr ?

Le producteur peut fournir des clés d'accès aux flux SIRI. \
transport.data.gouv.fr n’assure pas pour l’heure la diffusion de données SIRI. Nous nous contentons en effet de référencer l’API du producteur permettant l’accès à ces données. \
Nous recueillons toutefois actuellement les besoins pour bien comprendre les usages potentiels, et ainsi étudier la faisabilité d’un tel service.

### Proxy GTFS-RT&#x20;

#### Comment faire une demande de proxy pour mon flux GTFS-RT ?&#x20;

En attendant que le producteur soit en mesure de diffuser lui même ses données temps-réel, le PAN propose d'assurer temporairement la diffusion de ces données. \
Pour faire une demande, il suffit d'écrire à notre équipe à l'adresse [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr) et de suivre les étapes suivantes : \
\- Nous fournir une URL nous permettant d’accéder à des données au format GTFS-RT \
\- Nous vous transmettons une URL suivant le modèle : https://proxy.transport.data.gouv.fr/resource/nom\_aom\_gtfs-rt \
\- Cette URL est référencée en tant que ressource temps-réel en complément des données statiques GTFS pour les flux GTFS-RT par le producteur ou l'autorité organisatrice de la mobilité&#x20;

**Quelle est la durée de vie du proxy GTFS-RT et comment est elle définie ?**

Le service proxy est un service pérenne**.**

Le but du proxy est que le PAN assure la diffusion des données, en attendant que le producteur soit en mesure de les diffuser directement lui-même. \
Une fois que vos données seront diffusées avec une URL proxy, nous solliciterons les producteurs une fois par an afin de savoir si ils ont toujours besoin que nous fassions proxy.&#x20;

### Conversions

**Allez-vous proposer une conversion GTFS-RT vers le SIRI ?**

La conversion GTFS-RT vers le SIRI n'est pas encore proposé par [transport.data.gouv.fr](https://transport.data.gouv.fr) et nous ne prévoyons pas de le faire pour l'instant.

### Licences

#### Sous quelle.s licence.s sont publiées les données ?

Le choix de la licence est laissé à la discrétion du producteur de données. Le point d'accès national recommande toutefois l'utilisation de la licence ouverte pour les données en temps réel.





