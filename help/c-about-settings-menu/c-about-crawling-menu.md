---
description: Utilisez le menu déroulant pour définir des masques de date et d’URL, des mots de passe, des types de contenu, des connexions, des définitions de formulaire et des points d’entrée d’URL.
seo-description: Utilisez le menu déroulant pour définir des masques de date et d’URL, des mots de passe, des types de contenu, des connexions, des définitions de formulaire et des points d’entrée d’URL.
seo-title: A propos du menu Flux
solution: Target
subtopic: Crawling
title: A propos du menu Flux
topic: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
translation-type: tm+mt
source-git-commit: 77a4e88c7bf47b637030e3935a39dfdf4f175e80

---


# A propos du menu Flux{#about-the-crawling-menu}

Utilisez le menu déroulant pour définir des masques de date et d’URL, des mots de passe, des types de contenu, des connexions, des définitions de formulaire et des points d’entrée d’URL.

## A propos des points de fin d’URL {#concept_5D857E3B5C124E85BC0B5AE77A509573}

La plupart des sites Web comportent un point d’entrée principal ou une page d’accueil qu’un client consulte initialement. Ce point d&#39;entrée principal est l&#39;adresse URL à partir de laquelle le robot de recherche commence l&#39;analyse de l&#39;index. Toutefois, si votre site Web comporte plusieurs domaines ou sous-domaines ou si des parties de votre site ne sont pas liées à partir du point d’entrée principal, vous pouvez utiliser des points de entrées d’URL pour ajouter d’autres points d’entrée.

Toutes les pages du site Web situées en dessous de chaque point d’entrée d’URL spécifié sont indexées. Vous pouvez combiner des points d’entrée d’URL et des masques pour contrôler exactement les parties d’un site Web que vous souhaitez indexer. Vous devez recréer l’index de votre site Web avant que les effets des paramètres de points de fin d’URL ne soient visibles par les clients.

Le point d’entrée principal est généralement l’URL du site Web que vous souhaitez indexer et rechercher. Vous configurez ce point d’entrée principal dans Paramètres du compte.

Voir [Configuration des paramètres](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)de votre compte.

Après avoir spécifié le point d’entrée de l’URL principale, vous pouvez éventuellement spécifier d’autres points d’entrée que vous souhaitez analyser dans l’ordre. La plupart du temps, vous spécifiez des points d’entrée supplémentaires pour les pages Web qui ne sont pas liées à partir des pages situées sous le point d’entrée principal. Spécifiez des points d’entrée supplémentaires lorsque votre site Web s’étend sur plusieurs domaines, comme dans l’exemple suivant :

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

Vous pouvez qualifier chaque point d’entrée avec un ou plusieurs des mots-clés séparés par des espaces dans le tableau ci-dessous. Ces mots-clés affectent la manière dont la page est indexée.

**Important**: Veillez à séparer un mot-clé donné du point d&#39;entrée et de l&#39;autre par un espace ; une virgule n’est pas un séparateur valide.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mot-clé </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Si vous ne souhaitez pas indexer le texte sur la page du point d’entrée, mais que vous souhaitez suivre les liens de la page, ajoutez 
     <userinput>
       noindex 
     </userinput> après le point d’entrée. </p> <p>Séparez le mot-clé du point d’entrée par un espace, comme dans l’exemple suivant : </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>Ce mot-clé est équivalent à une balise meta robots avec 
     <userinput>
       content="noindex" 
     </userinput>) entre les 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> balises de la page du point d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Si vous souhaitez indexer le texte dans la page du point d’entrée mais que vous ne souhaitez pas suivre les liens de la page, ajoutez 
     <userinput>
       nofollow 
     </userinput> après le point d’entrée. </p> <p>Séparez le mot-clé du point d’entrée par un espace, comme dans l’exemple suivant : </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>Ce mot-clé est équivalent à une balise meta robots avec 
     <userinput>
       content="nofollow" 
     </userinput> entre les 
     <userinput>
       &lt;head&gt; 
     </userinput>... 
     <userinput>
       &lt;/head&gt; 
     </userinput> d’une page de point d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formulaire </p> </td> 
   <td colname="col2"> <p> Lorsque le point d’entrée est une page de connexion, 
     <userinput>
       formulaire 
     </userinput> est généralement utilisée de sorte que le robot de recherche puisse envoyer le formulaire de connexion et recevoir les cookies appropriés avant d’analyser le site Web. Lorsque le mot-clé "formulaire" est utilisé, la page du point d’entrée n’est pas indexée et le robot de recherche ne marque pas la page du point d’entrée comme étant analysée. Utilisez les  
     <userinput>
       nofollow 
     </userinput> si vous ne souhaitez pas que le robot de recherche suive les liens de la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [A propos des types](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07)de contenu.

Voir aussi [A propos du connecteur](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)d’index.

## Ajout de plusieurs points d’entrée d’URL à indexer {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Si votre site Web comporte plusieurs domaines ou sous-domaines et que vous souhaitez qu’ils soient analysés, vous pouvez utiliser des points de saisie d’URL pour ajouter d’autres URL.

Pour définir le point d’entrée de l’URL principale de votre site Web, utilisez Paramètres du compte.

Voir [Configuration des paramètres](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)de votre compte.

