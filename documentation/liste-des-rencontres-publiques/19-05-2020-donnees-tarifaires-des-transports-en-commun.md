# 19/05/2020 - Données tarifaires des transports en commun

**Compte-rendu de la rencontre publique transport.data.gouv.fr #23 consacrée à l’ouverture des données tarifaires des transports en commun**

### **Participants**

Producteurs de données de données transports en commun : 

* Ben Lister (Chargé de mission Open Data, Ville de Rennes et Rennes métropole)
* Cyril Kirche (Chargé de mission Open Data, Transdev)
* David Métayer (Consultant Manger à PwC en mission à Île-de-France Mobilités)
* Erwan Huon (Chef de projet Data, Keolis Rennes  )
* Frederick Petit (Project manager - opendata - transport, Grenoble Alpes Métropole)
* Gaël Chollet-Meirieu (Responsable données Open Data et information voyageur, SNCF)
* Jérôme Zuki (Chargé de mission transition numérique, Bordeaux)
* Léonard Vassord (Technicien territorial, Brest Métropole)
* Lise Paulus-Levet (Cheffe de projet Open Data, Grand Chambéry)
* Nicolas Madigner (Responsable data mobilité transport et développement numérique, Maas, Poitiers)
* Pauline Carquin (Responsable Open Data, Région Pays de la Loire)
* Sara Guillet (Chargée de projets - Service activateur des changements de mobilité  , Nantes Métropole)
* Séverine Ferrant (Responsable valorisation des données, Poitiers)
* Sven Baude (Responsable projets systèmes, Groupe Keolis)



Réutilisateurs de données transports en commun : 

