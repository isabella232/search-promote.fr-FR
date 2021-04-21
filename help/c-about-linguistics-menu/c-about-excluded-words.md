---
description: Vous pouvez utiliser des mots exclus pour spécifier les expressions fréquemment utilisées et les mots courants, tels que "a" et "the", que vous souhaitez exclure des résultats de la recherche.
solution: Target
title: A propos des mots exclus
topic-legacy: Linguistics,Site search and merchandising
uuid: 1c879462-1b19-44f6-a3b2-20aa786b3221
exl-id: d553b776-907a-4f4a-8481-b36dc0cb75c9
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# A propos des mots exclus{#about-excluded-words}

Vous pouvez utiliser des mots exclus pour spécifier les expressions fréquemment utilisées et les mots courants, tels que &quot;a&quot; et &quot;the&quot;, que vous souhaitez exclure des résultats de la recherche.

## Utilisation de mots exclus {#concept_9DB67BD2F0DC43AC88741003D9F39812}

Voir aussi [A propos des recherches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

Sans les mots exclus, les recherches qui contiennent ces mots peuvent identifier de nombreux résultats non pertinents. Lorsque vous excluez des mots et des expressions, les résultats de la recherche ne correspondent qu’aux termes exclus que vous avez spécifiés. Si une requête de recherche contient un mot exclu, seuls les mots non exclus sont utilisés pour trouver des documents.

Les mots de recherche exclus ne sont pas mis en évidence dans les résultats de la recherche. Cependant, le score de pertinence de chaque résultat est influencé par les mots exclus. En d’autres termes, les mots exclus sont ignorés lors de la recherche de documents, mais ils sont toujours utilisés lors du classement des documents dans la page des résultats de la recherche. Avant que les effets des paramètres Mots exclus (ou les modifications apportées à ces paramètres) ne soient disponibles pour les clients, veillez à régénérer l&#39;index de votre site.

Lorsque vous entrez des mots à exclure des résultats de la recherche, vous séparez les mots ou les expressions les uns des autres par des virgules. Vous pouvez saisir un ou plusieurs mots exclus par ligne. Voici un exemple de mots exclus sur des lignes distinctes et divisés par des virgules.

![](assets/excluded_words_1.jpg)

En utilisant l&#39;exemple de liste de mots exclus ci-dessus, si votre client recherche &quot;les états-unis d&#39;Amérique&quot;, les mots &quot;le&quot; et &quot;de&quot; sont exclus de la recherche. Au lieu de cela, la recherche trouve toutes les pages qui contiennent les mots &quot;unis&quot;, &quot;états&quot; et &quot;amérique&quot;. Les pages qui contiennent uniquement le mot &quot;de&quot; ou &quot;le&quot; ne s’affichent pas.

Certains sites contiennent des expressions spécifiques sur la plupart ou la totalité des pages. Par exemple, un site Web sur le tourisme à New York pourrait contenir les mots New York dans le titre de chaque page. Envisagez d&#39;ajouter cette expression, ainsi que d&#39;autres similaires, à la liste d&#39;exclusion :

![](assets/excluded_words_2.jpg)

Lorsqu’une expression est exclue, les mots individuels qui la composent sont toujours utilisés comme termes de recherche. Ce n&#39;est que lorsqu&#39;un visiteur recherche les mots exacts, dans l&#39;ordre exact d&#39;une expression exclue, que l&#39;expression est exclue des résultats de la recherche. Si, à l’aide de l’exemple ci-dessus, un client a recherché le &quot;ballet new york&quot;, les mots &quot;the&quot; et &quot;new york&quot; sont exclus ; seules les pages qui contiennent le mot &quot;ballet&quot; sont renvoyées comme résultat de recherche. D&#39;un autre côté, une recherche de &quot;nouveaux bâtiments&quot; ou &quot;duc de York&quot; trouve encore des pages qui contiennent respectivement le mot &quot;nouveau&quot; ou &quot;york&quot;.

## Configuration des mots exclus {#task_60BF6BB7A66C48479D2BBB32C0F38CDE}

Vous pouvez exclure des résultats de recherche les expressions et les mots courants fréquemment utilisés.

Vous pouvez saisir un ou plusieurs mots par ligne. Séparez chaque mot par des virgules, comme dans l’exemple suivant :

![](assets/excluded_words_1.jpg)

Vous pouvez choisir d&#39;afficher les résultats de la recherche lorsque tous les mots de la recherche du client sont exclus. Par exemple, si vous avez exclu le mot &quot;le&quot; et qu’un client choisit de rechercher uniquement &quot;le&quot;, les résultats de la recherche affichent toute page contenant le mot &quot;le&quot;. Ce résultat est vrai même si le mot &quot;le&quot; est exclu. Si vous ne cochez pas cette option, le client n’obtient aucun résultat de recherche. Ce paramètre n’a aucun effet si la recherche contient au moins un mot non exclu.

**Pour configurer des mots exclus**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Excluded Words]**.
1. Sur la page [!DNL Excluded Words], dans le champ de texte **[!UICONTROL Words and Phrases]**, saisissez les mots que vous souhaitez exclure des résultats de la recherche.
1. (Facultatif) Cliquez sur **[!UICONTROL Show results when all words in the query are excluded words]**.

   Lorsque tous les mots de la recherche du client sont des mots exclus, tous les mots sont utilisés ensemble pour effectuer la recherche.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. Pour prévisualisation les résultats de vos modifications, cliquez sur **[!UICONTROL regenerate your staged site index]** pour recréer l&#39;index de votre site Web intermédiaire.

   Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

   Voir [Exécution d’un index incrémentiel d’un site Web dynamique ou d’un site Web intermédiaire..](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).
1. (Facultatif) Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Excluded Words]**, puis effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
