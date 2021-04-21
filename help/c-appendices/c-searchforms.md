---
description: En savoir plus sur les formulaires de recherche dans Search&amp;Promote
solution: Target
title: Rechercher des formulaires
topic-legacy: Appendices,Site search and merchandising
uuid: 91153e3a-c437-47f3-8c2a-d9ac02965b8c
exl-id: 9771a19d-86a8-41db-9c80-d734fbd10ab7
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '2926'
ht-degree: 0%

---

# Rechercher des formulaires{#search-forms}

## Utilisation des collections dans les formulaires de recherche {#reference_5A079AEEEFB84457892EF0870D0605C3}

Les collections permettent à vos clients de rechercher des zones spécifiques de votre site Web. Selon que vous mettez en oeuvre une liste déroulante ou une liste de cases à cocher, vous pouvez permettre à vos clients de rechercher une ou plusieurs collections.

Voir aussi [A propos des collections](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127).

L’exemple suivant montre quatre noms de collection différents et les zones associées du site Web qu’ils couvrent :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nom de la collection </p> </th> 
   <th colname="col2" class="entry"> <p> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Variable  </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7AE70789C0914EBFBCCC7695C6F53B9E"> 
      <li id="li_72525BAA34E2442D86152F2FD8CA83D5"> https://www.mycompany.com/products.htm </li> 
      <li id="li_5CA4152239124BDBB251E6C94B15D45B"> https://www.mycompany.com/publish/ </li> 
      <li id="li_6E266736B3494696A3AFD841C4AFEC57"> https://www.mycompany.com/search/ </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Clients </p> </td> 
   <td colname="col2"> <p>https://www.mycompany.com/customers/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Actualités </p> </td> 
   <td colname="col2"> <p>https://www.mycompany.com/news/ </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>À propos de l'Adobe </p> </td> 
   <td colname="col2"> <p>https://www.mycompany.com/company/ </p> </td> 
  </tr> 
 </tbody> 
</table>

L’interface de formulaire de recherche déroulante permet aux utilisateurs de sélectionner une collection et ressemble à ce qui suit :

![](assets/DropdownsearchformUI.png)

Le formulaire de recherche déroulante est généré avec le code HTML suivant :

```
<select name="sp_k"> 
<option value="">All of Adobe</option> 
<option value="Products">Products</option> 
<option value="Customers">Customers</option> 
<option value="News">News</option> 
<option value="About Adobe">About Adobe</option> 
</select>
```

Vous pouvez également utiliser un groupe de cases à cocher dans votre formulaire de recherche afin que les visiteurs puissent sélectionner plusieurs collections :

![](assets/checkboxes.png)

Le formulaire de recherche de case à cocher est généré avec le code HTML suivant :

```
<input type="checkbox" name="sp_k" value="">All of Adobe<br> 
<input type="checkbox" name="sp_k" value="Products">Products<br> 
<input type="checkbox" name="sp_k" value="Customers">Customers<br> 
<input type="checkbox" name="sp_k" value="News">News<br> 
<input type="checkbox" name="sp_k" value="About Adobe">About Adobe<br>
```

## Résultats de la recherche {#section_BBDD5B44E2B349BC88D937F44583D350}

La balise de modèle de recherche `<search-input-collections>` génère le code HTML de la zone de liste de la collection dans les résultats de la recherche et sélectionne automatiquement la collection spécifiée dans la recherche. Si vous souhaitez plutôt générer des cases à cocher, utilisez la balise `<search-input>` au lieu de la balise `<input>` comme suit :

```
<search-input type="checkbox" name="sp_k" value="">All of Adobe<br> 
<search-input type="checkbox" name="sp_k" value="Products">Products<br> 
<search-input type="checkbox" name="sp_k" value="Customers">Customers<br> 
<search-input type="checkbox" name="sp_k" value="News">News<br> 
<search-input type="checkbox" name="sp_k" value="About Adobe">About Adobe<br>
```

La balise `<search-input>` génère une balise `<input>` et inclut l&#39;attribut `checked` si la collection a été spécifiée dans la recherche.

## Utilisation de cadres avec des formulaires {#reference_82CDDDA1E37042E4849EBF7EA05407C5}

Vous pouvez configurer vos jeux de cadres pour qu&#39;ils fonctionnent avec la recherche/le marchandisage sur le site.

Pour en savoir plus sur les cadres HTML et l&#39;élément de jeu de cadres HTML, voir l&#39;URL suivante :

