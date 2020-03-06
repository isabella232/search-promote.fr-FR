---
description: Vous pouvez utiliser les règles de post-recherche pour examiner les résultats d’une recherche et déterminer l’impact de la recherche sur le contenu affiché.
seo-description: Vous pouvez utiliser les règles de post-recherche pour examiner les résultats d’une recherche et déterminer l’impact de la recherche sur le contenu affiché.
seo-title: A propos des règles de post-recherche
solution: Target
title: A propos des règles de post-recherche
topic: Rules,Site search and merchandising
uuid: 312d1e4a-f5b6-4629-8645-17e6f6c09fc4
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d

---


# A propos des règles de post-recherche{#about-post-search-rules}

Vous pouvez utiliser les règles de post-recherche pour examiner les résultats d’une recherche et déterminer l’impact de la recherche sur le contenu affiché.

## Utilisation des règles de post-recherche {#concept_AF6ADFCC0ADF4A788003964939917FDE}

Si une recherche n’a aucun résultat, une règle de post-recherche peut effectuer une recherche pour un élément similaire. Il peut également afficher une page Web qui recommande d’autres éléments aux clients qui recherchent l’élément introuvable.

Chaque règle de post-recherche se compose de deux éléments principaux : les actions de la règle et ses conditions facultatives. Vous pouvez spécifier un nombre illimité de règles et de conditions. L’ordre de ces règles est important car le jeu de règles est bouclé par règle. Lorsque les conditions d’une règle correspondent, toutes les actions associées sont exécutées.

Vous pouvez affiner l&#39;ensemble des résultats de la recherche pour un maximum de trois tours de recherche. Ensuite, tout ce qui est actuellement disponible est utilisé. Cette limite empêche des boucles infinies et garantit une réponse efficace du client. Plus vous refaites une recherche, plus il faut de temps pour renvoyer les résultats. Si aucune des règles de correspondance ne modifie l’une des recherches pour le modèle de présentation actuellement utilisé ou ne change de modèle, l’ensemble des résultats de recherche est considéré comme finalisé et les résultats de la recherche sont supprimés.

Le traitement post-recherche s’appuie sur les modules de traitement antérieurs Nettoyage des requêtes et Prérecherche. Par conséquent, toutes les variables personnalisées définies dans ces modules peuvent être utilisées dans les règles de traitement post-recherche. De même, le traitement de pré-recherche a instancié tous les modèles dans lesquels chaque recherche nommée associée au modèle de présentation possède sa propre copie locale des paramètres CGI. Vous pouvez ensuite personnaliser chaque recherche individuellement.

Voir [A propos des règles](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C)de nettoyage de requête.

