---
description: Affichages de données affiche les résultats de la recherche avec les champs de métadonnées. Chaque colonne est un champ de métadonnées et chaque ligne résulte d'une requête de recherche. Personnalisez les vues des données en choisissant et en réorganisant les colonnes. Les vues de données peuvent également comporter des titres et des descriptions personnalisés.
seo-description: Affichages de données affiche les résultats de la recherche avec les champs de métadonnées. Chaque colonne est un champ de métadonnées et chaque ligne résulte d'une requête de recherche. Personnalisez les vues des données en choisissant et en réorganisant les colonnes. Les vues de données peuvent également comporter des titres et des descriptions personnalisés.
seo-title: A propos des vues de données
solution: Target
title: A propos des vues de données
topic: Reports,Site search and merchandising
uuid: 18930551-960d-40c2-b5b7-0807a2e11134
translation-type: tm+mt
source-git-commit: 7af85dd37f06fe506e5f57e28a25385ca7ab3db5

---


# A propos des vues de données{#about-data-views}

Affichages de données affiche les résultats de la recherche avec les champs de métadonnées. Chaque colonne est un champ de métadonnées et chaque ligne résulte d&#39;une requête de recherche. Personnalisez les vues des données en choisissant et en réorganisant les colonnes. Les vues de données peuvent également comporter des titres et des descriptions personnalisés.

## Utilisation des vues de données {#concept_DCA897D074464BC1861AA47B40CC86C3}

Chaque compte permet de créer plusieurs vues de données. Utilisez la page Vues de données pour créer et modifier ces vues de données.

Après avoir ajouté une vue de données, vous devez la modifier pour configurer et personnaliser la vue.

