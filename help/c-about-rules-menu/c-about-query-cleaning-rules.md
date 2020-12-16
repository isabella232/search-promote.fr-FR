---
description: Utilisez des règles de nettoyage de Requête pour analyser et modifier la requête entrante.
seo-description: Utilisez des règles de nettoyage de Requête pour analyser et modifier la requête entrante.
seo-title: A propos des règles de nettoyage des Requêtes
solution: Target
title: A propos des règles de nettoyage des Requêtes
topic: Rules,Site search and merchandising
uuid: 683af81f-f7c0-45f8-9212-e5e7cb82ccca
translation-type: tm+mt
source-git-commit: d07cdc2c88f93eed4cecb0ee8818f7fdea06ee9d
workflow-type: tm+mt
source-wordcount: '1611'
ht-degree: 1%

---


# À propos des règles de nettoyage de Requête{#about-query-cleaning-rules}

Utilisez des règles de nettoyage de Requête pour analyser et modifier la requête entrante.

## Utilisation de règles de nettoyage de Requête {#concept_17F3CDDC3C8A4128AF092A82B777B86C}

Cette fonction est souvent utilisée lorsque vous souhaitez modifier le comportement de recherche/marchandisage sur le site. Par exemple, vous pouvez remplacer une recherche vide par un mot-clé populaire plutôt que par une recherche &quot;*&quot;, ce qui permet de promouvoir un produit populaire. Vous pouvez également utiliser des règles de nettoyage des requêtes pour effectuer un accès direct, où vous redirigez vers une URL. Cela peut s’avérer particulièrement utile lorsque vous détectez qu’une personne recherche un SKU de produit et que vous souhaitez ignorer la recherche et rediriger vers la page de ce produit. Le nettoyage des requêtes peut également extraire la requête et définir des variables personnalisées qui peuvent être utilisées dans les étapes de flux de traitement ultérieures. Les règles de nettoyage des requêtes sont exécutées de manière séquentielle pour chaque requête. Pour modifier l’ordre de vos règles, vous pouvez utiliser la fonction glisser-déposer. La commande réelle n&#39;est pas modifiée tant que vous ne l&#39;avez pas enregistrée.

Les règles de nettoyage des requêtes d&#39;un module de nettoyage des requêtes sont examinées afin de déterminer si l&#39;un des paramètres de requête doit être modifié ou si des variables personnalisées doivent être définies. Chaque règle de nettoyage de requête se compose de deux éléments principaux : actions de la règle et conditions facultatives. Un nombre illimité de règles et de conditions peut être spécifié. L’ordre de ces règles est important, car la recherche de site/le marchandisage effectue des boucles par l’intermédiaire du jeu de règles règle par règle. Lorsque les conditions d’une règle correspondent, toutes les actions associées sont exécutées.

Une fois le nettoyage de la requête terminé, les paramètres CGI résultants sont utilisés à partir de maintenant. Toutes les variables personnalisées qui ont été définies peuvent être utilisées par les étapes ultérieures du flux de traitement. Par défaut, le système supprime automatiquement les espaces de début et de fin du terme de requête.

## À propos des conditions de nettoyage des Requêtes {#section_BF6F25F94FED4DDEA8600D921EA43A66}

Les conditions sont facultatives. Si vous décidez que des actions sont spécifiées pour chaque requête, les actions sont toujours effectuées. Les conditions peuvent être basées sur tout paramètre de requête CGI, cookie existant ou variable personnalisée défini par une règle précédente. Il est considéré comme étant la &quot;bonne pratique&quot; pour la première règle de nettoyage de requête à exécuter pour chaque requête, où elle définit et initialise toutes les variables personnalisées que vous prévoyez d’utiliser.

## A propos des actions de nettoyage de Requête {#section_78F74A9B48DE484191CDA95F5B4E7154}

Toutes les actions d’une règle de nettoyage de requête qui comporte des conditions correspondantes sont exercées. Les actions se composent généralement d’une opération, des données sur lesquelles l’opération doit être effectuée et de la valeur à utiliser.

Voir le tableau des options dans [Ajouter une règle de nettoyage de requête](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).

## À propos des redirections {#section_597481E6194440C0A7B9E6FC901A81C0}

