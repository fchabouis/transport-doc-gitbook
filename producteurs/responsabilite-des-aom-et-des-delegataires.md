# Responsabilités des AOM et des délégataires

### Autorités organisatrices de la mobilité

Les autorités organisatrices de la mobilité ont un rôle central dans le processus d’ouverture des données de transport. C’est aux AOM que revient la responsabilité de la publication de l’information sur le Point d’accès national transport.data.gouv.fr. Elles peuvent déléguer cette mission de publication.

### Opérateurs, cas des délégations de service public

Lors d’une concession ou d’une délégation de service public, sauf s’il en est explicitement dispensé par le contrat, le concessionnaire/délégataire se doit de partager avec l’autorité concédante/délégante, les données produites dans le cadre de la réalisation du contrat et indispensables à l’exécution du service.

<table>
  <thead>
    <tr>
      <th style="text-align:left">
        <p>
          <br /><b>LOI n&#xB0; 2016-1321 du 7 octobre 2016 pour une R&#xE9;publique num&#xE9;rique</b>
        </p>
        <p><b>Article 17, modifiant l&apos;ordonnance n&#xB0; 2016-65 du 29 janvier 2016 relative aux contrats de concession, cr&#xE9;ant l&#x2019;article 53-1</b>
        </p>
      </th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">
        <p><em><br />Lorsque la gestion d&apos;un service public est d&#xE9;l&#xE9;gu&#xE9;e, le concessionnaire fournit &#xE0; l&apos;autorit&#xE9; conc&#xE9;dante, sous format &#xE9;lectronique, dans un standard ouvert librement r&#xE9;utilisable et exploitable par un syst&#xE8;me de traitement automatis&#xE9;, les donn&#xE9;es et les bases de donn&#xE9;es collect&#xE9;es ou produites &#xE0; l&apos;occasion de l&apos;exploitation du service public faisant l&apos;objet du contrat et qui sont indispensables &#xE0; son ex&#xE9;cution.</em>
        </p>
        <p><em>La mise &#xE0; disposition ou la publication des donn&#xE9;es et bases de donn&#xE9;es fournies par le concessionnaire se fait dans le respect des articles L. 311-5 &#xE0; L. 311-7 du code des relations entre le public et l&apos;administration. L&apos;autorit&#xE9; conc&#xE9;dante peut, d&#xE8;s la conclusion du contrat ou au cours de son ex&#xE9;cution, exempter le concessionnaire de tout ou partie des obligations pr&#xE9;vues au pr&#xE9;sent article par une d&#xE9;cision motiv&#xE9;e fond&#xE9;e sur des motifs d&apos;int&#xE9;r&#xEA;t g&#xE9;n&#xE9;ral et rendue publique. &#xBB;</em>
        </p>
      </td>
    </tr>
  </tbody>
</table>

Par cohérence avec les autres textes en vigueur, ces données et leur format sont définies par le Règlement délégué \(Union européenne\) et la Loi d’orientation des mobilités. Le texte précédent, appliqué au domaine des transports en commun se traduit donc par une obligation \(sauf dispense explicite dans le contrat\) de partage par le délégataire avec l’autorité organisatrice d’un fichier au format NeTEx contenant toutes les informations disponibles. Un convertisseur étant développé, la publication au format GTFS est acceptable.

Vous pouvez télécharger ci-dessous un document rappelant le contexte légal autour de la publication de d'information voyageur et des obligations de chacun.

{% file src="../.gitbook/assets/ouverture\_de\_l\_information\_sur\_les\_transports-textes\_et\_obligations.pdf" %}

### Est-il nécessaire d'imposer un unique point de diffusion des données ?

L'ouverture des données de mobilité implique de multiples acteurs : AOM urbaines, AOM régionales, transporteurs, entreprises spécialisées dans le traitement de données et services d'information voyageurs...

L'équipe du Point d'Accès National recense **plusieurs cas où les données d'un même réseau sont diffusées par deux "producteurs de données" différents**. Par exemple, c'est la cas en Nouvelle-Aquitaine, où le syndicat de transport régional Nouvelle Aquitaine Mobilités transmet les données de toutes les AOM régionales comme locales opérant sur son territoire au PAN, et où simultanément plusieurs AOM publient en parallèle des données de mobilité décrivant l'offre de transport à l'échelle de leur territoire \(comme la Métropole de Bordeaux, par exemple\). La multiplication de sources de données ne pose pas d’inconvénient pour les réutilisateurs, **tant que le producteur de donnée est clairement identifié**.

La mise en place d'un point de diffusion unique de la donnée ne fait pas de sens dans un régime d'open data, car tout un chacun est libre de rediffuser ces mêmes données.

Il est dans l'intérêt du réutilisateur de **permettre aux acteurs qui apportent une modification ou une mise en qualité conséquente des données de diffuser cette donnée directement en open data**, indépendamment de leur statut \(transporteurs, agrégateurs de données...\). Cela permet de mettre en place la chaîne de communication la plus courte possible avec les réutilisateurs, afin de prendre en compte les retours faits par les réutilisateurs et d'effectuer d'éventuelles corrections si besoin.

La décision de privilégier une source de données plutôt qu’une autre pour alimenter un service numérique est donc essentiellement **un choix technique** qui revient au réutilisateur. En effet, entre deux sources de données décrivant la même offre de mobilité sur un territoire donnée, un réutilisateur pourra choisir de réutiliser une source de données plutôt qu’une autre en fonction de la qualité de la donnée, fréquence de mise à jour, granularité de la donnée \(jeu de données agrégés ou individuels\), complétion de champs facultatifs, ou autres attributs techniques.

