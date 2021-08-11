---
description: >-
  Ce schéma est une traduction du schéma json des aménagements cyclables au
  format tableur. Il a pour objectif de faciliter la compréhension des champs.
---

# Schéma au format tableur

Ce schéma, sous format tableur, reprend le schéma des aménagements cyclables publié au format json sur le[ GitHub dédié à ce schéma](https://github.com/etalab/schema-amenagements-cyclables). Cette version tableur est une simplification du schéma afin d'en faciliter la compréhension. Toute personne voulant se renseigner doit se baser sur la [version json](https://github.com/etalab/schema-amenagements-cyclables/blob/master/schema_amenagements_cyclables.json) qui est plus détaillée et la plus à jour.  

{% hint style="warning" %}
Les coordonnées géographiques des aménagements cyclables ne correspondent pas à des points mais à des formes géographiques. Elles ne seront pas représentées dans ce tableau bien que ce champ soit obligatoire.   
Le WGS84 est le système géodésique attendu. 
{% endhint %}

{% hint style="info" %}
* Certains champs ont des valeurs pré définies dans des listes déroulantes comme les champs "reseau\_loc", "ame\_d" etc. Ces valeurs ne seront pas listées dans ce schéma. Veuillez vous reporter au [schéma json ](https://github.com/etalab/schema-amenagements-cyclables/blob/master/schema_amenagements_cyclables.json)pour avoir ces détails. 
* La valeur "booléen" renvoie à "true" ou "false" 
{% endhint %}

## Schéma

<table>
  <thead>
    <tr>
      <th style="text-align:left">nom</th>
      <th style="text-align:left">description</th>
      <th style="text-align:left">type</th>
      <th style="text-align:left">Propri&#xE9;t&#xE9;s</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">id_local</td>
      <td style="text-align:left">identifant local de l&apos;am&#xE9;nagement</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur obligatoire</td>
    </tr>
    <tr>
      <td style="text-align:left">reseau_loc</td>
      <td style="text-align:left">type de r&#xE9;seau structurant local auquel l&apos;am&#xE9;nagement appartient</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">
          <p>valeur optionnelle</p>
          <p><em>liste d&#xE9;roulante</em>
          </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">nom_loc</td>
      <td style="text-align:left">nom et num&#xE9;ro des itin&#xE9;raires locaux</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">id_osm</td>
      <td style="text-align:left">identifiant de l&apos;am&#xE9;nagement sur OpenStreetMap (OSM)</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">num_iti</td>
      <td style="text-align:left">num&#xE9;ro des itin&#xE9;raires, des EuroVelo au sch&#xE9;ma d&#xE9;partementaux,
        auxquels le segment appartient. S&#xE9;par&#xE9; par &#xAB; : &#xBB;</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">code_com_d</td>
      <td style="text-align:left">code INSEE de la commune (5 caract&#xE8;res alphanum&#xE9;riques) sur
        la voie de droite</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur obligatoire</td>
    </tr>
    <tr>
      <td style="text-align:left">ame_d</td>
      <td style="text-align:left">type d&apos;am&#xE9;nagement pr&#xE9;sent sur la voie de droite</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">
          <p>valeur obligatoire</p>
          <p><em>liste d&#xE9;roulante</em>
          </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">regime_d</td>
      <td style="text-align:left">r&#xE9;gime pr&#xE9;sent sur la voie de droite</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>liste d&#xE9;roulante</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">sens_d</td>
      <td style="text-align:left">sens de circulation pour les cyclistes sur la voie de droite</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>liste d&#xE9;roulante</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">largeur_d</td>
      <td style="text-align:left">largeur hors marquage minimale utile de la voie de droite r&#xE9;serv&#xE9;e
        au cycliste, en m&#xE8;tre. La largeur du marquage est exclue</td>
      <td style="text-align:left">nombre</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">local_d</td>
      <td style="text-align:left">emplacement de l&apos;am&#xE9;nagement sur la voie de droite</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>liste d&#xE9;roulante</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">statut_d</td>
      <td style="text-align:left">niveau de r&#xE9;alisation de l&apos;infrastructure sur la voie de droite</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">
          <p>valeur optionnelle</p>
          <p><em>liste d&#xE9;roulante</em>
          </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">code_com_g</td>
      <td style="text-align:left">code INSEE de la commune (5 caract&#xE8;res alphanum&#xE9;riques) sur
        la voie de gauche</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur obligatoire</td>
    </tr>
    <tr>
      <td style="text-align:left">ame_g</td>
      <td style="text-align:left">type d&apos;am&#xE9;nagement pr&#xE9;sent sur la voie de gauche</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">
          <p>valeur obligatoire</p>
          <p>liste <em>d&#xE9;roulante</em>
          </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">regime_g</td>
      <td style="text-align:left">r&#xE9;gime pr&#xE9;sent sur la voie de gauche</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>liste d&#xE9;roulante</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">sens_g</td>
      <td style="text-align:left">sens de circulation pour les cyclistes sur la voie de gauche</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>liste d&#xE9;roulante</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">largeur_g</td>
      <td style="text-align:left">largeur hors marquage minimale utile de la voie de gauche r&#xE9;serv&#xE9;e
        au cycliste, en m&#xE8;tre. La largeur du marquage est exclue</td>
      <td style="text-align:left">nombre</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">local_g</td>
      <td style="text-align:left">emplacement de l&apos;am&#xE9;nagement sur la voie de gauche</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>liste d&#xE9;roulante</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">statut_g</td>
      <td style="text-align:left">niveau de r&#xE9;alisation de l&apos;infrastructure sur la voie de gauche</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">
          <p>valeur optionnelle</p>
          <p><em>liste d&#xE9;roulante</em>
          </p>
        </td>
    </tr>
    <tr>
      <td style="text-align:left">access_ame</td>
      <td style="text-align:left">accessibilit&#xE9; des aman&#xE9;gements par type de v&#xE9;hicule &#xE0;
        deux roues non motoris&#xE9;</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>liste d&#xE9;roulante</em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">date_maj</td>
      <td style="text-align:left">date de derni&#xE8;re mise &#xE0; jour des donn&#xE9;es du segment Notation
        ISO 8601, format AAAA-MM-JJ</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">trafic_vit</td>
      <td style="text-align:left">vitesse maximale autoris&#xE9;e pour le trafic adjacent &#xE0; l&apos;am&#xE9;nagement,
        en km/h. La vitesse 5 km/h correspond &#xE0; une vitesse &#xE0; l&apos;allure
        du pas</td>
      <td style="text-align:left">nombre entier</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">lumiere</td>
      <td style="text-align:left">am&#xE9;nagement &#xE9;clair&#xE9;</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">
        <p>valeur optionnelle</p>
        <p><em>bool&#xE9;en </em>
        </p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">d_service</td>
      <td style="text-align:left">date de mise en oeuvre de l&apos;am&#xE9;nagement (AAAA)</td>
      <td style="text-align:left">nombre</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">comm</td>
      <td style="text-align:left">remarques &#xE9;ventuelles au sujet de l&apos;am&#xE9;nagement</td>
      <td
      style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
        <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">source</td>
      <td style="text-align:left">entit&#xE9; ayant fourni les donn&#xE9;es</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">project_c</td>
      <td style="text-align:left">projection cartographique utilis&#xE9;e</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
    <tr>
      <td style="text-align:left">ref_geo</td>
      <td style="text-align:left">r&#xE9;f&#xE9;rentiel g&#xE9;ographique utilis&#xE9;</td>
      <td style="text-align:left">cha&#xEE;ne de caract&#xE8;res</td>
      <td style="text-align:left">valeur optionnelle</td>
    </tr>
  </tbody>
</table>

## Exemple 

| id\_local | reseau\_loc | nom\_loc | id\_osm | num\_iti | code\_com\_d | ame\_d | regime\_d | sens\_d | largeur\_d | local\_d | statut\_d | ame\_g | regime\_g | sens\_g | largeur\_g | local\_g | statut\_g | access\_ame | date\_maj | trafic\_vit | lumiere | d\_service | comm | source | project\_c | ref\_geo |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 751AC | Structurant | V1 | 7746952719 | 0001:0006:0045 | 75114 | BANDE CYCLABLE | AIRE PIETONNE | UNIDIRECTIONNEL | 3 | TROTTOIR | PROVISOIRE | BANDE CYCLABLE | AIRE PIETONNE | UNIDIRECTIONNEL | 4.1 | TROTTOIR | PROVISOIRE | VTT | 2020-08-15 | 80 | true | 2015 | forte pente sur 10 mètres | Ville de Paris | Peters | Bdortho |

## 

