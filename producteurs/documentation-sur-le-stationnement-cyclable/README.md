# Documentation sur le stationnement cyclable

Dans le cadre des travaux de l’équipe du Point d’accès national et de la mise en œuvre de l’ouverture des données pour améliorer l’information dont disposent les voyageurs, l’équipe de transport.data.gouv.fr propose une solution simple et structurée pour l’ouverture des données sur les équipements de stationnement cyclables : la Base Nationale du Stationnement Cyclable (BNSC). Elle s’adresse à toute collectivité qui souhaite se lancer dans l’ouverture d’une base décrivant ses équipements de stationnement cyclable.

Le schéma de la base de données a été co-construit avec :&#x20;

* [Vélo & Territoires](https://www.velo-territoires.org) : Association représentant les collectivités actrices du développement du vélo dans les territoires
* Des collectivités et entreprises productrices de données :
  * Montpellier Métropole
  * Ville de Paris
  * Métropole du Grand Lyon
  * Grand Chambéry
  * Grenoble Métropole
  * Montpellier Métropole
  * Grand Poitiers
  * Lille Métropole
  * Touraine Mobilités
  * Région Bretagne
  * Grenoble Métropole
  * Altinnova
* Des associations et instituts :&#x20;
  * L'Heureux Cyclage
  * MobilityData,&#x20;
  * OpenStreetMap
  * DGITM
  * Apitux
  * DRIEA
* Des réutilisateurs :&#x20;
  * MonUnivert&#x20;
  * Copark
  * Géovélo
  * Here Technologies

Deux ateliers ouverts (le [25/11/2020 ](../../documentation/liste-des-rencontres-publiques/25-11-2020-stationnement-cyclable-1.md)et le[ 24/02/2021](../../documentation/liste-des-rencontres-publiques/24-02-2021-stationnement-cyclable-2.md)) ont permis sa production. Il a notamment été établi après une enquête et plusieurs réunions du groupe de travail. Aujourd’hui disponible en version 0.2.0, il peut être mis-à-jour à l'avenir.

## Description du schéma

### Granularité du fichier

Chaque ligne correspond à un **ensemble cohérent d'équipements**. On utilise plusieurs lignes dans le fichier de données si le type de mobilier, le mode d'accès, la sécurisation et la couverture de l'équipement sont différents, même si la géolocalisation de l'équipement est identique.&#x20;

_Exemple : sur la place de la Mairie, au même endroit, j'ai à la fois un emplacement avec arceaux et un autre avec potelets, alors je distingue ces deux équipements en créant 2 lignes différentes_.&#x20;

### Type de mobilier &#x20;

Le champ "mobilier" est facultatif, il permet de décrire le type d'équipement de stationnement vélo. Le schéma de données reprend de près les modalités proposées par OpenStreetMap. La page décrivant les différents tags d'OpenStreetMap est ici : [https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)

Dans cette page de documentation nous vous présentons une photothèque des différents équipements pour illustrer chaque modalité retenue et de préciser à quel tag la modalité fait référence. N'hésitez pas à nous soumettre des images complémentaires.&#x20;

#### ARCEAU

Pièce de métal pliée contre laquelle vous pouvez appuyer votre vélo entier. Permet d'y fixer le cadre et une roue. Sécurité modérée. Utilisez cette étiquette pour les supports non rectangulaires également (par exemple, les supports ronds, les supports artistiques fantaisistes, les supports longs permettant d'attacher plus de deux véhicules).

_Dans OpenStreetMap, les arceaux sont généralement décrits au moyen du tag :  (_[_bicycle\_parking_](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)_=stands)_

****

<img src="../../.gitbook/assets/image (139).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (155).png" alt="" data-size="original">

<img src="../../.gitbook/assets/image (140).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (152).png" alt="" data-size="original"> **** <img src="../../.gitbook/assets/image (143).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (151).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (142).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (129).png" alt="" data-size="original">

<img src="../../.gitbook/assets/image (131).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (132).png" alt="" data-size="original">

{% hint style="warning" %}
**Ne pas confondre avec les potelets (**_**bollard**_**) plus dont le cercle central est plus petit et ne permet d'appuyer complètement le vélo**
{% endhint %}

#### **RATELIER**

Parfois appelés "pince-roues", les rateliers sont attachés aux murs ou fixés au sol. Fixe uniquement la roue avant (ou éventuellement la roue arrière), le mors avant ou le mors inférieur. En cas de mouvement violent, les roues du vélo peuvent être endommagées. Faible sécurité.&#x9;

_Dans OpenStreetMap, les rateliers sont généralement décrits au moyen du tag :  (_[_bicycle\_parking_](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)_=wall\_loops)_

