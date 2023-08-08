# API

{% hint style="info" %}
**Qu’est-ce qu’une API ?**

Une API est une interface, un contrat passé entre deux systèmes informatiques pour leur permettre de communiquer. Cette solution informatique permet d’automatiser des tâches depuis votre ordinateur ou vos serveurs.\
[Source](https://guides.data.gouv.fr/publier-des-donnees/guide-data.gouv.fr/api)[ : data.gouv.fr](https://guides.data.gouv.fr/publier-des-donnees/guide-data.gouv.fr/api)
{% endhint %}

## API data.gouv.fr pour publier les données



## API de transport.data.gouv.fr pour réutiliser les données&#x20;

Le PAN propose une API, sans authentification ni quota, en JSON. Elle diffuse des informations sur les jeux de données, ressources, AOMs, historisations, validations.

L'API permet :

* d'accéder automatiquement aux informations affichées sur le site web ;
* la construction d'automatisations spécifiques à vos besoins, en autonomie ;
* de suivre les dernières informations disponibles sur l'intégralité du catalogue du PAN.&#x20;

Plusieurs [APIs](https://transport.data.gouv.fr/swaggerui) sont disponibles.

### API principale

Le point d'entrée principal de l'API est le [catalogue des jeux de données disponibles](https://transport.data.gouv.fr/api/datasets) sur la plateforme.

Il est aussi possible de récupérer le détail d'un jeu de données ce qui permet, entre autre, d'avoir l'historique de ce jeu de données :

```
https://transport.data.gouv.fr/api/datasets/{id}
```



