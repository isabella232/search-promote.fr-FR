---
description: Découvrez comment personnaliser la sortie dans n’importe quel format texte, y compris XML ou JSON.
solution: Target
title: Sortie de recherche guidée
topic: Appendices,Site search and merchandising
uuid: 234fd563-f249-42b0-88ca-c89b44f8df77
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '6289'
ht-degree: 2%

---


# Sortie de recherche guidée{#guided-search-output}

Vous pouvez personnaliser la sortie dans n’importe quel format texte, y compris XML ou JSON.

## Utilisation de la sortie de recherche guidée {#concept_2A1BA3AD413848A1AC2A3ABC4FFE481F}

Le format de sortie est personnalisable pour prendre en charge les facettes, le tri et d’autres décisions spécifiques à l’implémentation qui sont prises pendant le processus de conception. Vous pouvez adapter le format lui-même pour simplifier le développement du client frontal, si nécessaire.

La sortie complète est contenue dans des balises `<result>` et la plupart des données dynamiques sont placées entre des balises `<![CDATA[ ]]>`. Cette organisation permet aux résultats de contenir du code HTML et d’autres entités non XML.

Lorsque des liens vers d’autres pages sont fournis, ils sont présentés sous la forme d’une URL relative. Ce résultat inclut également les paramètres de chaîne de requête transmis pour générer le résultat souhaité.

## Présentation d&#39;une implémentation de recherche guidée {#section_95483980930C4325BAB50A40BD47245A}

Lorsque vous commencez une mise en oeuvre de la recherche guidée, n’oubliez pas que [!DNL Adobe Search&Promote] est responsable de la couche métier. C&#39;est-à-dire la logique qui entoure les résultats et facettes présentés à un client à un moment donné.

Lorsque vous implémentez l’Application web frontale qui analyse et affiche les résultats au format HTML, limitez la fonctionnalité à l’affichage uniquement. En d&#39;autres termes, toute logique côté serveur que vous utilisez pour créer la couche Présentation ne prend pas les décisions concernant ce que vous devez présenter à un client, sauf si cela est nécessaire. Les règles de fonctionnement ne fonctionneront pas comme vous le prévoyez si le script frontal modifie les résultats de la recherche.

[!DNL Adobe Search&Promote] permet de conserver l’état utilisateur des options de raffinement de recherche sélectionnées au moyen des paramètres d’URL. Tous les noeuds `<link>` contiennent les paramètres appropriés des sélections du client. Ces paramètres peuvent inclure des sélections de chemin de navigation, de pagination, de tri et de facettes. Le cas échéant, les noeuds `<undolink>` sont renvoyés pour permettre à un client de &quot;désactiver&quot; une sélection. Facettes et chemins de navigation offre ces types de liens.

## Utilisation du serveur de recherche {#section_8DBEACDECD714E59BDED6315E6041B8D}

Une API de type REST est utilisée avec laquelle vous pouvez interagir pour effectuer des recherches et recevoir des résultats. Les formats les plus utilisés pour les résultats sont XML ou JSON.

L’URI de base est associé à un compte spécifique et à un environnement intermédiaire ou actif. Vous pouvez demander plusieurs alias pour l’URI de base à votre gestionnaire de compte. Par exemple, une société fictive appelée Megacorp comporte les deux URL de base suivantes associées à son compte :

* `https://search.megacorp.com `
* `https://stage.megacorp.com`

L’URI précédent effectue des recherches sur son index actif et l’URI suivant sur son index intermédiaire.

Les demandes de recherche se composent de l’URI de base et d’un ensemble de paramètres CGI ou de paires clé-valeur qui indiquent la recherche souhaitée pour le compte associé à l’URI de base.

Trois formats de paramètres CGI sont pris en charge. Par défaut, votre compte est configuré pour séparer les paramètres CGI par un point-virgule ( `;`), comme dans l&#39;exemple suivant :

* `https://search.megacorp.com?q=shoes ;page=2`

Si vous préférez, votre gestionnaire de compte peut configurer votre compte pour qu’il utilise des esperluettes ( `&`) pour séparer les paramètres CGI, comme dans l’exemple suivant :

* `https://search.megacorp.com?q=shoes &page=2`

Un troisième format, appelé format SEO, est également pris en charge lorsqu’une barre oblique ( `/`) est utilisée à la place du séparateur et que le signe égal est utilisé pour générer des liens &quot;propres&quot;, comme dans l’exemple suivant :

* `https://search.megacorp.com/q/shoes/page/2`

Chaque fois que le format d’optimisation du référencement est utilisé pour envoyer une requête, tous les liens de sortie sont renvoyés au même format.

## Paramètres de la requête de recherche {#section_7ADA5E130E3040C9BE85D0D68EDD3223}

Le tableau suivant décrit les paramètres standard de requête de recherche prêts à l’emploi que vous pouvez utiliser. Les règles de traitement et les règles de fonctionnement peuvent être créées à partir de paramètres de requête définis par l’utilisateur pour implémenter une logique métier personnalisée adaptée à votre société. Vous pouvez travailler avec l’équipe de conseil pour obtenir de la documentation sur ces paramètres.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Paramètre de requête de recherche </p> </th> 
   <th colname="col2" class="entry"> <p>Exemple </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q= chaîne  </span> </p> </td> 
   <td colname="col3"> <p> Indique la chaîne de requête pour la recherche. Ce paramètre correspond au paramètre de recherche principal <span class="codeph"> sp_q </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> q# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> q#= chaîne  </span> </p> </td> 
   <td colname="col3"> <p>Les paramètres numérotés <span class="codeph"> q </span> et <span class="codeph"> x </span> permettent d’accomplir des facettes ou de rechercher dans un champ donné. </p> <p>Le paramètre <span class="codeph"> q </span> définit le terme que vous recherchez dans la facette comme le paramètre numéroté <span class="codeph"> x </span> correspondant le désigne. Par exemple, si vous disposez de deux facettes nommées taille et couleur, vous pouvez avoir quelque chose comme ceci : </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>Ce paramètre correspond aux paramètres de recherche principale <span class="codeph"> sp_q_exact_# </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> x# </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> x#= chaîne  </span> </p> </td> 
   <td colname="col3"> <p> Les paramètres numérotés <span class="codeph"> q </span> et <span class="codeph"> x </span> permettent d’accomplir des facettes ou de rechercher dans un champ donné. </p> <p>Le paramètre <span class="codeph"> q </span> définit le terme que vous recherchez dans la facette comme le paramètre numéroté <span class="codeph"> x </span> correspondant le désigne. Par exemple, si vous disposez de deux facettes nommées taille et couleur, vous pouvez avoir quelque chose comme ceci : </p> <p> <span class="codeph"> q1=small;x1=size;q2=red;x2=color  </span> </p> <p>Ce paramètre correspond aux paramètres de recherche principale <span class="codeph"> sp_x_# </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> collecte </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> collection= chaîne  </span> </p> </td> 
   <td colname="col3"> <p> Indique la collection à utiliser pour la recherche. Ce paramètre correspond au paramètre de recherche principal <span class="codeph"> sp_k </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> count </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> count= nombre  </span> </p> </td> 
   <td colname="col3"> <p> Indique le nombre total de résultats affichés. La valeur par défaut est définie dans <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Recherche </span> &gt; <span class="uicontrol"> Recherches </span>. Ce paramètre correspond au paramètre de recherche principal <span class="codeph"> sp_c </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> page </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> page= nombre  </span> </p> </td> 
   <td colname="col3"> <p> Indique la page des résultats qui sont renvoyés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rang  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> rang= champ  </span> </p> </td> 
   <td colname="col3"> <p> Indique le champ de classement à utiliser pour le classement statique. Le champ doit être un champ de type Classement dont la pertinence est supérieure à 0. Ce paramètre correspond au paramètre principal <span class="codeph"> sp_sr </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gs_store  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> gs_store= chaîne  </span> </p> </td> 
   <td colname="col3"> <p> Indique le magasin à rechercher. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sort  </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> sort= nombre  </span> </p> </td> 
   <td colname="col3"> <p> Indique l’ordre de tri. "0" est la valeur par défaut et est triée par score de pertinence ; "1" est classé par date ; "-1" n’est pas trié. </p> <p>Les utilisateurs peuvent spécifier un nom de champ pour la valeur du paramètre <span class="codeph"> sp_s </span>. Par exemple, <span class="codeph"> sp_s=title </span> trie les résultats en fonction des valeurs contenues dans le champ de titre. Lorsqu’un nom de champ est utilisé pour la valeur d’un paramètre <span class="codeph"> sp_s </span>, les résultats sont triés par ce champ, puis subtriés par pertinence. </p> <p>Pour activer cette fonctionnalité, procédez comme suit : </p> 
    <ol id="ol_3894F81EA7BF4827A84DE8662111ABEF"> 
     <li id="li_C040C0B88F174A4885E1A8E721FD032A">Dans le menu produit, cliquez sur <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>. </li> 
     <li id="li_2E83C3A46D1B4BF991EABAD9D3E52B7D">Sur la page <span class="wintitle"> Définitions par étapes </span>, effectuez l'une des opérations suivantes : 
      <ul id="ul_8018FEE10E0A4C96A74F84A897080580"> 
       <li id="li_E9A7CE43E2734F4D9522A1283CA111FB">Cliquez sur <span class="uicontrol"> Ajouter un nouveau champ </span>. </li> 
       <li id="li_9D2434A321924FBD874569CA9AD2EEF7">Cliquez sur <span class="uicontrol"> Modifier </span> pour un nom de champ particulier. </li> 
      </ul> </li> 
     <li id="li_90D5E3F4AC0A4A6189934A5589F69903">Dans la liste déroulante <span class="wintitle"> Tri </span>, cliquez sur <span class="uicontrol"> Ascendant </span> ou <span class="uicontrol"> Descendant </span>. <p>Ce paramètre correspond au paramètre de recherche principal <span class="codeph"> sp_s </span>. </p> </li> 
    </ol> </td> 
  </tr> 
 </tbody> 
</table>

## Intégration à votre système {#section_91261B19A44A4E579B3FC9FAB9AD3665}

Vous trouverez ci-dessous des recommandations pour l’intégration à votre système.

* Communication avec le serveur de recherche.

   Vous pouvez communiquer avec les serveurs Web [!DNL Adobe Search&Promote] à l’aide de requêtes de GET HTTP. Vos serveurs génèrent ces requêtes ou côté client exécutant une requête Ajax.
* Enregistrement de l&#39;historique de recherche.

[!DNL Adobe Search&Promote] est sans état lorsque l’état entier est transmis dans la requête http.
* Analyse des résultats renvoyés.

   Il est recommandé d’utiliser un analyseur XML basé sur SAX pour analyser la réponse XML. Si vous générez une requête Ajax, configurez [!DNL Adobe Search&Promote] pour renvoyer des réponses JSON pour ces requêtes afin de faciliter l’analyse de la réponse.

## Sortie JSON de recherche guidée {#reference_EB8182A564DE4374BB84158F2AABEF74}

Tableaux décrivant la sortie de réponse JSON standard.

