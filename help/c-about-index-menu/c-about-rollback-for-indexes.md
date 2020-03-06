---
description: Vous pouvez utiliser Rollback pour sauvegarder et archiver les index de site Web que vous avez générés. Vous pouvez également restaurer la sauvegarde d’un index à tout moment.
seo-description: Vous pouvez utiliser Rollback pour sauvegarder et archiver les index de site Web que vous avez générés. Vous pouvez également restaurer la sauvegarde d’un index à tout moment.
seo-title: A propos de la restauration des index
solution: Target
subtopic: Rollback
title: A propos de la restauration des index
topic: Index,Site search and merchandising
uuid: abed878a-71b3-4122-9822-7410f4427a9a
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# A propos de la restauration des index{#about-rollback-for-indexes}

Vous pouvez utiliser [!DNL Rollback] pour sauvegarder et archiver les index de site Web que vous avez générés. Vous pouvez également restaurer la sauvegarde d’un index à tout moment.

## Utilisation de Rollback pour les index {#concept_0BC4BC975DB045A986C3607CF32705D8}

L&#39;archive contient quatre index : l&#39;index actuel du site et trois index précédents du site, que le robot de recherche archive automatiquement en fonction des paramètres de configuration de restauration. Chaque fois que votre site Web est indexé, l’archive est mise à jour. Les index plus récents remplacent les index archivés existants afin que l’archive reste toujours à jour.

Chaque index archivé est répertorié dans l’archive avec les informations suivantes :

* Date et heure auxquelles l&#39;index a été finalisé.
* Age de l&#39;index.
* Nombre de documents indexés.
* Type d’opération d’indexation (complète, incrémentielle, etc.).
* Statut de l’index, par exemple si l’index est actuellement actif et s’il sera conservé ou supprimé après le prochain index.

Chaque fois que votre site Web est indexé, le nouvel index est ajouté à l’archive et un index archivé existant est supprimé. Notez toutefois que l’index le plus ancien n’est pas nécessairement celui qui est supprimé. Lorsqu’un nouvel index est ajouté à l’archive, une comparaison de l’âge de chaque index archivé est effectuée avec les âges spécifiés dans les paramètres de configuration de restauration. L’index le plus éloigné du calendrier souhaité est supprimé. Supposons, par exemple, que le paramètre de configuration soit défini sur 24,48,72 et que les index enregistrés aient une âge de 5, 23, 47 et 71 ans. L’index le plus récent (cinq heures) est supprimé lorsqu’un nouvel index est ajouté à l’archive car son âge est le plus éloigné des paramètres. Par commodité, l&#39;archive indique quel index est supprimé lorsque le site est de nouveau indexé.

Vous pouvez accéder à d’autres zones de l’interface utilisateur lorsqu’un index est activé. Un indicateur d’état suit la progression de l’activation et est disponible lorsque vous affichez la [!DNL Rollback] page. Si un index archivé est restauré, les utilisateurs sont avertis en haut des pages Index complet, Index incrémentiel, Index par script et Régénérer. Aucune opération d’indexation ne peut se produire pendant la restauration d’un index. Si une opération de restauration est en conflit avec un index de site planifié, l’indexation planifiée est différée jusqu’à ce que la restauration soit terminée. Si un index est déjà en cours, il est annulé, à condition que l’utilisateur confirme que la restauration est prioritaire.

Pour préserver l’intégrité de l’archive, le robot de recherche ne met pas à jour l’archive de restauration si des erreurs sont détectées au cours d’une analyse. Il n’y a pas non plus de mise à jour si un utilisateur annule une opération d’indexation. Si une opération d’indexation dépasse la durée maximale, les octets, les pages ou les documents, l’analyseur finalise l’index et l’ajoute à l’archive. En outre, si le nombre minimum de pages n’est pas atteint lors d’une opération d’indexation, l’analyseur annule l’index et l’index précédent reste actif.

## Configuration du calendrier d&#39;archivage des index de restauration {#task_CD403B9AE2244B13A6B3861B5F9B055C}

Vous pouvez utiliser [!DNL Configure] pour déterminer les fichiers d’index à stocker dans l’archive de restauration. L&#39;archive peut stocker l&#39;index actuel et trois index de sauvegarde.

Le **[!UICONTROL Schedule]** champ contient trois valeurs séparées par des virgules qui représentent les heures écoulées depuis le moment présent. Par exemple, les valeurs de planification 24,48,72 indiquent 24 heures à partir du présent ou d’hier, 48 heures à partir du présent ou il y a deux jours et 72 heures à partir du présent ou il y a trois jours.

La recherche archive en permanence les index du site qui sont les plus proches d’un jour, de deux jours et de trois jours. Les heures et les dates réelles des index archivés peuvent varier selon le calendrier d’indexation de votre site Web.

**Pour configurer le calendrier d&#39;archivage de restauration des index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Configure]**.
1. Sur la [!DNL Rollback Configuration] page, dans le **[!UICONTROL Schedule]** champ, entrez une liste séparée par des commandes de trois âges d’index, en heures. Les index les plus proches de ces âges sont enregistrés.
1. Cliquez sur **[!UICONTROL Save Changes]**.

## Activation d’un index archivé {#task_5DCE3D660F6F4197993E92AA59227332}

Vous pouvez utiliser la fonction Restauration pour activer un index archivé.

Lorsque vous cliquez **[!UICONTROL Activate]** pour restaurer un index, l’index actif est déplacé dans l’archive.

Après l’activation de l’index archivé, vous revenez à la [!DNL Activate Index] page. Les informations sur la restauration de l’index s’affichent. En outre, la [!DNL Activate] colonne du [!DNL Available Indexes] tableau identifie l’index restauré avec l’état &quot;Index actif&quot;.

1. Dans le menu du produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Rollback]** > **[!UICONTROL Rollback]**.
1. Sur la [!DNL Activate Index] page, dans le [!DNL Available Indexes] tableau, cliquez sur **[!UICONTROL Activate]** le type d’index archivé associé que vous souhaitez activer.

   Utilisez les colonnes Date, Âge, Pages et Opération pour vous aider à déterminer l’index à activer.
1. Dans la [!DNL Verify Rollback] page, vérifiez les informations de l’index pour vous assurer que vous avez sélectionné l’index correct, puis cliquez sur **[!UICONTROL Activate Now]**.

## Affichage du journal de toutes les restaurations d’index {#task_D2D9AA7203F0465FB5AE0D49212AC41C}

Affichez la date et l’heure de toutes les opérations de restauration.

**Pour afficher le journal de toutes les restaurations d’index**

1. Dans le menu du produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Live Log]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Re-Rank Index]** > **[!UICONTROL Staged Log]**.

1. Dans la page du journal, en haut ou en bas, effectuez l’une des opérations suivantes :

   * Utilisez les options de navigation **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** pour parcourir le journal.

   * Utilisez les options d’affichage **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** pour affiner ce que vous voyez.

