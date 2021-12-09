# 10/10/2019 - Données Aériennes (2)

**Compte-rendu de la rencontre publique transport.data.gouv.fr #22 consacrée à l’ouverture des données aériennes**

### **Participants**

Compagnies :

* Air France / KLM
* Vueling
* Air Corsica

Fédérations :

* Fédération Nationale de l'Aviation Marchande (FNAM)&#x20;
* Syndicat des compagnies aériennes autonomes (SCARA)

Aéroports :

* Groupe Aéroports de Paris (ADP)
* Union des aéroports français (UAF)

Organismes centraux :

* Direction générale de l’aviation civile (DGAC) et Direction des services de la Navigation aérienne (DSNA)
* International Air Transport Association (IATA)
* transport.data.gouv.fr

****\
**Présentation de transport.data.gouv**&#x20;

Présentation déroulée en séance disponible à [ce lien](https://docs.google.com/presentation/d/1RndFYNZsfR\_ciD5QhhnM\_wQnM3RZPSWVXccYahmul9I/edit#slide=id.p1). \
Pour plus d’informations sur transport.data.gouv.fr, vous pouvez consulter [le guide publié ici](https://doc.transport.data.gouv.fr).

### **Formats existants**

**Parmi les formats existants, on trouve :**

* **SSIM :** le format standard d’échange d’information, créé par IATA mais qui s’applique à toutes les compagnies (pas seulement les adhérents à IATA) pour leurs échanges avec la DGAC par exemple, il est réputé complexe mais a le mérite d’être déjà utilisé ;
* Le format simplifié **Flight Status** considéré par IATA pour les API ;
* Le format simplifié **semaine type** qu’Air France a utilisé pour publier un premier jeu de données sur le PAN.

Lors des échanges, aucun format n’est apparu comme solution universelle. L'équipe transport.data.gouv.fr et IATA vont dialoguer pour voir les interconnexions entre les formats et voir si des simplifications ou documentations ouvertes peuvent être mises en place.\
****

### **Temporalité des données**

Le transport aérien a une temporalité qui ne peut pas se résumer à une dichotomie théorique / temps réel. Il y a dans un schéma simplifié :\
****

|                  | Mise à jour     | Portée                      | Données prenant en compte                     | Coût (production + requête)                                |
| ---------------- | --------------- | --------------------------- | --------------------------------------------- | ---------------------------------------------------------- |
| **Stratégique**  | Tous les 6 mois | Une saison IATA (été/hiver) | Programmes de cadre global                    | Faible, déjà produit                                       |
| **Pré-tactique** | Chaque jour     | 14 jours                    | Plans de vol, jours fériés, grèves            | Déjà produit, mais la requête demande du travail           |
| **Tactique**     | Temps réel      | Quelques heures/jour        | Aléas, météo, gestion de l’aéroport, imprévus | Semble très coûteux, à la fois en production et en requête |

### **Échanges actuels de données**

Il y a essentiellement 2 types d’échanges de données :

* Entre les compagnies et des instances centrales (DGAC, IATA), avec des formats standardisés (SSIM). À noter que si toutes les compagnies sont tenues de notifier la DGAC, IATA fonctionne sur la base de l’adhésion et notamment les low-cost n’y adhèrent pas.
* Entre les compagnies et les aéroports, en bilatéral avec des échanges qui pourraient être améliorés.

Les compagnies ont souligné qu’elles envoient beaucoup de données, et en bonne partie à l’administration. De là, elles apprécieraient ne pas avoir à envoyer le même fichier une fois de plus mais souhaiteraient privilégier une coordination des administrations pour rationaliser ces échanges de données pour éviter la multiplication des canaux.

Le principe de la démarche transport.data.gouv.fr pour s’adapter à cette situation est de s’intégrer comme un centralisateur d’information, ou en bout de chaîne après un acteur central. Ceci permettrait de ne pas ajouter de nouveau flux mais d’en prolonger un, ou d’en rationaliser certains.

### **Actions à venir**

**Données stratégiques :** transport.data.gouv.fr lance une discussion avec la DGAC pour voir comment il serait possible que les  données  transmises à la DGAC soient disponibles en open data sur le PAN. A défaut, il peut être envisageable que les compagnies aériennes partagent ces données à l’équipe transport.data.gouv.fr par le même canal par lequel elles envoient actuellement ces données à la DGAC.\
\
**Données pré-tactiques :** examiner la possibilité de les ouvrir, voir le meilleur canal pour ouvrir ces données, déterminer les coûts associés.\
\
**Données temps réel :** favoriser des expérimentations avec des volontaires. Voir avec les aéroports pour l'ouverture des données alimentant les écrans d'information.