L’interface Direct-Hits vous permet de définir un ensemble de redirections en fonction du terme de requête entrant. Les redirections dans le nettoyage de Requête étendent cette idée. Cependant, les redirections vous donnent une granularité plus précise sur le moment où une redirection a lieu en spécifiant des conditions et vous permet de rediriger vers une URL dynamique plutôt que statique. Lorsque vous sélectionnez l’action de redirection, la ligne est mise à jour pour contenir une zone de texte dans laquelle vous spécifiez l’URL vers laquelle vous souhaitez rediriger. Dans l’URL, vous pouvez spécifier des variables ou des paramètres que vous souhaitez remplacer en les encadrant entre des accolades de doublon. Les variables personnalisées ont une priorité plus élevée que les paramètres CGI dans la substitution.

## Exemples {#section_DB5047CC38FB4A57B15CAAF9848073E3}

Supposons que vous ayez un magasin de vêtements avec un site Web. Si l&#39;utilisateur clique sur Rechercher sans aucun terme de recherche, vous souhaitez renvoyer une recherche contre jeans, car c&#39;est ce pour quoi vous êtes connu à l&#39;international. Vous souhaitez également analyser le terme de requête pour un sexe afin de pouvoir créer une règle de pré-recherche ultérieurement, en fonction de la variable personnalisée qui utilise un modèle de présentation différent pour chaque sexe.

```
On condition: 
  query q equal 
Perform the following actions: 
  Set query parameter q to value jeans 
 
On condition: 
  Query q matches regular expression wom[e|a]n[s]|girl[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value female 
 
On condition: 
  Query q matches regular expression men[s]|boy[s] 
Perform the following actions: 
  Add custom variable gender 
  Set custom variable gender to value male
```

MegaElectronic est un grand magasin d&#39;électronique. En analysant leurs données de recherche, MegaElectronic a remarqué que de nombreux clients expérimentés recherchent souvent un produit à l&#39;aide du SKU du produit, plutôt que de renvoyer un résultat de recherche pour le produit unique, MegaElectronic aimerait rediriger vers la page Web associée à ce SKU.

```
On condition: 
  query q matches regular expression ^\D\D\D-\d\d\d\d$ 
Perform the following actions: 
  redirect to https://www.megaelectronic.com/?sku={{q}}
```

## Ajouter une règle de nettoyage de requête {#task_47F43988D3D9485F8AE1DFDA7E00BF54}

Vous pouvez définir des règles qui nettoient ou modifient la requête de recherche entrante d’un client.

Vous ne pouvez sélectionner que les modèles existants. Si vous ne disposez d’aucun modèle, vous devez d’abord le définir.

