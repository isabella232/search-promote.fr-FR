---
description: Vous pouvez utiliser les bannières pour gérer les bannières publicitaires sur votre site Web.
solution: Target
title: A propos des bannières
topic: Création, recherche sur site et marchandisage
uuid: 653b567d-5cf3-41a0-a260-a6912d0fd20d
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '4801'
ht-degree: 1%

---


# A propos des bannières {#about-banners}

Vous pouvez utiliser les bannières pour gérer les bannières publicitaires qui se trouvent sur votre site Web.

## Utilisation des bannières {#concept_5BBE01FEC6134393B43CC917C8CC64DA}

<!-- 

c_about_banners.xml

 -->

Il existe deux méthodes pour ajouter des bannières publicitaires à votre site Web.

La première méthode consiste à ajouter des bannières par Cible, Search &amp; Promote. Les bannières sont des fragments de code HTML qui s’affichent au moment où un client effectue une recherche sur votre site Web. Votre bannière peut inclure du texte ou une image au format GIF, JPEG ou PNG, ou une combinaison des deux. Vous pouvez choisir parmi des tailles prédéfinies ou définir vos propres dimensions personnalisées pour tenir compte de votre page. Le code HTML utilisé pour afficher la bannière peut également spécifier le style de police à utiliser et la bordure. Cette méthode d&#39;ajout d&#39;une bannière offre les fonctionnalités de base et ne nécessite pas de logiciel supplémentaire.

La deuxième méthode consiste à utiliser Adobe Dynamic Media Classic, un service de publication et de gestion dynamique des médias. Un compte Dynamic Media Classic d’Adobe valide vous permet de gérer et de diffuser directement le contenu des bannières à la Cible, à la Search &amp; Promote, à l’aide de Dynamic Media Classic. Dans la recherche/le marchandisage de site, vous configurez l’accès à votre compte Dynamic Media Classic. Ouvrez ensuite le navigateur de médias Dynamic Media Classic et sélectionnez un fichier multimédia dynamique que vous souhaitez utiliser comme bannière.

>[!NOTE]
>
>Avant de pouvoir utiliser des fichiers multimédias dynamiques comme bannières dans la recherche/le marchandisage sur le site, les fichiers sont d’abord téléchargés et préparés pour publication dans Scene7 Publishing System. Vous pouvez télécharger des fichiers à partir de la recherche/marchandisage sur le site et les préparer automatiquement pour publication par Scene7 Publishing System. Vous pouvez également télécharger et publier des fichiers depuis Scene7 Publishing System.

## Intégration de bannières à Adobe Scene7 Publishing System {#section_D4D7ADEA6A6348E68EDA138E184FE579}

Vous pouvez utiliser les types de ressources Dynamic Media Classic comme bannières dans la recherche/le marchandisage de sites, y compris les images, les bannières dynamiques et les modèles, tels que les modèles d’image ou de Flash.

Les modèles sont des fichiers d’image créés dynamiquement et superposés de manière adressable, tels que des fichiers superposés dans des applications de retouche d’images telles que Adobe Photoshop®. Contrairement à un fichier image statique, un modèle peut inclure des paramètres. Grâce aux paramètres, vous pouvez personnaliser les propriétés des images variables et le contenu des images.

>[!NOTE]
>
>Vous pouvez également créer des modèles à partir de conceptions basées sur des mises en page à l’aide de la publication de modèles dans Scene7 Publishing System et de fichiers provenant de Adobe Illustrator et Adobe InDesign.

