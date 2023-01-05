# Présentation du schéma

Le schéma de données dynamiques a été construit suite à des entretiens et ateliers publics avec l'écosystème au cours de l'année 2022. Les présentations des ateliers sont disponibles [ici](https://doc.transport.data.gouv.fr/documentation/liste-des-rencontres-publiques) (ateliers du 14/09/22 et du 20/10/2023).&#x20;

Les champs retenus pour ce schéma sont :&#x20;

**4 champs obligatoires :**

* id\_pdc\_itinerance
* etat\_pdc&#x20;
* occupation\_pdc&#x20;
* horodatage

**4 champs facultatifs :**

* etat\_prise\_type\_2
* etat\_prise\_type\_combo\_ccs
* etat\_prise\_type\_chademo
* etat\_prise\_type\_ef

| Champs                        | Caractère   | Type                 | Valeurs autorisées                                                                             | Définition                                                                                                                                                                                                                                                                                                          |
| ----------------------------- | ----------- | -------------------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| id\_pdc\_itinerance           | Obligatoire | chaîne de caractères | id\_pdc\_itinerance au format eMI3 (incluant le préfixe délivré par l’AFIREV au format FRABCE) | Caractérise l’identifiant du point de recharge en question. Cet identifiant permet de faire le lien avec le statique.                                                                                                                                                                                               |
| etat\_pdc                     | Obligatoire | chaîne de caractères | en\_service, hors\_service et inconnu                                                          | Caractérise l’état de fonctionnement du point de recharge : est-il en service ou hors service ? En l’absence d’information, etat\_pdc sera égal à ‘inconnu’.                                                                                                                                                        |
| occupation\_pdc               | Obligatoire | chaîne de caractères | libre, occupe, reserve et inconnu                                                              | Caractérise l’occupation du point de recharge : est-il libre, occupé ou réservé ? En l’absence d’information, occupation\_pdc sera égal à ‘inconnu’.                                                                                                                                                                |
| horodatage                    | Obligatoire | date heure           | iso 8601(aaaa-mm-jj 'T' hh:mm:ss:SSSZ)                                                         | Indique la date et heure de remonter de l’information publiée.                                                                                                                                                                                                                                                      |
| etat\_prise\_type\_2          | facultatif  | chaîne de caractères | <p>fonctionnel</p><p>hors_service</p><p>inconnu</p><p>chaîne vide = Non Applicable</p>         | <p>permet d’indiquer l’état de fonctionnement du connecteur en question (T2, Combo CCS, Chademo ou EF) : est-il fonctionnel ou hors-service ?</p><p>En l’absence d’information, indiquer ‘inconnu’.</p><p>En l’absence de connecteur de ce type sur le point de recharge, laisser une chaîne de caractère vide.</p> |
| etat\_prise\_type\_combo\_ccs | facultatif  | chaîne de caractères | <p>fonctionnel</p><p>hors_service</p><p>inconnu</p><p>chaîne vide = Non Applicable</p>         | <p>permet d’indiquer l’état de fonctionnement du connecteur en question (T2, Combo CCS, Chademo ou EF) : est-il fonctionnel ou hors-service ?</p><p>En l’absence d’information, indiquer ‘inconnu’.</p><p>En l’absence de connecteur de ce type sur le point de recharge, laisser une chaîne de caractère vide.</p> |
| etat\_prise\_type\_chademo    | facultatif  | chaîne de caractères | <p>fonctionnel</p><p>hors_service</p><p>inconnu</p><p>chaîne vide = Non Applicable</p>         | <p>permet d’indiquer l’état de fonctionnement du connecteur en question (T2, Combo CCS, Chademo ou EF) : est-il fonctionnel ou hors-service ?</p><p>En l’absence d’information, indiquer ‘inconnu’.</p><p>En l’absence de connecteur de ce type sur le point de recharge, laisser une chaîne de caractère vide.</p> |
| etat\_prise\_type\_ef         | facultatif  | chaîne de caractères | <p>fonctionnel</p><p>hors_service</p><p>inconnu</p><p>chaîne vide = Non Applicable</p>         | <p>permet d’indiquer l’état de fonctionnement du connecteur en question (T2, Combo CCS, Chademo ou EF) : est-il fonctionnel ou hors-service ?</p><p>En l’absence d’information, indiquer ‘inconnu’.</p><p>En l’absence de connecteur de ce type sur le point de recharge, laisser une chaîne de caractère vide.</p> |