Voir [À propos des modèles](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Pour ajouter une règle de nettoyage de requête**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Sur la page [!DNL Query Cleaning Rules], cliquez sur **[!UICONTROL Add New Rule]**.
1. Dans le champ [!DNL Name], saisissez le nom de la nouvelle règle de nettoyage de requête.
1. Sur la page [!DNL Add Query Cleaning Rule], utilisez les listes déroulantes et les champs de texte pour élaborer votre requête.

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
      <td colname="col2"> <p>Cookie HTTP. Vous pouvez définir des conditions basées sur des cookies associés à votre domaine. Vous pouvez également définir un cookie écrit avec les résultats de recherche sortants. Le nom et les valeurs des cookies doivent être encodés en Uniform Resource Identifier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Variable personnalisée </p> </td> 
      <td colname="col2"> <p>Variable définie par l’utilisateur. Ajoutez, supprimez ou définissez un nombre illimité de variables définies par l’utilisateur. Vous pouvez référencer n’importe quelle variable définie par l’utilisateur ici dans les règles de pré-recherche et les règles de post-recherche. </p> </td> 
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
          <li id="li_6FEE352DB7A842FCB2EBE1398AD03666"> <span class="uicontrol"> agent utilisateur  </span> <p>Chaîne "user-agent" du navigateur du client. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre de requête </p> </td> 
      <td colname="col2"> <p>Paramètres CGI transmis à la requête. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre principal </p> </td> 
      <td colname="col2"> <p>Les paramètres de requête entrants sont finalement convertis en paramètres principaux utilisés pour effectuer la recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Paramètres CGI de la recherche principale </a>. </p> <p>Les paramètres principaux n’apparaissent pas sur les éléments de navigation. Par conséquent, vous pouvez masquer les paramètres supplémentaires que vous souhaitez appliquer à une recherche effectuée auprès de vos clients. Les actions sur les paramètres principaux sont des liaisons tardives ; c'est-à-dire qu'elles sont appliquées juste avant l'envoi de la recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Facette </p> </td> 
      <td colname="col2"> <p>Paramètres CGI spéciaux associés à une facette donnée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Classement </p> </td> 
      <td colname="col2"> <p>Permet de spécifier la règle de classement à utiliser dans la recherche. Cette option ne s’affiche que si certains champs de classement et règles de classement sont définis. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Boutique </p> </td> 
      <td colname="col2"> <p>Le moteur de recherche détecte automatiquement le stockage dans lequel se trouve l'utilisateur en fonction du nom d'hôte ou du paramètre de requête <span class="codeph"> gs_store </span>, ce dernier paramètre ayant la priorité. Vous pouvez créer des conditions à partir de la boutique. Dans le nettoyage des requêtes uniquement, vous pouvez également utiliser une action pour remplacer la boutique actuelle. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Dernière règle </p> </td> 
      <td colname="col2"> <p>Lorsque les conditions sont remplies pour une règle qui a été définie en dernier, le module de traitement de nettoyage de requête n'exécute aucune règle supplémentaire après l'action de la règle correspondante. Cela s’avère utile lorsque vous avez défini des actions qui entraîneront la correspondance d’une règle ultérieure mais que vous ne souhaitez pas que la règle ultérieure se déclenche. Notez que si l’action d’une règle consiste à effectuer une redirection, celle-ci se produit immédiatement, de sorte qu’elle agit essentiellement comme si la dernière règle était définie. </p> </td> 
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

## Modification d&#39;une règle de nettoyage de requête {#task_FA2FF1A7E2634350AD703485CBC27CB3}

Vous pouvez modifier les règles de nettoyage de requête existantes que vous avez ajoutées à la page Règles de nettoyage de Requête.

**Pour modifier une règle de nettoyage de requête**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Sur la page [!DNL Query Cleaning Rules], sous la colonne **[!UICONTROL Actions]** du tableau, cliquez sur **[!UICONTROL Edit]** pour la règle associée à modifier.
1. Sur la page [!DNL Edit Query Cleaning Rule], utilisez les listes déroulantes et les champs de texte pour élaborer votre requête.

   Consultez le tableau des options sous [Ajouter une règle de nettoyage de requête](../c-about-rules-menu/c-about-query-cleaning-rules.md#task_47F43988D3D9485F8AE1DFDA7E00BF54).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d&#39;une règle de nettoyage de requête {#task_C52D17226B824590B087CAB6970CBB01}

Vous pouvez supprimer des règles de nettoyage de requête dont vous n’avez plus besoin ou que vous n’utilisez plus.

Lorsque vous supprimez une règle, l’ordre d’exécution des règles restantes est automatiquement ajusté pour tenir compte de la suppression.

**Pour supprimer une règle de nettoyage de requête**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Sur la page [!DNL Query Cleaning Rules], sous la colonne **[!UICONTROL Actions]** du tableau, cliquez sur **[!UICONTROL Delete]** pour la règle associée à supprimer.
1. Dans la boîte de dialogue [!DNL Confirmation], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification de l’ordre d’exécution des règles de nettoyage de requête {#task_C24012C45A4445468A7FD998017388CA}

Vous pouvez réorganiser les règles de nettoyage des requêtes pour modifier l’ordre dans lequel elles s’exécutent sur les modèles de présentation.

Les règles de nettoyage des requêtes s’exécutent dans l’ordre dans lequel elles ont été définies. Plus le numéro de commande d&#39;une règle est élevé, plus elle s&#39;exécute tard dans le processus, en l&#39;emportant sur les règles antérieures. Vous réorganisez les règles en entrant un nouveau numéro dans la colonne Ordre du tableau de la page [!DNL Query Cleaning Rules]. Vous pouvez également utiliser le glisser-déposer sur les règles pour modifier leur ordre d’exécution.

**Pour modifier l&#39;ordre d&#39;exécution des règles de nettoyage des requêtes**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Query Cleaning]**.
1. Sur la page [!DNL Query Cleaning Rules], effectuez l&#39;une des opérations suivantes :

   * Cliquez sur l&#39;en-tête de colonne [!DNL Order] pour trier les règles par ordre croissant ou décroissant.
   * Dans la colonne [!DNL Order], dans le champ de texte à gauche du nom d&#39;une règle de nettoyage de requête, tapez le numéro de commande à exécuter.
   * Faites glisser une rangée de tableau à l’emplacement où vous souhaitez que la règle s’exécute. Tous les numéros de commande sont mis à jour pour refléter le nouvel ordre dans lequel les règles s&#39;exécutent.

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

