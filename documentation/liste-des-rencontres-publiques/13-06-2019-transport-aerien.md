# 13/06/2019 - Transport aérien

**13 participants** dont 4 membres de transport.data.gouv, la DGITM \(Ministère chargé des transports\), la DGAC, 2 représentants de l’UAF-AFA, BAR France, 2 représentants de Air France, IATA et la FNAM. 

### 1ère partie : présentation de transport.data.gouv.fr 

La présentation déroulée en séance est disponible à [ce lien](https://docs.google.com/presentation/d/1y75RlTOsBkPOECViADSanY48cmJIM8yvkvo_K4U7mVs/edit#slide=id.g5538c1917c_0_17). 

Pour plus d’informations sur transport.data.gouv.fr, vous pouvez consulter [le guide publié ici](https://doc.transport.data.gouv.fr).

Dans le cadre des travaux de l’équipe du Point d’accès national et de la mise en oeuvre de l’ouverture des données pour améliorer l’information dont disposent les voyageurs, l’équipe de transport.data.gouv.fr s’intéresse au référencement des données relative au transport aérien en Open Data. 

La rencontre du 14 juin 2019 dernier a été l’occasion pour l’équipe de rencontrer pour la première fois les acteurs de l’aérien, afin de présenter les obligations réglementaires d’ouverture de données prévues par le règlement délégué européen et le Loi d’Orientation des Mobilités, mais aussi de répondre aux questions des participants. Le périmètre défini pour l’ouverture des données concerne toute donnée nécessaire à l’information voyageur \(horaires de vols réguliers, de navettes, localisation des arrêts et point d’accès...\). \(Ceci exclut toute information personnelle touchant à l’identité des voyageurs.\)

Cette rencontre a permis d’identifier les responsabilités d’ouverture de la donnée des différents acteurs, et de définir une série d’actions à mener d’ici la prochaine rencontre, prévue début Octobre 2019.  

#### Principaux retours de la salle

* La DGAC a signalé qu’ils détiennent des données d’usage historisées et a demandé si ces données devraient être ouvertes sur le Point d’Accès National \(PAN\). La DGITM a rappelé que ces données ne sont pas couvertes par la réglementation européenne en vigueur  \(2017/1926\), mais que ces données constituaient certainement des “données d’intérêt général” telles que définies par la Loi Lemaire, et que ces données pouvaient être publiées sur data.gouv.

### 2ème partie: Présentation des données aériennes dont l'ouverture est nécessaire

L’équipe de transport.data.gouv a rappelé que les opérateurs de transport \(dans ce cas les compagnies aériennes ainsi que les opérateurs de services de bus navette à l’aéroport \) et les gestionnaires d'infrastructure \(comme les aéroports et les opérateurs des parkings aéroportuaires\) sont concernés par l’obligation d’ouverture des données nécessaires à l’information voyageur. 

Pour rappel, les données à référencer sur le PAN sont: 

* les informations relatives à l'accessibilité: 
  * horaires et routes des bus navettes qui relient la ville avec l’aéroport \( données théoriques et en temps réel\)
* les informations relatives à l’infrastructure: 
  * places de parking, bornes IRVE  \(données statiques et en temps réel\)
  * autres infrastructures dédiées au transport: services de location de voitures, stationnement vélo, scooters. 
  * cartographie de l’intérieur des aéroports: cheminement, accès, dépose minute, temps de correspondance \(statique et en temps réel\).
  * information d'accessibilité interne de l’aéroport \(escaliers électriques, ascenseurs, accès PMR\), données statiques et en temps réel 
* Les informations sur les lignes aériennes régulières
  * Horaires des vols théoriques 
  * Information des vols en temps réel  

#### Observations

* Le [règlement délégué \(UE\) 2017/1926](https://eur-lex.europa.eu/legal-content/FR/TXT/?uri=CELEX%3A32017R1926) et la [Loi d’Orientation des Mobilités](https://www.legifrance.gouv.fr/affichLoiPreparation.do;jsessionid=08B56417C6B7B2BD1AED3B94D5BA26C4.tplgfr35s_1?idDocument=JORFDOLE000037646678&type=contenu&id=2&typeLoi=proj&legislature=15) exige l’ouverture de données qui sont déjà existantes, et n’exige donc pas la création de nouvelles données \(avec l’exception des données d’accessibilité PMR, comme stipulé dans [l’article 10 de la LOM](https://www.legifrance.gouv.fr/affichLoiPreparation.do;jsessionid=08B56417C6B7B2BD1AED3B94D5BA26C4.tplgfr35s_1?idDocument=JORFDOLE000037646678&type=contenu&id=2&typeLoi=proj&legislature=15) qui prévoit que les gestionnaires d’infrastructures créent cette donnée pour décembre 2021\). 
* Sur les délais d’ouverture des données 
  * Sur les données statiques : le délai de référencement des ces données sur le PAN, fixé par le règlement européen, est décembre 2019
  * Sur les données en temps réel : le délai de référencement de ces données sur le PAN, explicité dans le projet de loi LOM, est décembre 2020.
* Sur le référencement des données dans d’autres Points d’accès nationaux au sein de l’Union: 
  * Le règlement européen prévoit que dans le cas ou les données explicitées ci-dessus auraient déjà été référencées dans un Point d’accès national autre, les acteurs ne sont pas tenus d’ouvrir leurs données dans un autre PAN. Dans ce cas, le PAN demandeur de la donnée devra référencer directement la donnée à partir du PAN détenteur de la donnée. 
* _Sur les données d'accessibilité \(Navette et parking\)_
  * La UAF signale qu’aujourd’hui les services de navettes vers l’aéroport sont des services privés et indépendants, mais il peut y avoir aussi des services commandités par les aéroports et gérés par des opérateurs. Dans ce deuxième cas, les données doivent être ouvertes dans le PAN.   
  * Sur les stationnement hors voirie, un premier format d’ouverture des données statiques a été développé par l’équipe de transport.data.gouv. Les parkings aéroportuaires \(opérés ou non par l’aéroport\) doivent ouvrir leurs données sur le PAN suivant ce format. 
  * Sur la disponibilité en temps réel des parkings, les parkings aéroportuaires sont aussi obligés à référencer ces données. L’équipe de transport.data.gouv travaille actuellement sur le format de référencement de ces données. 
* _Sur la cartographie des aéroports_
  * Le règlement stipule l’ouverture des données relatives au cheminement, accès, dépose minute, temps de correspondance, ascenseurs et escalators en statique et en temps réel de l’ensemble des “noeuds d’accès” dont les aéroports font partie. L’équipe a rappelé que cette ouverture peut permettre le référencement des boutiques sur Apple Plans ou autres applications, et peut ainsi accroître la visibilité des équipements offerts. 
  * L’UAF a signalé qu’il est possible que la donnée en temps réel sur les points d’accès ne soit pas disponible sur les petits et moyens aéroports, ainsi que le risque que ces données puissent être utilisées par des personnes mal intentionnées. L’équipe rappelle que la LOM prévoit les obligations des opérateurs des infrastructures de créer les données autour de l'accessibilité à horizon décembre 2021. 
* _Sur les données de billettique_
  * Les opérateurs aériens, étant dans un régime dit de “yield management”, ne sont pas tenus d’ouvrir leurs données tarifaires en temps réel dans le PAN
* _Sur l’information des vols programmées_ 
  * Les opérateurs aériens semblent les meilleurs interlocuteurs pour référencer cette donnée sur le PAN. Les données que les opérateurs transmettent à l’official airline guide \(OAG\) décrivant les horaires programmés par saison, seraient satisfaisantes. 
  * D’autre part, la COHOR \(association de coordination des vols en France\), organisme chargé de l’attribution des créneaux horaires aux compagnies aériennes peut être aussi un bon interlocuteur pour déterminer les formats d’ouverture des données de vols programmés. 
* _Sur l’information des vols en temps réel \(TR\)_
  * Les différents acteurs ont rappelé l’hétérogénéité des données en temps réel sur les vols. Plusieurs acteurs entrent en jeu \(tour de contrôle, aéroport, compagnie\) selon la donnée dont on parle \(il y a le retard anticipé avant départ, le retard à l’heure d’arrivée et le TR effectif constaté\).  
  * Selon l’article 11bis du Code des Transports, les opérateurs sont tenus de publier par voie électronique les retards et les annulations susceptibles d’ouvrir des droits aux usagers.
* _Sur la portée de la réglementation sur l’ouverture des données des vols_ 
  * La réglementation explicite que seules les données des vols intra-européens doivent être ouvertes sur le PAN. Cependant transport.data.gouv encourage les opérateurs aériens d’ouvrir l’ensemble des informations sur les vols programmés à partir et/ou vers la France. 
* _Sur les données relatives aux perturbations, en TR_ 
  * Les participants nous ont indiqué l’absence d’un fichier consolidé répertoriant l'ensemble des perturbations des vols \(peut-être à l’exception de CDG et Orly\). Ainsi, pour avoir une donnée complète sur ces perturbations, il faudrait que chaque acteur responsable de la perturbation transmette la donnée directement \(ex neige : contrôleur aérien\). 
  * Concernant le stockage de ces données dans le PAN, la DGAC a souligné que les données historisées sur les perturbations aériennes peuvent être une ressource précieuse pour le développement de potentielles réutilisations. 

### Prochaines étapes 

* L’équipe de transport.data.gouv va travailler avec les équipes techniques des différents acteurs sur la définition du format de référence, tant pour les données statiques, que pour les données en TR. Air France a d’ores et déjà publié un fichier décrivant les horaires de vol des compagnies Air France  KLM sur le Point d’Accès National, en plus des APIs ouvertes mises à disposition pour décrire les tarifs. 
* Concernant les aéroports, l’équipe va lancer un appel à manifestation auprès d’aéroports volontaires, souhaitant être accompagnés dans leur démarche d’ouverture des données à titre de pilote. Il est prévu de faire un retour d’expérience lors de la rencontre d’Octobre. 
* D’autres producteurs ou réutilisateurs pilotes qui nous lisent ici et qui ne se seraient pas manifestés peuvent nous contacter à contact@transport.beta.gouv.fr pour participer aux travaux.

