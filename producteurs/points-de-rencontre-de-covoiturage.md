---
description: Base nationale des lieux de covoiturage
---

# Points de rencontre de covoiturage

{% hint style="success" %}
Savoir où l'on peut déposer ou prendre en charge des passagers constitue une information précieuse pour les covoitureurs. La connaissance des points de rencontre de covoiturage permet aux applications de covoiturage de fournir une information fiable sur les lieux où les conducteurs peuvent s’arrêter et stationner en toute sécurité.
{% endhint %}

Un [format de référence](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/latest.html) pour la publication de points de rencontre de covoiturage a été défini en concertation avec Etalab et Open Data France. 

Une [base nationale ](https://transport.data.gouv.fr/datasets/base-nationale-consolidee-des-lieux-de-covoiturage/)expose désormais ces lieux. 

### Comment faire apparaître les lieux de covoiturage de son territoire dans la base nationale 

Le Point d’accès national aux données de transport réalise en lien avec les équipes de la plateforme data.gouv.fr une consolidation régulière des fichiers déposés sur data.gouv.fr avec le mot-clé \(tag\) _**covoiturage.**_

#### Étapes à suivre : 

* Référencer les lieux de covoiturage de son territoire [en suivant la documentation technique](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/latest/documentation.html). Le fichier doit être en format _.csv_.

{% hint style="info" %}
Vous pouvez aussi utilisé [ce formulaire généré automatiquement](https://forms.validata.etalab.studio/?schema=etalab%2Fschema-lieux-covoiturage) à partir du schéma pour générer facilement des données valides.
{% endhint %}

* Vérifier la validité du jeu de données le jeu de données en utilisant [cet outil](https://validata.etalab.studio/table-schema?schema_name=schema-datagouv-fr.etalab%2Fschema-lieux-covoiturage&schema_ref=) ;
* Publier le jeu de données sur data.gouv.fr en utilisant le mot-clef "_**covoiturage**_" ;
* Transmettre un message à contact@transport.beta.gouv.fr pour confimer la publication et nous demander la consolidation de la base. 

### Ressources

* [Documentation du schéma](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/latest/documentation.html)
* [Répertoire git du schéma](https://github.com/etalab/schema-lieux-covoiturage) 
* [Formulaire de génération de données valides](https://forms.validata.etalab.studio/?schema=etalab%2Fschema-lieux-covoiturage)
* [Validateur de CSV](https://validata.etalab.studio/table-schema?schema_name=schema-datagouv-fr.etalab%2Fschema-lieux-covoiturage&schema_ref=)
* [Licence de réutilisation des données](../reutilisateurs/licence-odbl-et-conditions-de-reutilisation.md)

### Historique

* [Un fichier national décrivant les aires de covoiturage de 70 départements](https://www.data.gouv.fr/fr/datasets/aires-de-covoiturage-en-france) a été consolidé par BlaBlaCar en 2018 à partir des fichiers disponibles sur data.gouv.fr et sur les différents sites des départements français.
* La Fabrique des Mobilités a également ouvert un fichier relatif à des lieux de rdv de covoiturage \(grande variété de points, fichier non consolidé\), disponible [ici](https://www.data.gouv.fr/fr/datasets/base-de-donnees-commune-des-lieux-et-aires-de-covoiturage/), notamment grâce à un formulaire ouvert au grand public permettant de déclarer des points de rencontre pertinents.
* En 2019, Etalab, Open Data France et le Ministère chargé des transports proposent un schéma amélioré pour garantir la disponibilité d'une base nationale consolidée qui puisse être facilement mise à jour.

### Foire aux questions

#### Comment le schéma a-t-il été conçu ?

Le schéma découle de nombreuses discussions avec les parties-prenantes \(collectivités, réutilisateurs, etc\) lors de deux ateliers organisés par les équipes de transport.data.gouv.fr. Il a été pris en compte les contraintes des producteurs et les besoins des réutilisateurs pour proposer le schéma le plus simple possible, permettant de décrire facilement des points de rencontre en covoiturage.

L'harmonisation des jeux de données facilite la tâche aux réutilisateurs, qui n'ont alors pas à réaliser des développements spécifiques pour chaque territoire qu'ils souhaitent intégrer à leur service, en gérant des formats ou des conventions de nommage différents. **Grâce au schéma proposé, une base nationale consolidée peut être mise à disposition pour valoriser les données ouvertes par les producteurs et accélérer le déploiement d'une information fiable pour les covoitureurs, partout en France.**

#### Qu'est-ce que l'identifiant unique ? A quoi sert-il ?

Mettre à disposition une base nationale consolidée présente de nombreux enjeux de qualité et de mise à jour des données. Afin de garantir une mise à jour facilitée de cette base, transport.data.gouv.fr a attribué un identifiant unique national à chaque lieu de covoiturage \(format "_**INSEE-C-000**_"\) pour faciliter la mise à jour des jeux de données existants. Ainsi, lorsqu'un producteur souhaite modifier une ligne décrivant un lieu de covoiturage, il peut signaler la modification 

#### **Ma collectivité a déjà publié un jeu de données, dois-je republier une base ?**

Grâce au travail des équipes de Blablacar en 2018 puis de celles de transport.data.gouv.fr, tous les jeux de données disponibles sur data.gouv.fr en juin 2019 ont été adaptés au schéma proposé ici. Cela signifie que si votre jeu de données avait déjà été publié, il y a de fortes chances que vous n'ayez rien à faire : les lieux de covoiturage de votre ressort territorial devraient déjà être inclus à la base nationale consolidée.

#### Je souhaite mettre à jour les lieux de covoiturage de ma base nationale consolidée.

Vous pouvez, au choix :

* transmettre un message à contact@transport.beta.gouv.fr pour nous demander la mise à jour ; 
* publier une version conforme au schéma sur data.gouv.fr en incluant le mot-clé "_**covoiturage**_" pour que le jeu de données soit identifié lors de la prochaine mise à jour. Attention : si les lieux de covoiturage existaient déjà, un identifiant unique leur a été attribué. Pour modifier la description d'un jeu de données existant, il vous faudra utiliser le même pour que la mise à jour soit prise en compte. Nous vous conseillons donc de partir de la base nationale la plus récente, d'en extraire les lignes correspondant à votre ressort territoriale, et à effectuer les modifications directement dans le fichier.

Nous nous efforcerons de faciliter votre travail au fil de vos retours pour rendre ce processus plus simple.

#### Je souhaite intégrer de nouveaux lieux de covoiturage

Si les lieux de covoiturage de votre ressort territorial ne sont pas référencés sur la base nationale consolidée, vous pouvez utiliser [le formulaire de génération de données valides](https://forms.validata.etalab.studio/?schema=etalab%2Fschema-lieux-covoiturage) ou le [validateur de CSV](https://validata.etalab.studio/table-schema?schema_name=schema-datagouv-fr.etalab%2Fschema-lieux-covoiturage&schema_ref=) pour créer un jeu de données conforme au schéma et le publier sur data.gouv.fr avec le mot-clé "_**covoiturage**_". Il sera intégré sous peu par les équipes de transport.data.gouv.fr dans la base consolidée.

**Qui réutilise cette base ?**

Cette base a vocation à être utilisée par les services de mobilité intégrant le covoiturage pour informer les usagers sur les lieux où ils peuvent s'arrêter pour déposer ou prendre en charge des covoitureurs, en toute sécurité. Les réutilisateurs de cette base peuvent déclarer leur réutilisation de manière volontaire sur la [page du jeu de données](https://transport.data.gouv.fr/datasets/base-nationale-consolidee-des-lieux-de-covoiturage/).

**J'ai d'autres questions sur cette base**

N'hésitez pas à nous contacter : contact@transport.beta.gouv.fr.







