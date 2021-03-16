---
description: Les chemins de navigation sont un contrôle de navigation que vous pouvez ajouter à votre site Web. La barre de navigation donne aux clients des commentaires sur l'emplacement de leur contenu dans un jeu de résultats de recherche. Cela les aide également à revenir rapidement à une étape précédente.
solution: Target
subtopic: Navigation
title: A propos des chemins de navigation
topic: Création, recherche sur site et marchandisage
uuid: 3e630a72-a631-4f4f-8aa5-adf2882cdf1c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 1%

---


# A propos des chemins de navigation{#about-breadcrumbs}

Les chemins de navigation sont un contrôle de navigation que vous pouvez ajouter à votre site Web. La barre de navigation donne aux clients des commentaires sur l&#39;emplacement de leur contenu dans un jeu de résultats de recherche. Cela les aide également à revenir rapidement à une étape précédente.

## Utilisation des chemins de navigation {#concept_FB8A943C594A4A1593B118141DA61F03}

Les chemins de navigation effectuent le suivi du terme recherché et des facettes suivantes qui ont été sélectionnées pour réduire le jeu de résultats.

Utilisez les paramètres du chemin de navigation pour personnaliser le contrôle du chemin de navigation de votre couche de présentation de recherche. Si votre couche de présentation comporte plusieurs jeux de résultats de recherche, le contrôle de chemin de navigation agit sur la recherche Principale de la page.

Vous pouvez modifier un chemin de navigation pour modifier le comportement par défaut, la largeur maximale de la valeur et l’extension de la valeur, et pour choisir d’inclure ou non le terme de requête.

## Ajouter un nouveau chemin de navigation {#task_2FFA94F82AE74F10BDDE7367CDCEAE8B}

Vous pouvez ajouter une barre de navigation afin qu’un client puisse suivre où il se trouve sur votre site Web.

<!-- 

t_adding_a_new_breadcrumb.xml

 -->

>[!NOTE]
>
>Veillez à référencer la barre de navigation dans votre modèle de présentation afin qu’elle soit visible sur le site Web.

