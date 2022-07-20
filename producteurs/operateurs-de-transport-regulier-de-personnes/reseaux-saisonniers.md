# Réseaux saisonniers

Pour les offres de transports saisonniers ou non réguliers, hors transport à la demande (TAD), comme les réseaux scolaires ou les navettes de station de ski nous recommandons aux producteurs d'inclure le fichier [`feed_info.txt` ](https://developers.google.com/transit/gtfs/reference?hl=fr#feed\_infotxt)en complétant les champs `feed_start_date` et `feed_end_date`.\
Plus préconisations[ ici](https://gtfs.org/schedule/best-practices/#feed\_infotxt).&#x20;

La complétion de ces champs permettra aux producteurs de préciser qu'il n'y a pas de service dans le réseau jusqu'à une date précise. Ainsi, le GTFS n'apparaîtra pas comme étant périmé sur transport.data.gouv.fr &#x20;