[https://www.w3schools.com/html/html_frames.asp](https://www.w3schools.com/html/html_frames.asp)

Si votre site utilise des cadres, vous pouvez spécifier une cible pour les liens de résultats de recherche. La cible par défaut est _self, qui ouvre les liens dans le cadre actif ou la fenêtre de navigateur. Vous pouvez plutôt spécifier des cibles spécifiques au site ou réservées au navigateur :

* _top (réservé au navigateur) s’ouvre dans la fenêtre active du navigateur et remplace toutes les images actives.
* _blank (réservé au navigateur) s’ouvre dans une nouvelle fenêtre de navigateur.
* _parent (réservé au navigateur) s’ouvre dans le cadre parent du cadre actif.
* frame2 (spécifique au site) s’ouvre dans un cadre nommé &quot;frame2&quot;. Vous pouvez spécifier le nom de n’importe quel cadre comme valeur (par exemple, main ou contenu).

Si votre site n’utilise pas de cadres, vous ne souhaitez probablement pas modifier le nom de la cible par défaut.

Si vous créez un modèle de résultats de recherche personnalisé pour votre site Web, vous pouvez remplacer le paramètre spécifié en utilisant l&#39;attribut `target` de la balise `<search-link>`.

Le processus de configuration des jeux de cadres est le suivant :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Étape du processus </p> </th> 
   <th colname="col02" class="entry"> <p>Description du processus </p> </th> 
   <th colname="col2" class="entry"> <p>Lien </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col02"> <p>Ajoutez le formulaire au cadre de votre choix dans votre page Web. </p> </td> 
   <td colname="col2"> <p> <a href="#section_BAA8A502BB2243F8B5FF9783CDF2BFFD" type="section" format="dita" scope="local"> Ajouter le code du formulaire de recherche à un cadre dans votre...  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col02"> <p>Définissez le cadre de cible de la page des résultats de la recherche. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="#section_532CACB90888467093D95EACB64FDFA1" type="section" format="dita"> Définition de la cible de la page des résultats de la recherche  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col02"> <p>Définissez la cible des liens créés à partir de la page des résultats de la recherche. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="#section_523248C5AC424D878321C21A23A5CD66" type="section" format="dita"> Définition de la cible des liens créés à partir des résultats de la recherche...  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col02"> <p>Modifiez les pages de cadres de navigation pour les empêcher d’être indexées. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="#section_C62E5F0EE1294D5EBD97E123E54433FC" type="section" format="dita"> Modification des pages du cadre de navigation pour les empêcher d'être...  </a> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col02"> <p>Testez le formulaire de recherche. </p> </td> 
   <td colname="col2"> <p> <a scope="local" href="#section_43D8D4A7BF524DC480DFE5442F6A2E3C" type="section" format="dita"> Test du formulaire de recherche  </a> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ajouter le code du formulaire de recherche dans un cadre de votre page Web {#section_BAA8A502BB2243F8B5FF9783CDF2BFFD}

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   Le code du formulaire de recherche HTML ressemble à ce qui suit :

   ```
   <!-- Adobe Target HTML for [your customer name] --> 
   <form method="get" action="https://search.atomz.com/search/"> 
   <input size=15 name="sp_q"><br> 
   <input type=submit value="Search"> 
   <input type=hidden name="sp_a" value="[your account number]"> 
   </form>
   ```

1. Sur la page [!DNL Standard Form Source], sélectionnez et copiez le code du formulaire de recherche HTML qui apparaît dans le champ de texte.
1. Collez le code du formulaire de recherche dans le cadre de votre choix dans votre jeu de cadres.

   Dans l’exemple ci-dessous, le code du formulaire de recherche est collé dans le cadre de navigation, c’est-à-dire le cadre vertical étroit situé à gauche de l’écran.

   ![](assets/frames1.gif)

## Définition du cadre de cible de la page des résultats de la recherche {#section_532CACB90888467093D95EACB64FDFA1}

Si vous avez placé le code de votre formulaire de recherche dans le cadre de navigation vertical comme ci-dessus, vous pouvez afficher les résultats de la recherche dans le cadre principal plus grand. Dans cet exemple, vous appelez le cadre principal &quot;body&quot; et le définissez comme cadre de cible.

![](assets/frames2.gif)

1. Pour spécifier le cadre de cible de la page de résultats, ajoutez une cible et une valeur au formulaire en modifiant la ligne suivante dans le code du formulaire de recherche à partir des éléments suivants :

   `<form method="get" action="https://search.atomz.com/search/">`

   à ce qui suit :

   `<form target="body" method="get" action="https://search.atomz.com/search/">`

   Veillez à placer des guillemets autour de la valeur de la cible du formulaire.

Lorsqu’un client effectue une recherche sur votre site Web, les résultats de la recherche apparaissent dans le cadre &quot;body&quot; de la page Web.

## Définition de la cible des liens créés à partir de la page de résultats de la recherche {#section_523248C5AC424D878321C21A23A5CD66}

Vous pouvez définir le cadre de destination en modifiant directement votre modèle.

Si vos résultats de recherche apparaissent dans le cadre &quot;body&quot;, vous souhaitez probablement que les liens s’ouvrent également dans le cadre &quot;body&quot;. Dans la mesure où il s’agit du même cadre, la valeur de cible `"_self"` qui est le paramètre par défaut, vous n’avez pas besoin d’apporter des modifications.

Vous pouvez également définir le cadre de destination pour les liens de résultats. Vous trouverez ci-dessous quelques exemples de ce que vous pouvez faire :

* Spécifiez des cadres différents pour les résultats de la recherche et leurs liens de sorte que les résultats de la recherche restent principaux dans leur propre cadre tandis que chaque résultat sur lequel l’utilisateur clique s’ouvre dans un cadre distinct.
* Indiquez que les résultats de la recherche s’ouvrent dans une nouvelle fenêtre vierge, de sorte que votre ancienne fenêtre reste principale avec son contenu d’origine, ce qui préserve également les résultats de la recherche.

Le nom de la cible peut être soit le nom d’un cadre spécifié dans votre code HTML, soit l’un des paramètres HTML par défaut suivants :

* `target="_blank"` Ouvrez les liens dans une nouvelle fenêtre vierge sans nom.

* `target="_self"` Par défaut. Ouvrez les liens dans la même fenêtre que celle où résident les résultats de la recherche. Dans ce cas, la fenêtre des résultats de la recherche initiale. Utilisez cette option pour remplacer une cible de base affectée globalement.

* `target="_parent"` Ouvrez les liens dans le jeu de cadres parent de la page de liens. Si le document n&#39;a pas de parent, cela fonctionne comme `"_self"` par défaut.

* `target="_top"` Ouvrez les liens dans la fenêtre complète. Si le document se trouve déjà en haut de l&#39;écran, cette fonction est par défaut de type `"_self"`. Utilisez cette option pour rompre l’imbrication arbitraire d’images profondes.

Par exemple, pour définir le cadre de destination de la cible `_blank`, vous pouvez modifier le modèle de la manière suivante :

1. Dans le menu produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Templates]**.

1. Sur la page [!DNL Staged Templates], dans le tableau, cliquez sur le nom du modèle avec le cadre de destination ciblé.
1. Recherchez la balise `<search-link>`. La balise `<search-link>` par défaut doit ressembler à ce qui suit :

   `<search-link><search-title length=100></search-link>`

1. Ajoutez la cible du cadre à la balise `<search-link>`. Dans l’exemple ci-dessus, saisissez `target="_blank"`. Veillez à inclure le trait de soulignement et les guillemets autour de la valeur de la cible.

   La balise `<search-link>` s’affiche désormais comme suit :

   `<search-link target="_blank"><search-title length=100></search-link>`

Lorsqu&#39;un visiteur de site sélectionne un lien de résultats de recherche, la page liée s&#39;ouvre désormais dans une nouvelle fenêtre vierge.

## Modification des pages du cadre de navigation pour les empêcher d&#39;être indexées {#section_C62E5F0EE1294D5EBD97E123E54433FC}

En règle générale, vous souhaitez exclure vos cadres de navigation de l’indexation avec vos résultats de recherche. Pour accomplir cette fonctionnalité, vous pouvez ajouter une balise META `noindex` à ces pages.

1. Ouvrez la source de page HTML pour votre cadre de navigation.
1. Ajoutez la balise meta suivante dans la section `<head>` de votre code HTML :

   `<meta name="robots" content="noindex">`

   Par exemple :

   ```
   <html> 
   <head> 
   <title>This page is a frameset that I do not want indexed</title> 
   <meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1"> 
   <meta name="robots" content="noindex"> 
   </head>
   ```

## Test du formulaire de recherche {#section_43D8D4A7BF524DC480DFE5442F6A2E3C}

1. Accédez à votre site Web et accédez à un formulaire.
1. Dans le champ de recherche, entrez quelques termes de recherche, puis cliquez sur **[!UICONTROL Search]**.

   Ce qui suit est vrai :

   * La page des résultats de la recherche s’affiche dans la cible spécifiée.
   * Les liens des résultats de la recherche se trouvent dans la cible spécifiée.
   * Les résultats du cadre de navigation n’apparaissent pas.

   Si vous rencontrez des problèmes avec les cadres après avoir testé le formulaire de recherche, contactez le service clientèle.

## Exemple de formulaire de recherche avancée {#reference_82E1051918744EBA88A01E9E6AE42C4A}

Vous pouvez modifier le code de formulaire avancé en fonction de vos besoins de conception et de contenu, ou ajouter ou supprimer des paramètres de recherche supplémentaires.

Votre page d&#39;accueil est un bon endroit pour insérer un formulaire de recherche avancée car de nombreux clients s&#39;attendent à y trouver une fonctionnalité de recherche. Vous pouvez également créer une page HTML qui comprend le formulaire de recherche et d’autres informations utiles, puis créer un lien vers cette page sur l’ensemble de votre site Web.

Si vous indexez du contenu sécurisé, les résultats de la recherche peuvent être diffusés à partir des serveurs Web de recherche sécurisés. Modifiez l’URL de l’attribut d’action du formulaire de recherche en : action=&quot;https://search.atomz.com/search/&quot; pour ce faire.

>[!NOTE]
>
>Certains éditeurs HTML ont du mal à coller du code HTML à partir d&#39;autres applications. Si le code HTML s’affiche sur votre page Web sous la forme de texte, copiez et collez le code de recherche dans un éditeur de texte simple, tel que le Bloc-notes sous Windows ou le texte simple sous Mac, puis copiez et collez à nouveau du simple éditeur de texte dans votre éditeur HTML.

Les paramètres de recherche sont utilisés dans le code de formulaire de recherche avancée pour créer des boutons radio, des cases à cocher et des zones de liste que les clients peuvent utiliser pour personnaliser des recherches individuelles. Les clients peuvent indiquer le nombre de résultats de recherche affichés, par exemple, ou une plage de dates, ou si des résumés s&#39;affichent avec les résultats de la recherche, via les options qui apparaissent dans les formulaires de recherche avancée.

A l’aide de l’exemple de formulaire de recherche avancée suivant, le reste de cette rubrique vous montre comment chaque option du formulaire est créée à l’aide des paramètres de recherche.

![](assets/advancedsearchform.png)

Vous pouvez vue l&#39;intégralité du code HTML du formulaire de recherche avancée de l&#39;exemple ci-dessus.

Voir [Code HTML du formulaire de recherche avancée](#reference_9AAD4A46B68D4D48865508982CB86DB9).

Voir [Configuration de la saisie semi-automatique CSS](../c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Voir [Copie du code HTML du formulaire de recherche dans le...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

<table> 
 <thead> 
  <tr> 
   <th colname="col2" class="entry"> <p>Emplacement du formulaire </p> </th> 
   <th colname="col1" class="entry"> <p>Paramètre </p> </th> 
   <th colname="col3" class="entry"> <p>Code HTML </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col2"> <p>Activer les options de formulaire de recherche avancée (champ masqué) </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_advanced  </span> </p> </td> 
   <td colname="col3"> <p> <span class="syntax html codeph"> &lt;input type="hidden" name="sp_advanced" value="1"&gt; </span> </p> </td> 
   <td colname="col4"> <p>Active ou désactive les options de recherche avancée. Par exemple, vous pouvez placer un formulaire de recherche standard sur votre page d'accueil avec un lien vers une deuxième page contenant un formulaire avancé. Dans ce cas, vous devez placer une copie de votre formulaire standard dans <span class="codeph"> &lt;search-if-not-advanced&gt;...&lt;/search-if-not-advanced&gt; </span> balises de modèle. </p> <p>Un client qui effectue une recherche à partir du formulaire standard voit un formulaire de recherche standard lorsque les résultats de la recherche sont affichés. Dans l’écran du formulaire de recherche avancée, vous ajoutez la balise <span class="codeph"> &lt;input type=hidden name="sp_advanced" value=1&gt; </span> aux autres options de formulaire avancées. </p> <p>Vous incluez également une copie du formulaire de recherche avancée dans les balises de modèle &lt;search-if-advanced&gt;... &lt;/search-if-advanced&gt;. Un client qui effectue une recherche à partir de votre formulaire de recherche avancée voit apparaître un formulaire de recherche avancée lorsque les résultats de la recherche sont affichés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> Faire correspondre n’importe quelle expression, tout ou phrase </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_p  </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Allow&nbsp;"any,"&nbsp;"all,"&nbsp;or&nbsp;"phrase"&nbsp;--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_p"&nbsp;value="any"&gt;Any&nbsp;word 
      &lt;input&nbsp;type=radio&nbsp;name="sp_p"&nbsp;value="all"&nbsp;checked&gt;All&nbsp;words 
      &lt;input&nbsp;type=radio&nbsp;name="sp_p"&nbsp;value="phrase"&gt;Exact&nbsp;phrase </code> </p> </td> 
   <td colname="col4"> <p>Permet à votre client de spécifier que "n’importe quel mot", "tous les mots" ou "l’expression exacte" doit être présent pour qu’un document corresponde. Lorsque le paramètre <span class="codeph"> sp_p </span> est spécifié, les clients n'ont pas besoin d'utiliser "+" ou "-", ou les deux dans la requête de recherche. </p> <p> Si le paramètre <span class="codeph"> sp_p </span> est omis ou s'il est défini sur "" ou "any", les clients peuvent toujours utiliser les spécificateurs "+" et "-". Si le paramètre <span class="codeph"> sp_p </span> est défini sur "all" ou "phrase", les valeurs "+" et "-" spécifiées sont ignorées. </p> <p>Vous pouvez en savoir plus sur l’utilisation de "+" et "-" dans une recherche. </p> <p>Voir <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">A propos des recherches </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> Correspondance sonore </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_w  </span> </p> <p>et </p> <p> <span class="codeph"> sp_w_control  </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Checkbox&nbsp;enables&nbsp;sound-alike&nbsp;matching&nbsp;--&gt; 
      &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value=1&gt; 
      &lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;&nbsp;Sound-alike&nbsp;matching </code> </p> </td> 
   <td colname="col4"> <p>Permet aux clients d’activer ou de désactiver la mise en correspondance des sons similaires. La correspondance son-sosie permet aux requêtes de recherche mal orthographiées de correspondre à des mots qui "se ressemblent" dans vos documents. </p> <p>Lorsque le paramètre <span class="codeph"> sp_w_control </span> est défini sur 1 et que le paramètre <span class="codeph"> sp_w </span> est défini sur "identique", la case à cocher générée est sélectionnée, ce qui permet la correspondance du son par défaut. </p> <p>Si le paramètre <span class="codeph"> sp_w </span> est défini sur "", la case à cocher n'est pas sélectionnée. </p> <p>Si vous n'avez pas activé la correspondance son/sole lors de votre dernière opération d'indexation, la correspondance son/sole n'est pas possible et le paramètre <span class="codeph"> sp_w </span> est ignoré. Pour activer la correspondance du son, dans le menu du produit, cliquez sur <span class="uicontrol"> Linguistique </span> &gt; <span class="uicontrol"> Mots et langue </span> &gt; <span class="uicontrol"> Correspondance sonore </span>. </p> <p>Vous pouvez également attribuer les paramètres <span class="codeph"> sp_w </span> et <span class="codeph"> sp_w_control </span> de la manière suivante : </p> <p> <code class="syntax html"> &lt;!--&nbsp;Checkbox&nbsp;disables&nbsp;sound-alike&nbsp;matching&nbsp;--&gt; 
      &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value=0&gt; 
      &lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt; 
      No&nbsp;sound-alike&nbsp;matching </code> </p> <p>Dans ce cas, lorsque le paramètre <span class="codeph"> sp_w_control </span> est défini sur 0 et que le paramètre <span class="codeph"> sp_w </span> est défini sur "exact", la correspondance du son identique est désactivée par défaut. Si le paramètre <span class="codeph"> sp_w </span> est défini sur "", la correspondance du son est activée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Correspondance de plage de dates </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_d  </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--Specifies&nbsp;type&nbsp;of&nbsp;date&nbsp;range&nbsp;searching&nbsp;to&nbsp;perform.--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_d"&nbsp;value="custom"&nbsp;checked&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_d"&nbsp;value="specific"&gt; </code> </p> </td> 
   <td colname="col4"> <p>Le paramètre <span class="codeph"> sp_d </span> spécifie une plage de données personnalisée à exécuter ou une plage de dates spécifique à exécuter. </p> <p>Dans le formulaire de recherche avancée par défaut, cette option est présentée comme un groupe de boutons radio avec une liste déroulante de plages de dates "personnalisées", comme générée avec un paramètre <span class="codeph"> sp_date_range </span>. Il comprend également un groupe de dates de début et de fin "spécifiques" qui sont générées avec <span class="codeph"> sp_début_day </span>, <span class="codeph"> sp_début_month </span>, <span class="codeph"> sp_début_year </span>, <span class="codeph"> sp_end_day </span>, <span class="codeph"> sp_end_month &lt;a9/ et <span class="codeph"> sp_end_year </span> paramètres.</span> </p> <p>Une plage de dates "personnalisée" est une plage de dates nommée à rechercher. Par exemple, "En tout temps", "Aujourd'hui", "Au cours de l'année écoulée", etc. </p> <p>Une plage de dates "spécifique" comprend une date de début et une date de fin. Par exemple, de "8 septembre 2009 au 18 octobre 2011". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Correspondance de plage de dates : plage de dates personnalisée </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_date_range  </span> </p> <p> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--Selection&nbsp;list&nbsp;for&nbsp;custom&nbsp;date&nbsp;range.--&gt; 
      &lt;select&nbsp;name="sp_date_range"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=-1&nbsp;selected&gt;Anytime&lt;/option&gt; 
      &lt;option&nbsp;value=7&gt;Within&nbsp;the&nbsp;last&nbsp;week&lt;/option&gt; 
      &lt;option&nbsp;value=14&gt;Within&nbsp;the&nbsp;last&nbsp;2&nbsp;weeks&lt;/option&gt; 
      &lt;option&nbsp;value=30&gt;Within&nbsp;the&nbsp;last&nbsp;30&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=60&gt;Within&nbsp;the&nbsp;last&nbsp;60&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=90&gt;Within&nbsp;the&nbsp;last&nbsp;90&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=180&gt;Within&nbsp;the&nbsp;last&nbsp;180&nbsp;days&lt;/option&gt; 
      &lt;option&nbsp;value=365&gt;Within&nbsp;the&nbsp;last&nbsp;year&lt;/option&gt; 
      &lt;option&nbsp;value=730&gt;Within&nbsp;the&nbsp;last&nbsp;two&nbsp;years&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
   <td colname="col4"> <p>Le paramètre <span class="codeph"> sp_date_range </span> est utilisé pour créer une plage de dates "personnalisée". Par exemple, "En tout temps", "Aujourd'hui", "Au cours de l'année écoulée", etc. </p> <p>Les valeurs supérieures ou égales à zéro spécifient le nombre de jours avant la date d’aujourd’hui pour la recherche. Par exemple, la valeur 0 indique "Aujourd’hui", la valeur 1 indique "Aujourd’hui et Hier", la valeur 30 indique "Au cours des 30 derniers jours", etc. Les valeurs inférieures à zéro définissent une plage personnalisée comme suit : </p> <p> 
     <ul id="ul_E65DDE33883F441F9730F315E485AD98"> 
      <li id="li_83E9466AB9D7438A8544001F6B007186"> <p>-1 = "En tout temps", la même chose que de spécifier aucune plage de dates. </p> </li> 
      <li id="li_38AB8D97179A47F9B860A96EA09119BB"> <p>-2 = "Cette semaine", qui effectue une recherche du dimanche au samedi de la semaine en cours. </p> </li> 
      <li id="li_F4C3A8658428418A8A06FBAAB4733C68"> <p>-3 = "Semaine dernière", qui effectue une recherche du dimanche au samedi de la semaine précédant la semaine en cours. </p> </li> 
      <li id="li_DF2D0B043A4E4DE9BE8D82E69A76E793"> <p>-4 = "Ce mois-ci", qui recherche les dates du mois en cours. </p> </li> 
      <li id="li_76BC4C2CED574E2A81448158828BFF1B"> <p>-5 = "Dernier mois", qui recherche les dates du mois précédant le mois en cours. </p> </li> 
      <li id="li_17FF849384FB46D58AF6FF1D3BC408C8"> <p>-6 = "Cette année", qui recherche les dates de l’année en cours. </p> </li> 
      <li id="li_E2B8B4DFF3914BBDB86D0EB77F52B305"> <p>-7 = "L’année dernière", qui recherche les dates de l’année précédant l’année en cours. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Correspondance de plage de dates : Dates du début </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_début_day, sp_début_month, sp_début_year  </span> </p> <p> </p> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> <p>Ce triplet de valeurs numériques spécifie la date de début d’une plage de dates spécifique à rechercher. Veillez à spécifier les trois valeurs, car une date partiellement spécifiée est ignorée. </p> <p>Il est légal de spécifier uniquement la date de début, la date de fin ou à la fois la date de début et la date de fin. Si seule la date du début est spécifiée, la recherche inclut les documents correspondants datés le ou après la date du début. Si seule la date de fin est spécifiée, la recherche inclut les documents correspondants au plus tard à la date de fin. Si la date de début et la date de fin sont spécifiées, la recherche inclut les documents correspondants entre la date de début et la date de fin. </p> <p>Toutes les dates sont recherchées par rapport à l'heure de Greenwich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p> Correspondance de plage de dates : dates de fin </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_end_day, sp_end_month, sp_end_year  </span> </p> <p> </p> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> <p>Ce triplet de valeurs numériques spécifie la date de fin de la plage de dates spécifique à rechercher. Veillez à spécifier les trois valeurs, car une date partiellement spécifiée est ignorée. </p> <p>Il est légal de spécifier uniquement la date de début, la date de fin ou à la fois le début et la date de fin. Si seule la date du début est spécifiée, la recherche inclut les documents correspondants datés le ou après la date du début. Si seule la date de fin est spécifiée, la recherche inclut les documents correspondants au plus tard à la date de fin. Si le début et la date de fin sont spécifiés, la recherche inclut les documents correspondants entre la date de début et la date de fin. </p> <p>Toutes les dates sont recherchées par rapport à l'heure de Greenwich. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Dans le champ de recherche </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_x  </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;List&nbsp;box&nbsp;selects&nbsp;the&nbsp;search&nbsp;field&nbsp;--&gt; 
      Within&nbsp;&lt;select&nbsp;name="sp_x"&nbsp;size=1&gt; 
      &lt;option&nbsp;value="any"&nbsp;selected&gt;Anywhere&lt;/option&gt; 
      &lt;option&nbsp;value="title"&gt;Title&lt;/option&gt; 
      &lt;option&nbsp;value="desc"&gt;Description&lt;/option&gt; 
      &lt;option&nbsp;value="keys"&gt;Keywords&lt;/option&gt; 
      &lt;option&nbsp;value="body"&gt;Body&lt;/option&gt; 
      &lt;option&nbsp;value="alt"&gt;Alternate&nbsp;text&lt;/option&gt; 
      &lt;option&nbsp;value="url"&gt;URL&lt;/option&gt; 
      &lt;option&nbsp;value="target"&gt;Target&lt;/option&gt; 
      &lt;option&nbsp;value="date"&gt;Date&lt;/option&gt;* 
      &lt;/select&gt; </code> </p> </td> 
   <td colname="col4"> <p>La zone de liste <span class="codeph"> sp_x </span> permet à vos clients de spécifier le champ dans lequel rechercher les chaînes de requête. </p> <p>Les clients peuvent choisir entre tous les champs, le titre, la description du document, les mots-clés du document, le corps, le texte de remplacement, l’URL du document, la date ou les mots-clés de cible. </p> <p>Lorsque le paramètre <span class="codeph"> sp_x </span> est utilisé, les clients n'ont pas besoin de spécifier "title:", "desc:", "keys:", "body:", "alt:", "url:" et "cible:" dans les chaînes de requête de recherche. </p> <p>Si le paramètre <span class="codeph"> sp_x </span> est omis ou s'il est défini sur "" ou "any", les clients peuvent toujours utiliser les chaînes de spécificateur de champ. Si le paramètre <span class="codeph"> sp_x </span> est défini sur un champ spécifique, toutes les autres chaînes de spécificateur de champ sont ignorées. </p> <p>Voir <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">A propos des recherches </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Afficher le nombre de résultats </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_c  </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;List&nbsp;box&nbsp;selects&nbsp;number&nbsp;of&nbsp;results&nbsp;to&nbsp;show&nbsp;per&nbsp;page&nbsp;--&gt; 
      Show&nbsp;&lt;select&nbsp;name="sp_c"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=5&gt;5&lt;/option&gt; 
      &lt;option&nbsp;value=10&nbsp;selected&gt;10&lt;/option&gt; 
      &lt;option&nbsp;value=25&gt;25&lt;/option&gt; 
      &lt;option&nbsp;value=50&gt;50&lt;/option&gt; 
      &lt;option&nbsp;value=100&gt;100&lt;/option&gt; 
      &lt;/select&gt;&nbsp;results </code> </p> </td> 
   <td colname="col4"> <p>Permet aux clients de choisir le nombre de résultats de recherche affichés sur chaque page de résultats de recherche. </p> <p>Vous pouvez avoir autant de choix dans le formulaire que vous le souhaitez. Assurez-vous que la valeur "value=" correspond à la valeur affichée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Afficher ou masquer les résumés </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_m  </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Show&nbsp;or&nbsp;hide&nbsp;summaries&nbsp;in&nbsp;search&nbsp;results&nbsp;--&gt; 
      &lt;select&nbsp;name="sp_m"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=1&nbsp;selected&gt;with&lt;/option&gt; 
      &lt;option&nbsp;value=0&gt;without&lt;/option&gt; 
      &lt;/select&gt;&nbsp;summaries&nbsp; </code> </p> </td> 
   <td colname="col4"> <p>Permet aux clients de choisir si le texte de synthèse s’affiche pour chaque correspondance. </p> <p>Définissez la valeur sur 1 si vous souhaitez afficher des résumés. Définissez la valeur sur 0 si vous souhaitez masquer les résumés. Vous pouvez également utiliser le paramètre avec un ensemble de boutons radio, comme dans l’exemple suivant : </p> <p> <code class="syntax html"> &lt;!--&nbsp;Show&nbsp;or&nbsp;hide&nbsp;summaries&nbsp;in&nbsp;search&nbsp;results&nbsp;--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_m"&nbsp;value=1&nbsp;selected&gt;Show&nbsp;summaries 
      &lt;input&nbsp;type=radio&nbsp;name="sp_m"&nbsp;value=0&gt;Hide&nbsp;summaries </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col2"> <p>Trier par résultats </p> </td> 
   <td colname="col1"> <p> <span class="codeph"> sp_s  </span> </p> </td> 
   <td colname="col3"> <p> <code class="syntax html"> &lt;!--&nbsp;Sort&nbsp;results&nbsp;by&nbsp;relevance&nbsp;or&nbsp;by&nbsp;date&nbsp;--&gt; 
      Sort&nbsp;by&nbsp;&lt;select&nbsp;name="sp_s"&nbsp;size=1&gt; 
      &lt;option&nbsp;value=0&nbsp;selected&gt;relevance&lt;/option&gt; 
      &lt;option&nbsp;value=1&gt;date&lt;/option&gt; 
      &lt;/select&gt; </code> </p> </td> 
   <td colname="col4"> <p>Permet aux clients de choisir si les résultats sont répertoriés par ordre de pertinence ou de date. </p> <p>Lorsque la valeur est définie sur 1, les résultats sont répertoriés du document le plus récemment modifié au document le moins récemment modifié. Lorsque la valeur est définie sur 0, les résultats sont répertoriés du plus pertinent au moins pertinent. Vous pouvez également utiliser ce paramètre avec des boutons radio, comme dans l’exemple suivant : </p> <p> <code class="syntax html"> &lt;!--&nbsp;Sort&nbsp;results&nbsp;by&nbsp;relevance&nbsp;or&nbsp;by&nbsp;date&nbsp;--&gt; 
      &lt;input&nbsp;type=radio&nbsp;name="sp_s"&nbsp;value=0&nbsp;selected&gt;Sort&nbsp;by&nbsp;relevance 
      &lt;input&nbsp;type=radio&nbsp;name="sp_s"&nbsp;value=1&gt;Sort&nbsp;by&nbsp;date </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Code HTML de formulaire de recherche avancée {#reference_9AAD4A46B68D4D48865508982CB86DB9}

Code de formulaire HTML utilisé pour produire le formulaire de recherche avancée qui s’affiche en haut de la rubrique Exemple de formulaire de recherche avancée.

Voir [Exemple de formulaire de recherche avancée](#reference_82E1051918744EBA88A01E9E6AE42C4A).

Si vous utilisez ce code, veillez à remplacer la valeur `sp_a` de `sp99999999` par votre numéro de compte réel.

Pour trouver votre numéro de compte, dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Account Options]** > **[!UICONTROL Account Settings]**.

```
<form method="get" action="https://search.atomz.com/search/"> 
<table cellspacing=0 cellpadding=0 border=0> 
<tr><td colspan=4> 
<b>Search For:</b><br> 
<input size=35 name="sp_q"> 
<!-- The "Search" button --> 
<input type=submit value="Search"> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=hidden name="sp_f" value="ISO-8859-1"> 
</td></tr> 
<input type=hidden name="sp_advanced" value=1> 
<!-- Allow "any," "all," or "phrase" --> 
<tr><td valign=top> 
<b>Match: </b> 
</td><td colspan=4> 
<input type=radio name="sp_p" value="any">Any word 
<input type=radio name="sp_p" value="all" checked>All words 
<input type=radio name="sp_p" value="phrase">Exact phrase<br> 
<!-- Checkbox enables sound-alike matching --> 
<input type=hidden name="sp_w_control" value=1> 
<input type=checkbox name="sp_w" value="alike" checked> 
Sound-alike matching 
</td></tr> 
<!-- Date range criteria --> 
<tr><td><b>Dated:</b></td><td colspan=4> 
<input type=radio name="sp_d" value="custom" checked> 
<select name="sp_date_range" size=1> 
<option value=-1 selected>Anytime</option> 
<option value=7>Within the last week</option> 
<option value=14>Within the last 2 weeks</option> 
<option value=30>Within the last 30 days</option> 
<option value=60>Within the last 60 days</option> 
<option value=90>Within the last 90 days</option> 
<option value=180>Within the last 180 days</option> 
<option value=365>Within the last year</option> 
<option value=730>Within the last two years</option> 
</select> 
</td></tr> 
<tr><td></td><td rowspan=2> 
<input type=radio name="sp_d" value=specific> 
</td><td align=right>From:</td><td> 
<select name="sp_start_month" size=1> 
<option value=0 selected></option> 
<option value=1>January</option> 
<option value=2>February</option> 
<option value=3>March</option> 
<option value=4>April</option> 
<option value=5>May</option> 
<option value=6>June</option> 
<option value=7>July</option> 
<option value=8>August</option> 
<option value=9>September</option> 
<option value=10>October</option> 
<option value=11>November</option> 
<option value=12>December</option> 
</select> 
<select name="sp_start_day" size=1> 
<option value=0 selected></option> 
<option value=1>1</option> 
<option value=2>2</option> 
<option value=3>3</option> 
<option value=4>4</option> 
<option value=5>5</option> 
<option value=6>6</option> 
<option value=7>7</option> 
<option value=8>8</option> 
<option value=9>9</option> 
<option value=10>10</option> 
<option value=11>11</option> 
<option value=12>12</option> 
<option value=13>13</option> 
<option value=14>14</option> 
<option value=15>15</option> 
<option value=16>16</option> 
<option value=17>17</option> 
<option value=18>18</option> 
<option value=19>19</option> 
<option value=20>20</option> 
<option value=21>21</option> 
<option value=22>22</option> 
<option value=23>23</option> 
<option value=24>24</option> 
<option value=25>25</option> 
<option value=26>26</option> 
<option value=27>27</option> 
<option value=28>28</option> 
<option value=29>29</option> 
<option value=30>30</option> 
<option value=31>31</option> 
</select> 
<!--comma-->, 
<input size=4 name="sp_start_year"> 
</td></tr> 
<tr><td></td> 
<td align=right>To:</td><td> 
<select name="sp_end_month" size=1> 
<option value=0 selected></option> 
<option value=1>January</option> 
<option value=2>February</option> 
<option value=3>March</option> 
<option value=4>April</option> 
<option value=5>May</option> 
<option value=6>June</option> 
<option value=7>July</option> 
<option value=8>August</option> 
<option value=9>September</option> 
<option value=10>October</option> 
<option value=11>November</option> 
<option value=12>December</option> 
</select> 
<select name="sp_end_day" size=1> 
<option value=0 selected></option> 
<option value=1>1</option> 
<option value=2>2</option> 
<option value=3>3</option> 
<option value=4>4</option> 
<option value=5>5</option> 
<option value=6>6</option> 
<option value=7>7</option> 
<option value=8>8</option> 
<option value=9>9</option> 
<option value=10>10</option> 
<option value=11>11</option> 
<option value=12>12</option> 
<option value=13>13</option> 
<option value=14>14</option> 
<option value=15>15</option> 
<option value=16>16</option> 
<option value=17>17</option> 
<option value=18>18</option> 
<option value=19>19</option> 
<option value=20>20</option> 
<option value=21>21</option> 
<option value=22>22</option> 
<option value=23>23</option> 
<option value=24>24</option> 
<option value=25>25</option> 
<option value=26>26</option> 
<option value=27>27</option> 
<option value=28>28</option> 
<option value=29>29</option> 
<option value=30>30</option> 
<option value=31>31</option> 
</select> 
<!--comma-->, 
<input size=4 name="sp_end_year"> 
</td></tr> 
<!-- List box selects the search field --> 
<tr><td valign=top> 
<b>Within: </b> 
</td><td colspan=4><select name="sp_x" size=1> 
<option value="any" selected>Anywhere</option> 
<option value="title">Title</option> 
<option value="desc">Description</option> 
<option value="keys">Keywords</option> 
<option value="body">Body</option> 
<option value="alt">Alternate text</option> 
<option value="url">URL</option> 
<option value="target">Target</option> 
</select> 
</td></tr> 
<!-- List box selects number of results to show per page --> 
<tr><td valign=top> 
<b>Show: </b> 
</td><td colspan=4><select name="sp_c" size=1> 
<option value=5>5</option> 
<option value=10 selected>10</option> 
<option value=25>25</option> 
<option value=50>50</option> 
<option value=100>100</option> 
</select> results  
<!-- Show or hide summaries in search results --> 
<select name="sp_m" size=1> 
<option value=1 selected>with</option> 
<option value=0>without</option> 
</select> summaries<br> 
</td></tr> 
<!-- Sort results by relevance or by date --> 
<tr><td valign=top> 
<b>Sort by: </b> 
</td><td colspan=4><select name="sp_s" size=1> 
<option value=0 selected>relevance</option> 
<option value=1>date</option> 
</select> 
</td></tr> 
</table> 
</form>
```

## Code de modèle de formulaire de recherche avancée {#reference_D762C22E754E462DBEECD88D2C3FA579}

Vous pouvez ajouter le code HTML de formulaire de recherche avancée à votre modèle de telle sorte que le choix par défaut de tout paramètre soit le même que celui de la recherche précédente.

En d’autres termes, si un client clique sur le bouton radio **[!UICONTROL Exact phrase]**, vous pouvez vous assurer que le bouton radio est sélectionné par défaut lorsque les résultats de la recherche sont affichés.

Pour ce faire, supprimez tous les spécificateurs &quot;cochés&quot; ou &quot;sélectionnés&quot; des balises HTML standard, puis remplacez les balises HTML suivantes :

* `<input>`
* `<select>`
* `<option>`
* `</option>`
* `</select>`

avec les balises de modèle correspondantes suivantes :

* `<search-input>`
* `<search-select>`
* `<search-option>`
* `</search-option>`
* `</search-select>`

Pour ce faire, vous utilisez le code suivant comme balise `<form>` sur votre modèle de recherche.

```
<!-- Adobe Target results section.--> 
 
<!-- Show heading and logo graphic. --> 
<SEARCH-IF-RESULTS> 
<b>SEARCH RESULTS <SEARCH-LOWER> - <SEARCH-UPPER></b> 
of <SEARCH-TOTAL> total results for <b><SEARCH-QUERY></b><br> 
</SEARCH-IF-RESULTS> 
<SEARCH-IF-NOT-RESULTS> 
<b>SEARCH RESULTS</b> for <b><SEARCH-QUERY></b><br> 
</SEARCH-IF-NOT-RESULTS> 
<SEARCH-LOGO><br> 
 
<!-- Display Results. --> 
<SEARCH-RESULTS LENGTH=160> 
<p><b><SEARCH-LINK><SEARCH-TITLE LENGTH=160></SEARCH-LINK></b><br> 
<SEARCH-IF-SHOW-SUMMARIES> 
<SEARCH-IF-CONTEXT LENGTH=240><SEARCH-CONTEXT><br></SEARCH-IF-CONTEXT> 
<font size="-1"><SEARCH-URL LENGTH=60></font><br> 
</SEARCH-IF-SHOW-SUMMARIES> 
</SEARCH-RESULTS> 
 
<!-- If no results, show a message. --> 
<SEARCH-IF-NOT-RESULTS><p> 
Sorry, no matches were found containing <b><SEARCH-QUERY>.</b> 
</SEARCH-IF-NOT-RESULTS> 
<!-- Show By Relevance, By Date links, Show/Hide Summaries links. --> 
<SEARCH-IF-RESULTS><p> 
<SEARCH-IF-SORT-BY-DATE> 
<b><SEARCH-SORT-BY-SCORE COUNT=10>Sort By Relevance</SEARCH-SORT-BY-SCORE></b> 
</SEARCH-IF-SORT-BY-DATE> 
<SEARCH-IF-SORT-BY-SCORE> 
<b><SEARCH-SORT-BY-DATE COUNT=10>Sort By Date</SEARCH-SORT-BY-DATE></b> 
</SEARCH-IF-SORT-BY-SCORE> 
| <b> 
<SEARCH-IF-SHOW-SUMMARIES> 
<SEARCH-HIDE-SUMMARIES COUNT=20>Hide Summaries</SEARCH-HIDE-SUMMARIES> 
</SEARCH-IF-SHOW-SUMMARIES> 
<SEARCH-IF-HIDE-SUMMARIES> 
<SEARCH-SHOW-SUMMARIES COUNT=10>Show Summaries</SEARCH-SHOW-SUMMARIES> 
</SEARCH-IF-HIDE-SUMMARIES> 
</b><br> 
</SEARCH-IF-RESULTS> 
 
<!-- Display Prev & Next links. --> 
<SEARCH-IF-RESULTS> 
<SEARCH-IF-PREV-COUNT> 
<b><SEARCH-PREV>Prev <SEARCH-PREV-COUNT></SEARCH-PREV></b> 
<SEARCH-IF-NEXT-COUNT> | </SEARCH-IF-NEXT-COUNT> 
</SEARCH-IF-PREV-COUNT> 
<SEARCH-IF-NEXT-COUNT> 
<b><SEARCH-NEXT>Next <SEARCH-NEXT-COUNT></SEARCH-NEXT></b><br> 
</SEARCH-IF-NEXT-COUNT><p> 
</SEARCH-IF-RESULTS> 
 
<!-- Put up the next form. --> 
<form method="get" action="https://search.atomz.com/search/"> 
<SEARCH-IF-NOT-ADVANCED> 
<SEARCH-INPUT-ACCOUNT> 
<SEARCH-INPUT-GALLERY> 
<SEARCH-INPUT-QUERY SIZE=25> 
<SEARCH-INPUT type=hidden name=sp_p> 
<input type=submit value="New Search"> 
<SEARCH-IF-INPUT-COLLECTIONS> 
<br><SEARCH-INPUT-COLLECTIONS> 
</SEARCH-IF-INPUT-COLLECTIONS> 
</SEARCH-IF-NOT-ADVANCED> 
<SEARCH-IF-ADVANCED> 
<table cellspacing=0 cellpadding=0 border=0> 
<tr><td colspan=4> 
<b>Search For:</b><br> 
<SEARCH-INPUT-QUERY SIZE=35> 
 
<!-- The "Search" button --> 
<input type=submit value="New Search"> 
<SEARCH-INPUT-ACCOUNT> 
<SEARCH-INPUT-GALLERY> 
</td></tr> 
<SEARCH-IF-INPUT-COLLECTIONS> 
<!-- Collections --> 
<tr><td> 
<b>In: </b> 
</td><td colspan=4> 
<SEARCH-INPUT-COLLECTIONS> 
</td></tr> 
</SEARCH-IF-INPUT-COLLECTIONS> 
<input type=hidden name="sp_advanced" value=1> 
 
<!-- Allow "any," "all," or "phrase" --> 
<tr><td valign=top> 
<b>Match: </b> 
</td><td colspan=4> 
<SEARCH-INPUT type=radio name="sp_p" value="any">Any word 
<SEARCH-INPUT type=radio name="sp_p" value="all">All words 
<SEARCH-INPUT type=radio name="sp_p" value="phrase">Exact phrase<br> 
<!-- Checkbox enables sound-alike matching --> 
<input type=hidden name="sp_w_control" value=1> 
<SEARCH-INPUT type=checkbox name="sp_w" value="alike">Sound-alike matching 
</td></tr> 
 
<!-- Date range section --> 
<tr> 
<td><b>Dated:</b></td> 
<td colspan=3> 
<SEARCH-INPUT type=radio name="sp_d" value="custom"> 
<SEARCH-SELECT name="sp_date_range" size=1> 
<SEARCH-OPTION value=-1>Anytime</SEARCH-OPTION> 
<SEARCH-OPTION value=7>Within the last week</SEARCH-OPTION> 
<SEARCH-OPTION value=14>Within the last 2 weeks</SEARCH-OPTION> 
<SEARCH-OPTION value=30>Within the last 30 days</SEARCH-OPTION> 
<SEARCH-OPTION value=60>Within the last 60 days</SEARCH-OPTION> 
<SEARCH-OPTION value=90>Within the last 90 days</SEARCH-OPTION> 
<SEARCH-OPTION value=180>Within the last 180 days</SEARCH-OPTION> 
<SEARCH-OPTION value=365>Within the last year</SEARCH-OPTION> 
<SEARCH-OPTION value=730>Within the last two years</SEARCH-OPTION> 
</SEARCH-SELECT> 
</td></tr> 
<tr><td></td><td rowspan=2> 
<SEARCH-INPUT type=radio name="sp_d" value=specific></td> 
<td align=right>From:</td><td> 
<SEARCH-SELECT name="sp_start_month" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>January</SEARCH-OPTION> 
<SEARCH-OPTION value=2>February</SEARCH-OPTION> 
<SEARCH-OPTION value=3>March</SEARCH-OPTION> 
<SEARCH-OPTION value=4>April</SEARCH-OPTION> 
<SEARCH-OPTION value=5>May</SEARCH-OPTION> 
<SEARCH-OPTION value=6>June</SEARCH-OPTION> 
<SEARCH-OPTION value=7>July</SEARCH-OPTION> 
<SEARCH-OPTION value=8>August</SEARCH-OPTION> 
<SEARCH-OPTION value=9>September</SEARCH-OPTION> 
<SEARCH-OPTION value=10>October</SEARCH-OPTION> 
<SEARCH-OPTION value=11>November</SEARCH-OPTION> 
<SEARCH-OPTION value=12>December</SEARCH-OPTION> 
</SEARCH-SELECT> 
<SEARCH-SELECT name="sp_start_day" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>1</SEARCH-OPTION> 
<SEARCH-OPTION value=2>2</SEARCH-OPTION> 
<SEARCH-OPTION value=3>3</SEARCH-OPTION> 
<SEARCH-OPTION value=4>4</SEARCH-OPTION> 
<SEARCH-OPTION value=5>5</SEARCH-OPTION> 
<SEARCH-OPTION value=6>6</SEARCH-OPTION> 
<SEARCH-OPTION value=7>7</SEARCH-OPTION> 
<SEARCH-OPTION value=8>8</SEARCH-OPTION> 
<SEARCH-OPTION value=9>9</SEARCH-OPTION> 
<SEARCH-OPTION value=10>10</SEARCH-OPTION> 
<SEARCH-OPTION value=11>11</SEARCH-OPTION> 
<SEARCH-OPTION value=12>12</SEARCH-OPTION> 
<SEARCH-OPTION value=13>13</SEARCH-OPTION> 
<SEARCH-OPTION value=14>14</SEARCH-OPTION> 
<SEARCH-OPTION value=15>15</SEARCH-OPTION> 
<SEARCH-OPTION value=16>16</SEARCH-OPTION> 
<SEARCH-OPTION value=17>17</SEARCH-OPTION> 
<SEARCH-OPTION value=18>18</SEARCH-OPTION> 
<SEARCH-OPTION value=19>19</SEARCH-OPTION> 
<SEARCH-OPTION value=20>20</SEARCH-OPTION> 
<SEARCH-OPTION value=21>21</SEARCH-OPTION> 
<SEARCH-OPTION value=22>22</SEARCH-OPTION> 
<SEARCH-OPTION value=23>23</SEARCH-OPTION> 
<SEARCH-OPTION value=24>24</SEARCH-OPTION> 
<SEARCH-OPTION value=25>25</SEARCH-OPTION> 
<SEARCH-OPTION value=26>26</SEARCH-OPTION> 
<SEARCH-OPTION value=27>27</SEARCH-OPTION> 
<SEARCH-OPTION value=28>28</SEARCH-OPTION> 
<SEARCH-OPTION value=29>29</SEARCH-OPTION> 
<SEARCH-OPTION value=30>30</SEARCH-OPTION> 
<SEARCH-OPTION value=31>31</SEARCH-OPTION> 
</SEARCH-SELECT><!--comma-->, 
<SEARCH-INPUT size=4 name="sp_start_year"> 
</td></tr> 
<tr><td></td> 
<td align=right>To:</td><td> 
<SEARCH-SELECT name="sp_end_month" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>January</SEARCH-OPTION> 
<SEARCH-OPTION value=2>February</SEARCH-OPTION> 
<SEARCH-OPTION value=3>March</SEARCH-OPTION> 
<SEARCH-OPTION value=4>April</SEARCH-OPTION> 
<SEARCH-OPTION value=5>May</SEARCH-OPTION> 
<SEARCH-OPTION value=6>June</SEARCH-OPTION> 
<SEARCH-OPTION value=7>July</SEARCH-OPTION> 
<SEARCH-OPTION value=8>August</SEARCH-OPTION> 
<SEARCH-OPTION value=9>September</SEARCH-OPTION> 
<SEARCH-OPTION value=10>October</SEARCH-OPTION> 
<SEARCH-OPTION value=11>November</SEARCH-OPTION> 
<SEARCH-OPTION value=12>December</SEARCH-OPTION> 
</SEARCH-SELECT> 
<SEARCH-SELECT name="sp_end_day" size=1> 
<SEARCH-OPTION value=0></SEARCH-OPTION> 
<SEARCH-OPTION value=1>1</SEARCH-OPTION> 
<SEARCH-OPTION value=2>2</SEARCH-OPTION> 
<SEARCH-OPTION value=3>3</SEARCH-OPTION> 
<SEARCH-OPTION value=4>4</SEARCH-OPTION> 
<SEARCH-OPTION value=5>5</SEARCH-OPTION> 
<SEARCH-OPTION value=6>6</SEARCH-OPTION> 
<SEARCH-OPTION value=7>7</SEARCH-OPTION> 
<SEARCH-OPTION value=8>8</SEARCH-OPTION> 
<SEARCH-OPTION value=9>9</SEARCH-OPTION> 
<SEARCH-OPTION value=10>10</SEARCH-OPTION> 
<SEARCH-OPTION value=11>11</SEARCH-OPTION> 
<SEARCH-OPTION value=12>12</SEARCH-OPTION> 
<SEARCH-OPTION value=13>13</SEARCH-OPTION> 
<SEARCH-OPTION value=14>14</SEARCH-OPTION> 
<SEARCH-OPTION value=15>15</SEARCH-OPTION> 
<SEARCH-OPTION value=16>16</SEARCH-OPTION> 
<SEARCH-OPTION value=17>17</SEARCH-OPTION> 
<SEARCH-OPTION value=18>18</SEARCH-OPTION> 
<SEARCH-OPTION value=19>19</SEARCH-OPTION> 
<SEARCH-OPTION value=20>20</SEARCH-OPTION> 
<SEARCH-OPTION value=21>21</SEARCH-OPTION> 
<SEARCH-OPTION value=22>22</SEARCH-OPTION> 
<SEARCH-OPTION value=23>23</SEARCH-OPTION> 
<SEARCH-OPTION value=24>24</SEARCH-OPTION> 
<SEARCH-OPTION value=25>25</SEARCH-OPTION> 
<SEARCH-OPTION value=26>26</SEARCH-OPTION> 
<SEARCH-OPTION value=27>27</SEARCH-OPTION> 
<SEARCH-OPTION value=28>28</SEARCH-OPTION> 
<SEARCH-OPTION value=29>29</SEARCH-OPTION> 
<SEARCH-OPTION value=30>30</SEARCH-OPTION> 
<SEARCH-OPTION value=31>31</SEARCH-OPTION> 
</SEARCH-SELECT><!--comma-->, 
<SEARCH-INPUT size=4 name="sp_end_year"> 
</td></tr> 
<!-- List box selects the search field --> 
<tr><td valign=top> 
<b>Within: </b> 
</td><td colspan=4><SEARCH-SELECT name="sp_x" size=1> 
<SEARCH-OPTION value="any">Anywhere</SEARCH-OPTION> 
<SEARCH-OPTION value="title">Title</SEARCH-OPTION> 
<SEARCH-OPTION value="desc">Description</SEARCH-OPTION> 
<SEARCH-OPTION value="keys">Keywords</SEARCH-OPTION> 
<SEARCH-OPTION value="body">Body</SEARCH-OPTION> 
<SEARCH-OPTION value="alt">Alternate text</SEARCH-OPTION> 
<SEARCH-OPTION value="url">URL</SEARCH-OPTION> 
<SEARCH-OPTION value="target">Target</SEARCH-OPTION> 
</SEARCH-SELECT></td></tr> 
<!-- List box selects number of results to show per page --> 
<tr><td valign=top> 
<b>Show:</b> 
</td><td colspan=4><SEARCH-SELECT name="sp_c" size=1> 
<SEARCH-OPTION value=5>5</SEARCH-OPTION> 
<SEARCH-OPTION value=10>10</SEARCH-OPTION> 
<SEARCH-OPTION value=25>25</SEARCH-OPTION> 
<SEARCH-OPTION value=50>50</SEARCH-OPTION> 
<SEARCH-OPTION value=100>100</SEARCH-OPTION> 
</SEARCH-SELECT> results  
<!-- Show or hide summaries in search results --> 
<SEARCH-SELECT name="sp_m" size=1> 
<SEARCH-OPTION value=1>with</SEARCH-OPTION> 
<SEARCH-OPTION value=0>without</SEARCH-OPTION> 
</SEARCH-SELECT> summaries<br></td></tr> 
<!-- Sort results by relevance or by date --> 
<tr><td valign=top> 
<b>Sort by: </b> 
</td><td colspan=4><SEARCH-SELECT name="sp_s" size=1> 
<SEARCH-OPTION value=0>relevance</SEARCH-OPTION> 
<SEARCH-OPTION value=1>date</SEARCH-OPTION> 
</SEARCH-SELECT></td></tr> 
</table> 
</SEARCH-IF-ADVANCED> 
</form>
```
