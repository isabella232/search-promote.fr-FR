---
description: Search&amp ; amp ; Notes de mise à jour de Promote 8.11.0.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.11.0 (29/10/2013)
topic-legacy: Release Notes,Site search and merchandising
uuid: 973f9608-a5c7-4571-ae2b-6f1fa05bc862
exl-id: b417b275-7b04-4855-9e2a-9de0faa262cc
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 58%

---

# Notes de mise à jour de Search &amp; Promote 8.11.0 (29/10/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nouvelle fonctionnalité </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Outils de décomposition de mots pour le danois </p> </td> 
   <td colname="col2"> <p> Un mécanisme est maintenant mis en place pour permettre à <span class="keyword"> Adobe Search &amp; Promote</span> d'accéder à la langue (danoise) de détection, de décomposition, d'enracinement et de segmentation des services fournis par l'Adobe. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Améliorations et correctifs**

* Améliorations apportées aux fonctionnalités existantes de correspondance des tables [!DNL Search&Promote]. Ces améliorations assurent une meilleure prise en charge des besoins des clients en ce qui concerne les relations toujours plus complexes entre les données de SKU et de produit.

   >[!NOTE]
   >
   >Cette fonction n’est pas activée par défaut. Contactez le service d’assistance à la clientèle Adobe pour l’activer dans Search&amp;Promote.

* Ajout d’une option permettant à la recherche guidée de trier les facettes à l’aide du paramètre linguistique du compte.

   >[!NOTE]
   Cette fonction n’est pas activée par défaut. Contactez le service d’assistance à la clientèle Adobe pour l’activer dans Search&amp;Promote.

* Ajout d’une option permettant d’augmenter le nombre de valeurs de facette qu’un utilisateur peut spécifier pour les facettes à sélection multiple.

   >[!NOTE]
   Cette fonction n’est pas activée par défaut. Contactez le service d’assistance à la clientèle Adobe pour l’activer dans Search&amp;Promote.

* Ajouté l’option de case à cocher **[!UICONTROL Only allow searches that use HTTPS]** sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**.

   Voir [À propos des restrictions](../c-about-settings-menu/c-about-searching-menu.md#concept_B5B527E04EBF4E9AB5956EEF881DDBF1).

* Ajouté une option sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]** > **[!UICONTROL Create Feed]** > **[!UICONTROL Generic Feed]** pour conserver les caractères de tabulation dans le panneau [!DNL File Submission] de l&#39;Assistant.

   Voir [Création d’un flux](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250).

* Augmentation de la taille des données acceptées dans chacun des champs supérieurs et inférieurs pour le nouveau formulaire de définition de facettes ; la taille est désormais de 1 000 caractères, au lieu de 80 auparavant.

   Voir [A propos des facettes](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

* Les paramètres de débogage de la recherche guidée génèrent désormais un rapport correct sur les numéros des règles métier.
* Les règles métier sont maintenant appliquées dans l’environnement de production.
* Les recherches de proximité fonctionnent désormais en cas de recherche par longitude/latitude pour les comptes configurés avec la propriété Langue = &quot;Danois (Danemark)&quot;.
* Les déclencheurs basés sur les résultats auxquels aucune planification n’est affectée sont maintenant déclenchés.
* Des résultats cohérents sont maintenant signalés lors de l&#39;utilisation de l&#39;option **[!UICONTROL Ignore Apostrophes]** dans **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**.

   Voir [A propos des mots et de la langue](../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79).

* Le remplissage automatique de la liste des mots fonctionne désormais sur un grand nombre de facettes.
