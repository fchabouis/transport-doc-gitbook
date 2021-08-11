---
description: >-
  transport.data.gouv.fr n'a pas encore référencé de jeu de données relatif à
  l'offre d'auto-partage. Nous cherchons des opérateurs pilotes qui
  souhaiteraient ouvrir leurs données.
---

# Auto-partage

transport.data.gouv.fr lance un appel aux opérateurs d'auto-partage qui souhaitent diffuser au maximum leur offre grâce à l'ouverture de leurs données. Les premiers partenaires pilotes seront évidemment valorisés dans un moment où tout est encore à définir. 

D'une manière générale, nous sommes prêts à partir des données que vous avez déjà pour être le moins contraignant possible sur vos systèmes d’information.

### Données à ouvrir pour améliorer l'information des voyageurs 

Les informations les plus pertinentes pour alimenter des services numériques d'information voyageur sont :

* la position des véhicules disponibles en temps réel ;

{% hint style="info" %}
Il nous semble nécessaire de toujours exposer une api « bulk » qui exposerait la position de tous les véhicules en une seule requête. Cela permet de réduire la charge des serveurs pour les gros consommateurs
{% endhint %}

* leur description \(type de véhicule, carburant, etc\) ;
* les conditions d'accès au véhicule ;
* \(non prioritaire : le planning futur de disponibilité des véhicules\).

Une deuxième manière d'exposer la position des véhicules en temps réel pourrait répondre à des usages spécifques « tous les véhicules 500m autour de moi ». Ce deuxième accès peut être déduit du premier, éventuellement porté par [transport.data.gouv.fr](http://transport.data.gouv.fr/).

### **Charge**

Si vous êtes inquiets de la charge générée sur vos serveurs, [transport.data.gouv.fr](http://transport.data.gouv.fr/) pourrait agir en proxy pour l’absorber. Cela nécessite cependant l’exposition de votre côté d’une API en "bulk" que nous pourrions récupérer une fois toutes les 30 secondes, par exemple.

### **Licences, conditions d'utilisation, conditions d'accès**

Nous recommandons en général la licence ouverte \(dite "Etalab"\) pour les données exposées via l'API \(obligation pour le réutilisateur de citer la source et la date de validité de la données\). Cependant, nous pouvons discuter davantage de ce point en fonction de vos craintes.

L'ouverture des données suppose souvent un accès aux données sans identification préalable Bien évidemment, si nous allons plus loin \(API de réservation\) le contrôle d’accès sera indispensable.

### **Vie privée**

Tant qu’il n’y a pas de réservation, les identifiants de véhicules ne sont pas nécessaires. Les exposer pourrait peut-être permettre de reconstruire des traces, et donc d’atteindre à la vie privée. Dans un premier temps, en attendant une réflexion plus poussée sur la question, il serait opportun d'éviter de les exposer sur transport.data.gouv.fr.



