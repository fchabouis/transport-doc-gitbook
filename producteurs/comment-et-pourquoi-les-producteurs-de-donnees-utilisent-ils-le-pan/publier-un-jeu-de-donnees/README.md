# Publier un jeu de données

Plusieurs méthodes permettent de publier un jeu de données sur data.gouv.fr, nous présenterons ici 3 méthodes :&#x20;

1. Publication des données par transport.data.gouv.fr (méthode générique)
2. Publication des données par moissonnage (méthode adaptée si vous disposez d'un portail open data local)
3. Publication des données par publier.etalab.studio (méthode adaptée pour publier un jeu de données répondant à un schéma national référencé sur schema.data.gouv.fr (bornes IRVE, aires de covoiturage, stationnement cyclable...))

{% hint style="info" %}
Les données de mobilité publiées seront utilisées par _transport.data.gouv.fr_ et les réutilisateurs de la plateforme. S'il s'agit de jeux de données sur les horaires théoriques ou temps-réel de transports en commun, de vélos en libre service, d'aménagements cyclables, d'autopartage, les jeux de données seront référencés manuellement par l'équipe de _transport.data.gouv.fr_ sur notre site.&#x20;

D'autres données ne sont pas référencées mais intégrées à des bases nationales. Les jeux de données ne sont pas référencés individuellement mais intégrés à des bases nationales. C'est le cas pour les IRVE, le stationnement hors voirie ou les aires de covoiturage.&#x20;

Dans tous les cas, si vos données ne sont pas référencées ou intégrées à une base nationale, merci de nous le signaler à l'adresse _contact@transport.beta.gouv.fr_.
{% endhint %}

## Préconisations&#x20;

Pour toutes les données publiées, nous recommandons de : \


### 1/ Préciser la licence sous laquelle les données sont diffusées&#x20;

Cette licence permettra réutilisateurs de connaître les conditions d'utilisation et de repartage de vos données.

Pour ajouter une licence :

#### Si les données sont publiées directement sur data.gouv.fr (dépôt, URL distante référencée) :

* [ ] Rendez-vous dans votre espace administrateur [data.gouv.fr](https://www.data.gouv.fr/fr/)
* [ ] Cliquez sur le jeu de données en question, ensuite sur "Editer" puis sur "Mettre à jour ce jeu de données" \
  ![](<../../../.gitbook/assets/image (173).png>)
* [ ] Dans la section "Licence", choisissez une licence dans la liste déroulante. Nous recommandons la [Licence Ouverte](https://www.etalab.gouv.fr/licence-ouverte-open-licence/) ou la Licence ODbL\
  ![](<../../../.gitbook/assets/image (184).png>)\
  ![](<../../../.gitbook/assets/image (183).png>)
* [ ] Cliquez sur "Enregistrer"

#### Si les données sont [moissonnées](https://doc.transport.data.gouv.fr/producteurs/comment-et-pourquoi-les-producteurs-de-donnees-utilisent-ils-le-pan/publier-un-jeu-de-donnees/2.-methode-moissonnage)&#x20;

* [ ] Rendez-vous dans l'espace administration de votre portail open data&#x20;
* [ ] Dans la section "Informations", ajouter dans la partie "Licence" une des licences listées [ici](https://github.com/opendatateam/udata-ods/blob/4a54c5cb60969e00564aa3c3a93923fb84a6d547/udata\_ods/harvesters.py#L61) en respectant la formulation. Nous recommandons la [Licence Ouverte](https://www.etalab.gouv.fr/licence-ouverte-open-licence/) (\`fr-lo\`) ou la Licence ODbL ('odc-odbl')\
  ![](<../../../.gitbook/assets/image (181).png>)

### 2/ Référencer des URL https&#x20;

Si vos données proviennent d'un portail externe, renseigner une ULR https permettra de sécuriser l'accès à vos données et de les télécharger à partir de tous les moteurs de recherche. Certains moteurs de recherche bloquent l'accès aux pages http.&#x20;

Pour modifier l'URL :

* [ ] Rendez-vous dans votre espace administrateur [data.gouv.fr](https://www.data.gouv.fr/fr/)
* [ ] Cliquez sur le jeu de données en question. Sélectionnez ensuite la ressource concernée puis cliquez sur "Editer"\
  <img src="../../../.gitbook/assets/image (182).png" alt="" data-size="original">
* [ ] Modifiez l'URL pour renseigner une URL https \
  ![](<../../../.gitbook/assets/image (175).png>)
* [ ] Cliquez sur "Enregistrer"



Si vous avez des questions ou que vous rencontrez des difficultés, contactez nous à l'adresse : contact@transport.beta.gouv.fr
