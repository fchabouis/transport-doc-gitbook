# Publier des horaires théoriques de transport régulier

### Étape 1 : Générer le jeu de données au format GTFS ou au format NeTEx

Deux **formats** principaux existent pour décrire des réseaux de transports publics :

* [**NeTEx**](http://netex-cen.eu/) : norme européenne visant l’interopérabilité des données entre États membres. Les opérateurs de transport et les autorités organisatrices de mobilité sont tenues de mettre à disposition des données suivant la norme NeTEx.
* [**GTFS**](https://developers.google.com/transit/gtfs/) : standard le plus utilisé par les services de mobilité d’information voyageur multimodale. Il est moins riche, mais plus répandu que le NeTEx et plus simple à utiliser \(plus d’outils compatibles et plus simple de développer ses propres outils\). C'est le format qui permettra aux usagers de votre territoire de bénéficier de services de mobilité innovants au plus vite.

{% hint style="info" %}
À moyen-terme, **la plateforme transport.data.gouv.fr proposera des outils de conversion de fichiers GTFS vers la norme NeTEx** afin de vous aider à vous conformer à la réglementation.
{% endhint %}

Dans la plupart des cas, **le fichier GTFS décrivant votre réseau de transport public existe déjà** : c’est en effet le standard classique utilisé par les services d’information voyageur \(Système d’Information Multimodal \(SIM\), applications de mobilité, projet de recherche, etc.\). 

Ce fichier GTFS est généralement généré par l’exploitant transport, à l’aide d’un Système d’aide à l’exploitation et à l’information voyageur \(SAEIV\). En cas de difficulté pour générer un fichier GTFS, n’hésitez pas à contacter [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr) pour être conseillé par notre équipe.

Nous mettons à disposition un [validateur](https://transport.data.gouv.fr/validation) afin de tester votre fichier GTFS avant la publication.

### Étape 2 : Accepter les conditions d’utilisation de la plateforme

Chaque jeu de donnée mis à disposition du public sous une licence de réutilisation qui spécifie les droits et devoirs des réutilisateurs lorsque ceux-ci téléchargent les fichiers en question, sans besoin d’identification.

Le Point d’Accès National propose l’utilisation de la [licence ODbL](https://vvlibri.org/fr/licence/odbl-10/legalcode/unofficial) pour permettre la réutilisation la plus large possible des données et accélérer le déploiement de services de mobilité innovants facilitant les déplacements des usagers.

{% hint style="info" %}
Dans la mesure où la [licence ouverte](https://www.etalab.gouv.fr/wp-content/uploads/2017/04/ETALAB-Licence-Ouverte-v2.0.pdf) dite "Etalab" est plus permissive que la licence ODbL et garantit une liberté de réutilisation sans clause de partage à l'identique, la publication des données sous cette licence convient également.
{% endhint %}

Sur transport.data.gouv.fr, un [cadre juridique harmonisé](../../presentation-et-mode-demploi-du-pan/cadre-juridique-harmonise.md) s'applique sur l'ensemble des données relatives aux horaires théoriques de transport régulier de personnes.

> _La réutilisation des informations disponibles sur transport.data.gouv.fr est soumise à la licence ODbL. Il est précisé que la clause de partage à l’identique figurant à l’article 4.4 concerne les informations de même nature, de même granularité, de même conditions temporelles et de même emprise géographique._

### Étape 3 : Identifier un référent pertinent, responsable de la publication du jeu de données, de sa mise à jour et de sa correction

Il est essentiel que pour chaque jeu de données publié, un point de contact soit clairement identifié. Cette personne pourra notamment :

* créer un compte personnel sur [data.gouv.fr](https://data.gouv.fr/) pour publier le jeu de données ;
* mettre à jour le jeu de données lorsque c’est nécessaire ;
* répondre aux questions des réutilisateurs sur les données et sur le réseau grâce au module de discussion de la plateforme ;
* s’assurer de l’amélioration de la qualité du fichier au fil de l’eau, en utilisant notamment les outils proposés sur le Point d’Accès National \([module de validation](https://transport.data.gouv.fr/validation)\).

### Étape 4 : Référencer le jeu de données sur le Point d’Accès National

Le référencement du jeu de données au format GTFS sur le Point d’Accès National est possible dès lors qu’une fiche a été publiée par le producteur de données sur la plateforme nationale data.gouv.fr. 

Pour une explication pas à pas de l’utilisation de la plateforme data.gouv.fr, se référer au [guide détaillé](http://www.opendatalab.fr/images/doc/Tuto_chargement_donnees_Opendata_v2.pdf) publié par le SGAR Occitanie.

* Créez un compte personnel sur data.gouv.fr ;
* Créez un profil _organisation_ au nom de votre structure \(exemple : « Métropole Européenne de Lille »\) ou demandez à rejoindre l’organisation relative à votre structure si elle existe déjà ;
* Avez-vous une **plateforme de données ouvertes locale** \(telles que OpenDataSoft ou CKAN\) ?
  * **Oui :** Configurez le moissonneur de data.gouv.fr qui référencera tous les jeux de données de votre plateforme locale et qui mettra à jour les métadonnées toutes les nuits.
  * **Non :** Créez une fiche sur data.gouv.fr pour publier le jeu de données GTFS au nom de votre organisation. Vous pouvez soit héberger le jeu de données en le téléchargeant sur la plateforme \(auquel cas il faudra le mettre à jour manuellement\), soit spécifier l’adresse \(URL\) permanente où est hébergé le fichier.

Quelques points à retenir :

* **Titre du fichier** : spécifiez le nom du réseau de transport et son agglomération ;
* **Mot-clé** : spécifiez « GTFS » ;
* **Description** : décrivez les spécificités du réseau et du fichier publié pour aider les réutilisateurs à faire bon usage de votre jeu de données ;
* **Licence** : nos recommandations sont la Licence [**ODbL**](https://opendatacommons.org/licenses/odbl/summary/) ou la [**Licence Ouverte Etalab**](https://www.etalab.gouv.fr/wp-content/uploads/2017/04/ETALAB-Licence-Ouverte-v2.0.pdf). Les fichiers publiés sous Licence Ouverte — plus permissive — seront référencés sous Licence ODbL + conditions d’utilisation sur le Point d’Accès National, selon le principe du « qui peut le plus peut le moins ».

### Étape 5 : Valoriser votre jeu de données pour en faire bénéficier le maximum de voyageurs

Nous vous proposons ici [quelques conseils pour valoriser vos données](jai-publie-un-fichier-gtfs.-et-maintenant.md) une fois qu'elles sont publiées. 

### Étape 6 – S'assurer de la mise à jour de vos données

Un jeu de données qui est expiré, c'est des applications utilisatrices qui perdent la matière première qui leur permet d'informer les usagers sur l'offre de transport disponible. C'est aussi le risque d'induire les usagers en erreur avec des horaires périmés. Voici [quelques recommandations pour vous assurer de la mise à jour de vos données](../mettre-a-jour-des-donnees.md). 



[  
](https://transport.data.gouv.fr/guide#mail_form)

