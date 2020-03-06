---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 15.1.1 (15/01/2015)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 15.1.1 (15/01/2015)
topic: Release Notes,Site search and merchandising
uuid: 070f9c46-426f-4ca1-80c7-8ca53d40a402
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 15.1.1 Release Notes (01/15/2015){#search-promote-release-notes}

## Nouvelle fonctionnalité {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Auparavant, les particularités linguistiques du type recherche de radical, synonymes, etc. étaient toujours appliquées aux mots-clés dans les règles de recherche guidée. Vous pouvez maintenant désactiver cette extension afin que le mot-clé soit utilisé en l’état.

   Lorsque vous souhaitez appliquer des conditions de déclenchement à une règle de fonctionnement, dans la première liste déroulante [!DNL Advanced Rule Builder], **[!UICONTROL If any/all of the following conditions are met]** ci-dessous, sélectionnez **[!UICONTROL keyword]**, puis sélectionnez le nouvel opérateur **[!UICONTROL equal exact]** dans la seconde liste déroulante.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* [!DNL Visual Rule Builder] et [!DNL Advanced Rule Builder] ne tronque plus la valeur du champ MDI (Merchandising Document ID).
* Les échecs d’indexation RTBA sont maintenant corrigés.
* La modification d’une règle de fonctionnement existante dont l’état est &quot;approuvée&quot; révoque désormais l’état &quot;approuvé&quot;. You must use [!DNL Advanced Rule Builder] to recheck the option **[!UICONTROL Approved]**, and then save the rule as usual. If you do not reapprove an edited rule, the rule&#39;s status is automatically set to WIP (Work In Progress) on the [!DNL Business Rules] page.
* A new **[!UICONTROL Advanced Search]** option is now available on the [!DNL Business Rules] page for improved filtering of rules.
* Ajout d’une **[!UICONTROL contains word]** condition aux déclencheurs de règle [!DNL Query Cleaning], [!DNL Pre-Search Rules], [!DNL Post Search Rules]et [!DNL Business Rules], afin de vous permettre de spécifier facilement des sauts de mot.
* Des améliorations ont été apportées aux notes de règle de fonctionnement, telles que lorsque vous affichez une règle, vous pouvez désormais récupérer l’historique des notes pour cette règle. En outre, les notes sont maintenant connectées dans **[!UICONTROL Reports]** > **[!UICONTROL Change Log]**.
* Queries with nonzero `sp_i` values are no longer run through the [!DNL Adobe Analytics] redirector.

   Reportez-vous à la ligne 15 du tableau des paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)en arrière-plan.

