# Licence ODbL

Certaines données disponibles sur le Point d’Accès National transport.data.gouv.fr sont soumises à la licence ODbL, que les réutilisateurs s’engagent naturellement à respecter dès lors qu’ils téléchargent un jeu de données concerné. \
Seul le [texte complet](https://spdx.org/licenses/ODbL-1.0.html#licenseText) de la licence fait foi. Une [traduction non officielle en français est disponible ici](https://vvlibri.org/fr/licence/odbl-10/legalcode/unofficial) pour faciliter sa compréhension

{% hint style="success" %}
Cette licence permet au réutilisateur de reproduire, modifier, exploiter à titre commercial sous trois conditions :

* Mentionner la source ;&#x20;
* Redistribuer les modifications sous des conditions de partage identiques ;
* Maintenir ouvertes les bases de données redistribuées.
{% endhint %}

### Conditions Particulières d'Utilisation

Compte tenu de la rédaction large de la clause de partage à l’identique (article 4.4) les équipes de transport.data.gouv.fr, avec l'appui d'Etalab, de la DINUM et de la DGITM se sont accordées avec les acteurs de l’écosystème sur des conditions particulières d’application de cette clause. En particulier :&#x20;

> « _Il est précisé que la clause de partage à l’identique (article 4.4) concerne les informations de même nature, de même granularité, de même conditions temporelles et de même emprise géographique._\
> _Par extension, seule est exigée le repartage aux bases de données dérivées (paragraphe 4.6) pour les bases de données dérivées répondant à ces conditions._ »

Dès lors, ces conditions particulières amènent à considérer juridiquement qu’il :

* constitue une « _base de données dérivée_ », soumise à l’obligation de repartage à l’identique et gratuit, la base de données créée par un licencié au moyen d’une base de données initiale soumise à la licence ODbL, dès lors que les données des bases de données initiale comme dérivée sont de même nature, de même granularité, de même conditions temporelles et de même emprise géographique ;
* constitue une « création produite », non soumise à l’obligation de repartage à l’identique et gratuit, la base de données créée par un licencié au moyen d’une base de données initiale soumise à la licence ODbL, dès lors que les données de la création produite ne sont pas de même nature, de même granularité, de même conditions temporelles et de même emprise géographique que les données de la base de données initiale ;
* ne constitue ni une « _base de données dérivée_ », ni une « _création produite_ », dès lors non soumise à l’obligation de repartage à l’identique et gratuit, la base de données créée par un licencié au moyen d’une part non substantielle de la base de données initiale soumise à la licence ODbL.

> « _Les bases de données ainsi repartagées doivent être publiées sur le Point d'accès national transport.data.gouv.fr, dans le format d'origine._ »

{% hint style="info" %}
La procédure pour le repartage des bases de données est détaillée [ici](https://doc.transport.data.gouv.fr/reutilisateurs/repartager-les-modifications-apportees-a-une-ressource).
{% endhint %}

{% hint style="info" %}
L’ensemble des données sous licence ODbL présenté sur le Point d’accès national se voit appliqué les conditions particulières susmentionnées à l'exception des données issues d'OpenStreetMap..
{% endhint %}

### Dans quels cas faut-il republier des données modifiées ?

_Je crée une nouvelle base de données comprenant des données issues d'un fichier récupéré depuis transport.data.gouv.fr. Dois-je republier cette nouvelle base ?_

| **Oui**                                                                                                                                                                                       | **Non**                                                                                                                                                                                                                                                                                                                                             | **Justification**                   |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| <p>Correction ou ajout de coordonnées géographiques</p><p></p><p>Correction ou ajout de noms des arrêts</p><p></p><p>Correction ou ajout du nombre de place de stationnement d'un parking</p> | <p>Calcul de la distance à l'arrêt de bus le plus proche pour une liste de commerces<br><br>Utilisation des aménagements cyclables dans un calculateur d'itinéraire multimodal (pas de repartage des données routières non soumises à l'ODbL)<br><br></p>                                                                                           | Nature de la donnée                 |
| <p>Ajustement des temps de correspondance<br></p>                                                                                                                                             | <p>Ajout des cheminements piéton géolocalisés pour une correspondance<br></p><p>Statistiques par commune du nombre de places de stationnement</p>                                                                                                                                                                                                   | Granularité de la donnée            |
| <p>Corrections des horaires théoriques planifiés<br><br></p>                                                                                                                                  | <p>Horaires temps réel des prochains passages aux arrêts de bus<br><br>Prédiction du nombre de vélo disponibles dans 10 minutes</p>                                                                                                                                                                                                                 | Conditions temporelles de la donnée |
| <p>Ajout d'une ligne manquante appartenant au même réseau que celui du producteur du GTFS initial<br><br>Ajout de parkings à Biarritz dans la Base nationale du stationnement </p>            | <p>Ajout d'une ligne d'un réseau strictement frontalier ou d'un autre réseau que celui du producteur du GTFS initial<br><br>Ajouts de parkings à Berlin dans la Base nationale du stationnement<br><br>Ajout d'emplacements de stationnement vélo en région Île-de-France dans une base de stationnement vélo sur la région Centre-Val-de-Loire</p> | Emprise géographique de la donnée   |

Il est recommandé de republier les bases de données dérivées directement sur la fiche du producteur correspondant afin de notifier ce producteur de la mise à disposition d’un jeu de données enrichi pour envisager une correction à la source.

### Comment mentionner la source _(paternité)_ de la base de données ?

La réutilisation d’une base de données soumise à la licence ODbL, ou d’une partie de cette base, requiert la mention :

* des noms des différents contributeurs à cette base ;
* de la licence ODbL à laquelle est soumise cette base.

S’il s’avère impossible d’intégrer les mentions requises en raison de limitations de forme ou d’affichage (c’est-à-dire les applications smartphone, les résultats en fonction de la voix ou du texte, les agencements limités par l’espace), il est possible d’inclure les mentions à un emplacement (tel qu’un menu dédié pertinent) où les utilisateurs pourront les retrouver facilement. Il est ainsi possible de créer une page dédiée « mentions légales » ou « sources des données » référençant la liste des concédants avec les liens vers leurs portails open data.

La source pourra par exemple être mentionnée de la façon suivante :

> _« \[Nom du réutilisateur] utilise les dernières versions des jeux de données communiqués par les producteurs suivants :_
>
> _\[Liste des producteurs de données]_
>
> _Ces données sont disponibles sur transport.data.gouv.fr sous la licence « Open Database Licence » (ODbL).»_

### Cas complexes

Un atelier tenu le mardi 10 mai 2022 a permis d'identifier quelques cas complexes d'application de l'ODbL avec Conditions Particulières.

#### Quelles conditions d'utilisation pour les données disponibles sur le PAN qui sont extraites d'OpenStreetMap ?

Plusieurs bases de données disponibles sur le PAN sont extraites d'OpenStreetMap, notamment une [Base nationale des aménagements cyclables](https://transport.data.gouv.fr/datasets/amenagements-cyclables-france-metropolitaine/) et une [Base nationale du Stationnement Cyclable](https://transport.data.gouv.fr/datasets/stationnements-cyclables-issus-dopenstreetmap/).&#x20;

Pour ces bases de données les Conditions particulières ne se s'appliquent pas et l'usager de ces données doit se référer à la licence ODbL ainsi qu'aux "[Community Guidelines](https://wiki.osmfoundation.org/wiki/Licence/Community\_Guidelines)" de la communauté, c'est à dire aux règles particulières définies pour la ressource particulières qu'est OpenStreetMap. Ces Community Guidelines précisent quelles sont les règles auxquelles un utilisateur des données d'OpenStreetMap doit se conformer notamment sur les conditions où le repartage des amélioration est obligatoire ou non.

**Dois-je repartager si je simplifie une information ?**

Certaines modifications triviales de l'information ne sont pas soumises à l'obligation de repartage. Le critère qui permet de juger du caractère trivial de la modification peut se baser sur le fait qu'on n'ajoute pas d'information dans la modification. Par exemple en changeant d'unité (ex : m à cm) ou en créant des catégories à partir d'une variable continue.

En revanche pour certains regroupement on peut juger que le traitement mérite d'être repartagé. Par exemple en simplifiant le type d'accroche d'équipements de stationnement à partir de catégories métier, on peut considérer que cette nouvelle catégorisation des types d'accroche peut présenter une utilité pour un autre utilisateur et doit donc être repartagée.

&#x20;

**Dois-je repartager si j'ajoute une information manquante ?**

On peut considérer obligatoire de repartager une information essentielle ou générique que l'on aurait intégré à un fichier de données. Par exemple en renseignant le nombres de places disponibles dans un parking, on peut attendre que cette information soit repartagée.&#x20;

Dans le cas où l'information ajouté et de nature très différente. Par exemple le calcul de la proximité à un type de commerce en croisant avec une base propriétaires, ce repartage peut ne pas être soumis aux mêmes conditions. &#x20;



**Dois-je repartager quand je mélange des bases ?**

Le cas est particulièrement prégnant pour les calculateurs d'itinéraires. le principe es conditions particulières d'utilisation est de permettre à des acteurs manipulant des bases de données multithématiques d'intégrer des données spécifiques sans contrainte de repartage de données d'une autre nature (bâtiment, points d'intérêt). Doivent être repartagées seulement les améliorations directement faite sur les données consommées.



