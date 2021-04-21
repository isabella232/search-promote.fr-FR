---
description: Vous pouvez utiliser des balises MEO (Search Engine Optimization) pour aider à personnaliser certains éléments de vos pages et ainsi améliorer le positionnement des moteurs de recherche.
solution: Target
subtopic: SEO
title: A propos du référencement
topic-legacy: Settings,Site search and merchandising
uuid: 5c5d64f5-fe79-4489-85c6-399d1437f2c4
exl-id: 0045455b-cb86-4820-82fa-753475ab6ca6
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1201'
ht-degree: 1%

---

# A propos de SEO{#about-seo}

Vous pouvez utiliser des balises MEO (Search Engine Optimization) pour aider à personnaliser certains éléments de vos pages et ainsi améliorer le positionnement des moteurs de recherche.

## Utilisation de SEO {#concept_C58BFCE720824A2B9B5F5E613CFD4C0B}

Vous pouvez définir chaque élément comme un texte de début suivi d’une liste de mots. La liste de mots peut inclure les éléments suivants :

* Phrases de recherche populaires sur votre site au cours d’une période sélectionnée (par exemple, &quot;mois dernier&quot;), sous réserve de vos exclusions personnalisées.
* Jeu de valeurs d’un ou de plusieurs champs à partir de la recherche de la page.
* Mots et expressions statiques que vous définissez dans une liste

Les éléments de page les plus utilisés pour l’optimisation du référencement sont le titre de la page et les méta-balises &quot;mots-clés&quot; et &quot;description&quot;. Vous pouvez définir des paramètres pour ces trois éléments de page. En outre, vous pouvez définir ces trois paramètres pour chacun des trois types de pages : Pages de résultats de la recherche, Pages de navigation et Pages de détails de l’élément.

Lorsque vous enregistrez ou prévisualisation vos paramètres d&#39;optimisation du référencement, de petits segments de modèles de recherche (transport) sont générés, que vous pouvez inclure dans vos autres modèles de recherche avec la balise de modèle `<search-include>`. Par exemple, vous pouvez inclure le champ Titre des pages des résultats de la recherche dans un autre modèle avec ce qui suit :

```
<search-include file="seo/seo_search_title.tpl" />
```

Les neuf valeurs possibles pour l’attribut `file` de la balise `<search-include>` pour les champs d’optimisation du référencement sont les suivantes :

* `seo/seo_search_title.tpl`
* `seo/seo_search_description.tpl`
* `seo/seo_search_keywords.tpl`
* `seo/seo_browse_title.tpl`
* `seo/seo_browse_description.tpl`
* `seo/seo_browse_keywords.tpl`
* `seo/seo_item_title.tpl`
* `seo/seo_item_description.tpl`
* `seo/seo_item_keywords.tpl`

Pour utiliser les champs d’optimisation du référencement dans un modèle de présentation, vous devez effectuer plusieurs étapes.

Tout d’abord, vous utilisez `<search-include>` comme décrit ci-dessus pour inclure les champs souhaités dans un modèle de recherche XML, dans un élément `<general>`.

Ensuite, entourez chaque balise `<search-include>` de balises `<general-field>` et `</general-field>`, en indiquant les noms de champ dans l&#39;attribut `name` comme dans l&#39;exemple suivant :

```
<general> 
    <general-field name="seo_search_title"><search-include file="seo/seo_search_title.tpl" /></general-field> 
    <general-field name="seo_search_description"><search-include file="seo/seo_search_description.tpl" /></general-field> 
    <general-field name="seo_search_keywords"><search-include file="seo/seo_search_keywords.tpl" /></general-field> 
</general>
```

Ensuite, dans votre modèle de présentation, vous pouvez utiliser des balises `<guided-general-field>` pour insérer les champs nommés où vous le souhaitez, comme dans l&#39;exemple suivant :

```
<title><guided-general-field gsname="default" field="seo_search_title"></title> 
<meta name="description" content="<guided-general-field gsname="default" field="seo_search_description">"/> 
<meta name="keywords" content="<guided-general-field gsname="default" field="seo_search_keywords">"/>
```

Notez l&#39;utilisation de l&#39;attribut `gsname` pour spécifier, dans ce cas, la recherche &quot;par défaut&quot;.

Au total, vous pouvez définir neuf champs d’optimisation du référencement différents que vous pouvez utiliser dans vos pages Web. Il s&#39;agit des éléments suivants :

* Pages des résultats de recherche - titre, description et mots-clés
* Pages de navigation - titre, description et mots-clés
* Pages Détails de l&#39;élément - titre, description et mots-clés

Les neuf champs sont définis avec des paramètres similaires. En fait, les noms des neuf champs, tels que le champ &quot;titre&quot; dans &quot;Pages de résultats de la recherche&quot;, ne sont que des suggestions sur la façon de les utiliser. Vous pouvez utiliser n’importe quel champ dans n’importe quel contexte dans vos modèles de présentation et de recherche.

