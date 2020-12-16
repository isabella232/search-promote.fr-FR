---
description: Vous pouvez utiliser des menus pour personnaliser votre couche de présentation.
seo-description: Vous pouvez utiliser des menus pour personnaliser votre couche de présentation.
seo-title: A propos des menus
solution: Target
subtopic: Navigation
title: A propos des menus
topic: Design,Site search and merchandising
uuid: 011050cd-21b6-4150-9503-18fa3f771626
translation-type: tm+mt
source-git-commit: 552f93f1f630c64bbe3d5c8a87c4f5895ae6868c
workflow-type: tm+mt
source-wordcount: '763'
ht-degree: 1%

---


# Menus{#about-menus}

Vous pouvez utiliser des menus pour personnaliser votre couche de présentation.

## Utilisation des menus {#concept_68123CE5CF4447B59217B5D721424E32}

Ajoutez des menus qui correspondent aux paramètres de votre recherche. Chaque élément d&#39;un menu spécifie la valeur du paramètre du menu. Vous pouvez également personnaliser les étiquettes de menu.

Dans le modèle de présentation, vous pouvez référencer les menus définis. Vous pouvez ensuite les placer dans n’importe quel composant HTML de votre choix, tel qu’un contrôle Select. Cette combinaison permet aux utilisateurs de personnaliser leurs résultats de recherche. Trois types de menu sont pris en charge : tri, décompte et navigation.

## Ajouter un nouveau menu {#task_EE171532D3AE477FAFE8C2F4077A6D73}

Vous pouvez ajouter des menus qui correspondent aux paramètres des résultats de recherche.

<!-- 

t_adding_a_new_menu.xml

 -->

>[!NOTE]
>
>Veillez à référencer le menu dans votre modèle de présentation pour qu’il soit visible sur le site Web.

