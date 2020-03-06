---
description: L’évaluation vous permet de tester et de prévisualiser les modifications apportées à vos paramètres et configurations sans affecter votre index dynamique.
seo-description: L’évaluation vous permet de tester et de prévisualiser les modifications apportées à vos paramètres et configurations sans affecter votre index dynamique.
seo-title: A propos de l’évaluation
solution: Target
title: A propos de l’évaluation
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# A propos de l’évaluation{#about-staging}

L’évaluation vous permet de tester et de prévisualiser les modifications apportées à vos paramètres et configurations sans affecter votre index dynamique.

## A propos de l’évaluation {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

L’évaluation vous permet de tester et de prévisualiser les modifications apportées à vos paramètres et configurations sans affecter votre index dynamique.

Voir aussi ID [d’élément : context_A5783D07C72042EC8886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Toute page qui comporte des options d’évaluation **[!UICONTROL Push All Live]** ou **[!UICONTROL View Live Settings]** signifie que tous les paramètres de cette page peuvent être mis en scène. Les exceptions sont les pages Web dans Index. Les pages de cette zone sont soit explicitement destinées à l’index intermédiaire, soit à l’index dynamique pour vous permettre de contrôler directement les deux index indépendamment.

Vous pouvez organiser presque tout, y compris votre index. Certaines exceptions incluent des paramètres spécifiques au compte qui affectent à la fois votre environnement de production et votre environnement de production simultanément, ainsi que la planification des opérations d’indexation. Par défaut, lorsque vous enregistrez des modifications dans un paramètre pouvant être mis en scène, elles sont automatiquement mises en scène.

Lorsque les **[!UICONTROL Push All Live]** options ou **[!UICONTROL View Lives Settings]** les options ne sont pas activées (grisées), cela signifie que les paramètres intermédiaires de cette page sont les mêmes que les paramètres actifs.

Pour un élément qui est mis en scène, notez que la version en direct des paramètres est en lecture seule ; il ne peut être manipulé qu&#39;en mettant en oeuvre les paramètres intermédiaires.

## A propos de l’historique sur les pages d’évaluation {#section_5BE780AFF26A450A9EFF4000DE53531B}

La plupart des paramètres d’évaluation comportent une [!DNL History] option dans l’angle supérieur droit de la page. Lorsque vous cliquez sur **[!UICONTROL History]**, vous pouvez rétablir les modifications que vous avez récemment apportées à la page intermédiaire que vous avez ouverte.

Vous pouvez également afficher le journal des modifications pour obtenir une autre vue de l’historique. Chaque fois qu’une modification est appliquée, une version de sauvegarde du fichier de données sous-jacent est créée. Le journal des modifications présente chaque révision, indiquant le numéro de version, l’adresse électronique de l’utilisateur qui a effectué les modifications et la date à laquelle la sauvegarde a été effectuée. L’entrée avec une valeur de version en gras représente la version actuelle.

See [Viewing the Change Log](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## La page Gérer les paramètres de Live Stage {#section_E72B8CAF516345A5B6B6783CF6E512EE}

En plus d’offrir les options **[!UICONTROL Push All Live]** et **[!UICONTROL View Live Settings]** directement depuis une page donnée, vous pouvez également utiliser la **[!UICONTROL Manage Stage-Live Settings]** page pour faire la même chose. La **[!UICONTROL Manage Stage-Live Settings]** page, disponible à partir du menu principal du produit, est un emplacement central qui vous montre tous les paramètres de votre compte actuellement mis en scène. Vous pouvez activer tous les paramètres, activer uniquement les paramètres sélectionnés ou supprimer des paramètres. Il est toutefois recommandé de toujours diffuser tous les éléments de scène en direct afin d’éviter tout problème d’interdépendance.

Les paramètres de la page sont regroupés en catégories. Vous pouvez développer chaque catégorie afin d’afficher les paramètres de page qui sont mis en scène. Actuellement, les dépendances ne sont pas suivies dans le gestionnaire d’étapes. Par conséquent, il est recommandé de tout mettre en ligne en même temps, à l’exception de l’index.

Vous pouvez publier un index par étape. Assurez-vous d’abord de vérifier que l’index par étape n’est pas obsolète ou corrompu. Si vous commettez une erreur et que vous mettez en ligne l’index intermédiaire, vous pouvez restaurer un ancien index dynamique. La publication d’un index par étapes prend généralement moins de 30 secondes.

## Test d’un paramètre ou d’un index par étapes {#section_6800E52D20854A779946EAB600801F12}

Sur les pages qui prennent en charge un contrôle de test, vous pouvez le tester par rapport aux paramètres d’évaluation ou de production. Lorsque vous affichez les paramètres d’évaluation, le paramètre d’évaluation est utilisé pour le test. De même, lorsque vous affichez le paramètre en direct, le test utilise les paramètres en direct. Dans la section templates, tous les tests sont effectués par rapport à la version intermédiaire de l’index. Pour rechercher un index par étapes, définissez le paramètre `sp_staged` CGI sur 1. Cela indique à son tour que vous souhaitez utiliser l’index intermédiaire. Si aucun index intermédiaire n’existe, votre index dynamique est recherché et les paramètres de temps de recherche par étapes sont appliqués selon les besoins.

Voir aussi Paramètres [CGI de recherche](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal.

## Affichage des paramètres en direct {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

Vous pouvez consulter la version en direct des paramètres de n’importe quelle page intermédiaire.

<!-- 

t_viewing_live_settings.xml

 -->

Si l’ **[!UICONTROL View Live Settings]** option n’est pas activée (grisée), cela signifie que les paramètres d’affichage de cette page et les paramètres d’activation sont déjà synchronisés.

**Pour afficher les paramètres en direct**

1. Sur une page comportant des paramètres d’évaluation, cliquez sur **[!UICONTROL View Live Settings]** pour afficher la version en direct des paramètres.
1. Vous pouvez également effectuer l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL View]** pour afficher les options actuellement sélectionnées pour le paramètre d’évaluation.
   * Cliquez sur **[!UICONTROL View Stage Settings]** pour revenir au paramètre par étape où vous pouvez le modifier ou le supprimer.

## Activation des paramètres d’affichage {#task_44306783B4C0408AAA58B471DAF2D9A4}

Vous pouvez transmettre les paramètres en direct depuis n’importe quelle page vue intermédiaire ou depuis la **[!UICONTROL Manage Stage-Live Settings]** page centrale.

<!-- 

t_pushing_live_settings_live.xml

 -->

Lorsque l’ **[!UICONTROL Push Live]** option est activée (non grisée) sur une page, cela signifie qu’un paramètre est mis en scène. Cela signifie également qu’un paramètre comporte des modifications et que, lorsque vous l’enregistrez, le paramètre est mis en scène. Lorsque vous cliquez sur cette option, toutes les modifications non enregistrées sont enregistrées dans la zone d’évaluation. S’il n’y a aucune modification en attente, les paramètres de la page sont immédiatement activés.

**Pour diffuser les paramètres par étapes en direct**

1. Effectuez l’une des opérations suivantes :

   * Sur une page pour laquelle l’option &quot;Etape&quot; est sélectionnée comme vue, cliquez sur **[!UICONTROL Push Live]**.
   * Dans le menu du produit, cliquez sur **[!UICONTROL Staging]**. Sur la **[!UICONTROL Manage Stage-Live Settings]** page, effectuez l’une des opérations suivantes :

   * Utilisez l’arborescence des paramètres pour vérifier uniquement les paramètres que vous souhaitez publier, puis cliquez sur **[!UICONTROL Push Selected Live]**.
   * Cliquez sur **[!UICONTROL Push All Live]**.

## Suppression des paramètres stage-live d’un emplacement central {#task_B72BEA9269704B1399600A9CA273369B}

Si vous avez de nombreux paramètres à supprimer, vous pouvez utiliser la **[!UICONTROL Manage Stage-Live Settings]** page pour supprimer des paramètres d’un emplacement central.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Avertissement**: Lorsque vous cliquez **[!UICONTROL Delete Selected]**, tous les paramètres cochés sont immédiatement supprimés. il n’existe pas de boîte de dialogue de confirmation pour vérifier que vous souhaitez vraiment supprimer les paramètres sélectionnés. En outre, aucune fonctionnalité d’historique n’est associée à la page. Par conséquent, vous ne pouvez pas annuler votre suppression.

**Pour supprimer des paramètres d’affichage en direct d’un emplacement central**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Staging]**.
1. Sur la **[!UICONTROL Manage Stage-Live Settings]** page, utilisez l’arborescence des paramètres pour vérifier uniquement les paramètres que vous souhaitez supprimer.
1. Cliquez sur **[!UICONTROL Delete Selected]**.
