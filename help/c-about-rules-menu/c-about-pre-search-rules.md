---
description: Utilisez les règles de prérecherche pour analyser la requête entrante et déterminer le modèle de présentation à utiliser. Les règles de prérecherche sont exécutées en séquence pour chaque requête. Pour modifier l’ordre de vos règles, vous pouvez utiliser la fonction glisser-déposer. L’ordre réel ne change pas tant que vous ne l’avez pas enregistré.
seo-description: Utilisez les règles de prérecherche pour analyser la requête entrante et déterminer le modèle de présentation à utiliser. Les règles de prérecherche sont exécutées en séquence pour chaque requête. Pour modifier l’ordre de vos règles, vous pouvez utiliser la fonction glisser-déposer. L’ordre réel ne change pas tant que vous ne l’avez pas enregistré.
seo-title: A propos des règles de pré-recherche
solution: Target
title: A propos des règles de pré-recherche
topic: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# A propos des règles de pré-recherche{#about-pre-search-rules}

Utilisez les règles de prérecherche pour analyser la requête entrante et déterminer le modèle de présentation à utiliser. Les règles de prérecherche sont exécutées en séquence pour chaque requête. Pour modifier l’ordre de vos règles, vous pouvez utiliser la fonction glisser-déposer. L’ordre réel ne change pas tant que vous ne l’avez pas enregistré.

## Utilisation de règles de pré-recherche {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

Les règles de pré-recherche sont généralement utilisées pour sélectionner le modèle de présentation qui affiche les résultats en fonction de la requête entrante. Des fonctions plus avancées peuvent être utilisées pour modifier la requête utilisée pour une recherche effectuée pour un modèle de présentation. Vous pouvez ajouter, supprimer ou modifier la valeur des paramètres de requête, le cas échéant. Pour chaque requête entrante, un module de pré-traitement de recherche examine les règles de pré-recherche pour déterminer si la requête est modifiée et quel modèle de présentation est utilisé. Chaque règle de pré-recherche se compose de deux éléments principaux : actions de la règle et conditions facultatives. Vous pouvez spécifier un nombre illimité de règles et de conditions. L’ordre de ces règles est important, car le jeu de règles est lu en boucle règle par règle. Lorsque les conditions d’une règle correspondent, toutes les actions associées sont exécutées.

Dans le module Traitement avant la recherche, tous les modèles définis et les recherches nommées associées sont appelés, où chaque recherche reçoit une copie locale des paramètres cgi. Par conséquent, vous pouvez personnaliser une recherche en ajoutant, supprimant ou modifiant l&#39;un des paramètres cgi utilisés par la recherche sans modifier une autre recherche nommée utilisée par le modèle ou affecter l&#39;un des autres modèles. Par conséquent, si vous disposez d’un modèle de présentation qui affiche plusieurs jeux de résultats, vous pouvez personnaliser chaque recherche individuellement. Si vous souhaitez effectuer des modifications sur les paramètres CGI globaux avant qu’ils ne soient copiés dans chaque recherche pour chaque modèle, utilisez le module de nettoyage de requête.

## Conditions des règles pré-recherche {#section_B5568ADEB28546A280720309498B045D}

Les conditions sont facultatives. Si vous choisissez de spécifier des actions pour chaque requête, les actions sont toujours exécutées. Il est recommandé que votre première règle s’exécute pour chaque requête, où elle sélectionne votre modèle de présentation par défaut. Ainsi, vous pouvez être assuré que, quelle que soit la requête entrante, vous avez sélectionné un modèle de présentation de scénario le plus défavorable à utiliser. Les conditions peuvent être basées sur n’importe quel paramètre de requête CGI, cookie ou variable personnalisée défini par une règle précédente ou une variable système.

## Actions des règles de pré-recherche {#section_3B8E19D287554C1C969F5B8D81226981}

Toutes les actions d’une règle de pré-recherche qui comporte des conditions correspondantes sont exercées. Les actions consistent généralement en une opération, les données sur lesquelles effectuer l’opération et la valeur à utiliser. L’action la plus simple consiste à spécifier le modèle de présentation à utiliser lorsque la requête correspond aux conditions de la règle de pré-recherche. Définissez ensuite le modèle ciblé sur le nom du modèle de présentation. Des actions plus complexes peuvent être utilisées pour modifier la recherche utilisée pour un modèle donné en exécutant une opération sur le paramètre de recherche d’un modèle. Lors d’une opération sur le paramètre de recherche d’un modèle, vous spécifiez un modèle de présentation et une recherche.

## Règles génériques {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

