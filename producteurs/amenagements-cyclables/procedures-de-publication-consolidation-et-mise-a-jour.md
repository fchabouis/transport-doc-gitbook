# Procédures de publication, consolidation et mise à jour

### Procédures de publication&#x20;

Les jeux de données seront publiées au format GeoJSON. Certains champs sont obligatoires et d'autres optionnels. Les champs obligatoires doivent être complétés. Les champs optionnels peuvent être vides si la donnée n’est pas disponible. La colonne doit toutefois être présente.

Les producteurs pourront saisir leurs données sur :&#x20;

* des outils internes ;&#x20;
* l'outil développé par Vélo & Territoires ;
* OpenStreetMap (OSM) ;&#x20;

Géovélo a également mis en place une conversion des données sur les aménagements cyclables vers le s[chéma national ](https://schema.data.gouv.fr/etalab/schema-amenagements-cyclables/latest.html)pour leurs clients.&#x20;

Avant de publier les données, nous recommandons aux producteurs d'évaluer la qualité de leurs ressources en utilisant le validateur de fichier disponible dans l'onglet "Outils" > "Evaluer la qualité d'un fichier" de la page d'accueil de transport.data.gouv.fr. \
![](<../../.gitbook/assets/image (174).png>)\
Veuillez ensuite sélectionner "Aménagements cyclables" comme type de fichier.&#x20;



Pour la publication des données, les producteurs pourront :

* publier directement sur [data.gouv.fr ](https://www.data.gouv.fr/fr/)

Pour publier sur [data.gouv.fr](https://www.data.gouv.fr/fr/), vous aurez à créer un [compte personnel](https://doc.data.gouv.fr/gestion-du-compte/creer-un-compte/) puis un [compte pour votre organisation](https://doc.data.gouv.fr/organisations/creer-une-organisation/). Vous pourrez ensuite publier des jeux de données à travers votre compte organisation.&#x20;

* déléguer la publication des données à Vélo & Territoires si les données ont été saisie sur leur outil\

* déléguer la publication des données à Géovélo

Vous trouverez un schéma résumant les différents modes de production et de publication ici édité par la Direction Départementale des Territoires et de la Mer (DDTM) des Pyrénées-Atlantiques :&#x20;

![](../../.gitbook/assets/schema-de-saisie-des-amenagements-cyclablesv3.png)

Nous préconisons aux producteurs de données de publier leurs fichiers avec la règle de nommage suivante : amenagementcyclable\_nom.geojson avec nom étant le nom de la collectivité productrice des données, par exemple AménagementCyclable\_Ain.geojson

Nous encourageons également les producteurs à spécifier que le fichier déposé repose sur le schéma d'aménagements cyclables dans la section "schéma" (liste déroulante) et que le fichier est au format GeoJSON dans la section "format" lorsqu'ils publieront leurs données à partir de leur espace administrateur [data.gouv.fr](https://www.data.gouv.fr/fr/).&#x20;

![](<../../.gitbook/assets/image (124).png>)

### Consolidation&#x20;

Deux bases seront publiées sur transport.data.gouv.fr :&#x20;

* une base nationale regroupant les données publiées par les collectivités sur [data.gouv.fr](https://www.data.gouv.fr/fr/) ;
* une base rassemblant les données publiées sur OSM. Vélo & Territoires sera en charge de l'extraction de ces données.&#x20;

### Mise à jour

La consolidation de la base sera effectuée en continu par [transport.data.gouv.fr](https://transport.data.gouv.fr) à partir des fichiers publiés sur [data.gouv ](https://www.data.gouv.fr/fr/)avec le tag “aménagements cyclables” par les producteurs et Vélo & Territoires.  des fichiers importés depuis OpenStreetMap ou directement transmis par mail. De nouvelles versions seront publiées lorsque de nouveaux aménagements cyclables seront recensés ou mis-à-jour par les producteurs de données. Cette mise à jour se fait à partir du fichier communiqué précédemment et en reprenant, en les modifiant le cas échéant, les données existantes. Le fichier principal du dataset constitue ainsi systématiquement la dernière mise-à-jour.



Nous tenons à remercier les membres du groupe de travail pour leur investissement dans l'élaboration de ce schéma.
