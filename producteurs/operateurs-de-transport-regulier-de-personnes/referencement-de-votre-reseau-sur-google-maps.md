# Référencement de votre réseau sur Google Maps

## 1. Référencement dans Google Maps grâce à l'article 122 - Loi Climat et Résilience

Afin d'être intégré dans Google Maps, nous préconisons aux producteurs de favoriser l'emploi de la licence ouverte puisqu'elle permet au mieux de favoriser la réutilisation des données. En particulier, conformément aux dispositions de l’article 122 de la loi Climat & résilience, et selon les modalités définies par le[ décret n°2022-1119 du 3 août 2022](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000046144256), **les données sous licence ouverte Etalab font l’objet d’une obligation de réutilisation dans l’ensemble des calculateurs multimodales comme Google Maps.**

Ainsi, dès lors que vous publiez un GTFS sous licence ouverte, Google sera notifié et procèdera à son intégration.&#x20;

Aucune autre démarche ne sera nécessaire de votre part pour intégrer vos données dans Google Maps. Google Maps se chargera de les mettre en qualité (ajout des couleurs si absentes de vos données, vérification de la géolocalisation des arrêts...) et de les intégrer de son côté.&#x20;

Les délais d'intégration dépendront de vos données, nous pouvons si besoin faire l'intermédiaire avec Google Maps si vous souhaitez avoir une idée (contact@transport.beta.gouv.fr).&#x20;

**Quelques points de vigilance cependant pour que l'intégration dans Google Maps se passe au mieux :**&#x20;

* Veiller à **maintenir une url de téléchargement stable** pour que l'import des données se fasse automatiquement et sans rupture : pour cela, à chaque changement d'offre remplacer le dernier GTFS par le nouveau. Voir section [Remplacer un jeu de données existant](https://doc.transport.data.gouv.fr/producteurs/mettre-a-jour-des-donnees#remplacer-un-jeu-de-donnees-existant-plutot-quen-creer-un-nouveau)
* Veiller à **publier des jeux de données d'une bonne qualité** :&#x20;
  * **Qualité "commerciale"** sur le contenu de votre GTFS :  voir section [Mise en qualité des GTFS](https://doc.transport.data.gouv.fr/producteurs/operateurs-de-transport-regulier-de-personnes/mise-en-qualite-des-donnees-gtfs)&#x20;
  * **Qualité technique** : votre GTFS ne doit pas contenir d'erreurs auquel cas il risque d'être refusé par Google Maps. Pour cela, vous pouvez utiliser les outils de validation disponibles sur le PAN.

## 2. Demande de référencement auprès de Google Maps

Si vous souhaitez avoir la main sur l'intégration de vos données dans Google Maps, c'est tout à fait possible. Pour cela, il faudra passer par le process habituel qui demande une implication importante de la part du producteur pour aboutir à la publication du réseau sur Google Maps :&#x20;

* Demande de référencement auprès de transit-partners@google.com
* Process de mise en qualité des données entre le producteur et l'AOM (étape la plus longue en fonction de la qualité de vos données)
* Publication des données

Ces étapes sont détaillées dans la suite de ce paragraphe.

#### 1ère étape : demande expresse du producteur de données&#x20;

Le producteur de données exprime son souhait d’intégration sur Google Maps en transmettant une demande à transit-partners@google.com.

La personne qui sera mise en relation avec les équipes techniques de Google devrait être dans l’idéal une technicienne ou un technicien capable de modifier le GTFS afin de l’améliorer selon les retours des modules de validation Google.

#### 2e étape : mise en qualité des données&#x20;

Les équipes techniques de Google travaillent avec la technicienne/le technicien désigné·e par le producteur de données (durée : quelques semaines à quelques mois, selon la réactivité des deux parties et la qualité du fichier initial).

{% hint style="info" %}
**Attention :** les échanges se feront exclusivement en anglais. Durant tout le processus de mise en qualité, nous conseillons de laisser les équipes transport.data.gouv.fr en copie des échanges, afin que nous puissions intervenir en cas de situations bloquantes.
{% endhint %}

* Google Transit met à disposition un espace sur un compte partenaire (“_partnerdash_”) ;
* Le module de validation de Google établit un diagnostic sur le GTFS, qu’il conviendra de corriger. D’expérience, nous savons que certains “_Warnings_” ne seront pas pertinents, l’outil de Google étant extrêmement rigide. Il faudra alors confirmer que le GTFS est valide pour une information voyageur fiable, malgré les “_Warnings_” exposés sur le “_partnerdash_”.
* Le producteur, une fois satisfait des calculs d’itinéraires visibles dans l’environnement de test, remplit [un questionnaire](https://support.google.com/transitpartners/contact/ready\_to\_launch) pour valider le lancement.

{% hint style="info" %}
L’expérience des producteurs de données en France ayant travaillé avec les équipes techniques de Google Transit montre que la discussion peut être longue car les critères de qualité sont stricts. Cependant, ce temps n'est pas perdu, puisqu'il permet de réintéroger les process internes afin de contribuer à fournir des données plus qualitatives, pas seulement à Google, mais à l'ensemble de la communauté Open Data, pour une information voyageur beaucoup plus fiable.&#x20;
{% endhint %}

#### 3e étape : publication des données et mise à jour des mentions légales de Google Maps&#x20;

Une fois que le flux est approuvé par Google et par le producteur, il est publié sur Google Maps, qui met à jour ses [mentions légales](https://www.google.com/help/legalnotices\_maps/).

\
Le flux amélioré est partagé avec la communauté Open data, idéalement au travers de la plateforme [transport.data.gouv.fr](http://transport.data.gouv.fr/), et la page de mentions légales est mise à jour. Nous recommandons cependant de profiter du temps et des outils de Google afin de mettre en qualité le jeu de données publié dans le pot commun.
