---
description: Utilisez le menu Adobe Analytics pour configurer l’authentification des mesures Adobe Analytics, gérer les mesures Adobe Analytics d’une suite de rapports ou utiliser le SAINT pour améliorer les rapports Adobe Analytics en acceptant les données tabulaires provenant de sources externes.
solution: Target
subtopic: Adobe Analytics
title: A propos du menu Adobe Analytics
topic-legacy: Settings,Site search and merchandising
uuid: 5536edf1-d3a4-47af-a307-6e46f385f738
exl-id: e1f7b8f0-45d4-457a-a9d3-a8cb4b785059
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '3407'
ht-degree: 1%

---

# A propos du menu Adobe Analytics{#about-the-adobe-analytics-menu}

Utilisez le menu Adobe Analytics pour configurer l’authentification des mesures Adobe Analytics, gérer les mesures Adobe Analytics d’une suite de rapports ou utiliser le SAINT pour améliorer les rapports Adobe Analytics en acceptant les données tabulaires provenant de sources externes.

## Configuration de l&#39;authentification des mesures Adobe Analytics {#task_8AA93F6273B747F9B4DE9E8DFBCBDC42}

Pour incorporer des mesures Adobe Analytics dans les classements de recherche/marchandisage de votre site, vous devez d&#39;abord vous connecter aux services Web Adobe Analytics. Après avoir obtenu les informations de connexion, vous pouvez les utiliser pour configurer l’authentification Adobe Analytics dans la recherche/marchandisage de site.

