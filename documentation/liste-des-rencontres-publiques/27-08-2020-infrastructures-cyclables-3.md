# 27/08/2020 - Infrastructures cyclables #3

19 participants : Alexi Tourrand (Systra), Antoine (Angers), Benoît Chaumeret (Mairie de Paris), Cécile Rebout (département du Finistère), Axel Broman (contributeur OSM), Emmanuel ROCHE (Grand Chambéry), Dominique Harriague (AVAP), Fredercik Petit (Grenoble), Julien de Labaca (MobilityData), Léonard Vassord (Brest), Nicolas Madignier (Grand Poitiers), Michael Haüsle (SIOCA), Jean Vidal (association des citoyens du Seignanx), Elodie Lejeune (Ille-et-Vilaine), Simon Réau (Géovélo), Thomas Montagne (Vélo & Territoires), Julien Soubielle (Vélo & Territoires), Jeanne Astier (transport.data.gouv.fr), Miryad Ali (transport.data.gouv.fr)

Cet atelier a été co-animé avec l'association Vélo & Territoires.&#x20;



Pour rappel, ce schéma a été développé afin de **servir à l’information voyageur**. Il peut être utilisé pour alimenter OpenStreetMap (OSM) et à harmoniser les données des collectivités pour qu'elles puissent collaborer grâce à un standard commun.&#x20;

L'objectif du standard n'est pas de mettre toutes les informations. En effet, **il vise à renseigner les informations utiles aux réutilisateurs**. Les informations plus spécifiques aux territoires peuvent servir aux collectivités dans une logique patrimoniale, sans forcément être utiles pour l'information voyageur. **Les champs ont donc été définis pour répondre aux besoins des usagers et ce schéma est un tronc commun qui doit servir de base pour les collectivités**.&#x20;

**Résumé des étapes du projet :**&#x20;

1\. enquête en ligne pour mettre en évidence les besoins : 8.06.2020&#x20;

2\. standard alpha : 8.07.2020&#x20;

3\. standard bêta : 18.08.2020&#x20;

4\. version standard 1.0, présentée lors de cet atelier du 27.08.2020, qui pourra encore évoluer.&#x20;

**1. Point sur les modifications qui ont été apportées**&#x20;

Modifications réalisées en dehors des commentaires des participants :&#x20;

