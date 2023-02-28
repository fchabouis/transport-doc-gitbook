# Référencement de votre réseau sur Google Maps

## 1. Référencement dans Google Maps grâce à l'article 122 - Loi Climat et Résilience

Afin d'être intégré dans Google Maps, nous préconisons aux producteurs de favoriser l'emploi de la licence ouverte puisqu'elle permet au mieux de favoriser la réutilisation des données. En particulier, conformément aux dispositions de l’article 122 de la loi Climat & résilience, et selon les modalités définies par le[ décret n°2022-1119 du 3 août 2022](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000046144256), **les données sous licence ouverte Etalab font l’objet d’une obligation de réutilisation dans l’ensemble des calculateurs multimodales.**

Ainsi, aucune autre démarche ne sera nécessaire de votre part pour intégrer vos données dans Google Maps. Google Maps se chargera de les mettre en qualité et de les intégrer de son côté.&#x20;

Quelques points de vigilance cependant :&#x20;

* Veiller à maintenir une url de téléchargement stable pour que l'import des données se fasse automatiquement et sans rupture
* Veiller à publier des jeux de données d'une bonne qualité : voir section [Mise en qualité des GTFS](https://doc.transport.data.gouv.fr/producteurs/operateurs-de-transport-regulier-de-personnes/mise-en-qualite-des-donnees-gtfs)&#x20;

## 2. Demande de référencement auprès de Google Maps

Depuis janvier 2019, le service Google Maps fait partie des services numériques consommant des données ouvertes sous licence ouverte ou ODbL conditions particulières via la plateforme transport.data.gouv.fr. Afin de faciliter l’intégration à l’application Google Maps pour les producteurs de données qui le souhaitent, une procédure d’intégration simplifiée a été mise en place grâce au régime de l’ouverture des données. En l’espèce, **une fois un jeu de données GTFS (ou GTFS-RT) publié sur la plateforme transport.data.gouv.fr en licence ODbL, le contrat bilatéral entre Google et le producteur de données (**_**Google Transit Agreement**_**) n’a plus lieu d’être**.

Cependant, en raison des critères de qualité propres à l’application Google Maps, la procédure d’intégration demande une implication importante du producteur de données pour mettre en qualité les jeux de données.

### Procédure pour référencement des données d'un réseau de transports sur Google Maps

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

#### 3e étape : mise à jour des mentions légales de Google Maps&#x20;

Une fois que le flux est approuvé par Google et par le producteur, il est publié sur Google Maps, qui met à jour ses [mentions légales](https://www.google.com/help/legalnotices\_maps/).

****\
****Dans le cas où le producteur de données n’a pas la capacité d’allouer des ressources à la mise en qualité du jeu de données, Google peut s'occuper de la mise en qualité du flux – mais cela dépend de la feuille de route et des priorités de l’entreprise. Le flux amélioré est partagé avec la communauté Open data, idéalement au travers de la plateforme [transport.data.gouv.fr](http://transport.data.gouv.fr/), et la page de mentions légales est mise à jour. Nous recommandons cependant de profiter du temps et des outils de Google afin de mettre en qualité le jeu de données publié dans le pot commun.