**Pour configurer l&#39;authentification des mesures Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Authentication]**.
1. Sur la page [!DNL Setup Adobe Analytics Metrics Authentication], spécifiez les informations demandées dans chaque champ.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Champ de texte </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom de la Société de l’Adobe Analytics </p> </td> 
      <td colname="col2"> <p>Paramètre Nom de la Société utilisé pour se connecter à votre compte Adobe Analytics. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom d’utilisateur des services web </p> </td> 
      <td colname="col2"> <p>Nom d’utilisateur des services Web associé à votre compte Adobe Analytics. </p> <p>Vous pouvez obtenir ces informations en Adobe Analytics. Dans la barre de menus Adobe Analytics, cliquez sur <span class="uicontrol"> <b>Admin</b> </span> &gt; <span class="uicontrol"> <b>Admin Console</b> </span> &gt; <span class="uicontrol"> <b>Société</b> </span> &gt; <span class="uicontrol"> <b>Web Services</b> </span>. Les informations se trouvent dans le tableau Informations d'accès à l'API. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Secret partagé des services Web </p> </td> 
      <td colname="col2"> <p>Secret partagé des services Web associé à votre compte Adobe Analytics. </p> <p>Vous pouvez obtenir ces informations en Adobe Analytics. Dans la barre de menus Adobe Analytics, cliquez sur <span class="uicontrol"> <b>Admin</b> </span> &gt; <span class="uicontrol"> <b>Admin Console</b> </span> &gt; <span class="uicontrol"> <b>Société</b> </span> &gt; <span class="uicontrol"> <b>Web Services</b> </span>. Les informations se trouvent dans le tableau Informations d'accès à l'API. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des suites de rapports Adobe Analytics {#concept_1A51AEC5D40E459B813E7891D64B1BAE}

Pour utiliser les données de la suite de rapports Adobe Analytics dans le cadre de la recherche/marchandisage sur le site, vous devez d’abord créer des copies des données Adobe Analytics dans votre compte de recherche/marchandisage sur le site.

Vous pouvez créer de nouvelles définitions de Report Suites Adobe Analytics ou vous pouvez vue ou modifier vos Report Suites Adobe Analytics existantes et les mesures associées.

La première fois que vous accédez à Adobe Analytics à partir de la recherche/du marchandisage sur le site, une liste des Report Suites disponibles pour votre société est téléchargée et mise en cache. Si de nouvelles suites de rapports ont été ajoutées récemment ou si des suites existantes ont été supprimées, vous pouvez actualiser la liste de suite de rapports pour télécharger à nouveau la liste des suites de rapports.

## Ajouter une suite de rapports Adobe Analytics {#task_6DE17305EA7146DA8C30FF8FDF68A3C0}

Vous pouvez sélectionner une Report Suite Adobe Analytics sur laquelle baser les règles de classement de recherche/marchandisage de votre site.

La liste que vous pouvez sélectionner doit correspondre aux Report Suites disponibles dans votre compte Adobe Analytics. La suite de rapports sélectionnée détermine les mesures disponibles pour l’utilisation dans les règles de classement de recherche/marchandisage de votre site.

Voir [A propos des règles de classement](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Après avoir ajouté une suite de rapports Adobe Analytics, vous pouvez modifier ses mesures.

Voir [Modification des mesures Adobe Analytics d’une suite de rapports](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**Pour ajouter une suite de rapports Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Sur la page Adobe Analytics Report Suites, cliquez sur **[!UICONTROL Add Report Suite]**.
1. Dans la liste déroulante de la ligne de tableau nouvellement ajoutée, sélectionnez la Report Suite de votre choix.
1. Modifiez les mesures Adobe Analytics d’une suite de rapports.

## Modification des mesures Adobe Analytics d’une suite de rapports {#task_360904CCBBB140238ADA036C3CC07664}

Pour incorporer des mesures Adobe Analytics dans vos règles de classement dans la recherche/le marchandisage sur site, sélectionnez une ou plusieurs des mesures associées à la suite de rapports sélectionnée. Ensuite, vous configurez les options utilisées pour récupérer les données de mesure au moyen du service Web Adobe Analytics.

Voir [Ajouter une suite de rapports Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

Voir [Configuration des options Adobe Analytics avancées](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_C0FF2D69F59D44D8943A7831ED7FEC19).

**Pour modifier les mesures Adobe Analytics d’une suite de rapports**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Sur la page [!DNL Adobe Analytics Report Suites], sous la colonne **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Edit]** pour la suite de rapports dont vous souhaitez configurer les mesures.
1. Sur la page [!DNL Edit Adobe Analytics Metrics], définissez les mesures requises. Les mesures qui ne comportent pas d’astérisque (*) en regard du nom de la mesure sont facultatives.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Suite de rapports </p> </td> 
      <td colname="col2"> <p>Affiche le nom de la Report Suite que vous avez ajoutée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom de la Report Suite Vue </p> </td> 
      <td colname="col2"> <p>Fournit un nom "alias" pour le nom de la suite de rapports Adobe Analytics. Cet autre nom est utile si la même suite de rapports est utilisée dans plusieurs définitions. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sélectionner le type de rapport </p> </td> 
      <td colname="col2"> <p>Indique la valeur de type de rapport à utiliser avec la Report Suite sélectionnée. La valeur identifie la clé pour chaque ligne de résultats renvoyée. </p> <p>Le type de rapport est également connu sous le nom d’élément Adobe Analytics. </p> <p>Cette mesure est requise. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du champ de référence croisée </p> </td> 
      <td colname="col2"> <p>Indique un champ de métadonnées dont les valeurs sont utilisées comme "clés" de recherche dans les données de la suite de rapports. </p> <p>Si aucune valeur n’est sélectionnée ("— Aucune —"), les données de cette suite de rapports ne sont pas disponibles pour les calculs de classement ( <span class="uicontrol"> <b>Règles</b> </span> &gt; <span class="uicontrol"> <b>Règles de classement</b> </span> &gt; <span class="uicontrol"> <b>Modifier les règles</b> &lt;a 11/&gt;).</span> </p> <p>Lorsque vous sélectionnez une valeur, les valeurs de ce champ sont utilisées pour référencer les documents de recherche/marchandisage de site avec les données Adobe Analytics de cette suite de rapports, en utilisant la valeur de type de rapport sélectionnée que vous avez définie précédemment. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rapport Termes de recherche </p> </td> 
      <td colname="col2"> <p>Permet de créer des règles de fonctionnement et de simuler des termes de recherche à partir de la page <b>Prévisualisation de données Adobe Analytics Stage</b>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0" type="task" format="dita" scope="local">Prévisualisation des données Adobe Analytics</a>. </p> <p>Un menu déroulant s’affiche sur chaque ligne et propose deux options : <b>Simuler le terme de recherche</b> et <b>Créer une nouvelle règle de fonctionnement</b>. </p> <p>Les deux options utilisent les données du type de rapport comme termes de recherche. Par conséquent, cette fonctionnalité n'a de sens que si le type de rapport représente des termes de recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mesures </p> </td> 
      <td colname="col2"> <p>Identifie les valeurs de mesure que vous souhaitez télécharger et utiliser dans les règles de classement de recherche/marchandisage de votre site. </p> <p>Les mesures que vous configurez ici apparaissent comme des choix dans les <span class="uicontrol"> <b>Règles</b> </span> &gt; <span class="uicontrol"> <b>Règles de classement</b> </span> &gt; <span class="uicontrol"> <b>Modifier les règles</b> </span> pages du centre des membres, lorsque le type de données de la règle est défini <span class="uicontrol"> Adobe Analytics Metric (Number) </span>. Les choix indiquent une combinaison des noms des Report Suites ou des noms des Report Suites de Vue, le cas échéant, et des noms des mesures individuelles. </p> <p>Cette mesure est requise. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de mesure minimale </p> </td> 
      <td colname="col2"> <p>Permet de saisir une valeur non nulle pour spécifier une valeur minimale pour la mesure. </p> <p>Si la valeur est vide ou nulle, toutes les valeurs de la mesure sont téléchargées ; sinon, le téléchargement de cette mesure s’arrête lorsque la valeur minimale de la mesure est transmise. </p> <p>Les mesures Adobe Analytics sont récupérées dans un ordre décroissant. </p> <p>Cliquez sur <span class="uicontrol"> <b>+</b> </span> pour ajouter des définitions de mesure supplémentaires ; cliquez sur <span class="uicontrol"> <b>-</b> </span> pour supprimer les définitions de mesure dont vous n’avez plus besoin ou que vous ne souhaitez plus. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Période d’agrégation des mesures Adobe Analytics (en jours) </p> </td> 
      <td colname="col2"> <p> Contrôle le nombre de jours de mesures Adobe Analytics à récupérer, en comptant depuis la date d’hier. Aucune tentative de récupération des données du jour en cours n'est effectuée. </p> <p>La valeur par défaut est de 7. </p> <p>Cette mesure est requise. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fréquence d’actualisation des téléchargements Adobe Analytics (jours) </p> </td> 
      <td colname="col2"> <p> Définit l’intervalle minimum entre les téléchargements des données Adobe Analytics utilisées dans les calculs de classement. </p> <p>Les téléchargements déclenchés par l’index qui se produisent dans l’intervalle de fréquence d’actualisation des téléchargements sont ignorés. Cependant, les téléchargements manuels ignorent cette valeur. </p> <p>Lorsque vous définissez cette valeur sur la valeur par défaut 1, les données Adobe Analytics ne sont pas téléchargées plusieurs fois au cours d’une période de 24 heures. Tous les index de recherche qui surviennent dans l’intervalle de fréquence d’actualisation des téléchargements utilisent le dernier jeu de données téléchargé. </p> <p>Cette mesure est requise. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Voir aussi [A propos des règles de classement](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).
1. Cliquez sur **[!UICONTROL Save Changes]**.

   Vous revenez à la page de mise en scène [!DNL Adobe Analytics Report Suites].
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une suite de rapports Adobe Analytics {#task_0ACA172214D14654ABDB139F417B9F7D}

Vous pouvez utiliser Supprimer pour supprimer une suite de rapports de la page [!DNL Adobe Analytics Report Suites]. La suppression d&#39;une suite de rapports supprime uniquement la copie des données des serveurs de recherche/marchandisage du site ; elle n&#39;a aucune incidence sur les données des systèmes Adobe Analytics.

**Pour supprimer une Report Suite Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Sur la page [!DNL Adobe Analytics Report Suites], sous la colonne **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Delete]** pour la suite de rapports à supprimer.
1. Sur la page [!DNL Adobe Analytics Delete Report Suite], cliquez sur **[!UICONTROL Delete]**.

## Aperçu des données Adobe Analytics {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Vous pouvez utiliser la Prévisualisation pour vue vos dernières mesures Adobe Analytics chargées.

La colonne Ligne du tableau affiche le nombre de chaque ligne de données de mesure, indiquant l’ordre de chargement initial des mesures Adobe Analytics.

La colonne Produit affiche l’élément Adobe Analytics associé à chaque ligne de données de mesure. Les valeurs de cette colonne sont utilisées pour associer les pages de recherche/marchandisage de votre site à leurs valeurs de mesure correspondantes, telles que configurées dans vos définitions de classement.

Voir [A propos des règles de classement](../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397).

Voir [Configuration du classement](../c-about-rules-menu/c-about-ranking-rules.md#task_4CEBC13925B047FC95BDC217B48089C5).

Les autres colonnes affichent les valeurs de mesure associées à chaque entrée.

Si le tableau est vide, cela signifie que vous n’avez pas encore chargé de données Adobe Analytics. Vous pouvez fermer la page [!DNL Adobe Analytics Data Preview], puis charger les données Adobe Analytics.

Voir [Chargement des données Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).
Si le tableau a été désigné comme rapport de termes de recherche, un petit triangle apparaît sur chaque ligne. Vous pouvez cliquer sur la liste déroulante et sélectionner **Simuler le terme de recherche** ou **Créer une nouvelle règle de fonctionnement**. L&#39;action que vous sélectionnez est appliquée au terme de recherche de cette ligne, les données résidant dans la deuxième colonne.

**Pour prévisualisation des données Adobe Analytics**

1. Dans le menu produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**. Sur la page [!DNL Adobe Analytics Report Suites], sous la colonne [!DNL Actions], cliquez sur **[!UICONTROL Preview]** pour la suite de rapports dont vous voulez vue les données téléchargées.

   * Cliquez sur **[!UICONTROL Reports]** > **[!UICONTROL Adobe Analytics Terms Reports]**. Sur la page [!DNL Adobe Analytics Terms Report], sous la colonne [!DNL Actions], cliquez sur **[!UICONTROL Preview]** pour la suite de rapports dont vous voulez vue les données téléchargées.

1. Sur la page [!DNL Adobe Analytics Data Preview], utilisez les options de navigation et d’affichage en haut et en bas de la page pour vue les données.

   Cliquez sur un en-tête de colonne du tableau pour trier les données par ordre croissant ou décroissant.
1. Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Download to Desktop]** pour télécharger et enregistrer le tableau dans un fichier `.xlt`.

   * Fermez la page lorsque vous avez terminé de prévisualiser les données Adobe Analytics et revenez à la page précédemment consultée.

## Affichage du journal à partir du chargement de données Adobe Analytics le plus récent {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Vous pouvez utiliser le journal des Vues pour examiner le fichier journal des données Adobe Analytics du processus de téléchargement le plus récent. Vous pouvez également utiliser la vue de journal pour surveiller un téléchargement en cours d’exécution.

Voir [Chargement des données Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Pour vue du journal à partir du chargement de données Adobe Analytics le plus récent**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Sur la page [!DNL Adobe Analytics Report Suites], cliquez sur **[!UICONTROL View Log]**. Page de journal,
1. Sur la page [!DNL Adobe Analytics Data Log], utilisez les options de navigation et d’affichage en haut et en bas de la page pour vue les informations du journal.
1. Lorsque vous avez terminé, fermez la page pour revenir à la page [!DNL Adobe Analytics Report Suites].

## Chargement des données Adobe Analytics {#task_2F3C55189B0A4049AB2113F2291CC181}

Vous pouvez télécharger les données de la suite de rapports Adobe Analytics configurées dans la recherche/le marchandisage sur le site.

La page Chargement des données affiche l’état de votre dernière opération de chargement des données Adobe Analytics avec les informations suivantes :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Champ Statut </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>État </p> </td> 
   <td colname="col2"> <p>Indique la réussite ou l’échec de la dernière tentative de chargement de données. Ou, il affiche l’état d’une opération de chargement de données déjà en cours. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Résultats </p> </td> 
   <td colname="col2"> <p>Affiche le nombre de lignes de données de mesure téléchargées lors de la dernière tentative de chargement des données. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Heure de début </p> </td> 
   <td colname="col2"> <p>Affiche la date et l’heure auxquelles la dernière opération de chargement de données a démarré. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Heure d’arrêt </p> </td> 
   <td colname="col2"> <p>Affiche la date et l’heure de fin de la dernière opération de chargement de données. Il indique également que l’opération de chargement de données en cours est toujours en cours. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Pour charger les données Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Sur la page [!DNL Stage Adobe Analytics Report Suites], cliquez sur **[!UICONTROL Load Adobe Analytics Data]**.
1. Sur la page **[!UICONTROL Adobe Analytics Data Load]**, effectuez l&#39;une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Start Load]** pour début de l&#39;opération de chargement.

      Lors d’une opération de chargement de données, la ligne **Progress** fournit des informations sur son avancement.

   * Cliquez sur **[!UICONTROL Stop Load]** pour arrêter l&#39;opération de chargement.

1. Cliquez sur **[!UICONTROL Close]** pour revenir à la page [!DNL Stage Adobe Analytics Reports Suite].

## Actualisation de la liste de Report Suite {#task_EA6215D438CA4185B106657D9712ED34}

La première fois que vous accédez à Adobe Analytics à partir de l’interface utilisateur de recherche/marchandisage du site, une liste de vos Report Suites Adobe Analytics disponibles est téléchargée et mise en cache. Si de nouvelles Report Suites ont été ajoutées récemment ou si des Report Suites existantes ont été supprimées, vous pouvez utiliser la Liste Actualiser la Report Suite pour mettre à jour la liste actuellement affichée dans la recherche/marchandisage sur le site.

Voir [Ajouter une suite de rapports Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_6DE17305EA7146DA8C30FF8FDF68A3C0).

Voir [Suppression d’une suite de rapports Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_0ACA172214D14654ABDB139F417B9F7D).

**Pour actualiser la liste de Report Suites**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Metrics]**.
1. Sur la page [!DNL Adobe Analytics Report Suites], cliquez sur **[!UICONTROL Refresh Report Suite List]**.

## Configuration des options Adobe Analytics avancées {#task_C0FF2D69F59D44D8943A7831ED7FEC19}

Vous pouvez utiliser [!DNL Advanced Adobe Analytics Options] pour contrôler les paramètres destinés à vous aider à affiner le comportement du processus de téléchargement de la suite de rapports Adobe Analytics.

Voir [Modification des mesures Adobe Analytics d’une suite de rapports](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_360904CCBBB140238ADA036C3CC07664).

**Pour configurer les options Adobe Analytics avancées**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL Advanced Options]**.
1. Sur la page [!DNL Advanced Adobe Analytics Options], définissez les options suivantes :

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Lignes maximales, toute mesure </p> </td> 
      <td colname="col2"> <p>Paramètre d’optimisation qui empêche le téléchargement d’un trop grand nombre de données Adobe Analytics. </p> <p>Si vous définissez cette option sur une valeur non nulle, la récupération des données Adobe Analytics est arrêtée lorsque le nombre total de lignes extraites pour chaque mesure dépasse la valeur spécifiée. </p> <p>La valeur par défaut est 0 ; aucune valeur maximale appliquée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mesure Répétition de la taille de récupération (lignes) </p> </td> 
      <td colname="col2"> <p> Contrôle le nombre de valeurs de mesure Adobe Analytics à récupérer à la fois. Les lignes de données de mesure sont récupérées à plusieurs reprises jusqu’à ce que toutes les données soient récupérées ou jusqu’à ce que la limite de lignes maximale soit atteinte. </p> <p>Normalement, vous n'avez pas besoin de modifier ce paramètre. Cependant, il peut s’avérer utile d’optimiser la phase de téléchargement des mesures d’une réindexation complète de votre site. </p> <p>La valeur par défaut est 5000. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des flux de classification de SAINT {#concept_C55609DA24914BBC92CD90ED0259199D}

Vous pouvez utiliser le SAINT Adobe Analytics pour améliorer vos rapports d’analyse en acceptant les données tabulaires provenant de sources externes. Par exemple, vous pouvez utiliser la recherche/marchandisage sur site pour récupérer les données de ses propres index et les exporter vers Adobe Analytics.

Pour utiliser correctement la fonction SAINT Adobe Analytics dans la recherche/le marchandisage sur site, tenez compte des exigences suivantes :

* Vous devez disposer d’une société Adobe Analytics et d’une suite de rapports.

   Voir [A propos du menu Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#concept_5FD2D13C9D0D40988E6E51480D690411).
* Le compte utilisateur Adobe Analytics doit disposer de privilèges pour modifier la suite de rapports.

   Voir [Configuration de l’authentification des mesures Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_8AA93F6273B747F9B4DE9E8DFBCBDC42).
* L&#39;utilisateur Adobe Analytics doit appartenir au groupe API Web pour pouvoir utiliser l&#39;API Web Adobe Analytics.
* L&#39;index de recherche doit contenir des données que Adobe Analytics peut utiliser, telles que des données au format correct.

Avant de créer un flux, passez en revue les questions et informations suivantes afin de pouvoir exécuter l’assistant de flux de SAINT avec succès :

* Avec quelle suite de rapports allez-vous travailler ?
* Quel jeu de classifications, tel que product, e-var, etc., allez-vous fournir des données ?
* Quelles classifications existent dans les rapports ? La réponse à cette question est déterminée par le type de données qui est facilement disponible à partir de la recherche/marchandisage sur le site et le type de rapports que Adobe Analytics signale comme désirable.
* SAINT accepte les données issues de la recherche/marchandisage sur le site sous la forme d’un type de texte. Le format de ces données a un impact sur la présentation des rapports Adobe Analytics.

## Création d’un flux de SAINT Adobe Analytics {#task_914B5AB821E84627953D8EF9339A7DD0}

Vous pouvez utiliser Adobe Analytics SAINT pour améliorer les rapports Adobe Analytics en acceptant les données tabulaires provenant de sources externes.

Par exemple, vous pouvez utiliser la recherche/marchandisage sur site pour récupérer des données de ses propres index et les exporter vers Adobe Analytics.

**Pour créer un flux de SAINT Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Sur la page [!DNL SAINT Classification Feeds], cliquez sur **[!UICONTROL Create SAINT Feed]**.
1. Dans la boîte de dialogue [!DNL Create Feed], dans le champ de texte **Nom du flux**, saisissez le nouveau nom du flux, puis cliquez sur **[!UICONTROL Next]**.

   A ce stade, le flux est enregistré et ajouté à la page [!DNL SAINT Classification Feed]. Si vous le souhaitez, vous pouvez quitter le flux et le modifier ultérieurement pour terminer l’assistant.
1. Sur la page [!DNL Authentication], spécifiez le nom de la société Adobe Analytics, le nom d’utilisateur et le secret Web dans les champs de texte respectifs, puis cliquez sur **[!UICONTROL Next]**.

   Assurez-vous qu’il est autorisé à utiliser l’API Web avec Adobe Analytics.
1. Sur la page **[!UICONTROL Report Suite]**, choisissez une suite de rapports et son jeu de données de classification, puis cliquez sur **[!UICONTROL Next]**.
1. Sur la page [!DNL Field Maps], faites correspondre les classifications Adobe Analytics avec les champs de métadonnées de recherche/marchandisage de site, puis cliquez sur **[!UICONTROL Next]**.

   Pour ajuster les classifications Adobe Analytics, cliquez sur **[!UICONTROL Edit]** Classifications Adobe Analytics pour vous connecter à Adobe Analytics. Une fois les modifications effectuées, cliquez sur **[!UICONTROL Refresh Classifications]** pour actualiser les choix de classifications.
1. Sur la page [!DNL Search Criteria], les données issues de la recherche/marchandisage sur le site peuvent être filtrées avant d’être envoyées au SAINT Adobe Analytics. Créez ici des règles de filtrage à l’aide de l’interface du créateur de règles, puis cliquez sur **[!UICONTROL Next]**.
1. Sur la page [!DNL Configure FTP], sélectionnez le serveur FTP. Indiquez la fréquence de téléchargement des données, puis cliquez sur **[!UICONTROL Next]**.

   En règle générale, chaque flux possède son propre compte FTP afin d’éviter la perte accidentelle de données. Vous pouvez créer un nouveau compte FTP Adobe Analytics ici.
1. Sur la page [!DNL Verification], cliquez sur **[!UICONTROL Show Data View]** pour examiner la représentation de la vue de données de la sortie. S’il existe des fichiers de flux réels, ils sont répertoriés ici et peuvent être téléchargés.
1. Cliquez sur **[!UICONTROL Close]**.

## Modification d’un flux de SAINT Adobe Analytics {#task_5BF34D02D0D14359B1CF4B3C1B0ACC84}

Vous pouvez modifier tous les aspects d’un flux de SAINT existant que vous avez créé.

**Pour modifier un flux de SAINT Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Sur la page [!DNL Saint Classification Feeds], sous la colonne **[!UICONTROL Name]**, dans la liste déroulante en regard d’un flux, cliquez sur **[!UICONTROL Edit feed]**.
1. Dans la boîte de dialogue de flux de SAINT, dans le champ **Nom du flux**, saisissez le nouveau nom du flux, puis cliquez sur **[!UICONTROL Next]**.

   A ce stade, le flux est enregistré et ajouté à la page [!DNL SAINT Classification Feed]. Si vous le souhaitez, vous pouvez quitter le flux et le modifier ultérieurement pour terminer l’assistant.
1. Sur la page [!DNL Authentication], spécifiez le nom de la société Adobe Analytics, le nom d’utilisateur et le secret Web dans les champs de texte respectifs, puis cliquez sur **[!UICONTROL Next]**.

   Assurez-vous qu’il est autorisé à utiliser l’API Web avec Adobe Analytics.
1. Sur la page **[!UICONTROL Report Suite]**, choisissez une suite de rapports et son jeu de données de classification, puis cliquez sur **[!UICONTROL Next]**.
1. Sur la page [!DNL Field Maps], faites correspondre les classifications Adobe Analytics avec les champs de métadonnées de recherche/marchandisage de site, puis cliquez sur **[!UICONTROL Next]**.

   Pour ajuster les classifications Adobe Analytics, cliquez sur **[!UICONTROL Edit]** Classifications Adobe Analytics pour vous connecter à Adobe Analytics. Une fois les modifications effectuées, cliquez sur **[!UICONTROL Refresh Classifications]** pour actualiser les choix de classifications.
1. Sur la page [!DNL Search Criteria], les données issues de la recherche/marchandisage sur le site peuvent être filtrées avant d’être envoyées au SAINT Adobe Analytics. Créez ici des règles de filtrage à l’aide de l’interface du créateur de règles, puis cliquez sur **[!UICONTROL Next]**.
1. Sur la page [!DNL Configure FTP], sélectionnez le serveur FTP. Indiquez la fréquence de téléchargement des données, puis cliquez sur **[!UICONTROL Next]**.

   En règle générale, chaque flux possède son propre compte FTP afin d’éviter la perte accidentelle de données. Vous pouvez créer un nouveau compte FTP Adobe Analytics ici.
1. Sur la page [!DNL Verification], cliquez sur **[!UICONTROL Show Data View]** pour examiner la représentation de la vue de données de la sortie. S’il existe des fichiers de flux réels, ils sont répertoriés ici et peuvent être téléchargés.
1. Cliquez sur **[!UICONTROL Close]**.

## Suppression d’un flux de SAINT Adobe Analytics {#task_5319B1F4CA1A406393CFD7AE97258CEB}

Vous pouvez supprimer un flux de SAINT Adobe Analytics existant dont vous n’avez plus besoin ou que vous n’utilisez plus.

**Pour supprimer un flux de SAINT Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Sur la page [!DNL Saint Classification Feeds], sous la colonne **[!UICONTROL Name]**, dans la liste déroulante en regard d’un flux à supprimer, cliquez sur **[!UICONTROL Delete feed]**.
1. Dans la boîte de dialogue Supprimer, cliquez sur **Oui** pour vérifier la suppression du flux.

## Affichage d’un fichier de flux de SAINT Adobe Analytics {#task_F0C8BADD25E14E5DB30BF31D1F879FDB}

Vous pouvez ouvrir la page [!DNL Verification] d’un flux de SAINT existant pour examiner la représentation de la vue de données de la sortie.

S’il existe des fichiers de flux réels, ils sont répertoriés ici et peuvent être téléchargés en tant que fichier texte.

**Pour vue d’un fichier de flux de SAINT Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Sur la page [!DNL Saint Classification Feeds], sous la colonne **[!UICONTROL Name]**, dans la liste déroulante en regard d’un flux, cliquez sur **[!UICONTROL View Feed Files]**.
1. (Facultatif) Cliquez sur **[!UICONTROL Download File]** pour enregistrer le fichier de flux dans un fichier texte.
1. Cliquez sur **[!UICONTROL Close]** pour revenir à la page [!DNL SAINT Classification Feeds].

## Test d’un flux de SAINT Adobe Analytics {#task_9864D69BE3824FC29C10B36EE4855D25}

Vous pouvez tester un flux de SAINT Adobe Analytics existant sans téléchargement de fichier.

Voir [Génération et chargement d’un flux de SAINT Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_47AED946AA964334A877FDC8D4F6F00A).

Voir [Affichage d’un fichier de flux de SAINT Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB).

**Pour tester un fichier de flux de SAINT Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Sur la page [!DNL Saint Classification Feeds], sous la colonne **[!UICONTROL Name]**, dans la liste déroulante en regard d’un flux, cliquez sur **[!UICONTROL Test Feed (No file upload)]**.
1. Une fois le traitement du flux terminé, dans la liste déroulante du nom du flux, cliquez sur **[!UICONTROL View Feed Files]**.
1. Sur la page [!DNL Verification], cliquez sur **[!UICONTROL Download File]** pour télécharger le fichier de flux.
1. Cliquez sur **[!UICONTROL Close]** pour revenir à la page [!DNL SAINT Classification Feeds].

## Génération et chargement d’un flux de SAINT Adobe Analytics {#task_47AED946AA964334A877FDC8D4F6F00A}

Vous pouvez générer et télécharger des fichiers de flux pour un flux Adobe Analytics existant que vous avez créé.

Voir [Test d’un flux de SAINT Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_9864D69BE3824FC29C10B36EE4855D25).

Voir [Affichage d’un fichier de flux de SAINT Adobe Analytics](../c-about-settings-menu/c-about-adobe-analytics-menu.md#task_F0C8BADD25E14E5DB30BF31D1F879FDB).

**Pour générer et télécharger un fichier de flux de SAINT Adobe Analytics**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Adobe Analytics]** > **[!UICONTROL SAINT Classification Feeds]**.
1. Sur la page [!DNL Saint Classification Feeds], sous la colonne **[!UICONTROL Name]**, dans la liste déroulante en regard d’un flux, cliquez sur **[!UICONTROL Generate and Upload Feed]**.
1. Une fois le traitement du flux terminé, dans la liste déroulante du nom du flux, cliquez sur **[!UICONTROL View Feed Files]**.
1. Sur la page [!DNL Verification], cliquez sur **[!UICONTROL Download File]** pour télécharger le fichier de flux.
1. Cliquez sur **[!UICONTROL Close]** pour revenir à la page [!DNL SAINT Classification Feeds].
