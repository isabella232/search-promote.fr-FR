---
description: Utilisez le menu Options de compte pour mettre à jour les paramètres de votre compte, définir les préférences de marchandisage ou supprimer votre propre compte Search&amp;Promote.
solution: Target
subtopic: Account Options
title: A propos du menu Options de compte
topic-legacy: Settings,Site search and merchandising
uuid: 0f830033-de9e-4197-8d76-906c818662eb
exl-id: 0acaeeed-1649-46bb-af41-20f144400d7c
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1657'
ht-degree: 2%

---

# A propos du menu Options de compte{#about-the-account-options-menu}

Utilisez le menu Options de compte pour mettre à jour les paramètres de votre compte, définir les préférences de marchandisage ou supprimer votre propre compte de Search &amp; Promote.

## Configuration des paramètres de votre compte {#task_80A38D0C8E4F453395BD67B81E4B45D9}

Gérez les paramètres du compte, tels que le nom et l’adresse du site Web, le fuseau horaire, etc. Ou bien, vue votre numéro de compte.

**Pour configurer les paramètres de votre compte**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Account Settings]**.
1. Sur la page [!DNL Account Settings], définissez les options de votre choix.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom du site Web </p> </td> 
      <td colname="col2"> <p>Requis. </p> <p>Nom court utilisé pour décrire votre site Web/compte. Cette option est utile si vous avez plusieurs sites Web. </p> <p> <p>Remarque :  Vous devez contacter le support technique pour sélectionner un ou plusieurs noms à utiliser. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse du site Web </p> </td> 
      <td colname="col2"> <p>Requis. </p> <p>Adresse URL de votre site Web. L'adresse spécifiée ici est utilisée comme point d'entrée principal du site Web. </p> <p>Voir aussi <a href="../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45" type="task" format="dita" scope="local"> Ajouter plusieurs points d'entrée d'URL que vous souhaitez indexer </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuseau horaire (pour les rapports et la planification) </p> </td> 
      <td colname="col2"> <p>Fuseau horaire utilisé pour les rapports et les opérations de publication. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Validation des attributs de balise de modèle lors de l’enregistrement </p> </td> 
      <td colname="col2"> <p>Valide tous les attributs dans <span class="codeph"> &lt;guidé-*&gt; </span> et <span class="codeph"> &lt;search-*&gt; </span> lorsque vous enregistrez un modèle dans l’éditeur de modèles intermédiaires. </p> <p>Voir <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> Modification d'une présentation ou d'un modèle de transport </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valider les références de modèle aux objets GS lors de l'enregistrement </p> </td> 
      <td colname="col2"> <p> Vérifie l’existence d’objets de recherche guidée, tels que des menus, des facettes, des chemins de navigation, des variables personnalisées et des modèles, auxquels il est fait référence dans les balises <span class="codeph"> &lt;guidé-*&gt; </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Appliquer une vérification rigoureuse de la syntaxe des modèles </p> </td> 
      <td colname="col2"> <p>Rend le validateur de modèle plus strict et permet de vérifier des éléments tels que les guillemets déséquilibrés et les symboles &lt;&gt;. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Numéro de compte </p> </td> 
      <td colname="col2"> <p>Vous ne pouvez pas modifier le numéro de compte. Il est destiné uniquement à des fins d’affichage. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.

## Configuration de l’intégration avec Adobe CQ5 {#task_EA2FC2C24960498DAE01A1AB769D2F14}

Vous pouvez configurer l&#39;intégration de la recherche/marchandisage de site avec Adobe CQ5.

**Pour configurer l’intégration avec Adobe CQ5**

1. Obtenez votre ID de membre et votre ID de compte en procédant comme suit :

   * Connectez-vous à votre compte de recherche/marchandisage de site.
   * Dans le chemin d’accès de l’URL, copiez l’identifiant de membre et l’identifiant de compte.

      Par exemple, si le chemin d’accès à l’URL de votre compte est `https://searchandpromote.mycompany.com/px/home/?sp_id=00123a4b-sp1234a5b6`, l’identifiant de membre est `00123a4b` et l’identifiant de compte est `sp1234a5b6`.

1. Dans Adobe CQ5, utilisez l&#39;onglet Cloud Services pour créer la configuration de recherche/marchandisage de votre site.

   Utilisez l&#39;ID de membre et l&#39;ID de compte copiés pour les paramètres respectifs.

