---
description: Vous pouvez utiliser des règles de fonctionnement pour marchandiser votre recherche.
solution: Target
title: A propos des règles de fonctionnement
topic: Rules,Site search and merchandising
uuid: f2186f54-7a39-4f46-bb29-5115d5a17f07
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '3120'
ht-degree: 1%

---


# A propos des règles de fonctionnement{#about-business-rules}

Vous pouvez utiliser des règles de fonctionnement pour marchandiser votre recherche.

## Utilisation des règles de fonctionnement {#concept_2A93D76216754D3D8412CDEA00BD26BD}

Par exemple, vous pouvez configurer le moment où les bannières s&#39;affichent ou les résultats qui s&#39;affichent et dans quel ordre. Vous pouvez également configurer la position d’un élément dans votre facette et le modèle utilisé pour une recherche donnée. Les règles s&#39;exécutent dans l&#39;ordre dans lequel elles ont été définies ; plus le numéro d’ordre d’une règle est élevé, plus elle s’exécute dans le processus, ce qui l’emporte sur les règles antérieures. Vous pouvez faire glisser les règles pour les modifier ou les réorganiser en entrant un nouveau numéro dans la zone de texte Ordre des règles.

Chaque règle de fonctionnement est composée de déclencheurs et d’actions.

Le déclencheur définit le moment où la règle s’exécute. Par exemple, lorsque le terme de requête est &quot;homme&quot; ou lorsque les résultats sont principalement des chapeaux. Le déclencheur est constitué de plusieurs conditions qui doivent être toutes, ou n’importe lesquelles d’entre elles doivent être vraies pour que le déclencheur global soit vrai. Vous pouvez définir la priorité en modifiant l’opérateur de déclenchement.

L’action définit ce qui se produit lorsque la condition de déclenchement est remplie. Par exemple, la définition de la bannière pour afficher ou déplacer un résultat donné à la position 1. Le tableau des règles affiche des informations récapitulatives sur la règle. Vous pouvez cliquer sur le nom d’une règle pour l’ouvrir et afficher des informations supplémentaires.

Le tableau des règles présente une liste de toutes vos règles de fonctionnement. Par défaut, le tableau affiche les dix dernières règles qui ont été ajoutées, dans l’ordre décroissant. Vous pouvez cliquer sur les en-têtes de colonne du tableau pour trier les règles par ordre croissant ou décroissant.

Les règles de fonctionnement peuvent avoir l’un des trois états suivants : Approuvé, suspendu ou en cours (en cours)

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>État de la règle de fonctionnement </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Approuvés </p> </td> 
   <td colname="col2"> <p>Les règles de fonctionnement approuvées s’exécutent dans votre environnement réel et dans votre environnement d’évaluation. Vous approuvez une règle de fonctionnement dans le Créateur de règles avancé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Suspendu </p> </td> 
   <td colname="col2"> <p>Les règles de fonctionnement suspendues ne s’exécutent jamais dans votre environnement intermédiaire ou dans votre environnement réel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>WIP </p> </td> 
   <td colname="col2"> <p>WIP (Work In Progress) sont des règles de fonctionnement qui ne sont ni approuvées, ni suspendues. En d'autres termes, il se peut que vous travailliez encore sur eux ou que vous souhaitiez d'abord les tester avant de les approuver. Les règles de fonctionnement dans un état en cours ne s'exécutent que dans votre environnement intermédiaire. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous approuvez les règles de fonctionnement et les poussez en direct afin qu’elles s’exécutent dans votre environnement de production. Actuellement, vous ne pouvez transmettre que les règles *all*. Cependant, vous pouvez modifier l’état d’une règle pour contrôler les règles qui s’exécutent et qui ne s’exécutent pas dans votre environnement actif.

Par défaut, les règles s’exécutent chaque fois que leurs déclencheurs associés sont satisfaits. Cependant, vous pouvez éventuellement planifier l’exécution d’une règle pour une période et une période spécifiques.

