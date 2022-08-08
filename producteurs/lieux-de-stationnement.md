---
description: Base nationale des lieux de stationnement (BNLS)
---

# Lieux de stationnement hors voirie

Savoir où se garer, connaître les modalités d'accès au parking, et pouvoir estimer le tarif de stationnement constituent des informations précieuses pour bien gérer un déplacement en voiture. La mise à disposition de ces informations sous format numérique facilite leur diffusion auprès des usagers. Par exemple, cela permet aux services de calcul d'itinéraire de proposer des itinéraires multi-modaux (proposant de combiner l'usage de la voiture individuelle aux transports en commun). \
\
Suite à une investigation de plusieurs mois auprès de différents producteurs et réutilisateurs de données de stationnement, l’équipe de transport.data.gouv.fr propose une solution simple et structurée pour la mise à disposition des données de parcs de stationnement en France : la [**base nationale des lieux de stationnement hors voirie**](https://transport.data.gouv.fr/datasets?type=private-parking).

{% hint style="info" %}
Retrouvez les données publiées sur Transport.data.gouv.fr dans [la tuile Stationnement hors voirie](https://transport.data.gouv.fr/datasets?type=private-parking).
{% endhint %}



**Pourquoi créer une base nationale des lieux de stationnement ?**&#x20;

À l'été 2019, nous avons fait le constat qu'une trentaine de villes en France avaient ouvert des données décrivant leur offre de stationnement, mais que ces données étaient peu réutilisées. Les ré-utilisateurs citaient deux obstacles à la réutilisation : l'hétérogénéité des formats des données ouvertes et une trop faible couverture du territoire par les données ouvertes. \
\
[La base nationale consolidée des lieux de stationnement hors voirie ](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-stationnement/)proposée par transport.data.gouv.fr répond aux difficultés rencontrées par les réutilisateurs de données : en harmonisant les données déjà ouvertes par les collectivités selon un schéma unifié et les regroupant dans une base unique, elle réduit le temps de travail pour intégrer ces données à des services tiers.&#x20;

La base présente plusieurs cas d'usage :

* Elle permet de mettre en avant l'offre de stationnement d'une collectivité en permettant à des services de calcul d'itinéraire d'intégrer ces données. Cela permet notamment à ces services de proposer des itinéraires multimodaux à leurs usagers, combinant voiture et transports en commun par exemple ;
* Elle peut servir également à apporter une plus grande transparence sur l'offre de stationnement existante dans une ville, les tarifs qui y sont pratiqués.

**Création du schéma unifié pour le référencement des données de stationnement**

La base est élaboré selon un [schéma de données](https://schema.data.gouv.fr/etalab/schema-stationnement/latest.html) qui a été défini en concertation avec différents acteurs du stationnement. Ce schéma a pour but de documenter les informations essentielles au déploiement de services comme le calcul d'itinéraire, et définit un "standard minimal" des informations à renseigner. Il est possible de convertir les données ainsi produites vers des formats plus riches comme le NeTEx.

Le schéma a été élaboré en concertation avec de multiples acteurs, spécialistes des données de stationnement dont 18 métropoles et collectivités territoriales, 8 opérateurs de parkings, 3 services réutilisateurs et des experts du stationnement dont la Fédération Nationale des Métiers du Stationnement (FNMS), Alliance for Parking Data Standardization (APDS), et le Centre d'études et d'expertise sur les risques, l'environnement, la mobilité et l'aménagement (CEREMA).

Le schéma est officiellement documenté sur la page [schema.data.gouv.fr](https://schema.data.gouv.fr/etalab/schema-stationnement/latest.html) et sur [GitHub](https://github.com/etalab/schema-stationnement/). \
\
**Comment ajouter mes données à la base nationale consolidée des lieux de stationnement ?**&#x20;

Dans la première phase de la création de la base, l'équipe de transport.data.gouv.fr a récolté l'ensemble des données de stationnement déjà ouvertes en licence ouverte, et a procédé à un travail d'harmonisation et d'agrégation des données pour produire une [première version de la base](https://www.data.gouv.fr/fr/datasets/base-nationale-des-lieux-de-stationnement/).&#x20;

Une fois la base créée, toute nouvelle agglomération qui souhaite se lancer dans l’ouverture d’une base décrivant les stationnements hors-voirie de son ressort territorial, est invitée à produire des données directement selon le schéma de la base nationale des lieux de stationnement.

L’équipe de transport.data.gouv.fr met à disposition des acteurs un [générateur CSV conforme au schéma de données](https://csv-gg.etalab.studio/?schema=etalab%2Fschema-stationnement), ainsi qu’un [validateur ](https://validata.etalab.studio/table-schema?schema\_name=schema-datagouv-fr.etalab%2Fschema-stationnement\&schema\_ref=)pour les collectivités qui voudraient créer le fichier par leurs soins. N'hésitez pas à nous contacter pour toutes questions via contact@transport.beta.gouv.fr.&#x20;

Une fois les données produites, les collectivités peuvent transmettre systématiquement, sous forme de tableau mis à jour, les données relatives aux parcs de stationnement publics, ou privés à usage public à l'équipe transport.data.gouv.fr, ou en publiant le tableau sous format CSV sur data.gouv.fr en indiquant le mot-clé `stationnement`.&#x20;

#### Réutilisation des données

La base nationale des lieux de stationnement est mise à disposition pour une libre réutilisation, conformément aux conditions stipulées par [licence ODbL](https://doc.transport.data.gouv.fr/reutilisateurs/licence-odbl-et-conditions-de-reutilisation). Les réutilisateurs sont fortement encouragés à contacter l'équipe transport.data.gouv.fr pour faire part de leurs expériences de réutilisations, notamment pour nous aider à améliorer les données disponibles.

**Qualité des données**&#x20;

Avant de publier les données, nous recommandons aux producteurs d'évaluer la qualité de leurs ressources en utilisant le validateur de fichier disponible dans l'onglet "Outils" > "Evaluer la qualité d'un fichier"> "Lieux de stationnement" de la page d'accueil de transport.data.gouv.fr : [https://transport.data.gouv.fr/validation?type=etalab%2Fschema-stationnement](https://transport.data.gouv.fr/validation?type=etalab%2Fschema-stationnement)\
![](<../.gitbook/assets/image (174) (1) (1).png>)
