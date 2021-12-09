# Notre offre de service

* **Accompagnement technique et opérationnel** des producteurs dans la mise en qualité et en conformité de leurs données (analyse, recommandations, suivi), conversion au format normalisé exigé par le règlement européen. Cet accompagnement permet une mise en qualité au moindre coût ;
* **Harmonisation juridique** des conditions de réutilisation des données via le recours à la licence ODbL, adoptée par le groupe de travail animé par Etalab ;
* **Moissonnage possible** : si un producteur de données dispose déjà de son propre portail de données ouvertes, le PAN peut alors agir en tant que répertoire, donnant un accès direct à ces données stockées ailleurs ;
* **Simplification des relations avec les réutilisateurs**, qui n’ont plus besoin de contacter chaque fournisseur de données. Le PAN recueille les observations sur les données publiées et les détenteurs de ces données y répondent ;
* **Conversion automatique de données au format GTFS vers le format NETEX**, via le [convertisseur Gtfs2NetexFr](http://lafabriquedesmobilites.fr/articles/innovation/gtfs2netexfr-nouvel-outil-open-source-pour-faciliter-la-production-de-donnees-transport-au-format-netex/), afin de faciliter le respect des obligations réglementaires par les producteurs de données ;
* **Économies sur les frais de serveur** avec la possibilité d’héberger temporairement sur les serveurs du PAN les flux temps-réel à haut niveau de sollicitation.

{% hint style="info" %}
**Pour les données temps-réel :** l’information en temps réel permet d’augmenter sensiblement l’usage des différents services de mobilité, car l’utilisateur maîtrise mieux son temps d’attente et de trajet. Le producteur fournit un flux de données mis à jour toutes les 30 secondes. Pour cette raison, la charge sur les serveurs est une crainte légitime de nombreux producteurs.&#x20;

Le PAN teste actuellement une solution dans laquelle il joue le rôle de serveur mandataire (proxy) : seul le PAN effectue un téléchargement toutes les 30 secondes chez le producteur et les réutilisateurs téléchargent depuis le PAN.
{% endhint %}
