---
description: Vous pouvez utiliser des modèles pour gérer vos modèles de présentation et les modèles de transport.
seo-description: Vous pouvez utiliser des modèles pour gérer vos modèles de présentation et les modèles de transport.
seo-title: A propos des modèles
solution: Target
title: A propos des modèles
topic: Design,Site search and merchandising
uuid: f5805d3e-43bf-4e13-95df-b6bd6b762d11
translation-type: tm+mt
source-git-commit: 60cedaac1846e384a37699a42bf7fda33828e1c0

---


# A propos des modèles{#about-templates}

Vous pouvez utiliser **[!UICONTROL Templates]** pour gérer vos modèles de présentation et les modèles de transport.

## A propos des modèles {#concept_06EB481B14864E18A8AE2BCD1D6EF0B5}

<!-- 

c_about_templates.xml

 -->

Vous pouvez ajouter, modifier, copier, renommer ou supprimer des modèles de présentation et des modèles de transport. Lorsque vous cliquez sur un nom de modèle existant dans le tableau Modèles, il s’ouvre dans une fenêtre de l’éditeur (ou du lecteur) où vous pouvez apporter vos modifications.

Vous pouvez annuler les modifications apportées aux modèles à l’aide de la fonction Historique dans la liste déroulante des noms de modèle du tableau Modèles.

Vous pouvez réduire le poids de page d’un modèle de présentation en cochant la **[!UICONTROL Minimize]** case correspondante du modèle dans le tableau du modèle. En réduisant le poids de page du modèle, vous réduisez dynamiquement le code JavaScript intégré et le code CSS. Vous supprimez également les espaces blancs redondants dans le code HTML. La réduction du poids de la page du modèle de présentation peut vous aider à obtenir plus rapidement les résultats de votre recherche.

Vous pouvez prévisualiser l’aspect du modèle réduit en cliquant dans la liste déroulante en regard du nom de fichier, puis en cliquant sur **[!UICONTROL Preview minimized]**. Si vous réduisez le modèle de présentation principal, n’oubliez pas d’activer la réduction pour les modèles inclus (avec `guided-include` balise) car cette option n’est pas héritable.

Même si vous réduisez un modèle de présentation, vous pouvez toujours modifier la version &quot;non minimisée&quot; du même modèle.

Vous pouvez utiliser les règles de pré-recherche, les règles de post-recherche et les règles de fonctionnement pour déterminer quand utiliser l’un de vos autres modèles de présentation. Il est courant d’avoir une règle telle que &quot;Pour chaque recherche, définissez le modèle ciblé sur xxxx&quot;. Une telle règle étant en place, lorsque vous modifiez le modèle &quot;Par défaut&quot; dans le tableau Modèles, il semble n’avoir aucun effet.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## A propos des modèles de présentation {#section_ACDDEA5C499E481C828A517C230D4596}

Les modèles de présentation sont des modèles HTML visibles par un client lorsqu’il consulte les résultats de sa recherche sur votre site Web.

Dans la couche de présentation, vous pouvez disposer d’un modèle de présentation unique qui présente les résultats de plusieurs recherches provenant de différentes sources. Vous pouvez définir autant de modèles de présentation que vous le souhaitez et même définir des modèles de présentation partagés par d’autres modèles à l’aide de `include` commandes. Le modèle de présentation permet à tous les composants de conception, tels que les facettes, les menus et les chemins de navigation, de se réunir. Pour afficher les différents composants de conception, vous devez utiliser les balises de modèle de présentation.