● Modification du nom des champs (plus d'accents, moins de 10 caractères) ;&#x20;

● Certains champs sont passés en liste de choix fermée (pour qu'il y ait un menu déroulant) ;&#x20;

● Les choix pour les champs booléens sont maintenant vrai/faux contre précédemment 0/1 ;&#x20;

● Suppression du champ « Pente » car c’est une donnée qu’on peut retrouver facilement et il fallait réduire le nombre de champ.&#x20;

Commentaires non intégrés et justifications :&#x20;

● Ajouter la rue piétonne dans les aménagements : Ce n’est pas un aménagement mais une zone apaisée ;&#x20;

● Ajouter un champ sur l'état du revêtement : Appréciation jugée subjective ;&#x20;

● Pour la date de mise en service : on garde l'année seulement au lieu de laisser le choix « jour/mois/année, mois/année, année » pour l'homogénéité.&#x20;

**2. Retour sur le schéma de données champ par champ après intégration des commentaires du groupe de travail**&#x20;

_Les champs qui ont été laissés vide sont ceux qui n'ont eu aucune modification par rapport à la version alpha._&#x20;

● id : identifiant unique défini par le PAN&#x20;

Cet identifiant sera mis à jour si le segment n'a plus de correspondance.&#x20;

● id\_osm&#x20;

Cet identifiant n'est pas pérenne, il peut changer dans OMS (OpenStreetMap).&#x20;

Simon de GéoVélo, le seul réutilisateur présent lors de cet atelier, souligne que ce champ est néanmoins important car il permet de faire le lien avec les données OSM. Il peut croiser pour mettre à jour les données. Il est donc préférable de garder ce champ en le laissant optionnel pour les collectivités qui saisissent leurs données sur OSM&#x20;

● id\_local A laisser en optionnel car il permet aux collectivités de croiser avec sa base interne.&#x20;

● code\_com Difficile de demander aux producteurs de données de la saisir manuellement. Il faudrait trouver un moyen pour que ce champ soit saisi automatiquement. Les territoires maritimes qui n'ont pas de code INSEE seront rattachés à la commune la plus proche à la main.&#x20;

● geoshape : La localisation est importante dans le cadre d'une intégration de la donnée cyclable au sein du référentiel voirie. L'objectif pour les producteurs de données est d'éviter d'avoir à faire deux fois le même travail. À poursuivre dans une réflexion sur la mise en place de ce standard en parallèle de la mise en place des données sur le réseau routier pour les collectivités. Ce champ peut être produit facilement à partir des outils (Qgis, Arcgis, par exemple, avec la table attributaire qui génère automatiquement un geoshape)&#x20;

● num\_iti Ce champ référence le numéro des itinéraires européens, nationaux, régionaux et départementaux en lien avec le standard « Véloroute et voies vertes ». Le champ « reseau\_loc » a été ajouté pour être complémentaire à ce champ&#x20;

● reseau\_loc : Ce champ permettra de renseigner le nom et numéro des réseaux locaux : nationaux, régionaux&#x20;

● nom\_loc&#x20;

Ce champ est complémentaire au champ reseau\_loc et permet de renseigner les nom et numéros des réseaux locaux.&#x20;

Les champs suivants sont dupliqués à droite et à gauche (ou l’était dans la version bêta). On ne commente que ceux de droite mais les remarques valent aussi pour ceux de gauche.&#x20;

● ame\_d :&#x20;

Les aménagements spécifiques à certaines collectivités ne peuvent être toutes renseignées. L’objectif est d'arriver à renseigner des aménagements qu’on retrouve dans plusieurs collectivités. Les aménagements spécifiques peuvent être indiqués dans « autre ».&#x20;

La zone 30 est une valeur qui peut être utile pour les réutilisateurs afin d’indiquer les rues peu fréquentées qui relient les aménagements cyclables. On reste toutefois sur une notion d'aménagement plutôt que d'itinéraire ou de continuité. Les collectivités peuvent adapter le standard localement à leurs besoins.&#x20;

● a\_apaisee :&#x20;

Initialement « z\_apaise\_d », ce champ a été renommé ainsi afin de renseigner le régime de voie et inclure ainsi des données plus larges.&#x20;

La latéralisation de champ a été supprimé car cela augmente le nombre de saisie sans être une information pertinente.&#x20;

● sens\_v\_d :&#x20;

On supprime les recommandations du CEREMA pour la largeur des aménagements.&#x20;

● largeur\_d :&#x20;

Il s’agit ici de la largeur minimale sur le segment. Le marquage n'est pas pris en compte.&#x20;

● conformité&#x20;

Suppression de champ.&#x20;

● statut&#x20;

Un aménagement "en projet" n'est pas une information utile pour l'usager. Cette valeur a donc été retirée de la liste des valeurs autorisées.&#x20;

La latéralisation de champ a été supprimé car cela augmente le nombre de saisie sans être une information pertinente&#x20;

● revetement&#x20;

Ce champ n’est pas utile à l’usager. Ce dernier a besoin de savoir avec quel type de vélo il peut rouler sur l’aménagement mais il n’a pas besoin de connaître le type de revêtement.&#x20;

● localisation&#x20;

Le mot localisation est ambigu. Cette information est importante pour l’appréciation de l’aménagement car les piétons n’ont pas accès aux aménagements sur la chaussée.&#x20;

Garder deux valeurs autorisées : sur le trottoir et sur la chaussée.&#x20;

● date\_maj&#x20;

● trafic\_vitesse&#x20;

● lumiere&#x20;

Un débat a eu lieu concernant le fait de préciser si la lumière est allumée ou non car il peut y avait des luminaires qui ne s’allument qu’à certaines heures, un certain moment de l’année etc.

Dans une logique de simplification, nous conserverons seulement le fait qu’il y ai un luminaire ou non.

● d\_service&#x20;

● Comm&#x20;



**3. Les étapes à venir**&#x20;

● Établissement du dictionnaire de données&#x20;

● Intégration d’une photothèque pour les différents types d’aménagements cyclables \
