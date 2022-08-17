# Foire aux questions

#### Comment le schéma a-t-il été conçu ?

Le schéma découle de nombreuses discussions avec les parties-prenantes (collectivités, réutilisateurs, etc) lors de deux ateliers organisés par les équipes de transport.data.gouv.fr. Il a été pris en compte les contraintes des producteurs et les besoins des réutilisateurs pour proposer le schéma le plus simple possible, permettant de décrire facilement des points de rencontre en covoiturage.

L'harmonisation des jeux de données facilite la tâche aux réutilisateurs, qui n'ont alors pas à réaliser des développements spécifiques pour chaque territoire qu'ils souhaitent intégrer à leur service, en gérant des formats ou des conventions de nommage différents. **Grâce au schéma proposé, une** [**base nationale consolidée** ](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/)**peut être mise à disposition pour valoriser les données ouvertes par les producteurs et accélérer le déploiement d'une information fiable pour les covoitureurs, partout en France.**

#### Qu'est-ce que l'identifiant unique ? A quoi sert-il ?

Mettre à disposition une base nationale consolidée présente de nombreux enjeux de qualité et de mise à jour des données. Afin de garantir une mise à jour facilitée de cette base, Transport.data.gouv.fr a attribué un identifiant unique national à chaque lieu de covoiturage (format "_**INSEE-C-000**_") pour faciliter la mise à jour des jeux de données existants. C'est le champ "[id\_lieu](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html#propriete-id-lieu)" du[ schéma national](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html). Ainsi, lorsqu'un producteur souhaite modifier une ligne décrivant un lieu de covoiturage, il peut signaler la modification. \
Cet identifiant est généré automatiquement dans l'[outil Contribuer](https://contribuer.transport.data.gouv.fr/). Si le producteur n'utilise pas cet outil, il devra composer lui même cet identifiant en faisant attention aux identifiants déjà existants.&#x20;

#### **Ma collectivité a déjà publié un jeu de données, dois-je republier une base ?**

Grâce au travail des équipes de Blablacar en 2018 puis de celles de Transport.data.gouv.fr, tous les jeux de données disponibles sur data.gouv.fr en juin 2019 ont été adaptés au schéma proposé ici. Cela signifie que si votre jeu de données avait déjà été publié, il y a de fortes chances que vous n'ayez rien à faire : les lieux de covoiturage de votre ressort territorial devraient déjà être inclus à la [base nationale consolidée](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/).

#### Je souhaite mettre à jour les lieux de covoiturage de ma base nationale consolidée.

Vous pouvez, au choix :  &#x20;

* utiliser l'[outil Contribuer](https://contribuer.transport.data.gouv.fr/) ;
* transmettre un message à contact@transport.beta.gouv.fr avec vos données pour nous demander la mise à jour ;&#x20;
* publier une version conforme au schéma sur data.gouv.fr en incluant le mot-clé "_**covoiturage**_" pour que le jeu de données soit identifié lors de la prochaine mise à jour. \
  Attention : si les lieux de covoiturage existaient déjà, un identifiant unique leur a été attribué. Pour modifier la description d'un jeu de données existant, il vous faudra utiliser le même pour que la mise à jour soit prise en compte. Nous vous conseillons donc de partir de la base nationale la plus récente, d'en extraire les lignes correspondant à votre ressort territoriale, et à effectuer les modifications directement dans le fichier. Vous pouvez utiliser le champ "[id\_local](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.4/documentation.html#propriete-id-local)" pour renseigner les identifiants que vous utilisez en interne et retrouver plus facilement vos données dans la base.

Nous nous efforcerons de faciliter votre travail au fil de vos retours pour rendre ce processus plus simple.\
Plus d'information sur la contribution à la base consolidée [ici](https://doc.transport.data.gouv.fr/producteurs/lieux-de-covoiturage/contribuer-a-la-base-nationale-des-lieux-de-covoiturage).

#### Je souhaite intégrer de nouveaux lieux de covoiturage

Si les lieux de covoiturage de votre ressort territorial ne sont pas référencés sur la base nationale consolidée, vous pouvez utiliser :&#x20;

* l'[outil Contribuer ](https://contribuer.transport.data.gouv.fr/)
* [le formulaire de génération de données valides](https://forms.validata.etalab.studio/?schema=etalab%2Fschema-lieux-covoiturage) pour créer un jeu de données conforme au schéma et le publier sur data.gouv.fr avec le mot-clé "_**covoiturage**_". Il sera intégré sous peu par les équipes de transport.data.gouv.fr dans la base consolidée.

{% hint style="warning" %}
Pensez à bien vérifier la qualité de vos données avant de les publier. Seules les données valides seront intégrées à la base.
{% endhint %}

**Qui réutilise cette base ?**

Cette base a vocation à être utilisée par les services de mobilité intégrant le covoiturage pour informer les usagers sur les lieux où ils peuvent s'arrêter pour déposer ou prendre en charge des covoitureurs, en toute sécurité. Les réutilisateurs de cette base peuvent déclarer leur réutilisation de manière volontaire dans la section [Réutilisations](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/#dataset-reuses) de la [page du jeu de données](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/).&#x20;





**J'ai d'autres questions sur cette base**

N'hésitez pas à nous contacter : contact@transport.beta.gouv.fr.





