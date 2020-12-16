---
description: Utilisez les règles de pré-recherche pour analyser la requête entrante et déterminer le modèle de présentation à utiliser. Les règles pré-recherche sont exécutées de manière séquentielle pour chaque requête. Pour modifier l’ordre de vos règles, vous pouvez utiliser la fonction glisser-déposer. L'ordre réel ne change pas tant que vous ne l'avez pas enregistré.
seo-description: Utilisez les règles de pré-recherche pour analyser la requête entrante et déterminer le modèle de présentation à utiliser. Les règles pré-recherche sont exécutées de manière séquentielle pour chaque requête. Pour modifier l’ordre de vos règles, vous pouvez utiliser la fonction glisser-déposer. L'ordre réel ne change pas tant que vous ne l'avez pas enregistré.
seo-title: A propos des règles préalables à la recherche
solution: Target
title: A propos des règles préalables à la recherche
topic: Rules,Site search and merchandising
uuid: e75f9d9e-e8ca-4184-bf79-b1fdadb5c0fe
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d
workflow-type: tm+mt
source-wordcount: '1709'
ht-degree: 1%

---


# A propos des règles de pré-recherche{#about-pre-search-rules}

Utilisez les règles de pré-recherche pour analyser la requête entrante et déterminer le modèle de présentation à utiliser. Les règles pré-recherche sont exécutées de manière séquentielle pour chaque requête. Pour modifier l’ordre de vos règles, vous pouvez utiliser la fonction glisser-déposer. L&#39;ordre réel ne change pas tant que vous ne l&#39;avez pas enregistré.

## Utilisation de règles de pré-recherche {#concept_5BF84BB6FACB4645BA9CB7496A01CD1F}

Les règles pré-recherche sont généralement utilisées pour sélectionner le modèle de présentation qui affiche les résultats en fonction de la requête entrante. Des fonctions plus avancées peuvent être utilisées pour modifier la requête utilisée pour une recherche effectuée pour un modèle de présentation. Vous pouvez ajouter, supprimer ou modifier la valeur des paramètres de requête, si nécessaire. Pour chaque requête entrante, un module de prétraitement de recherche examine les règles de pré-recherche pour déterminer si la requête est modifiée et quel modèle de présentation est utilisé. Chaque règle de pré-recherche comprend deux éléments principaux : actions de la règle et conditions facultatives. Vous pouvez spécifier un nombre illimité de règles et de conditions. L’ordre de ces règles est important, car le jeu de règles est bouclé par règle. Lorsque les conditions d’une règle sont respectées, toutes les actions associées sont exécutées.

Dans le module Traitement avant la recherche, tous les modèles définis et leurs recherches nommées associées sont appelés, où chaque recherche reçoit une copie locale des paramètres cgi. Par conséquent, vous pouvez personnaliser une recherche en ajoutant, en supprimant ou en modifiant l&#39;un des paramètres cgi utilisés par la recherche sans modifier aucune autre recherche nommée utilisée par le modèle ou affecter l&#39;un des autres modèles. Par conséquent, si vous disposez d’un modèle de présentation qui affiche plusieurs jeux de résultats, vous pouvez personnaliser chaque recherche individuellement. Si vous souhaitez effectuer des modifications sur les paramètres CGI globaux avant qu’ils ne soient copiés dans chaque recherche pour chaque modèle, utilisez le module de nettoyage de Requête.

## Conditions des règles pré-recherche {#section_B5568ADEB28546A280720309498B045D}

Les conditions sont facultatives. Si vous choisissez de spécifier des actions pour chaque requête, les actions sont toujours effectuées. Il est recommandé que votre première règle s’exécute pour chaque requête, où elle sélectionne votre modèle de présentation par défaut. Ainsi, vous pouvez être assuré que, quelle que soit la requête entrante, vous avez sélectionné un modèle de présentation du scénario le plus défavorable à utiliser. Les conditions peuvent être basées sur tout paramètre de requête CGI, cookie ou variable personnalisée défini par une règle précédente ou une variable système.

## Actions de règle avant recherche {#section_3B8E19D287554C1C969F5B8D81226981}