<img src="../../.gitbook/assets/image (150).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (145).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (158).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (154).png" alt="" data-size="original">

#### **RACK DOUBLE ETAGE**

Un support à deux niveaux, où deux bicyclettes peuvent être stockées l'une au-dessus de l'autre.

_Dans OpenStreetMap, les racks double étage sont généralement décrits au moyen du tag :  (_[_bicycle\_parking_](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)_=two\_tier)_

<img src="../../.gitbook/assets/image (160).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (149).png" alt="" data-size="original">

**CROCHET**

Un crochet permet d'accrocher le vélo en suspension par la roue supérieure.&#x20;

_Dans OpenStreetMap, les crochets sont généralement décrits au moyen du tag :  (_[_bicycle\_parking_](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)_=tree)_

<img src="../../.gitbook/assets/image (159).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (147).png" alt="" data-size="original">

{% hint style="warning" %}
A différencier du support guidon qui ne laisse pas le vélo en suspension
{% endhint %}

**SUPPORT GUIDON**

Structure métallique avec des supports où le guidon d'une bicyclette peut être monté afin de garer la bicyclette.&#x20;

_Dans OpenStreetMap, les supports guidon sont généralement décrits au moyen du tag :  (_[_bicycle\_parking_](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)_=handlebar\_holder)_

&#x9;<img src="../../.gitbook/assets/image (135).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (144).png" alt="" data-size="original">

{% hint style="warning" %}
A différencier du crochet qui tient le vélo en suspension
{% endhint %}

#### **POTELET**

Type spécial de borne conçu pour le verrouillage des vélos. En général, le vélo est verrouillé sur le poteau central et des "bras" empêchent les voleurs de simplement soulever le vélo par-dessus le poteau.&#x20;

_Dans OpenStreetMap, les potelets sont généralement décrits au moyen du tag :  (_[_bicycle\_parking_](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)_=bollard)_

{% hint style="warning" %}
Ceux dont l'anneau est si grand qu'il peut être utilisé pour appuyer tout le vélo peuvent également être qualifiés d'arceau.&#x9;
{% endhint %}

<img src="../../.gitbook/assets/image (146).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (141).png" alt="" data-size="original">



#### **ARCEAU VELO GRANDE TAILLE**

Arceau spécial prévu pour les vélo de grande taille notamment vélos cargos.

<img src="../../.gitbook/assets/image (128).png" alt="" data-size="original"><img src="../../.gitbook/assets/image (136).png" alt="" data-size="original">

#### **AUCUN EQUIPEMENT (**_**floor**_**)**

Espace dédié au stationnement sans équipement pour accrocher le vélo. Cela peut être notamment le cas dans des box individuels sans accroche ou des espaces réservés au stationnement vélo dans des cours d'immeubles sans équipement spécifique.&#x20;

