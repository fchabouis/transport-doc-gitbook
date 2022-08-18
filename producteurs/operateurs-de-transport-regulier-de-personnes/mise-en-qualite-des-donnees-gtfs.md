---
description: >-
  ou comment publier en open data des données de qualité afin de faciliter leur
  intégration dans des applications tierces et ainsi encourager les usagers à
  emprunter les transports en commun ?
---

# Mise en qualité des données GTFS

Pour mettre en valeur votre réseau de transport à travers les supports numériques, il est important que vos GTFS comportent un maximum d'information à caractère commercial (nom commerciaux des lignes et arrêts, couleurs des lignes, accessibilité des arrêts, tracés des itinéraires, coordonnées de l'agence commerciale etc.).

La présence de ces informations assure la cohérence de votre réseau par rapport à votre stratégie commerciale et de communication et est complémentaire de vos autres supports (fiches horaires dépliants, affichage aux arrêts, plans de réseaux et de lignes etc.).&#x20;

En renseignant ces informations, vous facilitez la réutilisation de données tout en restant maitre de la diffusion des éléments constitutifs de votre réseau. Vous permettez ainsi, à travers l'intégration de vos données dans des calculateurs d'itinéraires, de toucher une plus grande cible de voyageurs potentiels en leur offrant une information de qualité représentative de votre réseau.&#x20;

En effet, un GTFS ne sert pas uniquement à décrire vos horaires, il permet également de décrire au mieux votre réseau, ses lignes et ses arrêts notamment, à travers des champs spécifiques que nous allons voir dans la suite de ce document. &#x20;

* **Les couleurs des lignes**

