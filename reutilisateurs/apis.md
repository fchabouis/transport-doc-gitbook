# APIs

Un certain nombre d'outils sont mis à disposition pour automatiser l'utilisation de la plateforme.

## API principale

Plusieurs [APIs](https://transport.data.gouv.fr/swaggerui) sont disponibles.

Le point d'entrée principal de l'API est le [catalogue des jeux de données disponibles](https://transport.data.gouv.fr/api/datasets) sur la plateforme.

Il est aussi possible de récupérer le détail d'un jeu de données ce qui permet, entre autre, d'avoir l'historique de ce jeu de données :

```
https://transport.data.gouv.fr/api/datasets/{id}
```

## Flux RSS

Un [Flux RSS ATOM](https://transport.data.gouv.fr/atom.xml) est disponible pour être être notifié de la publication d'un nouveau jeu de données et de son URL fixe.

## API annexe

* Point d'accès GBFS pour les données des vélos en libre-service : [https://transport.data.gouv.fr/gbfs](https://transport.data.gouv.fr/gbfs)