_Dans OpenStreetMap, les espaces de stationnement vélo sans équipement sont généralement décrits au moyen du tag :  (_[_bicycle\_parking_](https://wiki.openstreetmap.org/wiki/Key:bicycle\_parking)_=floor)_

### **Type d'accroche**

Le champ type d'accroche est obligatoire. Il permet de caractériser l'accroche du vélo sur l'équipement disponible. Les différents modes d'accroche possibles sont :&#x20;

* Cadre
* Roue
* Cadre et roue
* Sans accroche&#x20;

{% hint style="warning" %}
Cette informations est très importante pour connaître le niveau de sécurisation de l'équipement. En effet la Fédération des Usagers de la Bicyclette (FUB) recommande de développer des équipements permettant au moins l'accroche du cadre et d'une roue.&#x20;
{% endhint %}

{% hint style="info" %}
Voici une table indicative de correspondance des mobiliers avec le type d'accroche
{% endhint %}

| **Mobilier**              | **Type d'accroche** |
| ------------------------- | ------------------- |
| Arceau                    | Cadre et roue       |
| Râtelier                  | Roue                |
| Rack double-étage         | Cadre et roue       |
| Crochet                   | Roue                |
| Support guidon            | Cadre et roue       |
| Potelet                   | Cadre               |
| Arceau vélo grande taille | Cadre et roue       |
| Aucun équipement          | Sans accroche       |

### **Géolocalisation**

La géolocalisation de l'équipement est un champ obligatoire sous forme de point exprimé en longitude (X) et en latitude (Y).

* Si l'équipement est accessible librement sur la chaussée ou dans un espace avec de nombreux accès, on retiendra le centre de l'ensemble de l'équipement décrit. &#x20;
* Si l'accès de l'équipement est limité à une porte ou une entrée particulière, on peut privilégier la géolocalisation de cette entrée.&#x20;

{% hint style="danger" %}
**Point de vigilance :** souvent les outils permettant de donner les coordonnées x et y d'un point donnent d'abord la latitude Y puis la longitude X. Exemple : 48.82927, 2.366008 -> pour publier vos données, il faudra inverser en indiquant bien 2.366008, 48.82927.&#x20;
{% endhint %}

### Capacité&#x20;

La capacité de l'équipement est un champ obligatoire. Ce champ permet de déterminer la capacité totale de l'équipement en nombre de vélos. Cette capacité prend en compte les espaces réservés à des vélos spéciaux.&#x20;

Cette capacité peut être indicative car elle peut dépendre du mode de stationnement des usagers et de la taille des véhicules. En cas d'incertitude on prendra l'hypothèse permettant le stationnement du plus grand nombre de vélo.&#x20;

<img src="../../.gitbook/assets/image (140).png" alt="" data-size="original">6 places

<img src="../../.gitbook/assets/image (143).png" alt="" data-size="original">10 places

<img src="../../.gitbook/assets/image (154).png" alt="" data-size="original">4 places

<img src="../../.gitbook/assets/image (158).png" alt="" data-size="original">4 places

### Capacité vélo de grande taille

Ce champ est facultatif. Il permet de déterminer la capacité de l'équipement de stationnement pouvant être adaptée aux vélos de grande taille. La FUB indique qu'un emplacement adapté est d'une longueur de 2,50m et d'une largeur supérieure à 1,20m.&#x20;

<img src="../../.gitbook/assets/image (140).png" alt="" data-size="original">2 places (aux extrémités de l'équipement)

<img src="../../.gitbook/assets/image (143).png" alt="" data-size="original">10 places

<img src="../../.gitbook/assets/image (154).png" alt="" data-size="original">0 places (un pince-roue ne permet pas de stationner un vélo de grande taille)

### Accès

Ce champs permet de décrire le mode d'accès à l'emplacement de vélo : libre accès, accès sur abonnement ou inscription préalable ou accès privé.

_NB : un paiement immédiat sur place est considéré dans la catégorie libre accès dès lors qu'il ne nécessite pas une inscription au préalable._&#x20;

Ce champ est facultatif.

### Gratuité

Ce champ permet d'indiquer si l'usage de l'équipement est payant ou non.&#x20;

Ce champ est facultatif.&#x20;

### Identifiants

Il est attendu des producteurs de données de transmettre un identifiant unique par équipement de stationnement. Dans un fichier local il ne faut donc pas répéter plusieurs fois la même chaîne de caractères. Ce champ est obligatoire.

Si l'emplacement de stationnement est issu d'OpenStreetMap on indique son identifiant en le préfixant du code n s'il s'agit d'un [noeud](https://wiki.openstreetmap.org/wiki/Node), w s'il s'agit d'une [voie ](https://wiki.openstreetmap.org/wiki/Way)(way) et r s'il s'agit d'une [relation](https://wiki.openstreetmap.org/wiki/Relation) (champ id\_osm facultatif)

Enfin transport.data.gouv.fr donnera un identifiant national unique aux emplacements de stationnement à partir des identifiants locaux et de la source garantissant l'unicité des identifiants. Cette identifiant sera composé de cette manière : codeInsee-SV- {00001}

### Surveillance

L'emplacement de stationnement est-il surveillé ou non ? On choisit la valeur vraie si un système de vidéosurveillance est en place ou si un gardiennage est assuré.&#x20;

Ce champ est facultatif.&#x20;

### Couverture

L'emplacement est-il couvert par un toit protégeant l'équipement de la pluie ou de la neige ?

Ce champ est facultatif.&#x20;

### Lumière

L'équipement est-il éclairé la nuit par un éclairage dédié ou indirect (éclairage urbain) ?

Ce champ est facultatif.&#x20;

### Gestionnaire et propriétaire

Nom du gestionnaire et du propriétaire de l'équipement. Par gestionnaire on entend l'organisation en charge de l'entretien et potentiellement de l'exploitation commerciale de l'équipement. Par propriétaire, on entend l'organisation à qui appartient l'équipement.&#x20;

Ces champs sont facultatifs.&#x20;

### Année d'installation

Année durant laquelle l'équipement a été installé.

Ce champ est facultatif.&#x20;

### Date de mise à jour des données

Date à laquelle la ligne de données a été mise à jour la dernière fois.

Ce champ est facultatif.&#x20;

### Source

Organisation ou groupe de personnes ayant produit l'information. Par exemple : Grand Poitiers, Contributeurs OpenStreetMap...



