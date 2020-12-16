---
description: Vous pouvez utiliser l’index complet pour indexer toutes les pages de votre site Web intermédiaire ou intermédiaire. L'indexation permet à vos clients de trouver plus facilement ce qu'ils recherchent ou ce dont ils ont besoin lorsqu'ils effectuent une recherche.
seo-description: Vous pouvez utiliser l’index complet pour indexer toutes les pages de votre site Web intermédiaire ou intermédiaire. L'indexation permet à vos clients de trouver plus facilement ce qu'ils recherchent ou ce dont ils ont besoin lorsqu'ils effectuent une recherche.
seo-title: A propos de l'index complet
solution: Target
subtopic: Full Index
title: A propos de l'index complet
topic: Index,Site search and merchandising
uuid: dce1eafd-5aea-4945-8305-8f9e7dc392df
translation-type: tm+mt
source-git-commit: 7af85dd37f06fe506e5f57e28a25385ca7ab3db5
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 1%

---


# A propos de l&#39;index complet{#about-full-index}

Vous pouvez utiliser l’index complet pour indexer toutes les pages de votre site Web intermédiaire ou intermédiaire. L&#39;indexation permet à vos clients de trouver plus facilement ce qu&#39;ils recherchent ou ce dont ils ont besoin lorsqu&#39;ils effectuent une recherche.

## Utilisation de l&#39;index complet {#concept_C69BD21863FD4856B49326F35DB570D3}

Lorsque vous générez un index complet, des informations d’état s’affichent, telles que l’heure de début, le temps écoulé et les erreurs survenues pendant le processus d’indexation. Des informations sur l’état de votre dernier index s’affichent également.

Si vous avez modifié un paramètre de compte nécessitant une régénération d’index, l’état peut se lire &quot;Régénération&quot;. Lors de la régénération, les paramètres du compte sont appliqués pour créer un index de site mis à jour.

Vous pouvez arrêter ou redémarrer le processus d’indexation à tout moment.

Tandis que le nouvel index est créé pour un site Web actif, les clients peuvent continuer à rechercher votre site à l’aide de votre dernier index. Des informations sur l’état de votre dernier index s’affichent également.

## Définition du calendrier complet de l&#39;index pour un site Web actif {#task_6760F3256D004A228B38968DF15421F0}

Vous pouvez spécifier l’heure et les jours d’analyse de votre site Web et mettre à jour l’index.

L’heure sélectionnée est locale en fonction du fuseau horaire configuré dans les Paramètres du compte.

Voir [Configuration des paramètres de votre compte](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Les serveurs Web sont souvent programmés pour une maintenance en pleine nuit. Si votre serveur est hors service pendant une heure d&#39;indexation planifiée, le processus d&#39;indexation échoue. Veillez à sélectionner l’heure de la journée à laquelle votre serveur Web est disponible.

Le calendrier de l&#39;index ne s&#39;applique qu&#39;à votre index de production ; vous ne pouvez pas planifier des index par étapes.

**Pour définir la planification complète de l’index pour un site Web actif**

1. Dans le menu produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Schedule]**.
1. Dans la liste déroulante **[!UICONTROL Time]**, sélectionnez l’heure à laquelle vous souhaitez que l’indexation complète soit début.
1. Sélectionnez un ou plusieurs jours d&#39;exécution de l&#39;indexation complète.
1. Cliquez sur **[!UICONTROL Save Changes]**.

## Exécution d’un index complet d’un site Web en direct ou par étape {#task_F7FE04D8A1654A7787FCCA31B45EB42D}

Vous pouvez utiliser l’index complet pour indexer toutes les pages de votre site Web intermédiaire ou intermédiaire. L&#39;indexation permet à vos clients de trouver plus facilement ce qu&#39;ils recherchent ou ce dont ils ont besoin lorsqu&#39;ils effectuent une recherche.

**Pour exécuter un index complet d’un site Web en direct ou par étape**

