# Infrastructures de recharge de véhicules électriques \(IRVE\)

## Contexte

Dans le but de constituer un répertoire national des Infrastructures de recharge pour véhicules électriques \(IRVE\), ouvert et accessible à tous, les collectivités locales porteuses d’un projet d’installation d’IRVE doivent, au fur et à mesure de la mise en service des stations, publier sur la plateforme data.gouv.fr les données statiques relatives à la localisation et aux caractéristiques techniques de ces installations selon les modalités définies dans l’arrêté du [4 mai 2021.](https://www.legifrance.gouv.fr/jorf/id/JORFTEXT000043475441)

Etalab consolide l'ensemble des jeux de données produits par les différents acteurs territoriaux sur [un jeu de donnée consolidé](https://www.data.gouv.fr/fr/datasets/fichier-consolide-des-bornes-de-recharge-pour-vehicules-electriques/)\*. Celui-ci a pour objectif d'être le plus exhaustif possible et ambitionne de regrouper l'ensemble des bornes IRVE françaises.

Pour pouvoir être intégrés à ce fichier, les différents producteurs se doivent d'effectuer un certain nombre d'actions décrites sur cette page.

## Création d'un fichier de données conforme

Les données collectées doivent respecter un formalisme particulier \(schéma de données\) décrit sur [la page dédiée aux IRVE sur schema.data.gouv.fr](https://schema.data.gouv.fr/etalab/schema-irve/latest.html).

Les données sont à remplir au **format CSV**, encodage UTF-8.

Plusieurs solutions existent pour générer ce fichier CSV.

### **Utilisation de notre outil d'aide à la saisie**

Pour faciliter le remplissage des données, Etalab met à disposition un générateur CSV conforme au schéma de données, vous permettant de remplir les différents champs demandés. Cet outil vous permet de vous assurer que les données que vous remplissez sont au bon format. Pour l'utiliser, rendez-vous sur [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-irve), vous pourrez alors publier votre fichier à partir :

* d'un formulaire
* d'un tableur \(encore en expérimentation\)

![Choix du mode de saisie des donn&#xE9;es sur publier.etalab.studio](../.gitbook/assets/image%20%28120%29.png)

Une fois vos données chargées ou remplies, un formulaire vous proposera de les publier sur data.gouv.fr. Vous pouvez également à tout moment les télécharger au format CSV.

### **Production du fichier CSV par vos propres moyens**

Si vous désirez créer le fichier vous-même, vous pouvez partir de ce [fichier exemple](https://raw.githubusercontent.com/etalab/schema-irve/master/exemple-valide.csv).

Si vous préférez utiliser un logiciel tierce pour produire ce fichier, nous recommandons [LibreOffice](https://fr.libreoffice.org) \(outil libre et gratuit\) plutôt qu'Excel. La gestion des fichiers CSV y est en effet bien meilleure.

Une fois votre fichier produit, vous pouvez vous connectez sur [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-irve) pour vérifier que vos données ne comportent aucune erreur de format avant de les charger sur data.gouv.fr.

![Validation des donn&#xE9;es sur publier.etalab.studio](../.gitbook/assets/image%20%28123%29.png)

## Chargement des données sur data.gouv.fr

Pour mener à bien cette étape, il vous faudra préalablement créer un compte sur data.gouv.fr et vous affilier à une organisation si ce n'est pas déjà le cas \(voir sections ci-dessous\).

Une fois vos données prêtes, vous pouvez les charger sur data.gouv.fr directement depuis l'interface de l'outil [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-irve). Il vous faudra remplir un formulaire.

![Formulaire &#xE0; remplir avant de publier sa ressource sur data.gouv.fr](../.gitbook/assets/image%20%28121%29.png)

### **Création d'un compte**

Si vous n'en avez pas déjà un, créez un compte à votre nom sur [data.gouv.fr](https://www.data.gouv.fr).

📖 Référence : [https://doc.data.gouv.fr/gestion-du-compte/creer-un-compte/](https://doc.data.gouv.fr/gestion-du-compte/creer-un-compte/).

### **Création ou choix d'une organisation**

Si elle n'existe pas déjà, créez une organisation depuis votre compte. Cette organisation peut représenter votre collectivité ou votre société.

📖 Référence : [https://doc.data.gouv.fr/organisations/creer-une-organisation/](https://doc.data.gouv.fr/organisations/creer-une-organisation/)

Si l'organisation sous laquelle vous souhaitez publier existe déjà, vous pouvez la rejoindre

📖 Référence : [https://doc.data.gouv.fr/organisations/demander-a-rejoindre-une-organisation/](https://doc.data.gouv.fr/organisations/demander-a-rejoindre-une-organisation/).

## Et après ?

Une fois l'ensemble de ces actions réalisées, vos données seront correctement référencées sur la plateforme data.gouv.fr et automatiquement rassemblées dans le fichier consolidé des IRVE. La consolidation est aujourd'hui mensuelle \(tous les 25 du mois\).

_\*Vous pouvez accéder au code source permettant la génération de ce fichier_ [_ici_](https://github.com/etalab/notebooks/tree/master/irve)