**Pour ajouter plusieurs points d’entrée d’URL à indexer**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**.
1. Sur la [!DNL URL Entrypoints] page, dans le [!DNL Entrypoints] champ, saisissez une adresse URL par ligne.
1. (Facultatif) Dans la liste **[!UICONTROL Add Index Connector Configurations]** déroulante, sélectionnez un connecteur d’index à ajouter comme point d’entrée pour l’indexation.

   La liste déroulante n’est disponible que si vous avez déjà ajouté une ou plusieurs définitions de connecteur d’index.

   ![](assets/url_entrypoints_index_connector.png)

   Voir [Ajout d’une définition](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)de connecteur d’index.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des masques d’URL {#concept_8039DFC53FF3410AA494D602F71BA164}

Les masques URL sont des modèles qui déterminent quels documents de votre site Web les robots de recherche indexes ou non.

Veillez à recréer l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

Vous pouvez utiliser les deux types de masques d’URL suivants :

* Inclure les masques d’URL
* Exclure les masques d’URL

Insérez des masques d’URL pour indiquer au robot de recherche d’indexer tous les documents qui correspondent au modèle du masque.

Exclure les masques d’URL pour indiquer au robot de recherche d’indexer les documents correspondants.

Lorsque le robot de recherche voyage d’un lien à un autre à travers votre site Web, il rencontre des URL et recherche des masques qui correspondent à ces URL. La première correspondance détermine s’il faut inclure ou exclure cette URL de l’index. Si aucun masque ne correspond à une URL rencontrée, cette URL est ignorée de l’index.

Les masques d’URL inclus pour vos URL de point d’entrée sont générés automatiquement. Ce comportement garantit que tous les documents rencontrés sur votre site Web sont indexés. Il supprime aussi commodément les liens qui &quot;quittent&quot; votre site Web. Par exemple, si une page indexée renvoie à https://www.yahoo.com, le robot de recherche n’indexe pas cette URL, car elle ne correspond pas au masque d’inclusion généré automatiquement par l’URL du point d’entrée.

Chaque masque d’URL que vous spécifiez doit se trouver sur une ligne distincte.

Le masque peut spécifier l’une des valeurs suivantes :

* Un chemin complet comme dans `https://www.mydomain.com/products.html`.
* Chemin partiel comme dans `https://www.mydomain.com/products`.
* URL qui utilise des caractères génériques comme dans `https://www.mydomain.com/*.html`.
* Expression régulière (pour les utilisateurs avancés).

   Pour transformer un masque en expression régulière, insérez le mot-clé `regexp` entre le type de masque ( `exclude` ou `include`) et le masque d’URL.

Voici un exemple simple de masque d’URL d’exclusion :

```
exclude https://www.mydomain.com/photos
```

Comme il s’agit d’un masque d’URL d’exclusion, aucun document correspondant au modèle n’est indexé. Le modèle correspond à tout élément rencontré, à la fois aux fichiers et aux dossiers, de sorte que `https://www.mydomain.com/photos.html` et `https://www.mydomain.com/photos/index.html`, qui correspondent tous deux à l’URL d’exclusion, ne sont pas indexés. Pour ne correspondre qu’aux fichiers du `/photos/` dossier, le masque d’URL doit contenir une barre oblique comme dans l’exemple suivant :

```
exclude https://www.mydomain.com/photos/
```

L’exemple de masque d’exclusion suivant utilise un caractère générique. Il indique au robot de recherche de ne pas regarder les fichiers avec l&#39;extension &quot;.pdf&quot;. Le robot de recherche n’ajoute pas ces fichiers à votre index.

```
exclude *.pdf
```

Un simple masque d’URL d’inclusion est le suivant :

```
include https://www.mydomain.com/news/
```

Seuls les documents liés au moyen d’une série de liens à partir d’un point d’entrée d’URL ou utilisés comme point d’entrée d’URL sont indexés. La seule inscription de l’URL d’un document en tant que masque d’URL d’inclusion n’indexe pas un document non lié. Pour ajouter des documents non liés à votre index, vous pouvez utiliser la fonction Points de saisie d’URL.

Voir [A propos des points](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)d’entrée d’URL.

Les masques d’inclusion et d’exclusion peuvent fonctionner ensemble. Vous pouvez exclure une grande partie de votre site Web de l’indexation en créant un masque d’URL d’exclusion tout en incluant une ou plusieurs de ces pages exclues avec un masque d’URL d’inclusion. Supposons, par exemple, que votre URL de point d’entrée soit la suivante :

```
https://www.mydomain.com/photos/
```

Le robot de recherche analyse et indexe toutes les pages sous `/photos/summer/`, `/photos/spring/` et `/photos/fall/` (en supposant qu’il existe des liens vers au moins une page dans chaque répertoire à partir du `photos` dossier). Ce comportement se produit car les chemins d’accès aux liens permettent au robot de recherche de trouver les documents dans les dossiers `/summer/`, `/spring/`et `/fall/`, et les URL des dossiers correspondent au masque d’inclusion généré automatiquement par l’URL du point d’entrée.

Vous pouvez choisir d’exclure toutes les pages du `/fall/` dossier avec un masque d’URL d’exclusion, comme dans l’exemple suivant :

```
exclude https://www.mydomain.com/photos/fall/
```

Vous pouvez également inclure uniquement `/photos/fall/redleaves4.html` dans l’index avec le masque d’URL suivant :

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Pour que les deux exemples de masque ci-dessus fonctionnent comme prévu, le masque d’inclusion est répertorié en premier, comme dans l’exemple suivant :

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

Comme le robot de recherche suit les instructions dans l’ordre dans lequel elles sont répertoriées, il inclut d’abord `/photos/fall/redleaves4.html`, puis exclut le reste des fichiers du `/fall` dossier.

Si les instructions sont spécifiées de la manière opposée, comme dans l’exemple suivant :

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

N’ `/photos/fall/redleaves4.html` est alors pas inclus, même si le masque indique qu’il est inclus.

Un masque d’URL qui s’affiche en premier prévaut toujours sur un masque d’URL qui s’affiche ultérieurement dans les paramètres du masque. De plus, si le robot de recherche rencontre une page qui correspond à un masque d’URL d’inclusion et un masque d’URL d’exclusion, le masque répertorié en premier est toujours prioritaire.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

## A propos de l&#39;utilisation de mots-clés avec des masques d&#39;URL {#section_7609A7A6D79B482ABCA8900886541AAB}

Vous pouvez qualifier chaque masque d’inclusion avec un ou plusieurs mots-clés séparés par des espaces, ce qui affecte la manière dont les pages mises en correspondance sont indexées.

Une virgule n&#39;est pas valide comme séparateur entre le masque et le mot-clé ; vous ne pouvez utiliser que des espaces.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mot-clé </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Si vous ne souhaitez pas indexer le texte sur les pages qui correspondent au masque d’URL, mais que vous souhaitez suivre les liens de pages correspondants, ajoutez 
     <userinput>
       noindex 
     </userinput> après le masque d’URL d’inclusion. Veillez à séparer le mot-clé du masque avec un espace, comme dans l’exemple suivant : </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>L’exemple ci-dessus indique que le robot de recherche suit tous les liens des fichiers avec la variable 
     <userinput>
       .swf 
     </userinput> , mais désactive l’indexation de tout le texte contenu dans ces fichiers. </p> <p>L’ 
     <userinput>
       noindex 
     </userinput> est l’équivalent d’une balise meta de robot avec 
     <userinput>
       content="noindex" 
     </userinput> entre les 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> balises des pages correspondantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Si vous souhaitez indexer le texte sur les pages qui correspondent au masque d’URL, mais que vous ne souhaitez pas suivre les liens de la page correspondante, ajoutez 
     <userinput>
       nofollow 
     </userinput> après le masque d’URL d’inclusion. Veillez à séparer le mot-clé du masque avec un espace, comme dans l’exemple suivant : </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>L’ 
     <userinput>
       nofollow 
     </userinput> est l’équivalent d’une balise meta de robot avec 
     <userinput>
       content="nofollow" 
     </userinput> entre les 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> balises des pages correspondantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>Utilisé pour inclure et exclure des masques. </p> <p>Tout masque d’URL précédé de 
     <userinput>
       regexp 
     </userinput> est traitée comme une expression régulière. Si le robot de recherche rencontre des documents qui correspondent à un masque d’URL d’expression régulière exclus, ces documents ne sont pas indexés. Si le robot de recherche rencontre des documents qui correspondent à un masque d’URL d’expression régulière inclus, ces documents sont indexés. Supposons, par exemple, que vous ayez le masque d’URL suivant : </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>Le robot de recherche exclut les fichiers correspondants, tels que 
     <userinput>
       https://www.mydomain.com/products/page1.html 
     </userinput> </p> <p>Si vous aviez le masque d’URL d’expression régulière d’exclusion suivant : </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>Le robot de recherche ne doit pas inclure d’URL contenant un paramètre CGI tel que 
     <userinput>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </userinput>. </p> <p>Si vous aviez les éléments suivants, incluez le masque d’URL d’expression régulière : </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>Le robot de recherche suit tous les liens des fichiers avec l'extension ".swf". L’ 
     <userinput>
       noindex 
     </userinput> keyword indique également que le texte des fichiers correspondants n’est pas indexé. </p> <p>Voir <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ajout de masques d’URL à l’index ou non des parties de votre site Web {#task_E1AFC17C746048B8843013D979E082C1}

Vous pouvez utiliser [!DNL URL Masks] pour définir les parties de votre site Web que vous souhaitez ou ne souhaitez pas analyser et indexer.

Utilisez le champ Tester les masques d’URL pour vérifier si un document est inclus ou non après l’indexation.

Veillez à recréer l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

**Pour ajouter des masques d’URL à l’index ou non des parties de votre site Web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**.
1. (Facultatif) Sur la [!DNL URL Masks] page, dans le **[!UICONTROL Test URL Masks]** champ, saisissez un masque d’URL de test sur votre site Web, puis cliquez sur **[!UICONTROL Test]**.
1. Dans le [!DNL URL Masks] champ, saisissez `include` (pour ajouter un site Web à analyser et à indexer) ou `exclude` (pour empêcher l’analyse et l’indexation d’un site Web), puis saisissez l’adresse du masque d’URL.

   Entrez une adresse de masque d’URL par ligne. Exemple :

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des masques de date {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

Vous pouvez utiliser des masques de date pour inclure ou exclure des fichiers des résultats de recherche en fonction de l’âge du fichier.

Veillez à recréer l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

Vous pouvez utiliser les deux types de masques de date suivants :

* Inclure les masques de date (&quot;inclure-jours&quot; et &quot;inclure-date&quot;)

   Inclure les fichiers d’index des masques de date datant du ou avant la date spécifiée.
* Exclure les masques de date (&quot;jours exclus&quot; et &quot;date exclus&quot;)

   Exclure les fichiers d’index des masques de date datant du ou avant la date spécifiée.

Par défaut, la date du fichier est déterminée à partir des informations de balise meta. Si aucune balise Meta n’est trouvée, la date d’un fichier est déterminée à partir de l’en-tête HTTP reçu du serveur lorsque le robot de recherche télécharge un fichier.

Chaque masque de date que vous spécifiez doit se trouver sur une ligne distincte.

Le masque peut spécifier l’une des valeurs suivantes :

* Un chemin complet comme dans `https://www.mydomain.com/products.html`
* Un chemin partiel comme dans `https://www.mydomain.com/products`
* URL utilisant des caractères génériques `https://www.mydomain.com/*.html`
* Expression régulière. Pour transformer un masque en expression régulière, insérez le mot-clé `regexp` avant l’URL.

Les masques de date incluent et excluent tous les deux la date de l’une des deux manières suivantes. Les masques ne sont appliqués que si les fichiers correspondants ont été créés au plus tard à la date spécifiée :

1. Un certain nombre de jours. Supposons, par exemple, que votre masque de date soit le suivant :

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   Le nombre de jours spécifié est comptabilisé en retour. Si le fichier est daté le ou avant la date d’arrivée, le masque est appliqué.

1. Date réelle au format AAAA-MM-JJ. Supposons, par exemple, que votre masque de date soit le suivant :

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   Si le document mis en correspondance est daté le ou avant la date spécifiée, le masque de date est appliqué.

Voici un exemple simple de masque de date d’exclusion :

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

Puisqu’il s’agit d’un masque de date d’exclusion, tout fichier qui correspond au modèle n’est pas indexé et a au moins 90 jours d’existence. Lorsque vous excluez un document, aucun texte n’est indexé et aucun lien n’est suivi à partir de ce fichier. Le fichier est en fait ignoré. Dans cet exemple, les fichiers et les dossiers peuvent correspondre au modèle d’URL spécifié. Notez que les deux `https://www.mydomain.com/docs/archive.html` et `https://www.mydomain.com/docs/archive/index.html` correspondent au modèle et ne sont pas indexés s’ils ont 90 jours ou plus. Pour faire correspondre uniquement les fichiers du `/docs/archive/` dossier, le masque de date doit contenir une barre oblique de fin, comme dans l’exemple suivant :

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

Les masques de date peuvent également être utilisés avec des caractères génériques. Le masque d’exclusion suivant indique au robot de recherche d’ignorer les fichiers avec l’extension &quot;.pdf&quot; qui sont datés le ou avant 2011-02-15. Le robot de recherche n’ajoute aucun fichier correspondant à votre index.

```
exclude-date 2011-02-15 *.pdf
```

L’option Inclure le masque de date est similaire, seuls les fichiers correspondants sont ajoutés à l’index. L’exemple de masque de date suivant indique au robot de recherche d’indexer le texte à partir de fichiers de date antérieure ou égale à zéro jour dans la `/docs/archive/manual/` zone du site Web.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

Les masques d’inclusion et d’exclusion peuvent fonctionner ensemble. Par exemple, vous pouvez exclure une grande partie de votre site Web de l’indexation en créant un masque de date d’exclusion tout en incluant une ou plusieurs des pages exclues avec un masque d’URL d’inclusion. Si l’URL de votre point d’entrée est la suivante :

```
https://www.mydomain.com/archive/
```

Le robot de recherche analyse et indexe toutes les pages sous `/archive/summer/`, `/archive/spring/`et `/archive/fall/` (en supposant qu’il existe des liens vers au moins une page dans chaque dossier à partir du `archive` dossier). Ce comportement se produit car les chemins d’accès aux liens permettent au robot de recherche de &quot;trouver&quot; les fichiers dans les `/summer/`, `/spring/`et `/fall/` dossiers et les URL des dossiers correspondent au masque d’inclusion généré automatiquement par l’URL du point d’entrée.

Voir [A propos des points](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)d’entrée d’URL.

Voir [Configuration des paramètres](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)de votre compte.

Vous pouvez choisir d’exclure toutes les pages de plus de 90 jours dans le `/fall/` dossier avec un masque de date d’exclusion, comme dans l’exemple suivant :

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Vous pouvez inclure uniquement `/archive/fall/index.html` (quel que soit l’âge de la correspondance (tout fichier de 0 jour ou plus correspond) dans l’index avec le masque de date suivant :

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

Pour que les deux exemples de masque ci-dessus fonctionnent comme prévu, vous devez d’abord répertorier le masque d’inclusion comme dans l’exemple suivant :

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Comme le robot de recherche suit les instructions dans l’ordre spécifié, il inclut d’abord `/archive/fall/index.html`, puis exclut le reste des fichiers du `/fall` dossier.

Si les instructions sont spécifiées de la manière opposée, comme dans l’exemple suivant :

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

N’ `/archive/fall/index.html` est alors pas inclus, même si le masque indique qu’il doit l’être. Un masque de date qui s’affiche en premier est toujours prioritaire sur un masque de date qui peut apparaître ultérieurement dans les paramètres du masque. De plus, si le robot de recherche rencontre une page qui correspond à la fois à un masque de date d’inclusion et à un masque de date d’exclusion, le masque répertorié en premier est toujours prioritaire.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

## A propos de l&#39;utilisation de mots-clés avec des masques de date {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

Vous pouvez qualifier chaque masque d’inclusion avec un ou plusieurs mots-clés séparés par des espaces, ce qui affecte la manière dont les pages mises en correspondance sont indexées.

Une virgule n&#39;est pas valide comme séparateur entre le masque et le mot-clé ; vous ne pouvez utiliser que des espaces.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Mot-clé </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>noindex </p> </td> 
   <td colname="col2"> <p> Si vous ne souhaitez pas indexer le texte sur les pages qui sont datées au plus tard à la date spécifiée par le masque d’inclusion, ajoutez 
     <userinput>
       noindex 
     </userinput> après le masque de date d’inclusion, comme dans l’exemple suivant : </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Veillez à séparer le mot-clé du masque par un espace. </p> <p>L’exemple ci-dessus indique que le robot de recherche suit tous les liens des fichiers avec l’extension ".swf" qui ont 10 jours ou plus. Toutefois, il désactive l’indexation de tout le texte contenu dans ces fichiers. </p> <p>Assurez-vous que le texte des fichiers plus anciens n’est pas indexé, mais suivez tous les liens de ces fichiers. Dans ce cas, utilisez un masque de date d’inclusion avec le mot-clé "noindex" au lieu d’utiliser un masque de date d’exclusion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>nofollow </p> </td> 
   <td colname="col2"> <p> Si vous souhaitez indexer le texte sur les pages qui sont datées le ou avant la date spécifiée par le masque d’inclusion, mais que vous ne souhaitez pas suivre les liens de la page correspondante, ajoutez 
     <userinput>
       nofollow 
     </userinput> après le masque de date d’inclusion, comme dans l’exemple suivant : </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Veillez à séparer le mot-clé du masque par un espace. </p> <p>L’ 
     <userinput>
       nofollow 
     </userinput> est l’équivalent d’une balise meta de robot avec 
     <userinput>
       content="nofollow" 
     </userinput> entre les 
     <userinput>
       &lt;head&gt;...&lt;/head&gt; 
     </userinput> balise des pages correspondantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>Utilisé pour inclure et exclure des masques. </p> <p>Le robot de recherche télécharge et analyse généralement chaque fichier avant de vérifier les masques de date. Ce comportement se produit car certains types de fichiers peuvent spécifier une date dans le fichier lui-même. Par exemple, un document HTML peut inclure des balises meta définissant la date du fichier. </p> <p>Si vous souhaitez exclure de nombreux fichiers en fonction de leur date et que vous ne souhaitez pas placer une charge inutile sur vos serveurs, vous pouvez utiliser 
     <userinput>
       server-date 
     </userinput> après l’URL dans le masque de date. </p> <p>Ce mot-clé indique au robot de recherche de faire confiance à la date du fichier renvoyé par votre serveur au lieu d'analyser chaque fichier. Par exemple, le masque de date d’exclusion suivant ignore les pages qui correspondent à l’URL si les documents ont 90 jours ou plus, selon la date renvoyée par le serveur dans les en-têtes HTTP : </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> Si la date renvoyée par le serveur est antérieure à 90 jours ou plus, 
     <userinput>
       server-date 
     </userinput> indique que les documents exclus ne doivent pas être téléchargés depuis votre serveur. Cela signifie une indexation plus rapide de vos documents et une charge réduite sur vos serveurs. Si   
     <userinput>
       server-date 
     </userinput> n’est pas spécifiée, le robot de recherche ignore la date renvoyée par le serveur dans les en-têtes HTTP. En revanche, chaque fichier est téléchargé et vérifié pour voir si la date est spécifiée. Si aucune date n’est spécifiée dans le fichier, le robot de recherche utilise la date renvoyée par le serveur. </p> <p>Vous ne devez pas utiliser 
     <userinput>
       server-date 
     </userinput> si vos fichiers contiennent des commandes qui remplacent la date du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> À utiliser pour inclure et exclure des masques. </p> <p>Tout masque de date précédé de 
     <userinput>
       regexp 
     </userinput> est traitée comme une expression régulière. </p> <p>Si le robot de recherche rencontre des fichiers qui correspondent à un masque de date d’expression régulière exclu, il n’indexe pas ces fichiers. </p> <p>Si le robot de recherche rencontre des fichiers qui correspondent à un masque de date d’expression régulière inclus, il indexe ces documents. </p> <p>Supposons, par exemple, que vous ayez le masque de date suivant : </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>Le masque indique au robot de recherche d’exclure les fichiers correspondants de 180 jours ou plus. Autrement dit, les fichiers qui contiennent le mot "archive" dans leur URL. </p> <p>Voir <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ajout de masques de date à l’index ou non des parties de votre site Web {#task_0010543C55F648D2B5DEFEFAD60FAF04}

Vous pouvez utiliser des masques de date pour inclure ou exclure des fichiers des résultats de recherche des clients en fonction de l’âge des fichiers.

Utilisez les champs **[!UICONTROL Test Date]** et **[!UICONTROL Test URL]** pour vérifier si un fichier est ou n’est pas inclus après l’indexation.

Veillez à recréer l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

**Pour ajouter des masques de date à l’index ou non des parties de votre site Web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**.
1. (Facultatif) Sur la [!DNL Date Masks] page, dans le **[!UICONTROL Test Date]** champ, saisissez une date au format AAAA-MM-JJ (par exemple `2011-07-25`) ; dans le **[!UICONTROL Test URL]** champ, saisissez un masque d’URL à partir de votre site Web, puis cliquez sur **[!UICONTROL Test]**.
1. Dans le [!DNL Date Masks] champ, saisissez une adresse de masque de date par ligne.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des mots de passe {#concept_3EDBD731725D46B891F834D4472774DC}

Pour accéder à des parties de votre site Web protégées par l’authentification de base HTTP, vous pouvez ajouter un ou plusieurs mots de passe.

Avant que les effets des paramètres Mot de passe ne soient visibles par les clients, vous devez recréer l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

Sur la [!DNL Passwords] page, vous saisissez chaque mot de passe sur une seule ligne. Le mot de passe se compose d’une URL ou d’un domaine, d’un nom d’utilisateur et d’un mot de passe, comme dans l’exemple suivant :

```
https://www.mydomain.com/ myname mypassword
```

Au lieu d’utiliser un chemin d’URL, comme ci-dessus, vous pouvez également spécifier un domaine.

Pour déterminer le domaine à utiliser, ouvrez une page Web protégée par mot de passe avec un navigateur et ouvrez la boîte de dialogue &quot;Entrez le mot de passe réseau&quot;.

![](assets/realms.gif)

Dans ce cas, le nom du domaine est &quot;Mon domaine du site&quot;.

En utilisant le nom de domaine ci-dessus, votre mot de passe peut se présenter comme suit :

```
My Site Realm myusername mypassword
```

Si votre site Web comporte plusieurs domaines, vous pouvez créer plusieurs mots de passe en saisissant un nom d’utilisateur et un mot de passe pour chaque domaine sur une ligne distincte, comme dans l’exemple suivant :

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

Vous pouvez mélanger des mots de passe qui contiennent des URL ou des domaines afin que votre liste de mots de passe ressemble à ce qui suit :

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

Dans la liste ci-dessus, le premier mot de passe utilisé contient un domaine ou une URL qui correspond à la demande d’authentification du serveur. Même si le fichier `https://www.mysite.com/path1/path2/index.html` se trouve dans `Realm3`, par exemple `name2` et `password2` sont utilisés car le mot de passe défini avec l&#39;URL est répertorié au-dessus de celui défini avec le domaine.

## Ajout de mots de passe pour accéder aux zones de votre site Web qui nécessitent une authentification {#task_DED19D476FF04B48BB6456D5ECB8628A}

Vous pouvez utiliser Mots de passe pour accéder aux zones protégées par mot de passe de votre site Web à des fins d’analyse et d’indexation.

Avant que les effets de votre mot de passe ne soient visibles par les clients, veillez à recréer l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

**Pour ajouter des mots de passe pour accéder à des zones de votre site Web qui nécessitent une authentification**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**.
1. Sur la [!DNL Passwords] page, dans le **[!UICONTROL Passwords]** champ, saisissez un domaine ou une URL, son nom d’utilisateur et son mot de passe associés, séparés par un espace.

   Exemple de mot de passe de domaine et d’URL sur des lignes distinctes :

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   Ajoutez uniquement un mot de passe par ligne.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des types de contenu {#concept_6FEA1355C0374500B4C53090C34A8A07}

Vous pouvez utiliser [!DNL Content Types] pour sélectionner les types de fichiers à analyser et à indexer pour ce compte.

Les types de contenu que vous pouvez analyser et indexer incluent des documents PDF, des documents texte, des films Adobe Flash, des fichiers provenant d’applications Microsoft Office telles que Word, Excel et Powerpoint, ainsi que du texte dans des fichiers MP3. Le texte qui se trouve dans les types de contenu sélectionnés est recherché avec tout le reste du texte de votre site Web.

Avant que les effets des paramètres Types de contenu ne soient visibles par les clients, vous devez recréer l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

## A propos de l’indexation des fichiers de musique MP3 {#section_AD2E28BEEE3E46629E2B05C34A963673}

Si vous sélectionnez l’option **[!UICONTROL Text in MP3 Music Files]** sur la [!DNL Content Types] page, un fichier MP3 est analysé et indexé de deux manières. La première méthode la plus courante consiste à utiliser une balise href d’ancrage dans un fichier HTML, comme dans l’exemple suivant :

```
<a href="MP3-file-URL"></a>
```

La deuxième méthode consiste à entrer l’URL du fichier MP3 en tant que point d’entrée d’URL.

Voir [A propos des points](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)d’entrée d’URL.

Un fichier MP3 est reconnu par son type MIME &quot;audio/mpeg&quot;.

Sachez que les fichiers de musique MP3 peuvent être très volumineux, même s’ils ne contiennent généralement qu’une petite quantité de texte. Par exemple, les fichiers MP3 peuvent stocker des éléments tels que le nom de l’album, le nom de l’artiste, le titre de la chanson, le genre de chanson, l’année de publication et un commentaire. Ces informations sont stockées à la toute fin du fichier dans ce qu’on appelle la BALISE. Les fichiers MP3 contenant des informations TAG sont indexés de la manière suivante :

* Le titre de la chanson est traité comme le titre d’une page HTML.
* Le commentaire est traité comme une description définie pour une page HTML.
* Le genre est traité comme un mot-clé défini pour une page HTML.
* Le nom de l’artiste, le nom de l’album et l’année de publication sont traités comme le corps d’une page HTML.

Notez que chaque fichier MP3 analysé et indexé sur votre site Web compte comme une page.

Si votre site Web contient de nombreux fichiers MP3 volumineux, vous pouvez dépasser la limite d’octets d’indexation de votre compte. Si cela se produit, vous pouvez désélectionner **[!UICONTROL Text in MP3 Music Files]** sur la [!DNL Content Types] page pour empêcher l’indexation de tous les fichiers MP3 de votre site Web.

Si vous souhaitez uniquement empêcher l’indexation de certains fichiers MP3 sur votre site Web, vous pouvez effectuer l’une des opérations suivantes :

* Entourez les balises d’ancrage qui pointent vers les fichiers MP3 avec `<nofollow>` et `</nofollow>` des balises. Le robot de recherche ne suit pas les liens entre ces balises.

* Ajoutez les URL des fichiers MP3 en tant que masques d’exclusion.

   Voir [A propos des masques](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164)URL.

## Sélection des types de contenu à analyser et à indexer {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

Vous pouvez utiliser [!DNL Content Types] pour sélectionner les types de fichiers à analyser et à indexer pour ce compte.

Les types de contenu que vous pouvez analyser et indexer incluent des documents PDF, des documents texte, des films Adobe Flash, des fichiers provenant d’applications Microsoft Office telles que Word, Excel et Powerpoint, ainsi que du texte dans des fichiers MP3. Le texte qui se trouve dans les types de contenu sélectionnés est recherché avec tout le reste du texte de votre site Web.

Avant que les effets des paramètres Types de contenu ne soient visibles par les clients, vous devez recréer l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

Pour analyser et indexer des fichiers MP3 chinois, japonais ou coréens, procédez comme suit. Ensuite, dans **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, spécifiez le jeu de caractères utilisé pour coder les fichiers MP3.

Voir [A propos des injections](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

**Pour sélectionner des types de contenu à analyser et à indexer**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.
1. Sur la [!DNL Content Types] page, vérifiez les types de fichiers que vous souhaitez analyser et indexer sur votre site Web.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des connexions {#concept_E2F3B7E7521147479E5948A94BB3A40B}

Vous pouvez utiliser Connexions pour ajouter jusqu’à dix connexions HTTP que le robot de recherche utilise pour indexer votre site Web.

L’augmentation du nombre de connexions peut réduire de manière significative le temps nécessaire à l’exécution d’une analyse et d’un index. Sachez toutefois que chaque connexion supplémentaire augmente la charge sur votre serveur.

## Ajout de connexions pour augmenter la vitesse d’indexation {#task_3E9B83E43C1842A19066355A15C4A6FB}

Vous pouvez réduire le temps nécessaire pour indexer votre site Web en utilisant Connexions pour augmenter le nombre de connexions HTTP simultanées utilisées par le moteur de recherche. Vous pouvez ajouter jusqu&#39;à dix connexions.

Gardez à l’esprit que chaque connexion supplémentaire augmente la charge placée sur votre serveur.

**Pour ajouter des connexions afin d’augmenter la vitesse d’indexation**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**.
1. Sur la [!DNL Parallel Indexing Connections] page, dans le **[!UICONTROL Number of Connections]** champ, entrez le nombre de connexions (1-10) que vous souhaitez ajouter.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos de l’envoi de formulaire {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

Vous pouvez utiliser l’envoi de formulaires pour vous aider à reconnaître et à traiter les formulaires de votre site Web.

Lors de l’analyse et de l’indexation de votre site Web, chaque formulaire rencontré est comparé aux définitions de formulaire que vous avez ajoutées. Si un formulaire correspond à une définition de formulaire, le formulaire est envoyé pour indexation. Si un formulaire correspond à plusieurs définitions, le formulaire est envoyé une fois pour chaque définition correspondante.

## Ajout de définitions de formulaire pour l’indexation de formulaires sur votre site Web {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

Vous pouvez vous servir [!DNL Form Submission] pour traiter les formulaires reconnus sur votre site Web à des fins d’indexation.

Veillez à recréer l’index de votre site afin que les résultats de vos modifications soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

**Pour ajouter des définitions de formulaire pour l’indexation de formulaires sur votre site Web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Sur la [!DNL Form Submission] page, cliquez sur **[!UICONTROL Add New Form]**.
1. Sur la [!DNL Add Form Definition] page, définissez les options [!DNL Form Recognition] et [!DNL Form Submission] .

   Les cinq options de la [!DNL Form Recognition] section de la [!DNL Form Definition] page permettent d’identifier les formulaires pouvant être traités dans vos pages Web.

   Les trois options de la [!DNL Form Submission] section permettent de spécifier les paramètres et les valeurs qui sont envoyés avec un formulaire à votre serveur Web.

   Entrez un paramètre de reconnaissance ou d’envoi par ligne. Chaque paramètre doit inclure un nom et une valeur.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <b>Reconnaissance de formulaire</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque d’URL de page </p> </td> 
      <td colname="col2"> <p>Identifiez la ou les pages Web qui contiennent le formulaire. Pour identifier un formulaire qui s’affiche sur une seule page, entrez l’URL de cette page, comme dans l’exemple suivant : </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>Pour identifier les formulaires qui apparaissent sur plusieurs pages, spécifiez un masque d’URL qui utilise des caractères génériques pour décrire les pages. Pour identifier les formulaires rencontrés sur une page ASP sous <code> https://www.mydomain.com/register/ </code>, par exemple, vous devez spécifier les éléments suivants : </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>Vous pouvez également utiliser une expression régulière pour identifier plusieurs pages. Indiquez simplement la variable 
      <userinput>
        regexp 
      </userinput> avant le masque d’URL, comme dans l’exemple suivant : </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque d’URL d’action </p> </td> 
      <td colname="col2"> <p>Identifie l’attribut d’action de la variable 
      <userinput>
        &lt;formulaire&gt; 
      </userinput> Balise. </p> <p>Tout comme le masque d’URL de page, le masque d’URL d’action peut prendre la forme d’une URL unique, d’une URL avec des caractères génériques ou d’une expression régulière. </p> <p>Le masque d’URL peut être l’un des suivants : 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> Chemin complet, comme dans l’exemple suivant : <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> Chemin partiel comme dans l’exemple suivant : <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> URL qui utilise des caractères génériques comme dans l’exemple suivant : <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> Expression régulière comme dans l’exemple suivant : <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>Si vous ne souhaitez pas indexer le texte sur les pages identifiées par un masque d’URL ou par un masque d’URL d’action, ou si vous ne souhaitez pas que les liens soient suivis sur ces pages, vous pouvez utiliser la variable 
      <userinput>
        noindex 
      </userinput> et 
      <userinput>
        nofollow 
      </userinput> mots-clés. Vous pouvez ajouter ces mots-clés à vos masques à l’aide de masques d’URL ou de points d’entrée. </p> <p>Voir <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> A propos des points de saisie d’URL </a>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> A propos des masques d’URL </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque de nom de formulaire </p> </td> 
      <td colname="col2"> <p>Identifie les formulaires si la variable 
      <userinput>
        &lt;formulaire&gt; 
      </userinput> les balises de vos pages Web contiennent un attribut name. </p> <p>Vous pouvez utiliser un nom simple ( 
      <userinput>
        login_form 
      </userinput>), un nom avec un caractère générique ( 
      <userinput>
        formulaire* 
      </userinput>) ou une expression régulière ( 
      <userinput>
        regexp ^.*autoriser.*$ 
      </userinput>). </p> <p>Vous pouvez généralement laisser ce champ vide, car les formulaires n’ont généralement pas d’attribut name. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque d’ID de formulaire </p> </td> 
      <td colname="col2"> <p>Identifie les formulaires si la variable 
      <userinput>
        &lt;formulaire&gt; 
      </userinput> les balises de vos pages Web contiennent un attribut id. </p> <p>Vous pouvez utiliser un nom simple ( 
      <userinput>
        login_form 
      </userinput>), un nom avec un caractère générique ( 
      <userinput>
        formulaire* 
      </userinput>) ou une expression régulière ( 
      <userinput>
        regexp ^.*autoriser.*$ 
      </userinput>). </p> <p>Vous pouvez généralement laisser ce champ vide, car les formulaires n’ont généralement pas d’attribut name. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètres </p> </td> 
      <td colname="col2"> <p>Identifiez les formulaires qui contiennent ou ne contiennent pas un paramètre nommé ou un paramètre nommé avec une valeur spécifique. </p> <p>Par exemple, pour identifier un formulaire qui contient un paramètre de courrier électronique prédéfini sur rick_brough@mydomain.com, un paramètre de mot de passe, mais pas un paramètre de prénom, vous devez spécifier les paramètres suivants, une par ligne : </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Envoi de formulaire</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remplacer l’URL d’action </p> </td> 
      <td colname="col2"> <p>Indiquez quand la cible de l’envoi du formulaire est différente de ce qui est spécifié dans l’attribut d’action du formulaire. </p> <p>Par exemple, vous pouvez utiliser cette option lorsque le formulaire est envoyé par le biais d’une fonction JavaScript qui construit une valeur d’URL différente de celle du formulaire. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Méthode Override </p> </td> 
      <td colname="col2"> <p>Indiquez quand la cible de l’envoi du formulaire est différente de ce qui est utilisé dans l’attribut d’action du formulaire et quand le code JavaScript d’envoi a modifié la méthode. </p> <p>Valeurs par défaut de tous les paramètres de formulaire ( 
      <userinput>
        &lt;input&gt; 
      </userinput> balises, y compris les champs masqués), la valeur par défaut 
      <userinput>
        &lt;option&gt; 
      </userinput> de a 
      <userinput>
        &lt;sélectionner&gt; 
      </userinput> et le texte par défaut entre 
      <userinput>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </userinput> ) sont lues à partir de la page Web. Toutefois, tout paramètre répertorié dans la <span class="wintitle"> section Envoi de formulaire </span> , dans le champ <span class="uicontrol"> Paramètres </span> , est remplacé par les valeurs par défaut du formulaire. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètres </p> </td> 
      <td colname="col2"> <p>Vous pouvez prédéfinir les paramètres d’envoi du formulaire à l’aide de la variable 
      <userinput>
        ne sont pas 
      </userinput> mot-clé. </p> <p>Lorsque vous ajoutez un préfixe à un paramètre 
      <userinput>
        ne sont pas 
      </userinput>, elle n’est pas envoyée dans le cadre de l’envoi du formulaire. Ce comportement s’avère utile pour les cases à cocher qui doivent être envoyées et non sélectionnées. </p> <p>Supposons, par exemple, que vous souhaitiez envoyer les paramètres suivants : </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> Le paramètre de courrier électronique avec la valeur 
      <userinput>
        nobody@mydomain.com 
      </userinput> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> Le paramètre password avec la valeur 
      <userinput>
        tryme 
      </userinput> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> Le paramètre mycheckbox est désélectionné. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>Tous les autres 
      <userinput>
        &lt;formulaire&gt; 
      </userinput> paramètres comme valeurs par défaut </p> </li> 
      </ul> </p> <p>Le paramètre d’envoi du formulaire se présente comme suit : </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>L’attribut de méthode de la variable 
      <userinput>
        &lt;formulaire&gt; 
      </userinput> sur la page Web est utilisée pour déterminer si les données sont envoyées à votre serveur à l’aide de la méthode GET ou POST. </p> <p>Si nous avons généré    
      <userinput>
        &lt;formulaire&gt; 
      </userinput> ne contient pas d’attribut de méthode, le formulaire est envoyé à l’aide de la méthode GET. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une définition de formulaire {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Vous pouvez modifier une définition de formulaire existante si un formulaire de votre site Web a été modifié ou si vous devez simplement modifier la définition.

Gardez à l’esprit qu’il n’existe aucune [!DNL History] fonction sur la [!DNL Form Submission] page permettant de rétablir les modifications apportées à une définition de formulaire.

Veillez à recréer l’index de votre site afin que les résultats de vos modifications soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

**Pour modifier une définition de formulaire**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Sur la [!DNL Form Submission] page, cliquez **[!UICONTROL Edit]** à droite d’une définition de formulaire à mettre à jour.
1. Sur la [!DNL Edit Form Definition] page, définissez les options [!DNL Form Recognition] et [!DNL Form Submission] .

   Consultez le tableau des options sous [Ajout de définitions de formulaire pour l’indexation de formulaires sur votre site Web](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une définition de formulaire {#task_C350FC0CDE344F2786215D544C048B5E}

Vous pouvez supprimer une définition de formulaire existante si le formulaire n’existe plus sur votre site Web ou si vous ne souhaitez plus traiter et indexer un formulaire particulier.

Gardez à l’esprit qu’il n’existe aucune [!DNL History] fonction sur la [!DNL Form Submission] page permettant de rétablir les modifications apportées à une définition de formulaire.

Veillez à recréer l’index de votre site afin que les résultats de vos modifications soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

**Pour supprimer une définition de formulaire**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Sur la [!DNL Form Submission] page, cliquez **[!UICONTROL Delete]** à droite d’une définition de formulaire à supprimer.

   Veillez à choisir la définition de formulaire appropriée à supprimer. Il n’existe pas de boîte de dialogue de confirmation de suppression lorsque vous cliquez **[!UICONTROL Delete]** dans l’étape suivante.
1. Sur la [!DNL Delete Form Definition] page, cliquez sur **[!UICONTROL Delete]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos du connecteur d’index {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

Utilisez [!DNL Index Connector] pour définir des sources d’entrée supplémentaires pour indexer des pages XML ou tout type de flux.

Vous pouvez utiliser une source d’entrée de flux de données pour accéder au contenu stocké dans un formulaire différent de ce qui est généralement découvert sur un site Web à l’aide de l’une des méthodes d’analyse disponibles. Chaque document analysé et indexé correspond directement à une page de contenu de votre site Web. Cependant, un flux de données provient d’un document XML ou d’un fichier texte délimité par des virgules ou des tabulations et contient les informations de contenu à indexer.

Une source de données XML se compose de normes XML, ou enregistrements, qui contiennent des informations qui correspondent à des documents individuels. Ces documents individuels sont ajoutés à l’index. Un flux de données textuelles contient des enregistrements séparés par une nouvelle ligne qui correspondent à des documents individuels. Ces documents individuels sont également ajoutés à l’index. Dans les deux cas, une configuration de connecteur d’index décrit l’interprétation du flux. Chaque configuration décrit l’emplacement du fichier et la manière dont les serveurs y accèdent. La configuration décrit également les informations de &quot;mappage&quot;. C’est-à-dire comment les éléments de chaque enregistrement sont utilisés pour remplir les champs de métadonnées dans l’index résultant.

Après avoir ajouté une définition de Connecteur d’index à la [!DNL Staged Index Connector Definitions] page, vous pouvez modifier n’importe quel paramètre de configuration, *à l’exception* des valeurs Nom ou Type.

La [!DNL Index Connector] page affiche les informations suivantes :

* Nom des connecteurs d’index définis que vous avez configurés et ajoutés.
* L’un des types de source de données suivants pour chaque connecteur que vous avez ajouté :

   * **Texte** - Fichiers simples &quot;plats&quot;, délimités par des virgules, délimités par des tabulations ou autres formats délimités de manière cohérente.
   * **Flux** - Flux XML.
   * **XML** - Collections de documents XML.

* Indique si le connecteur est activé ou non pour l’analyse et l’indexation suivantes effectuées.
* Adresse de la source de données.

Voir aussi [A propos du connecteur d’index](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## Fonctionnement du processus d’indexation pour les configurations de texte et de flux dans Index Connector {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Étape </p> </th> 
   <th colname="col2" class="entry"> <p>Processus </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Téléchargez la source de données. </p> </td> 
   <td colname="col3"> <p>Pour les configurations de texte et de flux, il s’agit d’un téléchargement de fichier simple. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Ventilez la source de données téléchargée en pseudo-documents individuels. </p> </td> 
   <td colname="col3"> <p>Pour <span class="uicontrol"> Texte </span>, chaque nouvelle ligne de texte délimité par une ligne correspond à un document individuel et est analysée à l’aide du délimiteur spécifié, tel qu’une virgule ou un tabulation. </p> <p>Pour le <span class="uicontrol"> flux </span>, les données de chaque document sont extraites à l’aide d’un modèle d’expression régulière sous la forme suivante : </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>A l’aide de <span class="uicontrol"> Map </span> sur la page <span class="wintitle"> Index Connector Add </span> , créez une copie mise en cache des données, puis créez une liste de liens pour le moteur de recherche. Les données sont stockées dans un cache local et renseignées avec les champs configurés. </p> <p>Les données analysées sont écrites dans le cache local. </p> <p>Ce cache est lu ultérieurement pour créer les documents HTML simples dont le moteur de recherche a besoin. Par exemple : </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>L’élément <span class="codeph"> &lt;title&gt; </span> n’est généré que lorsqu’il existe un mappage au champ de métadonnées Titre. De même, l’élément <span class="codeph"> &lt;body&gt; </span> n’est généré que lorsqu’il existe un mappage au champ de métadonnées Body. </p> <p> <b>Important</b>: Il n’existe aucune prise en charge pour l’affectation de valeurs à la balise meta d’URL prédéfinie. </p> <p>Pour tous les autres mappages, <span class="codeph"> &lt;meta&gt; </span> balises sont générées pour chaque champ contenant des données dans le document d’origine. </p> <p>Les champs de chaque document sont ajoutés au cache. Pour chaque document écrit dans le cache, un lien est également généré, comme dans les exemples suivants : </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>Le mappage de la configuration doit comporter un champ identifié comme clé principale. Ce mappage forme la clé utilisée lorsque les données sont extraites du cache. </p> <p>L’analyseur reconnaît l’index d’URL <span class="codeph"> : préfixe </span> de schéma, qui peut ensuite accéder aux données mises en cache localement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Analyse du jeu de documents mis en cache. </p> </td> 
   <td colname="col3"> <p>Index <span class="codeph"> : </span> les liens sont ajoutés à la liste des liens en attente de l’analyseur et sont traités dans la séquence d’analyse normale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Traitez chaque document. </p> </td> 
   <td colname="col3"> <p>La valeur de clé de chaque lien correspond à une entrée dans le cache. L’analyse de chaque lien entraîne la récupération des données de ce document à partir du cache. Il est ensuite "assemblé" dans une image HTML qui est traitée et ajoutée à l’index. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Fonctionnement du processus d’indexation pour les configurations XML dans Index Connector {#section_7F1551EA51854C5C99F284CE260526EB}

Le processus d’indexation pour la configuration XML est similaire au processus pour les configurations Texte et Flux avec les modifications et exceptions mineures suivantes.

Les documents des analyses XML étant déjà séparés en fichiers individuels, les étapes 1 et 2 du tableau ci-dessus ne s’appliquent pas directement. Si vous spécifiez une URL dans les champs **[!UICONTROL Host Address]** et **[!UICONTROL File Path]** de la [!DNL Index Connector Add] page, elle est téléchargée et traitée en tant que document HTML normal. Le document de téléchargement devrait contenir un ensemble de `<a href="{url}"...` liens, chacun pointant vers un document XML qui est traité. Ces liens sont convertis au format suivant :

```
<a href="index:<ic_config_name>?url="{url}">
```

Par exemple, si la configuration d’Adobe renvoyait les liens suivants :

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

Dans le tableau ci-dessus, l’étape 3 ne s’applique pas et l’étape 4 est terminée au moment de l’analyse et de l’indexation.

Vous pouvez également mélanger vos documents XML avec d’autres documents qui ont été découverts naturellement lors du processus d’analyse. Dans ce cas, vous pouvez utiliser des règles de réécriture ( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**) pour modifier les URL des documents XML afin de les diriger vers Index Connector.

Voir [A propos de l’analyse de la liste Récupération des règles](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA)d’URL.

Par exemple, supposons que vous ayez la règle de réécriture suivante :

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

Cette règle traduit toute URL se terminant par `.xml` un lien Connecteur d’index. L’analyseur reconnaît et réécrit le schéma `index:` d’URL. Le processus de téléchargement est redirigé vers le serveur Apache Index Connector sur le serveur maître. Chaque document téléchargé est examiné à l’aide du même modèle d’expression régulière que celui utilisé avec les flux. Dans ce cas, toutefois, le document HTML fabriqué n’est pas enregistré dans le cache. Au lieu de cela, il est transmis directement au moteur de recherche pour le traitement de l’index.

## Configuration de plusieurs connecteurs d’index {#section_C2B14C0F06354A57AEF6238FF3814E5D}

Vous pouvez définir plusieurs configurations Index Connector pour n’importe quel compte. Les configurations sont automatiquement ajoutées à la liste déroulante dans **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]** , comme illustré ci-dessous :

![](assets/url_entrypoints_index_connector.png)

La sélection d’une configuration dans la liste déroulante ajoute la valeur à la fin de la liste des points d’entrée d’URL.

>[!NOTE]
>
>Bien que les configurations du connecteur d’index désactivées soient ajoutées à la liste déroulante, vous ne pouvez pas les sélectionner. Si vous sélectionnez la même configuration Index Connector une seconde fois, elle est ajoutée à la fin de la liste et l’instance précédente est supprimée.

Pour spécifier un point d’entrée Connector d’index pour une analyse incrémentielle, vous pouvez ajouter des entrées au format suivant :

```
index:<indexconnector_configuration_name>
```

L’analyseur traite chaque entrée ajoutée si elle se trouve sur la page Connecteurs d’index et si elle est activée.

Remarque : L’URL de chaque document étant construite à l’aide du nom de configuration du connecteur d’index et de la clé principale du document, veillez à utiliser le même nom de configuration du connecteur d’index lors des mises à jour incrémentielles ! Cela permet [!DNL Adobe Search&Promote] de mettre correctement à jour les documents indexés précédemment.

Voir aussi [A propos des points](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)d’entrée d’URL.

**Utilisation des zones de configuration lorsque vous ajoutez un connecteur d’index**

Lorsque vous ajoutez un connecteur d’index, vous pouvez éventuellement utiliser cette fonctionnalité **[!UICONTROL Setup Maps]** pour télécharger un exemple de source de données. Les données sont examinées pour déterminer si l’indexation est appropriée.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si vous avez choisi le type Connector... </p> </th> 
   <th colname="col2" class="entry"> <p>La fonction de configuration des zones... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texte </p> </td> 
   <td colname="col2"> <p>Détermine la valeur du délimiteur en essayant d’abord d’utiliser des tabulations, puis des barres verticales ( <span class="codeph"> | </span>) et enfin des virgules ( <span class="codeph"> , </span>). Si vous avez déjà spécifié une valeur de délimiteur avant de cliquer sur <span class="uicontrol"> Configurer les zones </span>, cette valeur est utilisée à la place. </p> <p>Le modèle adapté permet de remplir les champs de zone cliquable avec des estimations aux valeurs de balise et de champ appropriées. En outre, un échantillon des données analysées s’affiche. Veillez à sélectionner <span class="uicontrol"> En-têtes dans la première rangée </span> si vous savez que le fichier contient une rangée d’en-tête. La fonction de configuration utilise ces informations pour mieux identifier les entrées de mappage résultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flux </p> </td> 
   <td colname="col2"> <p>Télécharge la source de données et effectue une analyse XML simple. </p> <p>Les identifiants XPath résultants s’affichent dans les lignes Balise du tableau de mappage, et des valeurs similaires dans les champs. Ces lignes identifient uniquement les données disponibles et ne génèrent pas les définitions XPath les plus complexes. Cependant, il est toujours utile, car il décrit les données XML et identifie les valeurs d’Itemtag. </p> <p> <p>Remarque :  La fonction Setup Maps télécharge la source XML entière pour effectuer son analyse. Si le fichier est volumineux, cette opération peut expirer. </p> </p> <p>En cas de succès, cette fonction identifie tous les éléments XPath possibles, dont beaucoup ne sont pas souhaitables. Vérifiez que vous examinez les définitions de zone cliquable résultantes et supprimez celles dont vous n’avez pas besoin ou que vous ne souhaitez pas. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>Télécharge l’URL d’un document individuel représentatif, et non la liste des liens principaux. Ce document unique est analysé à l’aide du même mécanisme que celui utilisé avec les flux et les résultats sont affichés. </p> <p>Avant de cliquer sur <span class="uicontrol"> Ajouter </span> pour enregistrer la configuration, veillez à rétablir l’URL dans le document de la liste des liens maître. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Important**: La fonction Setup Maps (Mappages de configuration) peut ne pas fonctionner pour les jeux de données XML volumineux, car l’analyseur de fichiers tente de lire l’intégralité du fichier en mémoire. Par conséquent, vous pourriez rencontrer une situation de mémoire insuffisante. Cependant, lorsque le même document est traité au moment de l’indexation, il n’est pas lu en mémoire. Au lieu de cela, les documents volumineux sont traités &quot;en déplacement&quot; et ne sont pas lus entièrement en mémoire.

**Utilisation de l’aperçu lorsque vous ajoutez un connecteur d’index**

Lorsque vous ajoutez un connecteur d’index, vous pouvez éventuellement utiliser la fonctionnalité **[!UICONTROL Preview]** pour valider les données, comme si vous les aviez enregistrées. Il exécute un test par rapport à la configuration, mais sans enregistrer la configuration dans le compte. Le test accède à la source de données configurée. Toutefois, il écrit le cache de téléchargement à un emplacement temporaire ; il n’est pas en conflit avec le dossier cache principal utilisé par l’analyseur d’indexation.

L’option Aperçu traite uniquement un document par défaut de cinq, tel que contrôlé par Access:IndexConnector-Preview-Max-Documents. Les documents prévisualisés s’affichent sous forme source, dans la mesure où ils sont présentés au moteur d’indexation. L&#39;affichage est similaire à une fonction &quot;Afficher la source&quot; dans un navigateur Web. Vous pouvez parcourir les documents du jeu d’aperçu à l’aide de liens de navigation standard.

L’aperçu ne prend pas en charge les configurations XML, car ces documents sont traités directement et ne sont pas téléchargés dans le cache.

## Ajout d’une définition de connecteur d’index {#task_96779B651A654E1F871F55D6DBBC8886}

Chaque configuration du connecteur d’index définit une source de données et des mappages pour relier les éléments de données définis pour cette source aux champs de métadonnées de l’index.

Avant que les effets de la nouvelle définition activée ne soient visibles par les clients, recréez l’index de votre site.

**Pour ajouter une définition de connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la [!DNL Stage Index Connector Definitions] page, cliquez sur **[!UICONTROL Add New Index Connector]**.
1. Sur la [!DNL Index Connector Add] page, définissez les options de connecteur de votre choix. Les options disponibles dépendent de l’option **[!UICONTROL Type]** sélectionnée.

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
      <td colname="col2"> <p>Nom unique de la configuration du connecteur d’index. Vous pouvez utiliser des caractères alphanumériques. Les caractères "_" et "-" sont également autorisés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>Source de vos données. Le type de source de données que vous sélectionnez affecte les options disponibles sur la page d’ajout du connecteur <span class="wintitle"> d’index </span> . Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texte </span> <p>Fichiers de texte aplati simples, formats délimités par des virgules, tabulés ou autres formats délimités de manière cohérente. Chaque ligne de texte délimité par une nouvelle ligne correspond à un document individuel et est analysée à l’aide du délimiteur spécifié. </p> <p>Vous pouvez mapper chaque valeur, ou colonne, à un champ de métadonnées, référencé par le numéro de colonne, en commençant par 1 (un). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Flux </span> <p>Télécharge un document XML maître contenant plusieurs "lignes" d’informations. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>Télécharge un document XML original contenant des liens ( 
      <userinput>
        &lt;a&gt; 
      </userinput>) à des documents XML individuels. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Texte</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active l’analyse et l’index de la configuration. Vous pouvez également désactiver la configuration pour empêcher l’analyse et l’indexation. </p> <p> <b>Remarque</b>: Les configurations du connecteur d’index désactivées sont ignorées si elles figurent dans une liste de points d’entrée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse de l’hôte du serveur où se trouvent vos données. </p> <p>Si vous le souhaitez, vous pouvez spécifier un chemin d’accès URI complet (Uniform Resource Identifier) au document de source de données, comme dans les exemples suivants : </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>ou </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>L’URI est ventilé selon les entrées appropriées pour les champs Adresse hôte, Chemin du fichier, Protocole et, éventuellement, Nom d’utilisateur et Mot de passe. </p> <p>Indique l’adresse IP ou l’adresse URL du système hôte sur lequel le fichier de source de données est trouvé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Indique le chemin d’accès au fichier de texte plat simple, délimité par des virgules, délimité par des tabulations ou à un autre fichier de format délimité de manière cohérente. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin de fichier incrémentiel </p> </td> 
      <td colname="col2"> <p>Indique le chemin d’accès au fichier de texte plat simple, délimité par des virgules, délimité par des tabulations ou à un autre fichier de format délimité de manière cohérente. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations d’index incrémentiel. Si aucun fichier n’est spécifié, le fichier répertorié sous Chemin du fichier est utilisé à la place. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin d’accès vertical au fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au fichier de texte plat simple, délimité par des virgules, délimité par des tabulations ou à un autre fichier de format délimité de manière cohérente à utiliser lors d’une mise à jour verticale. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations de mise à jour verticale. </p> <p> <b>Remarque</b>: Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprime le chemin du fichier </p> </td> 
      <td colname="col2"> <p>Indique le chemin d’accès au fichier de texte aplati simple, contenant une seule valeur d’identificateur de document par ligne. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations d’index incrémentiel. Les valeurs trouvées dans ce fichier sont utilisées pour créer des requêtes "delete" afin de supprimer des documents indexés précédemment. Les valeurs de ce fichier doivent correspondre aux valeurs trouvées dans les fichiers Chemin d’accès au fichier complet ou incrémentiel, dans la colonne identifiée comme clé <span class="uicontrol"> principale </span>. </p> <p> <b>Remarque</b>: Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Spécifie le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Si nécessaire, vous pouvez entrer les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Expiration </p> </td> 
      <td colname="col2"> <p>Spécifie le délai d’expiration, en secondes, pour les connexions FTP, SFTP, HTTP ou HTTPS. Cette valeur doit être comprise entre 30 et 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Reprises </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal de tentatives pour les connexions FTP, SFTP, HTTP ou HTTPS ayant échoué. Cette valeur doit être comprise entre 0 et 10. </p> <p>Une valeur nulle (0) empêche les tentatives de nouvelle tentative. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Encodage </p> </td> 
      <td colname="col2"> <p>Spécifie le système de codage de caractères utilisé dans le fichier de source de données spécifié. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Délimiteur </p> </td> 
      <td colname="col2"> <p>Indique le caractère à utiliser pour délimiter chaque champ du fichier de source de données spécifié. </p> <p>La virgule ( <span class="codeph"> , </span>) est un exemple de délimiteur. La virgule agit comme un délimiteur de champ qui permet de séparer les champs de données dans le fichier de source de données spécifié. </p> <p>Sélectionner un <span class="uicontrol"> onglet ? </span> pour utiliser le caractère de tabulation horizontale comme délimiteur. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>En-têtes de première ligne </p> </td> 
      <td colname="col2"> <p>Indique que la première ligne du fichier de source de données contient uniquement des informations d’en-tête et non des données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre minimum de documents pour l’indexation </p> </td> 
      <td colname="col2"> <p>S’il est défini sur une valeur positive, il indique le nombre minimum d’enregistrements attendus dans le fichier téléchargé. Si moins d’enregistrements sont reçus, l’opération d’index est abandonnée. </p> <p> <b>Remarque</b>: Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> <p> <b>Remarque</b>: Cette fonction est uniquement utilisée lors des opérations d’index complètes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Indique les mappages colonne/métadonnées, à l’aide des numéros de colonne. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Colonne </span> <p> Spécifie un numéro de colonne, la première colonne étant 1 (un). Pour ajouter de nouvelles lignes de mappage pour chaque colonne, sous <span class="wintitle"> Action </span>, cliquez sur <span class="uicontrol"> + </span>. </p> <p>Il n’est pas nécessaire de référencer chaque colonne de la source de données. Vous pouvez plutôt choisir d’ignorer les valeurs. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Champ </span> <p>Définit la valeur d’attribut name utilisée pour chaque balise &lt;meta&gt; générée. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> devient une liste déroulante </span> à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actuel. </p> <p>La <span class="uicontrol"> valeur </span> de champ peut être un champ de métadonnées non défini, le cas échéant. Un champ de métadonnées non défini est parfois utile pour créer le contenu utilisé par <span class="wintitle"> le script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> A propos du filtrage de script </a>. </p> <p>Lorsque Index Connector traite des documents XML avec plusieurs accès sur un champ de mappage, les valeurs multiples sont concaténées dans une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur de virgule. Cependant, supposons que la <span class="wintitle"> valeur de champ correspondante </span> soit un champ de métadonnées défini. En outre, ce champ a l’ <span class="wintitle"> attribut Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Clé primaire? </span> <p>Une seule définition de mappage est identifiée comme clé principale. Ce champ devient la référence unique présentée lorsque ce document est ajouté à l’index. Cette valeur est utilisée dans l’URL du document dans l’index. </p> <p>Les <span class="uicontrol"> valeurs de clé </span> principale doivent être uniques dans tous les documents représentés par la configuration du connecteur d’index. Les doublons rencontrés seront ignorés. Si vos documents source ne contiennent pas une seule valeur unique à utiliser comme clé <span class="uicontrol"> principale </span>, mais que deux ou plusieurs champs pris ensemble <i>peuvent</i> former un identifiant unique, vous pouvez définir la clé <span class="uicontrol"> principale </span> <span class="uicontrol"> en combinant plusieurs valeurs de  de colonnes avec une barre verticale ("|") délimitant les valeurs.</span> </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> Bande du code HTML ? </span> <p>Lorsque cette option est cochée, toutes les balises HTML trouvées dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Action </span> <p>Permet d’ajouter des lignes au mappage ou de supprimer des lignes du mappage. L’ordre des rangées n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Flux</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active l’analyse et l’index de la configuration. Vous pouvez également désactiver la configuration pour empêcher l’analyse et l’indexation. </p> <p> <b>Remarque</b>: Les configurations du connecteur d’index désactivées sont ignorées si elles figurent dans une liste de points d’entrée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse IP ou l’adresse URL du système hôte sur lequel le fichier de source de données est trouvé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML maître qui contient plusieurs "lignes" d’informations. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin de fichier incrémentiel </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML incrémentiel qui contient plusieurs "lignes" d’informations. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations d’index incrémentiel. Si aucun fichier n’est spécifié, le fichier répertorié sous Chemin du fichier est utilisé à la place. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin d’accès vertical au fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML qui contient plusieurs "lignes" d’informations éparses à utiliser lors d’une mise à jour verticale. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations de mise à jour verticale. </p> <p> <b>Remarque</b>: Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprime le chemin du fichier </p> </td> 
      <td colname="col2"> <p>Indique le chemin d’accès au fichier de texte aplati simple, contenant une seule valeur d’identificateur de document par ligne. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations d’index incrémentiel. Les valeurs trouvées dans ce fichier sont utilisées pour créer des requêtes "delete" afin de supprimer des documents indexés précédemment. Les valeurs de ce fichier doivent correspondre aux valeurs trouvées dans les fichiers Chemin d’accès au fichier complet ou incrémentiel, dans la colonne identifiée comme clé <span class="uicontrol"> principale </span>. </p> <p> <b>Remarque</b>: Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Spécifie le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Si nécessaire, vous pouvez entrer les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifie l’élément XML que vous pouvez utiliser pour identifier des lignes XML individuelles dans le fichier de source de données que vous avez spécifié. </p> <p>Par exemple, dans le fragment Flux suivant d’un document Adobe XML, la valeur Itemtag est <span class="codeph"> record </span>: </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt;&lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt;         &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt;         &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt;         &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre minimum de documents pour l’indexation </p> </td> 
      <td colname="col2"> <p>S’il est défini sur une valeur positive, il indique le nombre minimum d’enregistrements attendus dans le fichier téléchargé. Si moins d’enregistrements sont reçus, l’opération d’index est abandonnée. </p> <p> <b>Remarque</b>: Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> <p> <b>Remarque</b>: Cette fonction est uniquement utilisée lors des opérations d’index complètes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Permet de spécifier des mappages élément-élément-XML/métadonnées à l’aide d’expressions XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Baliser </span> <p>Spécifie une représentation XPath des données XML analysées. A l’aide de l’exemple de document XML Adobe ci-dessus, sous l’option Itemtag, il peut être mappé à l’aide de la syntaxe suivante : </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La syntaxe ci-dessus se traduit comme suit : </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>L’attribut <span class="codeph"> displayurl </span> de l’ <span class="codeph"> élément d’enregistrement </span> est mappé au champ de métadonnées <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans un élément de  d’enregistrement, dont l’attribut de nom est  titre , est associé au de titre du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans l’élément de  d’enregistrement, dont l’attribut de nom est  description , correspond au desc du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans l’élément de  d’enregistrement, dont l’attribut de nom est  description , correspond au de corps du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
      </ul> </p> <p>XPath est une notation relativement compliquée. Pour plus d’informations, consultez l’emplacement suivant : </p> <p>Voir <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Champ </span> <p>Définit la valeur d’attribut name utilisée pour chaque balise générée <span class="codeph"> &lt;meta&gt; </span> . </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> devient une liste déroulante </span> à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actuel. </p> <p>La <span class="uicontrol"> valeur </span> de champ peut être un champ de métadonnées non défini, le cas échéant. Un champ de métadonnées non défini est parfois utile pour créer le contenu utilisé par <span class="wintitle"> le script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> A propos du filtrage de script </a>. </p> <p>Lorsque Index Connector traite des documents XML avec plusieurs accès sur un champ de mappage, les valeurs multiples sont concaténées dans une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur de virgule. Cependant, supposons que la <span class="wintitle"> valeur de champ correspondante </span> soit un champ de métadonnées défini. En outre, ce champ a l’ <span class="wintitle"> attribut Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Clé primaire? </span> <p>Une seule définition de mappage est identifiée comme clé principale. Ce champ devient la référence unique présentée lorsque ce document est ajouté à l’index. Cette valeur est utilisée dans l’URL du document dans l’index. </p> <p>Les <span class="uicontrol"> valeurs de clé </span> principale doivent être uniques dans tous les documents représentés par la configuration du connecteur d’index. Les doublons rencontrés seront ignorés. Si vos documents source ne contiennent pas une seule valeur unique à utiliser comme clé <span class="uicontrol"> principale </span>, mais que deux ou plusieurs champs pris ensemble <i>peuvent</i> former un identifiant unique, vous pouvez définir la clé <span class="uicontrol"> principale </span> <span class="uicontrol"> en combinant plusieurs définitions de  de balises avec une barre verticale ("|") délimitant les valeurs.</span> </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> Bande du code HTML ? </span> <p>Lorsque cette option est cochée, toutes les balises HTML trouvées dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> Utiliser pour la suppression ? </span> <p>Utilisé uniquement pendant les opérations d’index incrémentiel. Les enregistrements correspondant à ce modèle XPath identifient les éléments à supprimer. La valeur de clé <span class="uicontrol"> principale </span> de chaque enregistrement de ce type est utilisée pour créer des requêtes de suppression, comme dans le cas de la suppression du chemin d’accès au fichier. </p> <p> <b>Remarque</b>: Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonction à utiliser. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Action </span> <p>Permet d’ajouter des lignes au mappage ou de supprimer des lignes du mappage. L’ordre des rangées n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active l’analyse et l’index de la configuration. Vous pouvez également désactiver la configuration pour empêcher l’analyse et l’indexation. </p> <p> <b>Remarque</b>: Les configurations du connecteur d’index désactivées sont ignorées si elles figurent dans une liste de points d’entrée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse URL du système hôte sur lequel le fichier de source de données est trouvé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML maître contenant des liens ( 
      <userinput>
        &lt;a&gt; 
      </userinput>) à des documents XML individuels. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Spécifie le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>Si nécessaire, vous pouvez entrer les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> Fichier </li> 
      </ul> </p> <p> <b>Remarque</b>: Le paramètre Protocole n’est utilisé que lorsque des informations sont spécifiées dans les champs Adresse hôte et/ou Chemin d’accès au fichier. Les documents XML individuels sont téléchargés à l’aide de HTTP ou HTTPS, conformément à leurs spécifications d’URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifie l’élément XML qui définit une "ligne" dans le fichier de source de données que vous avez spécifié. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Permet de spécifier des mappages colonne/métadonnées à l’aide des numéros de colonne. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> Baliser </span> <p>Spécifie une représentation XPath des données XML analysées. A l’aide de l’exemple de document XML Adobe ci-dessus, sous l’option Itemtag, vous pouvez le mapper à l’aide de la syntaxe suivante : </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La syntaxe ci-dessus se traduit comme suit : </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>L’attribut <span class="codeph"> displayurl </span> de l’ <span class="codeph"> élément d’enregistrement </span> est mappé au champ de métadonnées <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans un élément de  d’enregistrement, dont l’attribut de nom est  titre , est associé au de titre du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans l’élément de  d’enregistrement, dont l’attribut de nom est  description , correspond au desc du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans l’élément de  d’enregistrement, dont l’attribut de nom est  description , correspond au de corps du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
      </ul> </p> <p>XPath est une notation relativement compliquée. Pour plus d’informations, consultez l’emplacement suivant : </p> <p>Voir <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> Champ </span> <p>Définit la valeur d’attribut name utilisée pour chaque balise &lt;meta&gt; générée. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> devient une liste déroulante </span> à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actuel. </p> <p>La <span class="uicontrol"> valeur </span> de champ peut être un champ de métadonnées non défini, le cas échéant. Un champ de métadonnées non défini est parfois utile pour créer le contenu utilisé par <span class="wintitle"> le script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> A propos du filtrage de script </a>. </p> <p>Lorsque Index Connector traite des documents XML avec plusieurs accès sur un champ de mappage, les valeurs multiples sont concaténées dans une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur de virgule. Cependant, supposons que la <span class="wintitle"> valeur de champ correspondante </span> soit un champ de métadonnées défini. En outre, ce champ a l’ <span class="wintitle"> attribut Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> Clé primaire? </span> <p>Une seule définition de mappage est identifiée comme clé principale. Ce champ devient la référence unique présentée lorsque ce document est ajouté à l’index. Cette valeur est utilisée dans l’URL du document dans l’index. </p> <p>Les <span class="uicontrol"> valeurs de clé </span> principale doivent être uniques dans tous les documents représentés par la configuration du connecteur d’index. Les doublons rencontrés seront ignorés. Si vos documents source ne contiennent pas une seule valeur unique à utiliser comme clé <span class="uicontrol"> principale </span>, mais que deux ou plusieurs champs pris ensemble <i>peuvent</i> former un identifiant unique, vous pouvez définir la clé <span class="uicontrol"> principale </span> <span class="uicontrol"> en combinant plusieurs définitions de  de balises avec une barre verticale ("|") délimitant les valeurs.</span> </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> Bande du code HTML ? </span> <p>Lorsque cette option est cochée, toutes les balises HTML trouvées dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> Action </span> <p>Permet d’ajouter des lignes au mappage ou de supprimer des lignes du mappage. L’ordre des rangées n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Cliquez sur **[!UICONTROL Setup Maps]** pour télécharger un exemple de source de données. Les données sont examinées pour déterminer si l’indexation est appropriée. Cette fonctionnalité est disponible uniquement pour le texte et les types de flux.
1. (Facultatif) Cliquez sur **[!UICONTROL Preview]** pour tester le fonctionnement réel de la configuration. Cette fonctionnalité est disponible uniquement pour le texte et les types de flux.
1. Cliquez sur **[!UICONTROL Add]** pour ajouter la configuration à la [!DNL Index Connector Definitions] page et à la liste [!DNL Index Connector Configurations] déroulante de la [!DNL URL Entrypoints] page.

   Voir [A propos des points](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573)d’entrée d’URL.
1. Sur la [!DNL Index Connector Definitions] page, cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la [!DNL Index Connector Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une définition de connecteur d’index {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

Vous pouvez modifier un connecteur d’index existant que vous avez défini.

>[!NOTE]
>
>Vous ne pouvez pas modifier toutes les options, telles que Nom du connecteur d’index ou Type dans la liste [!DNL Type] déroulante.

**Pour modifier une définition du connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Dans la [!DNL Index Connector] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Edit]** sur le nom de définition d’un connecteur d’index dont vous souhaitez modifier les paramètres.
1. Sur la [!DNL Index Connector Edit] page, définissez les options de votre choix.

   Voir le tableau des options sous [Ajout d’une définition](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886)de connecteur d’index.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la [!DNL Index Connector Definitions] page, cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la [!DNL Index Connector Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Affichage des paramètres d’une définition de connecteur d’index {#task_D0B71A7426E54247BDB3468EC576D871}

Vous pouvez consulter les paramètres de configuration d’une définition de connecteur d’index existante.

Une fois la définition du connecteur d’index ajoutée à la [!DNL Index Connector Definitions] page, vous ne pouvez plus modifier son paramètre Type. Vous devez supprimer la définition, puis en ajouter une nouvelle.

**Pour afficher les paramètres d’une définition d’Index Connector**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la [!DNL Index Connector] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Edit]** sur le nom de définition d’un connecteur d’index dont vous souhaitez vérifier ou modifier les paramètres.

## Copie d’une définition de connecteur d’index {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

Vous pouvez copier une définition de Connecteur d’index existante pour l’utiliser comme base d’un nouveau Connecteur d’index que vous souhaitez créer.

Lors de la copie d’une définition du connecteur d’index, la définition copiée est désactivée par défaut. Pour activer ou &quot;activer&quot; la définition, vous devez la modifier à partir de la [!DNL Index Connector Edit] page, puis sélectionner **[!UICONTROL Enable]**.

Voir [Modification d’une définition](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9)du connecteur d’index.

**Pour copier une définition de Connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Dans la [!DNL Index Connector] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Copy]** sur le nom de définition d’un connecteur d’index dont vous souhaitez dupliquer les paramètres.
1. Sur la [!DNL Index Connector Copy] page, saisissez le nouveau nom de la définition.
1. Cliquez sur **[!UICONTROL Copy]**.
1. (Facultatif) Sur la [!DNL Index Connector Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Changement du nom d’une définition de connecteur d’index {#task_5132118FC21B47D99881E0ED425225D7}

Vous pouvez modifier le nom d’une définition de Connecteur d’index existante.

Après avoir renommé la définition, sélectionnez **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Vous souhaitez vous assurer que le nouveau nom de définition est reflété dans la liste déroulante de la [!DNL URL Entrypoints] page.

Voir [Ajout de plusieurs points d’entrée d’URL à indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

**Pour renommer une définition de Connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la [!DNL Index Connector] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Rename]** pour le nom de définition du connecteur d’index que vous souhaitez modifier.
1. Sur la [!DNL Index Connector Rename] page, saisissez le nouveau nom de la définition dans le [!DNL Name] champ.
1. Cliquez sur **[!UICONTROL Rename]**.
1. Cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Si le nom du connecteur d’index précédent figure dans la liste, supprimez-le et ajoutez l’entrée nouvellement renommée.

   Voir [Ajout de plusieurs points d’entrée d’URL à indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45). 1. (Facultatif) Sur la [!DNL Index Connector Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une définition de connecteur d’index {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

Vous pouvez supprimer une définition de Connecteur d’index existante dont vous n’avez plus besoin ni utilisée.

**Pour supprimer une définition de Connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la [!DNL Index Connector Definitions] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Delete]** pour le nom de définition du connecteur d’index à supprimer.
1. Sur la [!DNL Index Connector Delete] page, cliquez sur **[!UICONTROL Delete]**.