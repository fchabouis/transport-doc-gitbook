# Description des champs du fichier "channel"

{% hint style="danger" %}
Cette documentation est en cours de rédaction : elle sera finalisée prochainement.  
Pour toute remarque, n'hésitez pas à nous contacter à l'adresse : [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr)
{% endhint %}

{% hint style="info" %}
Cette documentation sera enrichie grâce aux retours des producteurs et réutilisateurs. N'hésitez pas à nous contacter à l'adresse :  [contact@transport.beta.gouv.fr](mailto:contact@transport.beta.gouv.fr) si vous souhaitez que nous clarifions d'autres champs ****et/ou valeurs. 
{% endhint %}

### **counter\_transmission\_type** 

Ce champ définit la méthode utilisée pour récupérer les données depuis le compteur.   
La valeur "MANUEL" doit être utilisée seulement si un déplacement sur le site est nécessaire pour récupérer les données.   
Si les données peuvent être récupérées à distance, c'est la valeur "TELETRANSMISSION" qui doit être renseignée. 

Cette information permet notamment de comprendre pourquoi il y a des “trous” dans le fichier “measure”. En effet, si c’est une action manuelle qui permet de récupérer les données du compteur, il y aura plus de probabilités d’avoir des données qui ne sont pas mises à jour continuellement, d'avoir des périodes sans données. 

### **direction** 

Ce champ définit la direction vers laquelle se dirigent les usagers comptés. Il permet d’indiquer dans quel sens circulent les usagers en utilisant les points cardinaux.   
Un fichier measure correspond à un seul sens de circulation. Il faudra donc créer un fichier measure par sens de circulation. Ces différents fichiers “measure” auront le même “id\_site”  
 ****

### **data\_provider**

Ce champ définit l'entité ayant fourni la donnée. Il permet de préciser qui fournit les données aux collectivités et à transport.data.gouv.fr. Cela permet notamment de distinguer les fournisseurs de compteurs industriels des associations par exemple. 

### **temporality** 

Ce champ définit la périodicité du comptage. Il permet de préciser si le compteur est utilisé de manière pérenne sur un même site ou s' il compte temporairement dans des sites distincts. Un compteur est défini comme étant permanent lorsqu'il reste plus de 12 mois sur un même site.   
Lorsque le compteur est déplacé et qu’il ne rentre plus dans le périmètre du “site”, un nouveau fichier “channel” et “site” doivent être produits. 

### **started\_at** 

Ce champ définit la date et l'heure de début de comptage. Il permet de renseigner quand est ce que les données ont commencé à être produites et transmises. Cette période peut être antérieure à la transmission des données sur transport.data.gouv.fr. 

### ended\_at

Ce champ définit la date et l'heure de fin de comptage. Le producteur clôt le channel en renseignant cette information. Un channel peut être être clôt à la suite d'une modification d'un des champs du fichier comme _\`time\_step\` \`counter\_transmission\_type\` etc._   


### **time\_step** 

Ce champ définit le pas de temps des données fournies, en secondes.  
Lorsque le comptage se fait à une même fréquence pour un channel, le producteur peut préciser le pas de temps.  
Les données sont exprimées en secondes afin d’anticiper les améliorations qu’il y aura dans les délais de comptage. ****

