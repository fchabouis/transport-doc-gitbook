# Comptage des mobilités

{% hint style="danger" %}
Cette documentation est en cours de rédaction : elle sera finalisée prochainement.\
Pour toute remarque, n'hésitez pas à nous contacter à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)
{% endhint %}

Dans le cadre des travaux de l’équipe du Point d’accès national et de la mise en œuvre de l’ouverture des données pour améliorer l’information dont disposent les voyageurs, l’équipe de transport.data.gouv.fr, en collaboration avec l'association [Vélo & Territoires](https://www.velo-territoires.org) et [Eco-compteur](https://www.eco-compteur.com/application/mobilite-douce-fr/?gclid=CjwKCAjwvuGJBhB1EiwACU1AiRLcEsPSqoFAdNFvOqMzZoDdrAU4YY8Brnx8k-qBtPSuk3hbQlQdDRoC1ucQAvD_BwE), propose une solution simple et structurée pour l’ouverture des données de comptage des mobilités : le schéma national de comptage des mobilités. Il s’adresse à toute collectivité qui souhaite se lancer dans l’ouverture de jeux de données décrivant la fréquentation de leurs infrastructures.

Ce schéma  a été co-construit avec un groupe de travail composé 

* De collectivités :
  * Les villes d'Angers, de Brest, de Montpellier, d'Alençon et de Paris
  * Le syndicat intercommunautaire Ouest Cornouaille Aménagement (SIOCA)
  * Les communautés de communes Touraine et d'Annemasse   
  * La communauté d'agglomération du Grand Chambéry, 
  * La communauté urbaine Grand Poitiers
  * Les métropoles de Nantes, Grand Lyon, Grenoble, Bordeaux et de Rouen 
  * Les départements du Finistère et d'Ille-et-Vilaine
  * Les régions Bretagne, Île-de-France, Hauts-de-France et  Centre - Val de Loire
