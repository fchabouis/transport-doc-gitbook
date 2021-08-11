# 17/01/2019 - Transport régulier - Temps réel \(2\)

### 1re Partie: Modalités d'ouverture des données temps réel

#### 1\) Type de données temps réel à ouvrir.

Elles sont de deux types : 

a\) **Retards, perturbations** : c'est là où ça bloque le plus aujourd'hui. En France, le déploiement temps réel \(de qualité, fonctionnel, fiable\) est un des moins bons d'Europe.

- Les opérateurs \(SNCF, RATP, parfois branches régionales de Keolis et Transdev\) font de la résistance. Il y a de fortes résistances à rendre publique des informations sur les retards. 

- Certaines agglomérations ont des difficultés techniques pour exporter ces données. La donnée temps réel est souvent liée à un trajet. Les opérateurs ne savent pas mettre à disposition en 1 requête pour tous les retards liés à l'ensemble du réseau. 

b\) Information concernant **les alertes** : telle station est fermée, travaux, escalator cassé, grève,...

Ces données peuvent donner lieu à des dialogues directs avec les réutilisateurs \(avec des liens "Plus d'infos"\).

c\) **Localisation des véhicules \(bus\) en temps réel** : c'est une étape qu'est en train de franchir Google dans sa stratégie d'assistant personnel. GMaps va bientôt mélanger ces data avec les infos de géoloc d'Android pour être plus précis sur l'info voyageur que les opérateurs eux-mêmes. Ils pourront avoir de l'info sur l'affluence en temps réel également. Ils sont prêts à terme à ouvrir une discussion pour repartager ces informations.

**2\) Quel format privilégier pour la donnée temps réel \(transports en commun\) ?**  
  
- Historiquement, Google utilise du **GTFS-RT,** un flux qui permet de transmettre les retards dans leur globalité à un instant "t". Le fichier est très léger lorsqu'il y a peu de retards sur l'ensemble du réseau. 

* Le format **SIRI**, norme imposée par l'Europe : voir le [guide de l'AFIMB](http://www.normes-donnees-tc.org/wp-content/uploads/2017/06/Guide-pour-louverture-des-donn%C3%A9es-temps-r%C3%A9el-v4.pdf). 

Voici les différences principales entre les formats GTFS RT et SIRI : 

* GTFS RT : avantage de la compacité, renvoi l'ensemble des informations associées à une ligne \(rempli la fonction estimated timetable du SIRI\). Il faut un GTFS synchrone avec le temps réel, car le GTFS RT donne des delta qui renvoient à des identifiants d’arrêts qui doivent être définis dans le GTFS initiale \(pas de redite dans la description des objets\).
  * Efficace
  * Contrainte que tous les transporteurs sont pas capables de remplir = une difficulté sur laquelle bute le STIF \(canaux qui diffusent théoriques et temps réel ne sont pas synchrones\)
* SIRI : ensemble de services, le plus emblématique : stop-monitoring \(prochains passages à un arrêt\), c’est le plus déployé en France jusqu’à présent. 
  * La fonctionnalité SM-Stop Monitoring sert l'information voyageur, alors que la fonctionalité EM-Estimated Timetable est nécéssaire pour alimenter des calculateurs d'itinéraire.
  * Fait remonter les perturbations aux voyageurs par la fonctionalité GM-General Message
  * SX-Situation Exchange : fait remonter des perturbations pour un calculateur d’itinéraire

Il devrait être possible de convertir les données SIRI au format GTFS RT.

**3\) Conditions d'utilisation / licence**

GMaps a de gros problèmes avec certains opérateurs comme la RATP qui mettent en place des API dites "ouvertes", mais avec des Terms and Conditions fermées. Celles de la RATP interdisent le stockage des données : GMaps est donc obligée d'aller chercher les données à chaque recherche d'itinéraire, alors qu'il serait possible de reconstituer la base de donnée complète chaque minute en une \(ou un petit nombre de\) requête\(s\). 

Dans les faits, GMaps ne paye pas la donnée \(logique de plateforme\). Mais avec des données mises à disposition intelligemment, les réutilisateurs n'auront pas à faire de si nombreuses requêtes que ce que prétendent les opérateurs.

**4\) Rôle du Point d'Accès National**

Le Point d'Accès National \(PAN\) réunit dans un même lieu l'ensemble des données temps réel pour les réseaux de transport en commun de France. Il assure ainsi une meilleure découvrabilité des données ouvertes. 

Le PAN rempli également un rôle d'accompagnement auprès des producteurs de données pour faciliter l'ouverture. 

### 2ème Partie: Ateliers Thématiques

### Atelier : Coût vs. Bénéfices

### Coût

