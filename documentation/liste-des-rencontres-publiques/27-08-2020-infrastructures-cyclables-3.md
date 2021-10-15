# 27/08/2020 - Infrastructures cyclables #3

19 participants : Alexi Tourrand (Systra), Antoine (Angers), Benoît Chaumeret (Mairie de Paris), Cécile Rebout (département du Finistère), Axel Broman (contributeur OSM), Emmanuel ROCHE (Grand Chambéry), Dominique Harriague (AVAP), Fredercik Petit (Grenoble), Julien de Labaca (MobilityData), Léonard Vassord (Brest), Nicolas Madignier (Grand Poitiers), Michael Haüsle (SIOCA), Jean Vidal (association des citoyens du Seignanx), Elodie Lejeune (Ille-et-Vilaine), Simon Réau (Géovélo), Thomas Montagne (Vélo & Territoires), Julien Soubielle (Vélo & Territoires), Jeanne Astier (transport.data.gouv.fr), Miryad Ali (transport.data.gouv.fr)

Cet atelier a été co-animé avec l'association Vélo & Territoires. 



Pour rappel, ce schéma a été développé afin de **servir à l’information voyageur**. Il peut être utilisé pour alimenter OpenStreetMap (OSM) et à harmoniser les données des collectivités pour qu'elles puissent collaborer grâce à un standard commun. 

L'objectif du standard n'est pas de mettre toutes les informations. En effet,** il vise à renseigner les informations utiles aux réutilisateurs**. Les informations plus spécifiques aux territoires peuvent servir aux collectivités dans une logique patrimoniale, sans forcément être utiles pour l'information voyageur. **Les champs ont donc été définis pour répondre aux besoins des usagers et ce schéma est un tronc commun qui doit servir de base pour les collectivités**. 

**Résumé des étapes du projet : **

1\. enquête en ligne pour mettre en évidence les besoins : 8.06.2020 

2\. standard alpha : 8.07.2020 

3\. standard bêta : 18.08.2020 

4\. version standard 1.0, présentée lors de cet atelier du 27.08.2020, qui pourra encore évoluer. 

**1. Point sur les modifications qui ont été apportées **

Modifications réalisées en dehors des commentaires des participants : 

● Modification du nom des champs (plus d'accents, moins de 10 caractères) ; 

● Certains champs sont passés en liste de choix fermée (pour qu'il y ait un menu déroulant) ; 

● Les choix pour les champs booléens sont maintenant vrai/faux contre précédemment 0/1 ; 

● Suppression du champ « Pente » car c’est une donnée qu’on peut retrouver facilement et il fallait réduire le nombre de champ. 

Commentaires non intégrés et justifications : 

● Ajouter la rue piétonne dans les aménagements : Ce n’est pas un aménagement mais une zone apaisée ; 

● Ajouter un champ sur l'état du revêtement : Appréciation jugée subjective ; 

● Pour la date de mise en service : on garde l'année seulement au lieu de laisser le choix « jour/mois/année, mois/année, année » pour l'homogénéité. 

**2. Retour sur le schéma de données champ par champ après intégration des commentaires du groupe de travail **

_Les champs qui ont été laissés vide sont ceux qui n'ont eu aucune modification par rapport à la version alpha. _

● id : identifiant unique défini par le PAN 

Cet identifiant sera mis à jour si le segment n'a plus de correspondance. 

● id_osm 

Cet identifiant n'est pas pérenne, il peut changer dans OMS (OpenStreetMap). 

Simon de GéoVélo, le seul réutilisateur présent lors de cet atelier, souligne que ce champ est néanmoins important car il permet de faire le lien avec les données OSM. Il peut croiser pour mettre à jour les données. Il est donc préférable de garder ce champ en le laissant optionnel pour les collectivités qui saisissent leurs données sur OSM 

● id_local A laisser en optionnel car il permet aux collectivités de croiser avec sa base interne. 

● code_com Difficile de demander aux producteurs de données de la saisir manuellement. Il faudrait trouver un moyen pour que ce champ soit saisi automatiquement. Les territoires maritimes qui n'ont pas de code INSEE seront rattachés à la commune la plus proche à la main. 

● geoshape : La localisation est importante dans le cadre d'une intégration de la donnée cyclable au sein du référentiel voirie. L'objectif pour les producteurs de données est d'éviter d'avoir à faire deux fois le même travail. À poursuivre dans une réflexion sur la mise en place de ce standard en parallèle de la mise en place des données sur le réseau routier pour les collectivités. Ce champ peut être produit facilement à partir des outils (Qgis, Arcgis, par exemple, avec la table attributaire qui génère automatiquement un geoshape) 

● num_iti Ce champ référence le numéro des itinéraires européens, nationaux, régionaux et départementaux en lien avec le standard « Véloroute et voies vertes ». Le champ « reseau_loc » a été ajouté pour être complémentaire à ce champ 

● reseau_loc : Ce champ permettra de renseigner le nom et numéro des réseaux locaux : nationaux, régionaux 

● nom_loc 

Ce champ est complémentaire au champ reseau_loc et permet de renseigner les nom et numéros des réseaux locaux. 

Les champs suivants sont dupliqués à droite et à gauche (ou l’était dans la version bêta). On ne commente que ceux de droite mais les remarques valent aussi pour ceux de gauche. 

● ame_d : 

Les aménagements spécifiques à certaines collectivités ne peuvent être toutes renseignées. L’objectif est d'arriver à renseigner des aménagements qu’on retrouve dans plusieurs collectivités. Les aménagements spécifiques peuvent être indiqués dans « autre ». 

La zone 30 est une valeur qui peut être utile pour les réutilisateurs afin d’indiquer les rues peu fréquentées qui relient les aménagements cyclables. On reste toutefois sur une notion d'aménagement plutôt que d'itinéraire ou de continuité. Les collectivités peuvent adapter le standard localement à leurs besoins. 

● a_apaisee : 

Initialement « z_apaise_d », ce champ a été renommé ainsi afin de renseigner le régime de voie et inclure ainsi des données plus larges. 

La latéralisation de champ a été supprimé car cela augmente le nombre de saisie sans être une information pertinente. 

● sens_v_d : 

On supprime les recommandations du CEREMA pour la largeur des aménagements. 

● largeur_d : 

Il s’agit ici de la largeur minimale sur le segment. Le marquage n'est pas pris en compte. 

● conformité 

Suppression de champ. 

● statut 

Un aménagement "en projet" n'est pas une information utile pour l'usager. Cette valeur a donc été retirée de la liste des valeurs autorisées. 

La latéralisation de champ a été supprimé car cela augmente le nombre de saisie sans être une information pertinente 

● revetement 

Ce champ n’est pas utile à l’usager. Ce dernier a besoin de savoir avec quel type de vélo il peut rouler sur l’aménagement mais il n’a pas besoin de connaître le type de revêtement. 

● localisation 

Le mot localisation est ambigu. Cette information est importante pour l’appréciation de l’aménagement car les piétons n’ont pas accès aux aménagements sur la chaussée. 

Garder deux valeurs autorisées : sur le trottoir et sur la chaussée. 

● date_maj 

● trafic_vitesse 

● lumiere 

Un débat a eu lieu concernant le fait de préciser si la lumière est allumée ou non car il peut y avait des luminaires qui ne s’allument qu’à certaines heures, un certain moment de l’année etc.

Dans une logique de simplification, nous conserverons seulement le fait qu’il y ai un luminaire ou non.

● d_service 

● Comm 



**3. Les étapes à venir **

● Établissement du dictionnaire de données 

● Intégration d’une photothèque pour les différents types d’aménagements cyclables \
