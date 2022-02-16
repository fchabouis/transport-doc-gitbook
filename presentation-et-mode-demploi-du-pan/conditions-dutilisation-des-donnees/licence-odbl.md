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

Il est précisé que la clause de partage à l’identique (article 4.4) concerne les informations de même nature, de même granularité, de même conditions temporelles et de même emprise géographique.

Par extension, seule est exigée le repartage aux bases de données dérivées (paragraphe 4.6) pour les bases de données dérivées répondant à ces conditions.

### Dans quels cas faut-il republier des données modifiées ?

_Je crée une nouvelle base de données comprenant des données issues d'un fichier récupéré depuis transport.data.gouv.fr. Dois-je republier cette nouvelle base ?_

| **Oui**                                                                                                                            | **Non**                                                                                                           | **Justification**                   |
| ---------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------- | ----------------------------------- |
| <ul><li> Corrections des coordonnées</li><li> Correction des noms des arrêts</li><li> Ajout de coordonnées</li><li> etc.</li></ul> | Présence de commerces à proximité des arrêts                                                                      | Nature de la donnée                 |
| Ajustement des temps de correspondance                                                                                             | Cheminement piéton des correspondances                                                                            | Granularité de la donnée            |
| Corrections des horaires théoriques planifiés                                                                                      | Horaires temps réel des prochains passages aux arrêts de bus                                                      | Conditions temporelles de la donnée |
| Ajout d'une ligne manquante appartenant au même réseau que celui du producteur du GTFS initial                                     | Ajout d'une ligne d'un réseau strictement frontalier ou d'un autre réseau que celui du producteur du GTFS initial | Emprise géographique de la donnée   |

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

__
