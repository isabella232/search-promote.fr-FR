---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp ; amp ; Promote 15.1.1 (15/01/2015)
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 15.1.1 (15/01/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 17%

---


# Notes de mise à jour de la Search &amp; Promote 15.1.1 (15/01/2015){#search-promote-release-notes}

## Nouvelle fonctionnalité {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Auparavant, les particularités linguistiques du type recherche de radical, synonymes, etc. étaient toujours appliquées aux mots-clés dans les règles de recherche guidée. Vous pouvez maintenant désactiver cette extension afin que le mot-clé soit utilisé en l’état.

   Pour appliquer des conditions de déclenchement à une règle métier, dans [!DNL Advanced Rule Builder], après **[!UICONTROL If any/all of the following conditions are met]**, dans la première liste déroulante, sélectionnez **[!UICONTROL keyword]**, puis sélectionnez le nouvel opérateur **[!UICONTROL equal exact]** dans la seconde liste déroulante.

   Voir [A propos des règles de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Correctifs et améliorations {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] et  [!DNL Advanced Rule Builder] ne tronque plus la valeur du champ MDI (Merchandising Document ID).
* Les échecs d’indexation RTBA sont maintenant corrigés.
* La modification d’une règle de fonctionnement existante dont l’état est &quot;approuvée&quot; révoque désormais l’état &quot;approuvé&quot;. Vous devez utiliser [!DNL Advanced Rule Builder] pour vérifier à nouveau l&#39;option **[!UICONTROL Approved]**, puis enregistrer la règle comme d&#39;habitude. Si vous ne réapprouvez pas une règle modifiée, l&#39;état de la règle est automatiquement défini sur En cours (Travail en cours) sur la page [!DNL Business Rules].
* Une nouvelle option **[!UICONTROL Advanced Search]** est désormais disponible sur la page [!DNL Business Rules] pour améliorer le filtrage des règles.
* Condition **[!UICONTROL contains word]** Ajoutée pour déclencher des règles dans [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules] et [!DNL Business Rules], afin de vous permettre de spécifier facilement des sauts de mot.
* Des améliorations ont été apportées aux notes de règle de fonctionnement, par exemple lorsque vous vue une règle, vous pouvez désormais récupérer l’historique des notes pour cette règle. En outre, les notes sont maintenant consignées dans **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Les requêtes dont les valeurs sont différentes de zéro `sp_i` ne sont plus exécutées par le redirecteur [!DNL Adobe Analytics].

   Reportez-vous à la ligne 15 du tableau de [Paramètres CGI de recherche dorsale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

