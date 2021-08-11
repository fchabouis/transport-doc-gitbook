# Licence ODbL et conditions de réutilisation

Les données disponibles sur le Point d’Accès National transport.data.gouv.fr sont soumises à la licence ODbL que les réutilisateurs s’engagent à respecter dès lors qu’ils téléchargent un jeu de données. Seul le [texte complet](https://spdx.org/licenses/ODbL-1.0.html#licenseText) de la licence fait foi. Une [traduction non officielle en français est disponible ici](https://vvlibri.org/fr/licence/odbl-10/legalcode/unofficial) pour faciliter sa compréhension.

{% hint style="success" %}
Cette licence permet au réutilisateur de reproduire, modifier, exploiter à titre commercial sous trois conditions :

* Mentionner la source ; 
* Redistribuer les modifications sous des conditions de partage identiques ;
* Maintenir ouvertes les bases de données redistribuées.
{% endhint %}

### Conditions Particulières d'Utilisation

Il est précisé que la clause de partage à l’identique \(article 4.4\) concerne les informations de même nature, de même granularité, de même conditions temporelles et de même emprise géographique.

Par extension, seule est exigée le repartage aux bases de données dérivées \(paragraphe 4.6\) pour les bases de données dérivées répondant à ces conditions.

### Dans quels cas faut-il republier des données modifiées ?

_Je crée une nouvelle base de données comprenant des données issues d'un fichier récupéré depuis transport.data.gouv.fr. Dois-je republier cette nouvelle base ?_

<table>
  <thead>
    <tr>
      <th style="text-align:left">Oui</th>
      <th style="text-align:left">Non</th>
      <th style="text-align:left">Justification</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <ul>
          <li>Corrections des coordonn&#xE9;es</li>
          <li>Correction des noms des arr&#xEA;ts</li>
          <li>Ajout de coordonn&#xE9;es</li>
          <li>etc.</li>
        </ul>
      </td>
      <td style="text-align:left">Pr&#xE9;sence de commerces &#xE0; proximit&#xE9; des arr&#xEA;ts</td>
      <td
      style="text-align:left">Nature de la donn&#xE9;e</td>
    </tr>
    <tr>
      <td style="text-align:left">Ajustement des temps de correspondance</td>
      <td style="text-align:left">Cheminement pi&#xE9;ton des correspondances</td>
      <td style="text-align:left">Granularit&#xE9; de la donn&#xE9;e</td>
    </tr>
    <tr>
      <td style="text-align:left">Corrections des horaires th&#xE9;oriques planifi&#xE9;s</td>
      <td style="text-align:left">Horaires temps r&#xE9;el des prochains passages aux arr&#xEA;ts de bus</td>
      <td
      style="text-align:left">Conditions temporelles de la donn&#xE9;e</td>
    </tr>
    <tr>
      <td style="text-align:left">Ajout d&apos;une ligne manquante appartenant au m&#xEA;me r&#xE9;seau
        que celui du producteur du GTFS initial</td>
      <td style="text-align:left">Ajout d&apos;une ligne d&apos;un r&#xE9;seau strictement frontalier ou
        d&apos;un autre r&#xE9;seau que celui du producteur du GTFS initial</td>
      <td
      style="text-align:left">Emprise g&#xE9;ographique de la donn&#xE9;e</td>
    </tr>
  </tbody>
</table>

Il est recommandé de republier les bases de données dérivées directement sur la fiche du producteur correspondant afin de notifier ce producteur de la mise à disposition d’un jeu de données enrichi pour envisager une correction à la source.

### Comment mentionner la source _\(paternité\)_ de la base de données ?

La réutilisation d’une base de données soumise à la licence ODbL, ou d’une partie de cette base, requiert la mention :

* des noms des différents contributeurs à cette base ;
* de la licence ODbL à laquelle est soumise cette base.

S’il s’avère impossible d’intégrer les mentions requises en raison de limitations de forme ou d’affichage \(c’est-à-dire les applications smartphone, les résultats en fonction de la voix ou du texte, les agencements limités par l’espace\), il est possible d’inclure les mentions à un emplacement \(tel qu’un menu dédié pertinent\) où les utilisateurs pourront les retrouver facilement. Il est ainsi possible de créer une page dédiée « mentions légales » ou « sources des données » référençant la liste des concédants avec les liens vers leurs portails open data.

La source pourra par exemple être mentionnée de la façon suivante :

> _« \[Nom du réutilisateur\] utilise les dernières versions des jeux de données communiqués par les producteurs suivants :_
>
> _\[Liste des producteurs de données\]_
>
> _Ces données sont disponibles sur transport.data.gouv.fr sous la licence « Open Database Licence » \(ODbL\).»_

\_\_

