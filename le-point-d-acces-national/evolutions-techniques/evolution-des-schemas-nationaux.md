# Evolution des schémas nationaux

Chaque schéma national a un répertoire Github dédié. \
Toute personne intéressée par un schéma peut soumettre des propositions d'amélioration sur le dépôt GitHub consacré à cette thématique en faisant des issues ou des Pull Requests.&#x20;

Cet article a pour objectif :&#x20;

* de définir brièvement ce qu'est [GitHub ](https://github.com/)
* d'expliquer étape par étape comment contribuer à un schéma national en prenant pour exemple le [schéma des aménagements](https://schema.data.gouv.fr/etalab/schema-amenagements-cyclables/)&#x20;
* d'expliciter la gouvernance autour des modifications pouvant être apportées à ce schéma

### Qu'est ce que GitHub ?&#x20;

[GitHub](https://github.com/) est une plateforme web qui permet de stocker le code source d'une application informatique et à plusieurs personnes d'y apporter des modifications simultanément sans rien écraser. Chaque modification du code est ainsi stockée sur GitHub.\
L'ensemble de la base du code et de l’historique est disponible sur l’ordinateur de chaque développeur, ce qui permet des branchements et une fusion faciles. Les branchements, permettent au développeur de dupliquer localement une partie du code source dans une branche et de le modifier sans affecter le reste du projet. Une fois que le développeur voudra publier ses modifications, il pourra les fusionner au code source.&#x20;

&#x20;Vous trouverez une définition plus complète[ ici](https://fr.tuto.com/blog/2020/10/github.htm).



## Comment contribuer à un schéma national en utilisant GitHub&#x20;

{% hint style="info" %}
Ce tutoriel sera amené à évoluer selon les retours des contributeurs. \
Nous vous invitons à nous contacter si vous rencontrez des difficultés à faire une Pull Request à partir de ce tutoriel.
{% endhint %}

Pour contribuer à l'évolution d'un schéma en faisant des propositions d'améliorations, tout contributeur doit soumettre une issue ou Pull Resquest sur le dépôt GitHub.

### Faire une proposition d'évolution de schéma par une issue

{% hint style="info" %}
Nous recommandons aux personnes qui ne maitrisent pas Github de passer par une issue pour faire une demande d'évolution de schéma. C'est la manière la plus simple de faire.&#x20;

Notre équipe se chargera ensuite de faire une pull request de cette issue si la demande de modification est validée.
{% endhint %}

Une issue est une demande de changement sur un projet.&#x20;

Pour faire une issue, il suffit d'aller sur l'onglet "issue" du Github du schéma > cliquer sur "New issue" en haut à droite > donner un titre clair de demande de modification et faire la demande de modification en commentaire > cliquer sur "Submit new issue"

### Faire une proposition d'évolution de schéma par une Pull Request

{% hint style="info" %}
Nous recommandons aux personnes familières à Github de passer par une Pull Request pour faire une demande d'évolution de schéma.&#x20;

Notre équipe n'aura plus qu'à valider la demande si elle est acceptée par la communauté transport.&#x20;
{% endhint %}

Une Pull Request est une demande de "pull" (ajout) à un projet sur GitHub. Cela consiste à faire une proposition de modification du code et à demander au détenteur du dépôt original de la prendre en compte. Cette Pull Request permet également au détenteur de voir exactement ce que vous avez changé dans le code. Il peut :&#x20;

* approuver votre Pull Request et l'intégrer au projet
* désapprouver votre Pull request et votre proposition ne sera pas prise en compte&#x20;
* laisser des commentaires et ainsi entamer une discussion au sujet de votre contribution&#x20;

Afin de vous faciliter l'utilisation de GitHub pour les Pull Request, nous vous recommandons d'utiliser un des outils d'interface graphique mis à disposition par Git. Vous pouvez en choisir un [ici](https://git-scm.com/downloads/guis)

#### **Tutoriel d'une Pull Request basé sur le** [**répertoire Github du schéma aménagements cyclables**](https://github.com/etalab/amenagements-cyclables)

Ce tutoriel se basera sur l'outil "GitHub Desktop" (ou Bureau Github), compatible avec Mac et Windows.

Tout d’abord, si vous n'avez pas déjà un compte GitHub, il faut vous rendre sur la [page d'accueil](https://github.com/) de GitHub et créer un compte.

![](<../../.gitbook/assets/image (114).png>)

Une fois votre compte créé, vous pourrez vous rendre sur le dépôt sur lequel vous voulez contribuez, en l'occurrence [celui sur les aménagements cyclables](https://github.com/etalab/schema-amenagements-cyclables) puis :\
1/ Cliquer sur "Code" \
2/ Copier le lien fourni&#x20;

![](<../../.gitbook/assets/image (117).png>)

3/ Ouvrir "GitHub Desktop" > cliquer sur "Current Repository"\
4/ Cliquer sur "Add" > Cliquer sur "Clone'

![](<../../.gitbook/assets/image (112).png>)

Une fenêtre comme celle ci-dessous s'affichera \
5/ Cliquer sur "URL"\
6/ Coller le lien que vous avez copié dans le dépôt GitHub \
7/ Cliquer sur "Clone"

![](<../../.gitbook/assets/image (115).png>)

Vous venez de créer une copie du dépôt dans votre ordinateur. Vous pourrez le modifier localement autant que vous le souhaitez sans que cela modifie le schéma principal. Vous pouvez accéder au dépôt local en :

* suivant le chemin indiqué en positionnant votre souris ici &#x20;

![](<../../.gitbook/assets/image (111).png>)

* cherchant "schema-amenagaments-cyclables" dans vos fichiers

Exemple d'une modification du schéma : Suppression de la valeur "RAMPE" de l'énumération des types d'aménagements cyclables sur la voie de droite et de gauche dans le fichier schema\_amenagaments\_cyclables.json

![](<../../.gitbook/assets/image (102).png>)

Une fois le fichier modifié, vous pouvez l'enregistrer et vous rendre de nouveau sur le "GitHub Desktop". Vos modifications apparaîtront en rouge dans le fichier que vous avez modifié. \
\
8/ Décrire les modifications qui ont été faites dans le titre et justifier cette modification en description \
9/ Cliquer sur "Commit to master"\
Cette action va envoyer votre demande de modification dans le dépôt principal.&#x20;

![](<../../.gitbook/assets/image (107).png>)

10/ Cliquer en haut du "GitHub Destock" sur "Branch"\
11/ Cliquer sur "Create Pull Request"

![](<../../.gitbook/assets/image (113).png>)

La fenêtre de discussion ci-dessous apparaitra \
12/ Cliquer sur "Push commits"&#x20;

![](<../../.gitbook/assets/image (104).png>)

Vous serez ensuite directement renvoyé vers le GitHub. \
Tout en haut il sera écrit que vous comparez vos ajouts, avec le nom de votre branche, à la branche "master" et donc la branche principale du projet. \
Vous pourrez corriger et/ou compléter le titre et description de votre Pull Request\
\
13/ Cliquer sur "Create Pull Request"\


![](<../../.gitbook/assets/image (119).png>)

L'équipe de transportdatagouv sera notifiée de votre demande de modification. Cette demande sera visible par toutes les personnes visitant ce dépôt. \
\
Vous pourrez annoncer la publication de cette Pull Request dans le [Slack transportdatagouv dédié aux aménagements cyclables](https://transportdatagouvfr.slack.com/?redir=%2Farchives%2FC0178TC9JL9). Puis, attendre 14 jours civils avant de procéder au processus de vote. \


## Gouvernance autour des modifications d'un schéma

Que la demande de modification soit faite par issue ou par pull request, l'équipe de transportdatagouv sera notifiée de votre demande de modification. Cette demande sera visible par toutes les personnes visitant ce dépôt. \
\
Vous pourrez annoncer la publication de votre demabde dans le Slack transportdatagouv dédié au type de mobilité concerné par le schéma (exemple du [canal Slack aménagements cyclables](https://transportdatagouvfr.slack.com/archives/C0178TC9JL9)). Puis, attendre 14 jours civils avant de procéder au processus de vote.&#x20;

{% hint style="info" %}
La gouvernance autour de ce schéma reprend partiellement le [système de gouvernance adopté par NABSA pour l'amélioration du format GBFS](https://github.com/NABSA/gbfs).&#x20;
{% endhint %}

Tout le monde peut proposer un changement. Dès lors qu'une personne propose une modification en ouvrant une issue ou une Pull Request (PR) dans le référentiel du schéma national, elle devient le "Plaideur". \
Toute personne peut alors commenté sa proposition d'amélioration pendant 14 jours civils et entamer une discussion avec le "Plaideur". Le "Plaideur" peut modifier sa proposition pendant ces 14 jours. La discussion dure aussi longtemps que nécessaire pour répondre aux questions et révisions, mais doit durer au moins 14 jours civils.

\
Au bout de ces 14 jours, le "Plaideur" peut demander un vote pour que le reste de la communauté approuve sa proposition. L'annonce du vote doit être annoncée comme suit : \
" _Je demande par la présente un vote sur cette proposition. Le vote sera ouvert pendant 10 jours civils complets jusqu'à 23 h 59 UTC+1 l'hiver, UTC+2 l'été à partir de ce jour. Il prendra donc fin le JJ/MM/AAAA à 23h59._ \
_Veuillez voter pour ou contre la proposition, et inclure l'organisation pour laquelle vous votez dans votre commentaire._\
_Veuillez préciser si vous pouvez vous engager à mettre en œuvre la proposition."_\
_Le "Plaideur"_  doit également annoncer le vote sur le canal Slack du schéma avec un lien vers la PR. Le message doit être conforme à ce modèle:\
" _Un vote a été demandé sur la PR # \[titre du PR] (lien vers la PR). Ce vote sera ouvert pendant 10 jours civils complets, jusqu'à 23 h 59 UTC sur +1 l'hiver, +2 l'été soit jusqu'au JJ/MM/AAAA à 23h59. Veuillez voter pour ou contre la proposition sur GitHub"_ \
Une fois qu'un vote est appelé, une étiquette «Vote ouvert» sera ajoutée à la PR.&#x20;

Si le "Plaideur" ne fait pas de demande de vote ou ne répond pas aux commentaires de la communauté pendant 30 jours civils complets, n'importe qui dans la communauté peut lancer le vote.&#x20;

{% hint style="warning" %}
Les modifications rédactionnelles ainsi que les éléments qui ne se trouvent pas dans [schema\_amenagements\_cyclables.json](https://github.com/etalab/schema-amenagements-cyclables/blob/master/schema\_amenagements\_cyclables.json) n'ont pas besoin d'être votés. \
Seules les extensions qui incluent de nouveaux champs, de nouvelles valeurs autorisées dans les listes déroulantes, des changement de propriétés de champs (champ optionnel qui devient obligatoire, champs obligatoire qui devient optionnel) doivent être votées.
{% endhint %}

Un membre de l'équipe de [transport.data.gouv.fr ](https://transport.data.gouv.fr/)mettra un rappel sur la Pull Request sur GitHub et dans le canal Slack lorsqu'il restera 2 jours calendaires pour le vote. Le rappel doit être suivre ce modèle :&#x20;

* Slack:\
  _Le vote sur la PR # \[titre de la PR] (lien vers la PR) ou issue # \[titre de l'issue] (lien vers l'issue) se termine dans 2 jours civils. Veuillez voter pour ou contre la proposition sur GitHub._
* GitHub: \
  le _vote pour cette PR ou cette issue se termine dans 2 jours calendaires. Veuillez voter pour ou contre la proposition et inclure l'organisation pour laquelle vous votez dans votre commentaire. Veuillez noter si vous pouvez vous engager à mettre en œuvre la proposition._

Après le rappel de 2 jours, le libellé sera remplacé par "Clôture du vote bientôt". Une fois le vote clos, le libellé deviendra "Vote réussi" ou "Vote échoué" selon le résultat du vote.

{% hint style="success" %}
Une proposition est approuvée et est intégrée au schéma quand :

* Au moins un de ces votes doit provenir d'un producteur et au moins un doit provenir d'un réutilisateur.
* Les votes des producteurs et des réutilisateurs proviennent de parties prenantes autres que le "Plaideur".
* [transport.data.gouv.fr](https://transport.data.gouv.fr/) sert uniquement de facilitateur et ne vote pas sur les changements proposés.

Lorsqu'un vote est réussi, le changement passe au statut de Release Candidate (RC). Le changement reste dans le statut RC en attendant son intégration dans le schéma. La proposition est intégrée au schéma si :&#x20;

* au moins 1 producteur et 1 réutilisateur, appelés "exécutants", déclarent qu'ils appliqueront ce changement.
* Les exécutants doivent être des parties prenantes autres que le "Plaideur".

Une fois intégrée au schéma officiel, les producteurs pourront mettre à jour leurs bases/produire leurs données à partir de cette mise à jour du schéma.
{% endhint %}

{% hint style="danger" %}
Une proposition est rejetée quand :

* Une personne vote contre en fournissant une raison spécifique pour son vote et laisse des commentaires exploitables.

En cas d'échec du vote, l'avocat peut choisir  :

* de poursuivre le travail sur la proposition avec les commentaires reçus et de redémarrer le processus de gouvernance
* d'abandonner la proposition en fermant sa Pull Request.&#x20;

Un autre membre intéressé de la communauté peut reprendre sa proposition s'il estime qu'elle est pertinente.
{% endhint %}



Une Pull Request sera considérée comme obsolète après 120 jours, date à laquelle les participants seront informés à travers un commentaire. Si ils souhaitent garder la discussion ouverte, il est de la responsabilité des participants de reprendre la conversation. \
Si aucun commentaire n'est ensuite fait, la Pull Request sera clôturée 60 jours après la date d'expiration.



Si vous rencontrez des difficultés, vous pouvez nous contacter à l'adresse :  [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr).&#x20;