En outre, par défaut, les règles s’exécutent chaque fois que leurs déclencheurs associés sont satisfaits pour tous les magasins. Si vous souhaitez que la règle s&#39;applique uniquement à certains magasins, vous pouvez utiliser le panneau Magasins pour sélectionner un ou plusieurs magasins auxquels la règle s&#39;applique.

## Ajouter une nouvelle règle de fonctionnement {#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7}

Vous pouvez utiliser [!DNL Visual Rule Builder] ou [!DNL Advanced Rule Builder] pour ajouter des règles de fonctionnement qui adaptent l&#39;expérience de recherche de votre client.

**Pour ajouter une nouvelle règle de fonctionnement**

Les étapes suivantes supposent que vous utilisez le Créateur de règles visuel.

1. Effectuez l’une des opérations suivantes :

   * Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**. Sur la page [!DNL Business Rules], cliquez sur **[!UICONTROL Add New Rule]**.

   * Dans le menu produit, cliquez sur **[!UICONTROL Simulator]**. Sur la page **[!UICONTROL Simulator for Today]**, cliquez sur **[!UICONTROL Add New Rule]** à droite du menu déroulant **[!UICONTROL Options]**.

      Si l&#39;option **[!UICONTROL Add New Rule]** n&#39;est pas visible sur la page, dans le menu déroulant **[!UICONTROL Options]**, cliquez sur **[!UICONTROL Simulate Staged]**.

      ![](assets/Simulator.png)

1. Dans le champ de texte **[!UICONTROL Name]**, saisissez le nouveau nom de la règle métier.

   Ne cliquez pas encore sur **[!UICONTROL Save Rule]**.