1. Dans le menu produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Index]**.

1. Définissez les options d’indexation de votre choix.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Option </p> </th> 
    <th colname="col2" class="entry"> <p>Description </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Effacer le cache d'index </p> </td> 
    <td colname="col2"> <p>Supprime tous les documents du cache d'index. </p> <p>Lorsqu’elle est sélectionnée, chaque page de site Web est téléchargée à partir de votre serveur. Si ce paramètre est coché et désactivé, votre compte est configuré pour effacer le cache chaque fois qu'un index complet est exécuté. Certains paramètres de compte précédemment modifiés nécessitent désormais un index complet. </p> <p>Si elle est désélectionnée, toutes les pages indexées restent dans l’index jusqu’à ce que le serveur Web indique que la page n’existe plus. Cette situation est vraie même si les liens vers cette page sont supprimés. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Régénérer en attente </p> </td> 
    <td colname="col2"> <p>Sélectionnez Si vous avez apporté des modifications à vos paramètres de compte qui ont considérablement modifié le contenu de votre index. Parmi les modifications importantes à apporter, citons les suivantes : 
    <ul id="ul_4EB8FF692FEB47BBB9A64D61299380D1"> 
    <li id="li_7CF8D286512F4210BEA3DB9F0EFA097A">Synonymes </li> 
    <li id="li_8178ABC342BB4365B3927E20433756E3">Collections </li> 
    <li id="li_57C8BD06BFA64AFAA2C9EF2CC59520EF">Métadonnées </li> 
    <li id="li_C4B6A7DA023B4A43991D03EC592170C9">Mots exclus </li> 
    <li id="li_9E0AD4B6DDC24A5A8FB5C2C1CCD5348A">Langue du compte </li> 
    <li id="li_338F107547DF48AAA0EF90F4AD8664A5">Classement </li> 
    <li id="li_7F49B86D94974E79AAD381A64A1400F2">Basculement de la recherche sensible à la casse </li> 
    <li id="li_E8FE6EE240A840AC826ADF4294AAC6F6">Basculement du support diacritique </li> 
    <li id="li_51763D482DCB4ED0972966F492B8C0F2">Basculement de l'indexation des nombres </li> 
    </ul> </p> <p>Avant qu’une autre analyse n’ait lieu, toutes les données d’index sont traitées rapidement pour la rendre conforme aux nouveaux paramètres de compte. </p> <p>Cette option n’est disponible que si vous effectuez un index complet d’un site Web intermédiaire. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Compter toutes les pages </p> </td> 
    <td colname="col2"> <p>Permet à l’analyse des pages du site Web de se poursuivre même après avoir atteint la limite de page de votre compte. </p> <p>D'autres pages ne sont pas ajoutées à votre index, mais vous pouvez déterminer le nombre total de documents présents sur votre site Web. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Full Index Now]**.
1. (Facultatif) Si des erreurs d’indexation se sont produites, cliquez sur **[!UICONTROL View Errors]** pour vue du journal associé.

## Affichage du journal d&#39;index complet d&#39;un site Web en direct ou d&#39;un site Web intermédiaire {#task_02E5E944C56B4EB19CC1FF321F3221B8}

Lorsqu’un index complet actif ou un index complet intermédiaire est terminé, vous pouvez vue le journal associé pour résoudre les erreurs qui se sont produites.

Vous ne pouvez pas exporter de journaux ni les enregistrer. Le journal reste disponible pour affichage jusqu&#39;à ce que le nouvel index se produise.

**Pour vue du journal d&#39;index complet d&#39;un site Web en direct ou par étape**

1. Dans le menu produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Log]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Staged Log]**.

1. Dans la page de journal, en haut ou en bas, effectuez l’une des opérations suivantes :

   * Utilisez les options de navigation **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** pour parcourir le journal.

   * Utilisez les options d&#39;affichage **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** pour affiner ce que vous voyez.

