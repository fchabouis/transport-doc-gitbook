# 12/11/2020 - Transports personnels, Autopartage \#2

### Participants

Miryad Ali \(transport.data.gouv.fr\), Antoine Desbordes, \(transport.data.gouv.fr\), Francis Chabouis \(transport.data.gouv.fr\), Benoît Queyron \(transport.data.gouv.fr\), Thibaut Barrère, \(transport.data.gouv.fr\), Nicolas Berthelot \(transport.data.gouv.fr\), Nicolas Frasie \(Communauto & Association des Acteurs de l'Autopartage\), Josée Sabourin \(MobilityData\), Léo Franchet \(MobilityData\), Aurélien Allard \(PwC\), Clément Teillou \(PwC\), Bertrand Billoud \(Kisio\), Cameron Monagle \(Transit App\), Cindie Andrieu-Dupin \(DRIEA\), Emmanuelle Champaud \(TOTEM Mobi\), Erwan Huon \(Keolis Rennes\), Euryale Ambroise \(Île-de-France Mobilités, Vivien Michon \(Île-de-France Mobilités\), Fabien Serra \(MyBus\), Jean-Baptiste Sicart Ruiz \(Colombus Consulting\), Souhail Chraibi \(Colombus Consulting\), Jérémie Valentin \(Montpellier Métropole\), Jérôme van Oost \(Lille Métropole\), Nicolas Madignier \(Grand Poitiers\), Pierrick \(Fluctuo\), Ugo Nepi \(ZITY\), Jean-Philippe Clément \(Paris\), Yoann Benhacoun \(Moovit\), Pierre Trouvé \(Ubeego\), Matthieu Richard \(Here Technologies\), Badr Haji \(Share Now\)

Cet atelier a été coanimé avec [l’Association des Acteurs de l’Autopartage](https://asso-autopartage.fr/about.html) \(AAA\) et [MobilityData](https://mobilitydata.org/).  Nous collaborons avec ces deux associations afin d’établir une extension du format GBFS qui sera adapté aux données d’autopartage. 

#### Vous trouverez le support de présentation[ ici ](https://docs.google.com/presentation/d/1lo99tt-OAoysQCPophjYhA9C4I-TBbVgeqFJz-Ma-8A/edit?usp=sharing)

### 1. Evolution du GBFS et adaptation du format à l'autopartage \(Josée Sabourin, MobilityData\) 

[MobilityData ](https://mobilitydata.org/)est en charge de l'évolution de ce format avec une mise en place d'un processus de gouvernance et un travail d'animation d'une communauté de contributeurs via des issues et des Pull request sur le[ Github NABSA](https://github.com/NABSA/gbfs).

Le schéma de données a été publié par MobilityData dans le [Github](https://github.com/NABSA/gbfs/pull/255) NABSA et dans un [Google Doc](https://docs.google.com/document/d/16NKnf10SjmBBVwUlKrc7oeuxzeWqS_dQvztlT2F4dH8/edit#) 

#### État d'avancement du schéma

* Pull Request ouverte 
  * contributions de 4 personnes
* Google Doc ouvert où on peut laisser des commentaires

Changements proposés par les contributeurs du Github et du Google Doc : 

* remplacer seating\_capacity par rider\_capacity afin d'être plus générique
* inclure le numéro de la plaque d'immatriculation du véhicule 
* renseigner des informations spécifiques sur les véhicules \(comme les accessoires\) ?
* classifier les véhicules selon une liste pré-définie
* créer un blog sur medium avec des articles pas trop techniques sur le sujet

### 2.  Présentation de l'extension GBFS \(Nicolas Frasie, AAA\)

L'AAA a édité une [première version de l'extension GBFS](https://docs.google.com/spreadsheets/d/1r0rHbGmubgKAqvI4dOD86zwOL1hWjOQJxNhmeGeJtSs/edit#gid=917905368) \(v.1.0\). MobilityData a ensuite modifié ce schéma de données en supprimant, entre autre, l'autopartage en boucle de la proposition et en adaptant le fichier sur les tarifs \([v.1.1](https://docs.google.com/document/d/16NKnf10SjmBBVwUlKrc7oeuxzeWqS_dQvztlT2F4dH8/edit#)\).

L'enjeu est de faire converger ces deux schémas de données pour proposer une extension permettant de modéliser l'autopartage en boucle tout en renseignant les tarifs. 

Vous trouverez la présentation des points de convergence et divergence de ces deux versions dans la [présentation](https://docs.google.com/presentation/d/1lo99tt-OAoysQCPophjYhA9C4I-TBbVgeqFJz-Ma-8A/edit?usp=sharing) et plus en détail ici : 

**Fichier : vehicle\_types.json**

* car\_type \(type de véhicule\): désaccord sur le référentiel à utiliser
* vehicule\_description \(modèle de véhicule\) : pas inclus par MobilityData
* min\_fuel\_level : généralement pas de consigne sur le niveau minimal de carburant, AAA se demande si c'est utile
* Euro\_norm et gCO2\_km : afin de prendre en compte l'interdiction de certains véhicules de circuler dans les centre villes \(pas inclus par MobilityData \)
* vehicle\_desc: description libre \(problématique de langue\)
* use\_conditions: conditions d'accès aux véhicule comme une limite en fonction de l'âge \(ex: GetAround\). Possibilité d'inclure des restrictions sur l'ancienneté de l'obtention du permis \(Pierre Trouvé, Ubeeqo\)/

Jean-Philippe \(ville de Paris\) a soulevé la question de la prise en compte du territoire sur lequel est déployé le service et la diffusion   d'informations privées. Il a également souligné le fait que les règlementations vis a vis de la LOM ne sont pas forcément celles demandées par les villes et les territoires locaux. 

Nicolas Frasie \(AAA\) a rappelé que l'atelier ne concerne que la conformité des opérateurs d'autopartage à la LOM et Léo Frachet \(MobilityData\) a précisé que ce sont des discussions qu'ils ont et que toutes personnes qui veut en discuter peut les contacter directement.

**Fichier : station\_information.json**

* share\_type : précise le type d'auto partage. Ce champ n'est pas pris en compte par MobilityData 
* parking\_hoop : présence d'arceaux dans certaines stations. Ce champ n'est pas pris en compte par MobilityData 
* contact\_phone : contact du garage. Ce champ n'est pas pris en compte par MobilityData 

**Fichier : free\_bike\_status.json**

L'autonomie des voitures en autopartage se traduit en % restant. L'information sur le nombre de kilomètre pouvant être parcouru avec l'autonomie restante n'est pas toujours accessible. 

Quel référentiel utilisé pour classer les accessoires \(siège bébé, pneus hiver etc.\) ? 

* Question de Nicolas Madignier \(Grand Poitiers\) : Est-ce bien adapté au temps reel, car il y a 10 fichiers. Il peut donc y avoir des risques de de-synchronisation entre les fichiers.

Réponse de Josée Sabourin \(MobilityData\) : Le champ time to load \(TTL\) permet d'indiquer quand il faut recharger les données. Le TTL ne doit pas forcément être identique entre tous les fichiers \(certains fichiers doivent être rafraichis plus souvent que d'autres\). Le format est pensé pour le temps-réel.

Réponse de Leo Frachet : Oui il y a des risques de perte de synchronisation mais ce problème ne s'est jamais posé en pratique en production.

* Question d'Erwan Huon \(Keolis, Rennes\) : Qu'en est il du rafraîchissement des données sur un temps plus court qu'1min ?

Réponse d'Antoine Desbordes \(transportdatagouv\): Ce format permet de faire des économies de trafic car certaines informations bougent peu comme l'emplacement des stations.

* Question de Stanislas soufflet \(Clem\): Est-ce que le type de véhicule adapté aux Personnes à Mobilité Réduite \(PMR sans pédales\) pourra être représenté par le modèle ?

Réponse de Nicolas Frasie \(AAA\) : cette information pourra apparaitre dans le champ vehicule\_accessories.

* Question de Pierre Trouvé \(Ubeeqo\) : que signifie disponibilité ? 

Réponse de Nicolas Frasie \(AAA\) : Cela indique la disponibilité entre maintenant et les 3 prochaines heures. Il n'y a pas la possibilité de donner un calendrier futur de disponibilités.

**Fichier : system\_pricing\_plans.json**

Ce fichier est proposé par MobilityData. 

Nicolas Frasie \(AAA\) : comme cet aspect ne fait pas partie des obligations règlementaires prochaines, l'AAA n'a pas travaillé sur le sujet pour le moment.

* Question de Pierre Trouvé \(Ubeeqo\) : Est ce que l'utilisateur voit une explication de prix \(2€ de l'heure, 50 la journée\), ou est ce qu'il procède à une véritable simulation en donnant des dates ?

Réponse de Josée Sabourin \(MobilityData\): ça peut être un barème, ou une estimation du prix du voyage, ça dépend de chaque application.





L'AAA, MobilitData et transport.data.gouv.fr continueront d'enrichir cette extension du format GBFS en faisant notamment des entretiens réutilisateurs afin d'intégrer leurs attentes. 

Un prochain atelier sera proposé dans les mois à venir afin de proposer une v.1.2 du schéma. 