A travers les champs `route_text_color` _et `route_color` _ du fichier [`routes.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#routestxt), vous pouvez renseigner les couleurs de vos lignes afin qu'elles apparaissent telles quelles dans les calculateurs d'itinéraires ou dans tout autre canal qui publierait des informations sur vos lignes. Ainsi, l'information est cohérente entre tous les supports : vos supports distribués sur le réseau et les supports numériques.&#x20;

Les codes couleurs sont à renseigner au **format hexadécimal**. Différents outils gratuits existent sur internet pour convertir simplement vos codes couleurs RGB en hexadécimal. &#x20;

_Exemple : #FFFFFF = blanc, #000000 = noir_&#x20;

* **Les noms des lignes**

Il existe deux champs disponibles dans le fichier [`routes.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#routestxt) du GTFS pour décrire les noms des lignes :&#x20;

&#x20;   \- le champ `route_short_name` ou “nom court”&#x20;

&#x20;   \- et le champ `route_long_name` ou “nom long”.&#x20;

Il est obligatoire d’en renseigner a minima l’un des 2, mais **nous vous préconisons de renseigner les 2.**&#x20;

En effet, ces 2 champs n’ont pas la même vocation :

* Le nom court va être utilisé lors de recherches d’itinéraires pour afficher les options possibles. Généralement il s’agit d’une lettre ou d’un chiffre.&#x20;

_Exemple “A” ou “1” ou encore “212”._&#x20;

* Le nom long en revanche, a vocation à être utilisé lorsque la liste des lignes apparaît, en vue d’obtenir sa fiche horaire par exemple. Il est donc important que ce nom soit le plus descriptif possible afin que les voyageurs s’y retrouvent facilement. Généralement, ce nom est le même que celui qui se trouve sur vos dépliants horaires distribués. Il se compose souvent de l’origine et de la destination de la ligne.&#x20;

_Exemples (réseau Bibus de Brest Métropole) :_&#x20;

&#x20;_- “Gare - Hôpital Cavale” pour les lignes couvrant une seule collectivité_&#x20;

&#x20;_- “PLOUZANE Bourg - BREST Hôpital Cavale” lorsque le périmètre de la ligne couvre plusieurs collectivités, on peut ajouter le nom des villes en questions pour donner un maximum de précisions au voyageur._

![](https://lh5.googleusercontent.com/e3cHKkiJuF\_98Mlwwu3sYi3WtbU99jrv\_SHa6GtQ260ZhrMBGsTdbiUG1roe5a-ea7na4EZsc1JHryRVvylgczMZF7ceJYNBxCJFrx0KQNv3pxLobpW5CgXWlYZKdUU5pNcURqVXfz5hjuQerQ)![](https://lh4.googleusercontent.com/Y7WI7-z8UA8pMn2KD\_HkkP8\_Zz0CupJCKL9EK6D0bHu8dYq5hgxqHKHIev\_duVXHb6dZUeii1s2WBqyJRmZ5NQGqLGGV2vQPEi4ZELH1nVlNMKSt--Uka9RVCMlsWFmNkgrKErC5o3g19jW1fQ)![](https://lh4.googleusercontent.com/udjC7dKVQ7up0NrN4Ho\_c2RBf\_3JC8M\_GXack-7rn72bKTBGPR\_\_zsvujQ1nOXTir0lJc9hoqjU7HWf7vBkv2v90wOimI6DQH7sQEFk24Hd-9FsN37qDErx-4dzXyJpuEDCqKL-Ai5fJu3GcbA)

_Illustration de l’utilisation des noms longs (1ère image) et courts (2ème et 3ème image) des lignes dans une application mobile (Source : Bibus de Brest Métropole)_

* **Les tracés des lignes**

Dans la mesure du possible, nous préconisons d'intégrer au fichier GTFS le fichier [`shapes.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#shapestxt) permettant de décrire le tracés des itinéraires de vos lignes. Ainsi, lors des réutilisations de votre fichier, les itinéraires proposés indiqueront les routes réellement empruntées et non pas des itinéraires calculés par le calculateur ou des itinéraires "à la volée" non représentatifs de la réalité.&#x20;

Attention, pour pouvoir être utilisé, il faut bien que les `shape.id` soient repris dans le fichier  [`trips.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#tripstxt).

* **Les informations sur votre agence commerciale**

Le fichier [`agency.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#agencytxt) permet de renseigner les informations relatives à votre agence commerciale à savoir :      &#x20;

&#x20;   \- l'url du site web si vous disposez d'un site dédié à votre réseau de transport _(`agency_url`)_

&#x20;   \- le nom commercial de votre réseau de transport _(`agency_name`)_

&#x20;   \- le numéro de téléphone dédié à la relation clients _(`agency_phone`)_

Ces informations sont ensuite reprises dans les différents calculateurs d'itinéraires afin d'être présentées aux usagers dans le cas où ils auraient besoin de plus d'informations. &#x20;

Il est possible de créer plusieurs agences dans votre GTFS. Ainsi, si vous avez des lignes régulières et des lignes TAD vous pouvez tout à fait créer deux agences distinctes et ainsi inscrire les 2 coordonnées différentes (site internet du réseau de bus et site internet de réservation du TAD par exemple, idem pour le numéro de téléphone). L'information voyageurs sera alors d'autant plus précise.

* **L'accessibilité des points d'arrêts pour les usagers en fauteuil roulant**

Le fichier [`stops.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#stopstxt) permet de décrire les arrêts : nom commercial, ID, coordonnées etc. Il permet également de décrire si l'arrêt est aménagé pour les usagers en fauteuil roulant grâce au champ `wheelchair_boarding`.&#x20;

3 caractéristiques sont possibles : \
\- `0 ou vide` : information non connue / non renseignée\
\- `1` : certains véhicules à cet arrêt peuvent accueillir un usager en fauteuil roulant.\
\- `2` : les usagers en fauteuil roulant ne peuvent pas monter à bord des véhicules à cet arrêt.

NB : attention, un arrêt peut être décrit comme étant accessible dans le GTFS, mais le véhicule qui dessert cet arrêt doit également être en mesure d'accueillir un usager en fauteuil roulant. Cette information peut être retrouvée dans le champ `wheelchair_accessible` du fichier `trips.txt` _**(cf. paragraphe suivant sur l'accessibilité du trajet)**_

* **L'accessibilité du trajet, à l'intérieur des véhicules, pour les usagers en fauteuil roulant**

Le champ `wheelchair_accessible` du fichier [`trips.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#tripstxt) _****_ permet de décrire si le véhicule utilisé sur le trajet (trip) autorise ou non les usagers en fauteuil roulant.

Les caractéristiques possibles sont :&#x20;

`0` ou vide : aucune information disponible concernant les aménagements pour usagers en fauteuil roulant pour le trajet.\
`1` : le véhicule utilisé pour ce trajet peut accueillir au moins un usager en fauteuil roulant.\
`2` : le véhicule utilisé pour ce trajet ne peut accueillir aucun usager en fauteuil roulant.

C'est en croisant les informations aux arrêts et dans les véhicules que le calculateur d'itinéraire peut proposer des itinéraires accessibles aux usagers en fauteuil roulant. **Nous encourageons donc vivement les producteurs de données à renseigner ces 2 champs pour fournir une information la plus juste possible aux usagers.**

* **La possibilité de transporter un vélo non démonté pendant le trajet**

Le champ `bikes_allowed` du fichier [`trips.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#tripstxt) _****_ permet de décrire si le véhicule utilisé sur le trajet (trip) autorise ou non le transport d'un vélo non démonté avec soi.

Les caractéristiques possibles sont :

`0` ou vide : aucune information disponible concernant les aménagements pour vélos pour le trajet.\
`1` : le véhicule utilisé pour ce trajet peut accueillir au moins un vélo.\
`2` : le véhicule utilisé pour ce trajet ne peut accueillir aucun vélo.

* **Le Transport à la Demande en ligne virtuelle**

Les champs `pickup_type` (montée à bord) et `drop_off_type` (descente du véhicule) du fichier [`stop_times.txt`](https://developers.google.com/transit/gtfs/reference?hl=fr#stop\_timestxt) _****_ permet de décrire si le passage du véhicule est à la demande ou non (autrement dit, s'il est nécessaire de réserver son trajet ou non).

Les caractéristiques possibles sont :

`0` ou vide : les usagers peuvent monter / descendre aux horaires standards.\
`1` : les usagers ne peuvent pas monter / descendre  du véhicule\
`2` : les usagers doivent téléphoner à l'agence pour pouvoir monter / descendre du véhicule\
`3` : les usagers doivent contacter le conducteur pour pouvoir monter / descendre du véhicule

En cas de réservation, les calculateurs reprendront le numéro de téléphone contenu dans le fichier `agency.txt`. Dans le cas où votre réseau dispose de lignes 100% TAD nous vous suggérons de les associer à une agence spécifique TAD afin de faire apparaitre directement le numéro de réservation et non le numéro générique de votre agence (voir ci-dessus le chapitre agence).

NB : ce sont également ces champs qui permettent de modéliser les ITL (Interdiction de Trafic Local) via une caractérisation du passage en "`1`".

* _**Plus de thématiques à venir (tarification...)**_
* _Pour plus d'informations, vous pouvez également lire les_ [_best practices_](https://gtfs.org/schedule/best-practices/) _référencées par Mobility Data._&#x20;
