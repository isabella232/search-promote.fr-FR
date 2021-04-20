---
description: Utilisez le menu Rechercher pour définir des mots exclus, des collections, des restrictions, des prévisualisations et des cadres.
solution: Target
subtopic: Searching
title: A propos du menu Recherche
topic: Settings,Site search and merchandising
uuid: 072111fc-a32b-4acb-8337-cb21bcdb5542
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '11170'
ht-degree: 1%

---


# A propos du menu Recherche{#about-the-searching-menu}

Utilisez le menu Rechercher pour définir des mots exclus, des collections, des restrictions, des prévisualisations et des cadres.

## A propos des recherches {#concept_207105CF26B1448F8A3D223787C56AB8}

Vous pouvez utiliser les recherches pour définir et personnaliser les recherches nommées auxquelles vos modèles de présentation peuvent faire référence.

<!-- 

c_about_searches.xml

 -->

Dans votre modèle de présentation, vous pouvez référencer toute recherche nommée définie dans le module Recherches. Cela vous permet de personnaliser facilement le type de recherche effectuée pour un ensemble donné de modèles.

Pour exclure les expressions et les mots courants fréquemment utilisés des résultats de la recherche, voir [Configuration des mots exclus](../c-about-linguistics-menu/c-about-excluded-words.md#task_60BF6BB7A66C48479D2BBB32C0F38CDE).

Pour définir des zones spécifiques de votre site Web pouvant faire l&#39;objet de recherches, voir [Ajouter des collections](../c-about-settings-menu/c-about-searching-menu.md#task_07732D0F00104E59AD421297A704B2F6).

Pour spécifier un cadre de cible pour les liens de résultats de recherche, voir [Utilisation de cadres avec des formulaires](../c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Pour limiter les recherches en fonction du parrain HTTP, de l&#39;adresse IP ou du modèle de requête (HTTP ou HTTPS), voir [Définition de valeurs dans Prévisualisation](../c-about-settings-menu/c-about-searching-menu.md#task_CE267A0FF621474E80AB43B67B1C28D7).

## Conseils de recherche {#section_22F0E2BCF259459FA5F49FBCC0F09A7C}

Pour obtenir des résultats de recherche plus spécifiques, vous pouvez utiliser les conseils de recherche suivants.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Conseil de recherche </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Vérifier l'orthographe </p> </td> 
   <td colname="col2"> <p>Assurez-vous que les termes recherchés sont correctement orthographiés. Si <span class="uicontrol"> Correspondance sonore </span> est activée dans <span class="uicontrol"> Linguistique </span> &gt; <span class="uicontrol"> Mots et langues </span>, le moteur de recherche tente de trouver des mots qui ressemblent à vos termes de recherche. Cependant, il est toujours préférable d’essayer d’orthographier correctement les termes de recherche. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-words-and-language.md#concept_CEB4B9576F3C4E2EB87B352EEC738D79" type="concept" format="dita" scope="local"> À propos des mots et de la langue </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliser plusieurs mots </p> </td> 
   <td colname="col2"> <p>Exemple: 
     <code>
       our free product 
     </code> </p> <p>Les requêtes à plusieurs mots retournent des résultats plus affinés que les requêtes à un seul mot. </p> <p>Par exemple, 
     <code>
       our free product 
     </code> renvoie des résultats plus pertinents que le seul 
     <code>
       product 
     </code>. </p> <p>N’oubliez pas que les résultats pertinents sont renvoyés même s’ils ne contiennent pas tous les termes de requête. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliser des mots similaires </p> </td> 
   <td colname="col2"> <p>Exemple: 
     <code>
       safe secure privacy security 
     </code> </p> <p>Plus vous utilisez de mots similaires dans une requête de recherche, plus les résultats de la recherche sont pertinents. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliser la capitalisation appropriée </p> </td> 
   <td colname="col2"> <p>Exemple: 
     <code>
       Search Template Reference 
     </code> </p> <p>Capitalisez les noms appropriés. Si vous utilisez un mot en minuscules, le moteur de recherche correspond à la casse du mot. </p> <p>Par exemple, si vous tapez 
     <code>
       search 
     </code>, le moteur de recherche renvoie tous les documents qui contiennent les mots "search", "Search" et "SEARCH". Cependant, si vous tapez 
     <code>
       Search 
     </code>, le moteur de recherche renvoie des documents qui ne contiennent que le mot en majuscules. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliser des guillemets </p> </td> 
   <td colname="col2"> <p>Exemple: 
     <code>
       "our pledge to you" 
     </code> </p> <p>Utilisez des guillemets pour trouver des mots qui doivent apparaître adjacents, tels que "notre engagement envers vous". Sans les citations qui les entourent, les résultats de la recherche incluent les mots "notre", "engagement", "à" et "vous", mais pas nécessairement dans cet ordre. Au lieu de cela, les mots peuvent apparaître n'importe où, et dans n'importe quel ordre, dans le document. </p> <p> si vous utilisez le formulaire de recherche avancée avec des boutons radio pour <span class="uicontrol"> n'importe quel </span>, <span class="uicontrol"> tous </span> et <span class="uicontrol"> phrase </span>, vous ne pouvez utiliser des guillemets que lorsque <span class="uicontrol"> n'importe quel </span> est sélectionné. Les guillemets sont ignorés si <span class="uicontrol"> l'expression </span> ou <span class="uicontrol"> </span> est sélectionnée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliser + (plus) ou - (moins) </p> </td> 
   <td colname="col2"> <p>Exemple: 
     <code>
       +"template language" 
     </code> </p> <p>Utilisez + pour indiquer qu’un terme ou une expression de recherche doit apparaître dans les résultats de la recherche. </p> <p>Utiliser : pour indiquer qu'un terme ou une expression de recherche doit être absent des résultats de la recherche. </p> <p>Vous devez contenir une phrase entre guillemets. Ne laissez aucun espace entre le signe plus ou moins et le terme de recherche, comme dans l'exemple ci-dessus. </p> <p> si vous utilisez le formulaire de recherche avancée avec des boutons radio pour <span class="uicontrol"> n'importe quel </span>, <span class="uicontrol"> tous </span> et <span class="uicontrol"> phrase </span>, vous ne pouvez utiliser des guillemets que lorsque <span class="uicontrol"> n'importe quel </span> est sélectionné. Les modificateurs plus et moins sont ignorés si <span class="uicontrol"> l'expression </span> ou <span class="uicontrol"> </span> est sélectionnée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliser des recherches de champ </p> </td> 
   <td colname="col2"> <p>Exemples : </p> <p> 
     <ul id="ul_F7CFF7652894402E8D19D6BA49792530"> 
      <li id="li_27492EF933C5437CB2C499746EC8CF39"> 
       <code>
         title:about 
       </code> </li> 
      <li id="li_BD21505122104FD0B16A4DAD777811DA"> 
       <code>
         desc:"Our Team" 
       </code> </li> 
      <li id="li_8264630F8B3D46BF872EFEB1D69DB6BE"> 
       <code>
         keys:login 
       </code> </li> 
      <li id="li_EBB81CBFC6DA45E99A524890DCD56E9F"> 
       <code>
         body:security 
       </code> </li> 
      <li id="li_6A852E35D6984A2C94144AB6C6D2DFA0"> 
       <code>
         alt:"join now" 
       </code> </li> 
      <li id="li_F4C5699360484D12ACD62BBFB84A7904"> 
       <code>
         url:help 
       </code> </li> 
      <li id="li_B2DBBA2239E74D98868D92B3EDEF5B51"> 
       <code>
         target:Adobe 
       </code> </li> 
     </ul> </p> <p>Les recherches de champs vous permettent de créer des recherches spécifiques de mots qui apparaissent dans une partie spécifique d’un document. </p> <p>Vous pouvez effectuer une recherche de champ sur le corps du texte (corps :), le titre (titre :), le texte de remplacement (alt :), la méta-description (desc :), les mots clés de métadonnées (clés :), l’URL (url :) ou les mots clés de la cible de métadonnées (cible :). Utilisez la minuscule pour le nom du champ, suivie immédiatement d’un deux-points. Il n'y a pas d'espace entre le deux-points et le terme recherché. </p> <p>Les recherches de champ ne sont suivies que d’un mot ou d’une expression. Les expressions doivent être placées entre guillemets. </p> <p>si vous utilisez le formulaire de recherche avancée avec une zone de liste pour le nom du champ, vous ne pouvez saisir les noms de champ que lorsque <span class="uicontrol"> un </span> est sélectionné. Les noms de champ spécifiques sont ignorés si un autre champ Formulaire de recherche avancée est sélectionné dans la zone liste. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utiliser des caractères génériques </p> </td> 
   <td colname="col2"> <p>Exemples : </p> <p> 
     <ul id="ul_D8E3867EB15641B0A6E55AD546CCB4DD"> 
      <li id="li_CB8B8FC15EB14B13BB33BB69F5206303"> 
       <code>
         wh* 
       </code> </li> 
      <li id="li_5350A934648C4C81BD6C0875061B426B"> 
       <code>
         "wh* are" 
       </code> </li> 
      <li id="li_7965A2F7186F40039D2F0736299D11B1"> 
       <code>
         415-*-* 
       </code> </li> 
     </ul> </p> <p>Les recherches avec caractères génériques augmentent le nombre de correspondances pour une requête particulière. Le caractère * est utilisé comme caractère générique. </p> <p>Par exemple, la recherche de 
     <code>
       wh* 
     </code> trouve les mots "quoi", "pourquoi", "quand", "si" et tout autre mot qui début avec "pourquoi". A la recherche de *her*, on trouve les mots "ici", "si", "ensemble", "rassemblement", et tout autre mot qui contient "elle" n'importe où dans le mot. </p> <p>Vous pouvez combiner des caractères génériques avec des modificateurs + et -, des guillemets pour des expressions, ainsi que des spécificateurs de recherche de champ. </p> <p>La recherche 
     <code>
       +wh* -se*ch 
     </code> recherche toutes les pages qui contiennent un mot qui début avec "wh" et ne contient pas un mot qui début avec "se" et se termine par "ch". </p> <p>La recherche 
     <code>
       "wh* are" 
     </code> trouve les expressions "où sont", "ce qui sont", "pourquoi le sont", etc. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ajouter une nouvelle définition de recherche {#task_98D3A168AB5D4F30A1ADB6E0D48AB648}

Vous pouvez utiliser le panneau [!DNL GS Add Search] pour configurer et ajouter une nouvelle définition de recherche pour vos composants de recherche guidée, tels que les facettes, les chemins de navigation, la navigation sur les pages, les menus et les recherches récentes, dans la couche de présentation.

<!-- 

t_adding_a_new_definition.xml

 -->

Après avoir ajouté votre nouvelle définition de recherche, veillez à la référencer dans votre modèle de présentation pour qu’elle s’affiche.

Voir [À propos des modèles](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Pour ajouter une nouvelle définition de recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. Sur la page [!DNL Searches], cliquez sur **[!UICONTROL Add New Search]**.
1. Sur la page **[!UICONTROL GS Add Search]**, définissez les options de votre choix.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   Gardez à l’esprit que les règles de traitement qui sélectionnent votre modèle de présentation peuvent remplacer certaines de ces options.

   Voir [Ajouter une nouvelle définition de recherche](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) ou [Modifier une définition de recherche](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom de la recherche </p> </td> 
      <td colname="col2"> <p>Identifie le nom de la recherche définie. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Source </p> </td> 
      <td colname="col2"> <p>Permet de sélectionner la recherche principale à utiliser. Vous pouvez sélectionner <span class="wintitle"> SiteSearch </span> ou <span class="wintitle"> Marchandisage </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Compte </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Permet de sélectionner le compte de recherche/marchandisage du site que vous souhaitez rechercher. En règle générale, une recherche est effectuée dans le compte que vous utilisez actuellement. Cependant, votre modèle de présentation peut utiliser une recherche principale pour n’importe quel autre compte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom/adresse IP du serveur </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez choisi <span class="uicontrol"> Marchandisage </span> comme source. </p> <p>Spécifie le nom complet du serveur <span class="wintitle"> de marchandisage </span> auquel la recherche <span class="wintitle"> de marchandisage </span> doit accéder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Port du serveur </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez choisi <span class="uicontrol"> Marchandisage </span> comme source. </p> <p>Spécifie le numéro de port du serveur <span class="wintitle"> Merchandising </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pyramide </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez choisi <span class="uicontrol"> Marchandisage </span> comme source. </p> <p>Spécifie la pyramide dans le serveur <span class="wintitle"> de marchandisage </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de résultats </p> </td> 
      <td colname="col2"> <p>Indique le nombre de résultats de recherche que vous souhaitez renvoyer. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de résultats de la première page (si différent) </p> </td> 
      <td colname="col2"> <p>Indique le nombre de résultats renvoyés à la première page. Utilisez cette option si vous devez l’avoir différent des autres pages. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de colonnes </p> </td> 
      <td colname="col2"> <p>Indique le nombre de colonnes sur lesquelles les résultats de la recherche sont fractionnés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type De Recherche </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Vous permet de sélectionner parmi les trois types de recherche suivants. </p> <p> 
        <ul id="ul_2F6FA9EFD8DB49EEAB866C3D070E2644"> 
          <li id="li_ECFEBEDD86FF4DE2BB768423B3B91B5E"> <span class="uicontrol"> chacun </span> <p>Recherche les documents qui contiennent tous les mots de la chaîne de requête. </p> <p>L'utilisation de "+" et "-" avant les mots de recherche est désactivée et ces caractères sont ignorés. </p> </li> 
          <li id="li_62EB215BDDE74DF0BF76B3BD5B96776F"> <span class="uicontrol"> n'importe lequel </span> <p>L’utilisation des préfixes de mots "+" et "-" est autorisée. </p> </li> 
          <li id="li_3D71982C0BBA41AFA353069AF3F2F6D8"> <span class="uicontrol"> phrase  </span> <p>La chaîne de requête est traitée comme s’il s’agissait d’une phrase entre guillemets et tous les guillemets tapés par l’utilisateur sont ignorés. </p> <p>L'utilisation de "+" et "-" avant les mots de recherche est désactivée et ces caractères sont ignorés. </p> </li> 
        </ul> </p> <p> Si vous souhaitez que chaque mot d'une requête puisse éventuellement sélectionner une valeur de facette, votre recherche Principale doit toujours utiliser <span class="uicontrol"> all </span>. </p> <p>Vous pouvez consulter des conseils de recherche concernant l’utilisation des modificateurs + et - dans une requête de recherche. </p> <p>Voir <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">A propos des recherches </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Collecte </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Identifie la collection dans l'index que vous souhaitez rechercher. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Permet d’utiliser une sélection aléatoire à partir des résultats de la recherche, sous réserve du <span class="uicontrol"> Nombre de résultats </span> spécifié. </p> <p>Promosearch est un concept hérité. Nous vous recommandons donc d’utiliser le nouveau système de gestion des bannières dans la recherche/marchandisage sur le site. </p> <p>Voir <a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">A propos des bannières </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Appliquer les paramètres de facette </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source et que vous avez sélectionné <span class="uicontrol"> Promosearch </span>. </p> <p>Indique qu’une recherche promotionnelle utilise les facettes sélectionnées pour restreindre les promotions. La plupart des comptes promosearch n’utilisent pas cette option. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fournir une promotion par défaut si aucune promotion correspondante n'est pas proposée </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source et que vous avez sélectionné <span class="uicontrol"> Promosearch </span>. </p> <p>Indique qu'une autre recherche de promotion se produit si la recherche initiale d'une promotion ne trouve rien. La deuxième recherche d'une promotion supprime le mot-clé. Il recherche plutôt toute promotion dans laquelle un champ de métadonnées "is_default" est défini sur "yes". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mettre en surbrillance la recherche </p> </td> 
      <td colname="col2"> <p>Extrait un certain nombre de résultats de la recherche principale que vous souhaitez mettre en évidence dans une "zone-héros". </p> <p>En règle générale, les recherches en surbrillance ont des critères de recherche similaires à ceux de la recherche principale, mais avec un mécanisme de classement différent pour mettre en évidence certains résultats. Le logiciel supprime les duplicata de la recherche principale. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Recherche de base </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez sélectionné <span class="uicontrol"> Mettre en surbrillance la recherche </span>. </p> <p>Vous permet de sélectionner la recherche dont les résultats sont mis en évidence. Les duplicata sont supprimés de cette recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Priorité de déduplication </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez sélectionné <span class="uicontrol"> Mettre en surbrillance la recherche </span>. </p> <p>Permet d’effectuer plusieurs recherches de mise en surbrillance. </p> <p>Lorsque vous avez plusieurs recherches en surbrillance, vous devez spécifier la priorité de la déduplication, où "1" est la priorité la plus élevée. </p> <p>Supposons, par exemple, que vous ayez deux recherches de mise en surbrillance : best-sellers et nouveaux produits. Théoriquement. il est possible qu'un best-seller soit aussi un nouveau produit. Dans ce cas, vous souhaitez supprimer le duplicata des nouveaux produits et de la recherche principale. Par conséquent, vous définissez la priorité des best-sellers sur 1 et la priorité des nouveaux produits sur 2. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre </p> </td> 
      <td colname="col2"> <p>Permet d’ajouter des paramètres CGI à la recherche. </p> <p>Voir <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> Paramètres CGI de la recherche principale </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Sur la page [!DNL Searches], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d&#39;une définition de recherche {#task_AF1FFB1AEF874C13AB359C28F74BF461}

Vous pouvez utiliser le panneau [!DNL Staged GS Edit Search] pour reconfigurer une définition de recherche existante pour la couche de présentation Recherche guidée.

<!-- 

t_editing_a_search_definition.xml

 -->

Après avoir modifié la définition de recherche, veillez à l’avoir référencée dans votre modèle de présentation pour qu’elle s’affiche.

Voir [À propos des modèles](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Pour modifier une définition de recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. Sur la page [!DNL Searches], dans le tableau, cliquez sur **[!UICONTROL Edit]** dans la ligne de la définition à modifier.
1. Sur la page **[!UICONTROL GS Edit Search]**, définissez les options de votre choix.

   <!-- 
   
   r_gs_search_options.xml
   
   -->

   Gardez à l’esprit que les règles de traitement qui sélectionnent votre modèle de présentation peuvent remplacer certaines de ces options.

   Voir [Ajouter une nouvelle définition de recherche](../c-about-settings-menu/c-about-searching-menu.md#task_98D3A168AB5D4F30A1ADB6E0D48AB648) ou [Modifier une définition de recherche](../c-about-settings-menu/c-about-searching-menu.md#task_AF1FFB1AEF874C13AB359C28F74BF461).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom de la recherche </p> </td> 
      <td colname="col2"> <p>Identifie le nom de la recherche définie. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Source </p> </td> 
      <td colname="col2"> <p>Permet de sélectionner la recherche principale à utiliser. Vous pouvez sélectionner <span class="wintitle"> SiteSearch </span> ou <span class="wintitle"> Marchandisage </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Compte </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Permet de sélectionner le compte de recherche/marchandisage du site que vous souhaitez rechercher. En règle générale, une recherche est effectuée dans le compte que vous utilisez actuellement. Cependant, votre modèle de présentation peut utiliser une recherche principale pour n’importe quel autre compte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom/adresse IP du serveur </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez choisi <span class="uicontrol"> Marchandisage </span> comme source. </p> <p>Spécifie le nom complet du serveur <span class="wintitle"> de marchandisage </span> auquel la recherche <span class="wintitle"> de marchandisage </span> doit accéder. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Port du serveur </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez choisi <span class="uicontrol"> Marchandisage </span> comme source. </p> <p>Spécifie le numéro de port du serveur <span class="wintitle"> Merchandising </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pyramide </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez choisi <span class="uicontrol"> Marchandisage </span> comme source. </p> <p>Spécifie la pyramide dans le serveur <span class="wintitle"> de marchandisage </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de résultats </p> </td> 
      <td colname="col2"> <p>Indique le nombre de résultats de recherche que vous souhaitez renvoyer. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de résultats de la première page (si différent) </p> </td> 
      <td colname="col2"> <p>Indique le nombre de résultats renvoyés à la première page. Utilisez cette option si vous devez l’avoir différent des autres pages. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de colonnes </p> </td> 
      <td colname="col2"> <p>Indique le nombre de colonnes sur lesquelles les résultats de la recherche sont fractionnés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type De Recherche </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Vous permet de sélectionner parmi les trois types de recherche suivants. </p> <p> 
        <ul id="ul_E1D8B3DE9DB24DE4813D53F6298A03A6"> 
          <li id="li_C3DD7AA7699B477A9EE0731CFC012630"> <span class="uicontrol"> chacun </span> <p>Recherche les documents qui contiennent tous les mots de la chaîne de requête. </p> <p>L'utilisation de "+" et "-" avant les mots de recherche est désactivée et ces caractères sont ignorés. </p> </li> 
          <li id="li_4C66B9EFEFA042908A4D3730F9F54EB0"> <span class="uicontrol"> n'importe lequel </span> <p>L’utilisation des préfixes de mots "+" et "-" est autorisée. </p> </li> 
          <li id="li_37E9AD42A61C4E31A0816DFB8E71118D"> <span class="uicontrol"> phrase  </span> <p>La chaîne de requête est traitée comme s’il s’agissait d’une phrase entre guillemets et tous les guillemets tapés par l’utilisateur sont ignorés. </p> <p>L'utilisation de "+" et "-" avant les mots de recherche est désactivée et ces caractères sont ignorés. </p> </li> 
        </ul> </p> <p> Si vous souhaitez que chaque mot d'une requête puisse éventuellement sélectionner une valeur de facette, votre recherche Principale doit toujours utiliser <span class="uicontrol"> all </span>. </p> <p>Vous pouvez consulter des conseils de recherche concernant l’utilisation des modificateurs + et - dans une requête de recherche. </p> <p>Voir <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">A propos des recherches </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Collecte </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Identifie la collection dans l'index que vous souhaitez rechercher. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Promosearch </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source. </p> <p>Permet d’utiliser une sélection aléatoire à partir des résultats de la recherche, sous réserve du <span class="uicontrol"> Nombre de résultats </span> spécifié. </p> <p>Promosearch est un concept hérité. Nous vous recommandons donc d’utiliser le nouveau système de gestion des bannières dans la recherche/marchandisage sur le site. </p> <p>Voir <a href="../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA" type="concept" format="dita" scope="local">A propos des bannières </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Appliquer les paramètres de facette </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source et que vous avez sélectionné <span class="uicontrol"> Promosearch </span>. </p> <p>Indique qu’une recherche promotionnelle utilise les facettes sélectionnées pour restreindre les promotions. La plupart des comptes promosearch n’utilisent pas cette option. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fournir une promotion par défaut si aucune promotion correspondante n'est pas proposée </p> </td> 
      <td colname="col2"> <p>Cette option n'est disponible que si vous avez choisi <span class="uicontrol"> Search &amp; Promote </span> comme source et que vous avez sélectionné <span class="uicontrol"> Promosearch </span>. </p> <p>Indique qu'une autre recherche de promotion se produit si la recherche initiale d'une promotion ne trouve rien. La deuxième recherche d'une promotion supprime le mot-clé. Il recherche plutôt toute promotion dans laquelle un champ de métadonnées "is_default" est défini sur "yes". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mettre en surbrillance la recherche </p> </td> 
      <td colname="col2"> <p>Extrait un certain nombre de résultats de la recherche principale que vous souhaitez mettre en évidence dans une "zone-héros". </p> <p>En règle générale, les recherches en surbrillance ont des critères de recherche similaires à ceux de la recherche principale, mais avec un mécanisme de classement différent pour mettre en évidence certains résultats. Le logiciel supprime les duplicata de la recherche principale. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Recherche de base </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez sélectionné <span class="uicontrol"> Mettre en surbrillance la recherche </span>. </p> <p>Vous permet de sélectionner la recherche dont les résultats sont mis en évidence. Les duplicata sont supprimés de cette recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Priorité de déduplication </p> </td> 
      <td colname="col2"> <p>Cette option est disponible uniquement si vous avez sélectionné <span class="uicontrol"> Mettre en surbrillance la recherche </span>. </p> <p>Permet d’effectuer plusieurs recherches de mise en surbrillance. </p> <p>Lorsque vous avez plusieurs recherches en surbrillance, vous devez spécifier la priorité de la déduplication, où "1" est la priorité la plus élevée. </p> <p>Supposons, par exemple, que vous ayez deux recherches de mise en surbrillance : best-sellers et nouveaux produits. Théoriquement. il est possible qu'un best-seller soit aussi un nouveau produit. Dans ce cas, vous souhaitez supprimer le duplicata des nouveaux produits et de la recherche principale. Par conséquent, vous définissez la priorité des best-sellers sur 1 et la priorité des nouveaux produits sur 2. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètre </p> </td> 
      <td colname="col2"> <p>Permet d’ajouter des paramètres CGI à la recherche. </p> <p>Voir <a scope="local" href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita"> Paramètres CGI de la recherche principale </a>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la page [!DNL Searches], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d&#39;une définition de recherche {#task_1D8E991E4C4146B7A7311FAE5DAA3742}

Vous pouvez supprimer une définition de recherche de guide dont vous n’avez plus besoin ou que vous n’utilisez plus.

<!-- 

t_deleting_a_search_definition.xml

 -->

Voir [À propos des modèles](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5).

**Pour supprimer une définition de recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Searches]**.
1. Sur la page [!DNL Searches], dans le tableau, cliquez sur **[!UICONTROL Delete]** dans la ligne de la définition à supprimer.
1. Dans la boîte de dialogue [!DNL Confirmation], cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Sur la page [!DNL Searches], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos du Gestionnaire de mots-clés de résultats épinglés {#concept_0C5F152C029C485D8872C6795CBCD7C7}

Vous pouvez épingler manuellement les résultats de la recherche à un emplacement spécifique. Ces résultats épinglés sont associés à une ou plusieurs requêtes de recherche spécifiques. Vous pouvez utiliser [!DNL Pinned Result Keyword Manager] pour gérer tous les mots-clés avec des résultats épinglés.

<!-- 

c_about_pinned_results_keyword_manager.xml

 -->

## Règles de recherche de mots-clés à suivre {#section_ED67A24BE884468286F34FA5DFF826D7}

La requête de recherche que vous entrez dans le panneau comporte les règles suivantes :

* Les espaces de début et de fin sont supprimés de la requête.
* Aucun caractère de recherche spécial n&#39;est autorisé, par exemple :

   * Caractère générique correspondant à des astérisques (*).
   * Aucun élément obligatoire ou obligatoire n’utilise plus ou moins (+ ou -).
   * Aucun spécificateur de champ avec le caractère deux-points (:).
   * Aucune virgule ou guillemets de doublon ( ou &quot;).

* Plusieurs termes ou mots séparés par des espaces dans la requête sont autorisés.
* Les lettres en majuscules sont converties en minuscules.

Les termes recherchés sont mémorisés exactement tels quels ; vous devez réutiliser les mêmes termes de recherche pour obtenir exactement les mêmes résultats.

Les résultats épinglés ne prennent pas en charge la distinction majuscules/minuscules. Toutes les lettres majuscules des mots-clés sont converties en minuscules.

## Réorganisation des résultats de la recherche {#section_46FBE5279C7740A09D6DC9F54FE104AA}

Lorsque vous effectuez une recherche sur un mot-clé dans le panneau [!DNL Stage Add New Keyword] ou le panneau [!DNL Staged Edit Keyword], les résultats de la recherche reflètent ce qui pourrait se produire après la prochaine opération d&#39;index. Vous pouvez réorganiser les résultats de la recherche dans le tableau à l’aide de l’une des trois méthodes suivantes.

La première méthode consiste à utiliser la case à cocher **[!UICONTROL Pinned]**. La case à cocher est utilisée pour épingler un résultat à une position spécifique. Lorsque vous cochez la case, tous les résultats de recherche au-dessus de la case sont également épinglés. Cette fonctionnalité garantit que tous les résultats au-dessus de cette case à cocher s’affichent dans cet ordre spécifique. L&#39;activation d&#39;un résultat de recherche entraîne sa perte sous tous les résultats actuellement épinglés.

La deuxième méthode consiste à faire glisser et déposer le tableau. Vous pouvez déplacer un résultat vers une nouvelle position par glisser-déposer. Après avoir fait glisser un résultat vers un nouvel emplacement, tous les résultats situés au-dessus du nouvel emplacement sont épinglés. Cette épinglage automatique permet de s’assurer que le reste des résultats s’affiche au-dessus du résultat récemment glissé.

La troisième méthode consiste à définir l&#39;ordre des résultats épinglés en entrant une position spécifique dans la colonne &quot;#&quot;. Contrairement au glisser-déposer, l&#39;ordre des résultats de la recherche simulée n&#39;est évident que lors de la prochaine ouverture du panneau [!DNL Staged Edit Keyword]. La définition du numéro de commande d’une ligne actuellement non épinglée permet de s’assurer qu’au moins un grand nombre d’éléments sont épinglés. La définition du numéro de commande d’une ligne actuellement épinglée définit l’ordre de cet article dans les éléments actuellement épinglés. Cependant, il n’augmente pas le nombre d’éléments épinglés.

Lorsque vous enregistrez les résultats de la recherche, vous pouvez à nouveau vue les résultats en saisissant exactement la même requête dans le champ Mot-clé.

## A propos des résultats de la recherche épinglée {#section_46780B7812F249F3B45503161C4FBDEE}

Les résultats de la recherche sont souvent classés selon le score de pertinence. Cependant, un résultat de recherche épinglé ignore le score de pertinence et tente de remplacer l’ordre naturel par sa position prédéterminée. En s&#39;assurant que le résultat reste relativement tel qu&#39;il est, les autres résultats de recherche connus au-dessus doivent être épinglés.

Les résultats de la recherche affichés dans le panneau simulent ce qui s’affiche après l’index suivant. Toutefois, les modifications apportées au document d&#39;origine ou à certaines modifications de configuration dans le Centre de membres peuvent produire des résultats incohérents. Par exemple, la modification du contenu d’un document n’est connue qu’après l’index.

Les résultats épinglés s’affichent dans un ordre similaire ou identique après l’index, car ils ignorent la pertinence. Les résultats non épinglés reviennent à leur position naturelle après un indice ; l&#39;ordre des résultats non épinglés n&#39;est pas garanti.

## Ajouter un nouveau mot-clé {#task_8CED128DADD34D0DAD2C64B64D0D6B06}

Vous pouvez ajouter de nouveaux mots-clés et leurs résultats épinglés.

<!-- 

t_adding_a_new_keyword.xml

 -->

Au moment où vous ajoutez un nouveau mot-clé, vous pouvez réorganiser les résultats de la recherche et les épingler à une position spécifique.

**Pour ajouter un nouveau mot-clé**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. Sur la page [!DNL Pinned Keyword Results Manager], cliquez sur **[!UICONTROL Add New Keyword]**.
1. Sur la page [!DNL Add New Keyword], dans le champ **[!UICONTROL Keyword]**, entrez une requête de recherche, puis cliquez sur **[!UICONTROL Search Keyword]**.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   Vous pouvez utiliser le bouton Modifier le tableau pour ajuster la manière dont vous vue le tableau des résultats de la recherche. Par exemple, vous pouvez utiliser la liste des colonnes pour afficher ou masquer des colonnes spécifiques. Vous pouvez également réorganiser l’ordre des colonnes par glisser-déposer.

   Le tableau suivant décrit les propriétés de colonne figurant dans l’éditeur de tableau.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Colonne </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Commande </p> </td> 
      <td colname="col2"> <p>Indique l’ordre numérique de l’aspect des colonnes. Vous pouvez faire glisser les colonnes pour mettre automatiquement à jour l’ordre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du champ </p> </td> 
      <td colname="col2"> <p>Identifie le nom de l'en-tête de colonne qui apparaît dans le tableau <span class="wintitle"> Résultats de la recherche simulée </span> du panneau <span class="wintitle"> Nouveau mot-clé d'Ajoute intermédiaire </span> et du panneau <span class="wintitle"> Modification du mot-clé d'étape </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure </p> </td> 
      <td colname="col2"> <p>Si la case est cochée, la colonne apparaît dans la table des résultats épinglés. Si la zone est vide ou désélectionnée, la colonne disparaît du tableau. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afficher l’URL sous forme d’image </p> </td> 
      <td colname="col2"> <p>Si le champ de métadonnées affecté à cette colonne contient des URL de graphiques ou d’images, cochez cette case pour y placer des balises d’image HTML et l’image s’affiche. Les images manquantes ou les liens incorrects sont vides. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longueur de champ </p> </td> 
      <td colname="col2"> <p>Vous permet de saisir la longueur maximale du texte à afficher avant d’être tronqué avec des ellipses (...). Si la colonne est définie pour afficher les URL sous forme d’images, ce champ n’a aucun effet. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Réorganiser les résultats de la recherche.
   * Cliquez sur **[!UICONTROL Edit Table]** pour ajuster la vue de la table [!DNL Simulated Search Results]. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Changes]** pour revenir au panneau [!DNL Add New Keyword].

1. Cliquez sur **[!UICONTROL Save Search Results]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Pinned Results Keyword Manager], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d&#39;un mot-clé {#task_30C550A7350B4394B5B43536368A84B1}

Vous pouvez modifier des mots-clés existants et leurs résultats épinglés.

<!-- 

t_editing_a_keyword.xml

 -->

Au moment de modifier un mot-clé, vous pouvez réorganiser les résultats de la recherche et les épingler à un emplacement spécifique.

**Pour modifier un mot-clé**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. Sur la page [!DNL Pinned Keyword Results Manager], dans le tableau, cliquez sur **[!UICONTROL Edit]** dans la ligne du mot-clé à modifier.
1. Sur la page [!DNL Edit Keyword], dans le champ **[!UICONTROL Keyword]**, entrez une requête de recherche, puis cliquez sur **[!UICONTROL Search Keyword]**.

   Veillez à respecter les règles de recherche de mots-clés.

   <!-- 
   
   r_keyword_options.xml
   
   -->

   Vous pouvez utiliser le bouton Modifier le tableau pour ajuster la manière dont vous vue le tableau des résultats de la recherche. Par exemple, vous pouvez utiliser la liste des colonnes pour afficher ou masquer des colonnes spécifiques. Vous pouvez également réorganiser l’ordre des colonnes par glisser-déposer.

   Le tableau suivant décrit les propriétés de colonne figurant dans l’éditeur de tableau.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Colonne </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Commande </p> </td> 
      <td colname="col2"> <p>Indique l’ordre numérique de l’aspect des colonnes. Vous pouvez faire glisser les colonnes pour mettre automatiquement à jour l’ordre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du champ </p> </td> 
      <td colname="col2"> <p>Identifie le nom de l'en-tête de colonne qui apparaît dans le tableau <span class="wintitle"> Résultats de la recherche simulée </span> du panneau <span class="wintitle"> Nouveau mot-clé d'Ajoute intermédiaire </span> et du panneau <span class="wintitle"> Modification du mot-clé d'étape </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure </p> </td> 
      <td colname="col2"> <p>Si la case est cochée, la colonne apparaît dans la table des résultats épinglés. Si la zone est vide ou désélectionnée, la colonne disparaît du tableau. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afficher l’URL sous forme d’image </p> </td> 
      <td colname="col2"> <p>Si le champ de métadonnées affecté à cette colonne contient des URL de graphiques ou d’images, cochez cette case pour y placer des balises d’image HTML et l’image s’affiche. Les images manquantes ou les liens incorrects sont vides. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longueur de champ </p> </td> 
      <td colname="col2"> <p>Vous permet de saisir la longueur maximale du texte à afficher avant d’être tronqué avec des ellipses (...). Si la colonne est définie pour afficher les URL sous forme d’images, ce champ n’a aucun effet. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Réorganiser les résultats de la recherche.
   * Cliquez sur **[!UICONTROL Edit Table]** pour ajuster la vue de la table [!DNL Simulated Search Results].

      Voir [Ajouter un nouveau mot-clé](../c-about-settings-menu/c-about-searching-menu.md#task_8CED128DADD34D0DAD2C64B64D0D6B06).

      Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save Changes]** pour revenir au panneau [!DNL Add New Keyword].

1. Cliquez sur **[!UICONTROL Save Search Results]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Pinned Results Keyword Manager], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d&#39;un mot-clé {#task_F17D6357D6DD416495E6D4117899D81D}

Vous pouvez supprimer des mots-clés dont vous n&#39;avez plus besoin ou que vous n&#39;utilisez plus.

<!-- 

t_deleting_a_keyword.xml

 -->

Au moment où vous ajoutez un nouveau mot-clé, vous pouvez réorganiser les résultats de la recherche et les épingler à une position spécifique.

**Pour supprimer un mot-clé**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Pinned Results]**.
1. Sur la page [!DNL Pinned Keyword Results Manager], dans le tableau, cliquez sur **[!UICONTROL Delete]** dans la ligne du mot-clé à supprimer.
1. Sur la page [!DNL Delete Keyword], cliquez sur **[!UICONTROL Delete]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Pinned Results Keyword Manager], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des collections {#concept_62E42ACE53D54EEE9273433B86259127}

Vous pouvez utiliser les collections pour permettre aux clients de rechercher des zones spécifiques d’un site Web afin qu’ils puissent rapidement trouver ce qu’ils recherchent.

<!-- 

c_about_collections.xml

 -->

Voir [A propos des recherches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

Voir [Utilisation des collections dans les formulaires de recherche](../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Par exemple, les clients peuvent rechercher une collection d’URL liées aux ventes de produits ou aux services d’assistance. Avant que les clients puissent utiliser les collections que vous spécifiez, veillez à mettre à jour votre formulaire de recherche dans le menu Formulaire de recherche.

Avant que les effets des paramètres Collections ne soient visibles par les clients, recréez l’index de votre site.

Vous pouvez tester vos collections en entrant l’une des URL de votre site Web dans le champ facultatif **[!UICONTROL Test Collections]**, puis en cliquant sur **[!UICONTROL Test]**. La collection à laquelle appartient la page spécifiée est renvoyée.

Chaque collection est spécifiée sur une seule ligne avec un nom et un masque d’URL. Un masque d’URL peut être constitué des éléments suivants :

* un chemin complet tel que `https://www.mydomain.com/products.html`
* un chemin partiel tel que `https://www.mydomain.com/products`
* une expression régulière

   Pour faire d&#39;un masque une expression régulière, insérez le mot-clé `regexp` entre le nom de la collection et le masque d&#39;URL.

   Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Chaque ligne du champ Collections ne peut contenir qu’un seul masque d’URL. Cependant, vous pouvez spécifier plusieurs masques d’URL pour le même nom de collection sur différentes lignes. L’exemple suivant contient quatre noms de collection différents et cinq masques d’URL :

```
Company Info https://www.yoursite.com/company 
Products https://www.yoursite.com/products 
FAQs regexp ^.*/faqs 
Support https://www.yoursite.com/email_support/ 
Support https://www.yoursite.com/phone_support/
```

Dans cet exemple, après avoir mis à jour le formulaire de recherche pour inclure ces collections, les clients peuvent sélectionner et rechercher chaque collection définie individuellement. La collection `Support` comprend des fichiers qui correspondent aux deux masques d&#39;URL, de sorte que les fichiers de `www.yoursite.com/email_support/` et `www.yoursite.com/phone_support` soient recherchés lorsque cette collection est sélectionnée.

## Ajouter des collections {#task_07732D0F00104E59AD421297A704B2F6}

Vous pouvez ajouter des collections pour permettre aux clients de rechercher des zones spécifiques de votre site Web afin qu’ils puissent rapidement trouver ce qu’ils recherchent.

<!-- 

t_adding_collections.xml

 -->

Veillez à recréer l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Pour ajouter des collections**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Collections]**.
1. Dans le champ [!DNL Collections], saisissez un nom de collection et une adresse de masque d’URL, une par ligne.
1. (Facultatif) Sur la page [!DNL Collections], dans le champ **[!UICONTROL Test Collections]**, saisissez un masque d’URL de test sur votre site Web, puis cliquez sur **[!UICONTROL Test]**.

   Une fenêtre de sortie de la collection de tests s’affiche, indiquant l’URL et le nom de la collection.
1. Lorsque vous avez terminé d’ajouter des collections, cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Collections], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Restrictions {#concept_B5B527E04EBF4E9AB5956EEF881DDBF1}

Avant d’effectuer une recherche, l’URL de référence et l’adresse IP sont examinées afin de déterminer si une recherche est possible à partir de cet emplacement. Ce que vous avez spécifié dans [!DNL Restrictions] détermine si la recherche est autorisée. Si une recherche n&#39;est pas autorisée, une page d&#39;erreur générique est renvoyée au demandeur.

<!-- 

c_about_restrictions.xml

 -->

Vous pouvez définir des paramètres de restriction sous la forme de masques d’URL de parrain ou de masques d’adresse IP. Les deux types de restrictions utilisés incluent les masques pour autoriser les recherches et exclure les masques pour les refuser.

Une recherche est autorisée si elle transmet à la fois l’URL du parrain et les critères de restriction d’adresse IP. Si l&#39;un des paramètres n&#39;autorise pas la recherche, celle-ci échoue, quelles que soient les autres restrictions qui l&#39;autorisent.

Par exemple, si le champ &quot;parrain HTTP&quot; d’une requête de recherche correspond à un masque d’URL de parrain &quot;Exclure&quot;, la recherche échoue, même si l’adresse IP de la requête correspond à un masque d’adresse IP &quot;Inclure&quot;. Si aucun masque ne correspond à l’URL ou l’adresse IP du parrain, l’emplacement est inclus par défaut.

Saisissez chaque masque d’inclusion ou d’exclusion sur une seule ligne.

## Limites du masque d&#39;URL ou du masque d&#39;adresse IP du parrain {#task_E6FF2DD83E8D4B00A0E2809DC13A56C9}

Vous pouvez définir des paramètres de restriction sous la forme &quot;Masques d’URL de Parrain&quot; ou &quot;Masques d’adresses IP&quot;. Les deux types de restrictions utilisés incluent les masques pour autoriser les recherches et exclure les masques pour les refuser. Une recherche est autorisée si elle respecte à la fois les critères d’URL de parrain et de restriction d’adresse IP.

<!-- 

t_adding_url_mask_or_jp_address_restrictions.xml

 -->

**Pour ajouter un masque d’URL de parrain ou un masque d’adresse IP**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Restrictions]**.
1. Sur la page [!DNL Restrictions], définissez les options de restriction de votre choix. Entrez les adresses de masque d&#39;URL de parrain, les adresses de masque d&#39;adresse IP ou, éventuellement, l&#39;adresse URL d&#39;une page Web personnalisée qui s&#39;affiche pour les clients qui ne sont pas autorisés à effectuer des recherches sur votre site.

   <!-- 
   
   r_restriction_options.xml
   
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
      <td colname="col1"> <p>Masques d’URL de parrain </p> </td> 
      <td colname="col2"> <p>L’URL du parrain de l’en-tête du parrain HTTP est lue. Le premier masque qui correspond à l’URL du parrain détermine s’il faut autoriser la recherche, si le masque est un masque d’inclusion. Ou, il détermine s’il faut interdire la recherche, si le masque est un masque d’exclusion. Si aucun masque ne correspond à l’URL du parrain, cette URL est incluse et la recherche est autorisée. </p> <p> Si votre modèle de recherche contient un nouveau formulaire de recherche ou si votre modèle de recherche peut contenir des liens tels que "10 Suivant", "10 Précédent" ou "Masquer les résumés", vous pouvez liste votre modèle de résultats de recherche en tant que masque d’inclusion. La méthode la plus simple pour y parvenir est l’expression classique, comme dans l’exemple suivant : </p> <p> <span class="codeph"> inclure regexp ^https?://[^/]*\.atomz\.com/.*[ ?&amp;]sp_a=sp1000130e.*$ </span> </p> <p>L’exemple suivant contient cinq masques d’URL de parrain différents : </p> <p> <code> include&nbsp;https://www.mydomain.com/search/ 
          include&nbsp;https://search.mydomain.com/ 
          include&nbsp;regexp&nbsp;^https://www.mydomain.com/help/.*/search/ 
          include&nbsp;regexp&nbsp;^https?://[^/]*\.atomz\.com/.*[?&amp;]sp_a=sp1000130e.*$ 
          exclude&nbsp;* </code> </p> <p>Si les masques d’URL du parrain sont les suivants : </p> <p> <code> https://www.mydomain.com/search/searchpage.html&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://search.mydomain.com/advanced/&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/search/advanced/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          https://www.mydomain.com/help/products/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          https://www.anotherdomain.com/&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          blank&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masques d’adresse IP </p> </td> 
      <td colname="col2"> <p>Le premier masque qui correspond à l’adresse IP détermine si la recherche doit être autorisée, si le masque est un masque d’inclusion. Ou, il détermine si la recherche doit être autorisée ou non si le masque est un masque d’exclusion. Si aucun masque ne correspond à l’adresse IP de la demande, cette adresse IP est incluse et la recherche est autorisée. </p> <p>L'exemple suivant montre quatre masques d'adresse IP différents. </p> <p> <code> include&nbsp;64.128.192.* 
          include&nbsp;192.168. 
          include&nbsp;regexp&nbsp;^209\.42\.97\.[1-5]+ 
          exclude&nbsp;* </code> </p> <p>Si les masques d’adresse IP référente sont les suivants : </p> <p> <code> 64.128.192.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          192.168.10.127&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          209.42.97.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;allowed] 
          64.128.193.10&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          192.169.10.14&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] 
          209.42.97.68&nbsp;&nbsp;&nbsp;&nbsp;[then&nbsp;search&nbsp;is&nbsp;disallowed] </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Autoriser uniquement les recherches utilisant HTTPS </p> </td> 
      <td colname="col2"> <p>Limiter les recherches au protocole HTTPS. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>URL vers laquelle les requêtes désautorisées doivent être envoyées </p> </td> 
      <td colname="col2"> <p> Les utilisateurs restreints sont redirigés vers l’URL que vous saisissez ici. Cette option vous permet d’élaborer votre propre page d’erreur personnalisée à afficher aux clients qui ne sont pas autorisés à effectuer des recherches sur votre site. </p> <p>Si vous ne spécifiez pas d’URL, une page d’erreur générique est renvoyée lorsqu’un utilisateur restreint tente de rechercher votre site. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos de la Prévisualisation {#concept_DF293FD3B02C467F8842C8C21D62F294}

La chaîne de requête et les paramètres définis dans [!DNL Preview] sont utilisés chaque fois qu&#39;un formulaire de recherche est testé ou prévisualisé dans le logiciel.

<!-- 

c_about_preview.xml

 -->

Voir aussi [A propos des recherches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

## Définition de valeurs dans la Prévisualisation {#task_CE267A0FF621474E80AB43B67B1C28D7}

Les valeurs de prévisualisation que vous définissez sont utilisées chaque fois qu’un formulaire de recherche est testé ou prévisualisé dans le logiciel.

<!-- 

t_setting_values_in_preview.xml

 -->

**Pour définir des valeurs dans la Prévisualisation**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Preview]**.
1. Sur la page [!DNL Preview], définissez les options de votre choix.

   <!-- 
   
   r_preview_options.xml
   
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
      <td colname="col1"> <p>Requête </p> </td> 
      <td colname="col2"> <p>Par défaut, la chaîne de requête est définie sur <span class="codeph"> * </span>, ce qui renvoie généralement des résultats. Cependant, vous pouvez spécifier une requête plus spécifique au contenu de votre site Web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètres </p> </td> 
      <td colname="col2"> <p>Les paramètres sont définis avec un nom et une valeur. Vous pouvez spécifier autant de paramètres supplémentaires que nécessaire. Par exemple, vous pouvez spécifier des critères de recherche supplémentaires avec les paramètres <span class="codeph"> sp_q_1 </span> et <span class="codeph"> sp_x_1 </span>. La valeur de paramètre <span class="codeph"> sp_q_1=windows&amp;sp_x_1=platform </span> crée une recherche de prévisualisation qui recherche la valeur "windows" dans la balise meta "platform" des pages recherchées, en plus de la requête principale. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8" type="reference" format="dita" scope="local"> Paramètres CGI de la recherche principale </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Hôte </p> </td> 
      <td colname="col2"> <p>Si votre site Web utilise un libellé de domaine privé, définissez le nom d’hôte approprié pour prévisualisation précisément vos résultats de recherche. </p> <p>Pour plus d’informations sur l’étiquetage des domaines privés, contactez le service clientèle. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des flux {#concept_FEBFEE51A3AB49F88CBA0D16E2AD6916}

L’index de recherche est affiché comme une base de données volumineuse de votre site Web. Avec suffisamment d’informations provenant des balises meta correctes, les informations sont collectées et organisées, ou regroupées, en flux de données. Vous pouvez envoyer ces flux de données à un autre service, tel qu’un destinataire tiers.

<!-- 

c_about_feeds.xml

 -->

Une fois votre site Web analysé et indexé, vous pouvez générer des flux automatiques et les envoyer à des moteurs de recherche et à des moteurs d’achat biologiques tiers. Vous pouvez créer les flux de diffusion suivants :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Type de flux </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Adobe Recommendations </p> </td> 
   <td colname="col2"> <p>Les flux Recommendations offrent des fonctionnalités de syndication de données avec Adobe Recommendations. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flux générique </p> </td> 
   <td colname="col2"> <p>Vous pouvez implémenter de nombreux flux avec le type Flux générique. Une requête de recherche personnalisée est effectuée par rapport à l’index de votre site Web. Les données sont renvoyées par le biais de modèles de recherche personnalisés utilisant la même langue de modèle pour l’affichage des résultats de recherche. Ce type de flexibilité signifie que vous pouvez envoyer des flux à un plus grand nombre de fournisseurs, et pas seulement à des types de flux spécifiques. </p> <p>Vous pouvez ajouter le modèle de transport (recherche) en suivant les instructions de la rubrique d’aide suivante : </p> <p>Voir <a href="../c-about-design-menu/c-about-templates.md#task_73199757B6E748CAA604902FF913F012" type="task" format="dita" scope="local"> Ajouter un nouveau fichier de présentation ou de modèle de transport </a>. </p> <p> Après avoir ajouté le modèle, modifiez-le à l’aide de balises de modèle de recherche afin de définir les champs de métadonnées de recherche à inclure, ainsi que leur format. </p> <p>Voir <a href="../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3" type="task" format="dita" scope="local"> Modification d'une présentation ou d'un modèle de transport </a>. </p> <p>Voir <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Balises de modèle de recherche </a>. </p> <p>Veillez à mémoriser le nom du fichier de modèle de transport. Vous utilisez ce nom pour lier le flux générique au modèle lorsque vous spécifiez les critères du flux. </p> <p>Si vous avez déjà travaillé avec d’autres flux, n’oubliez pas que vous mappez les champs de flux aux champs de métadonnées de recherche. Cette étape spécifique n’est pas indiquée dans l’assistant <span class="uicontrol"> Créer un flux </span>. Au lieu de cela, le modèle spécifie les métadonnées et la mise en forme des métadonnées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Google Merchant </p> </td> 
   <td colname="col2"> <p>Google Merchant Center permet aux clients de vendre des produits via plusieurs services Google. Il comporte un composant de syndication de données dans lequel vous pouvez soumettre une liste de produits disponibles à la vente sur une base périodique. </p> <p>Comme pour tout fournisseur tiers de flux, Google Merchant Center a des normes spécifiques que vous respectez avant de les considérer comme légitimes. Pour plus d'informations, contactez votre représentant client et consultez la documentation Google Merchant. Voici un bref résumé de ce que Google Merchant Center considère lors de la validation d’un flux : </p> 
    <ul id="ul_3D84D4A6A4BF4C08860F86403F8F9CD6"> 
     <li id="li_5B6516CC7BC7493B8B8E8AFB454E573F">Chaque produit a une page de produits ; une URL dédiée. </li> 
     <li id="li_5A6D5AD5E1B54A94B224D19E888B5443"> Chaque variante de produit comporte une entrée distincte dans le flux. </li> 
     <li id="li_89748D3241B34A4493576DAC38681988"> Chaque produit possède une URL d’image, provenant de préférence de votre serveur. Les variantes de produit comportent des images spécifiques montrant leurs variations réelles. En d'autres termes, des couleurs de chaussures différentes ne devraient pas partager la même image. </li> 
     <li id="li_A594AD19480F41EAA72181355F28447B"> Chaque produit comporte des informations spécifiques telles que la disponibilité, l'état, la description, la catégorie et le prix. </li> 
     <li id="li_0955B3A6ED2746D2B7CB42DC8AB27D3A">En général, chaque produit possède un identifiant unique, tel que ISBN, UPC, JAN ou EAN, etc. </li> 
     <li id="li_2C371653F1C5471FA638F3A3818ABC17">En général, chaque produit est classé dans la taxonomie des produits de Google. </li> 
     <li id="li_6EB392A5A0BE490FAED5BC5E83228E32"> Les produits de vêtements comportent des champs supplémentaires obligatoires tels que le sexe, le groupe d’âge, la couleur et la taille. </li> 
     <li id="li_44B91FA9A95F4172A2F03F8206E9081E"> La taxe et la livraison sont spécifiées en tant que paramètre de compte dans Google Merchant Center ou sur la base produit par produit, dans ce flux. </li> 
     <li id="li_71A63E9905B840C0A04F6CDAA23C9AB0"> Les produits sur mesure et certains produits de vêtements peuvent être exemptés de certaines règles, mais vous devez contacter Google pour obtenir l'autorisation et les détails sur ces exemptions. </li> 
    </ul> <p>De nombreux détails régissent la validation des flux. Pour plus d’informations sur la gestion des flux, consultez la documentation de Google Merchant. Google apporte fréquemment des modifications aux spécifications, donc vérifiez souvent la documentation. </p> <p>Le flux associé à Google Merchant Center est souvent appelé le flux Google Shopping. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plans de site Google </p> </td> 
   <td colname="col2"> <p>Les plans de site Google vous permettent d’influencer la manière dont Google analyse votre site Web. Dans ce cas, un flux de données syndiqué, un plan de site, est régulièrement envoyé aux plans de site Google. Le plan de site contient des URL accessibles sur Internet et des informations spécifiques, telles que la date de la dernière modification ou la priorité de la page, peuvent être associées à chaque URL. Fournir à Google de telles informations peut augmenter la fréquence et les chances qu'une page spécifique soit analysée et indexée. Dans certains cas, un plan de site est utilisé pour annoncer une liste de liens qui ne peuvent pas être accessibles par leur analyseur de liens dans des circonstances normales. </p> <p>Si vous souhaitez créer un plan de site Google avec notre fonction de flux, contactez votre représentant client. Google a mis son service de plan de site Google à la disposition du grand public et fournit de la documentation sur sa page Google Webmaster Tools. </p> <p> <b>Conditions requises pour la création d’un flux de plan de site Google</b> </p> <p>Pour créer un flux de plan de site Google, assurez-vous d’avoir un compte Google Webmaster Tools avec Google Sitemap déjà configuré. Reportez-vous à la documentation des outils Google Webmaster Tools pour configurer le plan de site Google. </p> <p>Vous devez également déterminer comment les fichiers de plan de site sont distribués. En général, les fichiers de plan de site proviennent de votre domaine et, plus précisément, de la racine de votre site Web. Le modèle simple consiste à faire livrer les fichiers par FTP à vos serveurs. L’autre solution consiste à rediriger la demande des fichiers de plan de site vers le réseau de contenu de recherche/marchandisage du site. Contactez votre conseiller pour coordonner et configurer la diffusion des flux de plan de site. </p> </td> 
  </tr> 
 </tbody> 
</table>

Si vous êtes intéressé par les flux automatiques, veuillez contacter les services professionnels pour obtenir de l’aide. Chaque flux est soumis à des exigences strictes en matière de qualité des données et de transmission des fichiers.

Le type de flux sélectionné affecte les options qui s’affichent lorsque vous créez un champ à l’aide de l’assistant **[!UICONTROL Create Feed]**. Chaque type de flux possède différents formats de données. Veillez à respecter le format de données approprié pour éviter le rejet d’un flux par un destinataire de flux ou la publication de données incorrectes à vos clients. Outre le format des données, les fournisseurs ont généralement une ou plusieurs méthodes préférées pour recevoir les données. Consultez la documentation du fournisseur sur leurs flux.

La création d’un flux pose un problème de mise en correspondance des données entre la recherche/le marchandisage du site et le flux. En règle générale, le format des données extraites de l’analyse d’index est incorrect ou est absent. Vous trouverez ci-dessous une liste de questions qui peuvent vous aider à vous concentrer sur les éléments à rechercher lors de la création d’un flux.

* Quel type de relation d’affaires entretenez-vous avec le destinataire de flux ?
* Devez-vous vous inscrire et créer un compte auprès du destinataire de flux ?
* Qui va surveiller et s&#39;occuper des problèmes qui se présentent avec le flux à l&#39;égard du vendeur ? En général, il est de votre responsabilité de gérer le compte du fournisseur. Par exemple, Google Sitemap nécessite un compte WebMaster et une personne pour surveiller l’état du plan de site.
* Quel est le format de données du flux ?
* Votre index correspond-il à l’encodage des caractères du flux ? Les formats de données délimités par des tabulations et délimités par des virgules deviennent un problème lorsque vos données comportent des tabulations ou des virgules.
* Que faire lorsque vos données contiennent des tabulations ou des virgules ?
* Existe-t-il des pages dans votre index avec des données vides ?
* Le destinataire de flux peut-il accepter des données vides ? Vous pouvez résoudre des données vides en modifiant le critère de récupération des données par le logiciel.
* Le format des données correspond-il à ce que souhaite le destinataire de flux ? Par exemple, certains destinataires du flux sont spécifiques à la manière dont les prix et la devise sont affichés.
* Le fournisseur peut-il accepter un nombre maximum d&#39;articles ? Vous pouvez résoudre ce problème potentiel en limitant les résultats avec les critères de recherche.
* Comment le fournisseur souhaite-t-il recevoir le flux ? Les envois FTP et l’hébergement HTTP sont pris en charge.

## Création d’un flux {#task_63179C1FC359497483CD6CE13FD1C250}

Vous pouvez créer un ou plusieurs flux de données.

<!-- 

t_creating_a_feed.xml

 -->

**Pour créer un flux**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Sur la page [!DNL Feeds], sélectionnez un type de flux dans la liste déroulante **[!UICONTROL Create Feed]**.
1. Selon le type de flux que vous avez sélectionné, définissez les options identifiées dans chaque panneau de l’assistant dans la boîte de dialogue [!DNL Create Feed].

   <!-- 
   
   r_feed_options.xml
   
   -->

   Selon le type de flux que vous créez ou modifiez, les options disponibles diffèrent légèrement.

   **Adobe Recommendations**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panneau </p> </th> 
      <th colname="col2" class="entry"> <p>Nom du panneau Assistant </p> </th> 
      <th colname="col3" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nom du flux </p> </td> 
      <td colname="col3"> <p>Indique le nom du flux. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Zones cliquables </p> </td> 
      <td colname="col3"> <p>Permet de mapper des champs de flux spécifiques au fournisseur aux champs de métadonnées de recherche/marchandisage de site. Cette étape de mappage dans l’assistant est importante car elle permet aux flux de mettre en corrélation les informations entre les champs de l’index et les champs des données du flux. Dans la plupart des cas, à l’exception de <span class="wintitle"> Flux génériques </span>, les corrélations sont enregistrées dans un modèle de recherche généré dynamiquement. </p> <p>Chaque ligne de la table <span class="wintitle"> Zones cliquables </span> représente un mappage de champs. Dans la colonne Ajouter/Supprimer du tableau, cliquez sur <span class="uicontrol"> + </span> pour ajouter une nouvelle ligne de mappage de champ ; cliquez sur <span class="uicontrol"> - </span> pour supprimer de la table la ligne de mappage de champ actuellement sélectionnée. Pour associer un champ de flux à un champ de métadonnées de recherche de site/marchandisage, utilisez les listes déroulantes correspondantes pour choisir les champs de votre choix. </p> <p> <b>Mappages de champs pour Adobe Recommendations</b> </p> <p>Le flux de données de recommandation est un fichier CSV, contenant des colonnes de données séparées par des virgules. L’ordre d’aspect de chaque mappage sur la table des zones est important car il détermine l’ordre des colonnes dans le fichier de flux CSV. Créez les lignes de mappage dans l’ordre suivant : chaque ligne est obligatoire : </p> <p> 
        <ol id="ol_49C739D04DD340168DC6C1F794544C35"> 
          <li id="li_A95D9C5A353746A3A0D38F200AC2EEA2"> l’id </li> 
          <li id="li_044763D4C7054CEB948C94590735D74F"> name </li> 
          <li id="li_832F07CA0E3F4E10A4AE30171F3E8541"> categoryId </li> 
          <li id="li_2A33FB42F7E942ED881BA1F478542C4D"> message </li> 
          <li id="li_A76E66B2366845B0B63ED5C200531ADD"> thumbnailURL </li> 
          <li id="li_518CCD5E7E404521AB8199981BA86F76"> value </li> 
          <li id="li_14A0A8FCC2B34B758E1FBB98E3F2DFB2"> pageURL </li> 
          <li id="li_36D22F1603394AF89E0C7ADB18AAAAB7"> inventory </li> 
          <li id="li_ABDB9C762BBC4F27B82FEA4425A8DDC4"> margin </li> 
        </ol> </p> <p> <b>Utilisation avancée</b> </p> <p>Après avoir mappé les neuf premiers champs de flux requis comme indiqué ci-dessus, vous pouvez créer vos propres champs personnalisés. Dans la liste déroulante <span class="wintitle"> Champs de flux </span>, cliquez sur <span class="uicontrol"> Personnalisé </span>. Dans le champ de texte associé, saisissez un nom de balise personnalisé pour ce champ. Cette option personnalisée est utile si un flux nécessite des champs spécifiques à un fournisseur. </p> <p> <p>Remarque :  Bien que les spécifications du flux de recommandation stipulent que chaque nom de champ doit être précédé du préfixe "entité", il n’est pas nécessaire dans ce cas. </p> </p> <p>Vous pouvez également créer un champ de métadonnées personnalisé. Dans la liste déroulante <span class="wintitle"> Champs de métadonnées </span>, cliquez sur <span class="uicontrol"> Personnalisé </span>. Dans le champ de texte associé, saisissez une valeur de champ de métadonnées personnalisée. La valeur est insérée dans le modèle prégénéré et peut également être utilisée pour injecter des balises de modèle de recherche personnalisée. </p> <p>Voir <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Balises de modèle de recherche </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Critères de recherche </p> </td> 
      <td colname="col3"> <p>Lorsque les fichiers de flux sont générés, une requête de recherche est utilisée pour filtrer les données. Vous définissez les filtres utilisés pour la requête de recherche dans ce panneau. </p> 
        <ul id="ul_799ECF61C03A44878C7182F8B88CC3AD"> 
        <li id="li_0763F600A4FB4650ACC28BF337EB50AF"> <span class="uicontrol"> Meta Field  </span> <p>Définit le champ de métadonnées sur lequel vous souhaitez filtrer. </p> <p> <b>Utilisation avancée</b> </p> <p>Le système de filtrage étant une requête de recherche standard, vous pouvez sélectionner <span class="uicontrol"> Formulaire libre </span> dans la liste déroulante pour entrer des paramètres de recherche CGI et leurs valeurs. L’échappement d’URL est obligatoire. L'argument de recherche <span class="codeph"> sp_q </span> est ignoré. Vous pouvez créer plusieurs lignes de zones de texte Formulaire libre. Entre chaque ligne, les arguments sont délimités automatiquement par des &amp;. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Paramètres CGI de recherche </a>. </p> </li> 
        <li id="li_756B776902AE4A0E95524442D663343E"> <span class="uicontrol"> Critères </span> <p>Définit l’opération de filtrage. L’opération de filtrage que vous sélectionnez dans la liste déroulante applique la valeur constante saisie dans la troisième colonne. </p> </li> 
        <li id="li_7ADEDB8747B241D78AC50F1AC75AE695"> <span class="uicontrol"> Valeur </span> <p>Valeur constante. </p> </li> 
        <li id="li_4039A9BC2F74460B83BFF662B58DAA1B"> <span class="uicontrol"> Action </span> <p>Ajoute une nouvelle ligne de mappage de champ ou supprime la ligne actuellement mise en surbrillance. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envoi du fichier </p> </td> 
      <td colname="col3"> <p>Vous permet de configurer le calendrier d’envoi des fichiers de flux et de définir la méthode à utiliser pour télécharger les fichiers. </p> 
        <ul id="ul_55E253F83BDA46BAABF2BE38F0918E80"> 
        <li id="li_877A376B5B30422FAC816E31D50EA508"> <span class="uicontrol"> Planification </span> <p>Définit la fréquence maximale d’envoi d’un flux. La sélection de <span class="uicontrol"> Jamais </span> désactive le flux. D’autres valeurs définissent la période pendant laquelle le flux attend avant de soumettre à nouveau le flux. La décision de soumettre le flux est prise à chaque index. En d’autres termes, à la fin de l’index, un flux est contrôlé pour vérifier s’il a expiré et s’il doit être mis à jour et soumis par le fournisseur. Il est également utilisé comme méthode pour empêcher un compte de se soumettre de manière excessive à un fournisseur. Certains fournisseurs appliquent des règles à l’égard des sources de flux de données qui se chargent trop fréquemment. Veillez à vérifier la politique du fournisseur de flux de données concernant la fréquence des envois. 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--ick <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_760F5068D3ED46C582AE41392A2CA342"> <span class="uicontrol"> Méthode de transfert  </span> <p>La plupart des flux peuvent distribuer les fichiers de deux manières différentes : Réseau de contenu FTP et hébergé. </p> 
          <ul id="ul_666759EDDD034537AA7C0ED936A2F315"> 
          <li id="li_B4AD5CEEBB7B41C0B8DC291B95DC5F83"> <span class="uicontrol"> FTP </span> <p>Les serveurs de recherche/marchandisage de site utilisent le FTP passif. </p> <p>Le protocole FTP est le seul moyen de transférer un fichier vers un autre serveur. </p> <p> <span class="uicontrol"> Serveur FTP  </span> : indique le nom du serveur FTP. N’incluez pas le protocole ou le précédent "ftp://". </p> <p> <span class="uicontrol"> Nom d'utilisateur FTP  </span> - Indique le nom du compte FTP. </p> <p> <span class="uicontrol"> Mot de passe FTP  </span> - Indique le mot de passe du compte FTP. </p> <p> <span class="uicontrol"> Nom de fichier FTP  </span> - Indique le nom du fichier à transmettre. Ce nom est un modèle si le flux génère plusieurs fichiers, en incrémentant généralement un nombre à la fin du nom mais avant l’extension. Par exemple : basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml </p> <p> <span class="uicontrol"> Répertoire FTP  </span> - Si un chemin d'accès au répertoire spécifique est requis, entrez-le ici. N’incluez pas le nom de fichier dans le chemin d’accès. </p> </li> 
          <li id="li_C082D3993C6C469B9067F207703BE619"> <span class="uicontrol"> Réseau de contenu hébergé  </span> <p>Le réseau de contenu est le moyen de diffuser des fichiers à partir des serveurs Web de la recherche/marchandisage sur site. Le destinataire du flux l’extrait des serveurs Web à l’aide d’une requête HTTP. Le seul élément d'information pour configurer cette configuration est <span class="uicontrol"> Nom de fichier du réseau de contenu </span>. Le nom de fichier est le nom de base du fichier diffusé. Utilisez uniquement des noms de fichier avec une extension de nom de fichier. Selon le flux, le nom de fichier est un modèle pour plusieurs fichiers où le flux peut générer plusieurs fichiers au format suivant : basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. </p> <p>Une fois le nom de fichier de base saisi et l’enregistrement du flux réussi, l’URL du fichier Content Network s’affiche dans le panneau Vérification de l’assistant. L’URL devient principale une fois le flux traité. Le fournisseur peut obtenir les données de flux à partir de cette URL. Plusieurs fichiers utilisent le même chemin d’accès d’URL. Toutefois, veillez à remplacer ou à modifier le nom de fichier selon le modèle de énumération. </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Vérification </p> </td> 
      <td colname="col3"> <p>Lorsque vous accédez au panneau <span class="wintitle"> Vérification </span>, votre flux est enregistré à ce stade. Toutefois, les fichiers de flux réels ne sont enregistrés qu’à une date ultérieure. </p> <p>Le panneau <span class="wintitle"> Vérification </span> vous permet d’effectuer les opérations suivantes : </p> 
        <ul id="ul_0C6EFB38E06F401696084863D85CBD0D"> 
        <li id="li_07FC9F04C7F640048546F9DC5D91DA1D"> <span class="uicontrol"> Vue de données  </span> <p>Permet de cliquer sur le lien pour vérifier la sortie du flux au moyen d’une vue de données affichée dans un tableau. La vue de données peut également vous aider à résoudre les problèmes en vous montrant quels champs de métadonnées sont sélectionnés et comment tout critère de recherche spécifié dans le panneau <span class="wintitle"> Critères de recherche </span> de l’assistant affecte la sortie du flux. La vue de données est générée de manière dynamique, de sorte qu’elle est disponible à tout moment. </p> </li> 
        <li id="li_67046A56D08C48298E5A3E1F9C4A8AF3"> <span class="uicontrol"> Fichiers de flux  </span> <p>Une fois que les serveurs de recherche/marchandisage de site ont généré les fichiers de flux, vous pouvez utiliser la liste déroulante <span class="uicontrol"> Fichiers de flux </span> pour vue les fichiers à partir des serveurs. Un nouvel onglet de navigateur ou une nouvelle fenêtre de navigateur s’affiche avec le contenu du flux. Cette méthode est utile pour résoudre les problèmes de mise en forme des flux qui posent problème. Notez que vous ne vues pas les fichiers à partir de la destination finale ou des fournisseurs eux-mêmes. </p> <p> Si le flux est nouveau, la liste déroulante est vide jusqu’à ce que vous génériez des fichiers de flux. </p> </li> 
        <li id="li_99D66C7AD87A475CB3D831D514DB78A0"> <span class="uicontrol"> Lien réseau de contenu  </span> <p>Si vous avez choisi <span class="uicontrol"> Hosted Content Network </span> comme méthode de téléchargement dans le panneau <span class="wintitle"> File Submission </span> de l'Assistant, l'URL s'affiche ici. Si vous n’avez encore généré aucun fichier de flux, l’URL n’est pas valide tant que le flux n’a pas été généré correctement. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Flux générique**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panneau </p> </th> 
      <th colname="col2" class="entry"> <p>Nom du panneau Assistant </p> </th> 
      <th colname="col3" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nom du flux </p> </td> 
      <td colname="col3"> <p>Indique le nom du flux. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Critères de recherche </p> </td> 
      <td colname="col3"> <p>Lorsque les fichiers de flux sont générés, une requête de recherche est utilisée pour filtrer les données. Vous définissez les filtres utilisés pour la requête de recherche dans ce panneau. </p> 
        <ul id="ul_C750687E69A647D0A4440FF1B6CC7E05"> 
        <li id="li_B5C3B8523D71472E9508A04E23AC0211"> <span class="uicontrol"> Meta Field  </span> <p>Définit le champ de métadonnées sur lequel vous souhaitez filtrer. </p> <p> <b>Utilisation avancée</b> </p> <p>Le système de filtrage étant une requête de recherche standard, vous pouvez sélectionner <span class="uicontrol"> Formulaire libre </span> dans la liste déroulante pour entrer des paramètres de recherche CGI et leurs valeurs. L’échappement d’URL est obligatoire. L'argument de recherche <span class="codeph"> sp_q </span> est ignoré. Vous pouvez créer plusieurs lignes de zones de texte Formulaire libre. Entre chaque ligne, les arguments sont délimités automatiquement par des &amp;. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Paramètres CGI de recherche </a>. </p> </li> 
        <li id="li_D1E49834BBEA42CC8C49AE7D72037C53"> <span class="uicontrol"> Critères </span> <p>Définit l’opération de filtrage. L’opération de filtrage que vous sélectionnez dans la liste déroulante applique la valeur constante saisie dans la troisième colonne. </p> </li> 
        <li id="li_D5F0651B834F4EACAD15A2D154A0737B"> <span class="uicontrol"> Valeur </span> <p>Valeur constante. </p> </li> 
        <li id="li_FC8F382BD20C4518BC2230D4B4954591"> <span class="uicontrol"> Action  </span> <p>Ajoute une nouvelle ligne de mappage de champ ou supprime la ligne actuellement mise en surbrillance. </p> </li> 
        </ul> <p>Les flux génériques ont besoin d’un paramètre CGI spécial spécifié. Pour lier le modèle spécial associé à ce flux, définissez le paramètre <span class="codeph"> sp_t </span>. Définissez la valeur <span class="codeph"> sp_t </span> sur le nom du fichier de modèle de transport. Par exemple, si vous avez ajouté un fichier de modèle de transport nommé <span class="codeph"> super_feed.tpl </span>, vous créez un paramètre de recherche CGI personnalisé sous la forme <span class="codeph"> sp_t=super_feed </span>. La zone de texte permettant de saisir <span class="codeph"> sp_t </span> n’apparaît que lorsque vous sélectionnez <span class="uicontrol"> Formulaire libre </span> dans la liste déroulante <span class="wintitle"> Meta Field </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Envoi du fichier </p> </td> 
      <td colname="col3"> <p>Vous permet de configurer le calendrier d’envoi des fichiers de flux et de définir la méthode à utiliser pour télécharger les fichiers. </p> 
        <ul id="ul_30E830C41F6A4526822AF1FD3083075A"> 
        <li id="li_79EAFDBD2B9F411EA985CAEC1BAF3926"> <span class="uicontrol"> Planification </span> <p>Définit la fréquence maximale d’envoi d’un flux. La sélection de <span class="uicontrol"> Jamais </span> désactive le flux. D’autres valeurs définissent la période pendant laquelle le flux attend avant de soumettre à nouveau le flux. La décision de soumettre le flux est prise à chaque index. En d’autres termes, à la fin de l’index, un flux est contrôlé pour vérifier s’il a expiré et s’il doit être mis à jour et soumis par le fournisseur. Il est également utilisé comme méthode pour empêcher un compte de se soumettre de manière excessive à un fournisseur. Certains fournisseurs appliquent des règles à l’égard des sources de flux de données qui se chargent trop fréquemment. Veillez à vérifier la politique du fournisseur de flux concernant la fréquence des envois. 
          <!--he time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> 
          <!--<uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_20BF70A19E7E45BA91CD972E2FCE0EA4"> <span class="uicontrol"> Méthode de transfert  </span> <p>La plupart des flux peuvent distribuer les fichiers de deux manières différentes : Réseau de contenu FTP et hébergé. </p> 
          <ul id="ul_5888C2E9097645CE89938EE09F8CB4F1"> 
          <li id="li_EA9ED19F3BEA4BEAB1A9F2C2FAFF85F7"> <span class="uicontrol"> FTP  </span> <p>Les serveurs de recherche/marchandisage de site utilisent le FTP passif. </p> <p>Le protocole FTP est le seul moyen de transférer un fichier vers un autre serveur. </p> <p> <span class="uicontrol"> Serveur FTP  </span> : indique le nom du serveur FTP. N’incluez pas le protocole ou le précédent "ftp://". </p> <p> <span class="uicontrol"> Nom d'utilisateur FTP  </span> - Indique le nom du compte FTP. </p> <p> <span class="uicontrol"> Mot de passe FTP  </span> - Indique le mot de passe du compte FTP. </p> <p> <span class="uicontrol"> Nom de fichier FTP  </span> - Indique le nom du fichier à transmettre. Ce nom est un modèle si le flux génère plusieurs fichiers, en incrémentant généralement un nombre à la fin du nom mais avant l’extension. Par exemple : basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml </p> <p> <span class="uicontrol"> Répertoire FTP  </span> - Si un chemin d'accès au répertoire spécifique est requis, entrez-le ici. N’incluez pas le nom de fichier dans le chemin d’accès. </p> </li> 
          <li id="li_181268A7EE40456CA1DB768E8C66EEB9"> <span class="uicontrol"> Réseau de contenu hébergé  </span> <p>Le réseau de contenu hébergé est le moyen de diffuser des fichiers à partir des serveurs Web de recherche/marchandisage de site. Le destinataire du flux l’extrait des serveurs Web à l’aide d’une requête HTTP. Le seul élément d'information pour configurer cette configuration est <span class="uicontrol"> Nom de fichier du réseau de contenu </span>. Le nom de fichier est le nom de base du fichier diffusé. Utilisez uniquement des noms de fichier avec une extension de nom de fichier. 
            <!--Depending on the feed, the file name is a template for multiple files where the feed might generate multiple files in the following format: basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml. --> </p> <p>Une fois le nom de fichier de base saisi et l’enregistrement du flux réussi, l’URL du fichier Content Network s’affiche dans le panneau Vérification de l’assistant. L’URL devient principale une fois le flux traité. Le fournisseur peut obtenir les données de flux à partir de cette URL. </p> </li> 
          </ul> </li> 
        <li id="li_4DF56FA607A7479296CDA042A63C5A2C"> <p> <b>Conserver les onglets ?</b> </p> <p>Conserver les caractères de tabulation dans le flux. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Vérification </p> </td> 
      <td colname="col3"> <p>Lorsque vous accédez au panneau <span class="wintitle"> Vérification </span>, votre flux est enregistré à ce stade. Toutefois, les fichiers de flux réels ne sont enregistrés qu’à une date ultérieure. </p> <p>Le panneau <span class="wintitle"> Vérification </span> vous permet d’effectuer les opérations suivantes : </p> 
        <ul id="ul_7420C415987448A796DD979CF5FA2EB6"> 
        <li id="li_AF02E8609B7B4F20A01AF4E010308E15"> <span class="uicontrol"> Vue de données  </span> <p>Permet de cliquer sur le lien pour vérifier la sortie du flux au moyen d’une vue de données affichée dans un tableau. La vue de données peut également vous aider à résoudre les problèmes en vous montrant quels champs de métadonnées sont sélectionnés et comment tout critère de recherche spécifié dans le panneau <span class="wintitle"> Critères de recherche </span> de l’assistant affecte la sortie du flux. La vue de données est générée de manière dynamique, de sorte qu’elle est disponible à tout moment. </p> </li> 
        <li id="li_32CEB8885C184354BFA1773BA66DB7A7"> <span class="uicontrol"> Fichiers de flux  </span> <p>Une fois que les serveurs de recherche/marchandisage de site ont généré les fichiers de flux, vous pouvez utiliser la liste déroulante <span class="uicontrol"> Fichiers de flux </span> pour vue les fichiers à partir des serveurs. Un nouvel onglet de navigateur ou une nouvelle fenêtre de navigateur s’affiche avec le contenu du flux. Cette méthode est utile pour résoudre les problèmes de mise en forme des flux qui posent problème. Notez que vous ne vues pas les fichiers à partir de la destination finale ou des fournisseurs eux-mêmes. </p> <p> Si le flux est nouveau, la liste déroulante est vide jusqu’à ce que vous génériez des fichiers de flux. </p> </li> 
        <li id="li_8D1B876B0EC2455C8654EC573EC53FA9"> <span class="uicontrol"> Lien réseau de contenu  </span> <p>Si vous avez choisi <span class="uicontrol"> Hosted Content Network </span> comme méthode de téléchargement dans le panneau <span class="wintitle"> File Submission </span> de l'Assistant, l'URL s'affiche ici. Si vous n’avez encore généré aucun fichier de flux, l’URL n’est pas valide tant que le flux n’a pas été généré correctement. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Centre commercial Google**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panneau </p> </th> 
      <th colname="col2" class="entry"> <p>Nom du panneau Assistant </p> </th> 
      <th colname="col3" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Nom du flux </p> </td> 
      <td colname="col3"> <p>Indique le nom du flux. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Zones cliquables </p> </td> 
      <td colname="col3"> <p>Permet de mapper des champs de flux spécifiques au fournisseur aux champs de métadonnées de recherche/marchandisage de site. Cette étape de mappage dans l’assistant est importante car elle permet aux flux de mettre en corrélation les informations entre les champs de l’index et les champs des données du flux. Dans la plupart des cas, à l’exception de <span class="wintitle"> Flux génériques </span>, les corrélations sont enregistrées dans un modèle de recherche généré dynamiquement. </p> <p>Chaque ligne de la table Zone cliquable représente un mappage de champ. Dans la colonne <span class="wintitle"> Ajouter/Supprimer </span> de la table, cliquez sur <span class="uicontrol"> + </span> pour ajouter une nouvelle ligne de mappage de champ ; cliquez sur <span class="uicontrol"> - </span> pour supprimer de la table la ligne de mappage de champ actuellement sélectionnée. Pour associer un champ de flux à un champ de métadonnées de recherche de site/marchandisage, utilisez les listes déroulantes correspondantes pour choisir les champs de votre choix. </p> <p> <b>Utilisation avancée</b> </p> <p>Vous pouvez créer vos propres champs personnalisés. Dans la liste déroulante <span class="wintitle"> Champs de flux </span>, cliquez sur <span class="uicontrol"> Personnalisé </span>. Dans le champ de texte associé, saisissez un nom de balise personnalisé pour ce champ. Cette option personnalisée est utile si un flux nécessite des champs spécifiques à un fournisseur. </p> <p>Vous pouvez également créer un champ de métadonnées personnalisé. Dans la liste déroulante <span class="wintitle"> Champs de métadonnées </span>, cliquez sur <span class="uicontrol"> Personnalisé </span>. Dans le champ de texte associé, saisissez une valeur de champ de métadonnées personnalisée. La valeur est insérée dans le modèle prégénéré et peut également être utilisée pour injecter des balises de modèle de recherche personnalisée. </p> <p>Voir <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Balises de modèle de recherche </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Critères de recherche </p> </td> 
      <td colname="col3"> <p>Lorsque les fichiers de flux sont générés, une requête de recherche est utilisée pour filtrer les données. Vous définissez les filtres utilisés pour la requête de recherche dans ce panneau. </p> 
        <ul id="ul_8179321A58BB4C72B0CDB2B2BEC58FE4"> 
        <li id="li_9F8008A2398A4667B106BC49C94E5E3E"> <span class="uicontrol"> Meta Field  </span> <p>Définit le champ de métadonnées sur lequel vous souhaitez filtrer. </p> <p> <b>Utilisation avancée</b> </p> <p>Le système de filtrage étant une requête de recherche standard, vous pouvez sélectionner <span class="uicontrol"> Formulaire libre </span> dans la liste déroulante pour entrer des paramètres de recherche CGI et leurs valeurs. L’échappement d’URL est obligatoire. L'argument de recherche <span class="codeph"> sp_q </span> est ignoré. Vous pouvez créer plusieurs lignes de zones de texte Formulaire libre. Entre chaque ligne, les arguments sont délimités automatiquement par des &amp;. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Paramètres CGI de recherche </a>. </p> </li> 
        <li id="li_50C9CE59E9E5418895F8C1A070560063"> <span class="uicontrol"> Critères </span> <p>Définit l’opération de filtrage. L’opération de filtrage que vous sélectionnez dans la liste déroulante applique la valeur constante saisie dans la troisième colonne. </p> </li> 
        <li id="li_9F86D0F5010046A4A9F93DBA5FB158B3"> <span class="uicontrol"> Valeur </span> <p>Valeur constante. </p> </li> 
        <li id="li_1051AFD5AEA447D0AF5FAB305E1D1E64"> <span class="uicontrol"> Action  </span> <p>Ajoute une nouvelle ligne de mappage de champ ou supprime la ligne actuellement mise en surbrillance. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envoi du fichier </p> </td> 
      <td colname="col3"> <p>Vous permet de configurer le calendrier d’envoi des fichiers de flux et de définir la méthode à utiliser pour télécharger les fichiers. </p> 
        <ul id="ul_A6A3C333AADD4438B835BF3E16E2AEFF"> 
        <li id="li_FCC4DAF198E149278B5CFB870CB6218C"> <span class="uicontrol"> Planification </span> <p>Définit la fréquence maximale d’envoi d’un flux. La sélection de <span class="uicontrol"> Jamais </span> désactive le flux. D’autres valeurs définissent la période pendant laquelle le flux attend avant de soumettre à nouveau le flux. La décision de soumettre le flux est prise à chaque index. En d’autres termes, à la fin de l’index, un flux est contrôlé pour vérifier s’il a expiré et s’il doit être mis à jour et soumis par le fournisseur. Il est également utilisé comme méthode pour empêcher un compte de se soumettre de manière excessive à un fournisseur. Certains fournisseurs appliquent des règles à l’égard des sources de flux de données qui se chargent trop fréquemment. Veillez à vérifier la politique du fournisseur de flux concernant la fréquence des envois. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_2D9ECAFB8E8544D39B486F7BC3DCE589"> <span class="uicontrol"> Méthode de transfert  </span> <p>La plupart des flux peuvent distribuer les fichiers de deux manières différentes : Réseau de contenu FTP et hébergé. </p> <p>La méthode de transfert recommandée pour l’envoi du flux de données est <span class="uicontrol"> FTP </span>. Google Merchant Center héberge un serveur FTP à cet effet. Consultez l’aide de Google Merchant Center sur la configuration d’un compte FTP Google distinct pour ce flux Google Shopping. </p> 
          <ul id="ul_BC0D8B541068407883CAC948496DBD0A"> 
          <li id="li_DB28CA23C94A4AF09E1A0EB06DF8F40C"> <span class="uicontrol"> FTP  </span> <p>Les serveurs de recherche/marchandisage de site utilisent le FTP passif. </p> <p>Le protocole FTP est le seul moyen de transférer un fichier vers un autre serveur. </p> <p> <span class="uicontrol"> Serveur FTP  </span> : indique le nom du serveur FTP. Dans ce cas, il s’agit de 
            <code>
              uploads.google.com 
            </code>. N’incluez pas le protocole ou le précédent "ftp://". </p> <p> <span class="uicontrol"> Nom d'utilisateur FTP  </span> - Indique le nom du compte FTP. </p> <p> <span class="uicontrol"> Mot de passe FTP  </span> - Indique le mot de passe du compte FTP. </p> <p> <span class="uicontrol"> Nom de fichier FTP  </span> - Indique le nom du fichier à transmettre. Ce nom est un modèle si le flux génère plusieurs fichiers, en incrémentant généralement un nombre à la fin du nom mais avant l’extension. Par exemple : basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml </p> <p> <span class="uicontrol"> Répertoire FTP  </span> - Si un chemin d'accès au répertoire spécifique est requis, entrez-le ici. N’incluez pas le nom de fichier dans le chemin d’accès. </p> </li> 
          <li id="li_5990927146434DAF89273F4636D21437"> <span class="uicontrol"> Réseau de contenu hébergé  </span> <p>Le réseau de contenu est le moyen de diffuser des fichiers à partir des serveurs Web de la recherche/marchandisage sur site. Le destinataire du flux l’extrait des serveurs Web à l’aide d’une requête HTTP. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Vérification </p> </td> 
      <td colname="col3"> <p>Lorsque vous accédez au panneau <span class="wintitle"> Vérification </span>, votre flux est enregistré à ce stade. Toutefois, les fichiers de flux réels ne sont enregistrés qu’à une date ultérieure. </p> <p>Le panneau <span class="wintitle"> Vérification </span> vous permet d’effectuer les opérations suivantes : </p> 
        <ul id="ul_4A94355A8DF840A3BAF6BD5E9F11C27F"> 
        <li id="li_825697CB36B34C4AB5959B15EDDB55F1"> <span class="uicontrol"> Vue de données  </span> <p>Permet de cliquer sur le lien pour vérifier la sortie du flux au moyen d’une vue de données affichée dans un tableau. La vue de données peut également vous aider à résoudre les problèmes en vous montrant quels champs de métadonnées sont sélectionnés et comment tout critère de recherche spécifié dans le panneau <span class="wintitle"> Critères de recherche </span> de l’assistant affecte la sortie du flux. La vue de données est générée de manière dynamique, de sorte qu’elle est disponible à tout moment. </p> </li> 
        <li id="li_91B8B5F5F9DE4A13863CD62F74AA6206"> <span class="uicontrol"> Fichiers de flux  </span> <p>Une fois que les serveurs de recherche/marchandisage de site ont généré les fichiers de flux, vous pouvez utiliser la liste déroulante <span class="uicontrol"> Fichiers de flux </span> pour vue les fichiers à partir des serveurs. Un nouvel onglet de navigateur ou une nouvelle fenêtre de navigateur s’affiche avec le contenu du flux. Cette méthode est utile pour résoudre les problèmes de mise en forme des flux qui posent problème. Notez que vous ne vues pas les fichiers à partir de la destination finale ou des fournisseurs eux-mêmes. </p> <p> Si le flux est nouveau, la liste déroulante est vide jusqu’à ce que vous génériez des fichiers de flux. </p> </li> 
        <li id="li_4A5EC089628E43029A38F8919888FF0A"> <span class="uicontrol"> Lien réseau de contenu  </span> <p>Si vous avez choisi <span class="uicontrol"> Hosted Content Network </span> comme méthode de téléchargement dans le panneau <span class="wintitle"> File Submission </span> de l'Assistant, l'URL s'affiche ici. Si vous n’avez encore généré aucun fichier de flux, l’URL n’est pas valide tant que le flux n’a pas été généré correctement. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

   **Plans de site Google**

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Panneau </p> </th> 
      <th colname="col2" class="entry"> <p>Nom du panneau Assistant </p> </th> 
      <th colname="col3" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>3 </p> </td> 
      <td colname="col2"> <p>Nom du flux </p> </td> 
      <td colname="col3"> <p>Indique le nom du flux. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>2 </p> </td> 
      <td colname="col2"> <p>Zones cliquables </p> </td> 
      <td colname="col3"> <p>Permet de mapper des champs de flux spécifiques au fournisseur aux champs de métadonnées de recherche/marchandisage de site. Cette étape de mappage dans l’assistant est importante car elle permet aux flux de mettre en corrélation les informations entre les champs de l’index et les champs des données du flux. Dans la plupart des cas, à l’exception de <span class="wintitle"> Flux génériques </span>, les corrélations sont enregistrées dans un modèle de recherche généré dynamiquement. </p> <p>Chaque ligne de la table Zone cliquable représente un mappage de champ. Dans la colonne Ajouter/Supprimer du tableau, cliquez sur <span class="uicontrol"> + </span> pour ajouter une nouvelle ligne de mappage de champ ; cliquez sur <span class="uicontrol"> - </span> pour supprimer de la table la ligne de mappage de champ actuellement sélectionnée. Pour associer un champ de flux à un champ de métadonnées, utilisez les listes déroulantes correspondantes pour choisir les champs de votre choix. </p> <p> <b>Utilisation avancée</b> </p> <p>Vous pouvez créer vos propres champs personnalisés. Dans la liste déroulante <span class="wintitle"> Champs de flux </span>, cliquez sur <span class="uicontrol"> Personnalisé </span>. Dans le champ de texte associé, saisissez un nom de balise personnalisé pour ce champ. Cette option personnalisée est utile si un flux nécessite des champs spécifiques à un fournisseur. </p> <p>Vous pouvez également créer un champ de métadonnées personnalisé. Dans la liste déroulante <span class="wintitle"> Champs de métadonnées </span>, cliquez sur <span class="uicontrol"> Personnalisé </span>. Dans le champ de texte associé, saisissez une valeur de champ de métadonnées personnalisée. La valeur est insérée dans le modèle prégénéré et peut également être utilisée pour injecter des balises de modèle de recherche personnalisée. </p> <p>Voir <a href="../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4" type="reference" format="dita" scope="local"> Balises de modèle de recherche </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>1 </p> </td> 
      <td colname="col2"> <p>Critères de recherche </p> </td> 
      <td colname="col3"> <p>Lorsque les fichiers de flux sont générés, une requête de recherche est utilisée pour filtrer les données. Vous définissez les filtres utilisés pour la requête de recherche dans ce panneau. </p> 
        <ul id="ul_994585E89A044BD3A89A99D30F277432"> 
        <li id="li_61FA9246B9824E3C8124958C8EBFF0DA"> <span class="uicontrol"> Meta Field  </span> <p>Définit le champ de métadonnées sur lequel vous souhaitez filtrer. </p> <p> <b>Utilisation avancée</b> </p> <p>Le système de filtrage étant une requête de recherche standard, vous pouvez sélectionner <span class="uicontrol"> Formulaire libre </span> dans la liste déroulante pour entrer des paramètres de recherche CGI et leurs valeurs. L’échappement d’URL est obligatoire. L'argument de recherche <span class="codeph"> sp_q </span> est ignoré. Vous pouvez créer plusieurs lignes de zones de texte Formulaire libre. Entre chaque ligne, les arguments sont délimités automatiquement par des &amp;. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Paramètres CGI de recherche </a>. </p> </li> 
        <li id="li_A5D00883738845C8B8F612A7521F160F"> <span class="uicontrol"> Critères </span> <p>Définit l’opération de filtrage. L’opération de filtrage que vous sélectionnez dans la liste déroulante applique la valeur constante saisie dans la troisième colonne. </p> </li> 
        <li id="li_5A312C2984454C2CB518CA453AD9F6D2"> <span class="uicontrol"> Valeur </span> <p>Valeur constante. </p> </li> 
        <li id="li_666AAE1BC7A2432E91953B08EC7394DC"> <span class="uicontrol"> Action  </span> <p>Ajoute une nouvelle ligne de mappage de champ ou supprime la ligne actuellement mise en surbrillance. </p> </li> 
        </ul> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>4 </p> </td> 
      <td colname="col2"> <p>Envoi du fichier </p> </td> 
      <td colname="col3"> <p>Vous permet de configurer le calendrier d’envoi des fichiers de flux et de définir la méthode à utiliser pour télécharger les fichiers. </p> 
        <ul id="ul_49B3255BE669424B925BBAEE4C9B385F"> 
        <li id="li_939828C774D440EBB0769F6D5B0BBA23"> <span class="uicontrol"> Planification </span> <p>Définit la fréquence maximale d’envoi d’un flux. La sélection de <span class="uicontrol"> Jamais </span> désactive le flux. D’autres valeurs définissent la période pendant laquelle le flux attend avant de soumettre à nouveau le flux. La décision de soumettre le flux est prise à chaque index. En d’autres termes, à la fin de l’index, un flux est contrôlé pour vérifier s’il a expiré et s’il doit être mis à jour et soumis par le fournisseur. Il est également utilisé comme méthode pour empêcher un compte de se soumettre de manière excessive à un fournisseur. Certains fournisseurs appliquent des règles à l’égard des sources de flux de données qui se chargent trop fréquemment. Veillez à vérifier la politique du fournisseur de flux concernant la fréquence des envois. </p> <p> 
          <!--The time of the last upload and the status of the upload feed is displayed here. If any other feeds are currently running, their status appears here instead. Each account processes one feed at a time. --> </p> <p> 
          <!--Click <uicontrol>Manual Upload</uicontrol> to generate the feed and push the files to the final destination. Any schedule restrictions that you have already set are ignored. --> </p> <p> 
          <!--If <uicontrol>Manual Upload</uicontrol> is dimmed (inactive), the account is currently processing this feed or another feed. An account only works with one feed at a time. --> </p> </li> 
        <li id="li_07B5BCF7936241A7915C4898B231184B"> <span class="uicontrol"> Méthode de transfert  </span> <p>La plupart des flux peuvent distribuer les fichiers de deux manières différentes : Réseau de contenu FTP et hébergé. </p> 
          <ul id="ul_74FA98A82754469BA5FADCC63FC364F7"> 
          <li id="li_02940B712D6444A8B65C0A51834187E6"> <span class="uicontrol"> FTP  </span> <p>Les serveurs de recherche/marchandisage de site utilisent le FTP passif. </p> <p>Le protocole FTP est le seul moyen de transférer un fichier vers un autre serveur. </p> <p> <span class="uicontrol"> Serveur FTP  </span> : indique le nom du serveur FTP. N’incluez pas le protocole ou le précédent "ftp://". </p> <p> <span class="uicontrol"> Nom d'utilisateur FTP  </span> - Indique le nom du compte FTP. </p> <p> <span class="uicontrol"> Mot de passe FTP  </span> - Indique le mot de passe du compte FTP. </p> <p> <span class="uicontrol"> Nom de fichier FTP  </span> - Indique le nom du fichier à transmettre. Ce nom est un modèle si le flux génère plusieurs fichiers, en incrémentant généralement un nombre à la fin du nom mais avant l’extension. Par exemple : basename.xml, basename1.xml, basename2.xml, ..., basename-Nth.xml </p> <p> <span class="uicontrol"> Répertoire FTP  </span> - Si un chemin d'accès au répertoire spécifique est requis, entrez-le ici. N’incluez pas le nom de fichier dans le chemin d’accès. </p> </li> 
          <li id="li_EAE504436CD84452BA04BE51855A2BEF"> <span class="uicontrol"> Réseau de contenu hébergé  </span> <p>Le réseau de contenu est le moyen de diffuser des fichiers à partir des serveurs Web de la recherche/marchandisage de site. Le destinataire du flux l’extrait des serveurs Web à l’aide d’une requête HTTP. </p> <p> 
            <!--After the base filename is entered and the feed is successfully saved, the URL of the Content Network file is displayed on the Verification panel of the wizard. The URL becomes active after the feed is successfully processed. The vendor can get the feed data from this URL. Multiple files use the same URL path. However, be sure that you replace or change the filename according to the enumeration scheme. --> </p> </li> 
          </ul> </li> 
        </ul> <p>Notez que l’une ou l’autre des méthodes de téléchargement requiert que vous spécifiez l’URL utilisée par Google pour récupérer le plan de site, dans le champ <span class="wintitle"> URL du plan de site principal </span>. Le nom du fichier de plan de site est également déterminé ici. Si votre plan de site est volumineux, plusieurs fichiers peuvent exister et la convention d’affectation de nom consiste à joindre un numéro d’index à la fin du fichier en commençant par le numéro 1. Le premier fichier ou fichier d’index n’a pas d’index, comme dans <span class="codeph"> sitemap.xml </span>, <span class="codeph"> sitemap1.xml </span>, <span class="codeph"> sitemap2.xml </span> ... <span class="codeph"> sitemap12.xml </span>. </p> <p>Si vous choisissez <span class="uicontrol"> Réseau de contenu hébergé </span> comme méthode de téléchargement, l’URL des fichiers a les mêmes noms de fichier, mais l’URL a le chemin et le nom d’hôte du service d’hébergement. Par conséquent, vous redirigez les requêtes du plan de site vers le réseau de contenu hébergé. Vous devriez également pouvoir extraire les fichiers du même emplacement. </p> <p>Une fois les fichiers de flux créés et envoyés à la destination intermédiaire, Google est en train d’effectuer un balayage et leur indique que le flux de plan de site est prêt. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>5 </p> </td> 
      <td colname="col2"> <p>Vérification </p> </td> 
      <td colname="col3"> <p>Lorsque vous accédez au panneau <span class="wintitle"> Vérification </span>, votre flux est enregistré à ce stade. Toutefois, les fichiers de flux réels ne sont enregistrés qu’à une date ultérieure. </p> <p>Le panneau <span class="wintitle"> Vérification </span> vous permet d’effectuer les opérations suivantes : </p> 
        <ul id="ul_A1D889A84972419599FC83F39EA2676A"> 
        <li id="li_C8ED077B6DD1461E85A4914C1CFDBE88"> <span class="uicontrol"> Vue de données  </span> <p>Permet de cliquer sur le lien pour vérifier la sortie du flux au moyen d’une vue de données affichée dans un tableau. La vue de données peut également vous aider à résoudre les problèmes en vous montrant quels champs de métadonnées sont sélectionnés et comment tout critère de recherche spécifié dans le panneau <span class="wintitle"> Critères de recherche </span> de l’assistant affecte la sortie du flux. La vue de données est générée de manière dynamique, de sorte qu’elle est disponible à tout moment. </p> </li> 
        <li id="li_DACEE40703AF40EFBCD90D43825CE9C1"> <span class="uicontrol"> Fichiers de flux  </span> <p>Une fois les fichiers de flux générés, vous pouvez utiliser la liste déroulante <span class="uicontrol"> Fichiers de flux </span> pour vue les fichiers à partir des serveurs. Un nouvel onglet de navigateur ou une nouvelle fenêtre de navigateur s’affiche avec le contenu du flux. Cette méthode est utile pour résoudre les problèmes de mise en forme des flux qui posent problème. Notez que vous ne vue pas les fichiers depuis la destination finale ou les fournisseurs eux-mêmes. </p> <p> Si le flux est nouveau, la liste déroulante est vide jusqu’à ce que vous génériez des fichiers de flux. </p> </li> 
        <li id="li_1C530354B4F34EC79D92CEFEB5B39ED7"> <span class="uicontrol"> Lien réseau de contenu  </span> <p>Si vous avez choisi <span class="uicontrol"> Hosted Content Network </span> comme méthode de téléchargement dans le panneau <span class="wintitle"> File Submission </span> de l'Assistant, l'URL s'affiche ici. Si vous n’avez encore généré aucun fichier de flux, l’URL n’est pas valide tant que le flux n’a pas été généré correctement. </p> </li> 
        </ul> </td> 
      </tr> 
    </tbody> 
    </table>

1. Lorsque vous avez terminé les étapes de l&#39;Assistant, cliquez sur **[!UICONTROL Close]**.

## Modification d’un flux {#task_B855D28CD99B4FA58E2D4D4FD6DC9CEB}

Vous pouvez modifier la configuration d’un flux existant.

<!-- 

t_editing_a_feed.xml

 -->

>[!NOTE]
>
>Lorsque vous modifiez un flux, vous ne pouvez pas modifier son type. Si vous devez modifier le type de flux, supprimez le flux existant, puis ajoutez un nouveau flux avec le type souhaité.

Voir [Suppression d’un flux](../c-about-settings-menu/c-about-searching-menu.md#task_7E39A140E69D43C6B61FB42E81051269).

**Pour modifier un flux**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Effectuez l’une des opérations suivantes :

* Sur la page [!DNL Feeds], sous la colonne [!DNL Name] du tableau, cliquez sur la liste déroulante en regard d’un nom de flux, puis cliquez sur **[!UICONTROL Edit feed]**.

* Sur la page [!DNL Feeds], sous la colonne [!DNL Name], cliquez sur le nom d’un flux que vous souhaitez modifier.

1. Dans l’assistant de flux, définissez les options souhaitées pour chaque panneau de l’assistant.

   Consultez les tableaux des options sous **Ajouter un flux**.
1. À la fin de l&#39;Assistant, dans le panneau [!DNL Verification], cliquez sur **[!UICONTROL Close]**.

## Suppression d’un flux {#task_7E39A140E69D43C6B61FB42E81051269}

Vous pouvez supprimer un flux dont vous n’avez plus besoin ou que vous n’utilisez plus.

<!-- 

t_deleting_a_feed.xml

 -->

**Pour supprimer un flux**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Dans l’écran [!DNL Feeds Menu], sous la colonne [!DNL Actions], cliquez sur **[!UICONTROL Delete]** pour le nom du flux à supprimer.
1. Dans la boîte de dialogue [!DNL Delete feed], cliquez sur **[!UICONTROL Yes]** pour confirmer la suppression.

## Affichage des fichiers de flux {#task_1E413C7650DE466EA68925F72E086884}

Vous pouvez accéder au dernier panneau de l’assistant Flux pour accéder rapidement à l’affichage de la vue de données du flux ou pour télécharger les fichiers de flux actuels à partir du serveur. Cette fonctionnalité est utile si vous souhaitez vérifier et examiner la sortie du flux.

<!-- 

t_viewing_feed_files.xml

 -->

**Pour vue des fichiers de flux**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Sur la page [!DNL Feeds], sous la colonne [!DNL Name] du tableau, cliquez sur la liste déroulante en regard d’un nom de flux, puis cliquez sur **[!UICONTROL View Feed Files]**.
1. Dans le panneau [!DNL Verification] de l’assistant du flux, cliquez sur **[!UICONTROL Show Data View]**.
1. Cliquez sur **[!UICONTROL Close]**.

## Test d’un flux sans téléchargement de fichier {#task_F1F390F72E0A4886B6CD4CD86EDB4C8C}

Vous pouvez tester un flux sans télécharger de fichiers vers la destination finale.

<!-- 

t_testing_a_feed_with_no_file_upload.xml

 -->

**Pour tester un flux sans téléchargement de fichier**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Sur la page [!DNL Feeds], sous la colonne [!DNL Name] du tableau, cliquez sur la liste déroulante en regard d’un nom de flux, puis cliquez sur **[!UICONTROL Test Feed (No file upload)]**.
1. Sur la page [!DNL Feeds], la colonne [!DNL Feed Status] est mise à jour pendant et après le test.

## Génération et chargement d’un flux {#task_C9A57827C7674035B62A22D310DDAA0C}

Vous pouvez générer et envoyer manuellement des fichiers de flux vers la destination finale, quelle que soit la planification que vous avez définie dans le panneau [!DNL File Submission] de l’assistant Flux.

<!-- 

t_generating_and_uploading_a_feed.xml

 -->

Voir aussi [Création d’un flux](../c-about-settings-menu/c-about-searching-menu.md#task_63179C1FC359497483CD6CE13FD1C250).

**Pour générer et télécharger un flux**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Searching]** > **[!UICONTROL Feeds]**.
1. Sur la page [!DNL Feeds], sous la colonne [!DNL Name] du tableau, cliquez sur la liste déroulante en regard d’un nom de flux, puis cliquez sur **[!UICONTROL Generate and Upload Feed]**.
1. Sur la page [!DNL Feeds], la colonne [!DNL Feed Status] est mise à jour pendant et après la génération et le transfert du flux de données.