Lorsque vous effectuez des opérations sur le paramètre de recherche d’un modèle, il existe deux valeurs spéciales : *ciblée et *primaire pour le modèle de présentation et la recherche nommée respectivement. Ces valeurs vous permettent de créer des règles basées sur la recherche principale du modèle ciblé actuel. Ces éléments permettent de créer des règles génériques dans lesquelles vous n’avez pas à vous soucier de l’appellation du modèle ciblé actuel ou de la recherche principale. Il est évident qu’une règle pré-recherche précédente définit ce qu’est le modèle ciblé actuel. Sinon, un modèle de présentation initial est sélectionné pour vous, ce qui produit des résultats non souhaités.

## Exemples {#section_EA153A151987454EA44A4A6862466DF6}

Définissez le modèle par défaut sur guidé.tmpl, lorsque l’utilisateur transmet un paramètre cgi appelé lang, défini sur une langue connue, utilisez le modèle de cette langue.

```
    On condition: 
      Every Query 
    Perform the following actions: 
      Set targeted template to guided 
 
    On condition: 
      Query lang matches regular expression fr 
    Perform the following actions: 
      Set targeted template to guided_french 
 
    On condition: 
      Query lang matches regular expression de 
    Perform the following actions: 
      Set targeted template to guided_german
```

## Bonnes pratiques {#section_31EBAE5E54174DEE8986CBB636746A98}

* La première règle sélectionne un modèle par défaut pour chaque requête.
* L&#39;exploration des données de la requête s&#39;effectue dans les règles de nettoyage de requête. Vous pouvez les référencer dans le traitement de pré-recherche.
* Ajoutez toute nouvelle variable personnalisée que vous avez introduite dans les règles de pré-recherche à une règle de pré-recherche qui est exécutée pour chaque requête avant que d’autres règles de pré-recherche ne les référencent.

## Ajout d’une nouvelle règle de pré-recherche {#task_182B95918462490D8BDA7F16A81CAC11}

Vous pouvez utiliser [!DNL Pre-Search Rules] pour sélectionner le modèle de présentation utilisé pour afficher les résultats de la recherche en fonction de la requête entrante.

