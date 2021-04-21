---
description: Vous pouvez utiliser Rollback pour sauvegarder et archiver les index de site Web que vous avez générés. Vous pouvez également restaurer la sauvegarde d’un index à tout moment.
solution: Target
subtopic: Rollback
title: A propos de la restauration des index
topic-legacy: Index,Site search and merchandising
uuid: abed878a-71b3-4122-9822-7410f4427a9a
exl-id: bc75f6ba-d919-4dff-8ee2-e17568892626
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# A propos de la restauration des index{#about-rollback-for-indexes}

Vous pouvez utiliser [!DNL Rollback] pour sauvegarder et archiver les index de site Web que vous avez générés. Vous pouvez également restaurer la sauvegarde d’un index à tout moment.

## Utilisation de Rollback pour les index {#concept_0BC4BC975DB045A986C3607CF32705D8}

L&#39;archive contient quatre index : l&#39;index actuel du site et trois index précédents du site, que le robot de recherche archive automatiquement en fonction des paramètres de configuration de restauration. Chaque fois que votre site Web est indexé, l’archive est mise à jour. Les index plus récents remplacent les index archivés existants afin que l&#39;archive reste toujours à jour.

Chaque index archivé est répertorié dans l’archive avec les informations suivantes :

* Date et heure auxquelles l&#39;index a été finalisé.
* Age de l&#39;index.
* Nombre de documents indexés.
* Type d’opération d’indexation (complète, incrémentielle, etc.).
* Statut de l&#39;index, par exemple si l&#39;index est actuellement principal et s&#39;il sera conservé ou supprimé après l&#39;index suivant.

Chaque fois que votre site Web est indexé, le nouvel index est ajouté à l’archive et un index archivé existant est supprimé. Notez toutefois que l’index le plus ancien n’est pas nécessairement celui qui est supprimé. Lorsqu&#39;un nouvel index est ajouté à l&#39;archive, une comparaison de l&#39;âge de chaque index archivé est effectuée avec les âges spécifiés dans les paramètres de configuration de restauration. L’index le plus éloigné de la planification souhaitée est supprimé. Supposons, par exemple, que le paramètre de configuration soit de 24,48,72 et que les index enregistrés aient une âge de 5, 23, 47 et 71. L&#39;index le plus récent (âgé de cinq heures) est supprimé lorsqu&#39;un nouvel index est ajouté à l&#39;archive car son âge est le plus éloigné des paramètres. Pour plus de commodité, l&#39;archive indique quel index est supprimé lorsque le site est de nouveau indexé.

Vous pouvez accéder à d’autres zones de l’interface utilisateur pendant qu’un index est activé. Un indicateur d’état surveille la progression de l’activation et est disponible lorsque vous vue la page [!DNL Rollback]. Si un index archivé est restauré, les utilisateurs sont avertis en haut des pages Index complet, Index incrémentiel, Index par script et Régénérer. Aucune opération d’indexation ne peut se produire pendant la restauration d’un index. Si une opération d&#39;annulation est en conflit avec un index de site planifié, l&#39;indexation planifiée est différée jusqu&#39;à ce que la restauration soit terminée. Si un index est déjà en cours, il est annulé, à condition que l&#39;utilisateur confirme que la restauration est prioritaire.

Pour préserver l&#39;intégrité de l&#39;archive, le robot de recherche ne met pas à jour l&#39;archive de restauration si des erreurs sont détectées lors d&#39;une analyse. Il n’y a pas non plus de mise à jour si un utilisateur annule une opération d’indexation. Si une opération d’indexation dépasse la durée maximale, les octets, les pages ou les documents, l’analyseur finalise l’index et l’ajoute à l’archive. En outre, si le nombre minimum de pages n&#39;est pas atteint lors d&#39;une opération d&#39;indexation, l&#39;analyseur annule l&#39;index et l&#39;index précédent reste principal.

## Configuration du calendrier d&#39;archivage des index de restauration {#task_CD403B9AE2244B13A6B3861B5F9B055C}

Vous pouvez utiliser [!DNL Configure] pour déterminer les fichiers d&#39;index à stocker dans l&#39;archive de restauration. L&#39;archive peut stocker l&#39;index actuel et trois index de sauvegarde.

Le champ **[!UICONTROL Schedule]** contient trois valeurs séparées par des virgules qui représentent les heures écoulées depuis le moment présent. Par exemple, les valeurs de planification 24,48,72 indiquent 24 heures à partir du présent ou d’hier, 48 heures à partir du présent ou il y a deux jours et 72 heures à partir du présent ou il y a trois jours.

La recherche archive continuellement les index du site qui sont les plus proches d&#39;un jour, de deux jours et de trois jours. Les heures et dates réelles des index archivés peuvent varier en fonction du calendrier d’indexation de votre site Web.

**Pour configurer le calendrier d&#39;archivage des index de restauration**

1. Dans le menu produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Configure]**.
1. Sur la page [!DNL Rollback Configuration], dans le champ **[!UICONTROL Schedule]**, entrez une liste séparée par une commande de trois âges d&#39;index, en heures. Les index les plus proches de ces âges sont enregistrés.
1. Cliquez sur **[!UICONTROL Save Changes]**.

## Activation d&#39;un index archivé {#task_5DCE3D660F6F4197993E92AA59227332}

Vous pouvez utiliser la fonction Restauration pour activer un index archivé.

Lorsque vous cliquez sur **[!UICONTROL Activate]** pour restaurer un index, l&#39;index actuellement principal est déplacé dans l&#39;archive.

Après l’activation de l’index archivé, vous êtes renvoyé à la page [!DNL Activate Index]. Des informations sur la restauration de l&#39;index s&#39;affichent. En outre, la colonne [!DNL Activate] de la table [!DNL Available Indexes] identifie l&#39;index restauré avec l&#39;état &quot;Principal Index&quot;.

1. Dans le menu produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Rollback]**.
1. Sur la page [!DNL Activate Index], dans le tableau [!DNL Available Indexes], cliquez sur **[!UICONTROL Activate]** pour le type d&#39;index archivé associé que vous souhaitez rendre principal.

   Utilisez les colonnes Date, Âge, Pages et Opération pour vous aider à déterminer l’index à activer.
1. Sur la page [!DNL Verify Rollback], passez en revue les informations de l&#39;index pour vérifier que vous avez sélectionné l&#39;index correct, puis cliquez sur **[!UICONTROL Activate Now]**.

## Affichage du journal de toutes les restaurations d&#39;index {#task_D2D9AA7203F0465FB5AE0D49212AC41C}

Vue la date et l’heure de toutes les opérations liées à la restauration.

**Pour vue du journal de toutes les restaurations d&#39;index**

1. Dans le menu produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Live Log]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Staged Log]**.

1. Dans la page de journal, en haut ou en bas, effectuez l’une des opérations suivantes :

   * Utilisez les options de navigation **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** pour parcourir le journal.

   * Utilisez les options d&#39;affichage **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** pour affiner ce que vous voyez.