1. Investissement initial pour la création de la donnée.
2. Coût de mise à disposition et maintenance. 

Attention le coût ce n’est pas uniquement des frais de serveur car ces aspects techniques peuvent se résoudre. C’est aussi du temps homme pour créer, déposer, maintenir. 

Craintes Keolis + Apple : les éditeurs de SAEIV vont se faire beaucoup d’argent pour avoir accès aux modules qui ont les flux. 

Retours Apple : on est jamais rentrer dans les discussions de cout de “run” car les coûts de set up étaient trop élevés. On a réussi uniquement sur une ville au canada avec du vrai temps réel.

Retours SNCF : nous mettons à disposition une API, utilisée par 8000 personnes. Celle-ci a des conditions d’utilisation avec un seuil :  au delà de 5000 requêtes par jour c’est gratuit. 

Craintes : si cela coûte plus cher à l’agglo cela va freiner

Transdev : Il y a deux cas de figure : 

1. On passe par le SAE pour ouvrir les données
2. On a les données et on ouvre. 

### Solution

Les coûts existent de toute manière pour accéder à l’information. Au final en ouvrant les données elles sont accessibles et diffusées plus largement et donc finalement on y gagne en coût d’information \(centre d’appel, requête application de la ville, etc.\). C’est le conquête de client et de voyageur. Opportunité de rester compétitif. 

La solution la plus simple est d'ouvrir les données telles qu'elles existent, quitte à ce que les données soient converties dans un autre format par la suite. 

Il y a plein de manière de requêter un service. Il existe des solutions techniques pour empêcher les systèmes de saturation. Solution déposer un fichier pour l’ensemble du réseau et MAJ avec une certaine fréquence sur l’ensemble du réseau. ⇒ baisse de la consommation au lieu de requêter pour un arrêt \(ref : GTFS VS SIRI\).

Remarque de la SNCF : les abonnements payants sur l’API c’est pas forcément pour des raisons de volumétrie c’est pour avoir accès à un service VIP \(hotline, etc.\). Il peut y avoir des modèles où on ne récupère que les informations des horaires perturbés.

Attention, les spécifications des API sont toutes différentes donc il ne faut pas mettre un seuil commun. Comment calculer ce seuil ? Calcul en nombre de voyageur, de véhicules, de data point sur le réseau ? 

Risque : cela va rebuter les AO si le seuil est bas car les systèmes de paiement sont difficiles à mettre en place. 

Solution : le PAN fait convertisseur

Attention aux SAEIV qui font exprès de brider de l’information pour pouvoir la commercialiser par la suite.

Pour mesurer l’impact positif et relativiser coût / bénéfices : quel est le coût des guides horaires papiers ? 

## Atelier format

Il existe deux formats de diffusion de données en temps réel qui se font la guerre : 

1. SIRI lite
2. GTFS RT

Différences entre les deux formats :  

* Le SIRI lite expose des services. Par exemple, lorsque l’on demande des informations sur un arrêt précis alors que le GTFS RT donne une information sur l’ensemble du réseau. 
* Le SIRI lite il y a beaucoup de champs optionnels ce n’est pas forcément pratique. Continuer les travaux en cours pour harmoniser les choses.

Témoignages de deux AOM : Toulouse \(réseau Tisseo\) et Besançon \(réseau Ginko\). Ils aimeraient faire du GTFS mais constatent des histoires d’identifiants qui se perdent.

Here Technologie :  il y a une grosse prédominance du GTFS RT. Même si on perd de la qualité d’information c’est mieux car plus de personne arrive à lire ce format. 

GTFS RT est plus facilement mangé par les applications. 

## Atelier juridique

Les positions divergent entre les différents acteurs : 

* Position du Grand Lyon : je veux maîtriser les données pour que les gens ne fassent pas des choses que je ne veux pas avec. 

Est-ce que l’odbl a du sens, est-ce que les gens vont repartager ? Est-ce que le bon choix est de repartager à l’identique ?

## Atelier accompagnement technique

Rappel de la démarche beta.gouv : prendre un cas concret une ville et faire de manière incrémentale.

1. Etape zéro : faire une liste des API des prochains passages ? Le CEREMA le fait déjà. 
2. Première étape : Se contenter des prochains passages. 
3. Etape ultime de faire un flux des données temps réel de toute la france. C’est trop complexe pour une première étape.

Solution : 

Proposer de faire une API en Siri lite avec les AO qui jouent le jeu. Cette API sera coupée verticalement par réseau \(par exemple : appel à Toulouse puis appel à Rennes, etc\).

Transport Data Gouv encaisse la charge pour résoudre les problèmes de budget pour les petites AO. Entre nous on communique en SIRI.

Transport Data Gouv prend en charge une partie de l'infrastructure technique. 

