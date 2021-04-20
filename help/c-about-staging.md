---
description: L’évaluation vous permet de tester et de prévisualisation les modifications apportées à vos paramètres et configurations sans affecter votre index dynamique.
solution: Target
title: A propos de la mise en scène
topic: Staging,Site search and merchandising
uuid: 2e5889a6-2e9c-4ac7-9d6e-d35e7cafda5b
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 0%

---


# À propos de l’évaluation{#about-staging}

L’évaluation vous permet de tester et de prévisualisation les modifications apportées à vos paramètres et configurations sans affecter votre index dynamique.

## À propos de l’évaluation {#concept_08B8F3CA1F4241108F14BA7FC7806CA7}

L’évaluation vous permet de tester et de prévisualisation les modifications apportées à vos paramètres et configurations sans affecter votre index dynamique.

Voir aussi [ID d’élément : context_A5783D07C72042EC8886F300FFF62C50](c-about-simulator.md#context_A5783D07C72042EC8886F300FFF62C50).

Toute page présentant les options d’évaluation **[!UICONTROL Push All Live]** ou **[!UICONTROL View Live Settings]** signifie que tous les paramètres de cette page peuvent être intermédiaires. Les exceptions sont les pages Web dans Index. Les pages de cette zone sont explicitement destinées à l&#39;index intermédiaire ou à l&#39;index actif pour vous permettre de contrôler directement les deux index indépendamment.

Vous pouvez organiser pratiquement tout ce qui inclut votre index. Certaines exceptions incluent des paramètres spécifiques au compte qui affectent à la fois votre environnement de production et d&#39;évaluation simultanément et la planification des opérations d&#39;indexation. Par défaut, lorsque vous enregistrez des modifications dans un paramètre pouvant être mis en scène, elles sont automatiquement mises en scène.

Lorsque les options **[!UICONTROL Push All Live]** ou **[!UICONTROL View Lives Settings]** ne sont pas activées (grisées), cela signifie que les paramètres intermédiaires de cette page sont identiques aux paramètres actifs.

Pour un élément qui est mis en scène, notez que la version active des paramètres est en lecture seule ; il ne peut être manipulé qu&#39;en repoussant les paramètres mis en scène.

## A propos de l&#39;historique sur les pages intermédiaires {#section_5BE780AFF26A450A9EFF4000DE53531B}

La plupart des paramètres d’évaluation comportent une option [!DNL History] dans l’angle supérieur droit de la page. Lorsque vous cliquez sur **[!UICONTROL History]**, il vous permet de rétablir toutes les modifications que vous avez apportées récemment à la page intermédiaire particulière que vous avez ouverte.

Vous pouvez également vue le journal des modifications pour une autre vue de l&#39;historique. Chaque fois qu’une modification est appliquée, une version de sauvegarde du fichier de données sous-jacent est créée. Le journal des modifications présente chaque révision, indiquant le numéro de version, l&#39;adresse électronique de l&#39;utilisateur qui a effectué les modifications et la date à laquelle la sauvegarde a été effectuée. L’entrée avec une valeur de version en gras représente la version actuelle.

Voir [Affichage du journal des modifications](c-about-reports-menu/c-about-reports-menu.md#task_166F1156719F4B3D834BEA8E249C8057).

## La page Gérer les paramètres Stage-Live {#section_E72B8CAF516345A5B6B6783CF6E512EE}

Outre l&#39;offre des options **[!UICONTROL Push All Live]** et **[!UICONTROL View Live Settings]** directement depuis une page donnée, vous pouvez également utiliser la page **[!UICONTROL Manage Stage-Live Settings]** pour faire la même chose. La page **[!UICONTROL Manage Stage-Live Settings]**, disponible à partir du menu de produit principal, est un emplacement central qui vous montre tous les paramètres de votre compte actuellement mis en scène. Vous pouvez activer tous les paramètres, activer uniquement les paramètres sélectionnés ou supprimer les paramètres. Il est toutefois recommandé de toujours diffuser en direct tous les éléments de test afin d’éviter tout problème d’interdépendance.

Les paramètres de la page sont regroupés en catégories. Vous pouvez développer chaque catégorie afin d’afficher les paramètres de la page qui sont mis en scène. Actuellement, les dépendances ne sont pas suivies dans le gestionnaire d’étapes. Par conséquent, il est recommandé de tout publier en une seule fois, à l’exception de l’index.

Vous pouvez diffuser un index intermédiaire en direct. Assurez-vous d’abord de vérifier que votre index par étapes n’est pas obsolète ou corrompu. Si vous commettez une erreur et repoussez l&#39;index en direct, vous pouvez restaurer un ancien index en direct. La publication d’un index par étapes prend généralement moins de 30 secondes.

## Test d&#39;un paramètre ou d&#39;un index par étapes {#section_6800E52D20854A779946EAB600801F12}

Sur les pages qui prennent en charge un contrôle de test, vous pouvez effectuer un test par rapport aux paramètres d’évaluation ou de production. Lorsque vous vue les paramètres intermédiaires, le paramètre intermédiaire est utilisé pour le test. De même, lorsque vous affichez le paramètre en direct, le test utilise les paramètres en direct. Dans la section modèles, tous les tests sont effectués par rapport à la version intermédiaire de l’index. Pour effectuer une recherche dans un index intermédiaire, définissez le paramètre CGI `sp_staged` égal à 1. Cela indique à son tour que vous souhaitez utiliser l’index intermédiaire. Si aucun index intermédiaire n’existe, votre index actif fait l’objet d’une recherche et tous les paramètres de temps de recherche intermédiaire sont appliqués comme il convient.

Voir aussi [Paramètres CGI de recherche dorsale](c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Affichage des paramètres en direct {#task_401A0EBDB5DB4D4CA933CBA7BECDC10F}

Vous pouvez consulter la version en direct des paramètres de n’importe quelle page intermédiaire.

<!-- 

t_viewing_live_settings.xml

 -->

Si l&#39;option **[!UICONTROL View Live Settings]** n&#39;est pas activée (grisée), cela signifie que les paramètres d&#39;affichage de cette page et les paramètres d&#39;activation sont déjà synchronisés.

**Pour vue des paramètres en direct**

1. Sur toute page comportant des paramètres d’évaluation, cliquez sur **[!UICONTROL View Live Settings]** pour afficher la version en ligne des paramètres.
1. Vous pouvez également effectuer l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL View]** pour afficher les options actuellement sélectionnées pour le paramètre intermédiaire.
   * Cliquez sur **[!UICONTROL View Stage Settings]** pour revenir au paramètre intermédiaire dans lequel vous pouvez modifier ou supprimer le paramètre.

## Activation des paramètres d’étape {#task_44306783B4C0408AAA58B471DAF2D9A4}

Vous pouvez transmettre les paramètres en direct à partir de n’importe quelle vue de page intermédiaire ou de la page centrale **[!UICONTROL Manage Stage-Live Settings]**.

<!-- 

t_pushing_live_settings_live.xml

 -->

Lorsque l&#39;option **[!UICONTROL Push Live]** est activée (non grisée) sur une page, cela signifie qu&#39;un paramètre est mis en scène. Cela signifie également qu’un paramètre comporte des modifications et que, lors de l’enregistrement, le paramètre est mis en scène. Lorsque vous cliquez sur cette option, toutes les modifications non enregistrées sont enregistrées dans la zone d’évaluation. S’il n’y a aucune modification en attente, les paramètres de la page sont immédiatement répercutés.

**Pour diffuser les paramètres par étapes en direct**

1. Effectuez l’une des opérations suivantes :

   * Sur toute page où l’option &quot;Mise en scène&quot; a été sélectionnée comme Vue, cliquez sur **[!UICONTROL Push Live]**.
   * Dans le menu produit, cliquez sur **[!UICONTROL Staging]**. Sur la page **[!UICONTROL Manage Stage-Live Settings]**, effectuez l&#39;une des opérations suivantes :

   * Utilisez l&#39;arborescence des paramètres pour vérifier uniquement les paramètres à publier, puis cliquez sur **[!UICONTROL Push Selected Live]**.
   * Cliquez sur **[!UICONTROL Push All Live]**.

## Suppression des paramètres stage-live d’un emplacement central {#task_B72BEA9269704B1399600A9CA273369B}

Si vous avez de nombreux paramètres à supprimer, vous pouvez utiliser la page **[!UICONTROL Manage Stage-Live Settings]** pour supprimer des paramètres d&#39;un emplacement central.

<!-- 

t_deleting_staged_settings_from_a_central_location.xml

 -->

**Avertissement** : Lorsque vous cliquez sur  **[!UICONTROL Delete Selected]**, tous les paramètres cochés sont immédiatement supprimés ; il n&#39;existe pas de boîte de dialogue de confirmation pour vérifier que vous souhaitez vraiment supprimer les paramètres sélectionnés. En outre, aucune fonction d’historique n’est associée à la page. Par conséquent, vous ne pouvez pas annuler votre suppression.

**Pour supprimer des paramètres d’évaluation en direct d’un emplacement central**

1. Dans le menu produit, cliquez sur **[!UICONTROL Staging]**.
1. Sur la page **[!UICONTROL Manage Stage-Live Settings]**, utilisez l&#39;arborescence des paramètres pour vérifier uniquement les paramètres que vous souhaitez supprimer.
1. Cliquez sur **[!UICONTROL Delete Selected]**.
