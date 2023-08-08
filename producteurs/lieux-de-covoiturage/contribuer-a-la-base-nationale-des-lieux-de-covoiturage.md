# Contribuer à la Base Nationale des Lieux de Covoiturage (BNLC)

La [base nationale des lieux de covoiturage ](https://transport.data.gouv.fr/datasets/base-nationale-des-lieux-de-covoiturage/)(BNLC) tend à recenser l'ensemble des lieux, points de départ ou d'arrivée, propices au covoiturage. Elle est structurée selon le [schéma national des lieux de covoiturage](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/).

Pour y contribuer, en ajoutant de nouveaux lieux de covoiturage ou en actualisant des lieux de covoiturage déjà référencés, vous pouvez utiliser une des méthodes présentées ci-dessous. Nous vous conseillons l'utilisation de la première méthode, qui utilise l'outil "[Contribuer](contribuer-a-la-base-nationale-des-lieux-de-covoiturage.md#utiliser-loutil-daide-a-la-contribution-contribuer-conseille)".

### Utiliser l'outil d'aide à la contribution "[Contribuer](https://contribuer.transport.data.gouv.fr/)" (<mark style="color:green;">conseillé</mark>)

Cet outil a été développé spécifiquement pour faciliter la contribution des producteurs de données à la BNLC.

{% hint style="info" %}
Pour la suite des opérations, nous vous conseillons d'utiliser [LibreOffice Calc](https://fr.libreoffice.org/download/telecharger-libreoffice/) (alternative gratuite à Microsoft Excel).
{% endhint %}

<details>

<summary>Etape 1 - Récupérer la dernière version de la BNLC</summary>

La BNLC est **un fichier CSV unique** qui contient l'ensemble des lieux de covoiturages. Chaque contributeur apporte sa pierre à l'édifice (la BNLC) déjà existant.

Pour contribuer, il convient de récupérer la dernière version du fichier et de **modifier celui-ci** en ajoutant et/ou modifiant des lieux de covoiturage.

Pour récupérer la dernière version, rendez-vous sur l'outil "[Contribuer](https://contribuer.transport.data.gouv.fr/)" et cliquer le lien **"Télécharger la base actuelle"**.

![](<../../.gitbook/assets/image (2) (4).png>)

</details>

<details>

<summary>Etape 2 - Ouvrir le fichier BNLC</summary>

En ouvrant un fichier CSV, LibreOffice Calc **peut interpréter des données et les modifier de lui-même**.

Par exemple, le code postal "_07300_" peut être identifié comme un nombre. Il sera alors automatiquement modifié en "_7300_", sans action de votre part. Si vous importez ce fichier via l'outil Contribuer, **la BNLC se retrouvera avec ces modifications, et donc, des données erronées**.

**Ouvrez le fichier avec LibreOffice Calc**, une fenêtre va vous permettre de préciser comment doit être interprété le fichier.

Vérifiez que : \
\- **l'encodage** soit bien en UTF-8 ; \
\- le seul **séparateur** coché soit la virgule (comma) ;\
\- le **délimiteur** des champs soit des guillemets.

![](<../../.gitbook/assets/image (4) (3).png>)



Ensuite, toujours dans cette fenêtre, il faut spécifier à LibreOffice Calc d'**interpréter toutes les colonnes comme du text**e.&#x20;

Pour cela, \
1- **cliquez sur le rectangle en haut à gauche** de l'aperçu des données afin de sélectionner toutes les colonnes ;\
2- **modifier le type des colonnes** sélectionnées sur "Texte".\


![](<../../.gitbook/assets/image (5) (1).png>)



Vous pouvez à présent cliquer sur "**OK**" pour ouvrir le fichier CSV de la BNLC.

</details>

<details>

<summary>Etape 3 - Ajouter de nouvelles données</summary>

L'ajout de nouveaux lieux de covoiturage se fait **à la fin du fichier**. Ces lieux doivent respecter le [schéma national des lieux de covoiturage](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/).

Les coordonnées géographiques ([Xlong](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.8/documentation.html#propriete-xlong), [Ylat](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.8/documentation.html#propriete-ylat)) doivent être renseignées **au format WGS 84**. Vous pouvez vous aider de [Geoportail](https://www.geoportail.gouv.fr/carte) pour trouver ces coordonnées sur une carte. En faisant clique droit sur l'endroit du lieu de covoiturage et en cliquant ensuite sur "Adresse/coordonnées du lieu" \
![](<../../.gitbook/assets/image (5).png>)

&#x20;une fenêtre s'ouvrira en haut à gauche. Vous trouverez les coordonnées du lieu au format WGS 84. Le premier nombre correspond à la colonne Xlong et le second à la colonne Ylat. \
![](<../../.gitbook/assets/image (6).png>)

La colonne [`id_lieu`](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.8/documentation.html#propriete-id-lieu) ne doit pas être complétée, un identifiant national sera automatiquement créé lors de l'envoi du fichier via l'outil "Contribuer".

La colonne [`id_local`](https://schema.data.gouv.fr/etalab/schema-lieux-covoiturage/0.2.8/documentation.html#propriete-id-local) n'est pas obligatoire, mais elle vous permet de garder le lien entre la BNLC et vos données source. Il est conseillé d'établir une identification des lieux de covoiturage au sein de votre organisation et de compléter cette colonne avec ceux-ci.

</details>

<details>

<summary>Etape 4 - Modifier des données existantes</summary>

Vous êtes libres de modifier vos données, tout en gardant la colonne `id_lieu` intacte. En effet, cette colonne permet aux réutilisateurs de garder le lien avec le lieu de covoiturage, indépendamment de son nom, ses coordonnées géographiques, etc.

Il vous est possible de modifier **des lieux de covoiturage qui ne sont pas les vôtres**. Cependant, nous vous conseillons plutôt, en cas d'anomalie repérée, de nous contacter afin que nous puissions informer le producteur de ces données. Cela lui permettra d'actualiser les données de son côté ainsi que du côté de la BNLC.

</details>

<details>

<summary>Etape 5 - Sauvegarder le fichier</summary>

Lors de la sauvegarde, nous vous conseillons de créer une copie du fichier en utilisant **"Enregistrer sous"** (via le menu "**Fichier**" de LibreOffice Calc).

Cochez la case "**Edit filter settings**" et cliquez sur "**Enregistrer**"

![](<../../.gitbook/assets/image (1) (5).png>)



Dans la nouvelle fenêtre affichée, vérifiez que les paramètres sont renseignés comme présentés ci-dessous.

![](<../../.gitbook/assets/image (7) (2).png>)



Cliquez sur "**OK**" pour confirmer l'enregistrement du fichier CSV.

</details>

<details>

<summary>Etape 6 - Charger le fichier sur l'outil Contribuer</summary>

Rendez-vous sur l'outil "[Contribuer](https://contribuer.transport.data.gouv.fr)" (le même que dans l'étape 1).

**Chargez votre fichier** au niveau du point 3 sur l'outil.

![](<../../.gitbook/assets/image (9).png>)

Votre fichier est alors **immédiatement vérifié** : respect du schéma de données, ainsi que les ajouts et modifications.

Un message vous indique ensuite si votre fichier est conforme ou non.

</details>

<details>

<summary>Etape 7 ✅ - Vos contributions sont valides</summary>

Vous pouvez visualiser la localisation de vos ajouts en cliquant sur "_**🗺️ Voir la carte**_" avant de soumettre vos modifications.&#x20;

\
Un formulaire s'affiche (point 4) et vous permet de renseigner vos informations et d'envoyer le fichier pour analyse par l'équipe du PAN avant l'ajout à la BNLC.

</details>

<details>

<summary>Etape 7 ❌ - Vos contributions ne sont pas valides</summary>

Téléchargez le fichier à travers le lien "**ce fichier**". Il correspond à votre fichier, avec la colonne `id_lieu` complétée. Ce fichier sera nommé _"bnlc-for-validata"_.

![](<../../.gitbook/assets/image (3) (3).png>)

Rendez-vous sur le [validateur](https://validata.etalab.studio/table-schema?schema\_name=schema-datagouvfr.etalab%2Fschema-lieux-covoiturage) pour avoir plus de détails sur les éléments invalides. Corrigez-les puis réessayez.

**Vous devez rafraichir la page de l'outil "**[**Contribuer**](https://contribuer.transport.data.gouv.fr/)**"** (ou de la fermer et de l'ouvrir à nouveau) à chaque fois que vous souhaitez charger un fichier

</details>

Vous avez des idées d'améliorations pour faciliter les contributions à travers cet outil ? Proposez les nous à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)&#x20;



### Publier les données sur [data.gouv.fr](https://data.gouv.fr)

Un guide dédié à la contribution est accessible [via ce lien](https://www.data.gouv.fr/fr/pages/onboarding/producteurs/).

Votre contribution concerne alors uniquement les lieux de covoiturage qui vous concernent.

L'équipe du PAN fera manuellement l'ajout de vos données dans la BNLC.

{% hint style="info" %}
Veuillez préciser que les données sont structurées selon le schéma national des lieux de covoiturage dans l'onglet "schema" > Lieux de covoiturage.\
![](<../../.gitbook/assets/image (169) (1).png>)
{% endhint %}



### Utiliser les formulaires de [publier.etalab.studio](https://publier.etalab.studio/select?schema=etalab%2Fschema-lieux-covoiturage)

La plateforme schema.data.gouv propose deux outils pour faciliter la saisie des données établies sur les schémas référencés sur le site.&#x20;

Vous pouvez remplir :&#x20;

* un formulaire&#x20;
* un tableur

Ces outils préviennent lorsque les données contiennent des erreurs.

Une fois que les données seront valides, un fichier CSV sera généré. Vous pouvez ensuite choisir de télécharger le fichier CSV ou de le publier directement sur la plateforme datagouv.



### Contribuer via Github

Le dépôt est accessible à travers [ce lien](https://github.com/etalab/transport-base-nationale-covoiturage) (etalab/transport-base-nationale-covoiturage).



{% hint style="info" %}
Si vous rencontrez des difficultés à produire vos données, n'hésitez pas à nous contacter à l'adresse : [contact@transport.beta.gouv.fr ](mailto:contact@transport.beta.gouv.fr)
{% endhint %}