Toutes les actions d’une règle de pré-recherche qui comporte des conditions correspondantes sont exercées. Les actions se composent généralement d’une opération, des données sur lesquelles l’opération doit être effectuée et de la valeur à utiliser. L’action la plus simple consiste à spécifier le modèle de présentation à utiliser lorsque la requête correspond aux conditions de la règle de pré-recherche. Définissez ensuite le modèle ciblé sur le nom du modèle de présentation. Des actions plus complexes peuvent être utilisées pour modifier la recherche utilisée pour un modèle donné en exécutant une opération sur le paramètre de recherche d’un modèle. Lors d’une opération sur le paramètre de recherche d’un modèle, vous spécifiez un modèle de présentation et une recherche.

## Règles génériques {#section_885ECB9DBF0C4D539C14F82BCAA35B4E}

Lorsque vous effectuez des opérations sur le paramètre de recherche d’un modèle, il existe deux valeurs spéciales : *ciblé et *Principal pour le modèle de présentation et la recherche nommée, respectivement. Ces valeurs vous permettent de créer des règles basées sur la recherche Principale du modèle ciblé actuel. Ces éléments permettent de créer des règles génériques où vous n’avez pas à vous soucier de l’appellation du modèle ciblé actuel ou de la recherche Principale. De toute évidence, une règle pré-recherche précédente définit ce qu’est le modèle ciblé actuel. Dans le cas contraire, un modèle de présentation initial est sélectionné, ce qui produit des résultats indésirables.

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
* L&#39;exploration des données de la requête s&#39;effectue dans le cadre des règles de nettoyage des requêtes. Vous pouvez les référencer dans le traitement de pré-recherche.
* Ajoutez toutes les nouvelles variables personnalisées que vous avez introduites dans les règles de pré-recherche à une règle de pré-recherche exécutée pour chaque requête avant que d’autres règles de pré-recherche ne les référencent.

## Ajouter une nouvelle règle de pré-recherche {#task_182B95918462490D8BDA7F16A81CAC11}

Vous pouvez utiliser [!DNL Pre-Search Rules] pour sélectionner le modèle de présentation à utiliser pour afficher les résultats de recherche en fonction de la requête entrante.

**Pour ajouter une nouvelle règle de pré-recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la page [!DNL Pre-Search Rules], cliquez sur **[!UICONTROL Add New Rule]**.
1. Dans le champ [!DNL Name], saisissez le nom de la nouvelle règle de nettoyage de requête.
1. Sur la page [!DNL Add Pre-Search Rule], utilisez les listes déroulantes et les champs de texte pour élaborer votre requête.

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
      <td colname="col2"> <p>Cookie HTTP. Le nom et les valeurs des cookies doivent être encodés en Uniform Resource Identifier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable personnalisée </p> </td> 
      <td colname="col2"> <p>Variable définie par l’utilisateur. Ajoutez, supprimez ou définissez un nombre illimité de variables définies par l’utilisateur. </p> <p>Vous pouvez référencer toute variable que vous avez définie dans le module Nettoyage de Requêtes dans les règles de pré-recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable système </p> </td> 
      <td colname="col2"> <p>Variables en lecture seule définies par le système interne que vous pouvez vérifier. Les variables système suivantes sont prises en charge : </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> hostname </span> <p>Nom de l’hôte du serveur. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>URI requis sans chaîne de requête. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args  </span> <p>Chaîne de requête entière. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> environnement </span> <p>"Stage" ou "live" selon si la requête entrante a été envoyée à votre environnement de scène ou de production. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>URL d’où provient le client. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facette </p> </td> 
      <td colname="col2"> <p>Paramètres CGI spéciaux dans la collection globale qui sont associés à une facette particulière. Tous les paramètres CGI sont copiés dans chaque recherche nommée dans un modèle après le nettoyage de Requête. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre de requête </p> </td> 
      <td colname="col2"> <p>Paramètre CGI dans la collection globale. Ces paramètres sont copiés dans chaque recherche nommée dans un modèle après le nettoyage de Requête. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre de recherche du modèle </p> </td> 
      <td colname="col2"> <p>Paramètre CGI local à une recherche nommée associée à un modèle de présentation. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre principal du modèle </p> </td> 
      <td colname="col2"> <p>Les paramètres de requête entrants sont finalement convertis en paramètres principaux utilisés pour effectuer la recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Paramètres CGI de la recherche principale </a>. </p> <p>Les paramètres principaux n’apparaissent pas sur les éléments de navigation. Par conséquent, vous pouvez masquer les paramètres supplémentaires que vous souhaitez appliquer à une recherche effectuée auprès de vos clients. Le paramètre est local pour une recherche spécifique dans un modèle de présentation. Les actions sur les paramètres principaux sont des liaisons tardives ; c'est-à-dire qu'elles sont appliquées juste avant l'envoi de la recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Modèle ciblé </p> </td> 
      <td colname="col2"> <p>Instance spéciale d’une variable personnalisée définie par le système qui ne peut pas être supprimée. Cette variable contient le modèle de présentation ciblé actuel. Vous pouvez lire ou définir cette variable en spécifiant la variable personnalisée "target_template". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classement </p> </td> 
      <td colname="col2"> <p>Permet de spécifier la règle de classement à utiliser dans la recherche. Cette option n’apparaît que lorsque vous avez défini les champs de classement et les règles de classement. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Boutique </p> </td> 
      <td colname="col2"> <p>Le moteur de recherche détecte automatiquement dans quel magasin se trouve le client en fonction du nom d'hôte ou du paramètre de requête <span class="codeph"> gs_store </span>, ce dernier paramètre ayant la priorité. Vous pouvez créer des conditions à partir de la boutique. Dans le nettoyage des requêtes uniquement, vous pouvez également utiliser une action pour remplacer la boutique actuelle. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dernière règle </p> </td> 
      <td colname="col2"> <p>Lorsqu'elle est cochée, le module de traitement de pré-recherche n'exécute aucune règle supplémentaire après l'action de la règle correspondante. Cette action est utile lorsque vous avez défini des actions qui provoquent la correspondance d’une règle ultérieure mais que vous ne souhaitez pas que la règle ultérieure s’exécute. </p> </td> 
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

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d&#39;une règle de pré-recherche {#task_25F77050C5DA42B29DFD1C9718FB8C64}

