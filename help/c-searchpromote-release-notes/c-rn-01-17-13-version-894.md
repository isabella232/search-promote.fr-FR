---
description: Search&amp ; amp ; Notes de mise à jour de Promote 8.9.4.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.9.4 (17/01/2013)
topic-legacy: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
exl-id: cb5d93d9-54ac-4b41-96ad-66f18ee1e934
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 30%

---

# Notes de mise à jour de Search &amp; Promote 8.9.4 (17/01/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nouvelles fonctionnalités et améliorations </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Règles </p> </td> 
   <td colname="col2"> <p> Ajout de la capacité de créer des notes intégrées lors de la création de règles de nettoyage de requête, de règles pré-recherche et de règles post-recherche. Le champ de notes vous permet de documenter et d’expliquer les règles. </p> <p>Voir <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> À propos des règles de nettoyage de Requête</a>. </p> <p>Voir <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> À propos des règles préalables à la recherche</a>. </p> <p>Voir <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> À propos des règles de post-recherche</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recherche guidée </p> </td> 
   <td colname="col2"> <p> Balises de recherche guidée Ajoutées pour indiquer la durée totale de la recherche. </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> - Identifie la durée de la recherche. La valeur de temps de recherche renvoyée est spécifiée en ms. </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> - Renvoie le nombre de recherches de coeurs utilisées pour créer la page des résultats de la recherche. </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> - Teste si le nombre de recherches de base est supérieur à 1. </p> <p>Voir aussi Langage divers dans <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> Balises de modèle de présentation</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correctifs**

* Le rapport Termes ignore désormais le caractère astérisque.

   Voir [Affichage du rapport Termes ou du rapport Termes de recherche nuls..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Ouvrez **[!UICONTROL Reports > Null Search Terms Report]**, sélectionnez un intervalle de temps, puis vue le rapport. Cliquez sur un mot dans le rapport pour ouvrir la recherche, puis cliquez de nouveau sur Afficher le rapport. Le nombre de recherches du mot-clé sur lequel vous aviez cliqué était incrémenté deux fois. Ce problème est maintenant corrigé.

   Voir [Affichage du rapport Termes ou du rapport Termes de recherche nuls..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Une optimisation des performances a été réalisée lorsque vous publiez les règles métier.

   Voir [A propos des règles de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* La possibilité de supprimer dans [!DNL Breadcrumbs] ne fonctionnait pas toujours.

   Voir [A propos des chemins de navigation](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* A moins que vous n’utilisiez la fonction de régénération, la fonction de reclassement n’autorisait aucune modification des règles de classement à prendre effet dans les résultats de la recherche.

   Voir [A propos des règles de classement](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

   Voir [A propos de l&#39;index de classement](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692).
