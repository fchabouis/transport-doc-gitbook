---
description: >-
  La diffusion des données pour les véhicules en libre-service (vélos,
  trottinettes, scooters, voitures etc.) est attendue au format GBFS sur
  transport.data.gouv.fr.
---

# Publier des données pour les véhicules en libre-service

Le General Bikeshare Feed Specification ([GBFS](https://github.com/NABSA/gbfs)) est le standard ouvert pour les offres de mobilité partagées, qui a été développé par des opérateurs publics et privés, des développeurs d’applications et des fournisseurs de solutions technologiques. Les données, rafraîchies à une fréquence définie par le producteur, permettent notamment de connaître :&#x20;

* La localisation des stations, lorsqu’il y en a L’état des stations (pleines ou vides), lorsqu’il y en a&#x20;
* Le niveau de disponibilité des véhicules&#x20;
* La tarification&#x20;
* La description des véhicules. &#x20;

L’harmonisation des données existantes, aujourd'hui disponibles sous différents formats propriétaires, est un enjeu majeur pour faciliter la réutilisation de ces données.

### Référencer un flux GBFS sur transport.data.gouv.fr

#### Pour référencer les données sur le Point d'Accès National, vous devrez :&#x20;

* Créer un compte [utilisateur](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan/creer-un-compte-utilisateur-sur-data.gouv.fr) et [organisation](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan/creer-une-organisation-sur-data.gouv.fr) sur data.gouv.fr puis [référencé une URL distante ](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan/publier-un-jeu-de-donnees/1.-methode-transport.data.gouv.fr)
* Publier au format GBFS en ne référeçant que le [gbfs.json](https://github.com/NABSA/gbfs/blob/master/gbfs.md#gbfsjson). Ce fichier permet de découvrir les [autres fichiers](https://github.com/NABSA/gbfs/blob/master/gbfs.md#files)
* Préciser la licence sous laquelle ces données sont diffusées : ODbL ou ouverte.

#### Nous recommandons également :

* D’utiliser au moins la [v2.0](https://github.com/NABSA/gbfs/blob/v2.0/gbfs.md) afin d’anonymiser au mieux les trajets des véhicules&#x20;
* D’utiliser la [v2.1](https://github.com/NABSA/gbfs/blob/v2.1/gbfs.md) pour les véhicules en free-floating&#x20;
* D'utiliser le [validateur GBFS](https://transport.data.gouv.fr/tools/gbfs/analyze) pour vérifier la conformité du flux. Un rapport de validation apparaîtra sur votre ressource une fois qu'elle sera publiée comme [ici](https://transport.data.gouv.fr/datasets/trottinettes-bird-bordeaux/)
* De ne ne pas exiger d'authentification, d'inscription ou de limites d'accès
* De rafraîchir les données à une fréquence inférieure ou égale à 1 minute, idéalement 10 secondes, pour le fichier free\_bike\_status
* De publier un jeu de données par ville.&#x20;

Si vous avez des questions, n'hésitez pas à nous solliciter à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)