## Configuration des préférences de marchandisage {#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A}

Gérez les préférences de marchandisage, telles que le créateur de règles par défaut et le terme de recherche par défaut.

**Pour configurer les préférences de marchandisage**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Merchandising Preferences]**.
1. Sur la page [!DNL Merchandising Preferences], définissez les options de votre choix.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Seuil dominant du groupe de déclenchement </p> </td> 
      <td colname="col2"> <p> Pourcentage de seuil à appliquer aux déclencheurs basés sur les résultats "dominants du groupe" qui spécifient "utiliser le compte par défaut". </p> <p>La modification de ce paramètre peut immédiatement avoir un effet sur les recherches en direct. Par conséquent, soyez prudent lorsque vous modifiez ce paramètre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Définition de groupe </p> </td> 
      <td colname="col2"> <p>Nombre de résultats dans un groupe pour la console de marchandisage. Le maximum est de 50 000. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Champ MDI (Merchandising Document ID) </p> </td> 
      <td colname="col2"> <p> Le champ que vous spécifiez doit "unifier" les résultats de recherche que vous souhaitez manipuler au moyen de déclencheurs et d’actions basés sur les résultats "résultats uniques". </p> <p>L’utilisation du champ d’URL prédéfini fonctionne dans certains cas, mais n’est pas recommandée. Un champ de métadonnées défini par l’utilisateur avec un ID unique pour chaque page (comme SKU ou product_id par exemple) serait beaucoup plus efficace que l’utilisation du champ URL. La définition de "aucun" désactive les déclencheurs et actions basés sur les résultats de "résultat unique" dans le gestionnaire de règles. La modification de cette option s’applique uniquement aux règles enregistrées à l’avenir ; les règles existantes continuent d’utiliser le MDI avec lequel elles ont été enregistrées à l’origine. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Terme de recherche VRB par défaut (Visual Rule Builder) </p> </td> 
      <td colname="col2"> <p> Permet de personnaliser le terme de recherche initial utilisé dans Visual Rule Builder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Recherche par défaut VRB </p> </td> 
      <td colname="col2"> <p>Ce paramètre vous permet de définir la recherche par défaut initialement sélectionnée dans Visual Rule Builder. </p> <p> Ce paramètre n’est utile que pour l’implémentation avec plusieurs recherches. Le VRB vous permet de sélectionner la recherche à laquelle le déclencheur ou l'action auquel s'applique le groupe défini. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>VRB / Délai d’expiration du simulateur </p> </td> 
      <td colname="col2"> <p>Le VRB et le simulateur envoient des recherches via un serveur proxy qui sont plus lentes que la recherche de production. Dans certaines circonstances, comme le chargement lent des ressources, le VRB ou le simulateur peut expirer. Vous pouvez augmenter, ou diminuer, le nombre de secondes que l’interface utilisateur doit attendre avant de s’arrêter. Vous devez rarement augmenter ce paramètre par rapport à la valeur par défaut de 60. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.

## Configuration de l’accès à votre compte Dynamic Media Classic Adobe {#task_CEFF88C2033D41D0B2FE86C435EDAC6D}

Liez votre compte de recherche/marchandisage de site à l’Adobe Dynamic Media Classic afin que vous puissiez facilement ajouter des bannières publicitaires à votre site Web à l’aide de ressources numériques téléchargées depuis Adobe Scene7.

Voir [A propos des bannières](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA).

Voir [Ajouter une bannière à l’aide d’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

**Pour configurer l’accès à votre compte Adobe Dynamic Media Classic**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Scene7 Configuration]**.
1. Sur la page [!DNL Scene7 Configuration], définissez les options de votre choix.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Région </p> </td> 
      <td colname="col2"> <p>Requis. Identifie la région du monde où votre compte Dynamic Media Classic accède aux différents serveurs Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Société par défaut </p> </td> 
      <td colname="col2"> <p>Identifie le nom de la société associée à votre compte Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Courrier électronique </p> </td> 
      <td colname="col2"> <p>Requis. Identifie votre adresse électronique utilisée pour la connexion et les communications Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mot de passe </p> </td> 
      <td colname="col2"> <p>Requis. Votre mot de passe de connexion Dynamic Media Classic. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active tous les contrôles Dynamic Media Classic dans la recherche/le marchandisage sur le site. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test </p> </td> 
      <td colname="col2"> <p>Vérifie que le nom de la région Dynamic Media Classic, l’adresse électronique et le mot de passe sont corrects. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Cliquez sur **[!UICONTROL Test]** pour vérifier que le nom de la région Dynamic Media Classic, l’adresse électronique et le mot de passe sont corrects.