Voir Balises de modèle de [présentation](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Lorsque vous disposez de plusieurs modèles de présentation, vous définissez dans quelles conditions les différents modèles de présentation sont utilisés. Vous pouvez sélectionner le modèle de présentation à utiliser en fonction des paramètres CGI entrants et des cookies. Vous pouvez également changer le modèle de présentation que vous utilisez en fonction du résultat d’une recherche précédente.

Lorsque vous utilisez plusieurs modèles de présentation, assurez-vous d’indiquer le modèle que vous souhaitez que les résultats de la recherche apparaissent au départ. Pour ce faire, utilisez la **[!UICONTROL Default]** colonne du tableau Modèles.

## A propos des modèles de transport {#section_35FD3E8AAA4E4695A737DB7E00C3258B}

Les modèles de transport peuvent être des modèles XML ou JSON qui transmettent des données de la recherche principale à la couche de présentation de la recherche guidée.

Par défaut, votre compte est configuré pour utiliser des modèles de transport XML. Toutefois, si vous préférez utiliser JSON pour transmettre vos données à la recherche guidée, contactez le service de conseil d’Adobe qui peut vous aider.

Dans la couche de présentation, vous pouvez disposer d’un modèle de présentation unique qui présente les résultats de plusieurs recherches. Chaque recherche peut utiliser le même modèle de transport ou un modèle de transport personnalisé pour transmettre les données à la couche de présentation. Le modèle de transport étant uniquement utilisé pour transmettre des données à la couche de présentation, il ne doit pas comporter de code HTML utilisé pour afficher les résultats de la recherche. Le modèle utilise des balises de modèle de transport pour transmettre les résultats de la recherche et les résultats pour remplir les facettes. Dans ces balises, les balises de modèle de recherche standard sont utilisées pour afficher les valeurs réelles.

Voir [Rechercher des balises](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modèle.

**Balises spécifiques au modèle de transport XML**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Balise de modèle de transport XML </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;guided-xml&gt;&lt;/guided-xml&gt; </span> </p> </td> 
   <td colname="col2"> <p>Il s’agit des balises XML racine utilisées par la couche de présentation pour détecter ce qu’elle doit analyser à partir du modèle de transport. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;general&gt;&lt;/general&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ce jeu de balises entoure les balises de modèle de recherche qui fournissent des données de résumé basées sur le jeu de résultats. En règle générale, ces balises contiennent des balises de recherche pour le nombre total de résultats, le résultat le plus faible et le résultat le plus élevé. Vous pouvez définir un nombre illimité de champs globaux supplémentaires à l’aide de la balise <span class="codeph"> general-field </span> . </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;general&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;total&gt;&lt;search-total&nbsp;/&gt;&lt;/total&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;lower&gt;&lt;search-lower&nbsp;/&gt;&lt;/lower&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;upper&gt;&lt;search-upper&nbsp;/&gt;&lt;/upper&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;general-field&nbsp;name="my_custom_field"&gt;Some&nbsp;global&nbsp;content&lt;/general-field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/general&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;results&gt;&lt;/results&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises est entouré des résultats de la recherche, de sorte que la recherche guidée sache où les rechercher. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;result&gt;&lt;/result&gt; </span> </p> </td> 
   <td colname="col2"> <p>Ce jeu de balises est enveloppé autour de chaque résultat de recherche, de sorte que la recherche guidée identifie l’endroit où le contenu d’un seul résultat de recherche commence et se termine. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-cdata&gt;&lt;search-url&nbsp;length="500"&nbsp;/&gt;&lt;/search-cdata&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;attribute-table name="nom_table"&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cette balise vous permet de parcourir en boucle chaque élément d’une liste à plusieurs valeurs pour un seul résultat. N’utilisez la balise que dans un résultat. Son principal objectif est de vous permettre d’effectuer une itération sur les attributs appartenant à un champ de résultat. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;index&gt;&lt;search-index&nbsp;/&gt;&lt;/index&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;loc&gt;&lt;search-url&nbsp;/&gt;&lt;/loc&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;title&gt;&lt;search-title&nbsp;/&gt;&lt;/title&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;attribute-table&nbsp;name="downloads"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_title"&gt;&lt;search-display-field&nbsp;name="download_title"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;field&nbsp;name="download_link"&nbsp;delimiter="|"&gt;&lt;search-display-field&nbsp;name="download_link"&nbsp;/&gt;&lt;/field&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/attribute-table&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/result&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-results&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/results&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facettes&gt;&lt;/facettes&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises transmet les résultats qui renseignent les facettes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;facet name="name"&gt;&lt;/facet&gt; </span> </p> </td> 
   <td colname="col2"> <p>Chaque facette doit disposer de ses propres balises de facette pour lesquelles le paramètre name correspond au nom de la facette. Les balises de recherche sont utilisées dans les balises de facette pour les valeurs de facette. </p> <p>Voir <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" type="concept" format="dita" scope="local"> A propos des facettes </a>. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;facets&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="brand"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="brand"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;facet&nbsp;name="category"&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;values&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="values"&nbsp;sortby="values"&nbsp;/&gt;&lt;/values&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;counts&gt;&lt;search-field-value-list&nbsp;name="category"&nbsp;quotes="no"&nbsp;commas="yes"&nbsp;data="counts"&nbsp;sortby="values"&nbsp;/&gt;&lt;/counts&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/facet&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/facets&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestions&gt;&lt;/suggestions&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises encapsule vos suggestions Voulez-vous dire afin que la recherche guidée identifie les noeuds XML qui contiennent des suggestions. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> &lt;suggestion&gt;&lt;/suggestion&gt; </span> </p> </td> 
   <td colname="col2"> <p>Cet ensemble de balises encapsule chaque suggestion du message Voulez-vous dire. </p> <p> <b>Exemple</b> </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;&lt;search-if-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;value&gt;&lt;search-suggestion-text&nbsp;/&gt;&lt;/value&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;count&gt;&lt;search-suggestion-result-count&nbsp;/&gt;&lt;/count&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestion&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/suggestions&gt; 
      &nbsp;&nbsp;&nbsp;&nbsp;&lt;/search-if-suggestions&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Balises spécifiques au modèle de transport JSON**

La transmission de JSON par rapport au code XML à partir du moteur de recherche est connue pour être plus rapide car la charge utile est plus faible et l’analyseur plus rapide. Soyez toutefois prudent lorsque vous utilisez JSON pour vous assurer que la sortie est un fichier JSON strict, car l’analyseur n’est pas pardonnant.

Si vous découvrez JSON, vous pouvez utiliser les liens et exemples suivants pour vous aider à démarrer :

* Une introduction à JSON. Voir [https://www.json.org/](https://www.json.org/).
* Testez votre fichier JSON pour vous assurer qu’il est valide. Voir [https://jsonlint.com/](https://jsonlint.com/).

**Exemple de modèle JSON**

```
{ 
 "general": 
 { 
  "total" : "<search-total />", 
  "lower" : "<search-lower />", 
  "upper" : "<search-upper />", 
  "rbt-trigger-list" : "<search-rbta-trigger-id-list>", 
  "fields" :  
  [ 
   { 
    "name" : "seo_search_title", 
    "value" : "<search-include file="seo/seo_search_title.tpl" />" 
   }, 
   { 
    "name" : "seo_search_keywords", 
    "value" : "<search-include file="seo/seo_search_keywords.tpl" />" 
   } 
  ] 
 }, 
 
 <search-if-suggestions> 
 "suggestions": 
  [ 
  <search-suggestions> 
  { 
   "suggestion":"<search-suggestion-text />", 
   "count": "<search-suggestion-result-count>" 
  }<search-if-not-last-suggestion>,</search-if-not-last-suggestion> 
  </search-suggestions> 
 ], 
 </search-if-suggestions> 
 
 "facets" : 
 [ 
  { 
   "name" : "leveli", 
   "values" : [ <search-field-value-list name="leveli" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="leveli" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" :"levelii", 
   "values" : [<search-field-value-list name="levelii" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="levelii" quotes="no" sortby="values" data="results" />] 
  }, 
  { 
   "name" : "brand", 
   "values" : [<search-field-value-list name="brand" quotes="yes" sortby="values" data="values" encoding="json"/>], 
   "counts" : [<search-field-value-list name="brand" quotes="no" sortby="values" data="results" />] 
  }, 
 ], 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    }, 
    { 
     "name" : "title", 
     "value" : "<search-display-field name="title" encoding="json"/>" 
    }, 
    { 
     "name" : "img_url_thumbnail", 
     "value" : "<search-display-field name="img_url_thumbnail" encoding="json"/>" 
    }, 
    { 
     "name" : "description", 
     "value" : "<search-display-field name="description" encoding="json"/>" 
    }, 
    { 
     "name" : "mdi", 
     "value" : "<SEARCH-RBTA-DISPLAY-MDI-FIELD>" 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Exemple de section de résultat JSON avec un tableau d’attributs de résultats**

```
{ 
 "results" : 
 [ 
  <search-results> 
  { 
   "fields" : 
   [ 
    { 
     "name" : "index", 
     "value" : "<search-index />" 
    }, 
    { 
     "name" : "loc", 
     "value" : "<search-display-field name="url" length="500" encoding="json"/>" 
    } 
   ], 
   "tables" : 
   [ 
    { 
     "name" : "downloads", 
     "fields" : 
     [ 
      { 
       "name" : "download_title", 
       "value" : <search-display-field name="download_title" encoding="json"/> 
      }, 
      { 
       "name" : "download_link", 
       "value" : <search-display-field name="download_link" encoding="json"/> 
      } 
     ] 
    } 
   ] 
  }<search-if-not-last>,</search-if-not-last>  
  </search-results> 
 ] 
}
```

**Exemple de section Facette JSON pour une facette avec des champs associés**

```
{ 
 facets" : 
 [ 
  { 
   "name" : "t1", 
   "values" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
   "counts" : [<search-field-value-list name="t1" quotes="yes" commas="yes" data="results" sortby="values" />], 
   "custom-fields" : 
   [ 
    { 
     "name" : "taxonmyId", 
     "value" : [<search-field-value-list name="tax1" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />] 
    } 
   ] 
  } 
 ] 
}
```

**Exemple de section de facette JSON pour les facettes avec un graphique à secteurs**

```
{ 
  "facets" : 
  [  
   { 
    "name" : "fvalue0", 
                  "dynamic" : 1, 
                  "display-names" : [<search-field-value-list name="fname0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "values" : [<search-field-value-list name="fvalue0" quotes="yes" commas="yes" data="values" sortby="values" encoding="json" />], 
    "counts" : [<search-field-value-list name="fvalue0" quotes="no" commas="yes" data="results" sortby="values" />] 
   } 
  ] 
} 
```

## Ajout d’une nouvelle présentation ou d’un fichier de modèle de transport {#task_73199757B6E748CAA604902FF913F012}

Vous pouvez utiliser **[!UICONTROL Add Template]** pour ajouter des modèles de présentation (.tmpl) ou des modèles de transport (.tpl) à la [!DNL Templates] page.

<!-- 

t_adding_a_new_presentation_or_transport_template_file.xml

 -->

**Pour ajouter une nouvelle présentation ou un fichier de modèle de transport**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, cliquez sur **[!UICONTROL Add New Template]**.
1. Dans la [!DNL Add Template] boîte de dialogue, définissez les options de votre choix.

   <!-- 
   
   r_add_template_options.xml
   
   -->

   | Option | Description |
   |--- |--- |
   | Nouveau nom de fichier | Indique le nom du modèle à ajouter. L’extension de fichier appropriée est automatiquement ajoutée au nom du fichier, en fonction du type de modèle sélectionné.  Les modèles de présentation ont une extension de fichier .tmpl ; Les modèles de transport ont une extension de fichier .tpl. |
   | Nouveau type de modèle | Vous permet de choisir une présentation ou un modèle de transport à ajouter.  Voir [A propos des modèles](../c-about-design-menu/c-about-templates.md). |

   Voir aussi [Modification d’une présentation ou d’un modèle](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transport.
1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Sur la [!DNL Templates] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une présentation ou d’un modèle de transport {#task_800E0E2265C34C028C92FEB5A1243EC3}

Vous pouvez utiliser l’éditeur de modèles pour afficher et modifier le contenu de votre présentation et transporter les fichiers de modèles.

<!-- 

t_editing_a_template.xml

 -->

Vous pouvez modifier et tester votre présentation par étapes et les modèles de transport, tandis que les visiteurs de votre site Web continuent d’utiliser les versions en direct de vos modèles. Vous testez votre modèle d’évaluation à l’aide de la version intermédiaire de l’URL de votre domaine de recherche. Par exemple, vous pouvez tester votre modèle de transport par étapes en exécutant une requête par étapes ( `sp_staged=1`) avec `sp_t` qui est définie sur le nom de votre modèle de transport. Lorsque vous êtes satisfait de l’apparence de la mise en page, vous pouvez utiliser **[!UICONTROL Push Live]** depuis l’éditeur de modèles pour mettre le modèle en service. Une fois le modèle actif, les visiteurs du site commencent à l’utiliser.

Utilisez la référence de balise du modèle de présentation pour savoir comment associer votre modèle de présentation aux composants de recherche guidée tels que les facettes, les chemins de navigation et les menus.

Voir Balises de modèle de [présentation](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)

Utilisez la référence de balise du modèle de transport pour en savoir plus sur les balises à utiliser dans les modèles de transport.

Voir [Transport des balises de modèle](../c-appendices/c-templates.md#reference_227D199F5A7248049BE1D405C0584751)

**[!UICONTROL To edit a presentation or a transport template]**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, cliquez sur un nom de fichier de présentation ou de modèle de transport.
1. Sur la [!DNL Template Editor] page, effectuez les modifications que vous souhaitez apporter aux balises et au codage.

   Soyez attentif aux changements que vous apportez dans le [!DNL Template Editor]; il n’existe pas de fonction Annuler. Si vous effectuez une modification indésirable et souhaitez revenir à la version précédente du fichier, vous pouvez cliquer **[!UICONTROL Cancel]** pour revenir à la table des modèles (en supposant que vous n’ayez enregistré aucune de vos modifications jusqu’à ce moment). Si vous avez déjà enregistré vos modifications, vous pouvez les annuler **[!UICONTROL History]** dans l’éditeur.
1. (Facultatif) Cliquez sur **[!UICONTROL Insert Symbol]** pour saisir des caractères spéciaux et des symboles qui ne comportent pas de touches correspondantes sur les claviers en anglais américain.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Fermez la page Editeur de modèle lorsque vous avez terminé ; vous revenez à la page Modèles.

## Copie d’une présentation ou d’un fichier de modèle de transport {#task_B744AB3384C84DD59C33CD25E18C2C90}

Vous pouvez utiliser **[!UICONTROL Copy Template]** pour gagner du temps en dupliquant un modèle de présentation existant (.tmpl) ou un modèle de transport (.tpl) et l’ajouter à la page Modèles.

<!-- 

t_copying_a_presentation_or_a_transport_template.xml

 -->

Vous devez modifier le nom du modèle, son type ou les deux. Si vous n’apportez aucune modification, le modèle n’est pas copié.

Un modèle doit déjà être ajouté pour pouvoir copier un modèle.

Voir [Ajout d’un nouveau fichier](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de modèle de présentation ou de transport.

**Pour copier une présentation ou un fichier de modèle de transport**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, dans la liste déroulante en regard du nom du modèle à copier, cliquez sur **[!UICONTROL Copy]**.
1. Dans la [!DNL Copy Template] boîte de dialogue, définissez une ou plusieurs des options de votre choix.
1. Cliquez sur **[!UICONTROL Copy]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Attribution d’un nouveau nom à une présentation ou à un fichier de modèle de transport {#task_CC30050FC2DE4898BF44379D8378EB31}

Vous pouvez utiliser [!DNL Rename Template] pour modifier le nom d’un modèle de présentation existant (.tmpl) ou d’un modèle de transport (.tpl).

<!-- 

t_renaming_a_presentation_or_a_transport_template_file.xml

 -->

Vous pouvez également modifier le type de modèle, le cas échéant.

Un modèle doit déjà être ajouté pour renommer un modèle.

Voir [Ajout d’un nouveau fichier](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de modèle de présentation ou de transport.

**Pour renommer une présentation ou un fichier de modèle de transport**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, dans la liste déroulante en regard du nom du modèle à renommer, cliquez sur **[!UICONTROL Rename]**.
1. Dans la [!DNL Rename Template] boîte de dialogue, définissez une ou plusieurs des options de votre choix.
1. Cliquez sur **[!UICONTROL Rename]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une présentation ou d’un fichier de modèle de transport {#task_67E532C2B83A449687737E3B06C5AA58}

Vous pouvez utiliser **[!UICONTROL Delete Template]** pour supprimer un modèle de présentation existant (.tmpl) ou un modèle de transport (.tpl).

<!-- 

t_deleting_a_presentation_or_a_transport_template_file.xml

 -->

Vous disposez peut-être déjà d’une version correspondante du modèle mis en scène qui est publiée. Si c’est le cas, veillez à mettre en ligne le modèle supprimé **[!UICONTROL Staging]** afin qu’il soit également supprimé de l’environnement de production. Vous pouvez également utiliser **[!UICONTROL Push Live]** la page Modèles.

Voir [A propos de l’évaluation](../c-about-staging.md#concept_08B8F3CA1F4241108F14BA7FC7806CA7)

Voir [Pousser les paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

Un modèle doit déjà être ajouté pour pouvoir supprimer un modèle.

Voir [Ajout d’une nouvelle présentation ou d’un fichier de modèle de transport](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

**Pour supprimer une présentation ou un fichier de modèle de transport**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, dans la liste déroulante en regard du nom du modèle à supprimer, cliquez sur **[!UICONTROL Delete]**.
1. Dans la [!DNL Delete Template] boîte de dialogue, cliquez sur **[!UICONTROL Delete.]**
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Aperçu du modèle de présentation réduit {#task_1757B6207CC74221AE4BFFE5674D320B}

Vous pouvez **[!UICONTROL Preview minimized]** voir à quoi ressemblerait le poids réduit d’une page d’un modèle de présentation si vous choisissez de le réduire.

<!-- 

t_previewing_the_presentation_template_minimized.xml

 -->

Si vous réduisez le modèle de présentation principal, n’oubliez pas d’activer la réduction pour les modèles inclus (avec balise d’inclusion guidée) car cette option n’est pas héritable.

Voir [Réduction du poids d’une page d’un modèle de présentation sur votre...](../c-about-design-menu/c-about-templates.md#task_B09BB3CE89714DEAAE8D9A899CF3009E)

Vous devez déjà ajouter un modèle pour prévisualiser le modèle réduit.

Voir [Ajout d’une nouvelle présentation ou d’un fichier de modèle de transport](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)

Vous pouvez prévisualiser le code XML d’un fichier de modèle de transport.

Voir [Prévisualisation du code XML d’un fichier de modèle de transport](../c-about-design-menu/c-about-templates.md#task_58C6C52078E14AD88D2B2F0B3C439AE8)

**Pour prévisualiser le modèle de présentation réduit**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, dans la liste déroulante en regard du nom d’un modèle de présentation, cliquez sur **[!UICONTROL Preview minimized]**.

   Utilisez la **[!UICONTROL Type]** colonne du tableau Modèles pour trier les modèles par présentation et par transport.
1. (Facultatif) Sur la [!DNL Preview Minimized Template] page, cochez **[!UICONTROL Wrap lines]** la case pour lire les balises dans la fenêtre définie.
1. Cliquez sur **[!UICONTROL Close]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Réduction du poids de page d’un modèle de présentation sur votre site Web {#task_B09BB3CE89714DEAAE8D9A899CF3009E}

Vous pouvez réduire le poids d’une page d’un modèle de présentation en utilisant l’ **[!UICONTROL Minimize]** option du tableau du modèle.

<!-- 

t_reducing_the_page_weight_of_a_presentation_template.xml

 -->

En réduisant le poids de page du modèle, vous réduisez dynamiquement le code JavaScript intégré et le code CSS. Vous supprimez également les espaces blancs redondants dans le code HTML. La réduction du poids de la page du modèle de présentation peut vous aider à obtenir plus rapidement les résultats de votre recherche.

Vous pouvez également prévisualiser l’aspect du modèle de présentation réduit à l’aide de **[!UICONTROL Preview minimized]**.

Voir [Prévisualisation minimisée](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)du modèle de présentation.

**[!UICONTROL To reduce the page weight of a presentation template on your website]**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, sous la [!DNL Minimize] colonne, cochez la case correspondant à un ou plusieurs fichiers de modèle de présentation que vous souhaitez réduire au minimum sur votre site Web.

   Utilisez la **[!UICONTROL Type]** colonne du [!DNL Templates] tableau pour trier les modèles par présentation et par transport.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Définition du fichier de modèle de présentation par défaut à utiliser sur votre site Web {#task_C1E8CE817E4D43E096167A347C54DD53}

Lorsque vous disposez de plusieurs modèles de présentation, vous pouvez indiquer le modèle qui est initialement utilisé pour afficher les résultats de la recherche.

<!-- 

t_setting_the_default_presentation_template_file_to_use.xml

 -->

Vous pouvez utiliser les règles de pré-recherche, les règles de post-recherche et les règles de fonctionnement pour déterminer à quel moment l’un des autres modèles de présentation doit être utilisé.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

See [About Post-Search Rules](../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE).

See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

Il est courant d’avoir une règle du type &quot;Pour chaque recherche, définissez le modèle de présentation ciblé sur xxxx&quot;. Une telle règle étant en place, la modification du modèle &quot;par défaut&quot; sur la page Modèles ne semble pas avoir d’effet.

**[!UICONTROL To set the default presentation template file to use on your website]**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, sous la [!DNL Default] colonne, cliquez sur le bouton radio correspondant au fichier de modèle de présentation que vous souhaitez utiliser par défaut.

   Utilisez la **[!UICONTROL Type]** colonne du [!DNL Templates] tableau pour trier les modèles par présentation et par transport.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Prévisualisation du code XML d’un fichier de modèle de transport {#task_58C6C52078E14AD88D2B2F0B3C439AE8}

Vous pouvez utiliser [!DNL Preview] pour vérifier le code XML d’un modèle de transport que vous avez ajouté.

<!-- 

t_previewing_the_xml_of_a_transport_template_file.xml

 -->

Un modèle de transport doit déjà être ajouté pour prévisualiser le code XML du modèle.

Voir [Ajout d’un nouveau fichier](../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012)de modèle de présentation ou de transport.

Vous pouvez prévisualiser les fichiers de modèle de présentation minimisés afin d’afficher leur poids réduit.

Voir [Prévisualisation minimisée](../c-about-design-menu/c-about-templates.md#task_1757B6207CC74221AE4BFFE5674D320B)du modèle de présentation.

**Pour prévisualiser le code XML d’un fichier de modèle de transport**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.
1. Sur la [!DNL Templates] page, dans la liste déroulante en regard du nom d’un modèle de transport, cliquez sur **[!UICONTROL Preview]**.

   Utilisez la **[!UICONTROL Type]** colonne du [!DNL Templates] tableau pour trier les modèles par présentation et par transport.
1. Fermez la fenêtre d’affichage et revenez à [!DNL site search/merchandising].
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