**Pour ajouter un nouveau chemin de navigation**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Sur la page [!DNL Breadcrumbs], cliquez sur **[!UICONTROL Add Breadcrumb]**.
1. Sur la page [!DNL Add Breadcrumb], définissez les options de votre choix.

   Ces paramètres affectent à la fois le comportement et la présentation par défaut d’un chemin de navigation. Vous pouvez remplacer certains de ces paramètres par les paramètres du modèle de présentation.

   <!-- 
   
   r_breadcrumb_options.xml
    
    -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom de la barre de navigation </p> </td> 
      <td colname="col2"> <p>Nom du chemin de navigation. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Comportement </p> </td> 
      <td colname="col2"> <p>Définit l’un des trois comportements de chemin de navigation suivants : </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
        <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Aller  </span> <p>Atteindre supprime tous les chemins de navigation après celui sur lequel l’utilisateur a cliqué et début une nouvelle recherche à ce stade. </p> </li> 
        <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Supprimer </span> <p>Supprimer supprime du chemin la barre de navigation sur laquelle le client a cliqué, puis début une nouvelle recherche. Ce comportement s’avère utile lorsque vous souhaitez laisser le client annuler les étapes d’exploration vers le bas de la recherche. </p> </li> 
        <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Déposer  </span> <p>Déposer supprime tous les chemins de navigation. </p> </li> 
      </ul> </p> <p> Par exemple, supposons que vous avez un chemin de navigation de 1 &gt; 2 &gt; 3 &gt; 4. Lorsqu’un client clique sur "2", les résultats suivants s’affichent, en fonction du comportement que vous avez choisi : </p> <p> 
      <ul id="ul_96FCD8E4C3704B45B59BC18A7A1AC52A"> 
        <li id="li_B880037088DF426F880788EAA3072180">Aller à - 1 &gt; 2 </li> 
        <li id="li_D0F07A15DCD043EFA4563632ED33A9E2">Supprimer - 1 &gt; 3 &gt; 4 </li> 
        <li id="li_D848ED44B4E44538AA92010F9F186224"> Déposer : tout le chemin de navigation est abandonné, ramenant le client au point où il a commencé à descendre. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Largeur de valeur maximale </p> </td> 
      <td colname="col2"> <p>Indique la longueur de chaque valeur dans le chemin de navigation. Vous indiquez ce paramètre en tant que nombre de caractères. </p> <p>Par exemple, un paramètre de 6 signifie que le chemin de navigation peut comporter jusqu’à 6 caractères, y compris des espaces. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Extension de valeur </p> </td> 
      <td colname="col2"> <p>Indique les ellipses à utiliser lorsqu’un chemin de navigation est tronqué. </p> <p>Par défaut, un "..." (ellipses) est utilisé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure le terme de Requête </p> </td> 
      <td colname="col2"> <p>Contrôle la présence d’un terme de requête dans un chemin de navigation. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activer les miettes définies par l’utilisateur </p> </td> 
      <td colname="col2"> <p>Cochez cette case pour vous permettre d’utiliser les éléments définis par l’utilisateur dans des chemins de navigation en utilisant les paramètres <span class="codeph"> uX=[nom]&amp;[nom]=[valeur] </span> de l’URL. Vous pouvez utiliser des règles de traitement pour gérer ces paramètres comme vous le souhaitez. </p> <p>Par exemple, si cette fonction est activée et que vous disposez de l’URL <code> https://search.host.com/?1=category&amp;q1=Clothes&amp;u2= 
          type&amp;type=Men&amp;x3=kind&amp;q3=Sweater </code> si vous avez des facettes <span class="codeph"> <span class="varname"> catégorie </span> </span> et <span class="codeph"> <span class="varname"> </span> </span>, votre chemin de navigation ressemblera à <span class="codeph"> Vêtements &gt; Hommes &gt; Sweater &lt;a10/ .</span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Noms de boite définis par l’utilisateur </p> </td> 
      <td colname="col2"> <p>Liste séparée par des virgules de tous les noms possibles d’éléments de chemin de navigation définis par l’utilisateur. </p> <p>Cette option n'est disponible que si vous cochez <span class="uicontrol"> Activer les miettes définies par l'utilisateur </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Sur la page [!DNL Breadcrumbs], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’un chemin de navigation {#task_583481D9A23E4E0F97AEB18E72CBE13F}

Vous pouvez modifier les paramètres de tout chemin de navigation que vous avez ajouté.

<!-- 

t_editing_a_breadcrumb.xml

 -->

>[!NOTE]
>
>Veillez à référencer la barre de navigation dans votre modèle de présentation afin qu’elle soit visible sur le site Web.

**Pour modifier un chemin de navigation**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Sur la page [!DNL Breadcrumbs], cliquez sur **[!UICONTROL Edit]** à l&#39;extrémité droite du nom d&#39;un chemin de navigation.
1. Sur la page [!DNL Edit Breadcrumb], définissez les options de votre choix.

   Consultez le tableau des options sous [Ajouter un nouveau chemin de navigation](../c-about-design-menu/c-about-breadcrumbs.md#task_2FFA94F82AE74F10BDDE7367CDCEAE8B).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la page **[!UICONTROL Breadcrumb]**, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’un chemin de navigation {#task_401C6E481A744284906E15A29E04F757}

Vous pouvez supprimer tout chemin de navigation ajouté.

<!-- 

t_deleting_a_breadcrumb.xml

 -->

**Pour supprimer un chemin de navigation**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Breadcrumbs]**.
1. Sur la page [!DNL Breadcrumbs], cliquez sur **[!UICONTROL Delete]** à l&#39;extrémité droite du nom d&#39;un chemin de navigation.
1. Dans la boîte de dialogue [!DNL Confirmation], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