Voir aussi [Recherche guidée JSON Output](../c-appendices/c-guidedsearchoutput.md#reference_EB8182A564DE4374BB84158F2AABEF74).

Vous pouvez consulter la réponse JSON pour les éléments suivants :

* [Bannières](../c-appendices/c-guidedsearchoutput.md#section_88519CAAD25F4BD49D5E517077745B0E)
* [Chemin de navigation](../c-appendices/c-guidedsearchoutput.md#section_A7DB0F1DA9ED4CBCAE18395122F3E01E)
* [Facettes](../c-appendices/c-guidedsearchoutput.md#section_65932C95931743A1BFAF1DF16D7E6D92)
* [En-tête et Requête](../c-appendices/c-guidedsearchoutput.md#section_1D57062259CA46E0B4F598FA4EB37065)
* [Pagination](../c-appendices/c-guidedsearchoutput.md#section_504E7AB570BD49AF9839530DC438EE96)
* [Recherches récentes](../c-appendices/c-guidedsearchoutput.md#section_525816A0355C48F8970D89B8FC3F1FFF)
* [Résultats](../c-appendices/c-guidedsearchoutput.md#section_41AC56BB0A084BF59379B06C8BEF2157)
* [Formulaire de recherche](../c-appendices/c-guidedsearchoutput.md#section_434DA13EA295474C99FFE9F14801CD0E)
* [Tri](../c-appendices/c-guidedsearchoutput.md#section_558853CD376F4D71BACF211D53085D55)
* [Suggestions](../c-appendices/c-guidedsearchoutput.md#section_6EC104E1DDD94AC799B65E6E61A2FB3C)
* [Zones](../c-appendices/c-guidedsearchoutput.md#section_AE53A498B440465EAF2286F2AE87D548)

## Bannières {#section_88519CAAD25F4BD49D5E517077745B0E}

Exemple :

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les bannières </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> Noeud de bannière individuel. Vous pouvez avoir plusieurs noeuds de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Zone de la page Web dans laquelle la bannière est affichée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contenu HTML pour la zone de bannière. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Chemin de navigation {#section_A7DB0F1DA9ED4CBCAE18395122F3E01E}

Dans l’exemple suivant, chaque fois que le client se rétrécit davantage à travers les facettes, la sélection est ajoutée à la barre de navigation. Chaque élément est représenté sous la forme `<breadcrumb-item>`.

Exemple :

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans la barre de navigation </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Lien relatif vers les résultats de la recherche qui affiche la vue souhaitée. Le fait de cliquer sur un lien de chemin de navigation conduit le client à une vue dans laquelle toutes les améliorations suivantes sont supprimées. D’autres options sont également disponibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Texte destiné aux clients pour l’élément de chemin de navigation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facettes {#section_65932C95931743A1BFAF1DF16D7E6D92}

Les facettes sont des options de raffinement qui permettent aux clients de filtrer les résultats. Les facettes sont généralement utilisées pour la catégorisation, les plages de prix, les sélections de couleurs et d’autres ajustements d’attributs. Les métadonnées de l’index sont ce qui motive les facettes.

Il est courant de masquer ou d’afficher les facettes de catégorisation lorsqu’un client passe par la catégorisation. Le plus haut niveau de catégorisation (catégorie) est connu sous le nom de niveau 1. Lorsqu’un client clique sur une option de niveau 1, les options de raffinement de niveau 2 (sous-catégorie) s’affichent et les options de niveau 1 disparaissent. Lorsqu’un client clique sur une option de niveau 2, les options de raffinement de niveau 3 (sous-catégorie) s’affichent et les options de niveau 2 disparaissent. Comme nous l&#39;avons mentionné plus haut, ces options sont masquées et affichées. Votre application Web n&#39;est pas affectée par elles.

Chaque facette est contenue dans des balises `<facet-item>`. Dans l’exemple suivant, il présente une facette qui permet au client d’affiner les résultats de la recherche par &quot;vacances&quot;.

Exemple :

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item> 
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises en facettes </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Titre orienté client pour la facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Libellé destiné au client pour l’option de facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Lien relatif vers les résultats que l’option affine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nombre de résultats dans cet ensemble de résultats affiné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’une valeur de facette est sélectionnée, le noeud renvoie un "lien d’annulation" qui permet à un client d’annuler les résultats. </p> </td> 
  </tr> 
 </tbody> 
</table>

## En-tête et Requête {#section_1D57062259CA46E0B4F598FA4EB37065}

Exemple :

```xml
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

Utilisées ensemble, ces balises présentent un message tel que ce qui suit : &quot;Affichage des résultats 1 à 16 sur 621 pour la &quot;nouvelle année&quot;.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans l’en-tête et la requête </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> Requête de mots-clés envoyée avec la demande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Numéro de l'article du premier résultat sur cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Numéro de l'article du dernier résultat sur cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nombre total de résultats correspondant à la requête utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> Champ facultatif qui s’applique globalement aux résultats de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagination {#section_504E7AB570BD49AF9839530DC438EE96}

Exemple :

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans la pagination </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nombre total de pages de résultats, en fonction du nombre de résultats divisé par le nombre de résultats par page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la première page du jeu de résultats, sauf si le client consulte déjà la page 1. Dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la dernière page du jeu de résultats, sauf si le client consulte la dernière page. Dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la page précédente du jeu de résultats, sauf si le client consulte la page 1 ; dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la dernière page du jeu de résultats, sauf si le client consulte la dernière page. Dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers un numéro de page particulier. Dix numéros de page contigus s’affichent. À la page 1, il s'agirait des pages 1 à 10. À la fin de l'ensemble de résultats (dans ce cas, 39), il s'agirait des pages 30 à 39. Par exemple, au centre du jeu de résultats, page 15, il s’agirait des pages 11 à 20. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> Appliqué en tant qu’attribut à la page actuellement sélectionnée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recherches récentes {#section_525816A0355C48F8970D89B8FC3F1FFF}

Les recherches récentes sont une fonctionnalité basée sur des cookies qui ne fonctionne que si vous transmettez les informations des cookies aux serveurs.

Exemple :

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les recherches récentes </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> Noeud de recherche récente individuel. Vous pouvez avoir plusieurs noeuds de recherche récente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> Terme recherché précédemment par le client. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Liens vers la recherche précédente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Résultats {#section_41AC56BB0A084BF59379B06C8BEF2157}

Le jeu de résultats est une zone personnalisable de la réponse JSON. Chaque index est unique dans les mécanismes de nommage des champs des métadonnées. Des champs communs sont renvoyés pour chaque résultat, tels que le titre, la description et l’URL. Cependant, toutes les métadonnées définies pour une page de l’index peuvent être disponibles pour être utilisées dans chaque noeud de résultats. La catégorisation, les prix, les couleurs et les vignettes ne sont que quelques-unes des options que vous pouvez appliquer à un résultat pour obtenir des résultats de recherche plus convaincants.

Le format Résultats est personnalisé en fonction des métadonnées propres à votre implémentation. Toutes les données par résultat à afficher dans les résultats, y compris les URL des images miniatures, sont contenues ici.

En outre, il est possible de configurer plusieurs zones de résultats dans la page, telles que &quot;Résultats présentés&quot;, ou de séparer les sections &quot;Produits&quot; et &quot;Contenu&quot; des résultats. Dans ce cas, plusieurs zones de résultats sont fournies dans le code HTML, bien que les facettes ne soient associées qu’au jeu de résultats Principal.

Exemple :

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les résultats </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> Numéro de série du résultat dans ce jeu de résultats. Dans cet exemple, où dix résultats sont affichés par page, à la page 2 des résultats, le premier élément aurait un index de 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Titre destiné aux clients pour cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> URL de cette page. Il est utilisé pour créer un hyperlien qui permet au client de cliquer sur les résultats. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulaire de recherche {#section_434DA13EA295474C99FFE9F14801CD0E}

Exemple :

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans le formulaire de recherche </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Facultatif. Lorsqu’elle est présente dans le fichier JSON, une valeur de 1 indique que votre compte est lié à <span class="keyword"> Test&amp;Cible </span> et qu’il comporte au moins une règle métier qui fait partie d’un test A:B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> Facultatif. Lors de l’utilisation de la saisie semi-automatique, ce noeud est présent pour indiquer que le code CSS et JavaScript est présent sur la page, ainsi que le contenu du formulaire. En règle générale, ces champs ne changent pas, sauf si un utilisateur a modifié un paramètre de saisie semi-automatique. Dans ce cas, le champ xxx_cache_ver est incrémenté pour forcer l’invalidation du contenu mis en cache dans le navigateur de votre client. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> CSS associé à la saisie semi-automatique. Il est recommandé de placer cette balise en haut de la page pour améliorer le rendu des pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contenu requis dans votre recherche depuis l'utilitaire de saisie automatique pour se connecter au contrôle approprié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> JavaScript personnalisé requis pour la saisie semi-automatique. Il est recommandé de placer cette balise en bas de la page pour améliorer le rendu des pages. Le code JavaScript YUI est également requis pour la saisie automatique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient tous les paramètres masqués (nom et valeur) à inclure dans le formulaire de recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tri {#section_558853CD376F4D71BACF211D53085D55}

L&#39;exemple suivant montre les données d&#39;un menu de tri à trois options. Le menu permet au client de trier par pertinence, titre ou classement. L’élément actuellement sélectionné comprend un attribut &quot;selected=true&quot;. &quot;. Toujours offre une option de pertinence pour permettre à un client de revenir aux résultats de recherche par défaut qui étaient initialement affichés.

Exemple :

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans le menu Trier </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Texte de l’option destiné aux clients. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Représente la valeur du paramètre de chaîne de requête "sort" pour cette option. Cette balise n’est pas nécessaire si la valeur <span class="codeph"> &lt;link&gt; </span> est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Pour les options non sélectionnées, le paramètre <span class="codeph"> &lt;link&gt; </span> contient le lien relatif qui renvoie le même jeu de résultats, trié par le nouveau paramètre de tri. Ce champ est vide pour l’option de tri actuellement sélectionnée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggestions {#section_6EC104E1DDD94AC799B65E6E61A2FB3C}

Les suggestions sont renvoyées lorsqu’il n’y a que quelques résultats ou qu’aucun résultat n’est obtenu. Ce noeud contient des termes qui génèrent des requêtes réussies et peut être affiché sur une page &quot;Aucun résultat&quot;. Le lien est également renvoyé afin qu’un client puisse accéder à la nouvelle requête.

Exemple :

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les suggestions </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Lien relatif utilisé pour créer un hyperlien permettant de rechercher les résultats du terme de suggestion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>Terme suggéré. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_AE53A498B440465EAF2286F2AE87D548}

Exemple :

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises en zones </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> Noeud de zone individuel. Vous pouvez avoir plusieurs noeuds de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nom de la zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 ou 0 pour indiquer si la zone est affichée ou non. Le contenu de la zone peut être statique sur votre page Web ou dans les résultats de la recherche, par exemple les meilleurs vendeurs ou les produits associés. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sortie XML de recherche guidée {#reference_D93E859A277643068B10AE7A61C973EA}

Tableaux décrivant la sortie de réponse XML standard.

Vous pouvez consulter la réponse XML pour les éléments suivants :

* [Bannières](../c-appendices/c-guidedsearchoutput.md#section_6A19EC26DD3B494194AAA788151B78B5)
* [Chemin de navigation](../c-appendices/c-guidedsearchoutput.md#section_E48A71B0EBDB4EDDA7587009AD865488)
* [Facettes](../c-appendices/c-guidedsearchoutput.md#section_5CEB1F966C004FFEA3CF675638966E25)
* [En-tête et Requête](../c-appendices/c-guidedsearchoutput.md#section_802835E19BCB48239C6770A1B72DFFF8)
* [Pagination](../c-appendices/c-guidedsearchoutput.md#section_72DB86DDE1284B1EA295CFFBC16A3150)
* [Recherches récentes](../c-appendices/c-guidedsearchoutput.md#section_BCA2DDD17F264CF6BA11634E1A514E28)
* [Résultats](../c-appendices/c-guidedsearchoutput.md#section_EC496F5CA2634158891455E2F6DF6833)
* [Formulaire de recherche](../c-appendices/c-guidedsearchoutput.md#section_F92D8C3D37174A10A4E26CAFF3F3DF89)
* [Tri](../c-appendices/c-guidedsearchoutput.md#section_32DC50A103BF491BA3665A5CADCCAADE)
* [Suggestions](../c-appendices/c-guidedsearchoutput.md#section_D81BCE46F0AF443695DF9C4BA084B716)
* [Zones](../c-appendices/c-guidedsearchoutput.md#section_15D8AA585F3246799968BA88EE2C9FC2)

## Bannières {#section_6A19EC26DD3B494194AAA788151B78B5}

Exemple :

```xml
<banners> 
 <banner> 
  <area><![CDATA[top-left]]></area> 
  <content><![CDATA[<img src="https://www.megacorp.com/discount.gif"/>]]></content> 
 </banner> 
</banners>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les bannières </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;banner&gt; </span> </p> </td> 
   <td colname="col2"> <p> Noeud de bannière individuel. Vous pouvez avoir plusieurs noeuds de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;area&gt; </span> </p> </td> 
   <td colname="col2"> <p> Zone de la page Web dans laquelle la bannière est affichée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contenu HTML pour la zone de bannière. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Chemin de navigation {#section_E48A71B0EBDB4EDDA7587009AD865488}

Dans l’exemple suivant, chaque fois que le client se rétrécit davantage à travers les facettes, la sélection est ajoutée à la barre de navigation. Chaque élément est représenté sous la forme `<breadcrumb-item>`.

Exemple :

```xml
 <breadcrumb> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year]]></link> 
   <value><![CDATA[new year]]></value> 
  </breadcrumb-item> 
  <breadcrumb-item> 
   <link><![CDATA[?q=new+year;q1=Articles;x1=content-type]]></link> 
   <value><![CDATA[Articles]]></value> 
  </breadcrumb-item> 
 </breadcrumb> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans la barre de navigation </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Lien relatif vers les résultats de la recherche qui affiche la vue souhaitée. Le fait de cliquer sur un lien de chemin de navigation conduit le client à une vue dans laquelle toutes les améliorations suivantes sont supprimées. D’autres options sont également disponibles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Texte destiné aux clients pour l’élément de chemin de navigation. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facettes {#section_5CEB1F966C004FFEA3CF675638966E25}

Les facettes sont des options de raffinement qui permettent aux clients de filtrer les résultats. Les facettes sont généralement utilisées pour la catégorisation, les plages de prix, les sélections de couleurs et d’autres ajustements d’attributs. Les métadonnées de l’index sont ce qui motive les facettes.

Il est courant de masquer ou d’afficher les facettes de catégorisation lorsqu’un client passe par la catégorisation. Le plus haut niveau de catégorisation (catégorie) est connu sous le nom de niveau 1. Lorsqu’un client clique sur une option de niveau 1, les options de raffinement de niveau 2 (sous-catégorie) s’affichent et les options de niveau 1 disparaissent. Lorsqu’un client clique sur une option de niveau 2, les options de raffinement de niveau 3 (sous-catégorie) s’affichent et les options de niveau 2 disparaissent. Comme nous l&#39;avons mentionné plus haut, ces options sont masquées et affichées. Votre application Web n&#39;est pas affectée par elles.

Chaque facette est contenue dans des balises `<facet-item>`. Dans l’exemple suivant, il présente une facette qui permet au client d’affiner les résultats de la recherche par &quot;vacances&quot;.

Exemple :

```xml
 <facets> 
  <facet-item> 
   <facet-title><![CDATA[Holidays]]></facet-title> 
   <facet-value> 
    <label><![CDATA[New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[11]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Christmas]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Christmas;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Chinese New Year]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Chinese+New+Year;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Thanksgiving]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Thanksgiving;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[4th of July]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=4th+of+July;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Father&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Father's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Hanukkah]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Hanukkah;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Mother&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Mother's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Valentine&#39;s Day]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Valentine's+Day;x1=content-type;x2=holidays]]></link> 
    <count><![CDATA[1]]></count> 
   </facet-value> 
  </facet-item> 
  <facet-item> 
   <facet-title><![CDATA[Seasons]]></facet-title> 
   <facet-value> 
    <label><![CDATA[Winter]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Winter;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[20]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Summer]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Summer;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[7]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Autumn]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Autumn;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[4]]></count> 
   </facet-value> 
   <facet-value> 
    <label><![CDATA[Spring]]></label> 
    <link><![CDATA[?q=new+year;q1=Articles;q2=Spring;x1=content-type;x2=seasons]]></link> 
    <count><![CDATA[2]]></count> 
   </facet-value> 
  </facet-item>  
 </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises en facettes </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Titre orienté client pour la facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Libellé destiné au client pour l’option de facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Lien relatif vers les résultats que l’option affine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;count&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nombre de résultats dans cet ensemble de résultats affiné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;undolink&gt; </span> </p> </td> 
   <td colname="col2"> <p> Lorsqu’une valeur de facette est sélectionnée, le noeud renvoie un "lien d’annulation" qui permet à un client d’annuler les résultats. </p> </td> 
  </tr> 
 </tbody> 
</table>

## En-tête et Requête {#section_802835E19BCB48239C6770A1B72DFFF8}

Exemple :

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<result> 
 <query> 
  <user-query><![CDATA[new year]]></user-query> 
  <lower-results><![CDATA[1]]></lower-results> 
  <upper-results><![CDATA[16]]></upper-results> 
  <total-results><![CDATA[621]]></total-results> 
 </query> 
```

Utilisées ensemble, ces balises présentent un message tel que ce qui suit : &quot;Affichage des résultats 1 à 16 sur 621 pour la &quot;nouvelle année&quot;.&quot;

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans l’en-tête et la Requête </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;user-query&gt; </span> </p> </td> 
   <td colname="col2"> <p> Requête de mots-clés envoyée avec la demande. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;lower-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Numéro de l'article du premier résultat sur cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;upper-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Numéro de l'article du dernier résultat sur cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-results&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nombre total de résultats correspondant à la requête utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;custom-field&gt; </span> </p> </td> 
   <td colname="col2"> <p> Champ facultatif qui s’applique globalement aux résultats de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagination {#section_72DB86DDE1284B1EA295CFFBC16A3150}

Exemple :

```xml
<pagination> 
 <total-pages><39></total-pages> 
 <pages> 
   <page position="first"></page> 
   <page position="last">?i=1;page=39;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="previous"></page> 
   <page position="next">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="1" selected="true">?i=1;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="2">?i=1;page=2;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="3">?i=1;page=3;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="4">?i=1;page=4;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="5">?i=1;page=5;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="6">?i=1;page=6;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="7">?i=1;page=7;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="8">?i=1;page=8;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="9">?i=1;page=9;q=new+year;q1=Articles;x1=content-type]]></page> 
   <page position="10">?i=1;page=10;q=new+year;q1=Articles;x1=content-type]]></page> 
 </pages> 
</pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans la pagination </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;total-pages&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nombre total de pages de résultats, en fonction du nombre de résultats divisé par le nombre de résultats par page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="first"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la première page du jeu de résultats, sauf si le client consulte déjà la page 1. Dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="last"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la dernière page du jeu de résultats, sauf si le client consulte la dernière page. Dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="previous"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la page précédente du jeu de résultats, sauf si le client consulte la page 1 ; dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="next"&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers la dernière page du jeu de résultats, sauf si le client consulte la dernière page. Dans ce cas, il est vide. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;page position="x"&gt;</span> </p> </td> 
   <td colname="col2"> <p> Contient un lien relatif vers un numéro de page particulier. Dix numéros de page contigus s’affichent. À la page 1, il s'agirait des pages 1 à 10. À la fin de l'ensemble de résultats (dans ce cas, 39), il s'agirait des pages 30 à 39. Par exemple, au centre du jeu de résultats, page 15, il s’agirait des pages 11 à 20. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> selected="true"&gt;  </span> </p> </td> 
   <td colname="col2"> <p> Appliqué en tant qu’attribut à la page actuellement sélectionnée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recherches récentes {#section_BCA2DDD17F264CF6BA11634E1A514E28}

Les recherches récentes sont une fonctionnalité basée sur des cookies qui ne fonctionne que si vous transmettez les informations des cookies aux serveurs.

Exemple :

```xml
<recent-searches> 
 <recent-search> 
  <search-term><![CDATA[shoes]]></search-term> 
  <link><![CDATA[?q=shoes]]></link> 
 </recent-search> 
</recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les recherches récentes </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;recent-search&gt; </span> </p> </td> 
   <td colname="col2"> <p> Noeud de recherche récente individuel. Vous pouvez avoir plusieurs noeuds de recherche récente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;search-term&gt; </span> </p> </td> 
   <td colname="col2"> <p> Terme recherché précédemment par le client. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Liens vers la recherche précédente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Résultats {#section_EC496F5CA2634158891455E2F6DF6833}

Le jeu de résultats est une zone personnalisable de la réponse XML. Chaque index est unique dans les mécanismes de nommage des champs des métadonnées. Des champs communs sont renvoyés pour chaque résultat, tels que le titre, la description et l’URL. Cependant, toutes les métadonnées définies pour une page de l’index peuvent être disponibles pour être utilisées dans chaque noeud de résultats. La catégorisation, les prix, les couleurs et les vignettes ne sont que quelques-unes des options que vous pouvez appliquer à un résultat pour obtenir des résultats de recherche plus convaincants.

Le format Résultats est personnalisé en fonction des métadonnées propres à votre implémentation. Toutes les données par résultat à afficher dans les résultats, y compris les URL des images miniatures, sont contenues ici.

En outre, il est possible de configurer plusieurs zones de résultats dans la page, telles que &quot;Résultats présentés&quot;, ou de séparer les sections &quot;Produits&quot; et &quot;Contenu&quot; des résultats. Dans ce cas, plusieurs zones de résultats sont fournies dans le code HTML, bien que les facettes ne soient associées qu’au jeu de résultats Principal.

Exemple :

```xml
 <results> 
  <result> 
    <index><![CDATA[1]]></index> 
    <result-title><![CDATA[New Year's Eve Slumber Party]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-eve-slumber-party-705199/]]></url> 
    <meta-description><![CDATA[Fun New Year's celebration ideas for your kids]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve-

slumber-party-parties-photo-80-FF1200SLEEPA18.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/new-years-eve- 
slumber-party-parties-photo-160-FF1200SLEEPA18.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Nancy Mades]]></byline> 
    <blurb><![CDATA[Fun New Year's celebration ideas for your kids]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[2]]></index> 
    <result-title><![CDATA[10 Holiday Traditions to Start This Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/10-holiday-traditions-to-start-this-year-704781/]]></url> 
    <meta-description><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <small-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-80-FF1107HOLIA01.jpg]]></small-thumbnail-img> 
    <large-thumbnail-img><![CDATA[https://mysite.com/assets/cms/parties/10-holiday- 
traditions-to-start-this-year-parties-photo-160-FF1107HOLIA01.jpg]]></large-thumbnail-img> 
    <byline><![CDATA[Julie Taylor]]></byline> 
    <blurb><![CDATA[Reader ideas to make Thanksgiving, Christmas, and New Year's even more magical]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[3]]></index> 
    <result-title><![CDATA[A Perfect New Year's Eve]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/a-perfect-new-years-eve-705258/]]></url> 
    <meta-description><![CDATA[You can turn New Year's into a celebration for the whole family.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Teri Keough]]></byline> 
    <blurb><![CDATA[You can turn New Year's into a celebration for the whole family.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[4]]></index> 
    <result-title><![CDATA[New Year's Fun and Games]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/new-years-fun-and-games-705220/]]></url> 
    <meta-description><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Charlotte Meryman]]></byline> 
    <blurb><![CDATA[Craft, game and food ideas for a New Year's celebration with kids.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[5]]></index> 
    <result-title><![CDATA[11 Great Ways to Start the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/11-great-ways-to-start-the-new-year-705552/]]></url> 
    <meta-description><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <byline><![CDATA[Emily Block]]></byline> 
    <blurb><![CDATA[11 New Family Traditions to Start This Year from My Magazine]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[6]]></index> 
    <result-title><![CDATA[Celebrating Chinese New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/parties/celebrating-chinese-new-year-705260/]]></url> 
    <meta-description><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></meta-description> 
    <category><![CDATA[parties]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Crafts, food, and games to help you celebrate Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[7]]></index> 
    <result-title><![CDATA[New Year's Eve, Family Style]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/new-years-eve-family-style-701283/]]></url> 
    <meta-description><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Start a family New Year's Eve tradition by having an evening of kid-focused fun at home]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[8]]></index> 
    <result-title><![CDATA[Chinese New Year Activities]]></result-title> 
    <url><![CDATA[https://mysite.com/crafts/chinese-new-year-activities-710345/]]></url> 
    <meta-description><![CDATA[Activities for celebrating Chinese New Year.]]></meta-description> 
    <category><![CDATA[crafts]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Activities for celebrating Chinese New Year.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[9]]></index> 
    <result-title><![CDATA[More Organized in the New Year]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/more-organized-in-the-new-year-701284/]]></url> 
    <meta-description><![CDATA[Tips for getting your household more organized--and getting the kids to help.]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Tips for getting your household more organized--and getting your kids to help out.]]></blurb> 
  </result>   
  <result> 
    <index><![CDATA[10]]></index> 
    <result-title><![CDATA[Checklists: Year-End Safety Checklist]]></result-title> 
    <url><![CDATA[https://mysite.com/holidays/checklists-year-end-safety-checklist-701352/]]></url> 
    <meta-description><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></meta-description> 
    <category><![CDATA[holidays]]></category> 
    <content-type><![CDATA[Articles]]></content-type> 
    <blurb><![CDATA[Make sure that your home is safe with our year-end safety checklist!]]></blurb> 
  </result>   
 </results> 
</customer-result> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les résultats </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;index&gt; </span> </p> </td> 
   <td colname="col2"> <p> Numéro de série du résultat dans ce jeu de résultats. Dans cet exemple, où dix résultats sont affichés par page, à la page 2 des résultats, le premier élément aurait un index de 11. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result-title&gt; </span> </p> </td> 
   <td colname="col2"> <p> Titre destiné aux clients pour cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;url&gt; </span> </p> </td> 
   <td colname="col2"> <p> URL de cette page. Il est utilisé pour créer un hyperlien qui permet au client de cliquer sur les résultats. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulaire de recherche {#section_F92D8C3D37174A10A4E26CAFF3F3DF89}

Exemple :

```xml
<search-form> 
 <include-tnt-mbox>1 </included-tnt-mbox> 
 <autocomplete> 
  <css><![CDATA[<!--link rel="stylesheet" type="te 
        xt/css"href="//content.atomz.com/sp000000a8/publish/autoc 
        omplete_styles.css?sp_css_cache_ver=2" /-->]]> 
  </css> 
  <form-content><![CDATA[<div id="autocomplete"></div>]]> 
  </form-content> 
  <js><![CDATA[<script type="text/javascript" 
   src="//content.atomz.com/sp100491de/publish/autoc 
   omplete_data.js?sp_js_cache_ver=3"></script>]]> 
  </js> 
 </autcomplete> 
 <hidden-parameters> 
  <parameter> 
   <name><![CDATA[store]]></name> 
   <value><![CDATA[mens]]></value> 
  </parameter> 
 </hidden-parameters> 
</search-form>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans le formulaire de recherche </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;include-tnt-mbox&gt; </span> </p> </td> 
   <td colname="col2"> <p> Facultatif. Lorsqu’elle est présente dans le code XML, la valeur 1 indique que votre compte est lié à <span class="keyword"> Test&amp;Cible </span> et qu’il comporte au moins une règle métier qui fait partie d’un test A:B. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;autocomplete&gt; </span> </p> </td> 
   <td colname="col2"> <p> Facultatif. Lors de l’utilisation de la saisie semi-automatique, ce noeud est présent pour indiquer que le code CSS et JavaScript est présent sur la page, ainsi que le contenu du formulaire. En règle générale, ces champs ne changent pas, sauf si un utilisateur a modifié un paramètre de saisie semi-automatique. Dans ce cas, le champ xxx_cache_ver est incrémenté pour forcer l’invalidation du contenu mis en cache dans le navigateur de votre client. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;css&gt; </span> </p> </td> 
   <td colname="col2"> <p> CSS associé à la saisie semi-automatique. Il est recommandé de placer cette balise en haut de la page pour améliorer le rendu des pages. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;form-content&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contenu requis dans votre recherche depuis l'utilitaire de saisie automatique pour se connecter au contrôle approprié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;js&gt; </span> </p> </td> 
   <td colname="col2"> <p> JavaScript personnalisé requis pour la saisie semi-automatique. Il est recommandé de placer cette balise en bas de la page pour améliorer le rendu des pages. Le code JavaScript YUI est également requis pour la saisie automatique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;hidden-parameters&gt; </span> </p> </td> 
   <td colname="col2"> <p> Contient tous les paramètres masqués (nom et valeur) à inclure dans le formulaire de recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Tri {#section_32DC50A103BF491BA3665A5CADCCAADE}

L&#39;exemple suivant montre les données d&#39;un menu de tri à trois options. Le menu permet au client de trier par pertinence, titre ou classement. L’élément actuellement sélectionné comprend un attribut &quot;selected=true&quot;. &quot;. Toujours offre une option de pertinence pour permettre à un client de revenir aux résultats de recherche par défaut qui étaient initialement affichés.

Exemple :

```xml
 <sort> 
  <sort-item selected="true"> 
   <label><![CDATA[Relevance]]></label> 
   <value><![CDATA[relevance]]></value> 
   <link><![CDATA[]]></link> 
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Title]]></label> 
   <value><![CDATA[title]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=title;x1=content-type]]></link>     
  </sort-item> 
  <sort-item> 
   <label><![CDATA[Rating]]></label> 
   <value><![CDATA[user-rating]]></value> 
   <link><![CDATA[?q=new+year;q1=Articles;sort=user-rating;x1=content-type]]></link>     
  </sort-item> 
 </sort>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans le menu Trier </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;label&gt; </span> </p> </td> 
   <td colname="col2"> <p> Texte de l’option destiné aux clients. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;value&gt; </span> </p> </td> 
   <td colname="col2"> <p> Représente la valeur du paramètre de chaîne de requête "sort" pour cette option. Cette balise n’est pas nécessaire si la valeur <span class="codeph"> &lt;link&gt; </span> est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p> Pour les options non sélectionnées, le paramètre <span class="codeph"> &lt;link&gt; </span> contient le lien relatif qui renvoie le même jeu de résultats, trié par le nouveau paramètre de tri. Ce champ est vide pour l’option de tri actuellement sélectionnée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggestions {#section_D81BCE46F0AF443695DF9C4BA084B716}

Les suggestions sont renvoyées lorsqu’il n’y a que quelques résultats ou qu’aucun résultat n’est obtenu. Ce noeud contient des termes qui génèrent des requêtes réussies et peut être affiché sur une page &quot;Aucun résultat&quot;. Le lien est également renvoyé afin qu’un client puisse accéder à la nouvelle requête.

Exemple :

```xml
 <suggestions> 
  <suggestion-item> 
   <link><![CDATA[?q=video]]></link> 
   <word><![CDATA[video]]> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises dans les suggestions </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;link&gt; </span> </p> </td> 
   <td colname="col2"> <p>Lien relatif utilisé pour créer un hyperlien permettant de rechercher les résultats du terme de suggestion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;word&gt; </span> </p> </td> 
   <td colname="col2"> <p>Terme suggéré. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_15D8AA585F3246799968BA88EE2C9FC2}

Exemple :

```xml
<zones> 
 <zone> 
  <name><![CDATA[best-sellers]]></name> 
  <display><![CDATA[1]]></display> 
 </zone> 
</zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balises en zones </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;zone&gt; </span> </p> </td> 
   <td colname="col2"> <p> Noeud de zone individuel. Vous pouvez avoir plusieurs noeuds de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;name&gt; </span> </p> </td> 
   <td colname="col2"> <p> Nom de la zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;display&gt; </span> </p> </td> 
   <td colname="col2"> <p> 1 ou 0 pour indiquer si la zone est affichée ou non. Le contenu de la zone peut être statique sur votre page Web ou dans les résultats de la recherche, par exemple les meilleurs vendeurs ou les produits associés. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Sortie XML de recherche guidée pour Adobe Experience Manager {#reference_DBE13C606C3A4BB185DE53F88D0D3048}

Tableaux décrivant la sortie de réponse XML standard pour AEM (Adobe Experience Manager).

Voir également . [Sortie XML de recherche guidée](../c-appendices/c-guidedsearchoutput.md#reference_D93E859A277643068B10AE7A61C973EA)

Vous pouvez consulter la réponse XML pour les éléments suivants :

* [Bannières](../c-appendices/c-guidedsearchoutput.md#section_B16EDC5533FA4494AC9983AA7357CBE3)
* [Chemin de navigation](../c-appendices/c-guidedsearchoutput.md#section_49EA7043FBE44315A79A4E738BE30114)
* [Champs personnalisés](../c-appendices/c-guidedsearchoutput.md#section_38DD31AFE5DD4263A63644AFF484E0F4)
* [Facettes](../c-appendices/c-guidedsearchoutput.md#section_BE98990E3DD748A1BD4E0CA322314B79)
* [En-tête](../c-appendices/c-guidedsearchoutput.md#section_5305B1DC5774439485CA0665DB683F9C)
* [Menus et tri](../c-appendices/c-guidedsearchoutput.md#section_A34CBB645DBF4C70A12A5B7E81211295)
* [Pagination](../c-appendices/c-guidedsearchoutput.md#section_E52F81C6A6EB4B8F996157B657EC540F)
* [Requête](../c-appendices/c-guidedsearchoutput.md#section_3DAA1013F09742869B80F6A361816E6C)
* [Recherches récentes](../c-appendices/c-guidedsearchoutput.md#section_17F942F6EC07456DABED7A483AC08446)
* [Résultats](../c-appendices/c-guidedsearchoutput.md#section_155A80B8C4F641678DD9C8F257108412)
* [Formulaire de recherche](../c-appendices/c-guidedsearchoutput.md#section_9E4B99D4FEDC49629F6C7E866F3A7493)
* [Suggestions](../c-appendices/c-guidedsearchoutput.md#section_2899FACB9AD84F60B3687C1B4EF09E15)
* [Modèle](../c-appendices/c-guidedsearchoutput.md#section_1E2BB2F274B04F5491A4CCCC38F507BD)
* [Zones](../c-appendices/c-guidedsearchoutput.md#section_26C4A947E7B1474A8E37D86D9579B93E)

## Bannières {#section_B16EDC5533FA4494AC9983AA7357CBE3}

La recherche sur site/le marchandisage peut gérer les bannières d’un client, en branchant les bannières en plusieurs parties sur une page Web.

Exemple de bannière :

Voici un exemple de bannière placée dans la zone des pages appelée &quot;haut&quot;.

```xml
   <banners> 
       <banner> 
           <area><![CDATA[top]]></area> 
           <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
       </banner> 
    </banners> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>bannières </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Contient des noeuds de bannière 0-n indiquant chaque zone de bannière et le contenu connecté à cette zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>bannière </p> </td> 
   <td colname="col2"> <p>bannières </p> </td> 
   <td colname="col3"> <p>Noeud de bannière individuel. Vous pouvez avoir plusieurs noeuds de bannière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>area </p> </td> 
   <td colname="col2"> <p>bannière </p> </td> 
   <td colname="col3"> <p>Zone de la page Web dans laquelle la bannière est affichée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>content </p> </td> 
   <td colname="col2"> <p>bannière </p> </td> 
   <td colname="col3"> <p>Contenu de la bannière. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Chemin de navigation {#section_49EA7043FBE44315A79A4E738BE30114}

Plusieurs chemins de navigation sont pris en charge. Vous pouvez définir des chemins de navigation et leur comportement correspondant dans **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**. En outre, vous devez attribuer un nom unique pour chaque chemin de navigation que vous définissez. Le noeud XML des chemins de navigation effectue une itération sur tous les chemins de navigation définis. Il est recommandé de n&#39;afficher qu&#39;un seul chemin de navigation dans les résultats de la recherche.

Dans l’exemple suivant, chaque fois que le client se rétrécit davantage à travers les facettes, la sélection est ajoutée à la barre de navigation. Chaque élément est représenté sous la forme `<breadcrumb-item>`.

Exemple de noeud de chemin de navigation :

```xml
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;sp_cs=UTF-8;view=xml]]></link> 
   <value><![CDATA[mens]]></value> 
                <label><![CDATA[]]></label> 
      </breadcrumb-item> 
     <breadcrumb-item> 
   <link><![CDATA[?i=1;q=mens;q1=Channel;sp_cs=UTF-8;view=xml;x1=brand]]></link> 
   <value><![CDATA[Channel]]></value> 
                <label><![CDATA[brand]]></label> 
      </breadcrumb-item> 
   </breadcrumb> 
    </breadcrumbs> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>fil d'Ariane </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p> Contient des noeuds de chemin de navigation 0-n qui définissent chaque chemin de navigation. La plupart des clients n'ont qu'un seul chemin de navigation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>fil d'Ariane </p> </td> 
   <td colname="col2"> <p>fil d'Ariane </p> </td> 
   <td colname="col3"> <p> Contient les noeuds enfants définissant la définition d’un chemin de navigation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>fil d'Ariane </p> </td> 
   <td colname="col3"> <p> Nom du chemin de navigation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>breadcrumb-item </p> </td> 
   <td colname="col2"> <p>Élément individuel dans le chemin de navigation. Chaque élément indique une étape de la piste lorsque l’utilisateur affine l’ensemble de résultats. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>breadcrumb-item </p> </td> 
   <td colname="col3"> <p> Lien relatif vers les résultats de la recherche qui affiche la vue souhaitée. Le fait de cliquer sur un lien de chemin de navigation conduit le client à une vue dans laquelle toutes les améliorations suivantes sont supprimées. D’autres options sont également disponibles, telles que déposer et supprimer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>breadcrumb-item </p> </td> 
   <td colname="col3"> <p> Texte destiné aux clients pour l’élément de chemin de navigation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>libellé </p> </td> 
   <td colname="col2"> <p>breadcrumb-item </p> </td> 
   <td colname="col3"> <p> La balise d’étiquette génère un libellé pour une valeur de chemin de navigation qui détaille la facette sélectionnée pour générer cet élément de chemin de navigation. Il n'est utilisé que dans le contexte d'un bloc de chemin de fer guidé. Pour l’étape de requête terme, ce champ est vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Champs personnalisés {#section_38DD31AFE5DD4263A63644AFF484E0F4}

Les champs personnalisés sont une collection diverse de variables avec un contexte global. Il est généralement utilisé pour transmettre des variables à des fins d’optimisation du référencement définies dans les métadonnées de la page des résultats de la recherche.

Exemple de noeud de champs personnalisés :

```xml
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>champs personnalisés </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p> Peut contenir des noeuds enfants 0-n qui définissent des champs personnalisés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>champ personnalisé </p> </td> 
   <td colname="col2"> <p>champs personnalisés </p> </td> 
   <td colname="col3"> <p> Facultatif. Contient une valeur pour un champ personnalisé donné indiqué par l’attribut name. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Facettes {#section_BE98990E3DD748A1BD4E0CA322314B79}

Les facettes sont des options de raffinement qui permettent aux clients de filtrer les résultats. Les facettes sont généralement utilisées pour la catégorisation, les plages de prix, les sélections de couleurs et d’autres ajustements d’attributs. Les facettes sont construites sur les métadonnées de l’index.

Il est courant de masquer ou d’afficher les facettes de catégorisation lorsqu’un client passe par la catégorisation. Le plus haut niveau de catégorisation (catégorie) est connu sous le nom de niveau 1. Lorsqu’un client clique sur une option de niveau 1, les options de raffinement de niveau 2 (sous-catégorie) s’affichent et les options de niveau 1 disparaissent. Lorsqu’un client clique sur une option de niveau 2, les options de raffinement de niveau 3 (sous-catégorie) s’affichent et les options de niveau 2 disparaissent. Comme indiqué ci-dessus, ces options sont masquées et affichées ; votre application web ne les affecte pas.

Chaque facette est contenue dans des balises `<facet-item>`. Dans l’exemple suivant, il présente une facette qui permet au client d’affiner les résultats de recherche par &quot;vacances&quot;.

Exemple de bloc de facettes :

```xml
<facets>          
     <facet> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undo-link> 
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;q2=Mens;sp_staged=1;view=xml;x1=brand;x2=leveli]]></link> 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Armora+Jeans;sp_staged=1;view=xml;x1=brand]]></undolink> 
      </facet-value> 
      </facet> 
     <facet> 
         <facet-title><![CDATA[Sub-Category]]></facet-title> 
                <behavior><![CDATA[sticky]]></behavior> 
                <selected>0</selected> 
      <facet-value>           
              <label><![CDATA[Apparel]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans;q3=Apparel;sp_staged=1;view=xml;x1=leveli;x2=brand;x3=levelii]]></link> 
       <count><![CDATA[3]]></count>                         
      </facet-value>   
      </facet>         
     <facet> 
         <facet-title><![CDATA[Brand]]></facet-title> 
                <behavior><![CDATA[multi-select]]></behavior> 
                <selected>1</selected> 
                <undo-link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undo-link> 
      <facet-value>        
              <label><![CDATA[Amoura]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Amoura;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[9]]></count>                         
      </facet-value>   
      <facet-value>         
              <label><![CDATA[Armora]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[12]]></count>                        
      </facet-value>   
      <facet-value> 
          <selected><![CDATA[true]]></selected> 
              <label><![CDATA[Armora Jeans]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Armora+Jeans;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
 
       <count><![CDATA[3]]></count> 
                        <undolink><![CDATA[?i=1;lang=enus;q=*;q1=Mens;sp_staged=1;view=xml;x1=leveli]]></undolink> 
      </facet-value>   
      <facet-value>           
              <label><![CDATA[Art of Grooming]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Art+of+Grooming;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count>                         
      </facet-value>   
      <facet-value>          
              <label><![CDATA[Bear Co.]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Bear+Co.;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[1]]></count> 
      </facet-value> 
      <facet-value>      
              <label><![CDATA[Citizens]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|Citizens;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[4]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[D&amp;B]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|D%26B;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[17]]></count> 
      </facet-value> 
      <facet-value> 
              <label><![CDATA[David Yuri]]></label> 
       <link><![CDATA[?i=1;lang=enus;q=*;q1=Mens;q2=Armora+Jeans|David+Yuri;sp_staged=1;view=xml;x1=leveli;x2=brand]]></link> 
       <count><![CDATA[2]]></count>    
      </facet-value>   
      </facet> 
    </facets> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>facettes </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Noeud de facettes de conteneur contenant des noeuds enfants 0-n représentant chaque facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facette </p> </td> 
   <td colname="col2"> <p>facettes </p> </td> 
   <td colname="col3"> <p> Une instance de facette unique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facette-titre </p> </td> 
   <td colname="col2"> <p>facette </p> </td> 
   <td colname="col3"> <p>Titre orienté client pour la facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>comportement </p> </td> 
   <td colname="col2"> <p>facette </p> </td> 
   <td colname="col3"> <p>Comportement de la facette. Par exemple, normal, bascule ou à sélection multiple. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sélectionnés </p> </td> 
   <td colname="col2"> <p>facette </p> </td> 
   <td colname="col3"> <p>1 si la facette a une valeur sélectionnée sinon 0. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>undo-link </p> </td> 
   <td colname="col2"> <p>facette </p> </td> 
   <td colname="col3"> <p> Uniquement présente lorsque la facette est sélectionnée. Annuler le lien inverse la facette entière. Par exemple, s’il s’agit d’une facette à sélection multiple, elle désélectionne toutes les options sélectionnées pour la facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>facet-value </p> </td> 
   <td colname="col2"> <p>facette </p> </td> 
   <td colname="col3"> <p>Contient tous les éléments de facette individuels appartenant à la facette. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>sélectionnés </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>Si l’élément actif avec la facette est sélectionné, ce noeud est présent et défini sur "true". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>libellé </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>Libellé destiné au client pour l’option de facette. Par défaut, cette option doit déjà être précédée d’une séquence d’échappement HTML. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p> Lien relatif aux résultats que l’option affine davantage. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>count </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>Nombre de résultats dans cet ensemble de résultats affiné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>undo-link </p> </td> 
   <td colname="col2"> <p>facet-value </p> </td> 
   <td colname="col3"> <p>Lorsqu’une valeur de facette est sélectionnée, le noeud renvoie un "lien d’annulation" qui permet au client d’annuler la sélection de cette facette individuelle. </p> </td> 
  </tr> 
 </tbody> 
</table>

## En-tête {#section_5305B1DC5774439485CA0665DB683F9C}

Exemple :

```xml
xml version="1.0" encoding="utf-8" standalone="yes" 
```

## Menus et tri {#section_A34CBB645DBF4C70A12A5B7E81211295}

Les menus permettant de trier les résultats sont pris en charge et de modifier le nombre de résultats à renvoyer par page. Il prend également en charge un menu de navigation utile pour l’utilisation de la fonction &quot;recherche en tant que navigation&quot;. Un compte peut définir plusieurs menus du même type et utiliser n&#39;importe lequel des menus pour leur présentation.

Exemple de noeud de menus :

L&#39;exemple suivant montre les données d&#39;un menu de tri et d&#39;un menu de navigation à trois options. Le menu de tri permet au client de trier par pertinence, titre ou classement. L’élément actuellement sélectionné comprend un attribut &quot;selected=true&quot;. &quot;. Toujours offre une option de pertinence pour permettre à un client de revenir aux résultats de recherche par défaut qui étaient initialement affichés.

```xml
<menus> 
        <menu> 
           <name><![CDATA[sort]]></name>         
             <item selected="true"> 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=mens;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>   
                    <item> 
                        <label><![CDATA[WOMEN'S]]></label> 
          <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[MEN'S]]></label> 
          <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
          <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
          <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
          <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
          <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[GIFTS & HOME]]></label> 
          <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[CHILDREN & TOYS]]></label> 
          <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link> 
                    </item> 
                    <item> 
                        <label><![CDATA[ELECTRONICS]]></label> 
          <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
          <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link> 
                    </item> 
        </menu> 
    </menus> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>menus </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Contient des noeuds enfants 0-n définissant chaque menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>menu </p> </td> 
   <td colname="col2"> <p>menus </p> </td> 
   <td colname="col3"> <p>Instance unique d'un menu (correspond à un menu défini dans <span class="uicontrol"> Conception </span> &gt; <span class="uicontrol"> Navigation </span> &gt; <span class="uicontrol"> Menus </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>menu </p> </td> 
   <td colname="col3"> <p>Nom du menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>élément </p> </td> 
   <td colname="col2"> <p>menu </p> </td> 
   <td colname="col3"> <p>Définit chaque élément du menu. L'attribut facultatif sélectionné est défini sur true si l'élément de menu donné est actuellement sélectionné. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>libellé </p> </td> 
   <td colname="col2"> <p>élément </p> </td> 
   <td colname="col3"> <p>Texte orienté client de l’élément de menu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>value </p> </td> 
   <td colname="col2"> <p>élément </p> </td> 
   <td colname="col3"> <p>Représente la valeur de l'élément de menu (la valeur du paramètre de requête définie pour le menu). Cette balise n’est pas nécessaire si la valeur &lt;link&gt; est utilisée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>élément </p> </td> 
   <td colname="col3"> <p>Pour les options non sélectionnées, le paramètre &lt;link&gt; contient le lien relatif qui renvoie le même jeu de résultats, mais avec l'option de menu appliquée. Ce champ est vide pour l’option de tri actuellement sélectionnée. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Pagination {#section_E52F81C6A6EB4B8F996157B657EC540F}

Les jeux de résultats sont répartis sur plusieurs pages. En règle générale, les clients affichent 10 à 20 résultats sur une seule page. Les résultats suivants s’affichent sur la page suivante. Le code XML de pagination vous permet de créer un ensemble de liens de navigation afin que vos clients puissent parcourir les jeux de résultats page par page. Il existe quatre liens de navigation disponibles : premier, dernier, suivant et précédent. Chaque type de lien permet aux clients de parcourir rapidement les pages afin de pouvoir examiner et affiner facilement ce qu&#39;ils recherchent.

L&#39;exemple suivant montre la pagination d&#39;une recherche qui se trouve sur la première page et dont la pagination est configurée pour afficher les liens renvoyant à cinq pages.

Exemple de pagination :

```xml
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
            <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
        </pages> 
    </pagination> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>pagination </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p> Nombre total de pages de résultats, en fonction du nombre de résultats divisé par le nombre de résultats par page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nombre total de pages </p> </td> 
   <td colname="col2"> <p>pagination </p> </td> 
   <td colname="col3"> <p>Nombre total de pages sur lesquelles les résultats de la recherche sont répartis. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>pages spécifiques </p> </td> 
   <td colname="col2"> <p>pagination </p> </td> 
   <td colname="col3"> <p>Contient des noeuds de page 0 n définissant chaque page de la pagination. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>page </p> </td> 
   <td colname="col2"> <p>pages spécifiques </p> </td> 
   <td colname="col3"> <p>Il existe quatre noeuds de page spéciaux : premièrement, dernier, précédent et suivant. Ces quatre pages sont facultatives et apparaissent dans le jeu de résultats uniquement si elles ont du sens. Par exemple, si vous êtes à la page 1, il n’existe aucun lien "précédent". Toutes les autres pages indiquent une position. Le nombre de pages répertoriées dépend du "nombre de liens vers les pages" configuré dans l’interface utilisateur de pagination. L’attribut "sélectionné" indique la page sur laquelle se trouve actuellement le client. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requête {#section_3DAA1013F09742869B80F6A361816E6C}

Exemple de noeud de requête :

```xml
    <query> 
        <user-query><![CDATA[mens]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[265]]></total-results> 
    </query> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>query </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p> Noeud global qui fournit un aperçu de la requête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>requête utilisateur </p> </td> 
   <td colname="col2"> <p>requête </p> </td> 
   <td colname="col3"> <p> Mot-clé recherché. Si <span class="uicontrol"> Voulez-vous dire </span> a automatiquement recherché un terme suggéré en raison du terme d'origine qui n'a donné aucun résultat, il est reflété dans le nouveau mot-clé recherché (voir le noeud suggestions pour obtenir le mot-clé d'origine). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>résultats inférieurs </p> </td> 
   <td colname="col2"> <p>requête </p> </td> 
   <td colname="col3"> <p> Numéro de l'article du premier résultat sur cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>résultats supérieurs </p> </td> 
   <td colname="col2"> <p>requête </p> </td> 
   <td colname="col3"> <p> Numéro de l'article du dernier résultat sur cette page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>total-results </p> </td> 
   <td colname="col2"> <p>requête </p> </td> 
   <td colname="col3"> <p> Nombre total de résultats correspondant à la requête utilisateur. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Recherches récentes {#section_17F942F6EC07456DABED7A483AC08446}

Les recherches récentes sont une fonctionnalité basée sur des cookies qui ne fonctionne que si vous transmettez les informations des cookies aux serveurs de recherche/marchandisage de site.

Exemple de recherches récentes :

```xml
    <recent-searches> 
        <clear-link><![?q=womens&gscr=clear]]></clear-link> 
        <recent-search> 
            <link><![?q=mens]]></link> 
            <label><![CDATA[mens]]></label> 
        <recent-search> 
    </recent-searches> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Recherches récentes </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Le noeud n’est présent que si la recherche comporte des recherches récentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>lien clair </p> </td> 
   <td colname="col2"> <p>Recherches récentes </p> </td> 
   <td colname="col3"> <p>Chemin relatif qui efface toutes les recherches récentes du client. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>recherche récente </p> </td> 
   <td colname="col2"> <p>Recherches récentes </p> </td> 
   <td colname="col3"> <p>Définit les recherches récentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>recherche récente </p> </td> 
   <td colname="col3"> <p>Chemin d’accès permettant de créer un lien qui effectue une recherche récemment effectuée par l’utilisateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>libellé </p> </td> 
   <td colname="col2"> <p>recherche récente </p> </td> 
   <td colname="col3"> <p>Libellé d’affichage destiné au client pour la recherche récente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Résultats {#section_155A80B8C4F641678DD9C8F257108412}

Le jeu de résultats est une zone personnalisable de la réponse XML. Chaque index est unique dans les mécanismes de nommage des champs des métadonnées. Des champs communs sont renvoyés pour chaque résultat, tels que le titre, la description et l’URL. Cependant, toutes les métadonnées définies pour une page de l’index peuvent être disponibles pour être utilisées dans chaque noeud de résultats. La catégorisation, les prix, les couleurs et les vignettes ne sont que quelques-unes des options que vous pouvez appliquer à un résultat pour obtenir des résultats de recherche plus convaincants.

Le format des résultats est personnalisé en fonction des métadonnées propres à votre implémentation. Toutes les données par résultat à afficher dans les résultats, y compris les URL des images miniatures, sont contenues ici.

En outre, il est possible de configurer plusieurs zones de résultats dans la page, telles que &quot;Résultats présentés&quot;, ou de séparer les sections &quot;Produits&quot; et &quot;Contenu&quot; des résultats. Dans ce cas, plusieurs zones de résultats sont fournies dans le code HTML, bien que les facettes ne soient associées qu’au jeu de résultats Principal.

Exemple de noeud de résultats :

```xml
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
                    <field name="sku"><![CDATA[200190]]></field> 
                    <field name="pagename"><![CDATA[Relaxed Paint Splattered]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>   
         <result> 
                    <field name="index"><![CDATA[2]]></field> 
                    <field name="sku"><![CDATA[200195]]></field> 
                    <field name="pagename"><![CDATA[Tumbled Jeans]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[235]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>    
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
                    <field name="sku"><![CDATA[200196]]></field> 
                    <field name="pagename"><![CDATA[Montana Relaxed]]></field> 
 
                    <field name="img_sm_url"><![CDATA[https://geometrixx.com/images/08_geometrixx_icon_men.jpg]]></field> 
      <field name="brand"><![CDATA[Armora Jeans]]></field> 
      <field name="price"><![CDATA[220]]></field> 
      <field name="foundIn"><![CDATA[Mens,  
            Apparel,  
          Denim]]></field> 
         </result>         
        </result-set>   
    </results> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>résultats </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Noeud de conteneur pour les jeux de résultats 0-n. Les jeux de résultats zéro signifient que vous êtes sur un landing page spécial sans résultat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>jeu de résultats </p> </td> 
   <td colname="col2"> <p>résultats </p> </td> 
   <td colname="col3"> <p>Une recherche entrante peut déclencher plusieurs recherches. Chaque jeu de résultats contient les résultats d’une recherche nommée spécifique qui a été effectuée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>jeu de résultats </p> </td> 
   <td colname="col3"> <p>Nom de la recherche à laquelle appartient le jeu de résultats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>résultat </p> </td> 
   <td colname="col2"> <p>jeu de résultats </p> </td> 
   <td colname="col3"> <p>Contient tous les champs associés à un résultat individuel pour le jeu de résultats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>field </p> </td> 
   <td colname="col2"> <p>résultat </p> </td> 
   <td colname="col3"> <p>L’attribut name définit le nom du champ de l’index affiché. La valeur est la valeur réelle de ce champ. Certains résultats peuvent comporter des champs manquants qui ne sont pas pertinents pour ce résultat individuel. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Formulaire de recherche {#section_9E4B99D4FEDC49629F6C7E866F3A7493}

Le formulaire de recherche est inclus dans le jeu de résultats pour permettre aux clients de créer leur formulaire de recherche de manière dynamique. Cette étape est facultative. La plupart des clients ont un formulaire de recherche fixe. Cependant, il permet aux clients de déterminer si le formulaire de recherche a besoin d’une mbox Test&amp;Cible, en fonction d’au moins une règle de fonctionnement qui effectue un test A:B. De même, il permet aux clients de récupérer automatiquement la dernière saisie automatique de CSS et de JavaScript.

Exemple de formulaire de recherche XML :

```xml
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>search-form </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Contient les données permettant de générer le formulaire de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>include-tnt-mbox </p> </td> 
   <td colname="col2"> <p> search-form </p> </td> 
   <td colname="col3"> <p>Techniquement, vous n’avez besoin d’une mbox dans le formulaire de recherche que si au moins une règle métier effectue un test Test&amp;Cible A:B. Ce noeud indique si vous avez besoin d’une mbox ou si vous ne pouvez pas réduire le nombre d’accès sur les serveurs Test&amp;Cible. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>saisie automatique </p> </td> 
   <td colname="col2"> <p>search-form </p> </td> 
   <td colname="col3"> <p>Met en place le noeud enfant associé à la saisie semi-automatique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>enabled </p> </td> 
   <td colname="col2"> <p>saisie automatique </p> </td> 
   <td colname="col3"> <p>Définissez cette valeur sur 1 lorsque le compte de recherche utilise la saisie semi-automatique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>css </p> </td> 
   <td colname="col2"> <p> saisie automatique </p> </td> 
   <td colname="col3"> <p> CSS pour la saisie automatique. Placez ce noeud aussi haut que possible sur la page. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> form-content </p> </td> 
   <td colname="col2"> <p>saisie automatique </p> </td> 
   <td colname="col3"> <p>Contenu injecté dans le formulaire de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>javascript </p> </td> 
   <td colname="col2"> <p>saisie automatique </p> </td> 
   <td colname="col3"> <p>JavaScript pour la saisie automatique. Placez ce noeud aussi bas que possible sur la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Suggestions {#section_2899FACB9AD84F60B3687C1B4EF09E15}

Les clients peuvent configurer la fonctionnalité **[!UICONTROL Did You Mean]** de trois manières : faites des suggestions en raison de l&#39;absence de résultats, recherchez automatiquement la première suggestion lorsque nous n&#39;avons pas de résultats, ou faites des suggestions en raison de résultats faibles (lorsque les suggestions ont un nombre de résultats plus élevé). Toutes les suggestions donnent des résultats.

Ce noeud de suggestions contient les termes qui génèrent des requêtes réussies. Le lien est également renvoyé afin qu’un client puisse accéder à la nouvelle requête.

Exemple de résultat pour une suggestion en raison de 0 résultat :

```xml
    <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>0</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=arcade;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[arcade]]></word> 
 </suggestion-item>    
    </suggestions>
```

Exemple de sortie pour une recherche automatique par rapport à une suggestion :

```xml
    <suggestions> 
        <auto-searched>1</auto-searched> 
        <orig-query><![CDATA[arcace]]></orig-query> 
        <suggestions-low-results>0</suggestions-low-results>         
    </suggestions> 
```

Exemple de résultat pour une suggestion en raison de résultats faibles :

```xml
   <suggestions> 
        <auto-searched>0</auto-searched> 
        <suggestions-low-results>1</suggestions-low-results> 
 <suggestion-item> 
     <link><![CDATA[?i=1;q=coffee;sp_cs=UTF-8;view=xml]]></link> 
     <word><![CDATA[coffee]]></word> 
 </suggestion-item>  
    </suggestions> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>suggestion </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p> Contient des noeuds enfants qui définissent la suggestion, le cas échéant. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>recherche automatique </p> </td> 
   <td colname="col2"> <p>suggestions </p> </td> 
   <td colname="col3"> <p> S’il est présent, indique si la recherche/marchandisage sur le site a automatiquement effectué une recherche sur un nouveau terme en raison de l’absence de résultats. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>orig-requête </p> </td> 
   <td colname="col2"> <p>suggestions </p> </td> 
   <td colname="col3"> <p> Lorsque la recherche/marchandisage sur le site effectue automatiquement des recherches par rapport à la première suggestion, la requête utilisateur dans le noeud de requête affiche le mot-clé recherché. Ce noeud affiche le terme de requête d’origine. La combinaison des deux permet aux clients de créer des structures telles que "Recherche d’arcade au lieu d’arcade". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>suggestions-résultats faibles </p> </td> 
   <td colname="col2"> <p>suggestions </p> </td> 
   <td colname="col3"> <p>S’il est présent, indique si la recherche/le marchandisage du site fait des suggestions en raison du terme de recherche actuel produisant de faibles résultats et une suggestion produisant des résultats considérablement plus élevés. Les deux seuils sont configurables dans <span class="uicontrol"> Voulez-vous dire </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>suggestion-élément </p> </td> 
   <td colname="col2"> <p>suggestions </p> </td> 
   <td colname="col3"> <p>Contient des noeuds 0-n indiquant les différentes suggestions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>link </p> </td> 
   <td colname="col2"> <p>suggestion-élément </p> </td> 
   <td colname="col3"> <p>Contient le chemin de création d’un lien vers le terme suggéré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>word </p> </td> 
   <td colname="col2"> <p>suggestion-élément </p> </td> 
   <td colname="col3"> <p> Contient le mot suggéré. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Modèle {#section_1E2BB2F274B04F5491A4CCCC38F507BD}

La possibilité de changer une expérience de recherche de clients en fonction des résultats est prise en charge. Cela implique en partie de basculer entre différents modèles avec une disposition différente des résultats de recherche. Par exemple, vous pouvez avoir un modèle avec une grille de vue de produits pour quand vous avez beaucoup de produits. Vous pouvez également utiliser un modèle de &quot;projecteur&quot; lors de l’affichage d’un seul résultat contenant plus de détails. Vous pouvez également avoir un modèle &quot;aucun résultat&quot; lorsqu’une recherche ne donne aucun résultat. Le noeud de modèle indique quel modèle est utilisé pour afficher les résultats de la recherche.

Exemple de modèle :

```xml
<template><![CDATA[grid]]></template>
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>le modèle </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Indique le nom du modèle utilisé pour afficher les résultats de la recherche. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Zones {#section_26C4A947E7B1474A8E37D86D9579B93E}

Les zones sont des sections des pages qui peuvent être activées ou désactivées par les règles de fonctionnement. Une zone peut contenir tout contenu, y compris, mais sans s’y limiter, les facettes, les recherches, les chemins de navigation, le contenu statique. Les zones de la page Web des clients doivent correspondre aux mêmes zones que la recherche/le marchandisage du site.

Exemple de noeuds de zone :

```xml
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Noeud </p> </th> 
   <th colname="col2" class="entry"> <p>Noeud parent </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>zones </p> </td> 
   <td colname="col2"> <p>client-results </p> </td> 
   <td colname="col3"> <p>Contient des zones 0-n. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>zone </p> </td> 
   <td colname="col2"> <p>zones </p> </td> 
   <td colname="col3"> <p> Noeud de zone individuel. Vous pouvez avoir plusieurs noeuds de zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>name </p> </td> 
   <td colname="col2"> <p>zone </p> </td> 
   <td colname="col3"> <p>Nom de la zone. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>affichage </p> </td> 
   <td colname="col2"> <p>1 ou 0, indiquant si la zone correspondant au nom de la zone est affichée ou masquée. </p> </td> 
   <td colname="col3"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemples {#reference_64B7D8D228AF4B8D90EDF4DE507B0F84}

Exemple de sortie pour une recherche * sur un site Web fictif appelé Geometrixx et exemple de modèle de présentation utilisé pour produire l’exemple de sortie.

* [Exemple de sortie](../c-appendices/c-guidedsearchoutput.md#section_515C000A18B847D59097D0A9CCC02636)
* [Exemple de modèle de présentation](../c-appendices/c-guidedsearchoutput.md#section_AD42571DFB88491AA7F0FDF0929EBE97)

## Exemple de sortie {#section_515C000A18B847D59097D0A9CCC02636}

Exemple de sortie pour une recherche * sur un site Web fictif appelé Geometrixx.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[*]]></user-query> 
 <lower-results><![CDATA[1]]></lower-results> 
 <upper-results><![CDATA[12]]></upper-results> 
 <total-results><![CDATA[1337]]></total-results> 
    </query> 
 
    <custom-fields> 
 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name>

             <item selected="true"> 
 
          <label><![CDATA[Relevance]]></label> 
          <value><![CDATA[relevance]]></value> 
          <link><![CDATA[ ]]></link> 
             </item>

             <item> 
          <label><![CDATA[Lowest Price]]></label> 
          <value><![CDATA[Price]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Highest Price]]></label> 
          <value><![CDATA[Price_r]]></value> 
          <link><![CDATA[?i=1;q=*;sort=Price_r;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

             <item> 
          <label><![CDATA[Brand]]></label> 
          <value><![CDATA[brand]]></value> 
          <link><![CDATA[?i=1;q=*;sort=brand;sp_cs=UTF-8;sp_staged=1;view=xml]]></link>     
             </item>

        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name>

                    <label><![CDATA[WOMEN'S]]></label> 
      <value><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Womens;sp_sfvl_field=levelii|leveli|brand|leveliii;x=0;x1=leveli;y=0;view=nav;top=1;i=1;m_ss_head_nav=WOMEN'S]]></link>

                    <label><![CDATA[MEN'S]]></label> 
      <value><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></value> 
      <link><![CDATA[/q1/Mens/x1/leveli/view/nav/top/1/]]></link>

                    <label><![CDATA[JEWELRY & ACCESSORIES]]></label> 
      <value><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1]]></value> 
      <link><![CDATA[?q1=Jewelry+%26+Accessories&sp_sfvl_field=levelii|leveli|brand|leveliii&x1=leveli&view=nav&top=1;i=1;m_ss_head_nav=JEWELRY+%26+ACCESSORIES]]></link>

                    <label><![CDATA[BEAUTY & FRAGRANCE]]></label> 
      <value><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Beauty+%26+Fragrance;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=BEAUTY+%26+FRAGRANCE]]></link>

                    <label><![CDATA[GIFTS & HOME]]></label> 
      <value><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Gifts+%26+Home;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=GIFTS+%26+HOME]]></link>

                    <label><![CDATA[CHILDREN & TOYS]]></label> 
      <value><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Children+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=CHILDREN+%26+TOYS]]></link>

                    <label><![CDATA[ELECTRONICS]]></label> 
      <value><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1]]></value> 
      <link><![CDATA[?q1=Electronics+%26+Toys;sp_sfvl_field=levelii|leveli|brand|leveliii;x1=leveli;view=nav;top=1;i=1;m_ss_head_nav=ELECTRONICS]]></link>

        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
       
  <breadcrumb-item> 
    <link><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></link> 
    <value><![CDATA[*]]></value> 
                        <label><![CDATA[]]></label> 
   </breadcrumb-item> 
          
   </breadcrumb> 
 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched>0</auto-searched> 
         
        <suggestions-low-results>0</suggestions-low-results> 
         
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[112]]></total-pages> 
 
        <pages> 
     <page position="first"><![CDATA[]]></page> 
     <page position="last"><![CDATA[?i=1;page=112;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page> 
      
     <page position="next"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="1" selected="true"><![CDATA[?i=1;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="2"><![CDATA[?i=1;page=2;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="3"><![CDATA[?i=1;page=3;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="4"><![CDATA[?i=1;page=4;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

                <page position="5"><![CDATA[?i=1;page=5;q=*;sp_cs=UTF-8;sp_staged=1;view=xml]]></page>

        </pages> 
    </pagination> 
 
    <facets>  
         
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected>0</selected>

      <facet-value> 
           
              <label><![CDATA[Womens]]></label> 
 
       <link><![CDATA[?i=1;q=*;q1=Womens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[219]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Mens]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Mens;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[202]]></count> 
                         
      </facet-value> 
   
      <facet-value>

              <label><![CDATA[Beauty &amp; Fragrance]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Beauty+%26+Fragrance;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[169]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Children &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Children+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[209]]></count> 
                         
      </facet-value>

      <facet-value> 
           
              <label><![CDATA[Electronics &amp; Toys]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Electronics+%26+Toys;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[200]]></count> 
                         
      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Gifts &amp; Home]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Gifts+%26+Home;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[156]]></count>

      </facet-value> 
   
      <facet-value> 
           
              <label><![CDATA[Jewelry &amp; Accessories]]></label> 
       <link><![CDATA[?i=1;q=*;q1=Jewelry+%26+Accessories;sp_cs=UTF-8;sp_staged=1;view=xml;x1=leveli]]></link> 
       <count><![CDATA[182]]></count> 
                         
      </facet-value> 
   
      </facet-item> 
  
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
               
         <result> 
                    <field name="index"><![CDATA[1]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[2]]></field> 
      <field name="brand"><![CDATA[One For All]]></field> 
      <field name="price"><![CDATA[145]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[3]]></field> 
      <field name="brand"><![CDATA[Citizens]]></field> 
      <field name="price"><![CDATA[208]]></field> 
 
      <field name="foundIn"><![CDATA[Womens,  
            Apparel,  
          Denim]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[4]]></field> 
      <field name="brand"><![CDATA[Vera Watson]]></field> 
      <field name="price"><![CDATA[850]]></field> 
      <field name="foundIn"><![CDATA[Womens,  
            Dresses,  
          Day]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[5]]></field> 
 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[195]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[6]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[80]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[7]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[85]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[8]]></field> 
      <field name="brand"><![CDATA[Woolberry]]></field> 
 
      <field name="price"><![CDATA[280]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[9]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[149]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
 
                    <field name="index"><![CDATA[10]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[55]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[11]]></field> 
      <field name="brand"><![CDATA[Petrol]]></field> 
      <field name="price"><![CDATA[45]]></field> 
 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
        
         <result> 
                    <field name="index"><![CDATA[12]]></field> 
      <field name="brand"><![CDATA[Ray Laredo]]></field> 
      <field name="price"><![CDATA[47]]></field> 
      <field name="foundIn"><![CDATA[Children &amp; Toys,  
            Apparel,  
          Boys Toddler (2T-4T)]]></field> 
         </result>   
      
        </result-set>   
    </results>

    <banners> 
         
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<div style="color:#70A100">We have custom shipping</div>]]></content> 
            </banner>

    </banners> 
 
    <zones> 
        <zone> 
 
            <name><![CDATA[brand-facet]]></name> 
            <display>1</display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox>1</include-tnt-mbox> 
        <autocomplete> 
 
            <enabled>1</enabled> 
            <css><![CDATA[<link rel="stylesheet" type="text/css" href="https://content.t1.atomz.com/sp10043554/stage/autocomplete_styles.css?sp_js_param=2" /> 
]]></css> 
            <form-content><![CDATA[<div id="autocomplete"></div> 
<input type="hidden" name="sp_staged" id="sp_staged" value="1" /> 
]]></form-content> 
            <javascript><![CDATA[<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/utilities/utilities.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/datasource/datasource-min.js"></script> 
<script type="text/javascript" src="https://ajax.googleapis.com/ajax/libs/yui/2.6.0/build/autocomplete/autocomplete-min.js"></script> 
<script type="text/javascript" src="https://content.t1.atomz.com/sp10043554/stage/autocomplete_data.js?sp_js_param=3"></script>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

## Exemple de modèle de présentation {#section_AD42571DFB88491AA7F0FDF0929EBE97}

Voici un exemple de modèle de présentation utilisé pour produire l’exemple de sortie ci-dessus.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?> 
<customer-results> 
    <query> 
        <user-query><![CDATA[<guided-query-param gsname="q" />]]></user-query> 
 <lower-results><![CDATA[<guided-results-lower>]]></lower-results> 
 <upper-results><![CDATA[<guided-results-upper>]]></upper-results> 
 <total-results><![CDATA[<guided-results-total>]]></total-results> 
    </query> 
 
    <custom-fields> 
        <custom-field name="seo-search-title"><![CDATA[Geometrixx Search Results]]></custom-field> 
        <custom-field name="seo-search-keywords"><![CDATA[<guided-general-field gsname="default" field="seo_search_keywords"/>]]></custom-field> 
    </custom-fields> 
 
    <menus> 
 
        <menu> 
           <name>sort</name> 
     <guided-menu gsname="sort"> 
         <guided-if-menu-item-selected> 
             <item selected="true"> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[ ]]></link> 
             </item> 
        <guided-else-menu-item-selected> 
             <item> 
          <label><![CDATA[<guided-menu-item-label />]]></label> 
          <value><![CDATA[<guided-menu-item-value />]]></value> 
          <link><![CDATA[<guided-menu-item-path />]]></link>     
             </item> 
        </guided-if-menu-item-selected> 
    </guided-menu> 
        </menu> 
        <menu> 
            <name><![CDATA[ss_head_nav]]></name> 
            <guided-menu gsname="ss_head_nav"> 
                <guided-if-menu-item-selected> 
                    <item selected="true"> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                <guided-else-menu-item-selected> 
                    <label><![CDATA[<guided-menu-item-label />]]></label> 
      <value><![CDATA[<guided-menu-item-value />]]></value> 
      <link><![CDATA[<guided-menu-item-path />]]></link> 
                </guided-if-menu-item-selected> 
            </guided-menu>  
        </menu> 
    </menus> 
 
    <breadcrumbs> 
  <breadcrumb> 
            <name><![CDATA[default]]></name> 
      <guided-breadcrumb gsname="default"> 
  <breadcrumb-item> 
    <link><![CDATA[<guided-breadcrumb-path gsname="goto">]]></link> 
    <value><![CDATA[<guided-breadcrumb-value />]]></value> 
                        <label><![CDATA[<guided-breadcrumb-label>]]></label> 
   </breadcrumb-item> 
         </guided-breadcrumb> 
   </breadcrumb> 
    </breadcrumbs> 
 
    <suggestions> 
        <auto-searched><guided-if-suggestion-autosearch>1<guided-else-suggestion-autosearch>0</guided-if-suggestion-autosearch></auto-searched> 
        <guided-if-suggestion-autosearch><orig-query><![CDATA[<guided-suggestion-original-query/>]]></orig-query></guided-if-suggestion-autosearch> 
        <suggestions-low-results><guided-if-suggestion-low-results>1<guided-else-suggestion-low-results>0</guided-if-suggestion-low-results></suggestions-low-results> 
        <guided-suggestions> 
     <suggestion-item> 
         <link><![CDATA[<guided-suggestion-path />]]></link> 
  <word><![CDATA[<guided-suggestion />]]></word> 
     </suggestion-item> 
 </guided-suggestions> 
    </suggestions> 
 
    <pagination> 
        <total-pages><![CDATA[<guided-page-total />]]></total-pages> 
        <pages> 
     <page position="first"><![CDATA[<guided-page-path gsname="first" />]]></page> 
     <page position="last"><![CDATA[<guided-page-path gsname="last" />]]></page> 
     <guided-if-page-prev><page position="prev"><![CDATA[<guided-page-path gsname="prev" />]]></page></guided-if-page-prev> 
     <guided-if-page-next><page position="next"><![CDATA[<guided-page-path gsname="next" />]]></page></guided-if-page-next> 
     <guided-if-page-viewall><page position="viewall"><![CDATA[<guided-page-path gsname="viewall" />]]></page></guided-if-page-viewall> 
     <guided-if-page-viewpages><page position="viewall"><![CDATA[<guided-page-path gsname="viewpages" />]]></page></guided-if-page-viewpages> 
 
     <guided-pages> 
                <guided-if-page-selected><page position="<guided-page-number />" selected="true"><![CDATA[<guided-page-path />]]></page> 
  <guided-else-page-selected><page position="<guided-page-number />"><![CDATA[<guided-page-path />]]></page> 
  </guided-if-page-selected> 
     </guided-pages> 
        </pages> 
    </pagination> 
 
    <facets>  
        <guided-facet gsname="leveli"> 
     <facet-item> 
         <facet-title><![CDATA[Department]]></facet-title> 
                <selected><guided-if-facet-selected>1<guided-else-facet-selected>0</guided-if-facet-selected></selected> 
                <guided-if-facet-selected><undo-link><![CDATA[<guided-facet-undo-path gsname="leveli">]]></undo-link></guided-if-facet-selected> 
  <guided-facet-values> 
      <facet-value> 
          <guided-if-facet-value-selected><selected><![CDATA[true]]></selected></guided-if-facet-value-selected> 
              <label><![CDATA[<guided-facet-value>]]></label> 
       <link><![CDATA[<guided-facet-value-path />]]></link> 
       <count><![CDATA[<guided-facet-count>]]></count> 
                        <guided-if-facet-value-selected><undolink><![CDATA[<guided-facet-value-undo-path />]]></undolink></guided-if-facet-value-selected> 
      </facet-value> 
  </guided-facet-values> 
      </facet-item> 
 </guided-facet> 
    </facets> 
 
    <results> 
        <result-set> 
            <name><![CDATA[default]]></name> 
            <guided-results gsname="default">   
         <result> 
                    <field name="index"><![CDATA[<guided-result-index />]]></field> 
      <field name="brand"><![CDATA[<guided-result-field gsname="brand" />]]></field> 
      <field name="price"><![CDATA[<guided-result-field gsname="price" />]]></field> 
      <field name="foundIn"><![CDATA[<guided-if-result-field gsname="leveli"><!--tmpl_var name='leveli'-->, </guided-if-result-field> 
            <guided-if-result-field gsname="levelii"><!--tmpl_var name='levelii'-->, </guided-if-result-field> 
          <guided-if-result-field gsname="leveliii"><!--tmpl_var name='leveliii'--></guided-if-result-field>]]></field> 
         </result>   
     </guided-results> 
        </result-set>   
    </results> 
 
    <guided-if-recent-searches> 
    <recent-searches> 
        <clear-link><guided-recent-searches-clear-path/></clear-link> 
        <guided-recent-searches> 
            <recent-search> 
                <link><guided-recent-searches-path></link> 
                <label><guided-recent-searches-value></label> 
            <recent-search> 
        </guided-recent-searches> 
    </recent-searches> 
    </guided-if-recent-searches> 
 
    <banners> 
        <guided-if-banner-set gsname="top"> 
            <banner> 
                <area><![CDATA[top]]></area> 
                <content><![CDATA[<guided-banner gsname="top">]]></content> 
            </banner> 
        </guided-if-banner-set> 
        <guided-if-banner-set gsname="bottom"> 
            <banner> 
                <area><![CDATA[bottom]]></area> 
                <content><![CDATA[<guided-banner gsname="bottom">]]></content> 
            </banner> 
        </guided-if-banner-set> 
    </banners> 
 
    <zones> 
        <zone> 
            <name><![CDATA[brand-facet]]></name> 
            <display><guided-if-zone gsname="brand-facet">1<guided-else-zone>0</guided-if-zone></display> 
        </zone> 
    </zones> 
 
    <search-form> 
        <include-tnt-mbox><guided-if-tnt-business-rules>1<guided-else-tnt-business-rules>0</guided-if-tnt-business-rules></include-tnt-mbox> 
        <autocomplete> 
            <enabled><guided-if-autocomplete>1<guided-else-autocomplete>0</guided-if-autocomplete></enabled> 
            <css><![CDATA[<guided-ac-css/>]]></css> 
            <form-content><![CDATA[<guided-ac-form-content/>]]></form-content> 
            <javascript><![CDATA[<guided-ac-javascript/>]]></javascript> 
        </autocomplete> 
    </search-form> 
 
</customer-results> 
```

