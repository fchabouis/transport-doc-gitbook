# Outils pour les réutilisateurs

### Extraire un jeu de données d'un GTFS agrégé

Certaines régions \(Bretagne, Nouvelle-Aquitaine\) proposent un jeu de données qui agrège les transports urbains et interurbains de la zone.

Si vous souhaitez extraire un seul réseau de ce jeu de données, voici une manière de le faire automatiquement.

Nous cherchons à extraire le réseau Carabus du GTFS agrégé `naq-aggregated-gtfs.zip.`

1. Identifier le réseau à extraire :
   * Dans le GTFS, choisir le réseau à isoler à partir du fichier agency.txt
   * Noter le `agency_id`
   * Par exemple pour Carabus, `CAR:Authority:1`
2. Utilisez l’outil OneBusAway :
   * Télécharger sur [http://developer.onebusaway.org/modules/onebusaway-gtfs-modules/1.3.4-SNAPSHOT/onebusaway-gtfs-transformer-cli.html](http://developer.onebusaway.org/modules/onebusaway-gtfs-modules/1.3.4-SNAPSHOT/onebusaway-gtfs-transformer-cli.html)
   * Exécuter :`java -jar onebusaway-gtfs-transformer-cli-1.3.4-20150503.062227-12.jar --transform='{"op": "retain", "match": {"file": "agency.txt", "agency_id": "CAR:Authority:1"}}' naq-aggregated-gtfs.zip carabus.zip`
3. Vous obtenez un fichier `carabus.zip` avec uniquement ces données-là.

L’outil de OneBusAway permet de nombreuses autres manipulations. N’hésitez pas à explorer la documentation.

Ainsi, pour n’avoir que les lignes fluviales de Nantes, exéctuer :

```bash
java -jar onebusaway-gtfs-transformer-cli-1.3.4-20150503.062227-12.jar --transform='{"op": "retain", "match": {"file": "routes.txt", "route_type": 4}}'  gtfs-tan.zip nantes_ferry.zip
```





