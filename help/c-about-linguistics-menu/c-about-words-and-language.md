---
description: Vous pouvez utiliser Mots et langue pour déterminer comment les termes de recherche correspondent au contenu de vos pages Web.
solution: Target
title: A propos des mots et de la langue
topic: Linguistique,Recherche sur le site et marchandisage
uuid: 793d7a40-4609-44b8-a170-536eb1434537
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1026'
ht-degree: 0%

---


# Mots et langue{#about-words-language}

Vous pouvez utiliser [!DNL Words & Language] pour déterminer comment les termes de recherche correspondent au contenu de vos pages Web.

## Utilisation des mots et de la langue {#concept_CEB4B9576F3C4E2EB87B352EEC738D79}

Avant que les effets des paramètres [!DNL Words & Language] ne soient accessibles aux visiteurs du site, y compris les modifications que vous apportez à ces paramètres, vous devez régénérer l&#39;index de votre site. La régénération, contrairement à l’indexation, n’implique pas l’analyse de vos pages Web et ne prend que quelques secondes.

## Configuration de la correspondance des termes de recherche avec votre contenu Web {#task_351A9144A51F4B41923BDBACDEF3B616}

Vous pouvez utiliser les mots et la langue pour déterminer comment la recherche/le marchandisage sur le site correspond aux termes de recherche au contenu de vos pages Web.

<!-- 

t_configuring_how_search_terms_matched_to_your_web_content.xml

 -->

