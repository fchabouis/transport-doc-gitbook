# 25/04/2019 - Stationnement

**33 participants** étaient présents dont : 4 membres de l’équipe transport.data.gouv.fr, 4 étudiants du Policy Lab de Sciences Po, la DGITM (Ministère chargé des transports) et : l’AFIREV, la FNMS, Anayet, la SAGS, GIREVE, Qucit, 2 représentants de la ville de Paris, la SAEMES, Here Technologies, Mappy, Cityway, Capgemini Invent, la SCET, Sarepo, ADP, la SMTC Clermont-Ferrand, Bordeaux Métropole, Lyon Parc Auto (au téléphone).

###  1re partie : présentation de transport.data.gouv.fr

Présentation déroulée en séance disponible à [ce lien](https://drive.google.com/file/d/1biFGWNHHwJU3sxuZiWhBZuztU-MbCtcV/view?usp=sharing). \
Pour plus d’informations sur transport.data.gouv.fr, vous pouvez consulter [le guide publié ici](https://transport-data-gouv-fr.gitbook.io). 

Dans le cadre des travaux de l’équipe du Point d’accès national et de la mise en oeuvre de l’ouverture des données pour **améliorer l’information dont disposent les voyageurs**, l’équipe de transport.data.gouv.fr s’est associée à des étudiants de Sciences Po pour investiguer le sujet de l’ouverture des **données de stationnement hors-voirie**. La rencontre du 24 avril 2019 dernier a été l’occasion pour l’équipe de rencontrer l’écosystème, de comprendre les besoins, et d’identifier un certain nombre d’acteurs pilotes volontaires pour co-construire une méthode d’ouverture des données satisfaisante à la fois pour les producteurs et les réutilisateurs. Le but de la démarche ? S’assurer que **le voyageur puisse connaître l’offre disponible (de manière théorique et en temps réel) de places de stationnement**, dans un premier temps en s’intéressant aux parkings hors-voirie avant d’étendre les travaux au sujet plus complexe du stationnement sur voirie. \


### 2e partie : présentation par l’équipe de Sciences Po d’un prototype de fichier unique national (FUN) des données de description / localisation des stationnements hors-voirie en France

Présentation déroulée en séance disponible [à ce lien](https://docs.google.com/presentation/d/1X91\_cwd-fBCxViK4TzZnNmhS_kNTxa6gJzhHHGUKVWI/edit?usp=sharing).

Les 4 étudiants du Policy Lab de Sciences Po se sont plongés dans le sujet de l’ouverture des données de stationnement  en partant de l’existant (et notamment des opérateurs et collectivités ayant déjà ouvert leurs données) pour proposer **une structure simple mais standardisée de fichier unique national (FUN)**. Ce fichier, qui ne concerne que les données statiques, pourrait **servir de base à toute nouvelle agglomération qui souhaiterait se lancer dans l’ouverture** d’une base décrivant les stationnements hors-voirie de son ressort territorial. 

La salle a émis plusieurs retours sur le fichier : 

* La FNMS se demande s’il est utile d’indiquer le nombre total de place de parking dans le FUN : les usagers ont-ils besoin de cette information ? Bordeaux Métropole et la ville de Paris soutiennent au contraire que cette information peut avoir une utilité (connaître la capacité du parking peut permettre d’écarter un parking lorsqu’il est presque plein – si les données dynamiques sont disponibles) et soutiennent leur ouverture puisque ces données ne sont pas considérées comme “sensibles”. Ce sont également des données qui pourraient servir aux collectivités dans le cadre de leur gestion territoriale (capacité installée de stationnement en centre-ville, analyse des besoin de parkings supplémentaires à partir de l’offre existante)
* Un manque du fichier identifié par Cityway est l’identifiant unique, qui permet de faire la jointure entre le temps réel et théorique et qui est nécessaire en cas de changement de nom du parking. 
* La SMTC Clermont-Ferrand relève que dans le FUN, il manque la connaissance du territoire, avec tout ce qui permettrait de vraiment comprendre les données, et notamment les flux (certains parkings ne sont pas pratiques, etc). Une solution possible serait également d’indiquer clairement la marge d’erreur possible sur le jeu de données, afin de donner l’information dans sa globalité et de prévenir les utilisateurs.
* Il est demandé de rendre la catégorie “Payant/gratuit” obligatoire dans le fichier car c’est une information demandée par les passagers. 
* Plusieurs intervenants soulignent la difficulté de traiter les données tarifaires en statique. 
* Plusieurs intervenants, dont Bordeaux Métropole et la ville de Paris, se disent à la recherche de ce type de fichier unique nationale avec identification unique. 
* Les réutilisateurs se disent intéressés par d’autres catégories obligatoires dans le FUN : nom du gestionnaire, places disponibles (sans tenir en compte des places réservées). 

| <p>Prochaine étape.<br></p><p>Nous proposons la mise en place d’un groupe de discussion pour discuter des détails de ce fichier unique national. L’équipe de transport.data.gouv.fr mettra en place les outils nécessaires à l’animation de ce groupe dans les prochains jours. L’objectif sera de déterminer, d’une part si le format proposé facilitera l’ouverture de données statiques de stationnement par les collectivités territoriales, et d’autre part, suite aux retours de réutilisateurs qui se portent volontaires pour intégrer rapidement les données mises à disposition à titre d’expérimentation au format FUN, si le fichier sera facilement exploitable par les réutilisateurs (notamment, si le fichier, actuellement au format .xml, pourra facilement être convertible au format GeoJSON).. <br></p><p>A ce titre, les réutilisateurs qui souhaitent se porter volontaire pour expérimenter l’intégration d’un premier fichier FUN peuvent prendre contact directement avec l’équipe transport.data.gouv.fr pour les prochaines étapes. </p> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

Certaines discussions ont porté sur des considérations relatives aux données dynamiques, non traitées dans le FUN :

* La FNMS rappelle que les données affichées par les gestionnaires de parkings ne sont parfois pas les données brutes telles quelles, car la gestion de place de secours pour les abonnés nécessite des ajustements sur l’information affichée publiquement. Certains opérateurs n’afficheraient également jamais que le parking est complet afin de s’assurer qu’il apparaisse sur les GPS. L’équipe transport.data.gouv.fr rappelle cependant qu’il convient de ne pas induire l’usager final en erreur et que l’ouverture des données concerne en général les données brutes (et non les données transformées par les opérateurs de parking). Une réflexion plus approfondie pourra être menée sur le sujet afin de diffuser des bonnes pratiques.
* La donnée temps réel doit être la plus légère possible, par exemple avec un identifiant, une donnée brute, et des informations quantitatives.

### 3e partie : ateliers thématiques

### Atelier “Juridique”

Les discussions ont principalement porté sur le cadre juridique en vigueur et à venir autour de l’ouverture des données de transport. 

* L’[article 1115 du code des transports](https://www.legifrance.gouv.fr/affichCodeArticle.do?cidTexte=LEGITEXT000023086525\&idArticle=LEGIARTI000030983043) oblige les “services réguliers de transport public de personnes et \[l]es services de mobilité” à ouvrir leurs données “librement, immédiatement et gratuitement en vue d'informer les usagers et de fournir le meilleur service, notamment en permettant l'organisation optimale des services de mobilité et des modes de transport.”
* L’absence de décret d’application de cet article a fortement ralenti la mise en œuvre de cette politique publique.
* Le [règlement européen 2017/1926](https://eur-lex.europa.eu/legal-content/FR/TXT/HTML/?uri=CELEX:32017R1926\&from=FR), qui est en cours de transposition en France ([projet de loi d’orientation des mobilités](http://www.assemblee-nationale.fr/dyn/15/dossiers/loi_orientation_mobilites)), étend l’obligation d’ouverture à l’ensemble des modes de transport, publics comme privés.

Les collectivités territoriales émettent des craintes sur la réutilisation de leurs données – il est cependant rappelé que le producteur de donnée n’est aucunement responsable de la réutilisation éventuelle des personnes obligées par une licence de réutilisation. 

| <p>Prochaine étape <br></p><p>Afin de lever les craintes des collectivités territoriales dans l’ouverture de leurs données, il est proposé de publier un guide pour y présenter notamment ce cadre juridique ainsi que les nombreux avantages induits par l’ouverture des données. </p> |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

### Atelier “Technique”

Les réutilisateurs présents soutiennent leur intérêt à ce que (1) les données de stationnement hors-voirie soient ouvertes ; (2) elles le soient dans un format le plus standard possible. 

#### Question du format de la donnée

Les normes existantes poussées par l’Europe (Netex, Datex) peuvent convenir, mais :

* Netex n’est pas opérationnel aujourd’hui et son profil français n’est pas encore défini ;
* Datex sert davantage à un usage “voirie” et n’est pas forcément adapté à l’alimentation d’applications de calcul d’itinéraire multimodal.

Plusieurs participants soulignent l’importance d’intégrer les** parkings relais **et leurs spécificités dans la réflexion autour d’éventuels standards.

La métropole de Bordeaux se demande si elle a un intérêt de répondre à la demande de l’APDS (Alliance for Parking Data Standards) qui a entamé un travail de standardisation des données. L’équipe transport.data.gouv.fr n’a pas encore d’avis tranché sur la question, mais propose de demander directement aux réutilisateurs si le format en construction par l’APDS convient effectivement pour l’alimentation d’un calculateur d’itinéraire. 

#### Question de l’identifiant unique

Les réutilisateurs représentés ne voient pas l’intérêt d’un identifiant unique, mais soulignent l’importance de l’**homogénéité des identifiants d’un même parking** pour pouvoir effectuer une jointure entre les données statiques et dynamiques. 

#### Question des tarifs

La donnée tarifaire est complexe : elle n’est pas statique (elle varie au moins deux fois par an, et peut dépendre de l’heure de la journée) et les modèles de tarification selon les villes sont très hétérogènes (modèles linéaires, modèles non progressifs…) 

La donnée brute n’est pas très intéressante pour une information voyageur claire. Elle n’a un intérêt que s’il y a un calculateur sur le prix final à payer pour une durée X dans le parking. Certains opérateurs possèdent ces modèles et donc on pourrait rediriger les clients vers ce calculateur. Cependant, les collectivités territoriales affirment que ces données doivent être ouvertes car elles existent. 

#### Sur les données géographiques des parkings. 

Les réutilisateurs soulignent l’importance de récupérer les données géographiques de l’ensemble des points d’entrée et sortie des parking. Le format qui s’y prête le mieux serait le format GeoJson. 

| <p>Prochaine étape <br></p><p>En partant des données et des formats existants, l’équipe transport.data.gouv.fr propose de tester avec les réutilisateurs pilotes l’intégration des données (particulièrement les données dynamiques) mises à disposition, et à partir de ces retours, on pourra proposer des lignes directrices et un aperçu des meilleurs pratiques aux collectivités territoriales et autres producteurs de données pour l’ouverture des leurs données dynamiques. <br></p><p>Sur la question des données tarifaires, il sera nécessaire d’effectuer un travail supplémentaire avec les réutilisateurs et les collectivités pour déterminer si l’on décide de les ouvrir, et proposer un format adéquat pour structurer ces informations complexes. </p> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

### Atelier “Economique”

Les collectivités présentes à l’atelier soutiennent que les données relatives à la description, disponibilité et localisation sont des **biens publics**, et que tout le monde peut trouver de l’intérêt à promouvoir l’ouverture des données, dont les gestionnaires de parking. En termes d’ouverture de données, l’important pour la collectivité n’est pas la rentabilité, mais simplement de pouvoir rentrer dans leurs frais. 

Les opérateurs de parking insistent cependant sur le coût de l’ouverture des données et aimeraient obtenir une indemnisation. Ils évoquent le coût de mise en place de capteurs (200 euros/place), qui ont, de surcroît, une durée de vie limitée. Les opérateurs ne voient pas l’intérêt de donner la donnée gratuitement alors qu’ils ont des accords bilatéraux avec des plateformes qui en plus leur apportent des affaires.

D’autres participants évoquent l’intérêt pour l’opérateur de l’ouverture de la donnée : **être visible dans le maximum d’applications**. 

Ainsi l’ouverture des données crée un nouveau modèle économique et induit inévitablement de nouveaux coûts et donc une nouvelle viabilité économique à trouver pour opérateurs et concessionnaires. Elle redéfinira aussi la relation avec les opérateurs/concessionnaires : le partage des données sera-t-il compensé par l’arrivée de nouveaux clients ?



#### Autres questions à explorer dans les prochains ateliers : 

* Comment faire la liaison entre une donnée du PAN et l'opérateur du service qui produit l'accès à ce service ?
* Comment gérer le stationnement dans des hubs multimodaux ?
* Comment mieux mettre en valeur les services de mobilité déployés grâce aux données ?
* Quels retours data un opérateur peut avoir. Interrogation sur son service ?
* En marge de la thématique "info.voyageur", possibilité d'archiver les données stationnement à des fins d'étude (pour des autorités publiques) ?

### 4e partie : prochaines étapes 

| <p>Prochaine étape <br></p><p>Conformément à l’approche transport.data.gouv.fr, nous souhaitons travailler dans un premier temps avec des acteurs pionniers, pour co-construire une première méthodologie d’ouverture de données et référencer de premiers fichiers sur transport.data.gouv.fr. En séance, ont manifesté leur intérêt : </p><ul><li>côté producteurs : Bordeaux Métropole, la ville de Paris, le SMTC Clermont-Ferrand, la SAEMES et la FNMS ;</li><li>côté réutilisateurs : Mappy, Cityway, Qucit et Here Technologies.</li></ul><p>D’autres producteurs ou réutilisateurs pilotes qui nous lisent ici et qui ne se seraient pas manifestés peuvent nous contacter à <a href="mailto:contact@transport.beta.gouv.fr">contact@transport.beta.gouv.fr</a> pour participer aux travaux. <br></p><p>Nous mobiliserons ces acteurs pilotes pour leur demander leur avis sur les différentes questions que nous nous posons, pour valider avec eux une première version du fichier unique national et pour assurer que les données ouvertes soient véritablement utiles et réutilisés. Bien entendu, les données des producteurs pilotes seront référencés en premier sur transport.data.gouv.fr, ce qui accroîtra leur visibilité.</p> |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