Vous pouvez modifier les règles de pré-recherche existantes que vous avez ajoutées à la page [!DNL Pre-Search Rules].

**Pour modifier une règle de pré-recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la page [!DNL Pre-Search Rules], sous la colonne **[!UICONTROL Actions]** du tableau, cliquez sur **[!UICONTROL Edit]** pour la règle associée à modifier.
1. Sur la page [!DNL Edit Pre-Search Rule], utilisez les listes déroulantes et les champs de texte pour élaborer votre requête.

   Consultez le tableau des options sous [Ajouter une nouvelle règle de pré-recherche](../c-about-rules-menu/c-about-pre-search-rules.md#task_182B95918462490D8BDA7F16A81CAC11).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d&#39;une règle de pré-recherche {#task_128B6A79CA6C451C991AEDAD58F51743}

Vous pouvez supprimer les règles de pré-recherche dont vous n’avez plus besoin ou que vous n’utilisez plus.

Lorsque vous supprimez une règle, l’ordre d’exécution des règles restantes est automatiquement ajusté pour tenir compte de la suppression.

**Pour supprimer une règle de pré-recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la page [!DNL Pre-Search Rules], sous la colonne **[!UICONTROL Actions]** du tableau, cliquez sur **[!UICONTROL Delete]** pour la règle associée à supprimer.
1. Dans la boîte de dialogue [!DNL Confirmation], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification de l’ordre d’exécution des règles de pré-recherche {#task_C18817276A3C459089C97448076365D1}

Vous pouvez réorganiser les règles de pré-recherche pour modifier l’ordre dans lequel elles s’exécutent sur les modèles de présentation.

Les règles de pré-recherche s’exécutent dans l’ordre dans lequel elles ont été définies. Plus le numéro de commande d&#39;une règle est élevé, plus elle s&#39;exécute tard dans le processus, en l&#39;emportant sur les règles antérieures. Vous réorganisez les règles en entrant un nouveau numéro dans la colonne Ordre du tableau de la page [!DNL Pre-Search Rules]. Vous pouvez également utiliser le glisser-déposer sur les règles pour modifier leur ordre d’exécution.

**Pour modifier l&#39;ordre d&#39;exécution des règles de pré-recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la page [!DNL Pre-Search Rules], effectuez l&#39;une des opérations suivantes :

   * Cliquez sur l&#39;en-tête de colonne **[!UICONTROL Order]** pour trier les règles par ordre croissant ou décroissant.
   * Dans la colonne **[!UICONTROL Order]**, dans le champ de texte à gauche du nom d&#39;une règle de pré-recherche, tapez le numéro d&#39;ordre à exécuter.
   * Faites glisser une rangée de tableau à l’emplacement où vous souhaitez que la règle s’exécute. Tous les numéros de commande sont mis à jour pour refléter le nouvel ordre dans lequel les règles s&#39;exécutent.

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

