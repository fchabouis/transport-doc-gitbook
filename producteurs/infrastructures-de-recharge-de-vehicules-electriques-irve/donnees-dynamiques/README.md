# Données dynamiques

### Contexte

Dans le but de constituer un répertoire national de données relatif à l’offre de recharge pour véhicules électriques, ouvert et accessible à tous, les aménageurs d’infrastructures de recharge pour véhicules électriques (IRVE), ou les personnes qu’ils désignent, doivent publier sur la plateforme data.gouv.fr les données pour tout point de recharge en service et ouvert au public.&#x20;

L’ouverture des données dynamiques relatives à l’état de fonctionnement et la disponibilité des points de recharge et de leurs connecteurs s’effectue selon les modalités définies par l’arrêté.&#x20;

* [Présentation du schéma de données](https://doc.transport.data.gouv.fr/producteurs/infrastructures-de-recharge-de-vehicules-electriques-irve/donnees-dynamiques/presentation-du-schema)
* [Illustration de cas d'usage](https://doc.transport.data.gouv.fr/producteurs/infrastructures-de-recharge-de-vehicules-electriques-irve/donnees-dynamiques/cas-dusage)

### Documents de cadrage technique

* [Définition et structure des identifiants attribués par l'Association Française pour l'Itinérance de la Recharge Electrique des Véhicules (AFIREV)](http://www.afirev.fr/fr/informations-generales/)
* [Schéma.data.gouv.fr](https://schema.data.gouv.fr/etalab/schema-irve/)

### Création d'un fichier de données conforme

Les données collectées doivent respecter un formalisme particulier (schéma de données) décrit sur [la section documentation](https://schema.data.gouv.fr/etalab/schema-irve/latest/documentation.html) de cette page.

Les données sont à remplir au format CSV, encodage UTF-8.

Pour être conformes, les données dynamiques doivent faire référence aux données statiques via la clé commune  “id\_pdc\_itinerance”.&#x20;

**Chaque nouvel état de fonctionnement ou de disponibilité d’un point de recharge (ou d’un de ses connecteurs) doit nécessairement entraîner la mise à jour des données dynamiques.**