Voir [Publication de modèles](https://help.adobe.com/en_US/scene7/using/WSFBFBAD30-2694-4b18-B7CE-894F9FC5CDDF.html) dans le Guide de l’utilisateur de Dynamic Media Classic (Scene7).

Un modèle peut contenir n’importe quel nombre de calques d’image et de texte. Vous pouvez convertir un fichier statique contenant des calques, tel qu’un fichier PSD superposé, en modèle ou créer des modèles dans Dynamic Media Classic. Vous pouvez créer des calques de texte dans des modèles à l’aide de polices que vous avez téléchargées dans Scene7 Publishing System. Après avoir ajouté du texte à un modèle, vous pouvez le mettre en forme en modifiant sa justification, ses polices, sa taille et sa couleur.

L’écran Paramètres de Dynamic Media Classic vous permet de convertir n’importe quel aspect d’un modèle en paramètre adressable. Ce faisant, vous pouvez modifier l’image superposée à utiliser ou la valeur de texte à utiliser dans votre modèle. Les paramètres sont transmis avec la chaîne URL, ce qui vous permet de modifier n’importe quel paramètre pour personnaliser dynamiquement l’image de réponse générée à partir du serveur d’images.

Vous pouvez en savoir plus sur l’utilisation de Dynamic Media Classic pour créer des modèles et paramétrer les propriétés des calques afin de pouvoir les utiliser dans des bannières.

Voir [Concepts de base des modèles](https://help.adobe.com/en_US/scene7/using/WS60B68844-9054-4099-BF69-3DC998A04D3C.html) dans le Guide de l’utilisateur de Dynamic Media Classic (Scene7).

**Téléchargement et publication de fichiers**

Vous devez télécharger et publier des fichiers dans Dynamic Media Classic avant de pouvoir les utiliser pour des bannières dans la recherche/le marchandisage de site. Ce prérequis inclut également tous les actifs utilisés par un modèle d’image ou un modèle de Flash. Utilisez votre compte Dynamic Media Classic pour télécharger et publier des ressources numériques. Vous pouvez également utiliser la recherche sur site/le marchandisage pour télécharger un fichier numérique, puis demander à Dynamic Media Classic de le publier automatiquement en fonction de vos paramètres de téléchargement. Si vous tentez de sélectionner un fichier qui n’est pas encore téléchargé et publié, vous en êtes informé dans l’interface utilisateur et vous avez la possibilité de le télécharger avant de continuer.

Vous pouvez en savoir plus sur le téléchargement et la publication de ressources numériques à l’aide de Scene7 Publishing System.

Voir [Téléchargement et publication des ressources](https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html) dans le Guide de l’utilisateur Dynamic Media Classic (Scene7).

>[!NOTE]
>
>Pour utiliser la fonctionnalité de téléchargement dans la visionneuse de ressources Dynamic Media Classic, assurez-vous que le compte Dynamic Media Classic que vous utilisez a déjà le rôle &quot;Administrateur de Société SPS&quot;.

Voir [Configuration de l’administration](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) dans le Guide de l’utilisateur de Dynamic Media Classic (Scene7).

**Modification des paramètres de modèle Dynamic Media Classic dans une bannière à l’aide de règles de fonctionnement**

Si vous avez ajouté une ressource Dynamic Media Classic en tant que bannière, vous pouvez utiliser [!DNL Visual Rule Builder] dans [!DNL Business Rules] pour l’ajouter à n’importe quelle zone de bannière de votre site Web. Par exemple, vous ajoutez la bannière à vos pages de résultats de recherche, comme vous le feriez pour toute autre bannière. Vous pouvez également remplacer les valeurs de paramètre par défaut dans les modèles Dynamic Media Classic en les personnalisant en fonction de vos besoins spécifiques. Ce type de fonctionnalité vous permet de personnaliser des modèles Dynamic Media Classic avec différents messages marketing et des hyperliens vers différents points de terminaison.

Voir aussi [Ajouter une nouvelle règle de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).

Voir aussi [Modification d&#39;une règle de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

## Ajouter une bannière {#task_549D02B5F73B4158B105A94E39D937B7}

Vous pouvez utiliser [!DNL Banners] pour gérer les bannières publicitaires et leur emplacement sur votre site Web. Lorsque vous ajoutez une bannière, vous référencez l’image de manière externe au moyen de fragments de code HTML qui s’affichent au moment de la recherche.

<!-- 

t_adding_a_new_banner.xml

 -->

Si vous disposez d’un compte d’Adobe Dynamic Media Classic valide, vous pouvez ajouter des bannières publicitaires au moyen de Scene7 Publishing System.

Voir [Ajouter une bannière à l’aide d’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

Voir [Configuration de l’accès à votre compte Dynamic Media Classic Adobe](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D).

**Pour ajouter une bannière**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Sur la page [!DNL Banners], dans la liste déroulante **[!UICONTROL Add Banner]**, sélectionnez **[!UICONTROL HTML code]**.
1. Dans la boîte de dialogue [!DNL Add Banner], définissez les options de votre choix.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom </p> </td> 
      <td colname="col2"> <p>Requis. Identifie le nom de votre bannière. Le nom est utilisé pour faire référence à la bannière lorsque vous l’ajoutez dans le Créateur de règles visuel dans les Règles métier. Le nom n’apparaît pas dans la bannière elle-même. </p> <p>Voir <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" type="task" format="dita" scope="local"> Ajouter une nouvelle règle de fonctionnement.</a> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bannière HTML </p> </td> 
      <td colname="col2"> <p> Permet de coller le code HTML associé à la bannière. </p> <p>Tout code HTML est acceptable, y compris le code CSS entouré de 
        Balises <code>
          &lt;style&gt; 
        </code> ou code JavaScript entouré de 
        <code>
          &lt;script&gt; 
        </code> balises. Par exemple, le bloc de code suivant est destiné à une bannière de texte de type Horizontal top : <code> &lt;div&nbsp;style="width:&nbsp;684px;&nbsp;background-image:&nbsp;url('https://www.brough.com/blackb.gif');&nbsp; 
          padding-top:&nbsp;10px;&nbsp;padding-bottom:&nbsp;10px;&nbsp;color:&nbsp;white;&nbsp;font-family:&nbsp;verdana;&nbsp; 
          text-align:&nbsp;center;&nbsp;font-size:&nbsp;20px;"&gt;&nbsp;Sound&nbsp;Study&nbsp;ships&nbsp;free!&nbsp;&lt;/div&gt; </code>Dans l’exemple suivant, le bloc de code correspond à une image de démarrage complète : <code> &lt;img&amp;nbsp;src='https://geometrixx.com/images/GEOAds/geometrixx-beauty-home-01.jpg'&amp;nbsp;border="0"&amp;nbsp;/&gt; </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>Spécifie les types de bannières suivants : 
        <ul id="ul_6423AEDB9E664049989EB529D63C4A62"> 
          <li id="li_BF6CD60B3ED748D49CFFB9C5D607661C"> <span class="uicontrol"> [nouveau type]  </span> <p>Permet de spécifier le type de bannière souhaité, y compris les dimensions et le nom. </p> </li> 
          <li id="li_1A29AB22AD644E60A12298187B5E898E"> <span class="uicontrol"> Démarrage complet  </span> <p>La dimension définie pour ce type de bannière est de 680 pixels de large et de 650 pixels de haut. Vous pouvez éventuellement spécifier le nom du type ou accepter le nom par défaut qui correspond au nom du type de bannière lui-même. </p> </li> 
          <li id="li_2BE06D013CB54DDE851051BFC038BB57"> <span class="uicontrol"> Haut horizontal  </span> <p> La bannière est placée dans la partie supérieure de votre site Web. Ce type est utile si vous avez l’intention d’ajouter des hyperliens à gauche ou à droite de la bannière. La dimension définie pour ce type de bannière est de 468 pixels de large et de 60 pixels de haut. Vous pouvez éventuellement spécifier le nom du type ou accepter le nom par défaut qui correspond au nom du type de bannière lui-même. </p> </li> 
          <li id="li_EC35AB92234749F08AA8A9BD26D0EA8D"> <span class="uicontrol"> Haut horizontal - Pleine largeur  </span> <p>Ce type est celui par défaut lorsque vous ajoutez une nouvelle bannière. La bannière est positionnée sur la partie supérieure de votre site Web et occupe toute la largeur de la page. La dimension définie pour ce type de bannière est de 670 pixels de large et de 150 pixels de haut. Vous pouvez éventuellement spécifier le nom du type ou accepter le nom par défaut qui correspond au nom du type de bannière lui-même. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Balises </p> </td> 
      <td colname="col2"> <p>Ajoute les balises ou "mots-clés" que vous souhaitez associer à la bannière. Si vous utilisez de nombreuses bannières, l’ajout de balises peut vous aider à affiner la recherche de bannières afin que vous puissiez rapidement localiser la bannière appropriée à vos besoins. Vous pouvez également supprimer les balises que vous avez ajoutées. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d&#39;une bannière {#task_D4081083BE7B40F5A003D1A2F1435AEA}

Utilisez [!DNL Edit Banner] pour modifier des éléments tels que le nom de la bannière, le code HTML de la bannière, le type de la bannière et les balises associées.

<!-- 

t_editing_a_banner.xml

 -->

Si vous avez ajouté une bannière à l’aide de la recherche sur le site/du marchandisage, vous modifiez également la bannière à l’aide de l’Adobe Dynamic Media Classic.

Voir aussi [Modification d’une bannière à l’aide d’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

**Pour modifier une bannière**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Sur la page [!DNL Banners], cliquez sur ![](assets/icon_edit_16.gif).

   au-dessus d’une miniature de bannière à modifier.
1. Sur la page [!DNL Edit Banner], définissez les options de votre choix.

   Consultez le tableau des options sous [Ajouter une bannière](../c-about-design-menu/c-about-banners.md#task_549D02B5F73B4158B105A94E39D937B7).
1. Lorsque vous avez terminé de modifier la bannière, cliquez sur **[!UICONTROL Save]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Ajouter une bannière à l’aide d’Adobe Dynamic Media Classic {#task_AD1E0C00A9E04B1FA819EB93288786B3}

Vous pouvez utiliser [!DNL Banners] pour gérer les bannières publicitaires sur votre site Web. Lorsque vous ajoutez une bannière à l’aide d’Adobe Dynamic Media Classic, vous pouvez choisir parmi n’importe quelle ressource numérique que vous avez téléchargée sur Scene7 Publishing System.

<!-- 

t_adding_a_banner_using_adobe_scene7.xml

 -->

Pour ajouter une bannière à l’aide de l’Adobe Dynamic Media Classic, assurez-vous d’avoir configuré l’accès à votre compte Dynamic Media Classic valide.

Voir [Configuration de l’accès à votre compte Dynamic Media Classic Adobe](../c-about-settings-menu/c-about-account-options-menu.md#task_CEFF88C2033D41D0B2FE86C435EDAC6D).

**Pour ajouter une bannière à l’aide d’Adobe Dynamic Media Classic**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Banners.]**
1. Sur la page [!DNL Banners], dans la liste déroulante **[!UICONTROL Add Banner]**, cliquez sur **[!UICONTROL Adobe Scene7]**.
1. Dans la boîte de dialogue [!DNL Pick an Asset], dans le volet de gauche, utilisez les options de navigation de l’interface utilisateur pour localiser le dossier contenant la ressource numérique à utiliser pour une bannière.

   À l’exception des options de navigation des fichiers, toutes les autres options dépendent de la ressource numérique que vous avez sélectionnée pour l’ajouter ou la modifier.

   Utilisez les options de navigation des ressources pour localiser un fichier que vous souhaitez utiliser pour une nouvelle bannière dans la recherche/le marchandisage de site. Les options de navigation s’appliquent à tous les types de ressources numériques sélectionnées.

   >[!NOTE]
   >
   >Les options de navigation des fichiers ne s’affichent pas lorsque vous modifiez la bannière dans la boîte de dialogue [!DNL Change Parameters].

   Voir [Modification d’une bannière à l’aide de l’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   **Options de navigation des fichiers**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option de navigation </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/S7_folders.png"> </p> </td> 
      <td colname="col2"> <p>Permet de sélectionner le compte Dynamic Media Classic pour votre société particulière dans la liste déroulante et de parcourir les dossiers de ressources numériques de ce compte. </p> <p>Lorsque vous sélectionnez un dossier, le volet droit de la boîte de dialogue <span class="wintitle"> Sélectionner un fichier </span> affiche toutes les ressources numériques disponibles contenues dans ce dossier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_folderhistory.png"> </p> </td> 
      <td colname="col2"> <p>Permet de parcourir l'historique de navigation des dossiers en avant ou en arrière. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_reloadfolder.png"> </p> </td> 
      <td colname="col2"> <p>Actualise la liste des ressources numériques affichées pour un dossier sélectionné. </p> <p>Vous devrez peut-être cliquer sur ce contrôle si vous déplacez, supprimez ou renommez une ressource sélectionnée à l’aide de la liste déroulante <span class="uicontrol"> Actions </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_list_or_grid.png"> </p> </td> 
      <td colname="col2"> <p>Affiche les ressources numériques dans une vue de liste. La liste affiche l’icône ou l’image miniature associée à chaque fichier, le nom de fichier, le type de fichier numérique, les dimensions (le cas échéant) et la date de sa dernière modification. </p> <p>La vue de grille affiche les ressources numériques du dossier sélectionné sous la forme d’icônes, de miniatures ou des deux. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_actionsdropdown.png"> </p> </td> 
      <td colname="col2"> <p>Dans la vue de liste, vous pouvez déplacer, supprimer ou renommer une ressource numérique sélectionnée. </p> <p>Dans la vue de grille, vous pouvez déplacer ou supprimer une ou plusieurs ressources numériques sélectionnées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_upload.png"> </p> </td> 
      <td colname="col2"> <p>Ouvre la boîte de dialogue <span class="wintitle"> Télécharger </span> dans laquelle vous pouvez télécharger un fichier numérique sélectionné depuis votre bureau ou depuis un serveur externe afin de l’utiliser comme bannière. </p> <p>Une fois le fichier téléchargé, une tâche de publication est automatiquement planifiée dans Scene7 Publishing System. </p> <p>Consultez le tableau des options dans <a href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita" scope="local"> Ajouter une bannière à l’aide d’Adobe Dynamic Media Classic </a>. </p> <p>Vous pouvez en savoir plus sur le téléchargement et la publication de ressources numériques à l’aide de Scene7 Publishing System. </p> <p>Voir <a href="https://help.adobe.com/en_US/scene7/using/WS3673AD39-098B-4f08-8A24-CA51261B7366.html" scope="external" format="html"> Téléchargement et publication des ressources </a> dans le Guide de l’utilisateur de Scene7 Publishing System. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_searchfield.png"> </p> </td> 
      <td colname="col2"> <p>Permet de rechercher une ressource numérique par mot-clé ou de rechercher par emplacement de fichier dans le dossier sélectionné et ses sous-dossiers associés. </p> <p>Lorsque vous cliquez sur le champ de recherche, il ajoute automatiquement un champ de filtre facultatif. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Ajoute un autre filtre de ressources afin que vous puissiez affiner davantage la liste des ressources numériques affichées par type ou par date spécifique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_Kindfilter.png"> </p> </td> 
      <td colname="col2"> <p>Affinez la liste des ressources numériques affichées afin de n’afficher que celles d’un certain type, tel que Flash, image, modèle ou Tout autre. </p> <p>Cliquez sur <img src="assets/s7_deletefilter.png"> pour supprimer le filtre de la recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_datefilter.png"> </p> </td> 
      <td colname="col2"> <p>Affinez la liste des ressources numériques affichées pour n’afficher que celles créées ou modifiées avant une certaine date ou après une certaine date. </p> <p>Cliquez sur <img src="assets/s7_deletefilter.png" /> pour supprimer le filtre de la recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_assetzoom.png"> </p> </td> 
      <td colname="col2"> <p>Permet de faire glisser le curseur vers la gauche ou la droite pour réduire ou agrandir la vue entière du volet des ressources numériques, respectivement. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Options des propriétés**

   Les options Propriétés s’affichent si vous choisissez un modèle de Flash, un modèle d’image ou une image. En fonction de la ressource numérique choisie, toutes les options ne sont pas disponibles.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option Propriétés </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom </p> </td> 
      <td colname="col2"> <p>Nom descriptif du modèle ou de l’image, sans espaces. Vous pouvez éventuellement inclure la spécification de taille d’image dans le nom afin d’aider les utilisateurs à mieux identifier la ressource. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format </p> </td> 
      <td colname="col2"> <p>Identifie le format de l’image, ou modèle d’image. </p> <p>Vous pouvez choisir parmi les formats suivants : </p> 
        <ul id="ul_9A19421BCC424CF585645049DCB87F10"> 
        <li id="li_A4913D783BD547F9AFA1A259C56EC2B3">jpeg </li> 
        <li id="li_66237D7BE8754FB0B0088CE5A02C0214">png </li> 
        <li id="li_4EDDFD7C8AB04677BEC20EFC9AEBBF1F">png-alpha </li> 
        <li id="li_4FCB03C29AE647ACBAF5105016DF7579">gif </li> 
        <li id="li_B884BD7DFF1845FAA9C58EF09B888A77">gif-alpha </li> 
        </ul> <p>Cette option ne s’applique pas aux modèles de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Qualité </p> </td> 
      <td colname="col2"> <p>Contrôle le niveau de compression des images au format JPEG ou GIF. Ce paramètre affecte à la fois la taille du fichier et la qualité de l’image. L'échelle de qualité est de 1 à 100. </p> <p>Lorsque vous faites glisser le curseur à gauche ou à droite, l’image dans la fenêtre de prévisualisation est mise à jour pour refléter le changement de qualité. </p> <p>Cette option ne s’applique pas aux modèles de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Largeur </p> </td> 
      <td colname="col2"> <p>Indique la largeur de la ressource numérique, en pixels. Cette dimension correspond à la largeur de vue de la ressource par les clients qui visitent votre site Web. </p> <p>Cette option ne s’applique pas aux modèles de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hauteur </p> </td> 
      <td colname="col2"> <p>Indique la hauteur de la ressource numérique, en pixels. Cette dimension correspond à la hauteur à laquelle la ressource est vue par les clients qui visitent votre site Web. </p> <p>Cette option ne s’applique pas aux modèles de Flash. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Options de lien de bannière**

   Les options Lien de bannière s’affichent uniquement si vous avez choisi une image ou un modèle d’image pour votre bannière.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option Lien de bannière </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>URL du lien </p> </td> 
      <td colname="col2"> <p>Indique l’adresse URL à laquelle vous souhaitez lier la bannière lorsqu’un client clique sur l’image. </p> <p>Si vous ne souhaitez pas que la bannière renvoie à quoi que ce soit, laissez vide le champ URL du lien. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Target </p> </td> 
      <td colname="col2"> <p>Indique l’emplacement d’ouverture de la bannière liée, telle qu’une nouvelle fenêtre de navigateur ou un nouvel onglet. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Modifier les liens, option**

   L’option Modifier les liens s’affiche uniquement si vous avez choisi un modèle de Flash pour votre bannière.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Modifier les liens, option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img placement="inline" id="image_EBB8159690C74D4692B5DF945B045E0B" src="assets/icon_edit_16.gif" /> </p> </td> 
      <td colname="col2"> <p>Permet de modifier le champ de lien URL utilisé dans le modèle de Flash. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Options Remplacer le texte**

   Les options Remplacer le texte s’affichent uniquement si vous avez choisi un modèle de Flash pour votre bannière contenant des calques de texte modifiables.

   Toute modification apportée au texte dans le modèle de Flash est répercutée dans la fenêtre de Prévisualisation.

   >[!NOTE]
   >
   >Si vous ajoutez une commande search and replace pour remplacer &quot;cow&quot; par &quot;apple&quot;, puis créez une deuxième commande pour remplacer &quot;apple&quot; par &quot;orange&quot;, la seconde commande n&#39;a aucune incidence.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Remplacer le texte, option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_addfilter.png"> </p> </td> 
      <td colname="col2"> <p>Ajoute un champ de recherche et de remplacement. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_deletefilter.png"> </p> </td> 
      <td colname="col2"> <p>Supprime un champ Rechercher et remplacer et restaure le texte précédemment utilisé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rechercher </p> </td> 
      <td colname="col2"> <p>Permet de saisir un terme de recherche pour du texte non lié dans les calques du modèle de Flash. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remplacez </p> </td> 
      <td colname="col2"> <p>Permet de spécifier le texte à insérer à la place du texte que vous recherchez. </p> <p>Lorsque vous appuyez sur <span class="uicontrol"> Entrée </span> dans ce champ, la fenêtre de prévisualisation est mise à jour avec votre texte de remplacement. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Options des paramètres**

   Les options de paramètres s’affichent uniquement si vous avez choisi un modèle d’image ou un modèle de Flash pour votre bannière. Les options de paramètre réelles varient selon la manière dont le modèle a été créé et paramétré dans Scene7 Publishing System. Par exemple, votre modèle peut paramétrer des champs qui vous permettent de modifier du texte, du style de police, du prix, des codes spéciaux utilisés pour la livraison gratuite, la taille de l’image dans la bannière ou même de rechercher une autre image à utiliser.

   >[!NOTE]
   >
   >Gardez à l’esprit que toute modification apportée aux paramètres peut être remplacée par des règles de fonctionnement. Les paramètres servent uniquement de valeurs par défaut lorsqu’aucune règle de fonctionnement n’est créée qui, autrement, modifierait les paramètres.

   Voir [Ajouter une nouvelle règle de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).

   Voir [Modification d&#39;une règle de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

   **Basculer les options de visibilité des calques**

   L’option Basculer la visibilité des calques s’applique uniquement si vous avez choisi un modèle de Flash pour votre bannière.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Activer/désactiver l’option Visibilité de calque </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <img src="assets/s7_togglelayervisibility.png"> </p> </td> 
      <td colname="col2"> <p>Permet d’activer ou de désactiver la visibilité des différents calques qui composent le fichier de modèle de Flash. </p> <p>Chaque fois que vous activez ou désactivez la visibilité d’un calque, la fenêtre de prévisualisation est actualisée pour mettre à jour l’affichage. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   (Facultatif) Si le fichier numérique que vous souhaitez utiliser pour une bannière n’est pas disponible dans le dossier sélectionné, vous devrez peut-être le télécharger. Cliquez sur **[!UICONTROL Upload]**, puis sélectionnez le fichier et les options de votre choix. Le fichier est téléchargé vers le dossier sélectionné.

   >[!NOTE]
   >
   >Si vous souhaitez utiliser la fonctionnalité de téléchargement dans la visionneuse de ressources Scene7, assurez-vous que le compte Scene7 que vous utilisez a déjà le rôle &quot;Administrateur de Sociétés SPS&quot; défini.

   Voir [Configuration de l’administration](https://help.adobe.com/en_US/scene7/using/WS662101DF-D697-47a7-A7D8-B52FD8E94438.html) dans le Guide de l’utilisateur de Scene7 Publishing System.

   **Options de base**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Parcourir </p> </td> 
      <td colname="col2"> <p> Permet d’accéder au fichier que vous souhaitez télécharger, publier, puis sélectionner pour l’utiliser comme bannière. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Remplacer </p> </td> 
      <td colname="col2"> <p>Les fichiers que vous téléchargez remplacent les fichiers existants par le même nom de fichier, dans le dossier sélectionné. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Préférences de courriel </p> </td> 
      <td colname="col2"> <p> Vous permet de choisir la notification par courrier électronique que vous recevez pour le téléchargement, ou de ne pas être averti pour quoi que ce soit concernant la tâche de téléchargement. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Options avancées**

   Lorsque vous téléchargez des fichiers d’image PostScript (EPS) ou Illustrator (AI), vous pouvez les formater de différentes manières. Vous pouvez pixelliser les fichiers, les convertir au format FXG pour la publication de modèles, conserver l’arrière-plan transparent, choisir une résolution et choisir un espace colorimétrique.

   Les fichiers PSD (Photoshop Document) sont le plus souvent utilisés dans Dynamic Media Classic pour créer des modèles. Lorsque vous téléchargez un fichier PSD, vous pouvez créer automatiquement un modèle Dynamic Media Classic à partir du fichier (sélectionnez l’option **[!UICONTROL Create Template]**).

   Scene7 Publishing System crée plusieurs images à partir d’un fichier PSD avec des calques si vous utilisez le fichier pour créer un modèle ; il crée une image pour chaque calque.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Nom du groupe d’options </p> </th> 
      <th colname="col02" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Options de Profil des couleurs </p> </td> 
      <td colname="col02"> <p>Profil de couleur </p> </td> 
      <td colname="col2"> <p> Vous permet de choisir parmi les options suivantes : </p> 
        <ul id="ul_6927BC08CA2647EDB2C85DAD2B82AE31"> 
        <li id="li_CA3F44FF9C0F4CE987DCB0AF9303C2E4"> <span class="uicontrol"> Convertir en SRVB  </span> <p>Convertit en SRGB (Standard Red Green Blue). SRVB est l’espace colorimétrique recommandé pour l’affichage d’images sur les pages Web. </p> </li> 
        <li id="li_FCCEE6B14CCD4246ADA152932010ABF1"> <span class="uicontrol"> Conserver l’espace colorimétrique d’origine  </span> <p>Conserve l’espace colorimétrique d’origine. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options d’édition d’images </p> </td> 
      <td colname="col02"> <p>Créer un masque à partir du chemin de tracé </p> </td> 
      <td colname="col2"> <p>Créez un masque pour l’image en fonction de ses informations de chemin de tracé. Cette option s’applique aux images créées à l’aide d’applications de retouche d’images dans lesquelles un chemin de tracé a été créé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options PostScript </p> <p>Options Illustrator </p> </td> 
      <td colname="col02"> <p>Traitement </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> L’ </span> option Pixelliser convertit les graphiques vectoriels du fichier au format bitmap. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Options Postscript </p> <p>Options Illustrator </p> </td> 
      <td colname="col02"> <p> Résolution </p> </td> 
      <td colname="col2"> <p> Détermine le paramètre de résolution. Ce paramètre détermine le nombre de pixels affichés par pouce dans le fichier. La valeur par défaut est de 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Options PostScript </p> <p>Options Illustrator </p> </td> 
      <td colname="col02"> <p> Espace colorimétrique </p> </td> 
      <td colname="col2"> <p>Permet de choisir un espace colorimétrique pour le fichier Illustrator. L’espace colorimétrique RVB est préférable pour l’affichage en ligne. </p> <p>Vous pouvez choisir parmi les options d’espace colorimétrique suivantes : </p> 
        <ul id="ul_0E83E2762A574480B243F963A7FB2ACD"> 
        <li id="li_B9FEC7D220D04CCABACD30839051DAE4"> <span class="uicontrol"> Détecter automatiquement  </span> <p> Conserve l’espace colorimétrique du fichier PDF. </p> </li> 
        <li id="li_ED0EB3B12BCF41C7AFC435447010B6FF"> <span class="uicontrol"> Forcer comme RVB  </span> <p> Convertit dans l’espace colorimétrique RVB. </p> </li> 
        <li id="li_3FB5DD8887C540BC97148A4D63B38F72"> <span class="uicontrol"> Forcer comme CMJN  </span> <p> Convertit dans l’espace colorimétrique CMJN. </p> </li> 
        <li id="li_6C018D3A4B254880AD41896E9F4AF3D9"> <span class="uicontrol"> Forcer comme Niveaux de gris  </span> <p> Convertit dans l’espace colorimétrique Niveaux de gris. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Options PostScript </p> <p>Options Illustrator </p> </td> 
      <td colname="col02"> <p> Tenir à jour l'arrière-plan transparent </p> </td> 
      <td colname="col2"> <p>Conserve la transparence d’arrière-plan du fichier. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options Photoshop </p> </td> 
      <td colname="col02"> <p> Conserver les calques </p> </td> 
      <td colname="col2"> <p>Pixellise les calques du fichier PSD, le cas échéant, dans des fichiers individuels. Les calques de fichier restent associés au fichier PSD. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Options Photoshop </p> </td> 
      <td colname="col02"> <p>Création d’un modèle </p> </td> 
      <td colname="col2"> <p> Crée un modèle à partir des calques du fichier PSD. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Options Photoshop </p> </td> 
      <td colname="col02"> <p> Extraire du texte </p> </td> 
      <td colname="col2"> <p> Extrait le texte afin que les clients puissent rechercher des mots-clés dans une bannière. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options Photoshop </p> </td> 
      <td colname="col02"> <p> Etendre les calques </p> </td> 
      <td colname="col2"> <p>Etend la taille des calques d’image pixellisés à celle du calque d’arrière-plan. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options Photoshop </p> </td> 
      <td colname="col02"> <p> Nom de calque </p> </td> 
      <td colname="col2"> <p>Les calques du fichier PSD sont téléchargés en tant qu’images distinctes. Vous pouvez sélectionner l’une des options suivantes pour choisir le nom de ces images dans Scene7 Publishing System : </p> 
        <ul id="ul_C2A25177A07740CA90B32C638304D39F"> 
        <li id="li_477D5BFF7238454BBF0E04B22DE378F7"> <span class="uicontrol"> Utiliser le nom du calque à partir du fichier PSD  </span> <p>Nomme les images après leur nom de calque dans le fichier PSD. Par exemple, un calque nommé <span class="codeph"> Etiquette de prix </span> dans le fichier PSD d’origine devient une image nommée <span class="codeph"> Etiquette de prix </span>. Cependant, si les noms de calque du fichier PSD sont des noms de calque Photoshop par défaut (Arrière-plan, Calque 1, Calque 2, etc.), les images sont nommées d’après leur numéro de calque dans le fichier PSD, et non leur nom de calque par défaut. </p> </li> 
        <li id="li_EB4173B884FC41328CFBDE27DA6D43AA"> <span class="uicontrol"> Utiliser le nom de fichier PSD et le numéro d’ajout  </span> <p>Nomme les images après leur numéro de calque dans le fichier PSD, en ignorant les noms de calque d’origine. Les images sont nommées avec le nom de fichier Photoshop et un numéro de calque annexé. Par exemple, le second calque d’un fichier appelé <span class="codeph"> Pub printemps </span> est nommé <span class="codeph"> Pub printemps_2 </span> même s’il portait un nom non par défaut dans Photoshop. </p> </li> 
        <li id="li_10B2D2DE2FD24BD08DB56D1D95ABA53D"> <span class="uicontrol"> Utiliser le nom de fichier PSD et le nom ou numéro de calque  </span> <p>Nomme les images après le fichier PSD suivi du nom du calque ou du numéro de calque. Le numéro de calque est utilisé si les noms de calque du fichier PSD sont des noms de calque Photoshop par défaut. Par exemple, un calque nommé <span class="codeph"> Etiquette de prix </span> dans un fichier PSD nommé <span class="codeph"> PubPrintemps </span> est nommé <span class="codeph"> Etiquette de prix de l'annonce de printemps </span>. Un calque portant le nom par défaut <span class="codeph"> Layer 2 </span> est nommé <span class="codeph"> Spring Ad_2 </span>. </p> </li> 
        <li id="li_5E57AC0719D4484B9C9BD14DB42B4455"> <span class="uicontrol"> Créer un dossier en fonction du nom de fichier PSD  </span> <p>Crée un dossier pour les images de calque à l’aide du nom de fichier du fichier PSD. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options Photoshop </p> </td> 
      <td colname="col02"> <p>Ancrage </p> </td> 
      <td colname="col2"> <p>Indiquez comment les images sont ancrées dans les modèles générés à partir de la composition superposée produite à partir du fichier PSD. </p> <p>Par défaut, l’ancre est le centre. Une ancre centrale permet aux images de remplacement de remplir au mieux le même espace, quel que soit le format de l’image de remplacement. Les images d’un aspect différent qui remplacent cette image, lors du référencement du modèle et de l’utilisation de la substitution de paramètres, occupent effectivement le même espace. Changez de paramètre si votre application a besoin des images de remplacement pour occuper l’espace alloué dans le modèle. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options PDF </p> </td> 
      <td colname="col02"> <p>Traitement </p> </td> 
      <td colname="col2"> <p> <span class="uicontrol"> L’ </span> option Pixelliser permet d’extraire les pages du fichier PDF et de convertir les graphiques vectoriels en images bitmap.  
        <!--Choose this option to create an eCatalog. (This option is thedefault.)--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options PDF </p> </td> 
      <td colname="col02"> <p> Résolution </p> </td> 
      <td colname="col2"> <p>Détermine le paramètre de résolution. Ce paramètre détermine le nombre de pixels affichés par pouce dans le fichier PDF. La valeur par défaut est de 150. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options PDF </p> </td> 
      <td colname="col02"> <p> Espace colorimétrique </p> </td> 
      <td colname="col2"> <p>Permet de choisir un espace colorimétrique pour le fichier PDF. La plupart des fichiers PDF comportent des images couleur RVB et CMJN. L’espace colorimétrique RVB est préférable pour l’affichage en ligne. </p> <p>Vous pouvez choisir parmi les options d’espace colorimétrique suivantes : </p> 
        <ul id="ul_44A8C39DEB21473F9375E3962F14D3C6"> 
        <li id="li_1046FA0017934C5EB7C0100F8F78507D"> <span class="uicontrol"> Détecter automatiquement  </span> <p> Conserve l’espace colorimétrique du fichier PDF. </p> </li> 
        <li id="li_561CCF705EDD451993D2DA2EB33F05F7"> <span class="uicontrol"> Forcer comme RVB  </span> <p> Convertit dans l’espace colorimétrique RVB. </p> </li> 
        <li id="li_D9E8CF61C40140979484EDEF7DAD2C44"> <span class="uicontrol"> Forcer comme CMJN  </span> <p> Convertit dans l’espace colorimétrique CMJN. </p> </li> 
        <li id="li_F3606B45C0F84BA594263EA12243F67A"> <span class="uicontrol"> Forcer comme Niveaux de gris  </span> <p> Convertit dans l’espace colorimétrique Niveaux de gris. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Options PDF </p> </td> 
      <td colname="col02"> <p>Générer automatiquement un catalogue électronique à partir d’un PDF de plusieurs pages </p> </td> 
      <td colname="col2"> <p> Crée automatiquement un catalogue électronique à partir du fichier PDF. Le catalogue électronique porte le nom du fichier PDF que vous avez téléchargé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Options PDF </p> </td> 
      <td colname="col02"> <p>Extraire les mots-clés </p> </td> 
      <td colname="col2"> <p>Extrait les mots du fichier PDF afin que le fichier puisse faire l’objet d’une recherche par mots-clés. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Dans le volet de droite, cliquez sur l’image, le modèle ou le fichier de Flash de votre choix.

   La fenêtre contextuelle [!DNL Pick An Asset] s&#39;affiche.
1. (Facultatif) Dans la fenêtre contextuelle [!DNL Pick An Asset], dans la liste déroulante [!DNL Actions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Move]**. Dans la boîte de dialogue [!DNL Select a folder to move to], sélectionnez le dossier dans lequel vous souhaitez déplacer la ressource numérique. Cliquez sur **[!UICONTROL Move]**.

      Vous pouvez également sélectionner plusieurs fichiers numériques que vous souhaitez déplacer vers un autre dossier.

   * Cliquez sur **[!UICONTROL Delete]**. Dans la boîte de dialogue [!DNL Delete Selected Assets], cliquez sur **[!UICONTROL Delete]**.

      Vous pouvez également sélectionner plusieurs fichiers numériques à supprimer du dossier.

   * Cliquez sur **[!UICONTROL Rename]**. Dans la boîte de dialogue [!DNL Enter a new name for], dans le champ de texte, tapez un nouveau nom pour la ressource numérique. Cliquez sur **[!UICONTROL Rename]**.

1. (Facultatif) En fonction de la ressource numérique que vous avez sélectionnée, définissez les options de votre choix dans le volet gauche de la fenêtre contextuelle [!DNL Pick an Asset].
1. Cliquez sur le fichier pour le sélectionner pour l’utiliser comme bannière.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une bannière à l’aide d’Adobe Dynamic Media Classic {#task_C3E782477FBF428ABEA220751781ACA9}

Utilisez [!DNL Edit Banner] pour modifier les propriétés et paramètres d&#39;une bannière que vous avez ajoutée à l&#39;aide de l&#39;Adobe Dynamic Media Classic.

<!-- 

t_editing_a_banner_using_adobe_scene7.xml

 -->

Si vous avez ajouté une bannière en y ajoutant du code HTML, vous modifiez la bannière en utilisant plutôt la fonction de recherche/marchandisage sur le site.

Voir aussi [Modification d&#39;une bannière](../c-about-design-menu/c-about-banners.md#task_D4081083BE7B40F5A003D1A2F1435AEA).

**Pour modifier une bannière à l’aide de l’Adobe Dynamic Media Classic**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. Sur la page [!DNL Banners], cliquez sur ![](assets/icon_edit_16.gif) au-dessus d’une miniature de bannière contenant une icône S7 dans le coin inférieur gauche de la fenêtre de bannière.
1. Sur la page [!DNL Change Parameter], définissez les options de votre choix.
1. Lorsque vous avez terminé de modifier la bannière, cliquez sur **[!UICONTROL Save]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression de bannières {#task_32F3BADC481E4E8984B2AA04B96052EB}

Vous pouvez supprimer des bannières par étapes dont vous n’avez plus besoin ou que vous ne souhaitez plus utiliser, individuellement ou en tant que groupe.

<!-- 

t_deleting_banners.xml

 -->

**Pour supprimer des bannières**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Facultatif) Effectuez une ou plusieurs des opérations suivantes :

   * Sur la page [!DNL Banners], sélectionnez le type de bannière à rechercher dans la liste déroulante **[!UICONTROL Find banner of type]**. Si vous le souhaitez, spécifiez un nom de balise dans le champ de texte **[!UICONTROL with tag]** ou un nom de type de bannière dans le champ de texte **[!UICONTROL with name]**. Cliquez sur **[!UICONTROL Find.]**

   * Dans la liste déroulante **[!UICONTROL Sort]**, sélectionnez la liste des bannières commandées.
   * Dans la liste déroulante **[!UICONTROL Show]**, sélectionnez le nombre de bannières à charger dans la page active que vous consultez.

1. Effectuez l’une des opérations suivantes :

   * Dans le coin supérieur gauche d’une bannière, cochez la case de chaque bannière à supprimer.
   * Dans la barre supérieure de la page [!DNL Banners], cochez **[!UICONTROL Select all]** pour sélectionner chaque bannière chargée sur la page actuellement affichée.

1. Dans la liste déroulante **[!UICONTROL Bulk Actions]**, cliquez sur **[!UICONTROL Delete]**.
1. Dans la boîte de dialogue [!DNL Confirmation Action], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Aperçu des bannières {#task_6AB1F81A984A4DC2ACACD1FE030545E2}

Vous pouvez parcourir les bannières que vous avez ajoutées à la page [!DNL Banners] pour en vue la taille complète. Aucune page CSS du modèle qui affecte la bannière n’est affichée.

<!-- 

t_previewing_banners.xml

 -->

**Pour prévisualisation des bannières**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Facultatif) Effectuez une ou plusieurs des opérations suivantes :

   * Sur la page [!DNL Banners], sélectionnez le type de bannière à rechercher dans la liste déroulante **[!UICONTROL Find banner of type]**. Si vous le souhaitez, spécifiez un nom de balise dans le champ de texte **[!UICONTROL with tag]** ou un nom de type de bannière dans le champ de texte **[!UICONTROL with name]**. Cliquez sur **[!UICONTROL Find.]**

   * Dans la liste déroulante **[!UICONTROL Sort]**, sélectionnez la liste des bannières commandées.
   * Dans la liste déroulante **[!UICONTROL Show]**, sélectionnez le nombre de bannières à charger dans la page active que vous consultez.

1. Sur la page [!DNL Banners], cliquez sur une miniature de bannière pour en vue la taille complète.
1. Effectuez l’une des opérations suivantes :

   * Dans la boîte de dialogue prévisualisation de la bannière, cliquez sur la flèche vers la gauche ou la flèche vers la droite pour parcourir et vue les bannières en taille réelle que vous avez ajoutées.
   * Cliquez sur le bouton de fermeture pour fermer la boîte de dialogue de prévisualisation de bannière et revenir à la page [!DNL Banners].

## Pousser les bannières en direct {#task_161F4FEC8362474296A566E64BF05B97}

Vous pouvez publier une ou plusieurs bannières sélectionnées sur votre site Web.

<!-- 

t_pushing_banners_live.xml

 -->

Ou, si vous préférez, vous pouvez diffuser en direct toutes les modifications sur une bannière à l’aide de l’option **[!UICONTROL Push Live]** située au bas de la page [!DNL Banners].

Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

**Pour diffuser des bannières en direct**

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Banners]**.
1. (Facultatif) Effectuez une ou plusieurs des opérations suivantes :

   * Sur la page [!DNL Banners], sélectionnez le type de bannière à rechercher dans la liste déroulante **[!UICONTROL Find banner of type]**. Si vous le souhaitez, spécifiez un nom de balise dans le champ de texte **[!UICONTROL with tag]** ou un nom de type de bannière dans le champ de texte **[!UICONTROL with name]**. Cliquez sur **[!UICONTROL Find]**.

   * Dans la liste déroulante **[!UICONTROL Sort]**, sélectionnez la liste des bannières commandées.
   * Dans la liste déroulante **[!UICONTROL Show]**, sélectionnez le nombre de bannières à charger dans la page active que vous consultez.

1. Effectuez l’une des opérations suivantes :

   * Dans le coin supérieur gauche d’une bannière, cochez la case de chaque bannière à supprimer.
   * Dans la barre supérieure de la page [!DNL Banner], cochez **[!UICONTROL Select all]** pour sélectionner chaque bannière chargée sur la page actuellement affichée.

1. Dans la liste déroulante **[!UICONTROL Bulk Actions]**, cliquez sur **[!UICONTROL Push live]**.
1. Dans la boîte de dialogue [!DNL Confirmation Action], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Sur la page [!DNL Banners], cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

   Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).