* Christopher Do Nascimento (Project Manager, MyBus)
* Eric Fiere (Directeur innovation, Cityway)
* François-Xavier Aguessy (Back-end développeur, TheTreep
* Marielle Faure (Responsable de la collecte des données, HERE Technologies)
* Pascal Rhodes (Traitement métiers pour la collecte et distribution de l’information voyageur, Kisio)
* Raphaël Coin (CityMapper  )

Experts spécifications de données et animation de l'atelier : 

* Benoît Queyron (Chargé de mission, DGITM)
* Julien De Labaca (Consultant nouvelles mobilités, Mobility Data  )
* Laurent Chevereau (Maas et responsable données mobilité, CEREMA)
* équipe transport.data.gouv : 
  * Antoine Desbordes
  * Béatrice Mercier
  * Francis Chabouis
  * Miryad Ali
  * Nicolas Berthelot

**Présentation de transport.data.gouv **

Présentation déroulée en séance disponible à [ce lien](https://docs.google.com/presentation/d/17-xgbFM1ke9673FFbRnJvPjPQ0V5Whjqj2NEsucEdco/edit?usp=sharing). \
Pour plus d’informations sur transport.data.gouv.fr, vous pouvez consulter [le guide publié ici](https://doc.transport.data.gouv.fr).

### Etat des lieux

Les informations tarifaires sont spécifiques à chaque ville, bien qu'on retrouve certains champs communs comme la durée du trajet, les interconnexions possibles etc. Il n’y a pas d’homogénéité dans les types de titres de transports proposés à l’échelle nationale ou régionale.

Ces données sont difficiles à modéliser, notamment dans les grandes villes où il y a une diversité de gammes tarifaires (IDFM : ticket t+, ticket RER hors Paris, tarif moins de 10 ans, carnet de 10 tickets, réduction handicap etc.).



### Besoin des réutilisateurs

Certains réutilisateurs préfèrent modéliser eux-mêmes la donnée sans inclure les gammes tarifaires, comme CityMapper (GTFS) et Kisio (modèle interne), car les villes ne sont pas encore capables de modéliser ces types de données ou elles ne sont pas complètes.

Ces données sont importantes pour les réutilisateurs qui veulent inciter leurs usagers à prendre les transports en commun, notamment pour les trajets courts et occasionnels. Le fait de pouvoir fournir le prix, en plus de la durée du trajet, permettra d’influencer le choix des usagers.

Besoins :

* Avoir accès à des données tarifaires exhaustives car pour l’instant il n’y a pas encore assez de données pour pouvoir transmettre une information voyageur pertinente et fiable ;
* Avoir des données harmonisées car intégrer des formats différents serait chronophage ;
* Inclure une fonction billettique permettant d’acheter directement les titres de transport.

 Problématiques rencontrées :

* CityWay : intégration complexe car les villes veulent des offres tarifaires qui n’intègrent pas que les transports en commun mais toute ou partie de l’ensemble des mobilités : VLS, covoiturage, etc.)

Ces demandes rajoutent de la complexité dans la modélisation des offres et dans leurs intégrations pour pouvoir les rediffuser

### Les difficultés des producteurs de données 

Les données tarifaires ne sont pas structurées de la même manière : chaque système billettique a son format différent. Il sera donc difficile de produire des données identiques à partir d’un format établi car il faudrait homogénéiser des données venant de différents systèmes d’information sur plusieurs réseaux.

La recherche avancée sera compliquée à produire pour eux « Tarif pour >12 ans, dans telle région avec tel abonnement » par exemple.

Les villes de Nantes et Grenoble fournissent les données tarifaires dans leur GTFS grâce aux fichiers _fare_attributes.txt_ et _fare_rules.txt_ qui sont des fichiers optionnels du [format GTFS](https://developers.google.com/transit/gtfs/reference?hl=fr). La ville de Nantes a intégré des données tarifs classiques et spécifiques avec la navette pour l’aéroport. Elles ont intégré ces données à la suite d’une collaboration avec Google Maps. Ces données ont été produites à la main, ce qui a représenté un travail fastidieux et difficile reproductible de manière régulière.

Les producteurs de données ferroviaires se basent sur la gamme tarifaire kilométrique

 Besoins :

* Outil pour générer automatiquement la donnée car cela prendrait trop de temps pour la produire manuellement. Les logiciels qui sont en charge de la gestion des tarifs dans un réseau sont rarement que que les logiciels assistant l'exploitation. Il faudrait que ces logiciels permettent l'export d'informations intégrables de manière structurées dans un fichier NeTEx ou GTFS.
* Avoir accès à la base de données de la SNCF pour connaître le nombre de kilomètres entre chaque gare et leur matrice pour fixer les tarifs (Régions).

 Problématiques rencontrées :

* La mise à jour des données produites manuellement,
* Les données renseignées par Nantes et Grenoble ne sont pas satisfaisantes car elles indiquent les prix les plus élevés, pour limiter les réclamations, ce qui ne rend donc l’offre attractive et fournit une information partielle.

### **Actions à venir**

* Inclure les développeurs des principaux logiciels/système d’information dédiées aux informations tarifaires dans la discussion - contact : deploiement@transport.beta.gouv.fr 
* Améliorer et adapter le format GTFS Fares pour pouvoir intégrer des systèmes billettiques complexes comme l’intégration des différentes gammes tarifaire (âge, statut, billet 24h, week-end etc.). Ainsi, la V2 partira des besoins des collectivités et des réutilisateurs : Initiative de MobilityData   \- contact : [julien@mobilitydata.org](mailto:julien@mobilitydata.org)
* Développer le  profil NeTEx France par le groupe GT7 - contact : [christophe.duquesne@aurigetech.com](mailto:christophe.duquesne@aurigetech.com)
* Participer à la simplification de la billettique à l’échelle régionale pour pouvoir modéliser plus facilement cette information ;
* Partager les détails de l'expérience de Grenoble et Nantes dans la création de leurs données tarifaires basiques sous la norme GTFS Fares ;
* Etudier la possibilité que transport.data.gouv développe un outil de création de données tarifaires basiques sous un standard GTFS et/ou NeTEx. 

****