Voir [Modification d’une vue](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de données.

Vous pouvez copier une vue de données existante à utiliser comme base pour créer une vue de données.

Voir [Copie d’une vue](../c-about-reports-menu/c-about-data-views.md#task_78D4C2799BC84677843ED4CA1CD205AF)de données.

## Ajout d’une vue de données {#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D}

Vous pouvez ajouter une vue de données à la [!DNL Data Views] page pour afficher les valeurs de chaque champ de métadonnées avec une requête de recherche.

Après avoir ajouté une vue de données, vous devez la modifier pour configurer et personnaliser la vue.

Voir [Modification d’une vue](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de données.

**Pour ajouter une vue de données**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Sur la [!DNL Data Views] page, cliquez sur **[!UICONTROL Add New Data View]**.
1. Dans la boîte de [!DNL Add New Data View] dialogue, dans le [!DNL Title] champ, saisissez le nom de la vue de données à créer.
1. Cliquez sur **[!UICONTROL Add]**.

## Modification d’une vue de données {#task_258A367896C24DD498C755925EA8F516}

Lorsque vous ajoutez une vue de données à la [!DNL Data Views] page, vous utilisez Modifier pour modifier le nom et la description de la vue de données ou pour déplacer, afficher ou masquer l’affichage de chaque champ de métadonnées.

Vous pouvez également verrouiller ou déverrouiller une vue de données sélectionnée.

Voir [Ajout d’une vue](../c-about-reports-menu/c-about-data-views.md#task_A20FEB2E1CA1444D816D2F5F4B6E5B2D)de données.

**Pour modifier une vue de données**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Sur la [!DNL Data Views] page, dans la [!DNL Actions] colonne du tableau, cliquez **[!UICONTROL Edit]** dans la ligne avec l’affichage des données à modifier.
1. Sur la [!DNL Data Views Editor] page, définissez les options de votre choix.

   L’éditeur d’affichage des données dispose de toutes les commandes permettant de masquer, d’afficher et de déplacer les colonnes de champ sur la page d’affichage des données.

   Lorsque vous affichez une vue de données, le tableau résultant affiche également les champs de colonne supplémentaires suivants qui ne sont pas modifiables : Classement, pertinence et score (global). Ces trois champs spéciaux représentent les scores de pertinence, les scores de classement et les scores globaux pour chaque résultat.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Titre </p> </td> 
      <td colname="col2"> <p>Nom de la vue de données. Le nom s’affiche en haut à droite lorsque vous affichez l’affichage des données. </p> <p>Voir <a href="../c-about-reports-menu/c-about-data-views.md#task_FD0D2CE53DF84CBD9220AD7CA920011F" type="task" format="dita" scope="local"> Affichage d’une vue</a>de données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Description </p> </td> 
      <td colname="col2"> <p>(Facultatif) Contient une description de l’affichage des données. La description s’affiche entre le nom du titre de la vue de données et le champ de texte <span class="wintitle"> Nouvelle recherche</span> . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètres de recherche </p> </td> 
      <td colname="col2"> <p>Permet de spécifier les paramètres de recherche par défaut. Lorsque la vue des données est affichée pour la première fois, ces paramètres CGI sont automatiquement ajoutés. </p> <p>Ne modifiez ni ne supprimez <span class="codeph"> sp_cs</span> ou <span class="codeph"> sp_f</span>. Ces paramètres sont essentiels pour la vue des données, quel que soit le jeu de caractères préféré du compte. </p> <p>Voir Paramètres <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"></a>CGI de recherche principal. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Verrouiller l’état </p> </td> 
      <td colname="col2"> <p>Permet de verrouiller ou de déverrouiller l’affichage des données. </p> <p>Vous pouvez afficher une vue de données verrouillée uniquement avec un mot de passe et un nom d’utilisateur. L’utilisateur doit être membre actuel du compte. </p> <p>Une vue de données déverrouillée est accessible sans mot de passe ni compte utilisateur. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Commande </p> </td> 
      <td colname="col2"> <p> Permet de modifier l’ordre des colonnes en modifiant le nombre dans la zone de texte <span class="wintitle"> Ordre</span> . Vous pouvez également faire glisser une rangée pour modifier l’ordre des colonnes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure </p> </td> 
      <td colname="col2"> <p> Permet d’activer ou de désactiver l’affichage de la colonne. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afficher l’URL sous forme d’image </p> </td> 
      <td colname="col2"> <p>Affichez des miniatures et des images dans cette colonne si le résultat de la recherche pour cette colonne renvoie une URL. </p> <p>L’URL est dépouillée de son nom ou protocole de schéma avant de devenir une valeur de l’attribut <span class="codeph"> src</span> d’une balise d’image. </p> <p>Si le résultat de la recherche renvoyée ne ressemble pas à une URL d’une image, un message s’affiche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longueur de champ </p> </td> 
      <td colname="col2"> <p>Définit le nombre de caractères affichés en conséquence sur l’affichage des données. </p> <p>La valeur par défaut est de 100 caractères. </p> <p>Certains champs, tels que le score de classement et le champ de date, n’ont pas de longueur de champ ajustable. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copie d’une vue de données {#task_78D4C2799BC84677843ED4CA1CD205AF}

Vous pouvez copier une vue de données existante sur la [!DNL Data Views] page à utiliser comme base pour créer une vue de données.

Après avoir copié une vue de données, vous pouvez la personnaliser davantage en la modifiant.

Voir [Modification d’une vue](../c-about-reports-menu/c-about-data-views.md#task_258A367896C24DD498C755925EA8F516)de données.

**Pour copier une vue de données**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Sur la [!DNL Data Views] page, dans la [!DNL Actions] colonne du tableau, cliquez **[!UICONTROL Copy]** dans la ligne avec l’affichage des données à copier.
1. Sur la [!DNL Copy Data View] page, dans le champ de [!DNL New Title] texte, saisissez le nouveau nom que vous souhaitez attribuer à l’affichage des données.
1. Cliquez sur **[!UICONTROL Copy]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une vue de données {#task_61C32F8F00A549A5A3E7EDDA6F537098}

Vous pouvez supprimer une vue de données sur la [!DNL Data Views] page dont vous n’avez plus besoin ou que vous n’utilisez plus.

**Pour supprimer une vue de données**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Sur la [!DNL Data Views] page, dans la [!DNL Actions] colonne du tableau, cliquez **[!UICONTROL Delete]** dans la ligne avec l’affichage des données à supprimer.
1. Sur la [!DNL Delete Data View] page, cliquez sur **Supprimer**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Affichage d’une vue de données {#task_FD0D2CE53DF84CBD9220AD7CA920011F}

Vous pouvez utiliser [!DNL View] sur la [!DNL Data Views] page pour afficher une vue de données sélectionnée.

La vue de données que vous sélectionnez s’ouvre dans une fenêtre de navigateur distincte.

**Pour afficher une vue de données**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Data Views]**.
1. Utilisez l’une des méthodes suivantes :

   * Sur la [!DNL Data Views] page, dans la [!DNL Title] colonne du tableau, cliquez sur le nom d’une vue de données à ouvrir.

   * Sur la [!DNL Data Views] page, dans la [!DNL Actions] colonne du tableau, cliquez **[!UICONTROL View]** sur la ligne contenant l’affichage des données à ouvrir.

