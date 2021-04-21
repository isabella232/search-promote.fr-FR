---
description: Search&amp ; amp ; Notes de mise à jour de Promote 8.16.0.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.16.0 (18/09/2014)
topic-legacy: Release Notes,Site search and merchandising
uuid: 0a59858b-213b-40d6-aea1-d085c4d6d2fa
exl-id: 929d6f97-4939-4e37-aded-6a746757b960
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 39%

---

# Notes de mise à jour de la version 8.16.0 (18/9/2014){#search-promote-release-notes}

## Notes de mise à jour de la version 8.16.0 (18/9/2014) {#topic_5BECD3F66C684987828F6AE65E62DA29}

## Nouvelles fonctionnalités {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Mise en cache des résultats de la recherche dans Guided Search 3 (GS3) - Pour configurer cette fonctionnalité personnalisée afin que vous puissiez l’utiliser dans votre compte, contactez votre gestionnaire de compte technique Adobe.
* Mises à jour verticales pour les champs fréquemment modifiés : vous pouvez désormais mettre rapidement à jour toutes les valeurs d’un ensemble de champs de métadonnées sans avoir à réindexer complètement votre contenu.

   Voir l’option Champ de mise à jour verticale dans le tableau sous [Ajouter un nouveau champ de balise meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5) et [À propos de la mise à jour verticale](../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899).

   Cette fonctionnalité ne peut être utilisée que sur les comptes [!DNL Adobe Search&Promote] qui utilisent Index Connector. Pour que cette fonction personnalisée soit configurée afin que vous puissiez l’utiliser dans votre compte, contactez votre gestionnaire de compte technique Adobe.

## Correctifs et améliorations {#section_22D1AFC99F394D569898828A0D3C419D}

* Correction de l’analyse du connecteur d’index des flux XML qui contenaient une chaîne `?>`.
* Correction des flux SFTP du connecteur d’index lorsque le nombre minimum de documents est en vigueur.
* L’exportation de rapports vers Microsoft Excel prend maintenant en charge le format UTF8.
* Recherche guidée : la compilation des facettes était lente.
* Chargeur d’attributs : les données agrégées comprenaient des clés en double.
* Correction de l’ordre d’exécution incorrect des règles métier lors de la publication d’une règle individuelle.
* Des liens de facettes Annuler incorrects étaient générés par la recherche guidée.
* Ajout d’une nouvelle opération de contrôle à distance (`sp_lines=N`) qui empêchait de vérifier la progression et l’état d’une analyse d’index en cours d’exécution.

   Voir [À propos du contrôle à distance pour l&#39;indexation](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

* La nécessité d’envoyer des informations d’authentification lors de la récupération supprime les informations durant l’incrémentation du connecteur d’index.
* Le rapport [!DNL Change Log] identifie maintenant l&#39;utilisateur qui lance une opération d&#39;indexation manuelle.

   Voir [Affichage du journal des modifications](../c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

* Lorsque vous exportez un [!DNL Terms Report], vous n&#39;êtes plus limité à 500 éléments ou moins dans le rapport.

   Voir [Affichage du rapport Termes ou du rapport Termes de recherche nuls..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* Le paramètre **[!UICONTROL Strip HTML]** du connecteur d’index s’affichait toujours comme coché.
* Des résultats de recherche incohérents ont été observés avec la fonction **[!UICONTROL Common Phrases]**.
* L’affichage des noms d’attribut était tronqué dans le résumé des listes de règles.
* La publication d’une règle métier individuelle impliquait la mise en oeuvre de toutes les règles métier.
