---
description: >-
  Cette foire à question, produite avec Vélo & Territoire, répond aux questions
  les plus couramment posées depuis que le schéma national sur les aménagements
  cyclables a été publié.
---

# Foire Aux Questions

Cette foire à question a été élaborée à partir des questions qui ont été posées lors de la session Question/Réponses du Webinaire de Vélo & Territoires et celles posées sur le [GitHub dédié au schéma national des aménagements cyclables de transport.data.gouv.fr.](https://github.com/etalab/schema-amenagements-cyclables) Elle a pour objectif de répondre aux questions les plus couramment posées, depuis la publication du [schéma national des aménagements cyclables](https://github.com/etalab/schema-amenagements-cyclables), afin de faciliter la compréhension et la prise en main de ce schéma.   
Elle est classé par thématique :   
  
Elle sera mise à jour fréquemment de sorte à répondre aux nouvelles difficultés rencontrées par les producteurs et réutilisateurs des données produites à partir de ce schéma. 

## Numérisation

### Plage d'échelle recommandée 

#### Pour les producteurs, quelle est la plage d'échelle prévue, recommandée ou limite pour la numérisation ?

La plage d'échelle prévue recommandée est de 1:5000. C'est notamment celle qui est utilisée dans l['outil d'aide à la saisie de Vélo & Territoires](https://on3v.veremes.net/vmap/?mode_id=vmap&map_id=31&token=publictoken#).

### Code INSEE 

#### Comment renseigner les champs codes INSEE \(code\_com\_d et code\_com\_g\), notamment pour les cas d'aménagement traversant plusieurs communes ?

Une voirie pouvant faire office de limite communale, il est possible que l'aménagement cyclable de gauche et de droite n'aient pas le même code INSEE. Il convient alors de renseigner les code code\_com\_d et code\_com\_g en fonction. Un aménagement traversant plusieurs communes devra être scindé en autant d'objets géométriques, de manière à ce que chacun disposent des codes INSEE droite et gauches correspondants.

#### Le code INSEE attendu dans le champ code\_com correspond-il au code postal ?

Non, il s'agit de deux codes de 5 chiffres mais qui ne sont pas identiques. Contrairement au code postale, chaque commune dispose d'un et un seul code INSEE unique \(plus d'information : [https://www.insee.fr/fr/information/4316069](https://www.insee.fr/fr/information/4316069)\)

### Aménagements spécifiques

#### Un aménagement en site propre est-il considéré comme une voirie à part entière, et dans ce cas, quel axe de numérisation utiliser ?

Le schéma ne fait pas de distinction entre site propre et site partagé. Il prévoit que les aménagements qui jouxtent une voirie de circulation soient numérisés sur l'axe de cette voirie, et non sur leur axe propre. Toutefois, il n'existe pas toujours une voirie adjacente, ou cette voirie peut parfois être séparée par un terre-plein plus ou moins large. Dans ces cas là il est recommandé de numériser l'aménagement sur son axe propre. Cela peut classiquement concerner :

- Piste cyclable  
- Voie verte  
- Aménagement mixte piéton/vélo hors voie verte  
- Autre

#### Pour certains types d'aménagement, la notion de droite et de gauche n'a pas de sens, comment gérer les attributs de ces aménagements ?

Pour les aménagements sans voirie de circulation adjacente, et ceux dont le concept n'est pas déclinable en droite et gauche, cette notion de positionnement par rapport à la voirie n’est effectivement pas exploitable. Pour ceux là, il est donc recommandé de n'utiliser que la série de champs réservée à l'aménagement droit. Pour l'aménagement de gauche il reste toutefois à renseigner le champs insee\_com\_g \(qui peut être différent de insee\_com\_d si l'aménagement est à cheval sur une limite communale\), et choisir AUCUN comme type d'aménagement de gauche. \(champ ame\_g\).  
Cela concerne :  
  
- Piste cyclable  
- Voie verte  
- Aménagement mixte piéton/vélo hors voie verte  
- Vélorue

#### Les territoires qui localisent précisément leur aménagement, comme une piste cyclable à côté de la chaussée, et non au centre de celle-ci; comment peuvent-ils diffuser leur donnée dans le format proposé ?

Le schéma se veut le plus synthétique possible afin de faciliter sa prise en main. Vous pouvez préciser cette information dans le champ "comm" qui permet d'ajouter des remarques supplémentaires. La valeur "intermédiaire" a notamment été ajouté au champ permettant d'indiquer l'emplacement de l'aménagement sur la voie de droite et sur la voie de gauche "local\__d/local\__g" afin de modéliser les aménagements qui se trouvent entre le trottoir et la chaussée. 

#### Quel type d'aménagement spécifier pour les sections "mixtes partagés" telles que les routes forestières ou chemins agricoles qui ne sont ni des voies vertes, ni des pistes cyclables ?

Le schéma a pour vocation de recenser les aménagements cyclables uniquement, et ne s'intéresse pas aux autres types d'infrastructures. La liste des aménagements et leur description est disponible ici \([https://doc.transport.data.gouv.fr/producteurs/amenagements-cyclables\#amenagements-cyclables](https://doc.transport.data.gouv.fr/producteurs/amenagements-cyclables#amenagements-cyclables)\).

#### Ne serait-il pas intéressant de pouvoir également renseigner les aménagements de type stationnement vélo ou autre? Si oui faut-il les signaler dans l'attribut comm \(commentaire libre\) ?

Il n'est pas conseillé d'indiquer la présence d'aménagements dans le champ comm d'un tronçon d'aménagement cyclable. D'une part il ne s'agit pas réellement d'une information relative à l'aménagement, et s'agissant d'un élément ponctuel \(alors qu'un aménagement cyclable est linéaire\), il ne serait dont pas réellement localisable. Cette manière de procéder rendrait également difficile un requêtage de votre système d'information. Concernant les stationnements vélo, le mieux est de les renseigner dans une couche ou table spécifique. Actuellement un schéma de données des stationnements vélo est justement en cours de création. Pour plus d'information à ce sujet, vous pouvez prendre contact avec [transport.data.gouv.fr](https://transport.data.gouv.fr/). Des travaux sont également en cours pour la création d'un modèle de données des équipements des véloroutes.

### Gouvernance des doublons 

#### Comment sont gérés les potentiels doublons entre un aménagement saisi une première fois par un EPCI et une deuxième fois par un Département \(voire une 3ème fois sur OSM\) lorsque chaque collectivité reverse ses données sur la base nationale ?

{% hint style="info" %}
Réponse à venir
{% endhint %}

### Référentiel géographique 

#### Sur la base de quel référentiel géographique s'appuyer pour la numérisation ?

Chaque gestionnaire ayant ses propres habitudes, il n'y a pas de préconisation de référentiel géographique pour ce schéma. Cela peut être la BD Topo, OSM, une orthophotographie, etc. Toutefois, il est recommandé d'indiquer celui qui a été utilisé dans le champ ref\_geom.

#### Si l'on base la numérisation sur un référentiel comme la BD Topo dans lequel la voirie est généralement découpée en tronçons entre les intersections, est ce nécessaire de subdiviser les aménagements cyclables de la même manière ou faut-t-il les regrouper ?

L'important est que chaque tronçon d'aménagement cyclable soit homogène et continu. Dès lors il n'y a pas de contrainte particulière à subdiviser "trop" un aménagement. En revanche, il est fréquent que les aménagements cyclables soient interrompus au droit des intersections. Regrouper "trop" les tronçons pourraient entrainer une perte d'information sur ces discontinuités qui sont pourtant bien réelles.

### Collecte et production des données 

#### Est-il possible de collecter et renseigner les informations via un outil nomade sur le terrain ?

Le [WebSIG de Vélo & Territoires](https://on3v.veremes.net/vmap/?mode_id=vmap&map_id=31&token=publictoken#) peut théoriquement être utilisé sur tablette mais il nécessite une connexion permanente, ce qui n'est pas toujours possible. Pour un utilisateur de QGIS l'application[ QField ](https://qfield.org/)peut être une option intéressante. Elle permet en effet d'installer son projet sur un périphérique mobile sous Android, et de faire de la numérisation sur le terrain.

#### Dans le cas où mon SIG métier intègre déjà des données vélo structurés différemment, comment mettre en place ce nouveau schéma?

Tout dépend du format de votre jeu de données actuel. Dans le meilleur des cas une simple conversion pourrait suffire, mais peut être qu'il y a nécessité de modifier ou compléter la donnée de votre SIG actuel. Pour un conseil plus personnalisé, vous pouvez prendre contact avec Vélo & Territoires.

#### Pour les petites collectivités qui n'ont pas de compétence en géomatique ou SIG, que recommandez-vous comme outil pour déployer ce nouveau schéma ?

La manière la plus simple pour une petite collectivité sans SIG est d'utiliser le[ WebSIG de Vélo & Territoires](https://on3v.veremes.net/vmap/?mode_id=vmap&map_id=31&token=publictoken#). Accessible librement \(sous réserve d'être une collectivité et de faire une demande d'ouverture de compte\) il permet, sans compétence en géomatique, de procéder à la numérisation de son réseau cyclable, et de le maintenir à jour. Pour plus

#### Les collectivités sont-elles les seules à pouvoir produire de la données sur les aménagements cyclables au format du schéma ?

En complément du schéma de données, transport.data.gouv.fr a créé deux bases de données nationales des aménagements cyclables. Une première est effectivement alimentée par les jeux de données publiés en open data par les collectivité \(y compris celles qui utilisent le WebSIG de Vélo & Territoires pour la numérisation de leurs infrastructures\). La seconde reprendra la donnée présente dans OSM. A terme il est prévu de consolider ces deux jeux de données au sein d'une 3ème base unifiée. Dès lors, tout acteur même privé ou associatif peut contribuer à la base nationale, en contribuant à OSM.

#### Dans notre système d’information actuel, nous numérisons chaque aménagement sur son axe propre. Est-ce compatible avec le Schéma de données ?

Le choix de l’axe de numérisation est une question qui a longuement fait débat lors de la construction du schéma, entre les partisans de la solution la plus simple \(numérisation des aménagements sur l’axe de la chaussée de circulation\) et ceux favorables à la numérisation de chaque aménagement sur son axe propre. La première solution est celle qui a finalement été retenue. En cas d’aménagement numérisé sur son axe propre, il est toutefois possible d’utiliser le schéma de données. La distinction droite est gauche n’est dans ce cas plus utile puisque chaque aménagement a son propre objet géométrique. Le sens de numérisation doit correspondre au sens de circulation, et la description de l’aménagement sera saisie dans le bloc de données correspondant à l’aménagement de droite \(champs : ame\_d, largeur\_d, etc.\). S’agissant de champs obligatoires, le type d’aménagement de gauche devra comporter la valeur AUCUN et le code INSEE de gauche devra être rempli.  Pour plus de détail, se référer à la Notice de numérisation terrain.

## Itinéraires 

### Intégration des itinéraires 

#### Comment indiquer que plusieurs itinéraires de cyclotourisme transitent par un même aménagement cyclable ?

Deux champs sont prévus pour indiquer le passage d'itinéraire\(s\) : les champs nom\_loc \(nom de l'itinéraire utilisé localement\) et num\_iti \(numéro de l'itinéraire quel que soit le schéma dans lequel il est inscrit\). Pour les deux il est possible de saisir plusieurs références d'itinéraire en les séparant par le caractère " : " \(point-virgule\).

## Compréhension des champs  

### Choix de la typologie des informations à saisir 

#### Pourquoi le choix de la chaine de caractère pour les id, notamment avec l'id\_local plutôt qu'un Serial ou integer ?

Pour l'id\_local nous avons opté pour une chaîne de caractère car ce sont des identifiants propres à chaque collectivité qui seront renseignés : les collectivités peuvent avoir des identifiants par série, de longueur variables, alphanumériques etc.

#### Pour les champs contraints par une liste de valeurs, est-ce possible, si besoin, d'en ajouter d'autres ?

Oui, ce schéma a été conçu comme une base que chaque utilisateur est libre de compléter en fonction de ses propres réalités et besoins. Dès lors, si une valeur semble manquer, au moins deux solutions sont possibles :

* L'ajouter dans son propre système d'information géographique
* Soumettre sa proposition aux autre utilisateurs du modèle pour que la modification intègre éventuellement une prochaine mise à jour du schéma et profite à toute la communauté \([https://github.com/etalab/schema-amenagements-cyclables/pulls](https://github.com/etalab/schema-amenagements-cyclables/pulls)\)."

### Niveaux de réalisation des aménagements 

#### Est-il prévu de renseigner les aménagements cyclables programmés, ou bien seulement ceux qui sont déjà en service ?

Ce schéma a été conçu comme une base que chaque utilisateur est libre de compléter en fonction de ses propres réalités et besoins. Les champs statut\_ame\_d et statut\_ame\_g sont prévus pour renseigner le niveau de réalisation de l'infrastructures, avec les valeurs possibles suivantes : "En travaux", "En service", "Provisoire". Pour de la planification, un gestionnaire d'aménagement peut ajouter d'autres valeurs telles que "En projet" dans sa base interne mais ces ajouts ne sont pas destinés à être renseignés dans la base de données qui sera publiées sur[ transport.data.gouv.fr](https://transport.data.gouv.fr/).

### Champ calculé

#### Pourquoi le schéma ne prévoit-il pas de champ calculé, tel que la longueur des tronçons ou leur pente ?

  
Le schéma prévoit un certain nombre d'informations de base et est un compromis entre simplicité de mise en œuvre et exhaustivité. Il ne comprend effectivement pas de champ dérivé \(issus de calcul\). Toutefois chaque producteur de données peut ajouter les champs correspondant à ses besoins spécifiques. Et tout réutilisateur de ces données pourra aisément calculer les champs nécessaires à la définition d'un itinéraire par exemple, sur la base de l'attribut géométrique pour la longueur, et d'un modèle numérique de terrain pour la pente, etc.

## Lien avec OSM et le standard véloroutes et voies vertes 

### Articulation du schéma avec le standard véloroutes et voies vertes et avec OpenStreetMap \(OSM\)

#### Comment s'articulent le schéma de données aménagements cyclables et le standard des véloroutes et voies vertes ?

Chacun de ces modèles de données est indépendant et peut être mis en œuvre sur un territoire indépendamment l'un de l'autre. Toutefois, le champ num\_iti du schéma de données sur les aménagements cyclables est similaire au champ idi\_iti du standard des véloroutes et voies vertes, ce qui rend possible une jointure entre deux jeux de données.

#### Comment fonctionnera la synchronisation entre les données publiées au format du schéma et celles d'OSM ?

Les données issues d'OSM seront publiées sur [transport.data.gouv.fr](https://transport.data.gouv.fr/) par Géovélo avec une fréquence de mise à jour mensuelle.   
Il n'y a toutefois pas de remontées de données prévues par notre équipe ni celle de Vélo & Territoires de [transport.data.gouv.fr](https://transport.data.gouv.fr/) vers OSM.   
L'id\_osm permettra de faire une correspondance entre les données publiées sur transport.data.gouv.fr et celles publiées sur OSM. 

### Evolution des identifiants OSM 

#### comment gérer des évolutions des osm\_id : coupure ou fusion de différents éléments ? 

Les id\_osm pourront être mises à jour fréquemment. Ce champ reste toutefois optionnel. Si vous ne pensez pas pouvoir mettre à jour votre base de données de sorte à ce que que les id saisis dans la base publiée sur le [transport.data.gouv.fr](http://transport.data.gouv.fr/) soit conformes aux id d'OSM, nous vous invitons à laisser ce champ vide

## Réutilisation du schéma et des données produites à partir de ce schéma 

### Utilisation du schéma à l'international 

#### Est-il possible d'utiliser ce schéma de données dans un autre pays ?

Oui, l'ensemble des ressources et la documentation du schéma sont publiés et réutilisables librement \([https://github.com/etalab/schema-amenagements-cyclables](https://github.com/etalab/schema-amenagements-cyclables)\). En revanche la publication des données au Point d’Accès National aux données de transport et leur visualisation sur le WebSIG de Vélo & Territoires ne concerneront que les données du territoire français. Accès aux données 

### Accès aux données produites à partir du schéma 

#### Comment est-il possible de consulter les jeux de données d'aménagements cyclables publiés au format du schéma ?

En plus des éventuelles plateformes d'open data des collectivités concernées, deux solutions sont possibles pour accéder aux données 

* Le Point d’Accès National aux données de transport \([https://transport.data.gouv.fr/](https://transport.data.gouv.fr/)\) qui propose un moteur de recherche permettant d'accéder, entre autre, aux jeux de données d'aménagements cyclables
* Le WebSIG de Vélo & Territoires \([https://on3v.veremes.net/vmap/?mode\_id=vmap&map\_id=31&token=publictoken\#](https://on3v.veremes.net/vmap/?mode_id=vmap&map_id=31&token=publictoken#)\) qui permettra bientôt de visualiser l'ensemble des données publiées sur un fond cartographique et d'interroger les données attributaires"

### Réutilisation par des services tiers 

#### Les données issues du schéma pourront elles être réutilisées par des services d'informations voyageurs comme des calculateurs d'itinéraires ?

Ce schéma a été produit avec des producteurs mais également des réutilisateurs des données cyclables, comme Géovélo, afin de l'adapter aux besoins des services d'information voyageur. Le schéma et format choisis permettront donc d'intégrer ces données dans ces services, notamment dans des calculateurs d'itinéraires. Il n y aura aucun calcul intégré dans la base nationale. Toutefois, les producteurs de données peuvent fournir des informations sur la pente, l'altitude dans le champ ""comm"" qui est dédié à toute sorte de commentaires. Les réutilisateurs pourront quant à eux calculer les longueurs si ils le souhaitent"  


## Les outils et ressources prévus

### Outils de saisie et de conversion 

#### Quels outils sont prévus pour faciliter la prise en main et la mise en œuvre du schéma et où les trouver ?

Pour permettre la mise en œuvre du schéma par toutes les collectivités qui le souhaitent, quels que soient leurs moyens, plusieurs outils ont été mis en place :

* [Le WebSIG de Vélo & Territoire](https://on3v.veremes.net/vmap/?mode_id=vmap&map_id=31&token=publictoken#) qui permet à chacun, sans compétence particulière en géomatique/SIG, de numériser ou mettre à jour des données grâce à une interface cartographique simple. 
* Un [gabarit au format shapefile pour QGIS](https://github.com/etalab/schema-amenagements-cyclables/blob/master/tools/AC_TEMPLATE_SHP_QGIS_v0.3.0.zip), plus adaptés pour les collectivités travaillant déjà sous SIG, intégrant un formulaire de saisie des attributs.
* Un[ script SQL](https://github.com/etalab/schema-amenagements-cyclables/blob/master/tools/AC_SQL_POSTGIS_v0.3.0.zip) pour la création d’une base de données Postgres/PostGIS « vierge », structurée au format du schéma \(incluant la table des aménagements cyclables comprenant l’attribut géographiques, mais aussi les tables des valeurs possibles des champs concernés\), ainsi que le modèle conceptuel de données.

  L’ensemble de ces ressources est disponible sur le dépôt GitHub du schéma \([https://github.com/etalab/schema-amenagements-cyclables](https://github.com/etalab/schema-amenagements-cyclables)\). On y trouve également un guide de numérisation.

#### L'outil de numérisation du WebSIG de Vélo & Territoire est-il accessible aux collectivités non adhérentes à l'association ?

Oui, toute collectivité peut accéder à cet outil, en revanche il faut au préalable demander la création d'un compte auprès de Vélo & Territoires pour accéder aux outils d'édition. Pour plus d'information à ce sujet, vous pouvez prendre contact avec Vélo & Territoires.

### Ressources 

#### Quelles ressources sont prévues pour faciliter la compréhension du schéma ? 

Plusieurs ressources ont été publiées afin de faciliter la compréhension du schéma, à savoir : 

* Une [photothèque](https://doc.transport.data.gouv.fr/producteurs/amenagements-cyclables) pour faciliter l'identification des aménagements cyclables inclus dans les valeurs des champs "ame\__d /ame\__g"
* une documentation pour mieux comprendre le[ cadre juridique](https://doc.transport.data.gouv.fr/producteurs/amenagements-cyclables/cadre-juridique) autour de l'élaboration de ce schéma
* une version tableur du schéma `[mettre lien vers la version tableur]` pour faciliter la lecture du schéma 

### Outils pour échanger 

#### Quels sont les outils dont nous disposons pour échanger sur ce schéma et comment en privilégier un par rapport à un autre selon les thématiques ?

Slack est une plateforme de messagerie instantanée basée sur des canaux, comme Microsoft Teams. Les canaux sont souvent par thématiques, comme c'est le canal pour le Slack de [transport.data.gouv.fr](http://transport.data.gouv.fr/) où il y a un [canal dédié aux aménagements cyclables](https://transportdatagouvfr.slack.com/archives/C0178TC9JL9).   
  
  

![](../../.gitbook/assets/capture%20%281%29.png)

Tandis que [GitHub](https://github.com/) est un site web conçu pour fédérer et partager le code source d'un projet de développement d'application géré par plusieurs personnes. Il permet de suivre l’évolution des fichiers sources et de garder les anciennes versions sans rien supprimer.  
Toutes les versions du schéma sur les aménagements cyclable sont donc sauvegardées dans le [GitHub des aménagements cyclables](https://github.com/etalab/schema-amenagements-cyclables). 

![](../../.gitbook/assets/image%20%2899%29.png)

Nous recommandons d'utiliser GitHub au maximum pour poser des questions au sujet du schéma, remonter des difficultés rencontrées et[ proposer des améliorations du schéma](https://doc.transport.data.gouv.fr/producteurs/amenagements-cyclables/contribution-au-schema-sur-les-amenagements-cyclables) afin que l'ensemble de la communauté puisse en tirer profit. Les équipes de [transport.data.gouv.fr ](https://transport.data.gouv.fr/)et de Vélo & Territoires vous répondront.

## Licence 

#### Il est proposé à défaut une licence ODBL là où pour d'autre données le choix semble porter sur la LOV2. Pourquoi ce choix dans le cas présent ? Par nécessité d'héritage pour une donnée source en provenance de OSM ?

Toutes les données publiées sur [transport.data.gouv.fr](http://transport.data.gouv.fr/) sont soit sous licence ODBL soit sous licence ouverte. Les bases nationales seront par conséquent soumises à ces licences. Etant donné que les bases nationales rassembleront des données en Licence Ouverte et ODbL nous adopterons la licence ODbL, plus contraignante. Nous avons explicité notre compréhension de la licence ODbL sur [notre page de documentation](https://doc.transport.data.gouv.fr/reutilisateurs/licence-odbl-et-conditions-de-reutilisation). Les réutilisateurs auront pour responsabilité de partager en ODbL les améliorations qu'ils feront sur les données des bases nationales seulement si elles portent sur des objets de même nature, de même granularité et de même couverture géographique.

## Un schéma représentant les différentes BD modes actifs et leurs liaisons existe-t-il ?

A ce jour, il n'existe pas de tel schéma permettant de faire une liaison entre les aménagements cyclables avec des schémas permettant de décrire le réseau routier ou les trottoirs. Des travaux pourront être menés dans ce sens à l'avenir.

## Elaboration et évolutions du schéma 

### Elaboration et suivi du schéma 

#### Pourquoi avoir fait le choix de créer un nouveau schéma de données aménagements cyclables, plutôt que de modifier le standard des véloroutes et voies vertes ? Standardisation par le CNIG

Le standard des véloroutes et voies vertes a vocation à décrire des itinéraires de plusieurs centaines de kilomètres de long principalement en milieu rural, d'en suivre le niveau de réalisation et d'en permettre la promotion touristique \(notamment par France Vélo Tourisme\). Les producteurs de cette données sont principalement les départements et acteurs du tourisme. Pour les aménagements cyclables, l'enjeu se situe plutôt en zones urbaines \(même si ça n'est pas restrictif\), les décrire vise à répondre à des problématiques de mobilités et nécessite un degré de précision plus élevé. Ces informations sont principalement produites par les gestionnaires de voiries communales et intercommunales. Dès lors, décrire les itinéraires cyclables et les aménagements cyclables n'implique ni les même enjeux, ni les même acteurs et il a été jugé que répondre à ces deux besoins par un seul modèle de données risquait de complexifier nettement son utilisation et donc de compromettre son appropriation par le plus grand nombre.

### Standardisation par le CNIG 

#### Ce schéma sera t'il standardisé par le CNIG ?

A l'heure actuelle cela n'est pas prévu. Le CNIG a bien été consulté durant la démarche de création du schéma. Toutefois une de ses recommandations était que la numérisation des aménagements cyclables soit compatible avec le PCRS \(Le Plan Corps de Rue Simplifié\), ce qui impliquait donc un référencement géographique dit de "Classe A", de précision centimétrique. Dès lors, la numérisation du moindre aménagement imposait le recours à un géomètre. Les premières échéances des collectivités en matière de création de PCRS étant en 2026, et ce niveau de précision n'ayant pas de réelle plus-value sur l'information voyageur et le calcul d'itinéraire, le choix a été fait de rester sur l'idée d'un schéma simple à mettre en œuvre, déployable rapidement et ouvert au plus grand nombre.

### Amélioration du schéma 

#### Comment faire des propositions d'amélioration du schéma ?Comment est-ce qu'on s'assure que la structure reste stable sans que cela génère une surcharge permanente ?

Tout producteur ou réutilisateur peut contribuer à l'amélioration du schéma. L'objectif est de permettre à ce schéma de s'adapter aux besoins des parties prenantes. Un processus de vote sera mis en place pour que les modifications proposées conviennent à l'ensemble des partie prenantes. Ce processus de vote permet d'assurer une stabilité du schéma. Vous pouvez accéder au guide d'aide à la contribution ici `[mettre le lien]`





Pour toute autre question, nous vous invitons à les poser sur le [GitHub des aménagements cyclables](https://github.com/etalab/schema-amenagements-cyclables) sous forme d'[issue](https://docs.github.com/en/github/managing-your-work-on-github/creating-an-issue). 







