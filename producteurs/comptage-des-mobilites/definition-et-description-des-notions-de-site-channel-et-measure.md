# Définition et description des notions de site, channel et measure

{% hint style="danger" %}
Cette documentation est en cours de rédaction : elle sera finalisée prochainement.  
Pour toute remarque, n'hésitez pas à nous contacter à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)
{% endhint %}

Le schéma national des mobilités est composé de trois entités, aussi appelées "notion" dans cette documentation :   
- Site  
- Channel  
- Measure

Pour l'instant, chacune de ces notions a sa propre page sur schema.data.gouv.fr car des limitations techniques ne permettaient pas de les héberger sur la même page. Chaque entité a son propre fichier. Ces fichiers s’articulent entre eux grâce à des identifiants. 

![](../../.gitbook/assets/image%20%28164%29.png)

Ainsi, le fichier “channel” ne peut être réutilisé sans l’identifiant du fichier “site” et le fichier “measure” ne peut être compris ni réutilisé sans les identifiants des fichiers “site” et “channel”.  
Vous trouverez, ci-dessous, une description de chacune de ses notions.  

{% hint style="info" %}
Cette documentation sera enrichie grâce aux retours des producteurs et réutilisateurs. N'hésitez pas à nous contacter à l'adresse :  [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr) si vous souhaitez que nous clarifions d'autres champs. 
{% endhint %}

## 1. Site 

Le fichier site permet de décrire les réalités physiques du site de comptage des mobilités. Ainsi, le “site” représente un lieu physique, auquel les “channels” sont rattachés. Un site a une position géographique immuable \(latitude/longitude\), dispose d’un code commune de rattachement, d’un type de voie. Le champ "bike\_path\_ids" permet notamment d'articuler le schéma au [schéma national des aménagements cyclables](https://schema.data.gouv.fr/etalab/schema-amenagements-cyclables/latest.html). 

## 2. Channel

La notion de "channel" a été introduite pour faire le lien entre la réalité immuable physique du site, et les mesures fournies par des “compteurs physiques”.  
Ce fichier définit les modalités techniques de comptage \(types de pratiques mesurées, méthode utilisée pour récupérer les données\), et permet de regrouper entre elles des mesures. À l’inverse, un channel ne définit pas d’identifiant physique du compteur, de façon volontaire.  
Ceci permet de faire en sorte qu’un premier compteur physique émette des données sur un channel de 10h à 11h, puis qu’un deuxième compteur physique prenne le relais de 11h à 12h, sans changement du channel lui-même \(continuité de la série temporelle des mesures\).  
Cette capacité permet notamment de gérer correctement:

* les changements de compteur physique \(opération de maintenance, compteur défectueux, interruption temporaire\)
* les réaffectations à un site différent de compteurs physiques, sous forme de “compteurs temporaires”.

## **3. Measure**

Le fichier measure contient les données de comptage. Ce fichier est dit “dynamique” car les données seront amenées à être fréquemment mises à jour selon le pas de temps ou la fréquence de rafraîchissement que le producteur définira en amont.   
Les données fournies le sont soit en "temps-réel", soit à posteriori. 