See [About Pre-Search Rules](../c-about-rules-menu/c-about-pre-search-rules.md#concept_5BF84BB6FACB4645BA9CB7496A01CD1F).

## A propos des conditions des règles après la recherche {#section_C43EB77CC0AC43B8B9D38569264BF1B5}

Les conditions sont facultatives. Si vous spécifiez que les actions sont spécifiées pour chaque requête, les actions sont toujours exécutées. Vous pouvez baser les conditions sur n’importe quel paramètre de requête CGI, cookie, résultat de recherche ou variable personnalisée défini par une règle précédente. Vous pouvez également le baser sur une condition système telle que le modèle actuellement sélectionné ou s’il s’agit de la dernière recherche. Lorsque vous créez une condition sur les résultats d’une recherche ou d’un paramètre CGI, vous indiquez le modèle et le nom de la recherche.

## A propos des actions des règles après la recherche {#section_0E15FE683A894ECAAA386267EEC7F7C5}

Toutes les actions d’une règle de post-recherche qui comportent des conditions de correspondance sont exercées. Les actions consistent généralement en une opération, les données sur lesquelles effectuer l’opération et la valeur à utiliser. L’action la plus simple consiste à changer le modèle de présentation à utiliser en fonction des conditions de la règle de post-recherche. Vous pouvez utiliser des actions plus avancées pour modifier les paramètres d’une recherche qui entraîne le rétablissement de la recherche. Lors d’une opération sur le paramètre de recherche d’un modèle, spécifiez un modèle de présentation et effectuez une recherche.

## Règles générales {#section_AEE923988CC748FF9DEF2233FBF333B5}

Lorsque vous effectuez des opérations sur le paramètre de recherche d’un modèle, il existe deux valeurs spéciales : *ciblé et *principal pour le modèle de présentation et la recherche nommée respectivement. Utilisez ces valeurs pour créer des règles basées sur la recherche principale du modèle ciblé actuel. Ces éléments vous permettent de créer des règles génériques dans lesquelles vous n’avez pas à vous soucier de l’appellation du modèle ciblé actuel ou de la recherche principale. Si cette passe est la première par le biais du traitement post-recherche, le modèle ciblé est tout ce que le traitement pré-recherche lui attribue.

## Redirections {#section_E5669A2F13C240F2968E31C75591CD6A}

Les accès directs et les redirections dans le nettoyage des requêtes vous permettent de rediriger vers une URL en fonction des termes de recherche entrants. Les redirections dans les règles de post-recherche étendent cette idée, sauf qu&#39;elles vous permettent de vérifier le nombre de résultats renvoyés par la recherche avant de décider si vous souhaitez qu&#39;une redirection se produise. Avec les règles de post-recherche, vous pouvez rediriger vers une URL, où vous pouvez remplacer des variables personnalisées ou des paramètres de requête. Vous pouvez également rediriger vers un champ du premier résultat. Lorsque vous redirigez vers le champ d’un résultat, vous définissez le champ dans le modèle de transport et il doit contenir une URL explicite valide, sinon la redirection est ignorée.

Lorsque vous utilisez le mécanisme de redirection dans les règles de post-recherche, vous pouvez détecter le moment où une recherche renvoie un seul résultat. Plutôt que de renvoyer un tel résultat, vous pouvez rediriger vers la page Web associée au résultat.

Voir l’exemple de redirection ci-dessous pour un exemple d’utilisation des redirections avec les règles de post-recherche.

## Dernière règle {#section_FC1E0050C9324278B171038E98F6C335}

Lorsque les conditions sont remplies pour une règle dont l’option **[!UICONTROL Last Rule]** est définie, le module de traitement post-recherche n’exécute aucune règle supplémentaire après l’action de la règle correspondante. Cette situation est utile lorsque vous avez défini des actions qui provoquent la correspondance d’une règle ultérieure mais que vous souhaitez que le traitement s’arrête. Et, pour que cette règle ultérieure corresponde potentiellement après le prochain tour de recherche.

## Exemples {#section_DDB98383690941F9B44AD00FBA55BB56}

Dans l’exemple suivant, supposons que vous disposez de deux modèles de présentation. Un modèle est utilisé pour afficher de nombreux résultats de recherche et l&#39;autre modèle est utilisé pour afficher un seul résultat et une recherche supplémentaire d&#39;accessoires liés à la recherche principale. Vous souhaitez détecter le moment où vous avez un seul résultat et passer à votre autre modèle de présentation. Pour accomplir cette tâche, vous pouvez utiliser les règles suivantes :

```
On condition: 
  targeted template is default 
  targeted template primary results equal 1 
  not last search 
Perform the following actions: 
  Set targeted template to product_spotlight
```

MegaElectronic est un grand magasin d&#39;électronique. Après avoir analysé leurs données de recherche, MegaElectronic remarque que de nombreux clients effectuent une recherche de produit à l&#39;aide du numéro de référence d&#39;un produit. Dans ce cas, MegaElectronic souhaite rediriger vers la page Web associée au produit, si le client l&#39;a recherché directement et qu&#39;un seul produit a été trouvé.

Pour obtenir ce résultat, vous pouvez utiliser une seule règle avec trois conditions. La première condition vérifie que la recherche renvoyée n’a qu’un seul résultat. La deuxième condition garantit que le terme de requête correspond au format du numéro de référence de MegaElectronic pour les résultats qu’il souhaite provoquer la redirection. La troisième condition garantit que le client n’a pas utilisé de facettes pour analyser un résultat, étant donné que le numéro d’article peut être un numéro d’article partiel et renvoyer plusieurs résultats. L’action redirige vers un champ dans le résultat.

```
On condition: 
  targeted template's primary results equal 1 
  query q matches regular expression ^\D\D\D-\d+ 
  no facet selected ^\D\D\D-\d+ 
Perform the following actions: 
  redirect to result field "loc" in template *targeted for search *primary
```

## Bonnes pratiques {#section_1BF7DE1BD5664B3BAEC26AA829FDB0BA}

* Tout ensemble de règles qui déclenche un nouveau cycle de recherche doit toujours comporter une clause conditionnelle pour vérifier qu’il ne s’agit pas de la dernière transmission du module. Si vous avez déjà effectué le nombre maximal de recherches, vous ne pouvez pas rétablir les recherches.
* Si vous êtes sur le dernier passage du module et que les résultats sont encore médiocres, vous pouvez passer à un modèle &quot;aucun résultat&quot;.
* Vous devez baser la modification d’un modèle de présentation sur le résultat d’une recherche qui peut comporter d’autres paramètres. Si vous souhaitez sélectionner un modèle basé uniquement sur la requête entrante, une règle de pré-recherche est plus efficace.
* L&#39;exploration des données de la requête est effectuée dans le module de nettoyage de requête. Vous pouvez référencer les variables personnalisées dans le traitement après la recherche.
* Lorsque vous effectuez des redirections, vérifiez toujours que le client n’a sélectionné aucune facette. La raison en est qu’il est gênant lorsqu’un client analyse une facette et qu’il est soudainement retiré des résultats de la recherche. Le client peut vouloir désélectionner la facette lorsqu’il voit que le résultat unique n’est pas la volonté qu’il recherchait.

## Ajout d’une nouvelle règle de post-recherche {#task_52F6F9AAD65B45B5ACA1FF245DFFADD9}

Vous pouvez utiliser [!DNL Post-Search Rules] pour sélectionner le modèle de présentation utilisé pour afficher les résultats de la recherche en fonction de la requête entrante.

**Pour ajouter une nouvelle règle de post-recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Sur la [!DNL Post-Search Rules] page, cliquez sur **[!UICONTROL Add New Rule]**.
1. Dans le [!DNL Name] champ, saisissez le nom de la nouvelle règle de nettoyage de requête.
1. Sur la [!DNL Add Post-Search Rule] page, utilisez les listes déroulantes et les champs de texte pour créer votre requête.

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
      <td colname="col2"> <p>Un cookie HTTP. Les noms et valeurs des cookies doivent être codés dans l’identifiant de ressource unique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable personnalisée </p> </td> 
      <td colname="col2"> <p>Variable définie par l’utilisateur. Vous pouvez ajouter, supprimer ou définir un nombre illimité de variables personnalisées. </p> <p>Vous pouvez référencer toutes les variables personnalisées que vous avez définies dans le nettoyage des requêtes et dans les modules Règles de pré-recherche, dans les Règles de post-recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable système </p> </td> 
      <td colname="col2"> <p>Variables en lecture seule définies par le système interne que vous pouvez vérifier. Les variables système suivantes sont prises en charge : </p> <p> 
        <ul id="ul_BC17F1637F27424CA4E8F530C28A3245"> 
          <li id="li_C7DF96EFD7AA4A449D00F7EACCAA0EB1"> <span class="uicontrol"> nom d’hôte </span> <p>Nom de l’hôte du serveur. </p> </li> 
          <li id="li_F85AB1D2B9374A859657D12B8ED6674B"> <span class="uicontrol"> uri </span> <p>Identifiant de ressource unique demandé sans chaîne de requête. </p> </li> 
          <li id="li_440149C9EC6E4805B77BBC97BE41542A"> <span class="uicontrol"> args </span> <p>Chaîne de requête complète. </p> </li> 
          <li id="li_F583FC4B0E404858BB3522B33A6F7A0A"> <span class="uicontrol"> environnement </span> <p>"Stage" ou "live" selon que la requête entrante a été envoyée à votre environnement d’évaluation ou de production. </p> </li> 
          <li id="li_15902AA49B144D42A5E95D7E8B0FB1E1"> <span class="uicontrol"> referrer </span> <p>Localisateur de ressources uniforme d’où provient le client. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable système </p> </td> 
      <td colname="col2"> <p>Variables en lecture seule que vous pouvez utiliser dans les conditions pour déterminer l’état actuel. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facette de recherche du modèle </p> </td> 
      <td colname="col2"> <p>Facette locale à une recherche nommée associée à un modèle de présentation. Une facette est essentiellement des paramètres CGI spéciaux utilisés pour indiquer la valeur d’une facette sélectionnée par un client. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre de recherche du modèle </p> </td> 
      <td colname="col2"> <p>Paramètre CGI local à une recherche nommée associée à un modèle de présentation. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre principal du modèle </p> </td> 
      <td colname="col2"> <p>Les paramètres de requête entrants sont finalement convertis en paramètres principaux utilisés pour effectuer la recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Paramètres CGI de recherche en arrière-plan </a>. </p> <p>Les paramètres du serveur principal ne s’affichent pas sur les éléments de navigation. Par conséquent, vous pouvez masquer les paramètres supplémentaires que vous souhaitez appliquer à une recherche de vos clients. </p> <p>Le paramètre est local pour une recherche spécifique dans un modèle de présentation. Les actions sur les paramètres principaux sont des liaisons tardives; c' est-à-dire qu' ils sont appliqués juste avant l' envoi de la recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Modèle ciblé </p> </td> 
      <td colname="col2"> <p>Instance spéciale d’une variable personnalisée définie par le système qui ne peut pas être supprimée. Cette variable contient le modèle de présentation ciblé actuel. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classement </p> </td> 
      <td colname="col2"> <p>Permet de spécifier la règle de classement à utiliser dans la recherche. Cette option s’affiche uniquement lorsque vous avez défini des champs de classement et des règles de classement. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dernière règle </p> </td> 
      <td colname="col2"> <p>Lorsqu’il est coché, le module de traitement post-recherche n’exécute aucune règle supplémentaire après l’action de la règle correspondante. Cette action est utile lorsque vous avez défini des actions qui provoquent la correspondance d’une règle ultérieure mais que vous ne souhaitez pas que la règle ultérieure s’exécute. </p> </td> 
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

## Modification d’une règle après la recherche {#task_ECB00334C0A74C87AF857DB3EB372119}

Vous pouvez modifier les règles post-recherche existantes que vous avez ajoutées à la [!DNL Post-Search Rules] page.

**Pour modifier une règle après la recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Pre-Search Rules]**.
1. Sur la [!DNL Post-Search Rules] page, sous la **[!UICONTROL Actions]** colonne du tableau, cliquez **[!UICONTROL Edit]** pour la règle associée à modifier.
1. Sur la [!DNL Edit Post-Search Rule] page, utilisez les listes déroulantes et les champs de texte pour créer votre requête.

   Voir le tableau des options sous [Ajout d’une nouvelle règle](../c-about-rules-menu/c-about-post-search-rules.md#task_52F6F9AAD65B45B5ACA1FF245DFFADD9)post-recherche.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une règle après la recherche {#task_0F4653AB20D54B769A4FA8D1491AB4CF}

Vous pouvez supprimer les règles de post-recherche dont vous n’avez plus besoin ou que vous n’utilisez plus.

Lorsque vous supprimez une règle, l’ordre d’exécution des règles restantes est ajusté automatiquement pour tenir compte de la suppression.

**Pour supprimer une règle après la recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Sur la [!DNL Post-Search Rules] page, sous la **[!UICONTROL Actions]** colonne du tableau, cliquez **[!UICONTROL Delete]** pour la règle associée à supprimer.
1. Dans la [!DNL Confirmation] boîte de dialogue, cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification de l’ordre d’exécution des règles post-recherche {#task_40542FCD32234BBF881A81BF5477F78F}

Vous pouvez réorganiser les règles de post-recherche pour modifier l’ordre dans lequel elles s’exécutent sur les modèles de présentation.

Les règles de post-recherche s’exécutent dans l’ordre dans lequel elles ont été définies. Plus le numéro d’ordre d’une règle est élevé, plus le processus est long, ce qui l’emporte sur les règles antérieures. Vous réorganisez les règles en entrant un nouveau numéro dans la colonne Ordre du tableau de la [!DNL Post-Search Rules] page. Vous pouvez également faire glisser des règles pour modifier leur ordre d’exécution.

**Pour modifier l’ordre d’exécution des règles de post-recherche**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Post-Search Rules]**.
1. Sur la [!DNL Post-Search Rules] page, effectuez l’une des opérations suivantes :

   * Cliquez sur l’en-tête de **[!UICONTROL Order]** colonne pour trier les règles par ordre croissant ou décroissant.
   * Dans la [!DNL Order] colonne, dans le champ de texte à gauche du nom d’une règle de pré-recherche, saisissez le numéro d’ordre à exécuter.
   * Faites glisser une rangée de tableau à l’emplacement où vous souhaitez que la règle s’exécute. Tous les numéros de commande sont mis à jour pour refléter le nouvel ordre dans lequel les règles s’exécutent.

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
