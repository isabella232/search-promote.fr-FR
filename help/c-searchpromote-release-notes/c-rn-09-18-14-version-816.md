---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 8.16.0 (18/09/2014)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 8.16.0 (18/09/2014)
topic: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 8.16.0 Release Notes (9/18/2014){#search-promote-release-notes}

## Search&amp;Promote 8.16.0 Release Notes (9/18/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## New features {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Mise en cache des résultats de recherche dans Guided Search 3 (GS3) - Pour configurer cette fonctionnalité personnalisée pour que vous puissiez l’utiliser dans votre compte, contactez votre gestionnaire de compte technique Adobe.
* Mises à jour verticales pour les champs fréquemment modifiés : vous pouvez désormais mettre à jour rapidement toutes les valeurs d’un ensemble de champs de métadonnées sans avoir à complètement réindexer votre contenu.

   Reportez-vous à l’option Champ de mise à jour verticale dans le tableau de la section [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) de balise meta et [A propos de la mise à jour](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)verticale.

   This feature can only be used on [!DNL Adobe Search&Promote] accounts that use Index Connector. Pour que cette fonction personnalisée soit configurée afin que vous puissiez l’utiliser dans votre compte, contactez votre gestionnaire de compte technique Adobe.

## Fixes and enhancements {#section_22D1AFC99F394D569898828A0D3C419D}

* Corrected the Index Connector parsing of XML feeds that contained `?>` string.
* Correction des flux SFTP du connecteur d’index lorsque le nombre minimum de documents est en vigueur.
* L’exportation de rapports vers Microsoft Excel prend maintenant en charge le format UTF8.
* Recherche guidée : la compilation des facettes était lente.
* Chargeur d’attributs : les données agrégées comprenaient des clés en double.
* Correction de l’ordre d’exécution incorrect des règles métier lors de la publication d’une règle individuelle.
* Des liens de facettes Annuler incorrects étaient générés par la recherche guidée.
* Ajout d’une nouvelle opération de contrôle à distance (`sp_lines=N`) qui empêchait de vérifier la progression et l’état d’une analyse d’index en cours d’exécution.

   Voir [A propos du contrôle à distance pour l’indexation](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* La nécessité d’envoyer des informations d’authentification lors de la récupération supprime les informations durant l’incrémentation du connecteur d’index.
* The [!DNL Change Log] report now identifies the user who initiates a manual index operation.

   See [Viewing the Change Log](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* When you export a [!DNL Terms Report], you are no longer limited to 500 or less items in the report.

   Voir [Affichage du rapport Termes ou du rapport Termes de recherche nuls...](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Le paramètre **[!UICONTROL Strip HTML]** du connecteur d’index s’affichait toujours comme coché.
* Inconsistent search results were experienced with the **[!UICONTROL Common Phrases]** feature.
* L’affichage des noms d’attribut était tronqué dans le résumé des listes de règles.
* La publication d’une règle métier individuelle entraînait l’activation de toutes les règles métier.