**Pour ajouter un nouveau menu**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. Sur la page [!DNL Menus], cliquez sur **[!UICONTROL Add New Menu]**.
1. Sur la page [!DNL Add Menu], définissez les options de votre choix.

   Ces paramètres affectent à la fois le comportement et la présentation par défaut d’un chemin de navigation. Vous pouvez remplacer certains de ces paramètres par les paramètres du modèle de présentation.

   Voir [Menus](../c-about-design-menu/c-about-menus.md#concept_68123CE5CF4447B59217B5D721424E32).

   <!-- 
   r_add_menu_options.xml
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
      <td colname="col1"> <p>Nom du menu </p> </td> 
      <td colname="col2"> <p>Nom du menu. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type de menu </p> </td> 
      <td colname="col2"> <p>Définit l’un des trois types de menu suivants : </p> <p> 
      <ul id="ul_7E66ACC1DA494B20BEC3B0B2CCAB103A"> 
      <li id="li_D81876660A8B48AFB70D3317063FBF6F"> <span class="uicontrol"> Tri </span> <p>Organise la recherche selon l’un de vos types de métadonnées définis. </p> <p>Par exemple, vous pouvez définir un menu de tri avec les types de métadonnées suivants : trois points pertinents ; un champ de métadonnées personnalisé tel qu'un code de disponibilité ; et le prix. Les trois éléments peuvent se voir attribuer les étiquettes "Trier par pertinence", "Trier par disponibilité" et "Trier par prix", respectivement. Lorsque vous incluez ceci dans votre modèle de présentation, le client peut utiliser ce contrôle pour trier ses résultats de recherche. </p> </li> 
      <li id="li_63AE06B544B64DCAA8C55031B3DFFFF7"> <span class="uicontrol"> Nombre </span> <p>Définit le nombre de résultats de recherche à afficher. Ce type de menu correspond au paramètre cgi <span class="varname"> sp_c </span>. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" format="dita" scope="local"> Paramètres CGI de la recherche principale </a>. </p> </li> 
      <li id="li_EEC810D420FF41498ECE49EBAAB33BE5"> <span class="uicontrol"> Navigation </span> <p>Indique un ensemble d’URL statiques associées à des éléments de menu. En règle générale, un menu de navigation est utilisé pour créer une barre de navigation de niveau supérieur sur votre page de résultats de recherche. </p> <p>Par exemple, vous pouvez créer un menu qui comprend des femmes, des hommes, des garçons et des filles, où les options de menu se présentent comme suit : 
      <code>
        /?q1=womens;x1=gender 
      </code>, 
      <code>
        /?q1=mens;x1=gender 
      </code> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Marchandisage </p> 
        <!--DONT' KNOW WHAT THIS DOES--> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous choisissez le type de menu <span class="uicontrol"> Trier. </span> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre d'éléments dans le menu </p> </td> 
      <td colname="col2"> <p>Indique le nombre d'éléments d'un menu. La modification de ce paramètre permet d’ajouter ou de supprimer des champs du formulaire. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Élément par défaut </p> </td> 
      <td colname="col2"> <p>Permet de sélectionner l’option de menu qui s’affiche par défaut. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de l’élément </p> </td> 
      <td colname="col2"> <p>La valeur de l'élément dépend du type de menu que vous avez défini. </p> 
        <ul id="ul_2F14E6AA673640578A2D5161FD9D13EF"> 
        <li id="li_5017EC6E4ACB4B8E99E0AA61CBAAFFAE"> Type de menu Trier <p>Identifie l'élément sélectionné dans le menu à trier. Les éléments sélectionnés sont renseignés par des champs de métadonnées pouvant être triés. </p> <p>Pour un seul élément, vous pouvez trier par trois champs de métadonnées. Le tri est effectué dans l’ordre spécifié. </p> </li> 
        <li id="li_CC6BAFBF969C4367A71B55F08E0758D1"> Type de menu Compter <p>Permet de spécifier le nombre de résultats à renvoyer lorsque le client sélectionne cette option de menu. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Libellé de l’élément </p> </td> 
      <td colname="col2"> <p>Le libellé de l'élément dépend du type de menu que vous avez défini. </p> 
        <ul id="ul_957BF01235F84748B5EB7062D6AEAC41"> 
        <li id="li_03FB2E2C96134A2B8E08154F87F0CD55"> Type de menu Trier <p>Identifie le libellé personnalisé que votre client doit voir lorsqu’il vue cet élément dans le menu. </p> </li> 
        <li id="li_C9FE2BC46D9443FB85FEB837C7CA45E1"> Type de menu Compter <p>Identifie le libellé personnalisé que vous souhaitez afficher pour cet élément de menu. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Sur la page [!DNL Menus], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d&#39;un menu {#task_0770DBFD0C7046169097FB6F771B9114}

Vous pouvez modifier les paramètres de tout menu que vous avez ajouté.

<!-- 

t_editing_a_menu.xml

 -->

>[!NOTE]
>
>Veillez à référencer le menu dans votre modèle de présentation pour qu’il soit visible sur le site Web.

**Pour modifier un menu**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**.
1. Sur la page [!DNL Menus], cliquez sur **[!UICONTROL Edit]** à l&#39;extrémité droite du nom d&#39;un menu.
1. Sur la page [!DNL Edit Menu], définissez les options de votre choix.

   Consultez le tableau des options sous [Ajouter un nouveau menu](../c-about-design-menu/c-about-menus.md#task_EE171532D3AE477FAFE8C2F4077A6D73).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la page [!DNL Menus], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d&#39;un menu {#task_645E212311A045CD8D9D906878165F47}

Vous pouvez supprimer tout menu que vous avez ajouté.

<!-- 

t_deleting_a_menu.xml

 -->

**Pour supprimer un menu**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Menus]**
1. Sur la page [!DNL Menus], cliquez sur **[!UICONTROL Delete]** à l&#39;extrémité droite du nom d&#39;un menu.
1. Dans la boîte de dialogue [!DNL Confirmation], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

