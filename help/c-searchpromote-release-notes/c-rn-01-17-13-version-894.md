---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 8.9.4 (17/01/2013)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 8.9.4 (17/01/2013)
topic: Release Notes,Site search and merchandising
uuid: a9d550f6-0a23-4c71-b123-c31b997e7384
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9.4 Release Notes (01/17/2013){#search-promote-release-notes}

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
   <td colname="col2"> <p> Ajout de la capacité de créer des notes intégrées lors de la création de règles de nettoyage de requête, de règles pré-recherche et de règles post-recherche. Le champ de notes vous permet de documenter et d’expliquer les règles. </p> <p>Voir <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" format="dita" scope="local"> A propos des règles</a>de nettoyage de requête. </p> <p>See <a href="../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F" format="dita" scope="local"> About Pre-Search Rules</a>. </p> <p>See <a href="../c-about-rules-menu/c-about-post-search-rules.md#concept_AF6ADFCC0ADF4A788003964939917FDE" format="dita" scope="local"> About Post-Search Rules</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Recherche guidée </p> </td> 
   <td colname="col2"> <p> Ajout de balises de recherche guidée pour indiquer le temps total nécessaire à une recherche. </p> <p> <span class="codeph"> &lt;guided-search-time&gt;</span> : identifie la durée de la recherche. La valeur de temps de recherche renvoyée est spécifiée en ms. </p> <p> <span class="codeph"> &lt;guided-fall-through-searches&gt;</span> : renvoie le nombre de recherches de noyaux utilisées pour créer la page des résultats de la recherche. </p> <p> <span class="codeph"> &lt;guided-if-fall-through-search&gt;</span> - Teste si le nombre de recherches principales est supérieur à 1. </p> <p>Voir aussi Langue diverse dans les balises <a href="../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64" format="dita" scope="local"> de modèle de</a>présentation. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correctifs**

* Le rapport Termes ignore désormais le caractère astérisque.

   Voir [Affichage du rapport Termes ou du rapport Termes de recherche nuls...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Ouvrez Rapports > Null Search Terms Report (rapport des termes de recherche nuls), sélectionnez un intervalle de temps, puis affichez le rapport. Cliquez sur un mot dans le rapport pour ouvrir la recherche, puis cliquez de nouveau sur Afficher le rapport. Le nombre de recherches du mot-clé sur lequel vous aviez cliqué était incrémenté deux fois. Ce problème est maintenant corrigé.

   Voir [Affichage du rapport Termes ou du rapport Termes de recherche nuls...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Les performances ont été optimisées pour la publication des règles commerciales. 

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* La capacité de suppression dans les chemins de navigation ne fonctionnait pas toujours.

   Voir [A propos des chemins de navigation](../c-about-design-menu/c-about-breadcrumbs.md#concept_FB8A943C594A4A1593B118141DA61F03).

* A moins que vous n’utilisiez l’option Régénérer, la fonction Reclasser n’autorisait aucune modification des règles de classement dans les résultats de la recherche.

   Voir [A propos des règles de classement](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

   Voir [A propos de l’index](../c-about-index-menu/c-about-re-rank-index.md#concept_147B0A9FCD51451787DA898E06F7C692)de classement.