**Pour ajouter une nouvelle règle de pré-recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la [!DNL Pre-Search Rules] page, cliquez sur **[!UICONTROL Add New Rule]**.
1. Dans le [!DNL Name] champ, saisissez le nom de la nouvelle règle de nettoyage de requête.
1. Sur la [!DNL Add Pre-Search Rule] page, utilisez les listes déroulantes et les champs de texte pour créer votre requête.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Cookie </p> </td> 
      <td colname="col2"> <p>Un cookie HTTP. Le nom et les valeurs des cookies doivent être codés dans l’identifiant de ressource unique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable personnalisée </p> </td> 
      <td colname="col2"> <p>Variable définie par l’utilisateur. Ajoutez, supprimez ou définissez un nombre illimité de variables définies par l’utilisateur. </p> <p>Vous pouvez référencer toutes les variables que vous avez définies dans le module de nettoyage des requêtes dans les règles de pré-recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable système </p> </td> 
      <td colname="col2"> <p>Variables en lecture seule définies par le système interne que vous pouvez vérifier. Les variables système suivantes sont prises en charge : </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> nom d’hôte </span> <p>Nom de l’hôte du serveur. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>URI requis sans chaîne de requête. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args </span> <p>Chaîne de requête complète. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> environnement </span> <p>"Stage" ou "live" selon que la requête entrante a été envoyée à votre environnement d’évaluation ou de production. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>URL d’où provient le client. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facette </p> </td> 
      <td colname="col2"> <p>Paramètres CGI spéciaux dans la collection globale qui sont associés à une facette particulière. Tous les paramètres CGI sont copiés dans chaque recherche nommée dans un modèle après le nettoyage de requête. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre de requête </p> </td> 
      <td colname="col2"> <p>Paramètre CGI dans la collection globale. Ces paramètres sont copiés dans chaque recherche nommée dans un modèle après le nettoyage de requête. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre de recherche du modèle </p> </td> 
      <td colname="col2"> <p>Paramètre CGI local à une recherche nommée associée à un modèle de présentation. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre principal du modèle </p> </td> 
      <td colname="col2"> <p>Les paramètres de requête entrants sont finalement convertis en paramètres principaux utilisés pour effectuer la recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Paramètres CGI de recherche en arrière-plan </a>. </p> <p>Les paramètres du serveur principal ne s’affichent pas sur les éléments de navigation. Par conséquent, vous pouvez masquer les paramètres supplémentaires que vous souhaitez appliquer à une recherche de vos clients. Le paramètre est local pour une recherche spécifique dans un modèle de présentation. Les actions sur les paramètres principaux sont des liaisons tardives; c' est-à-dire qu' ils sont appliqués juste avant l' envoi de la recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Modèle ciblé </p> </td> 
      <td colname="col2"> <p>Instance spéciale d’une variable personnalisée définie par le système qui ne peut pas être supprimée. Cette variable contient le modèle de présentation ciblé actuel. Vous pouvez lire ou définir cette variable en spécifiant la variable personnalisée "target_template". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classement </p> </td> 
      <td colname="col2"> <p>Permet de spécifier la règle de classement à utiliser dans la recherche. Cette option s’affiche uniquement lorsque vous avez défini des champs de classement et des règles de classement. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Magasin </p> </td> 
      <td colname="col2"> <p>Le moteur de recherche détecte automatiquement dans quel magasin se trouve le client en fonction du nom d'hôte ou du paramètre de <span class="codeph"> </span> requête gs_store, ce dernier paramètre ayant la priorité. Vous pouvez créer des conditions à partir de la boutique. Dans le nettoyage des requêtes uniquement, vous pouvez également utiliser une action pour remplacer la banque actuelle. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dernière règle </p> </td> 
      <td colname="col2"> <p>Lorsqu’il est coché, le module de traitement de pré-recherche n’exécute aucune règle supplémentaire après l’action de la règle correspondante. Cette action est utile lorsque vous avez défini des actions qui provoquent la correspondance d’une règle ultérieure mais que vous ne souhaitez pas que la règle ultérieure s’exécute. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suspendre </p> </td> 
      <td colname="col2"> <p>Désactive l’exécution de la règle mais ne la supprime pas. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Editing a pre-search rule {#task_25F77050C5DA42B29DFD1C9718FB8C64}

Vous pouvez modifier les règles de pré-recherche existantes que vous avez ajoutées à la [!DNL Pre-Search Rules] page.

**Pour modifier une règle de pré-recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la [!DNL Pre-Search Rules] page, sous la **[!UICONTROL Actions]** colonne du tableau, cliquez **[!UICONTROL Edit]** pour la règle associée à modifier.
1. Sur la [!DNL Edit Pre-Search Rule] page, utilisez les listes déroulantes et les champs de texte pour créer votre requête.

   Voir le tableau des options sous [Ajout d’une nouvelle règle](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11)de pré-recherche.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une règle de pré-recherche {#task_128B6A79CA6C451C991AEDAD58F51743}

Vous pouvez supprimer les règles de pré-recherche dont vous n’avez plus besoin ou que vous n’utilisez plus.

Lorsque vous supprimez une règle, l’ordre d’exécution des règles restantes est ajusté automatiquement pour tenir compte de la suppression.

**Pour supprimer une règle de pré-recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la [!DNL Pre-Search Rules] page, sous la **[!UICONTROL Actions]** colonne du tableau, cliquez **[!UICONTROL Delete]** pour la règle associée à supprimer.
1. Dans la [!DNL Confirmation] boîte de dialogue, cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification de l’ordre d’exécution des règles de pré-recherche {#task_C18817276A3C459089C97448076365D1}

Vous pouvez réorganiser les règles de pré-recherche pour modifier l’ordre dans lequel elles s’exécutent sur les modèles de présentation.

Les règles de pré-recherche s’exécutent dans l’ordre dans lequel elles ont été définies. Plus le numéro d’ordre d’une règle est élevé, plus le processus est long, ce qui l’emporte sur les règles antérieures. Vous réorganisez les règles en entrant un nouveau numéro dans la colonne Ordre du tableau de la [!DNL Pre-Search Rules] page. Vous pouvez également faire glisser des règles pour modifier leur ordre d’exécution.

**Pour modifier l&#39;ordre d&#39;exécution des règles de pré-recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la [!DNL Pre-Search Rules] page, effectuez l’une des opérations suivantes :

   * Cliquez sur l’en-tête de **[!UICONTROL Order]** colonne pour trier les règles par ordre croissant ou décroissant.
   * Dans la **[!UICONTROL Order]** colonne, dans le champ de texte à gauche du nom d’une règle de pré-recherche, saisissez le numéro d’ordre à exécuter.
   * Faites glisser une rangée de tableau à l’emplacement où vous souhaitez que la règle s’exécute. Tous les numéros de commande sont mis à jour pour refléter le nouvel ordre dans lequel les règles s’exécutent.

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