Voir aussi [À propos des modèles](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

Voir aussi [Balises de modèle de présentation](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64).

Voir aussi [Rechercher des balises de modèle](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Voir aussi [Configuration d&#39;une liste de mots de résultats de recherche](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).

## Configuration d&#39;une liste de mots de résultats de recherche {#task_A459A3734EC04042BA52C81184251DD4}

Vous pouvez configurer la liste des mots et expressions de résultats de recherche qui sont inclus dans les titres de page, les descriptions et les mots-clés.

**Pour configurer une liste de mots de résultats de recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Sur la page [!DNL SEO Browse Pages Word List], dans les groupes [!DNL Title], [!DNL Description] et [!DNL Keywords] respectifs, définissez les options de votre choix.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Titre | Description | Mots-clés Débuts avec </p> </td> 
      <td colname="col2"> <p>Texte à afficher devant la liste de mots. </p> <p>Par exemple, vous souhaitez peut-être que la liste Mots-clés commence par le mot "Marques". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure les recherches populaires pendant </p> </td> 
      <td colname="col2"> <p>Période pendant laquelle les recherches sont incluses. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre maximal de recherches </p> </td> 
      <td colname="col2"> <p>Nombre maximal de recherches incluses. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure les valeurs de champ </p> </td> 
      <td colname="col2"> <p>Valeurs de champ incluses dans la liste de mots des résultats. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajouter ces mots et expressions </p> </td> 
      <td colname="col2"> <p>Liste des mots à ajouter au titre de la page des résultats de la recherche, au titre de la page de navigation ou au titre de la page des détails de l'article. </p> <p>Cliquez sur <b>Modifier</b> pour ajouter des mots à la liste. </p> <p>Vous pouvez ajouter un mot ou une expression par ligne. Lorsque vous avez terminé, cliquez sur <b>Enregistrer les modifications</b>, puis fermez la page pour revenir à la page d’optimisation du référencement principale. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer ces mots et expressions (à l’exception des valeurs de champ incluses) </p> </td> 
      <td colname="col2"> <p>Liste des mots à supprimer du titre de la page des résultats de la recherche, du titre de la page de navigation ou du titre de la page des détails de l'élément. </p> <p>Cliquez sur <b>Modifier</b> pour ajouter des mots à la liste de suppression. </p> <p>Vous pouvez ajouter un mot ou une expression par ligne. Lorsque vous avez terminé, cliquez sur <b>Enregistrer les modifications</b>, puis fermez la page pour revenir à la page d’optimisation du référencement principale. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Cliquez sur **Prévisualisation Exemple de résultat** pour prévisualisation les valeurs résultantes pour les champs d’optimisation du référencement que vous avez définis.

   Voir [Prévisualisation des métadonnées d’optimisation du référencement que vous avez configurées](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL SEO Search Results Word List], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuration d’une liste de mots de pages de navigation {#task_D7A1D765A92A4D6C94E672B3A86ECB5A}

Vous pouvez configurer la liste des mots et expressions des pages de navigation qui sont inclus dans les titres, descriptions et mots-clés des pages.

**Pour configurer une liste de mots des pages de navigation**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Browse Pages]**.
1. Sur la page [!DNL SEO Browse Pages Word List], dans les groupes [!DNL Title], [!DNL Description] et [!DNL Keywords] respectifs, définissez les options de votre choix.

   Consultez le tableau des options sous [Configuration d&#39;une liste de mots de résultats de recherche](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Facultatif) Cliquez sur **Prévisualisation Exemple de résultat** pour prévisualisation les valeurs résultantes pour les champs d’optimisation du référencement que vous avez définis.

   Voir [Prévisualisation des métadonnées d’optimisation du référencement que vous avez configurées](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL SEO Browse Pages Word List], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuration d&#39;une liste de mots de détails d&#39;article {#task_761538C519B34164BE189F13C39B2495}

Vous pouvez configurer la liste des mots et expressions de détail d’article inclus dans les titres de page, les descriptions et les mots-clés.

**Pour configurer une liste de mots des détails d&#39;un article**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Item Detail Pages]**.
1. Sur la page [!DNL SEO Item Detail Word List], dans les groupes [!DNL Title], [!DNL Description] et [!DNL Keywords] respectifs, définissez les options de votre choix.

   Consultez le tableau des options sous [Configuration d&#39;une liste de mots de résultats de recherche](../c-about-settings-menu/c-about-seo.md#task_A459A3734EC04042BA52C81184251DD4).
1. (Facultatif) Cliquez sur **Prévisualisation Exemple de résultat** pour prévisualisation les valeurs résultantes pour les champs d’optimisation du référencement que vous avez définis.

   Voir [Prévisualisation des métadonnées d’optimisation du référencement que vous avez configurées](../c-about-settings-menu/c-about-seo.md#task_3F97949E193C4F92A104AD117FE49621).
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL SEO Item Detail Word List], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Prévisualisation des balises MEA SEO que vous avez configurées {#task_3F97949E193C4F92A104AD117FE49621}

Vous pouvez prévisualisation les valeurs résultantes des champs d’optimisation du référencement que vous avez définis pour voir ce qui est inséré à l’endroit où vous les utilisez.

Les champs d’optimisation du référencement peuvent contenir des valeurs de champ incluses, de sorte que les résultats de la recherche peuvent dépendre de la requête de recherche spécifiée.

**Pour prévisualisation des balises méta d’optimisation du référencement que vous avez configurées**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL SEO]** > **[!UICONTROL Search Result Pages]**.
1. Sur la page d’optimisation du référencement, cliquez sur **Exemple de sortie de Prévisualisation**.
1. Sur la page [!DNL SEO Preview], dans le champ [!DNL Enter sample query], entrez le terme de requête sur lequel vous souhaitez effectuer une recherche.
1. Cliquez sur **Rechercher**.

   Les champs Titre, Description et Mots-clés qui en résultent affichent le contenu inséré dans une page en fonction de la requête de recherche que vous venez de saisir.
1. Cliquez sur **Fermer** pour revenir à la page d’optimisation du référencement principale.
