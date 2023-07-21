# Lieux de covoiturage

{% hint style="info" %}
Savoir où l'on peut déposer ou prendre en charge des passagers constitue une information précieuse pour les covoitureurs. La connaissance des points de rencontre de covoiturage permet aux applications de covoiturage de fournir une information fiable sur les lieux où les conducteurs peuvent s’arrêter et stationner en toute sécurité.
{% endhint %}

La [base nationale des lieux de covoiturage](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/) (BNLC) recense les points de rencontre où les conducteurs peuvent déposer et prendre en charge des passagers en toute sécurité. Il est sous format .csv encodé en UTF8.\
Ce format a été défini en concertation avec Etalab, Open Data France, la ville de Paris et l'Agence d'aménagement et d'urbanisme de Corse. Le [schéma national des lieux de covoiturage](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/) a été publié par Etalab. Le schéma et la [BNLC](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/) sont maintenus par l'équipe de transport.data.gouv.fr.&#x20;

Ce jeu de données est sous [licence ODbL](https://doc.transport.data.gouv.fr/presentation-et-mode-demploi-du-pan/conditions-dutilisation-des-donnees/licence-odbl#conditions-particulieres-dutilisation).

{% hint style="warning" %}
Les producteurs de données ne doivent référencer que les lieux de rencontre assurant la sécurité de prise en charge des passagers, au regard notamment de leur accessibilité par voie piétonne.
{% endhint %}

La première base a été publiée en septembre 2019. Elle rassemblait les données publiées par [BlaBlacar](https://www.data.gouv.fr/fr/datasets/aires-de-covoiturage-en-france/) et la [Fabrique des Mobilités](https://www.data.gouv.fr/fr/datasets/aires-de-covoiturage-base-de-donnees-commune-des-lieux-et/). Plusieurs départements, villes, régions, covoitureurs et entreprises comme [Vinci Autoroute](https://doc.transport.data.gouv.fr/notre-ecosysteme/les-facilitateurs) ou [Rézo Pouce](https://doc.transport.data.gouv.fr/notre-ecosysteme/les-facilitateurs) ont contribué à la [BNLC](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/) depuis sa création.&#x20;

#### Comment les données sont ajoutées dans la Base nationale des lieux de covoiturage

\
Les contributeurs, peuvent transmettre directement les données relatives aux lieux qu’elles considèrent pertinents pour les covoitureurs en utilisant l'outil d'aide à la contribution : [https://contribuer.transport.data.gouv.fr/](https://contribuer.transport.data.gouv.fr/) ou en nous écrivant à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr). Plus d'informations sur les différentes manières de contribuer à la Base nationale des lieux de covoiturage [ici](https://doc.transport.data.gouv.fr/producteurs/lieux-de-covoiturage/contribuer-a-la-base-nationale-des-lieux-de-covoiturage#utiliser-loutil-daide-a-la-contribution-contribuer).\
Transport.data.gouv.fr réalise une consolidation régulière des fichiers déposés sur l'outil Contribuer, sur data.gouv.fr avec le mot-clé (tag) _**covoiturage**_ ou envoyés par mail dans la BNLC.&#x20;

#### Mise en qualité des données&#x20;

Avant de transmettre vos données, nous vous encourageons à évaluer leur qualité avec les outils suivants : &#x20;

* [le validateur de Transport.data.gouv.fr](https://transport.data.gouv.fr/validation?type=etalab%2Fschema-lieux-covoiturage)
* [Validata](https://validata.fr/table-schema?schema\_name=schema-datagouvfr.etalab%2Fschema-lieux-covoiturage)

{% hint style="warning" %}
Seules les données ne contenant aucune erreur seront intégrées à la BNLC.&#x20;
{% endhint %}

#### Ressources

* [Documentation du schéma](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/latest/documentation.html)
* [Répertoire git du schéma](https://github.com/etalab/schema-lieux-covoiturage)&#x20;
* [Licence de réutilisation des données : ODbL](https://doc.transport.data.gouv.fr/presentation-et-mode-demploi-du-pan/conditions-dutilisation-des-donnees/licence-odbl)

#### Historique

* [Un fichier national décrivant les aires de covoiturage de 70 départements](https://www.data.gouv.fr/fr/datasets/aires-de-covoiturage-en-france) a été consolidé par BlaBlaCar en 2018 à partir des fichiers disponibles sur data.gouv.fr et sur les différents sites des départements français.
* La Fabrique des Mobilités a également ouvert un fichier relatif à des lieux de rencontre de covoiturage (grande variété de points, fichier non consolidé), disponible [ici](https://www.data.gouv.fr/fr/datasets/base-de-donnees-commune-des-lieux-et-aires-de-covoiturage/), notamment grâce à un formulaire ouvert au grand public permettant de déclarer des points de rencontre pertinents.
* En 2019, Etalab, Open Data France et le Ministère chargé des transports proposent un [schéma amélioré](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html) pour garantir la disponibilité d'une base nationale consolidée qui puisse être facilement mise à jour.

