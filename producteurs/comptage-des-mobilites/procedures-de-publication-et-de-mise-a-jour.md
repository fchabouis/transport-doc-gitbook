# Procédures de production, publication et de mise à jour

{% hint style="danger" %}
Cette documentation est en cours de rédaction : elle sera finalisée prochainement.  
Pour toute remarque, n'hésitez pas à nous contacter à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)
{% endhint %}

Les fichiers issus du schéma national de comptage des mobilités devront être au format csv, encodé en UTF8 avec séparateur virgule ",". Certains champs sont obligatoires et d'autres optionnels. Les champs obligatoires doivent être complétés. Les champs optionnels peuvent être vides si la donnée n’est pas disponible. La colonne doit toutefois être présente.

Chacune des notions est retranscrite dans son propre fichier :

* les sites vont dans un fichier “sites.csv” avec une ligne par site
* les channels dans un fichier “channels.csv” avec une ligne par channel
* les mesures dans un fichier “measures.csv” avec une ligne par mesure

## Production des fichiers 

{% hint style="info" %}
Cette partie explique comment les fichiers sont structurés. 

Les procédures de production sont en cours de définition. Nous enrichirons prochainement cette documentation.
{% endhint %}

### Le fichier sites.csv 

Chaque site physique est retranscrit sous la forme d’une ligne dans le fichier “sites.csv”.  
Une nouvelle ligne doit être créée dans le fichier lorsque :

* le site de comptage a été déplacé \(coordonnées modifiées\)
* le type de voie où se trouve le site est modifié. Par exemple, si une bande cyclable devient une piste cyclable car cela permet de mieux interpréter l’évolution des chiffres

### Le fichier channel.csv

Chaque "channel" est retranscrit sous la forme d’une ligne dans le fichier “channel.csv”. Un channel mesure un seul sens de circulation \(ou une absence de sens de circulation\), orienté à l’aide d’un point cardinal pour des questions de simplicité. Pour modéliser plusieurs directions, il convient de définir plusieurs channels. Le producteur fera donc autant de lignes qu’il y a de directions   
Une nouvelle ligne doit être créée dans le csv lorsque : 

* la pratique du comptage change. En effet, un changement de pratique de “vélo” à “vélo + piéton” fausserait les données en terme d’analyse.
* la méthode utilisée pour récupérer les données a changé
* il y a plusieurs directions distinctes sur un site
* le pas de temps est modifié 
* une date de fin de comptage a été renseignée. Le channel est alors considéré comme clos. 

### Le fichier measure.csv 

Le CSV contiendra autant de ligne que de comptage par créneau temporel ou par pas de temps. 

## Maintenir à jour les données 

Dans le but de maintenir à jour des données sur les comptages des mobilités en France, les collectivités sont invitées à transmettre systématiquement les données relatives aux compteurs sur leur territoire. Elles peuvent ajouter le mot-clef "comptage-mobilité" lors de la publication de leur jeu de données. Les producteurs pourront 

* publier directement sur data.gouv.fr ;
* publier sur un portail local ou régional et s'assurer que les données publiées sont bien[ moissonnées](https://doc.data.gouv.fr/jeux-de-donnees/demander-a-datagouvfr-de-moisonner-votre-site/) et référencées sur data.gouv.fr.

