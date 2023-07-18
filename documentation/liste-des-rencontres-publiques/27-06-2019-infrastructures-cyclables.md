# 27/06/2019 - Infrastructures cyclables

**24 participants** dont 5 membres de transport.data.gouv, la DGITM (Ministère chargé des transports), l’Association Vélo et Territoire, Géovélo, Fédération Française des Usagers de la Bicyclette (FUB), Fédération Française des Vélos, Association Paris en Selle, Contributeurs OSM, Association Mieux se déplacer en Bicyclette, Association Citoyen!, Ile-de-France Mobilités, Ville d’Angers, Ville de Paris, Ville de Strasbourg, CA Paris-Saclay, IGN&#x20;

### 1ère partie : Présentation de transport.data.gouv&#x20;

Présentation déroulée en séance disponible à [ce lien](https://docs.google.com/presentation/d/1QxEvqRXy99UuIjEzOZF84qaqQ18CsAdQ08oWOwLcCbI/edit?usp=sharing).&#x20;

Pour plus d’informations sur transport.data.gouv.fr, vous pouvez consulter [le guide publié ici](https://doc.transport.data.gouv.fr).

Dans le cadre des travaux de l’équipe du Point d’accès national (PAN) et de la mise en oeuvre de l’ouverture des données pour améliorer l’information dont disposent les voyageurs, l’équipe de transport.data.gouv.fr s’intéresse actuellement aux données relatives aux infrastructures cyclables.&#x20;

La rencontre du 27 Juin 2019 dernier a été l’occasion pour l’équipe de rencontrer pour la première fois les acteurs de cet écosystème, afin de présenter notre mission et notre démarche d’ouverture des données. Nous avons également rappelé le cadre normatif  d’ouverture existant (règlement (UE) 1926/2017) et à venir (notamment avec l’approbation de la Loi d’Orientation des Mobilités). Un élément notable est que le règlement européen n’exige la mise en open data que des données qui existent déjà dans un format lisible en machine, et non la création de ces données numériques.

### 2ème partie : Etat des lieux de l'ouverture des données de stationnement et d’aménagements cyclables&#x20;

L’équipe de transport.data.gouv a présenté le travail réalisé par une équipe d’étudiants de Sciences Po ainsi qu’un travail fait en interne pour établir un premier état des lieux sur l’ouverture des données relatives aux infrastructures cyclables. Les résultats nous permettent de faire un double constat :&#x20;

1. Peu de données relatives aux aménagements cyclables sont disponibles en open data et leurs structures sont hétérogènes. Il n’y a pas une typologie commune pour l’ouverture de ces données et il existe différentes nomenclatures pour une même catégorie.&#x20;
2. Open Street Map (OSM) référence aujourd’hui des données relatives à l’infrastructure cyclable grâce à du crowdsourcing. De part leur format unique et la réutilisation de leurs données par des applications comme Géovélo, certaines collectivités  (Montpellier ou Ile-de-France par exemple) créent leurs bases de données des infrastructures cyclables directement sur OSM avant de les exporter vers leurs portails Open Data.&#x20;

Simon Réau de Géovélo  et Thomas Montagne de Vélos et Territoires ont complété notre révision en présentant des démarches nationales et interurbaines existantes pour référencer les données des infrastructures cyclables. Au niveau inter-urbain, Ile-de-France, en partenariat avec Géovélo, s’est basé sur Open Street Map pour référencer les données des infrastructures cyclables dans le territoire. Au niveau national, l’association Vélos et Territoires est mandatée pour administrer une plateforme nationale recensant les principaux itinéraires inter-urbains et nationaux. Cette plateforme est alimentée en particulier grâce aux remontées des données départementales et régionales. Cette donnée est aujourd’hui disponible sous licence ouverte. L’association s’est rapproché d’OSM pour créer une méthodologie de comparaison des deux données, cependant la donnée référencée dans la plateforme Vélos et Territoires est bien la donnée officielle déclarée par les collectivités territoriales. \


**Les principaux retours de la salle:**&#x20;

* Les collectivités ont signalé que la licence ODBL constituait un frein pour utiliser les données d’OSM pour enrichir leurs bases de données ou pour faire du comparatif des données. L’équipe juridique de transport.data.gouv s’est précédemment penchée sur cette question et rappelle que sur transport.data.gouv.fr, une Condition Particulière d’Utilisation a été ajoutée à la licence ODbL, précisant :

> “la clause de partage à l’identique (article 4.4) concerne les informations de même nature, de même granularité, de même conditions temporelles et de même emprise géographique”
>
> (Le lien pour la documentation complète de transport.data.gouv sur la licence ODBL [ici](https://doc.transport.data.gouv.fr/presentation-et-mode-demploi-du-pan/conditions-dutilisation-des-donnees/licence-odbl#conditions-particulieres-dutilisation).)

### 3ème partie : Quels sont les besoins des réutilisateurs de données aujourd’hui ?&#x20;

Le premier besoin relevé par les réutilisateurs de la donnée est celui de l’exhaustivité et de la fiabilité de la donnée mise à disposition. Cette donnée peut servir à la fois des applications pour donner des itinéraires les plus fiables possibles, comme à des citoyens ou des associations pour soutenir des demandes pour améliorer les infrastructures existantes.  Dans ce cadre, un enjeu majeur est l’animation du processus de référencement des données auprès des petites collectivités locales, pour lesquelles les données n’existent ni dans OSM ni dans les fichiers des collectivités. Transport.data.gouv.fr rappelle que son rôle se limite à l’ouverture des données existantes et donc ne peut pas forcer les collectivités à créer des données. Cependant il encourage les collectivités à se saisir d’instruments innovants (tels que les cartoparties) et de la comparaison avec les données OSM afin de créer une base de données des infrastructures cyclables.&#x20;

Le deuxième besoin qui a été relevé est celui de la création d’un standard pour les données des infrastructures cyclables (format + structures des données). Dans cette ligne, l’équipe a demandé s’il était pertinent d’utiliser le format de données mis en place par Ile-de-France mobilités en partenariat avec Géovélo. Ce schéma a l’avantage d’être une modélisation OSM qui peut être exportée dans un format SIG. La salle a cependant rappelé certaines limites sur le modèle mis en place par Ile-de-France mobilités:&#x20;

* Pour les informations géographiques, c’est le CNIG qui définit les standards pour la normalisation de ces données. Cependant aucun travail a été réalisé par le Conseil dans ce sens, et certaines personnes de la salle ont exprimé leur préoccupation sur le délai de fixation d’un standard. &#x20;
* Il existe déjà un schéma national vélo, validé par le CIAT (Comité interministériel d’aménagement et de développement du territoire). Ce schéma réunit aujourd’hui les grands itinéraires cyclables nationaux. Un format qui englobe les données nationales, interurbaines et urbaines doit tenir compte du travail fait au niveau national.&#x20;
* Des villes ont aussi ont aussi insisté sur le fait que si les données d’OSM sont utiles aux collectivités, elles n’ont pas pour vocation de remplacer les données existantes dans leurs systèmes internes, mais de permettre de les comparer. Ainsi ils voient OSM comme un outil complémentaire pour établir une donnée plus fiable.&#x20;

### 4ème partie : Quels sont les besoins des producteurs de données aujourd’hui ?&#x20;

Aujourd’hui les collectivités s’interrogent sur quelles données doivent être ouvertes. En effet certaines collectivités ont aussi des données relatives aux projets de construction d’aménagement cyclables, en plus des données des aménagements existants. L’équipe de transport.data.gouv explique que,  idéalement, il faudrait créer deux jeux de données : un pour les infrastructures existantes (et qui donc constituent des informations pour les usagers de vélos) et un deuxième, optionnel, sur les projets.&#x20;

Les producteurs des données partagent la nécessité de créer un format unique et facile à ré-utiliser pour l’ouverture des données des infrastructures cyclables. Les producteurs se sont aussi demandé quels seraient les mécanismes de mise à jours de ces données.&#x20;

L’enjeu de la remontée d’informations par les usagers (équipements endommagés ou manquants, etc.), et de la prise en compte de ces informations a été soulevé à plusieurs reprises. Ces retours sont à la fois précieux et difficiles à prendre en compte par les collectivités.

Enfin, plusieurs collectivités ont souligné que les données d’infrastructures cyclables n’ont pas pour unique vocation d’être réutilisées par de tiers, mais qu’elles sont aussi très utilisées en interne, d’où la difficulté à ne se passer des logiciels “métier” classique (SIG etc.).\


### 5ème partie : OSM comme outil de saisie des données cyclables par défaut&#x20;

L’équipe de transport.data.gouv a demandé à la salle si le schéma suivant était pertinent, applicable à tous, sous quelles conditions et avec quelles limites : d’abord la collectivité saisit ses données cyclables dans OSM, puis des exports en sont fait. Le PAN exporterait automatiquement pour publication en open data sur la plateforme nationale, et les collectivités pourraient mettre en place leurs propres exports (pour leur portail local, le SIG etc.).

Certaines villes se sont montrées réticentes à donner à OSM une légitimité telle qu’elle devienne l’outil de saisie de leurs données cyclables. D’autres ont ajouté qu’OSM ne leur permettait pas de référencer correctement leurs aménagements cyclables et qu’ils préféraient donc avoir leur propre schéma.&#x20;

### Prochaines étapes&#x20;

L’équipe de transport.data.gouv a lancé un appel pour établir un groupe de travail sur l'ouverture des données des infrastructures cyclables. Se sont montrés intéressés les représentants de : IGN - Ville d’Angers - Ville de Strasbourg - Ville de Paris - Paris en selle - Géovelo - Ville et Territoires - MDB - Ville de Poitiers - Grenoble Métropole - OpenStreetMap France

L’objectif de ce groupe de travail est d’établir une proposition de schéma de publication et de standard pour les données relatives aux infrastructures cyclables.&#x20;

\
D’autres producteurs ou réutilisateurs pilotes qui nous lisent ici et qui ne se seraient pas manifestés peuvent nous contacter à contact@transport.beta.gouv.fr pour participer aux travaux.
