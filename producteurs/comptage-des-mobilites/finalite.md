# Finalité

{% hint style="danger" %}
Cette documentation est en cours de rédaction : elle sera finalisée prochainement.  
Pour toute remarque, n'hésitez pas à nous contacter à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)
{% endhint %}

Pour faciliter la réutilisation et réduire le coût d’intégration des données de comptage des mobilités dans des services tiers, un schéma a été défini afin d’assurer une harmonisation de ces données sur l’ensemble du territoire. Il permet de modéliser les comptages de différents types de mobilité : vélos, trottinettes, piétons, scooters, motos, camions, etc. 

Ce schéma est structuré en trois notions distinctes : les sites, les channels, et les mesures.

![](../../.gitbook/assets/image%20%28164%29.png)

Chacune de ces notions est retranscrite dans son propre fichier :

* les sites vont dans un fichier “sites.csv” avec une ligne par site
* les channels dans un fichier “channels.csv” \(idem\)
* les mesures dans un fichier “measures.csv” \(idem\)

Ce schéma définit des informations obligatoires, qui sont nécessaires pour fournir une information voyageur minimale, et complémentaires à fournir par le producteur. Cette distinction a été mise en place pour ne pas pénaliser les petits producteurs de données, et définit un standard minimal de complétude des données. Il est toutefois demandé aux producteurs de données de compléter le schéma avec le plus grand niveau de détail possible, afin de transmettre une information plus riche à l’usager final.

La base présente plusieurs cas d’usage : elle recense les sites de comptage d’une collectivité en permettant à des services de calcul d’itinéraire d’intégrer ces données et à chacun de suivre la fréquentation des mobilités d'un territoire donné. Elle peut également être utilisé par une collectivité pour étudier la part modale.

Ce schéma comprend notamment :

* l'identifiant unique pérenne du site de comptage ;
* la localisation du site de comptage ;
* les types de pratiques enregistrés par le compteur sur la voie ;
* la méthode utilisée pour récupérer les données depuis le compteur ;
* le pas de temps des données fournies, etc.