**Pour configurer la correspondance des termes de recherche avec votre contenu Web**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Words & Language]**.
1. Sur la page [!DNL Words & Languages], définissez les options de votre choix.

   <!-- 
   
   r_words_and_languages_options.xml
   
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
      <td colname="col1"> <p>Respect de la casse </p> </td> 
      <td colname="col2"> <p>Non sélectionné par défaut. </p> <p>Détermine si les lettres en majuscules sont distinguées des lettres en minuscules. Par exemple, lorsque cette option est sélectionnée, "Réussite" est distingué de "Réussite" et les résultats de la recherche peuvent varier d’une recherche à l’autre. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Sensibilité diacritique </p> </td> 
      <td colname="col2"> <p>Sélectionné par défaut. </p> <p> Détermine si les mots qui contiennent des caractères diacritiques sont distingués des mots qui ne le sont pas. Par exemple, lorsqu’elle est sélectionnée, "pagina" est distingué de "página". Désélectionnez cette option si vous disposez d’un site Web qui utilise des langues autres que l’anglais. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Numéros </p> </td> 
      <td colname="col2"> <p>Sélectionné par défaut. </p> <p>Détermine si les mots contenant des chiffres sont indexés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorer les apostrophes </p> </td> 
      <td colname="col2"> <p>Non sélectionné par défaut. </p> <p>Les apostrophes sont retirées des requêtes. Par exemple, une recherche sur "Arbres" retournerait les mêmes résultats qu’une recherche sur "Arbres". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorer les tirets </p> </td> 
      <td colname="col2"> <p>Non sélectionné par défaut. </p> <p>Les tirets sont supprimés des requêtes. Par exemple, une recherche de "blue-bell" retournerait les mêmes résultats qu’une recherche de "bluebell". </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Correspondance alphanumérique partielle </p> </td> 
      <td colname="col2"> <p>Non sélectionné par défaut. </p> <p>Lorsqu’elle est sélectionnée, cette option vous permet de fractionner des jetons sur des transitions alphabétiques et numériques pour permettre des correspondances en texte libre sur des jetons de pièce ou de produit. </p> <p>Supposons, par exemple, que vous disposiez d’un identifiant de produit <span class="codeph"> 910XT </span> dans le contenu du corps d’une ou de plusieurs pages d’un site Web. Lorsque cette option est <i>non</i> sélectionnée, <span class="keyword"> Search &amp; Promote d'Adobe </span> trouve des correspondances pour cet identifiant de produit lors de la recherche de <span class="codeph"> 910XT </span>. Et, avec <span class="uicontrol"> l'option Rechercher Concat-Div-Enable </span> activée, <span class="keyword"> Adobe Search &amp; Promote </span> trouverait également <span class="codeph"> 910 XT </span>. Cependant, il ne trouverait pas exclusivement les instances de <span class="codeph"> 910 </span> ou <span class="codeph"> XT </span>. </p> <p>Lorsque vous sélectionnez <span class="uicontrol"> Correspondance alphanumérique partielle </span>, l’indexeur fractionne ces jetons alphanumériques mixtes en plusieurs jetons. Par exemple, un identifiant de produit tel que <span class="codeph"> XYZ123 </span> est indexé en trois jetons : <span class="codeph"> XYZ123 </span>, <span class="codeph"> XYZ </span> et <span class="codeph"> 123 </span>. Cette fonctionnalité permet la mise en correspondance de texte libre en temps de recherche sur l’une de ces variantes. </p> <p>Dans un autre exemple, supposons que vous disposiez de l’identifiant de produit <span class="codeph"> AB910XT </span>. Si vous sélectionnez <span class="uicontrol"> Correspondance alphanumérique partielle </span> <i>et </i> que <span class="uicontrol"> Concat-Div-Enable </span> est activé, <span class="keyword"> Adobe Search &amp; Promote </span> l'indexe comme <span class="codeph"> AB910XT </span>, <span class="codeph"> </span>, <span class="codeph"> 910 </span> et <span class="codeph"> XT </span>. Ensuite, lorsqu’un utilisateur recherche <span class="codeph"> 910XT </span>, par exemple, la recherche se développe pour trouver également les instances de <span class="codeph"> 910XT </span>, <span class="codeph"> 910 </span> ou <span class="codeph"> XT </span>. </p> <p> <p>Remarque :  <span class="uicontrol"> La recherche Concat-Div-Enable </span> n'est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> </p> <p> <p>Remarque :  <span class="uicontrol"> Correspondance alphanumérique partielle </span> est appliquée globalement à tous les champs indexés. Cependant, elle n'affecte que la mise en correspondance de texte libre ; cela n'affecte pas la correspondance exacte ou la correspondance de plage. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Correspondance sonore </p> </td> 
      <td colname="col2"> <p>Sélectionné par défaut. </p> <p>Les mots qui se ressemblent sont associés comme "santé" et "santé". Cette fonctionnalité permet à votre client de rechercher facilement malgré une faute d'orthographe d'un mot. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Autre Forms Word </p> </td> 
      <td colname="col2"> <p>La valeur par défaut est <b>Forms Word alternatif par défaut</b>. </p> <p>Vous pouvez sélectionner l’une des options suivantes dans la liste déroulante Autre mot Forms : 
      <ul id="ul_CAC73FB4D1384312BB5DD327D3D66948"> 
      <li id="li_F4E76CD27EA34AC5BC81E648BC6CBA4C"><b>None</b> <p>Aucun formulaire de recherche de radical ni aucun autre formulaire de texte n’est appliqué lors de l’indexation. </p> </li> 
      <li id="li_3186FD1F3BC94A5CB66FFF8EA6726D81"><b>Forms Word secondaire par défaut</b> <p>Le blocage s’effectue automatiquement lors de l’indexation. </p> </li> 
      <li id="li_5815DE0795E0423C9C84C62B96A3F841"><b>Dictionnaire de domaine</b> <p>Tout dictionnaire de domaine que vous définissez en tant que dictionnaire de radical est utilisé comme source d’autres formulaires Word. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> A propos des dictionnaires </a>. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-dictionaries.md#task_541E8453A12F4A8E89CF6F595469F074" type="task" format="dita" scope="local"> Configuration d’un dictionnaire en tant que dictionnaire de recherche de radical </a>. </p> </li> 
      </ul> </p> <p>Si l’enchaînement des expressions est activé dans l’<span class="keyword"> Search &amp; Promote d’Adobe </span>, sachez que d’autres formulaires de mots se produisent également dans les expressions. </p> <p>Voir <a href="../c-searchpromote-release-notes/c-rn-06-19-14-version-815.md#concept_E8CEBC65A28A4E61BDE69B4B4DA55E73" format="dita" scope="local"> Notes de mise à jour de la Search &amp; Promote 8.15.0 (19/06/2014) </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Langue </p> </td> 
      <td colname="col2"> <p>La valeur par défaut est <b>Anglais (Etats-Unis)</b>. </p> <p>La langue sélectionnée garantit que les valeurs de date et numériques sont analysées selon les conventions utilisées dans la partie sélectionnée du monde. </p> <p>Lorsque <span class="uicontrol"> Forms Word de remplacement </span> est défini sur <span class="uicontrol"> Forms Word de remplacement par défaut </span> ou sur <span class="uicontrol"> Dictionnaire de domaine </span>, les formulaires de mots et les fins de mot changent selon les règles linguistiques de la langue sélectionnée. </p> <p>Par défaut, le paramètre Langue n’est pas utilisé pour déterminer la langue des pages lues sur votre site Web. La langue d’une page lue est déterminée à partir de ses en-têtes HTTP ou des métadonnées de la page elle-même. Votre site Web peut contenir des pages dans plusieurs langues différentes. Chaque page est correctement lue et indexée, quelle que soit la langue sélectionnée ici. </p> <p>Si vous utilisez un codage de jeu de caractères Unicode tel que UTF-8 pour certaines pages de votre site Web, assurez-vous que la langue de chacune de ces pages est correctement spécifiée. Si les en-têtes ou les métadonnées HTTP appropriés n’existent pas pour vos documents Unicode, vous pouvez utiliser <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Injections </span> pour spécifier la langue appropriée. </p> <p>Cochez <span class="uicontrol"> Appliquer aux documents sans langue spécifiée ? </span> pour utiliser le paramètre Langue pour les pages lues à partir de votre site Web sans paramètre explicite. Utilisez ce paramètre uniquement si <i>certains </i> de vos documents ne possèdent pas de paramètres de langue. Utilisez <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Injections </span> si <i>aucun</i> de vos documents a des paramètres de langue, ou si l'ensemble de documents concernés est une liste bien connue et gérablement petite. </p> <p>Voir <a href="../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5" type="concept" format="dita" scope="local"> À propos des injections </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Utiliser le décompositeur ? </p> </td> 
      <td colname="col2"> <p> <p>Remarque :  Cette fonctionnalité est uniquement utilisée pour le danois et l’allemand. En outre, cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. Une fois activé, l'<b>Utiliser le décompositeur ?</b> n’apparaît dans l’interface utilisateur que si vous sélectionnez  <span class="uicontrol"> danois  </span> ou  <span class="uicontrol"> allemand  </span> dans la liste  <span class="uicontrol">   </span> déroulante Langue décrite plus haut dans ce tableau. </p> </p> <p>Lorsque vous sélectionnez <span class="uicontrol"> Utiliser le décompositeur ? </span>, le service ventile les mots composés danois ou allemands, qui permettent l'indexation des mots composant avec les mots composés d'origine. </p> <p>Pour voir comment fonctionne cette fonction, saisissez des mots dans le champ de texte, puis cliquez sur <span class="uicontrol"> Test </span>. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Settings]**.
1. Pour prévisualisation les résultats de vos modifications, cliquez sur **[!UICONTROL regenerate your staged site index]** pour recréer l&#39;index de votre site Web intermédiaire.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

