# Produire ses données

## Création d'un fichier de données conforme

Les données collectées doivent respecter un formalisme particulier (schéma de données) décrit sur [la page dédiée aux IRVE sur schema.data.gouv.fr](https://schema.data.gouv.fr/etalab/schema-irve/latest.html).

Les données sont à remplir au **format CSV**, encodage UTF-8.&#x20;

**Chaque ligne du fichier CSV doit correspondre à un point de recharge tel que défini dans le décret et**[ **retranscrit ici**](definitions.md)**.**&#x20;

**Chaque point de recharge dispose de son identifiant unique** _(soit dont le préfixe est délivré par l'AFIREV en cas d'itinérance, soit via l'utilisation de_ [_https://heidi.app.etalab.studio/_](https://heidi.app.etalab.studio/) _en cas d'identifiant local)_

Zoom sur les identifiants : ****&#x20;

* &#x20;Si la borne est en itinérance le “id\_pdc\_itinerance” débute par un préfixe délivré par l’AFIREV et composé de : “FR” + 3 caractères délivrés par l’AFIREV&#x20;
  * \+ “E” pour “EVSE” (Electric Vehicule Supply Equipment. Exemple : FRxyzE&#x20;
  * Idem pour le “id\_station\_itinerance” mais avec un “P” pour “Pool” pour désigner la station. Exemple : FRxyzP
* Si la borne n’est pas en itinérance, elle doit nécessairement avoir un id\_pdc\_local globalement unique (https://heidi.app.etalab.studio/)

Plusieurs solutions existent pour générer ce fichier CSV :&#x20;

* Outil d'aide à la saisie publier.etalab.studio
* Par vos propres moyens via un tableur

### **Utilisation de notre outil d'aide à la saisie**

Pour faciliter le remplissage des données, Etalab met à disposition un générateur CSV conforme au schéma de données, vous permettant de remplir les différents champs demandés. Cet outil vous permet de vous assurer que les données que vous remplissez sont au bon format. Pour l'utiliser, rendez-vous sur [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-irve), vous pourrez alors publier votre fichier à partir :

* d'un formulaire
* d'un tableur (encore en expérimentation)

![Choix du mode de saisie des données sur publier.etalab.studio](<../../.gitbook/assets/image (120).png>)

Une fois vos données chargées ou remplies, un formulaire vous proposera de les publier sur data.gouv.fr. Vous pouvez également à tout moment les télécharger au format CSV.

### **Production du fichier CSV par vos propres moyens**

Si vous désirez créer le fichier vous-même, vous pouvez partir de ce [fichier exemple](https://raw.githubusercontent.com/etalab/schema-irve/master/exemple-valide.csv).

Si vous préférez utiliser un logiciel tierce pour produire ce fichier, nous recommandons [LibreOffice](https://fr.libreoffice.org) (outil libre et gratuit) plutôt qu'Excel. La gestion des fichiers CSV y est en effet bien meilleure.

Une fois votre fichier produit, vous pouvez vous connectez sur [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-irve) pour vérifier que vos données ne comportent aucune erreur de format avant de les charger sur data.gouv.fr.

![Validation des données sur publier.etalab.studio](<../../.gitbook/assets/image (123).png>)

##