* De fournisseurs de données de comptage : 
*
  * [Eco-Compteur](https://www.eco-compteur.com/application/mobilite-douce-fr/?gclid=CjwKCAjwvuGJBhB1EiwACU1AiRLcEsPSqoFAdNFvOqMzZoDdrAU4YY8Brnx8k-qBtPSuk3hbQlQdDRoC1ucQAvD_BwE)
  * [Metrocount](https://metrocount.com/fr/)
  * [Alyce](https://alyce.fr)
  * [Sterela](http://www.sterela.fr)
  * [TagMaster](https://tagmaster.com)
  * [Wintics](https://wintics.com/fr/accueil/)
* D'associations et instituts : [Club des villes et territoires cyclables](https://villes-cyclables.org), Droit au Vélo ([ADAV](https://droitauvelo.org)) 
* De réutilisateurs : [Vélo & Territoires](https://www.velo-territoires.org), [Géovélo](https://www.geovelo.fr/france/route), Le Centre d'études et d'expertise sur les risques, l'environnement, la mobilité et l'aménagement ([CEREMA](https://www.cerema.fr/fr))

Trois ateliers ouverts (le[ ](https://doc.transport.data.gouv.fr/documentation/liste-des-rencontres-publiques/27-06-2019-infrastructures-cyclables)[23/04/2021](https://doc.transport.data.gouv.fr/documentation/liste-des-rencontres-publiques/23-04-2021-comptage-velo-1)) le 17/06/2021, et le[ ](https://doc.transport.data.gouv.fr/documentation/liste-des-rencontres-publiques/27-08-2020-infrastructures-cyclables-3)28/09/2021) ont permis sa production. Il a notamment été établi après des entretiens avec différents fournisseurs de solutions de comptage afin de nous assurer que les champs proposés répondaient bien à leurs besoins et compétences. Ce schéma permet de recenser les sites de comptages et de comptabiliser la fréquentation d'infrastructures.  

Source des définitions : 

* [https://www.securite-routiere.gouv.fr/](https://www.securite-routiere.gouv.fr)
* [Centre nationale de ressources textuelles et lexicales ](https://cnrtl.fr/definition)
* [Larousse ](https://www.larousse.fr/dictionnaires)\


## Description des différentes types de pratiques pouvant être distinguées par les compteurs 

Vous trouverez ci-dessous la définition de toutes les pratiques pouvant être distinguées par des compteurs dans le champ "user_type"  du schéma. 

{% hint style="info" %}
Les noms des pratiques sont en français, accompagnés de leur traduction anglaise. 
{% endhint %}

### Bus

Un bus est un véhicule terrestre, à moteur, de grande taille qui permet de transporter plusieurs personnes. La longueur d'un bus peut aller de 11 mètres à 24.50 mètres pour les bus accordéons en France. 

### Camion - Truck 

Un camion renvoie à de gros véhicules automobiles utilisés pour le transport des marchandises.\
En France, ils renvoient à des véhicules de plus de 2.5 tonnes et seuls sont autorisés les camions de 16,5 mètres ou 18,75 mètres de longueur. 

### Canoe

Un canoe est embarcation légère manœuvrée à la pagaie ou à la rame qu'on utilise pour la descente des rivières au cours rapide

### Cavalier - Horse rider

Un cavalier est une personne qui se déplace à cheval, en étant sur le cheval. 

### Deux roues motorisées - Two wheels motorized 

Un cycle moteur est un véhicule motorisé à deux ou trois roues allant jusqu'à 50 cm³. 

### Minibus

Un minibus est, selon la norme ISO,  un bus à un étage ne comportant pas plus de dix-sept places assises, y compris celle du conducteur. \
Il peut mesurer de 4 à 7 mètres. 

### Pieton - Pedestrian 

Un piéton est une personne qui se déplace à pied, soit en marchant soit en courant. Certaines personnes se déplaçant autrement qu'avec leur pied peuvent être assimilées à des piétons [(article R 412-34 du code de la route).](https://www.legifrance.gouv.fr/affichCodeArticle.do?cidTexte=LEGITEXT000006074228\&idArticle=LEGIARTI000023095936) Sont ainsi assimilées à des piétons les personnes qui conduisent un véhicule pour personne à mobilité réduite, ou tout autre véhicule de petite dimension sans moteur. Les personnes qui marchent avec un cycle ou un cyclomoteur à la main,  les infirmes qui se déplacent dans une chaise roulante mue par eux-mêmes ou circulant à l'allure du pas peuvent rentrer dans la catégorie "piéton".\
Selon les types de technologies du compteur ou la classification utilisée par le fournisseur de compteur, une personne à pied tenant un vélo à la main sera considéré comme piéton ou à vélo. 

### Tramway

Mode de transport collectif public urbain ou interurbain électrique circulant sur des voies ferrées équipées de rails plats, et qui est soit implanté en site propre, soit encastré à l'aide de rails à gorge dans la voirie routière. 

### Trottinette - E-scooter

Une trottinette est un moyen de transport urbain individuel, composé d'une plaque métallique montée sur deux roues, un guidon et sur laquelle l'utilisateur peut poser un pied tandis qu'avec l'autre il fait mouvoir l'ensemble.

### **Véhicule utilitaire légers** - VAN

Un véhicule utilitaire léger est un** **véhicule terrestre utilisé pour le transport de marchandise et de moins de 3,5 tonnes. 

### Velo - Cycle 

Un vélo est un véhicule terrestre à deux ou trois roues dont la capacité motrice est activée par un mouvement circulaire des jambes ou des bras de son conducteur. \
Les vélos à assistance électrique et vélos cargo sont inclus dans cette catégorie.\
Selon les types de technologies du compteur, ou la classification utilisée par le fournisseur de compteur, une personne à pied tenant un vélo à la main sera considéré comme piéton ou à vélo. 

### Voiture - Car

Une voiture est un véhicule terrestre léger, à moteur, constitué d’un châssis généralement sur quatre roues et utilisé principalement pour le transport des personnes



###