1. (Facultatif) Si vous gérez un grand nombre de règles de fonctionnement, vous pouvez baliser les règles de fonctionnement avec des étiquettes spécifiques. Dans le champ **[!UICONTROL Tags]**, saisissez un ou plusieurs libellés de balise, utilisez une virgule, une tabulation ou saisissez un délimiteur.

   Sur la page [!DNL Business Rules], utilisez la fonction **[!UICONTROL Filter by tag]** pour filtrer les règles qui correspondent à une étiquette donnée. 1. Sur la page [!DNL Business Rule Builder], définissez les déclencheurs et les actions à utiliser.

   **Options de déclenchement**

   Les déclencheurs sont les conditions qui doivent être remplies pour qu’une règle métier s’exécute. Lorsqu’une règle de fonctionnement comporte plusieurs déclencheurs, vous pouvez configurer la manière dont les déclencheurs répondent à l’aide de l’une des trois méthodes suivantes :

   * Réponse dans laquelle tous les déclencheurs doivent être vrais (paramètre par défaut), comme dans l’exemple suivant :

      `if a AND b AND c then ...`

   * Réponse où l’un des déclencheurs doit être vrai, comme dans l’exemple suivant :

      `if a OR b OR c then ...`

   * Réponse dans laquelle une combinaison personnalisée de déclencheurs est spécifiée. Autrement dit, vous combinez des déclencheurs ou des &quot;conditions&quot; individuels avec des opérateurs `AND` et `OR`.

      Vous pouvez également modifier la priorité d’évaluation en ajoutant des combinaisons entre parenthèses gauche et droite, comme dans l’exemple suivant :

      `if (a OR b) AND c then ...`

      >[!NOTE]
      >
      >Si vous combinez des opérateurs `AND` avec des opérateurs `OR` dans un jeu de règles métier personnalisé, veillez à spécifier des parenthèses appropriées pour vous assurer que les déclencheurs sont évalués dans l&#39;ordre approprié.

      Cette fonction particulière de personnalisation d’une combinaison de déclencheurs n’est pas activée par défaut. Contactez l’assistance technique pour activer cette fonction.
   <table> 
      <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option Déclencheurs </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Correspond au mot-clé </p> </td> 
      <td colname="col2"> <p>Déclencheur est true lorsque le terme de recherche correspond au mot-clé sensible à la casse donné. Le déclencheur est true pour le mot-clé et tous ses synonymes, comme défini dans le dictionnaire linguistique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Correspond à la requête </p> </td> 
      <td colname="col2"> <p> Le déclencheur est true lorsque tous les paramètres de recherche correspondent. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Le groupe de résultats est dominant </p> </td> 
      <td colname="col2"> <p> Le déclencheur est true lorsque le groupe de résultats défini par la recherche donnée domine le jeu de résultats. </p> <p>Par défaut, la dominance est définie à 50 %. Ce paramètre est une préférence de marchandisage que vous pouvez définir. </p> <p> 
        <!--See <xref href="t_Configuring_Merchandising_preferences.xml#task_7AC7B9F5D9F44E10AB5BC0B8CB31C37A" type="task" format="dita" scope="local">Configuring Merchandising preferences</xref>. --> </p> <p>Le groupe entier doit être présent dans le jeu de résultats pour que ce déclencheur soit vrai. Le groupe de résultats est dynamique. Ils peuvent changer après les opérations d’index, en fonction des résultats qui correspondent aux critères de recherche d’origine. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Groupe de résultats présent </p> </td> 
      <td colname="col2"> <p> Le déclencheur est true lorsque le groupe de résultats défini par la recherche donnée est présent dans le jeu de résultats. Le groupe entier doit être présent dans le jeu de résultats pour que ce déclencheur soit atteint (les résultats peuvent apparaître sur n’importe quelle page). Le groupe de résultats est dynamique et peut changer après les opérations d’index en fonction des résultats qui correspondent aux critères de recherche d’origine. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Résultat présent </p> </td> 
      <td colname="col2"> <p> Le déclencheur est true lorsque le résultat individuel est trouvé dans le jeu de résultats. Le résultat peut se trouver n’importe où dans le jeu de résultats, il n’est pas nécessaire qu’il se trouve sur la page actuellement consultée par l’utilisateur. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Options d’action**

   Lorsque les déclencheurs d&#39;une règle métier sont satisfaits, les actions associées à la règle sont exécutées. Bien que le Créateur de règles visuel vous permette de créer les actions suivantes, vous pouvez utiliser le Créateur de règles avancé pour créer d’autres types d’actions.

   Les actions Supprimer l’élément de facette, Afficher l’élément de facette, Afficher la facette, Supprimer la facette, Envoyer l’élément de facette dans le tableau suivant nécessitent une facette. L’interface permettant de choisir une facette dépend de la manière dont votre compte est configuré. Par exemple, un compte normal utilise une liste déroulante pour le choix des facettes. Cependant, si votre compte comporte des facettes en pointillés, une zone de texte de saisie automatique s’affiche, dans laquelle vous pouvez saisir le nom de n’importe quelle facette. La saisie automatique suggère des facettes dans une liste déroulante lorsque vous tapez le nom de la facette. Les suggestions incluent les facettes actuellement définies. Si votre compte comporte un mappage d’emplacements, il suggère également des facettes en pointillés.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option Actions </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Groupe Push </p> </td> 
      <td colname="col2"> <p> Place le groupe de résultats de recherche tel que défini par les critères de recherche spécifiés à une position spécifique. </p> <p>Le fait de pousser un groupe de résultats de recherche n’ajoute pas implicitement le groupe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajouter un groupe </p> </td> 
      <td colname="col2"> <p> Ajoutez le groupe de résultats de recherche tel que défini par les critères de recherche spécifiés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer un groupe </p> </td> 
      <td colname="col2"> <p> Supprimez le groupe de résultats de recherche défini par les critères de recherche spécifiés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Push Single </p> </td> 
      <td colname="col2"> <p> Place le résultat de la recherche à la position sélectionnée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajouter une seule </p> </td> 
      <td colname="col2"> <p> Ajoute un résultat de recherche individuel à la position sélectionnée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer un seul </p> </td> 
      <td colname="col2"> <p> Supprime un résultat de recherche individuel du jeu de résultats de la recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer tous les résultats </p> </td> 
      <td colname="col2"> <p>Supprime tous les résultats du jeu de résultats de la recherche. </p> <p> 
        <!-- Bug #3331637 The option is meant to be used in conjunction with other rule actions in order to create "canned landing pages" where we want to create a page's content solely by rule actions, and need to completely discard the "natural" results of the search. Given that the other options don't have any kind of "here's how/why you might use this", I don't see much point in breaking that precedent here.--> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sélectionner une bannière différente </p> </td> 
      <td colname="col2"> <p> Modifie la bannière dans la zone de bannière sélectionnée. </p> <p>Cette option est disponible lorsque vous cliquez avec le bouton droit sur une bannière dans la zone d’affichage de la page Web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajouter les commandes de bannière </p> </td> 
      <td colname="col2"> <p>S’applique uniquement aux modèles Dynamic Media Classic Adobe. </p> <p>Permet de modifier les paramètres par défaut utilisés dans le modèle de bannière. </p> <p>Consultez le tableau des options dans <a scope="local" href="../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3" type="reference" format="dita"> Ajouter une bannière à l’aide d’Adobe Dynamic Media Classic </a>. </p> <p>Voir aussi <a href="../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9" type="task" format="dita" scope="local"> Modification d'une bannière à l'aide d'Adobe Dynamic Media Classic </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer la bannière </p> </td> 
      <td colname="col2"> <p> Supprime la bannière de la zone de bannière sélectionnée ; aucune bannière n’est affichée, sauf si une autre règle qui définit une bannière remplace cette règle. </p> <p>Cette option est disponible lorsque vous cliquez avec le bouton droit sur une bannière dans la zone d’affichage de la page Web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Elément de facette push </p> </td> 
      <td colname="col2"> <p> Place un élément d’une facette à la position sélectionnée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer la zone </p> </td> 
      <td colname="col2"> <p> Supprime une zone de la page des résultats de la recherche. </p> <p>Voir aussi l’action Supprimer la facette ci-dessous. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Zone de détection </p> </td> 
      <td colname="col2"> <p> Affiche une zone dans la page des résultats de la recherche. </p> <p>Voir aussi l’action Afficher la facette ci-dessous. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer un élément de facette </p> </td> 
      <td colname="col2"> <p> Supprime un élément de facette d’une facette. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afficher l’élément de facette </p> </td> 
      <td colname="col2"> <p> Affiche un élément de facette spécifique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afficher la facette </p> </td> 
      <td colname="col2"> <p> Affiche une facette spécifique. Cette action est préférée à l’action Zone visible. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer la facette </p> </td> 
      <td colname="col2"> <p> Supprime une facette spécifique. Cette action est préférable à l’action Supprimer une zone. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   En fonction du panneau du créateur de règles principal (déplié), vous pouvez également effectuer les opérations suivantes pour définir des déclencheurs et des actions.

   * Lorsque le panneau **[!UICONTROL Triggers]** est déplié, dans la zone du modèle de présentation de la page Créateur de règles de fonctionnement, cliquez avec le bouton droit de la souris sur un résultat de recherche ou une facette de recherche, puis cliquez sur **[!UICONTROL Add "result present" trigger]**.

      Dans le panneau Déclencheurs, cliquez sur le X à gauche d&#39;un déclencheur pour le supprimer de la liste des déclencheurs.

   * Lorsque le panneau **[!UICONTROL Actions]** est déplié, cliquez avec le bouton droit sur un résultat de recherche dans la zone du modèle de présentation de la page Créateur de règles de fonctionnement. Cliquez sur **[!UICONTROL Add Result]**, **[!UICONTROL Remove Result]**, **[!UICONTROL Push to bottom]** ou **[!UICONTROL Push to #`<n>`]** (où `<n>` est un nombre).


1. (Facultatif) Dans tout panneau Créateur de règles métier ( [!DNL Triggers], [!DNL Actions] ou [!DNL Schedule]), effectuez l’une des opérations suivantes :

   * Dans la zone de modèle de présentation de la page Créateur de règles de fonctionnement, cliquez avec le bouton droit de la souris sur une bannière, puis cliquez sur **[!UICONTROL Select different banner]**. Sur la page **[!UICONTROL Pick Banner]**, cliquez sur **[!UICONTROL Pick this banner]** sous la miniature de la bannière pour l’ajouter à votre modèle de présentation. Seules les bannières qui correspondent à la taille et à la zone de la bannière d’origine sur le modèle de présentation peuvent être sélectionnées.

      L&#39;action d&#39;ajout de bannière est ajoutée au panneau [!DNL Actions].

   * Dans la zone de modèle de présentation de la page [!DNL Business Rule Builder], cliquez avec le bouton droit sur une bannière de modèle de modèle Dynamic Media Classic Adobe dont vous souhaitez modifier les paramètres, puis cliquez sur **[!UICONTROL Add banner commands]**. Dans la boîte de dialogue [!DNL Change Parameters], définissez les options de paramètre de votre choix.

      Consultez le tableau des options dans [Ajouter une bannière à l’aide d’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Cliquez sur **[!UICONTROL Save]**.

      Les modifications de paramètre sont ajoutées au panneau [!DNL Actions].

      Voir aussi [Modification d’une bannière à l’aide d’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * Dans la zone du modèle de présentation de la page Créateur de règles de fonctionnement, cliquez avec le bouton droit sur une bannière à supprimer de la page, puis cliquez sur **[!UICONTROL Remove banner]**. L’action de suppression de bannière est ajoutée au panneau Actions.

1. (Facultatif) Dans le panneau **[!UICONTROL Schedule]**, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Run Indefinitely]** pour que la règle s&#39;exécute chaque fois que les déclencheurs associés sont satisfaits. Il s’agit de l’option par défaut.
   * Cliquez sur **[!UICONTROL Fixed Schedule]**, puis indiquez la date et l’heure de début, ainsi que la date et l’heure de fin auxquelles la règle doit s’exécuter chaque fois que le déclencheur associé est satisfait.

1. Cliquez sur **[!UICONTROL Save Rule]**.
1. (Facultatif) Sur la page [!DNL Business Rules], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d&#39;une règle de fonctionnement {#task_375CFA75D1D94D9E92A35DE1228E5087}

Vous pouvez utiliser Visual Rule Builder ou Advanced Rule Builder pour modifier les règles de fonctionnement que vous avez ajoutées.

**Pour modifier une nouvelle règle de fonctionnement**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Sur la page [!DNL Business Rules], effectuez l&#39;une des opérations suivantes :

   * Sous la colonne [!DNL Name], cliquez sur le nom d&#39;une règle de fonctionnement à modifier.

      La règle de fonctionnement s’ouvre dans l’interface par défaut spécifiée dans **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL My Preferences]**.

   * Dans la liste déroulante, en regard du nom d’une règle de fonctionnement à modifier, cliquez sur **[!UICONTROL Edit in advanced mode]** ou **[!UICONTROL Edit in visual mode]**.

1. Dans le champ de texte [!DNL Name], saisissez le nouveau nom de la règle métier.

   Ne cliquez pas encore sur **[!UICONTROL Save Rule]**. 1. Sur la page [!DNL Business Rule Builder], définissez les déclencheurs et les actions à utiliser.

   Consultez le tableau des options sous [Ajouter une nouvelle règle de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7).
1. (Facultatif) Dans tout panneau **[!UICONTROL Business Rule Builder]** ( [!DNL Triggers], [!DNL Actions] ou [!DNL Schedule], effectuez l’une des opérations suivantes :

   * Dans la zone du modèle de présentation de la page [!DNL Business Rule Builder], cliquez avec le bouton droit de la souris sur une bannière, puis cliquez sur **[!UICONTROL Select different banner]**. Sur la [!DNL Pick Banner page], cliquez sur **[!UICONTROL Pick this banner]** sous la miniature de la bannière pour l’ajouter à votre modèle de présentation. Seules les bannières qui correspondent à la taille et à la zone de la bannière d’origine sur le modèle de présentation peuvent être sélectionnées.

      L&#39;action d&#39;ajout de bannière est ajoutée au panneau [!DNL Actions].

   * Dans la zone de modèle de présentation de la page [!DNL Business Rule Builder], cliquez avec le bouton droit sur une bannière de modèle de modèle Dynamic Media Classic Adobe dont vous souhaitez modifier les paramètres, puis cliquez sur **[!UICONTROL Add banner commands]**. Dans la boîte de dialogue [!DNL Change Parameters], définissez les options de paramètre de votre choix.

      Consultez le tableau des options dans [Ajouter une bannière à l’aide d’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_AD1E0C00A9E04B1FA819EB93288786B3).

      Cliquez sur **[!UICONTROL Save]**.

      Les modifications de paramètre sont ajoutées au panneau [!DNL Actions].

      Voir aussi [Modification d’une bannière à l’aide d’Adobe Dynamic Media Classic](../c-about-design-menu/c-about-banners.md#task_C3E782477FBF428ABEA220751781ACA9).

   * Dans la zone du modèle de présentation de la page [!DNL Business Rule Builder], cliquez avec le bouton droit de la souris sur une bannière à supprimer de la page, puis cliquez sur **[!UICONTROL Remove banner]**. L&#39;action Supprimer la bannière est ajoutée au panneau [!DNL Actions].

1. (Facultatif) Dans le panneau [!DNL Schedule], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Run Indefinitely]** pour que la règle s&#39;exécute chaque fois que les déclencheurs associés sont satisfaits. Il s’agit de l’option par défaut.
   * Cliquez sur **[!UICONTROL Fixed Schedule]**, puis indiquez la date et l’heure de début, ainsi que la date et l’heure de fin auxquelles la règle doit s’exécuter chaque fois que le déclencheur associé est satisfait.

1. Cliquez sur **[!UICONTROL Save Rule]**.

   La page [!DNL Business Rule Builder] se ferme et vous revenez à la page **[!UICONTROL Business Rule]**. Vos règles s’affichent dans le tableau. Cliquez sur l&#39;en-tête de colonne **[!UICONTROL Modified]** pour trier les règles par date de modification. 1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copie d&#39;une règle de fonctionnement {#task_89F1879C71A54EE9B7454439302C03EC}

Vous pouvez copier une règle de fonctionnement existante à utiliser comme base pour une nouvelle règle de fonctionnement que vous souhaitez créer.

**Pour copier une règle de fonctionnement**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Sur la page **[!UICONTROL Business Rules]**, dans la liste déroulante en regard du nom d&#39;une règle de fonctionnement à copier, cliquez sur **[!UICONTROL Copy rule]**.
1. Modifiez la règle de fonctionnement copiée comme vous le faites habituellement.

   Voir [Modification d&#39;une règle de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087).

## Approbation des règles de fonctionnement {#task_BD569D18BF664272B8692294C162E2C1}

Vous pouvez activer des règles de fonctionnement dont l&#39;état est en cours (en cours) ou qui sont suspendues.

**Pour approuver les règles de fonctionnement**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Sur la page [!DNL Business Rules], en utilisant l&#39;en-tête de colonne d&#39;état dans la colonne [!DNL Status] du tableau des règles de fonctionnement, triez les règles dont l&#39;état est **[!UICONTROL WIP]** ou **[!UICONTROL suspended]**.

   Utilisez l’en-tête de colonne de case à cocher situé à gauche du tableau pour vérifier toutes les règles actuellement affichées sur la page ou uniquement celles dont l’état est **[!UICONTROL WIP]** ou **[!UICONTROL suspended]**. 1. Dans la barre de menus située en haut de la page, cliquez sur **[!UICONTROL Approve]**.
1. Dans la boîte de dialogue **[!UICONTROL Confirm Action]**, cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suspension des règles de fonctionnement {#task_364E1FFB905141C08E306C8F1794A20E}

Vous pouvez suspendre les règles de fonctionnement dont l&#39;état est en cours (Work In Progress) ou qui ont été approuvées.

Lorsque vous suspendez une règle, vous indiquez dans l’interface utilisateur que vous l’avez temporairement rendue inactive et que vous remettez toute tâche sur cette règle à plus tard. Vous pouvez toutefois toujours modifier une règle suspendue.

**Pour suspendre les règles de fonctionnement**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Sur la page [!DNL Business Rules], en utilisant l&#39;état de la colonne État du tableau des règles de fonctionnement, dans la colonne située à l&#39;extrémité gauche du tableau, vérifiez les règles dont l&#39;état est **[!UICONTROL WIP]** ou **[!UICONTROL approved]**.
1. Dans la barre de menus située en haut de la page, cliquez sur **[!UICONTROL Suspend]**.
1. Dans la boîte de dialogue **[!UICONTROL Confirm Action]**, cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Reprendre les règles de fonctionnement {#task_E67D678C765B436EA2A3D6ADD7A49ABA}

Vous pouvez reprendre les règles de fonctionnement pour réactiver une règle suspendue. Une fois la règle de fonctionnement reprise, son état est défini sur En cours (travail en cours).

**Pour reprendre les règles de fonctionnement**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Sur la page [!DNL Business Rules], en utilisant l&#39;état de la colonne État du tableau des règles de fonctionnement, dans la colonne située à l&#39;extrémité gauche du tableau, vérifiez les règles dont l&#39;état est **[!UICONTROL suspended]**.
1. Dans la barre de menus située en haut de la page, cliquez sur **[!UICONTROL Resume]**.
1. Dans la boîte de dialogue [!DNL Confirm Action], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification de l&#39;ordre d&#39;exécution des règles métier {#task_FE3B1C17307F49B49050C2EC5A063991}

Vous pouvez réorganiser les règles de fonctionnement afin de modifier l’ordre dans lequel elles s’exécutent sur les modèles de présentation.

Les règles de fonctionnement s&#39;exécutent dans l&#39;ordre dans lequel elles ont été définies ; plus le numéro d’ordre d’une règle est élevé, plus elle s’exécute dans le processus, ce qui l’emporte sur les règles antérieures. Vous réorganisez les règles en entrant un nouveau numéro dans la colonne Ordre du tableau de la page [!DNL Business Rules]. Vous pouvez également utiliser le glisser-déposer sur les règles pour modifier leur ordre d’exécution.

**Pour modifier l&#39;ordre d&#39;exécution des règles de fonctionnement**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rule]** > **[!UICONTROL Business Rules]**.
1. Sur la page [!DNL Business Rules], dans le tableau, effectuez l’une des opérations suivantes :

   * Cliquez sur l&#39;en-tête de colonne **[!UICONTROL Order]** pour trier les règles par ordre croissant ou décroissant.
   * Dans la colonne **[!UICONTROL Order]**, dans le champ de texte à gauche du nom d&#39;une règle métier, tapez le numéro de commande à exécuter.
   * Faites glisser une rangée de tableau à l’emplacement où vous souhaitez que la règle s’exécute. Tous les numéros de commande sont mis à jour pour refléter le nouvel ordre dans lequel les règles s&#39;exécutent.

1. Cliquez sur **[!UICONTROL Save Changes]**.

   Vos règles de fonctionnement s’exécuteront désormais dans l’ordre indiqué. L&#39;exception est lorsqu&#39;une règle métier de redirection est spécifiée. Si et lorsque la règle métier de redirection est déclenchée ou atteinte, le traitement des règles métier s’arrête pour autoriser la redirection.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression de règles de fonctionnement {#task_AE37B42412044541BCC6D46CF8793DFF}

Vous pouvez supprimer des règles de fonctionnement dont l&#39;état est En cours, Suspendu ou approuvé, à l&#39;aide du menu déroulant Actions en masse.

**Pour supprimer des règles de fonctionnement**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Business Rules]**.
1. Sur la page [!DNL Business Rules], effectuez l&#39;une des opérations suivantes :

   * Utilisez l’en-tête de colonne de la case à cocher pour vérifier toutes les règles actuellement affichées sur la page.
   * Vérifiez uniquement les règles de fonctionnement que vous souhaitez supprimer, en fonction de l&#39;état de la colonne État du tableau.

1. Dans la liste déroulante [!DNL Bulk Actions], cliquez sur **[!UICONTROL Delete]**.
1. Dans la boîte de dialogue [!DNL Confirm Action], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