1. Cliquez sur **[!UICONTROL Save Changes]**.

## Configuration du redirecteur Adobe Analytics {#task_2C9DE333FD7246E4A460FC0F55204160}

Si vous utilisez [!DNL Adobe Analytics] pour le suivi des visiteurs de site, vous pouvez utiliser [!DNL Adobe Analytics Redirector] dans la recherche/marchandisage de site pour effectuer le suivi de toutes les redirections HTTP avec [!DNL Adobe Analytics].

**Pour configurer le redirecteur Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Adobe Analytics Redirector]**.
1. Sur la page [!DNL Adobe Analytics Redirector], définissez les options de votre choix.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Activer la fonction Redirecteur Adobe Analytics </p> </td> 
      <td colname="col2"> <p>Active le suivi des redirections HTTP avec Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Serveur de suivi </p> </td> 
      <td colname="col2"> <p> Identifie le nom du serveur de suivi Adobe Analytics. </p> <p>Pour connaître le nom du serveur de suivi, </p> <p> 
      <ol id="ol_D17B77E81F8D40D0948415CD60839BE3"> 
      <li id="li_BE58DBA104D44F0DB6C64AD3F12CEA97"> En Adobe Analytics, cliquez sur <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Gestionnaire de code </span>. </li> 
      <li id="li_67A93D17C3A14874928C6DC4FF2D4784"> Dans la zone de groupe <span class="wintitle"> Options </span>, sélectionnez une suite de rapports dans la liste déroulante correspondante. </li> 
      <li id="li_5AAB004AC58441DBB0F813BDE30EFFD4"> Cliquez sur <span class="uicontrol">Générer le code </span>. </li> 
      <li id="li_E80368993F4D4DD69E37509FF4348B36"> Sur la page <span class="wintitle"> Gestionnaire de code </span>, cliquez sur l’onglet <span class="uicontrol"> Fichier Javascript principal </span>. </li> 
      <li id="li_991BDCDDA41A445F85CEEAAE9A46A304"> Dans <span class="wintitle"> Config Section </span>, recherchez la ligne qui ressemble à ce qui suit : <p> <code> s.trackingServer="yourcompany.122.2o7.net" </code> </p> <p>Dans ce cas, le nom du serveur de suivi est <span class="codeph"> "yourcompany.122.2o7.net" </span> </p> </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Identifiant de suite de rapports </p> </td> 
      <td colname="col2"> <p> Identifie votre identifiant de suite de rapports. </p> <p>Pour connaître l'identifiant de votre suite de rapports, </p> <p> 
      <ol id="ol_4FD7B2459358486DBDB130426131D16A"> 
      <li id="li_9AF624CEB128453C808892EEE385D5D1"> En Adobe Analytics, cliquez sur <span class="uicontrol"> Admin </span> &gt; <span class="uicontrol"> Admin Console </span> &gt; <span class="uicontrol"> Report Suites </span>. </li> 
      <li id="li_AAC47EAA04144A67BDCB5C7B8D8098E9"> Consultez la colonne <span class="wintitle"> Identifiant de Report Suite </span> du tableau pour trouver l’identifiant. </li> 
      </ol> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètres personnalisés </p> </td> 
      <td colname="col2"> <p>Permet d’ajouter des paramètres personnalisés à l’URL de redirection Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Définissez la casse de toutes les valeurs personnalisées sur </p> </td> 
      <td colname="col2"> <p>Vous permet de normaliser le boîtier utilisé pour toutes les valeurs de paramètre personnalisées que vous avez indiquées ci-dessus. Adobe Analytics étant sensible à la casse, il existe une raison d’unifier la casse des valeurs. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Adobe Analytics Redirector], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuration des fichiers racine {#task_5F175C8743FB49A2A003813CBF7C56BF}

Gérez les fichiers racine dans le dossier racine de votre site Web.

**Pour configurer les fichiers racine**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Root Files]**.
1. Sur la page [!DNL Root Files], accédez aux fichiers racine à télécharger.

   <table> 
    <thead> 
    <tr> 
      <th colname="col1" class="entry"> <p>Fichier racine </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
      <td colname="col1"> <p>favicon.ico </p> </td> 
      <td colname="col2"> <p> Icône du site. En règle générale, elle s’affiche dans la barre d’adresse du navigateur du client. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>robots.txt </p> </td> 
      <td colname="col2"> <p>Permet ou interdit aux robots d’accéder à certaines parties du site Web. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>sitemap.xml </p> </td> 
      <td colname="col2"> <p>Fichier XML contenant une liste de toutes les pages disponibles sur le site Web. </p> </td> 
    </tr> 
    <tr> 
      <td colname="col1"> <p>crossdomain.xml </p> </td> 
      <td colname="col2"> <p>Permet ou refuse au Flash Player d’accéder aux fichiers entre domaines. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Root Files], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Transfert de la propriété du compte à un autre utilisateur de compte {#task_47E3C66CC6374274830DA10171E0CF17}

En tant que propriétaire de compte, si vous avez l’intention d’annuler votre connexion, vous devez d’abord transférer la propriété à un autre utilisateur principal du compte. Vous pouvez utiliser [!DNL Transfer Ownership] pour accomplir cette tâche.

Vous pouvez transférer la propriété à tout utilisateur de compte de recherche/marchandisage de site existant.

Une fois le transfert de propriété terminé, le nouveau titulaire du compte reçoit un avis par courriel et l&#39;ancien propriétaire est déchargé des restrictions et responsabilités de ce poste.

Il ne peut y avoir qu&#39;un seul propriétaire par compte. Si vous transférez votre propriété à un autre utilisateur, vous n’avez plus de droits de propriété.

Voir [Annulation de votre connexion](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Voir [Suppression d’un compte](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Voir [Vous retirer d&#39;un compte](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

**Pour transférer la propriété du compte vers un autre compte**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Transfer Ownership]**.
1. Sur la page [!DNL Transfer Ownership], cliquez sur l’utilisateur qui doit être propriétaire de votre compte.
1. Cliquez sur **[!UICONTROL Transfer]**.

## Suppression d&#39;un compte {#task_975178D5B9444BF8B52D72B897A49C32}

Vous pouvez supprimer entièrement un compte de la recherche/marchandisage sur le site. Dans ce cas, vous et les autres utilisateurs de votre compte n’y avez plus accès.

Lorsque vous supprimez votre compte, il ne peut plus être utilisé pour indexer ou rechercher votre site actif. Aussi,

Pour permettre à d’autres utilisateurs de continuer à utiliser ce compte, vous pouvez transférer la propriété à un autre utilisateur, puis vous retirer en tant qu’utilisateur du compte.

Voir [Transfert de la propriété du compte à un autre utilisateur de compte](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

Si vous disposez d’autres comptes, après avoir supprimé le compte actuel, vous êtes dirigé vers le premier compte répertorié dans votre ouverture de session.

Voir [Vous retirer d&#39;un compte](../c-about-settings-menu/c-about-account-options-menu.md#task_C56F5AB87B664BAAAC2FD2F15003E73F).

Voir [Annulation de votre connexion](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

**Pour supprimer un compte**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Account]**.
1. (Facultatif) Dans le champ [!DNL Reason for Removal], entrez un motif de suppression du compte.
1. Cliquez sur **[!UICONTROL Remove Account]**.

## Vous retirer d&#39;un compte {#task_C56F5AB87B664BAAAC2FD2F15003E73F}

Vous pouvez vous retirer d&#39;un compte de recherche/marchandisage de site.

Lorsque vous vous supprimez d’un compte, vous ne pouvez plus y accéder et vous ne pouvez pas modifier les paramètres du compte ni indexer votre site avec celui-ci.

Pour récupérer l’accès au compte, demandez à un utilisateur du compte actuel de vous rétablir.

Voir [Annulation de votre connexion](../c-about-settings-menu/c-about-my-profile-menu.md#task_D57701BB726243B08CEA14EEC86C3087).

Voir [Suppression d’un compte](../c-about-settings-menu/c-about-account-options-menu.md#task_975178D5B9444BF8B52D72B897A49C32).

Voir [Transfert de la propriété du compte à un autre utilisateur de compte](../c-about-settings-menu/c-about-account-options-menu.md#task_47E3C66CC6374274830DA10171E0CF17).

**Pour vous retirer d’un compte**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Remove Yourself]**.
1. Cliquez sur **[!UICONTROL Remove Yourself]**.
