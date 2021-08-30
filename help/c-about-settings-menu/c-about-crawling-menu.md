---
description: Utilisez le menu Analyse pour définir des masques de date et d’URL, des mots de passe, des types de contenu, des connexions, des définitions de formulaire et des points d’entrée d’URL.
solution: Target
subtopic: Crawling
title: À propos du menu Analyse
topic-legacy: Settings,Site search and merchandising
uuid: a58c03bf-90f7-4b5b-91ff-988b95c246b0
exl-id: 22dbbc30-bf1c-4d51-8fb0-708115ba844b
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '11015'
ht-degree: 1%

---

# À propos du menu Analyse{#about-the-crawling-menu}

Utilisez le menu Analyse pour définir des masques de date et d’URL, des mots de passe, des types de contenu, des connexions, des définitions de formulaire et des points d’entrée d’URL.

## À propos des points de fin d’URL {#concept_5D857E3B5C124E85BC0B5AE77A509573}

La plupart des sites web ont un point d’entrée ou une page d’accueil Principal qu’un client visite initialement. Ce point d’entrée principal est l’adresse URL à partir de laquelle le robot de recherche commence l’analyse de l’index. Cependant, si votre site web comporte plusieurs domaines ou sous-domaines, ou si des parties de votre site ne sont pas liées à partir du point d’entrée Principal, vous pouvez utiliser des points de fin d’URL pour ajouter d’autres points d’entrée.

Toutes les pages de site web situées sous chaque point d’entrée d’URL spécifié sont indexées. Vous pouvez combiner des points d’entrée d’URL avec des masques pour contrôler exactement les parties d’un site web que vous souhaitez indexer. Vous devez recréer l’index de votre site web avant que les effets des paramètres de points d’entrée d’URL ne soient visibles par les clients.

Le point d’entrée principal est généralement l’URL du site web que vous souhaitez indexer et rechercher. Vous configurez ce point d’entrée principal dans Paramètres du compte.

Voir [Configuration des paramètres de votre compte](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Après avoir spécifié le point d’entrée de l’URL principale, vous pouvez éventuellement spécifier des points d’entrée supplémentaires que vous souhaitez analyser dans l’ordre. La plupart du temps, vous spécifiez des points d’entrée supplémentaires pour les pages web qui ne sont pas liées à partir des pages sous le point d’entrée principal. Spécifiez des points d’entrée supplémentaires lorsque votre site web s’étend sur plusieurs domaines, comme dans l’exemple suivant :

`https://www.domain.com/`

`https://www.domain.com/not_linked/but_search_me_too/`

`https://more.domain.com/`

Vous qualifiez chaque point d’entrée avec un ou plusieurs des mots-clés séparés par des espaces dans le tableau ci-dessous. Ces mots-clés affectent la manière dont la page est indexée.

**Important** : Veillez à séparer un mot-clé donné du point d’entrée et l’un de l’autre par un espace ; une virgule n’est pas un séparateur valide.

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
     <code>
       noindex 
     </code> après le point d’entrée. </p> <p>Séparez le mot-clé du point d’entrée par un espace, comme dans l’exemple suivant : </p> <p> <code> https://www.my-additional-domain.com/more_pages/main.html&amp;nbsp;noindex </code> </p> <p>Ce mot-clé équivaut à une balise meta de robots avec 
     <code>
       content="noindex" 
     </code>) entre les 
     <code>
       &lt;head&gt; 
     </code>... 
     Balises <code>
       &lt;/head&gt; 
     </code> de la page du point d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noFollow </p> </td> 
   <td colname="col2"> <p> Si vous souhaitez indexer le texte dans la page du point d’entrée mais que vous ne souhaitez pas suivre les liens de la page, ajoutez 
     <code>
       nofollow 
     </code> après le point d’entrée. </p> <p>Séparez le mot-clé du point d’entrée par un espace, comme dans l’exemple suivant : </p> <p> <code> https://www.domain.com/not_linked/directory_listing&amp;nbsp;nofollow </code> </p> <p>Ce mot-clé équivaut à une balise meta de robots avec 
     <code>
       content="nofollow" 
     </code> entre les 
     <code>
       &lt;head&gt; 
     </code>... 
     Balise <code>
       &lt;/head&gt; 
     </code> d’une page de point d’entrée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>formulaire </p> </td> 
   <td colname="col2"> <p> Lorsque le point d’entrée est une page de connexion, 
     <code>
       form 
     </code> est généralement utilisé afin que le robot de recherche puisse envoyer le formulaire de connexion et recevoir les cookies appropriés avant d’analyser le site web. Lorsque le mot-clé "formulaire" est utilisé, la page du point d’entrée n’est pas indexée et le robot de recherche ne marque pas la page du point d’entrée comme étant analysée. Utilisation 
     <code>
       nofollow 
     </code> si vous ne souhaitez pas que le robot de recherche suive les liens de la page. </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [À propos des types de contenu](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

Voir aussi [À propos du connecteur d’index](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84).

## Ajout de plusieurs points d’entrée d’URL que vous souhaitez indexer {#task_2338A47387D74CFDAC4D4EF4A367ED45}

Si votre site web comporte plusieurs domaines ou sous-domaines et que vous souhaitez les analyser, vous pouvez utiliser des points de saisie d’URL pour ajouter d’autres URL.

Pour définir le point d’entrée de l’URL principale de votre site web, utilisez Paramètres du compte.

Voir [Configuration des paramètres de votre compte](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

**Pour ajouter plusieurs points d’entrée d’URL que vous souhaitez indexer**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**.
1. Sur la page [!DNL URL Entrypoints], dans le champ [!DNL Entrypoints], saisissez une adresse URL par ligne.
1. (Facultatif) Dans la liste déroulante **[!UICONTROL Add Index Connector Configurations]**, sélectionnez un connecteur d’index à ajouter en tant que point d’entrée pour l’indexation.

   La liste déroulante n’est disponible que si vous avez déjà ajouté une ou plusieurs définitions de connecteur d’index.

   ![](assets/url_entrypoints_index_connector.png)

   Voir [Ajout d’une définition de connecteur d’index](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des modèles d’URL {#concept_8039DFC53FF3410AA494D602F71BA164}

Les masques d’URL sont des modèles qui déterminent quels documents de votre site web sont indexés ou non par le robot de recherche.

Veillez à reconstruire l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Vous trouverez ci-dessous deux types de masques d’URL que vous pouvez utiliser :

* Inclure des masques d’URL
* Exclure les masques d’URL

Inclure des masques d’URL indique au robot de recherche d’indexer tout document correspondant au modèle du masque.

Exclure les masques d’URL indique au robot de recherche d’indexer les documents correspondants.

Alors que le robot de recherche voyage d’un lien à l’autre à travers votre site web, il rencontre des URL et recherche des masques correspondant à ces URL. La première correspondance détermine s’il faut inclure ou exclure cette URL de l’index. Si aucun masque ne correspond à une URL rencontrée, cette URL est ignorée de l’index.

Des masques d’URL d’inclusion pour vos URL de point d’entrée sont automatiquement générés. Ce comportement garantit que tous les documents rencontrés sur votre site web sont indexés. Il supprime aussi facilement les liens qui &quot;quittent&quot; votre site web. Par exemple, si une page indexée renvoie vers https://www.yahoo.com, le robot de recherche n’indexe pas cette URL, car elle ne correspond pas au masque d’inclusion généré automatiquement par l’URL du point d’entrée.

Chaque masque d’URL que vous spécifiez doit se trouver sur une ligne distincte.

Le masque peut spécifier l’une des options suivantes :

* Chemin complet comme dans `https://www.mydomain.com/products.html`.
* Chemin partiel comme dans `https://www.mydomain.com/products`.
* URL qui utilise des caractères génériques comme dans `https://www.mydomain.com/*.html`.
* Expression régulière (pour les utilisateurs avancés).

   Pour faire d&#39;un masque une expression régulière, insérez le mot-clé `regexp` entre le type de masque ( `exclude` ou `include`) et le masque d&#39;URL.

Voici un exemple simple de masque d’URL d’exclusion :

```
exclude https://www.mydomain.com/photos
```

Comme cet exemple est un masque d’URL d’exclusion, tout document correspondant au modèle n’est pas indexé. Le modèle correspond à tous les éléments rencontrés, fichiers et dossiers, de sorte que `https://www.mydomain.com/photos.html` et `https://www.mydomain.com/photos/index.html`, qui correspondent tous deux à l’URL d’exclusion, ne soient pas indexés. Pour ne faire correspondre que les fichiers du dossier `/photos/`, le masque d&#39;URL doit contenir une barre oblique comme dans l&#39;exemple suivant :

```
exclude https://www.mydomain.com/photos/
```

L’exemple de masque d’exclusion suivant utilise un caractère générique. Il indique au robot de recherche d’ignorer les fichiers avec l’extension &quot;.pdf&quot;. Le robot de recherche n’ajoute pas ces fichiers à votre index.

```
exclude *.pdf
```

Un simple masque d’URL d’inclusion est le suivant :

```
include https://www.mydomain.com/news/
```

Seuls les documents liés par une série de liens à partir d’un point d’entrée d’URL ou utilisés comme point d’entrée d’URL sont indexés. La simple inscription de l’URL d’un document en tant que masque d’URL d’inclusion n’indexe pas un document non lié. Pour ajouter des documents non liés à votre index, vous pouvez utiliser la fonction Points d’entrée d’URL .

Voir [À propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Les masques d’inclusion et d’exclusion peuvent fonctionner ensemble. Vous pouvez exclure une grande partie de votre site web de l’indexation en créant un masque d’URL d’exclusion tout en incluant une ou plusieurs des pages exclues avec un masque d’URL d’inclusion. Supposons, par exemple, que votre URL de point d’entrée soit la suivante :

```
https://www.mydomain.com/photos/
```

Le robot de recherche analyse et indexe toutes les pages sous `/photos/summer/`, `/photos/spring/` et `/photos/fall/` (en supposant qu’il existe des liens vers au moins une page dans chaque répertoire à partir du dossier `photos`). Ce comportement se produit car les chemins de lien permettent au robot de recherche de trouver les documents dans les dossiers `/summer/`, `/spring/` et `/fall/`, ainsi que les URL de dossier correspondant au masque d’inclusion automatiquement généré par l’URL du point d’entrée.

Vous pouvez choisir d&#39;exclure toutes les pages du dossier `/fall/` avec un masque d&#39;URL d&#39;exclusion, comme dans l&#39;exemple suivant :

```
exclude https://www.mydomain.com/photos/fall/
```

Vous pouvez également inclure uniquement `/photos/fall/redleaves4.html` dans l’index avec le masque d’URL suivant :

```
include https://www.mydomain.com/photos/fall/redleaves4.html
```

Pour que les deux exemples de masque ci-dessus fonctionnent comme prévu, le masque d&#39;inclusion est répertorié en premier, comme dans l&#39;exemple suivant :

```
include https://www.mydomain.com/photos/fall/redleaves4.html 
exclude https://www.mydomain.com/photos/fall/
```

Étant donné que le robot de recherche suit les instructions dans l’ordre dans lequel elles sont répertoriées, le robot de recherche commence par inclure `/photos/fall/redleaves4.html`, puis exclut le reste des fichiers du dossier `/fall`.

Si les instructions sont spécifiées de la manière inverse, comme dans l’exemple suivant :

```
exclude https://www.mydomain.com/photos/fall/ 
include https://www.mydomain.com/photos/fall/redleaves4.html
```

`/photos/fall/redleaves4.html` n’est pas inclus, même si le masque indique qu’il est inclus.

Un masque d’URL qui apparaît en premier est toujours prioritaire par rapport à un masque d’URL qui apparaît ultérieurement dans les paramètres du masque. De plus, si le robot de recherche rencontre une page correspondant à un masque d’URL d’inclusion et un masque d’URL d’exclusion, le masque qui est répertorié en premier est toujours prioritaire.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## À propos de l’utilisation de mots-clés avec des masques d’URL {#section_7609A7A6D79B482ABCA8900886541AAB}

Vous pouvez qualifier chaque masque d’inclusion avec un ou plusieurs mots-clés séparés par des espaces, ce qui affecte la manière dont les pages correspondantes sont indexées.

Une virgule n’est pas valide comme séparateur entre le masque et le mot-clé ; vous ne pouvez utiliser que des espaces.

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
     <code>
       noindex 
     </code> après le masque d’URL d’inclusion. Veillez à séparer le mot-clé du masque avec un espace, comme dans l'exemple suivant : </p> <p> <code> include&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>L’exemple ci-dessus indique que le robot de recherche suit tous les liens des fichiers avec la variable 
     Extension <code>
       .swf 
     </code>, mais désactive l’indexation de tout le texte contenu dans ces fichiers. </p> <p>Le 
     Le mot-clé <code>
       noindex 
     </code> équivaut à une balise méta-robot avec 
     <code>
       content="noindex" 
     </code> entre la variable 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> balises des pages correspondantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noFollow </p> </td> 
   <td colname="col2"> <p> Si vous souhaitez indexer le texte sur les pages qui correspondent au masque d’URL, mais que vous ne souhaitez pas suivre les liens de la page correspondante, ajoutez 
     <code>
       nofollow 
     </code> après le masque d’URL d’inclusion. Veillez à séparer le mot-clé du masque avec un espace, comme dans l'exemple suivant : </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Le 
     Le mot-clé <code>
       nofollow 
     </code> équivaut à une balise méta-robot avec 
     <code>
       content="nofollow" 
     </code> entre la variable 
     <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> balises des pages correspondantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p>Utilisé pour inclure et exclure des masques. </p> <p>Tout masque d’URL précédé de 
     <code>
       regexp 
     </code> est traité comme une expression régulière. Si le robot de recherche rencontre des documents qui correspondent à un masque URL d’expression régulière d’exclusion, ces documents ne sont pas indexés. Si le robot de recherche rencontre des documents qui correspondent à un masque URL d’expression régulière inclus, ces documents sont indexés. Supposons, par exemple, que vous ayez le masque d’URL suivant : </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*/products/.*\.html$ </code> </p> <p>Le robot de recherche exclut les fichiers correspondants, tels que 
     <code>
       https://www.mydomain.com/products/page1.html 
     </code> </p> <p>Si vous aviez le masque d’URL d’expression régulière d’exclusion suivant : </p> <p> <code> exclude&amp;nbsp;regexp&amp;nbsp;^.*\?..*$ </code> </p> <p>Le robot de recherche ne doit pas inclure d’URL contenant un paramètre CGI tel que 
     <code>
       https://www.mydomain.com/cgi/prog/?arg1=val1&amp;arg2=val2 
     </code>. </p> <p>Si vous aviez le masque d’URL d’expression régulière suivant : </p> <p> <code> include&amp;nbsp;regexp&amp;nbsp;^.*\.swf$&amp;nbsp;noindex </code> </p> <p>Le robot de recherche suit tous les liens des fichiers avec l’extension ".swf". Le 
     Le mot-clé <code>
       noindex 
     </code> indique également que le texte des fichiers correspondants n’est pas indexé. </p> <p>Voir <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ajout de masques d’URL pour indexer ou non les parties de votre site web {#task_E1AFC17C746048B8843013D979E082C1}

Vous pouvez utiliser [!DNL URL Masks] pour définir les parties de votre site web que vous souhaitez ou ne souhaitez pas analyser et indexer.

Utilisez le champ Tester les masques d’URL pour tester si un document est inclus ou non après l’indexation.

Veillez à reconstruire l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Ajout de masques d’URL pour indexer ou non des parties de votre site web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**.
1. (Facultatif) Sur la page [!DNL URL Masks], dans le champ **[!UICONTROL Test URL Masks]**, saisissez un masque d’URL de test sur votre site web, puis cliquez sur **[!UICONTROL Test]**.
1. Dans le champ [!DNL URL Masks] , saisissez `include` (pour ajouter un site web à analyser et indexer) ou `exclude` (pour empêcher l’analyse et l’indexation d’un site web), suivi de l’adresse du masque d’URL.

   Saisissez une adresse de masque URL par ligne. Exemple :

   ```
   include https://www.mycompany.com/summer 
   include https://www.mycompany.com/spring 
   exclude regexp .*\.xml 
   exclude https://www.mycompany.com/fall
   ```

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des masques de date {#concept_F4F1F58A646F4A86B8650EC46FDCEF66}

Vous pouvez utiliser des masques de date pour inclure ou exclure des fichiers de vos résultats de recherche en fonction de l’âge du fichier.

Veillez à reconstruire l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Vous trouverez ci-dessous deux types de masques de date que vous pouvez utiliser :

* Inclure les masques de date (&quot;include-days&quot; et &quot;include-date&quot;)

   Incluez les fichiers d’index de masques de date datant le ou avant la date spécifiée.
* Exclure les masques de date (&quot;exclude-days&quot; et &quot;exclude-date&quot;)

   Exclure les fichiers d’index de masques de date datant le ou avant la date spécifiée.

Par défaut, la date du fichier est déterminée à partir des informations de la balise META. Si aucune balise Meta n’est trouvée, la date d’un fichier est déterminée à partir de l’en-tête HTTP reçu du serveur lorsque le robot de recherche télécharge un fichier.

Chaque masque de date que vous indiquez doit se trouver sur une ligne distincte.

Le masque peut spécifier l’une des options suivantes :

* Un chemin complet comme dans `https://www.mydomain.com/products.html`
* Un chemin partiel comme dans `https://www.mydomain.com/products`
* Une URL qui utilise des caractères génériques `https://www.mydomain.com/*.html`
* Une expression régulière. Pour faire d&#39;un masque une expression régulière, insérez le mot-clé `regexp` devant l&#39;URL.

Les masques de date d’inclusion et d’exclusion peuvent tous deux spécifier une date de l’une des deux manières suivantes. Les masques ne sont appliqués que si les fichiers correspondants ont été créés à la date spécifiée ou avant :

1. Nombre de jours. Supposons, par exemple, que votre masque de date soit le suivant :

   ```
   exclude-days 30 https://www.mydomain.com/docs/archive/)
   ```

   Le nombre de jours spécifiés est recompté. Si le fichier est daté le ou avant la date d’arrivée, le masque est appliqué.

1. Date réelle au format AAAA-MM-JJ. Supposons, par exemple, que votre masque de date soit le suivant :

   ```
   include-date 2011-02-15 https://www.mydomain.com/docs/archive/)
   ```

   Si le document correspondant est daté le ou avant la date spécifiée, le masque de date est appliqué.

Voici un exemple simple de masque de date d&#39;exclusion :

```
exclude-days 90 https://www.mydomain.com/docs/archive
```

Puisqu’il s’agit d’un masque de date d’exclusion, tout fichier correspondant au modèle n’est pas indexé et a 90 jours ou plus. Lorsque vous excluez un document, aucun texte n’est indexé et aucun lien n’est suivi à partir de ce fichier. Le fichier est en fait ignoré. Dans cet exemple, les fichiers et les dossiers peuvent correspondre au modèle d’URL spécifié. Notez que `https://www.mydomain.com/docs/archive.html` et `https://www.mydomain.com/docs/archive/index.html` correspondent tous deux au modèle et ne sont pas indexés s’ils ont 90 jours ou plus. Pour ne faire correspondre que les fichiers du dossier `/docs/archive/`, le masque de date doit contenir une barre oblique comme dans l&#39;exemple suivant :

```
exclude-days 90 https://www.mydomain.com/docs/archive/
```

Les masques de date peuvent également être utilisés avec des caractères génériques. Le masque d’exclusion suivant indique au robot de recherche d’ignorer les fichiers avec l’extension &quot;.pdf&quot; dont la date est antérieure ou antérieure au 2011-02-15. Le robot de recherche n’ajoute aucun fichier correspondant à votre index.

```
exclude-date 2011-02-15 *.pdf
```

Le masque de date d’inclusion ressemble à cela. Seuls les fichiers correspondants sont ajoutés à l’index. L’exemple suivant indique au robot de recherche d’indexer le texte à partir de n’importe quel fichier de zéro jour ou plus dans la zone `/docs/archive/manual/` du site web.

```
include-days 0 https://www.mydomain.com/docs/archive/manual/
```

Les masques d’inclusion et d’exclusion peuvent fonctionner ensemble. Par exemple, vous pouvez exclure une grande partie de votre site web de l’indexation en créant un masque de date d’exclusion tout en incluant une ou plusieurs des pages exclues avec un masque d’URL d’inclusion. Si l’URL de votre point d’entrée est la suivante :

```
https://www.mydomain.com/archive/
```

Le robot de recherche analyse et indexe toutes les pages sous `/archive/summer/`, `/archive/spring/` et `/archive/fall/` (en supposant qu’il existe des liens vers au moins une page dans chaque dossier à partir du dossier `archive`). Ce comportement se produit car les chemins d’accès aux liens permettent au robot de recherche de &quot;trouver&quot; les fichiers dans les dossiers `/summer/`, `/spring/` et `/fall/` et les URL de dossier correspondent au masque d’inclusion automatiquement généré par l’URL du point d’entrée.

Voir [À propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Voir [Configuration des paramètres de votre compte](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Vous pouvez choisir d&#39;exclure toutes les pages de plus de 90 jours dans le dossier `/fall/` avec un masque de date d&#39;exclusion, comme dans l&#39;exemple suivant :

```
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Vous pouvez inclure de manière sélective uniquement `/archive/fall/index.html` (quel que soit l’âge, tous les fichiers de 0 jour ou plus sont associés) dans l’index avec le masque de date suivant :

```
include-days 0 https://www.mydomain.com/archive/fall/index.html
```

Pour que les deux exemples de masque ci-dessus fonctionnent comme prévu, vous devez d&#39;abord répertorier le masque d&#39;inclusion comme dans l&#39;exemple suivant :

```
include-days 0 https://www.mydomain.com/archive/fall/index.html 
exclude-days 90 https://www.mydomain.com/archive/fall/
```

Étant donné que le robot de recherche suit les instructions dans l’ordre spécifié, le robot de recherche commence par inclure `/archive/fall/index.html`, puis exclut le reste des fichiers du dossier `/fall`.

Si les instructions sont spécifiées de la manière inverse, comme dans l’exemple suivant :

```
exclude-days 90 https://www.mydomain.com/archive/fall/ 
include-days 0 https://www.mydomain.com/archive/fall/index.html 
```

`/archive/fall/index.html` n’est pas inclus, même si le masque indique qu’il doit l’être. Un masque de date qui s’affiche en premier est toujours prioritaire par rapport à un masque de date qui peut apparaître plus tard dans les paramètres du masque. De plus, si le robot de recherche rencontre une page qui correspond à la fois à un masque de date d’inclusion et à un masque de date d’exclusion, le masque qui est répertorié en premier est toujours prioritaire.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## À propos de l’utilisation de mots-clés avec des masques de date {#section_CCBB3E3FDBDE4725B2B571FD6594470C}

Vous pouvez qualifier chaque masque d’inclusion avec un ou plusieurs mots-clés séparés par des espaces, ce qui affecte la manière dont les pages correspondantes sont indexées.

Une virgule n’est pas valide comme séparateur entre le masque et le mot-clé ; vous ne pouvez utiliser que des espaces.

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
   <td colname="col2"> <p> Si vous ne souhaitez pas indexer le texte sur les pages datées le ou avant la date spécifiée par le masque d’inclusion, ajoutez 
     <code>
       noindex 
     </code> après le masque de date d’inclusion comme dans l’exemple suivant : </p> <p> <code> include-days&amp;nbsp;10&amp;nbsp;*.swf&amp;nbsp;noindex </code> </p> <p>Veillez à séparer le mot-clé du masque par un espace. </p> <p>L’exemple ci-dessus indique que le robot de recherche suit tous les liens des fichiers avec l’extension ".swf" qui ont 10 jours ou plus. Cependant, il désactive l’indexation de tout le texte contenu dans ces fichiers. </p> <p>Vous pouvez vous assurer que le texte des fichiers plus anciens n’est pas indexé, tout en suivant tous les liens de ces fichiers. Dans ce cas, utilisez un masque de date d’inclusion avec le mot-clé "noindex" au lieu d’utiliser un masque de date d’exclusion. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>noFollow </p> </td> 
   <td colname="col2"> <p> Si vous souhaitez indexer le texte sur les pages dont la date est antérieure ou égale à la date spécifiée par le masque d’inclusion, mais que vous ne souhaitez pas suivre les liens de la page correspondante, ajoutez 
     <code>
       nofollow 
     </code> après le masque de date d’inclusion comme dans l’exemple suivant : </p> <p> <code> include-days&amp;nbsp;8&amp;nbsp;https://www.mydomain.com/photos&amp;nbsp;nofollow </code> </p> <p>Veillez à séparer le mot-clé du masque par un espace. </p> <p>Le 
     Le mot-clé <code>
       nofollow 
     </code> équivaut à une balise méta-robot avec 
     <code>
       content="nofollow" 
     </code> entre la variable 
     Balise <code>
       &lt;head&gt;...&lt;/head&gt; 
     </code> des pages correspondantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>server-date </p> </td> 
   <td colname="col2"> <p>Utilisé pour inclure et exclure des masques. </p> <p>Le robot de recherche télécharge et analyse généralement chaque fichier avant de vérifier les masques de date. Ce comportement se produit car certains types de fichiers peuvent spécifier une date dans le fichier lui-même. Par exemple, un document HTML peut inclure des méta-balises qui définissent la date du fichier. </p> <p>Si vous allez exclure de nombreux fichiers en fonction de leur date et que vous ne souhaitez pas placer de charge inutile sur vos serveurs, vous pouvez utiliser 
     <code>
       server-date 
     </code> après l’URL dans le masque de date. </p> <p>Ce mot-clé indique au robot de recherche de faire confiance à la date du fichier renvoyé par votre serveur au lieu d’analyser chaque fichier. Par exemple, le masque de date d’exclusion suivant ignore les pages qui correspondent à l’URL si les documents ont plus de 90 jours, selon la date renvoyée par le serveur dans les en-têtes HTTP : </p> <p> <code> exclude-days&amp;nbsp;90&amp;nbsp;https://www.mydomain.com/docs/archive&amp;nbsp;server-date </code> </p> <p> Si la date renvoyée par le serveur est antérieure de 90 jours ou plus, 
     <code>
       server-date 
     </code> indique que les documents exclus ne doivent pas être téléchargés depuis votre serveur. Cela se traduit par une indexation plus rapide de vos documents et une charge réduite placée sur vos serveurs. If 
     <code>
       server-date 
     </code> n’est pas spécifié, le robot de recherche ignore la date renvoyée par le serveur dans les en-têtes HTTP. Au lieu de cela, chaque fichier est téléchargé et vérifié pour voir si la date est spécifiée. Si aucune date n’est spécifiée dans le fichier, le robot de recherche utilise la date renvoyée par le serveur. </p> <p>Vous ne devez pas utiliser 
     <code>
       server-date 
     </code> si vos fichiers contiennent des commandes qui remplacent la date du serveur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>regexp </p> </td> 
   <td colname="col2"> <p> Utilisez pour inclure et exclure des masques. </p> <p>Tout masque de date précédé de 
     <code>
       regexp 
     </code> est traité comme une expression régulière. </p> <p>Si le robot de recherche rencontre des fichiers correspondant à un masque de date d’expression régulière exclu, il n’indexe pas ces fichiers. </p> <p>Si le robot de recherche rencontre des fichiers correspondant à un masque de date d’expression régulière inclus, il indexe ces documents. </p> <p>Supposons, par exemple, que vous ayez le masque de date suivant : </p> <p> <code> exclude-days&amp;nbsp;180&amp;nbsp;regexp&amp;nbsp;.*archive.* </code> </p> <p>Le masque indique au robot de recherche d'exclure les fichiers correspondants de 180 jours ou plus. En d’autres termes, les fichiers contenant le mot "archive" dans leur URL. </p> <p>Voir <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Ajout de masques de date pour indexer ou non les parties de votre site web {#task_0010543C55F648D2B5DEFEFAD60FAF04}

Vous pouvez utiliser des masques de date pour inclure ou exclure des fichiers des résultats de recherche des clients en fonction de l’âge des fichiers.

Utilisez les champs **[!UICONTROL Test Date]** et **[!UICONTROL Test URL]** pour tester si un fichier est ou n’est pas inclus après l’index.

Veillez à reconstruire l’index de votre site afin que les résultats de vos masques d’URL soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Pour ajouter des masques de date à l’index ou non des parties de votre site web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Date Masks]**.
1. (Facultatif) Sur la page [!DNL Date Masks], dans le champ **[!UICONTROL Test Date]**, saisissez une date au format AAAA-MM-JJ (par exemple, `2011-07-25`). dans le champ **[!UICONTROL Test URL]** , saisissez un masque URL de votre site web, puis cliquez sur **[!UICONTROL Test]**.
1. Dans le champ [!DNL Date Masks] , saisissez une adresse de masque de date par ligne.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des mots de passe {#concept_3EDBD731725D46B891F834D4472774DC}

Pour accéder à des parties de votre site web protégées par l’authentification HTTP de base, vous pouvez ajouter un ou plusieurs mots de passe.

Avant que les effets des paramètres Mot de passe ne soient visibles par les clients, vous devez reconstruire l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Sur la page [!DNL Passwords], saisissez chaque mot de passe sur une seule ligne. Le mot de passe se compose d’une URL ou d’un domaine, d’un nom d’utilisateur et d’un mot de passe, comme dans l’exemple suivant :

```
https://www.mydomain.com/ myname mypassword
```

Au lieu d’utiliser un chemin d’URL, comme ci-dessus, vous pouvez également spécifier un domaine.

Pour déterminer le domaine correct à utiliser, ouvrez une page web protégée par un mot de passe avec un navigateur et examinez la boîte de dialogue &quot;Saisir le mot de passe réseau&quot;.

![](assets/realms.gif)

Dans ce cas, le nom du domaine est &quot;Mon domaine du site&quot;.

En utilisant le nom de domaine ci-dessus, votre mot de passe peut se présenter comme suit :

```
My Site Realm myusername mypassword
```

Si votre site web comporte plusieurs domaines, vous pouvez créer plusieurs mots de passe en saisissant un nom d’utilisateur et un mot de passe pour chaque domaine sur une ligne distincte, comme dans l’exemple suivant :

```
Realm1 name1 password1 
Realm2 name2 password2 
Realm3 name3 password3
```

Vous pouvez mélanger des mots de passe qui contiennent des URL ou des domaines afin que votre liste de mots de passe puisse se présenter comme suit :

```
Realm1 name1 password1 
https://www.mysite.com/path1/path2 name2 password2 
Realm3 name3 password3 
Realm4 name4 password4 
https://www.mysite.com/path1/path5 name5 password5 
https://www.mysite.com/path6 name6 password6
```

Dans la liste ci-dessus, le premier mot de passe est utilisé et contient un domaine ou une URL correspondant à la demande d’authentification du serveur. Même si le fichier à `https://www.mysite.com/path1/path2/index.html` se trouve dans `Realm3`, par exemple, `name2` et `password2` sont utilisés, car le mot de passe défini avec l’URL est répertorié au-dessus de celui défini avec le domaine.

## Ajout de mots de passe pour accéder aux zones de votre site web nécessitant une authentification {#task_DED19D476FF04B48BB6456D5ECB8628A}

Vous pouvez utiliser des mots de passe pour accéder aux zones protégées par mot de passe de votre site web à des fins d’analyse et d’indexation.

Avant que les effets de votre mot de passe ne soient visibles par les clients, veillez à reconstruire l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Ajout de mots de passe pour accéder aux zones de votre site web nécessitant une authentification**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Passwords]**.
1. Sur la page [!DNL Passwords], dans le champ **[!UICONTROL Passwords]**, saisissez un domaine ou une URL, ainsi que son nom d’utilisateur et son mot de passe associés, séparés par un espace.

   Exemple de mot de passe de domaine et de mot de passe URL sur des lignes distinctes :

   ```
   Realm1 name1 password1 
   https://www.mysite.com/path1/path2 name2 password2
   ```

   Ajoutez uniquement un mot de passe par ligne.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des types de contenu {#concept_6FEA1355C0374500B4C53090C34A8A07}

Vous pouvez utiliser [!DNL Content Types] pour sélectionner les types de fichiers à analyser et à indexer pour ce compte.

Les types de contenu que vous pouvez choisir d’analyser et d’indexer incluent des documents PDF, des documents texte, des films de Flash d’Adobe, des fichiers provenant d’applications Microsoft Office telles que Word, Excel et PowerPoint et du texte dans des fichiers MP3. Le texte qui se trouve dans les types de contenu sélectionnés est recherché avec le reste du texte de votre site web.

Avant que les effets des paramètres Types de contenu ne soient visibles par les clients, vous devez reconstruire l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

## A propos de l&#39;indexation des fichiers de musique MP3 {#section_AD2E28BEEE3E46629E2B05C34A963673}

Si vous sélectionnez l’option **[!UICONTROL Text in MP3 Music Files]** sur la page [!DNL Content Types], un fichier MP3 est analysé et indexé de deux façons. La première méthode, la plus courante, consiste à utiliser une balise href d’ancrage dans un fichier HTML, comme dans l’exemple suivant :

```
<a href="MP3-file-URL"></a>
```

La deuxième méthode consiste à saisir l’URL du fichier MP3 en tant que point d’entrée d’URL.

Voir [À propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

Un fichier MP3 est reconnu par son type MIME &quot;audio/mpeg&quot;.

Gardez à l’esprit que les fichiers de musique MP3 peuvent être très volumineux, même s’ils ne contiennent généralement qu’une petite quantité de texte. Par exemple, les fichiers MP3 peuvent éventuellement stocker des éléments tels que le nom de l’album, le nom de l’artiste, le titre de la chanson, le genre de la chanson, l’année de publication et un commentaire. Ces informations sont stockées à la fin du fichier dans ce qui est appelé la balise . Les fichiers MP3 contenant des informations TAG sont indexés de la manière suivante :

* Le titre de la chanson est traité comme le titre d’une page HTML.
* Le commentaire est traité comme une description définie pour une page HTML.
* Le genre est traité comme un mot-clé défini pour une page HTML.
* Le nom de l’artiste, le nom de l’album et l’année de publication sont traités comme le corps d’une page HTML.

Notez que chaque fichier MP3 analysé et indexé sur votre site web compte comme une page.

Si votre site web contient de nombreux fichiers MP3 volumineux, vous pouvez dépasser la limite d’octets d’indexation de votre compte. Si cela se produit, vous pouvez désélectionner **[!UICONTROL Text in MP3 Music Files]** sur la page [!DNL Content Types] afin d’empêcher l’indexation de tous les fichiers MP3 de votre site web.

Si vous souhaitez uniquement empêcher l’indexation de certains fichiers MP3 sur votre site web, vous pouvez effectuer l’une des opérations suivantes :

* Entourez les balises d’ancrage qui se lient aux fichiers MP3 avec les balises `<nofollow>` et `</nofollow>`. Le robot de recherche ne suit pas les liens entre ces balises.

* Ajoutez les URL des fichiers MP3 en tant que masques d’exclusion.

   Voir [À propos des masques d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

## Sélection des types de contenu à analyser et à indexer {#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8}

Vous pouvez utiliser [!DNL Content Types] pour sélectionner les types de fichiers à analyser et à indexer pour ce compte.

Les types de contenu que vous pouvez choisir d’analyser et d’indexer incluent des documents PDF, des documents texte, des films de Flash d’Adobe, des fichiers provenant d’applications Microsoft Office telles que Word, Excel et PowerPoint et du texte dans des fichiers MP3. Le texte qui se trouve dans les types de contenu sélectionnés est recherché avec le reste du texte de votre site web.

Avant que les effets des paramètres Types de contenu ne soient visibles par les clients, vous devez reconstruire l’index de votre site.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

Pour analyser et indexer des fichiers MP3 chinois, japonais ou coréens, procédez comme suit. Ensuite, dans **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, spécifiez le jeu de caractères utilisé pour coder les fichiers MP3.

Voir [À propos des injections](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

**Pour sélectionner les types de contenu à analyser et à indexer**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.
1. Sur la page [!DNL Content Types], vérifiez les types de fichiers que vous souhaitez analyser et indexer sur votre site web.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des connexions {#concept_E2F3B7E7521147479E5948A94BB3A40B}

Vous pouvez utiliser Connexions pour ajouter jusqu’à dix connexions HTTP que le robot de recherche utilise pour indexer votre site web.

L’augmentation du nombre de connexions peut réduire considérablement le temps nécessaire à l’exécution d’une analyse et d’un index. Notez toutefois que chaque connexion supplémentaire augmente la charge sur votre serveur.

## Ajout de connexions pour augmenter la vitesse d’indexation {#task_3E9B83E43C1842A19066355A15C4A6FB}

Vous pouvez réduire le temps nécessaire pour indexer votre site web en utilisant Connexions pour augmenter le nombre de connexions HTTP simultanées utilisées par le moteur de recherche. Vous pouvez ajouter jusqu’à dix connexions.

Gardez à l’esprit que chaque connexion supplémentaire augmente la charge placée sur votre serveur.

**Ajout de connexions pour augmenter la vitesse d’indexation**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Connections]**.
1. Sur la page [!DNL Parallel Indexing Connections], dans le champ **[!UICONTROL Number of Connections]**, saisissez le nombre de connexions (1 à 10) à ajouter.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos de l’envoi de formulaire {#concept_CADD5D7CF373497DAA6F8564D7BC8502}

Vous pouvez utiliser l’envoi de formulaire pour vous aider à reconnaître et à traiter les formulaires sur votre site web.

Pendant l’analyse et l’indexation de votre site web, chaque formulaire rencontré est comparé aux définitions de formulaire que vous avez ajoutées. Si un formulaire correspond à une définition de formulaire, le formulaire est envoyé pour indexation. Si un formulaire correspond à plusieurs définitions, le formulaire est envoyé une fois pour chaque définition correspondante.

## Ajout de définitions de formulaire pour l’indexation de formulaires sur votre site web {#task_62FBCE9E6DBE4BDA8D1249233ADFC00F}

Vous pouvez utiliser [!DNL Form Submission] pour faciliter le traitement des formulaires reconnus sur votre site web à des fins d’indexation.

Veillez à reconstruire l’index de votre site afin que les résultats de vos modifications soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Ajout de définitions de formulaire pour l’indexation de formulaires sur votre site web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Sur la page [!DNL Form Submission], cliquez sur **[!UICONTROL Add New Form]**.
1. Sur la page [!DNL Add Form Definition], définissez les options [!DNL Form Recognition] et [!DNL Form Submission].

   Les cinq options de la section [!DNL Form Recognition] de la page [!DNL Form Definition] sont utilisées pour identifier les formulaires de vos pages web qui peuvent être traités.

   Les trois options de la section [!DNL Form Submission] permettent de spécifier les paramètres et les valeurs qui sont envoyés avec un formulaire à votre serveur web.

   Saisissez un paramètre de reconnaissance ou d’envoi par ligne. Chaque paramètre doit inclure un nom et une valeur.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <b>Reconnaissance des formulaires</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque d’URL de page </p> </td> 
      <td colname="col2"> <p>Identifiez la ou les pages web qui contiennent le formulaire. Pour identifier un formulaire qui apparaît sur une seule page, saisissez l’URL de cette page, comme dans l’exemple suivant : </p> <p> <code> https://www.mydomain.com/login.html </code> </p> <p>Pour identifier les formulaires qui apparaissent sur plusieurs pages, spécifiez un masque d’URL qui utilise des caractères génériques pour décrire les pages. Pour identifier les formulaires rencontrés sur une page ASP sous <code> https://www.mydomain.com/register/ </code>, vous devez par exemple spécifier les éléments suivants : </p> <p> <code> https://www.mydomain.com/register/*.asp&amp;nbsp; </code> </p> <p>Vous pouvez également utiliser une expression régulière pour identifier plusieurs pages. Il vous suffit de spécifier la variable 
      Mot-clé <code>
        regexp 
      </code> devant le masque d'URL, comme dans l'exemple suivant : </p> <p> <code> regexp&amp;nbsp;^https://www\.mydomain\.com/.*/login\.html$ </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque des URL d’action </p> </td> 
      <td colname="col2"> <p>Identifie l’attribut d’action de la variable 
      Balise <code>
        &lt;form&gt; 
      </code>. </p> <p>Tout comme le masque URL de la page, le masque URL d’action peut prendre la forme d’une seule URL, d’une URL avec des caractères génériques ou d’une expression régulière. </p> <p>Le masque d'URL peut être l'un des suivants : 
      <ul id="ul_EDFE7688D3DD4C0BBACCE5D4648D8E44"> 
      <li id="li_77550A448D954EF29FF33EE5E8B5E0F5"> Un chemin complet comme dans l’exemple suivant : <code> https://www.mydomain.com/products.html </code> </li> 
      <li id="li_F84E25553BBA41419BE153DC0709E011"> Un chemin partiel comme dans l’exemple suivant : <code> https://www.mydomain.com/products </code> </li> 
      <li id="li_8DADA1C8604740FCACBA30B4AAADB2A1"> Une URL qui utilise des caractères génériques comme dans l’exemple suivant : <code> https://www.mydomain.com/*.html </code> </li> 
      <li id="li_1EF637B450654B509AA4B618F7FD3C2B"> Une expression régulière comme dans l’exemple suivant : <code> regexp&amp;nbsp^https://www\.mydomain\.com/.*/login\.html$ </code> </li> 
      </ul> </p> <p>Si vous ne souhaitez pas indexer le texte sur des pages identifiées par un masque d’URL ou par un masque d’URL d’action, ou si vous ne souhaitez pas que des liens soient suivis sur ces pages, vous pouvez utiliser la variable 
      <code>
        noindex 
      </code> et 
      <code>
        nofollow 
      </code> mots-clés. Vous pouvez ajouter ces mots-clés à vos masques à l’aide de masques d’URL ou de points d’entrée. </p> <p>Voir <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573" type="concept" format="dita" scope="local"> À propos des points d’entrée d’URL </a>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> À propos des masques d’URL </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque du nom du formulaire </p> </td> 
      <td colname="col2"> <p>Identifie les formulaires si la variable 
      Les balises <code>
        &lt;form&gt; 
      </code> de vos pages web contiennent un attribut name . </p> <p>Vous pouvez utiliser un nom simple ( 
      <code>
        login_form 
      </code>), un nom avec un caractère générique ( 
      <code>
        form* 
      </code>) ou une expression régulière ( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>En règle générale, vous pouvez laisser ce champ vide, car les formulaires n’ont généralement pas d’attribut name . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Masque des ID de formulaire </p> </td> 
      <td colname="col2"> <p>Identifie les formulaires si la variable 
      Les balises <code>
        &lt;form&gt; 
      </code> de vos pages web contiennent un attribut id . </p> <p>Vous pouvez utiliser un nom simple ( 
      <code>
        login_form 
      </code>), un nom avec un caractère générique ( 
      <code>
        form* 
      </code>) ou une expression régulière ( 
      <code>
        regexp ^.*authorize.*$ 
      </code>). </p> <p>En règle générale, vous pouvez laisser ce champ vide, car les formulaires n’ont généralement pas d’attribut name . </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètres </p> </td> 
      <td colname="col2"> <p>Identifiez les formulaires qui contiennent ou ne contiennent pas un paramètre nommé ou un paramètre nommé avec une valeur spécifique. </p> <p>Par exemple, pour identifier un formulaire contenant un paramètre d’e-mail prédéfini sur rick_brough@mydomain.com, un paramètre de mot de passe, mais pas un paramètre de prénom, vous devez spécifier les paramètres suivants, une par ligne : </p> <p> <code> email=rick_brough@mydomain.com password  not&nbsp;first-name </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Envoi de formulaire</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remplacer l’URL d’action </p> </td> 
      <td colname="col2"> <p>Spécifiez quand la cible de l’envoi du formulaire est différente de ce qui est spécifié dans l’attribut action du formulaire. </p> <p>Par exemple, vous pouvez utiliser cette option lorsque le formulaire est envoyé par le biais d’une fonction JavaScript qui construit une valeur d’URL différente de celle du formulaire. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Méthode de remplacement </p> </td> 
      <td colname="col2"> <p>Indiquez quand la cible de l’envoi du formulaire est différente de celle utilisée dans l’attribut d’action du formulaire et quand l’envoi du code JavaScript a modifié la méthode . </p> <p>Les valeurs par défaut de tous les paramètres de formulaire ( 
      <code>
        &lt;input&gt; 
      </code> balises, y compris les champs masqués), par défaut 
      <code>
        &lt;option&gt; 
      </code> d’un 
      Balise <code>
        &lt;select&gt; 
      </code> et texte par défaut entre 
      Les balises <code>
        &lt;textarea&gt;...&lt;/textarea&gt; 
      </code> sont lues à partir de la page web. Cependant, tout paramètre répertorié dans la section <span class="wintitle"> Envoi de formulaire </span>, dans le champ <span class="uicontrol"> Paramètres </span>, est remplacé par les valeurs par défaut du formulaire. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Paramètres </p> </td> 
      <td colname="col2"> <p>Vous pouvez préfixer les paramètres d’envoi du formulaire à l’aide de la fonction 
      Mot-clé <code>
        not 
      </code>. </p> <p>Lorsque vous ajoutez un préfixe à un paramètre 
      <code>
        not 
      </code>, il n’est pas envoyé dans le cadre de l’envoi du formulaire. Ce comportement s’avère utile pour les cases à cocher qui doivent être soumises et désélectionnées. </p> <p>Supposons, par exemple, que vous souhaitiez envoyer les paramètres suivants : </p> <p> 
      <ul id="ul_962D12BACF464FF189DB12BFAFCC93A6"> 
      <li id="li_830C6C3EC8D2448388A453BB8EDE5940"> Le paramètre d’e-mail avec la valeur 
      <code>
        nobody@mydomain.com 
      </code> </li> 
      <li id="li_905497E3FACE472DBDD49392D5B45E01"> Le paramètre password avec la valeur 
      <code>
        tryme 
      </code> </li> 
      <li id="li_AAA411708ADC464793EADF0D821E282E"> Le paramètre de la case à cocher a été désélectionné. </li> 
      <li id="li_0D3DDE641E2B4BEF9F570C03FDB40ED2"> <p>Toutes les autres 
      Paramètres <code>
        &lt;form&gt; 
      </code> comme valeurs par défaut </p> </li> 
      </ul> </p> <p>Votre paramètre d’envoi de formulaire ressemblerait à ce qui suit : </p> <p> <code> email=nobody@mydomain.com 
        password=tryme 
        not&nbsp;mycheckbox </code> </p> <p>L’attribut method de la variable 
      La balise <code>
        &lt;form&gt; 
      </code> de la page web permet de déterminer si les données sont envoyées à votre serveur à l’aide de la méthode GET ou de la méthode POST. </p> <p>Si la variable 
      La balise <code>
        &lt;form&gt; 
      </code> ne contient pas d’attribut de méthode, le formulaire est envoyé à l’aide de la méthode GET. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une définition de formulaire {#task_9FB34E9C8A814DFE9BF7F8F8F69BF314}

Vous pouvez modifier une définition de formulaire existante si un formulaire de votre site web a été modifié ou si vous avez simplement besoin de la modifier.

Gardez à l’esprit qu’il n’existe aucune fonction [!DNL History] sur la page [!DNL Form Submission] pour annuler toute modification apportée à une définition de formulaire.

Veillez à reconstruire l’index de votre site afin que les résultats de vos modifications soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Pour modifier une définition de formulaire**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Sur la page [!DNL Form Submission], cliquez sur **[!UICONTROL Edit]** à droite d’une définition de formulaire que vous souhaitez mettre à jour.
1. Sur la page [!DNL Edit Form Definition], définissez les options [!DNL Form Recognition] et [!DNL Form Submission].

   Consultez le tableau des options sous [Ajout de définitions de formulaire pour l’indexation de formulaires sur votre site web](../c-about-settings-menu/c-about-crawling-menu.md#task_62FBCE9E6DBE4BDA8D1249233ADFC00F).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une définition de formulaire {#task_C350FC0CDE344F2786215D544C048B5E}

Vous pouvez supprimer une définition de formulaire existante si le formulaire n’existe plus sur votre site web ou si vous ne souhaitez plus traiter et indexer un formulaire particulier.

Gardez à l’esprit qu’il n’existe aucune fonction [!DNL History] sur la page [!DNL Form Submission] pour annuler toute modification apportée à une définition de formulaire.

Veillez à reconstruire l’index de votre site afin que les résultats de vos modifications soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Pour supprimer une définition de formulaire**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Form Submission]**.
1. Sur la page [!DNL Form Submission], cliquez sur **[!UICONTROL Delete]** à droite d’une définition de formulaire à supprimer.

   Veillez à choisir la définition de formulaire appropriée à supprimer. Il n’existe pas de boîte de dialogue de confirmation de suppression lorsque vous cliquez sur **[!UICONTROL Delete]** à l’étape suivante.
1. Sur la page [!DNL Delete Form Definition], cliquez sur **[!UICONTROL Delete]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos du connecteur d’index {#concept_CA6921E2FBF641F9B4F60C92B32AFA84}

Utilisez [!DNL Index Connector] pour définir des sources d’entrée supplémentaires pour indexer des pages XML ou tout type de flux.

Vous pouvez utiliser une source d’entrée de flux de données pour accéder au contenu stocké dans un formulaire qui diffère de ce qui est généralement découvert sur un site web à l’aide de l’une des méthodes d’analyse disponibles. Chaque document analysé et indexé correspond directement à une page de contenu de votre site web. Cependant, un flux de données provient d’un document XML ou d’un fichier texte délimité par des virgules ou des tabulations et contient les informations de contenu à indexer.

Une source de données XML est constituée de normes XML, ou enregistrements, qui contiennent des informations qui correspondent à des documents individuels. Ces documents individuels sont ajoutés à l’index. Un flux de données texte contient des enregistrements individuels délimités par de nouvelles lignes qui correspondent à des documents individuels. Ces documents individuels sont également ajoutés à l’index. Dans les deux cas, une configuration du connecteur d’index décrit comment interpréter le flux. Chaque configuration décrit l’emplacement du fichier et la manière dont les serveurs y accèdent. La configuration décrit également les informations de &quot;mappage&quot;. En d’autres termes, la manière dont les éléments de chaque enregistrement sont utilisés pour remplir les champs de métadonnées dans l’index obtenu.

Après avoir ajouté une définition de connecteur d’index à la page [!DNL Staged Index Connector Definitions], vous pouvez modifier n’importe quel paramètre de configuration, *sauf* pour les valeurs Nom ou Type.

La page [!DNL Index Connector] présente les informations suivantes :

* Nom des connecteurs d’index définis que vous avez configurés et ajoutés.
* L’un des types de source de données suivants pour chaque connecteur que vous avez ajouté :

   * **Texte**  : fichiers &quot;plats&quot; simples, délimités par des virgules, délimités par des tabulations ou autres formats délimités de manière cohérente.
   * **Flux**  : flux XML.
   * **XML**  - Collections de documents XML.

* Si le connecteur est activé ou non pour l’analyse et l’indexation suivantes effectuées.
* Adresse de la source de données.

Voir aussi [À propos du connecteur d’index](../c-about-settings-menu/c-about-crawling-menu.md#concept_CA6921E2FBF641F9B4F60C92B32AFA84)

## Fonctionnement du processus d’indexation pour les configurations de texte et de flux dans le connecteur d’index {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>Pour les configurations Texte et Flux , il s’agit d’un simple téléchargement de fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Ventilez la source de données téléchargée en pseudo-documents individuels. </p> </td> 
   <td colname="col3"> <p>Pour <span class="uicontrol"> Texte </span>, chaque nouvelle ligne de texte délimitée par des lignes correspond à un document individuel et est analysée à l’aide du délimiteur spécifié, tel qu’une virgule ou un onglet. </p> <p>Pour le flux <span class="uicontrol"> </span>, les données de chaque document sont extraites à l’aide d’un modèle d’expression régulière sous la forme suivante : </p> <p> <code> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>À l’aide de <span class="uicontrol"> Map </span> sur la page <span class="wintitle"> Index Connector Add </span> , créez une copie mise en cache des données, puis créez une liste de liens pour le moteur de recherche. Les données sont stockées dans un cache local et sont renseignées avec les champs configurés. </p> <p>Les données analysées sont écrites dans le cache local. </p> <p>Ce cache est lu ultérieurement pour créer les documents HTML simples dont le moteur de recherche a besoin. Par exemple : </p> <p> <code> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>L’élément <span class="codeph"> &lt;title&gt; </span> n’est généré que lorsqu’il existe un mappage sur le champ de métadonnées Titre. De même, l’élément <span class="codeph"> &lt;body&gt; </span> n’est généré que lorsqu’il existe un mappage sur le champ de métadonnées Body. </p> <p> <b>Important</b> : L’affectation de valeurs à la balise meta d’URL prédéfinie n’est pas prise en charge. </p> <p>Pour tous les autres mappages, les balises <span class="codeph"> &lt;meta&gt; </span> sont générées pour chaque champ contenant des données présentes dans le document d’origine. </p> <p>Les champs de chaque document sont ajoutés au cache. Pour chaque document écrit dans le cache, un lien est également généré, comme dans les exemples suivants : </p> <p> <code> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>Le mappage de la configuration doit comporter un champ identifié comme Clé Principal. Ce mappage forme la clé utilisée lorsque les données sont extraites du cache. </p> <p>Le robot reconnaît l’index <span class="codeph"> de l’URL : </span> préfixe de schéma, qui peut ensuite accéder aux données mises en cache localement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Analyse du jeu de documents mis en cache. </p> </td> 
   <td colname="col3"> <p>Index <span class="codeph"> : Les liens </span> sont ajoutés à la liste en attente du moteur de recherche et sont traités dans l’ordre d’analyse normal. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Traitez chaque document. </p> </td> 
   <td colname="col3"> <p>La valeur de clé de chaque lien correspond à une entrée dans le cache. L’analyse de chaque lien entraîne la récupération des données de ce document à partir du cache. Il est ensuite "assemblé" dans une image HTML qui est traitée et ajoutée à l’index. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Fonctionnement du processus d’indexation pour les configurations XML dans le connecteur d’index {#section_7F1551EA51854C5C99F284CE260526EB}

Le processus d’indexation pour la configuration XML est similaire au processus pour les configurations Texte et Flux avec les modifications et exceptions mineures suivantes.

Les documents des analyses XML étant déjà séparés en fichiers individuels, les étapes 1 et 2 du tableau ci-dessus ne s’appliquent pas directement. Si vous spécifiez une URL dans les champs **[!UICONTROL Host Address]** et **[!UICONTROL File Path]** de la page [!DNL Index Connector Add], elle est téléchargée et traitée comme un document HTML normal. On s’attend à ce que le document de téléchargement contienne une collection de liens `<a href="{url}"...`, chacun pointant vers un document XML qui est traité. Ces liens sont convertis sous la forme suivante :

```
<a href="index:<ic_config_name>?url="{url}">
```

Par exemple, si la configuration de l’Adobe renvoyait les liens suivants :

```
<a href="https://www.adobe.com/somepath/doc1.xml">doc 1</a> 
<a href="https://www.adobe.com/otherpath/doc2.xml">doc 2</a>
```

Dans le tableau ci-dessus, l’étape 3 ne s’applique pas et l’étape 4 est complétée au moment de l’analyse et de l’indexation.

Vous pouvez également mélanger vos documents XML à d’autres documents qui ont été découverts naturellement par le biais du processus d’analyse. Dans ce cas, vous pouvez utiliser des règles de réécriture ( **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**) pour modifier les URL des documents XML afin de les diriger vers Index Connector.

Voir [À propos de l’analyse des règles de récupération d’URL de la liste](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

Par exemple, supposons que vous ayez la règle de réécriture suivante :

```
RewriteRule (^http.*[.]xml$) index:Adobe?key=$1
```

Cette règle convertit toute URL se terminant par `.xml` en lien connecteur d’index. Le robot reconnaît et réécrit le schéma d’URL `index:`. Le processus de téléchargement est redirigé vers le serveur Apache Index Connector sur la Principale. Chaque document téléchargé est examiné à l’aide du même modèle d’expression régulière que celui utilisé avec les flux. Dans ce cas, cependant, le document HTML fabriqué n’est pas enregistré dans le cache. Au lieu de cela, il est directement transmis au moteur de recherche pour le traitement des index.

## Configuration de plusieurs connecteurs d’index {#section_C2B14C0F06354A57AEF6238FF3814E5D}

Vous pouvez définir plusieurs configurations du connecteur d’index pour n’importe quel compte. Les configurations sont automatiquement ajoutées à la liste déroulante dans **[!UICONTROL Settings]** > **[!UICONTROL Crawl]** > **[!UICONTROL URL Entrypoints]** comme illustré ci-dessous :

![](assets/url_entrypoints_index_connector.png)

La sélection d’une configuration dans la liste déroulante ajoute la valeur à la fin de la liste des points d’entrée d’URL.

>[!NOTE]
>
>Bien que les configurations du connecteur d’index désactivées soient ajoutées à la liste déroulante, vous ne pouvez pas les sélectionner. Si vous sélectionnez la même configuration de connecteur d’index une seconde fois, elle est ajoutée à la fin de la liste et l’instance précédente est supprimée.

Pour spécifier un point d’entrée du connecteur d’index pour une analyse incrémentielle, vous pouvez ajouter des entrées au format suivant :

```
index:<indexconnector_configuration_name>
```

Le moteur de recherche traite chaque entrée ajoutée si elle se trouve sur la page Index Connectors et si elle est activée.

Remarque : Comme l’URL de chaque document est construite à l’aide du nom de configuration du connecteur d’index et de la clé Principale du document, veillez à utiliser le même nom de configuration du connecteur d’index lors de l’exécution de mises à jour incrémentielles ! Cela permet à [!DNL Adobe Search&Promote] de mettre correctement à jour les documents indexés précédemment.

Voir aussi [À propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

**Utilisation des mappages de configuration lors de l’ajout d’un connecteur d’index**

Lorsque vous ajoutez un connecteur d’index, vous pouvez éventuellement utiliser la fonction **[!UICONTROL Setup Maps]** pour télécharger un exemple de votre source de données. Les données sont examinées pour déterminer l’adéquation de l’indexation.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si vous choisissez le type Connecteur d’index... </p> </th> 
   <th colname="col2" class="entry"> <p>La fonction de configuration des cartes... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texte </p> </td> 
   <td colname="col2"> <p>Détermine la valeur du délimiteur en commençant par essayer les onglets, puis les barres verticales ( <span class="codeph"> | </span>), et enfin des virgules ( <span class="codeph"> , </span>). Si vous avez déjà spécifié une valeur de délimiteur avant de cliquer sur <span class="uicontrol"> Mappages de configuration </span>, cette valeur est utilisée à la place. </p> <p>Le modèle le mieux adapté entraîne le remplissage des champs de mappage avec des estimations aux valeurs de balise et de champ appropriées. De plus, un échantillonnage des données analysées s’affiche. Veillez à sélectionner <span class="uicontrol"> En-têtes dans la première ligne </span> si vous savez que le fichier contient une ligne d’en-tête. La fonction de configuration utilise ces informations pour mieux identifier les entrées de mappage résultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flux </p> </td> 
   <td colname="col2"> <p>Télécharge la source de données et effectue une analyse XML simple. </p> <p>Les identifiants XPath résultants sont affichés dans les lignes Balises du tableau Carte et les valeurs similaires dans Champs. Ces lignes identifient uniquement les données disponibles et ne génèrent pas les définitions XPath les plus complexes. Cependant, il reste utile, car il décrit les données XML et identifie les valeurs des balises intelligentes. </p> <p> <p>Remarque :  La fonction Setup Maps télécharge l’intégralité de la source XML pour effectuer son analyse. Si le fichier est volumineux, cette opération peut expirer. </p> </p> <p>En cas de réussite, cette fonction identifie tous les éléments XPath possibles, dont la plupart ne sont pas souhaitables. Veillez à examiner les définitions de mappage qui en résultent et à supprimer celles dont vous n’avez pas besoin ou que vous souhaitez. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>XML </p> </td> 
   <td colname="col2"> <p>Télécharge l’URL d’un document individuel représentatif, et non la Principale liste de liens. Ce document unique est analysé à l’aide du même mécanisme que celui utilisé avec les flux et les résultats s’affichent. </p> <p>Avant de cliquer sur <span class="uicontrol"> Ajouter </span> pour enregistrer la configuration, veillez à restaurer l’URL dans le Principal document de liste de liens. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Important** : La fonction Setup Maps (Mappages de configuration) peut ne pas fonctionner pour les jeux de données XML volumineux, car l’analyseur de fichiers tente de lire l’intégralité du fichier en mémoire. Par conséquent, vous pourriez rencontrer une condition de mémoire insuffisante. Cependant, lorsque le même document est traité au moment de l’indexation, il n’est pas lu en mémoire. Au lieu de cela, les documents volumineux sont traités &quot;en déplacement&quot; et ne sont pas lus entièrement en mémoire.

**Utilisation de l’aperçu lors de l’ajout d’un connecteur d’index**

Au moment de l’ajout d’un connecteur d’index, vous pouvez éventuellement utiliser la fonction **[!UICONTROL Preview]** pour valider les données, comme si vous l’enregistriez. Il exécute un test par rapport à la configuration, mais sans enregistrer la configuration dans le compte. Le test accède à la source de données configurée. Cependant, il écrit le cache de téléchargement dans un emplacement temporaire. il n’entre pas en conflit avec le dossier cache principal utilisé par l’analyseur d’indexation.

L’aperçu traite uniquement une valeur par défaut de cinq documents, comme contrôlé par Acct:IndexConnector-Preview-Max-Documents. Les documents prévisualisés sont affichés sous forme source, dans la mesure où ils sont présentés au moteur de recherche d&#39;indexation. L’affichage est similaire à la fonction &quot;Afficher la source&quot; d’un navigateur Web. Vous pouvez parcourir les documents de l’ensemble d’aperçu à l’aide de liens de navigation standard.

L’aperçu ne prend pas en charge les configurations XML, car ces documents sont traités directement et ne sont pas téléchargés dans le cache.

## Ajout d’une définition de connecteur d’index {#task_96779B651A654E1F871F55D6DBBC8886}

Chaque configuration du connecteur d’index définit une source de données et des mappages afin de relier les éléments de données définis pour cette source aux champs de métadonnées de l’index.

Avant que les effets de la nouvelle définition activée ne soient visibles par les clients, reconstruisez l’index de votre site.

**Pour ajouter une définition de connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la page [!DNL Stage Index Connector Definitions], cliquez sur **[!UICONTROL Add New Index Connector]**.
1. Sur la page [!DNL Index Connector Add], définissez les options de connecteur de votre choix. Les options disponibles dépendent de la balise **[!UICONTROL Type]** sélectionnée.

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
      <td colname="col2"> <p>Source de vos données. Le type de source de données que vous sélectionnez affecte les options résultantes disponibles sur la page <span class="wintitle"> Index Connector Add </span> . Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texte </span> <p>Fichiers texte plats simples, délimités par des virgules, délimités par des tabulations ou autres formats délimités de manière cohérente. Chaque nouvelle ligne de texte délimitée par des lignes correspond à un document individuel et est analysée à l’aide du délimiteur spécifié. </p> <p>Vous pouvez associer chaque valeur, ou colonne, à un champ de métadonnées, référencé par le numéro de colonne, en commençant à 1 (un). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Flux </span> <p>Télécharge un Principal document XML contenant plusieurs "lignes" d’informations. </p> </li> 
      <li id="li_5A61C53522D74D4C9A5F65989604BDEF"> <span class="uicontrol"> XML </span> <p>Télécharge un document XML Principal contenant des liens ( 
      <code>
        &lt;a&gt; 
      </code>) à des documents XML individuels. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Texte</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active la configuration pour analyser et indexer. Vous pouvez également désactiver la configuration pour empêcher l’analyse et l’indexation. </p> <p> <b>Remarque</b> : Les configurations du connecteur d’index désactivées sont ignorées si elles se trouvent dans une liste de points d’entrée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse de l’hôte du serveur où se trouvent vos données. </p> <p>Si vous le souhaitez, vous pouvez spécifier un chemin d’accès URI (Uniform Resource Identifier) complet au document de source de données, comme dans les exemples suivants : </p> <p> <code> https://www.somewhere.com/some_path/some_file.xml </code> </p> <p>ou </p> <p> <code> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.xml </code> </p> <p>L’URI est ventilé en entrées appropriées pour les champs Adresse de l’hôte, Chemin du fichier, Protocole et, éventuellement, Nom d’utilisateur et Mot de passe. </p> <p>Indique l’adresse IP ou l’adresse URL du système hôte sur lequel se trouve le fichier de source de données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au fichier de texte simple, délimité par des virgules, délimité par des tabulations ou à tout autre fichier de format délimité de manière cohérente. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin d’accès au fichier incrémentiel </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au fichier de texte simple, délimité par des virgules, délimité par des tabulations ou à tout autre fichier de format délimité de manière cohérente. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations Index incrémentiel. Si aucun fichier n’est spécifié, le fichier répertorié sous Chemin du fichier est utilisé à la place. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin d’accès au fichier vertical </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au fichier texte plat simple, délimité par des virgules, délimité par des tabulations ou à tout autre fichier de format délimité de manière cohérente à utiliser lors d’une mise à jour verticale. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations de mise à jour verticale . </p> <p> <b>Remarque</b> : Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonctionnalité à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprime le chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au fichier texte plat simple, contenant une seule valeur d’identificateur de document par ligne. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations Index incrémentiel. Les valeurs trouvées dans ce fichier sont utilisées pour construire des requêtes de suppression pour supprimer des documents indexés précédemment. Les valeurs de ce fichier doivent correspondre aux valeurs trouvées dans les fichiers Chemin de fichier complet ou incrémentiel, dans la colonne identifiée en tant que <span class="uicontrol"> Clé Principal </span>. </p> <p> <b>Remarque</b> : Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonctionnalité à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Indique le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Si nécessaire, vous pouvez saisir des informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Expiration </p> </td> 
      <td colname="col2"> <p>Indique le délai d’expiration, en secondes, pour les connexions FTP, SFTP, HTTP ou HTTPS. Cette valeur doit être comprise entre 30 et 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Reprises </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal de tentatives pour les connexions FTP, SFTP, HTTP ou HTTPS en échec. Cette valeur doit être comprise entre 0 et 10. </p> <p>Une valeur de zéro (0) permet d’empêcher les tentatives de nouvelle tentative. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Encodage </p> </td> 
      <td colname="col2"> <p>Spécifie le système de codage des caractères utilisé dans le fichier de source de données spécifié. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Délimiteur </p> </td> 
      <td colname="col2"> <p>Indique le caractère à utiliser pour délimiter chaque champ du fichier de source de données spécifié. </p> <p>La virgule ( <span class="codeph"> , </span>) est un exemple de délimiteur. La virgule agit comme un délimiteur de champ qui permet de séparer les champs de données dans le fichier de source de données spécifié. </p> <p>Sélectionnez l’onglet <span class="uicontrol"> ? </span> pour utiliser le caractère de tabulation horizontale comme délimiteur. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>En-têtes de première ligne </p> </td> 
      <td colname="col2"> <p>Indique que la première ligne du fichier de source de données contient des informations d’en-tête uniquement, et non des données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre minimum de documents à indexer </p> </td> 
      <td colname="col2"> <p>S’il est défini sur une valeur positive, cette valeur indique le nombre minimum d’enregistrements attendus dans le fichier téléchargé. Si moins d’enregistrements sont reçus, l’opération d’index est abandonnée. </p> <p> <b>Remarque</b> : Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonctionnalité à utiliser. </p> <p> <b>Remarque</b> : Cette fonctionnalité n’est utilisée que lors des opérations d’index complètes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Indique les mappages colonne/métadonnées à l’aide des numéros de colonne. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Colonne </span> <p> Spécifie un numéro de colonne, la première colonne étant 1 (une). Pour ajouter de nouvelles lignes de mappage pour chaque colonne, sous <span class="wintitle"> Action </span>, cliquez sur <span class="uicontrol"> + </span>. </p> <p>Il n’est pas nécessaire de référencer chaque colonne de la source de données. Vous pouvez plutôt choisir d’ignorer les valeurs. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Champ </span> <p>Définit la valeur de l’attribut name utilisée pour chaque balise &lt;meta&gt; générée. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> </span> devient une liste déroulante à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actif. </p> <p>La valeur <span class="uicontrol"> Champ </span> peut être un champ de métadonnées non défini, si vous le souhaitez. Un champ de métadonnées non défini est parfois utile pour créer du contenu utilisé par <span class="wintitle"> Script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> À propos du filtrage des scripts </a>. </p> <p>Lorsque Index Connector traite des documents XML avec plusieurs accès sur n’importe quel champ de mappage, les valeurs multiples sont concaténées en une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur virgule. Cependant, supposons que la valeur <span class="wintitle"> de champ </span> correspondante soit un champ de métadonnées défini. En outre, ce champ a l’attribut <span class="wintitle"> Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Clé primaire? </span> <p>Une seule définition de mappage est identifiée en tant que clé Principale. Ce champ devient la référence unique qui est présentée lorsque ce document est ajouté à l’index. Cette valeur est utilisée dans l’URL du document dans l’index. </p> <p>Les valeurs <span class="uicontrol"> Clé Principal </span> doivent être uniques dans tous les documents représentés par la configuration du connecteur d’index. Les doublons rencontrés seront ignorés. Si vos documents source ne contiennent pas de valeur unique unique à utiliser comme <span class="uicontrol"> clé Principal </span>, mais que deux ou plusieurs champs combinés <i>peuvent </i> former un identifiant unique, vous pouvez définir la <span class="uicontrol"> clé Principal </span> en combinant plusieurs valeurs <span class="uicontrol"> colonne </span> avec une barre verticale ("|") délimitant les valeurs. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> Bande du code HTML ?  </span> <p>Lorsque cette option est cochée, toutes les balises HTML figurant dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Action </span> <p>Permet d’ajouter des lignes à la carte ou de supprimer des lignes de la carte. L’ordre des lignes n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Flux</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active la configuration pour analyser et indexer. Vous pouvez également désactiver la configuration pour empêcher l’analyse et l’indexation. </p> <p> <b>Remarque</b> : Les configurations du connecteur d’index désactivées sont ignorées si elles se trouvent dans une liste de points d’entrée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse IP ou l’adresse URL du système hôte sur lequel se trouve le fichier de source de données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML Principal qui contient plusieurs "lignes" d’informations. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin d’accès au fichier incrémentiel </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML incrémentiel qui contient plusieurs "lignes" d’informations. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations Index incrémentiel. Si aucun fichier n’est spécifié, le fichier répertorié sous Chemin du fichier est utilisé à la place. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin d’accès au fichier vertical </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML qui contient plusieurs "lignes" d’informations éparses à utiliser lors d’une mise à jour verticale. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations de mise à jour verticale . </p> <p> <b>Remarque</b> : Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonctionnalité à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprime le chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au fichier texte plat simple, contenant une seule valeur d’identificateur de document par ligne. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> <p>Ce fichier, s’il est spécifié, est téléchargé et traité lors des opérations Index incrémentiel. Les valeurs trouvées dans ce fichier sont utilisées pour construire des requêtes de suppression pour supprimer des documents indexés précédemment. Les valeurs de ce fichier doivent correspondre aux valeurs trouvées dans les fichiers Chemin de fichier complet ou incrémentiel, dans la colonne identifiée en tant que <span class="uicontrol"> Clé Principal </span>. </p> <p> <b>Remarque</b> : Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonctionnalité à utiliser. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Indique le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Si nécessaire, vous pouvez saisir des informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifie l’élément XML que vous pouvez utiliser pour identifier les lignes XML individuelles dans le fichier de source de données que vous avez spécifié. </p> <p>Par exemple, dans le fragment de flux suivant d’un document XML d’Adobe, la valeur de l’élément est <span class="codeph"> enregistrement </span> : </p> <p> <code> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col1"> <p>Nombre minimum de documents à indexer </p> </td> 
      <td colname="col2"> <p>S’il est défini sur une valeur positive, cette valeur indique le nombre minimum d’enregistrements attendus dans le fichier téléchargé. Si moins d’enregistrements sont reçus, l’opération d’index est abandonnée. </p> <p> <b>Remarque</b> : Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonctionnalité à utiliser. </p> <p> <b>Remarque</b> : Cette fonctionnalité n’est utilisée que lors des opérations d’index complètes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Permet de spécifier des mappages XML-élément-vers-métadonnées à l’aide d’expressions XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Baliser </span> <p>Spécifie une représentation XPath des données XML analysées. En utilisant l’exemple de document XML d’Adobe ci-dessus, sous l’option Itemtag, il peut être mappé à l’aide de la syntaxe suivante : </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
      /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
      /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La syntaxe ci-dessus se traduit comme suit : </p> <p> 
      <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
      <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>L’attribut <span class="codeph"> display </span> de l’élément <span class="codeph"> enregistrement </span> est mappé au champ de métadonnées <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu à l'intérieur d'un élément <span class="codeph"> de métadonnées </span> contenu à l'intérieur d'un élément <span class="codeph"> d'enregistrement </span> dont l'attribut name est <span class="codeph"> title </span> est associé au champ de métadonnées <span class="codeph"> title &lt;a/&gt;.</span> </p> </li> 
      <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu à l'intérieur d'un élément <span class="codeph"> metadata </span> contenu à l'intérieur de l'élément <span class="codeph"> record </span> , dont l'attribut name est <span class="codeph"> description </span> est mappé au champ de métadonnées <span class="codeph"> desc &lt;a11111 1/&gt;.</span> </p> </li> 
      <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu dans un élément <span class="codeph"> metadata </span> contenu dans l'élément <span class="codeph"> record </span> , dont l'attribut name est <span class="codeph"> description </span>, est associé au champ de métadonnées <span class="codeph"> corps </span>. </p> </li> 
      </ul> </p> <p>XPath est une notation relativement compliquée. Vous trouverez plus d’informations à l’emplacement suivant : </p> <p>Voir <a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Champ </span> <p>Définit la valeur de l’attribut name utilisée pour chaque balise <span class="codeph"> &lt;meta&gt; </span> générée. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> </span> devient une liste déroulante à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actif. </p> <p>La valeur <span class="uicontrol"> Champ </span> peut être un champ de métadonnées non défini, si vous le souhaitez. Un champ de métadonnées non défini est parfois utile pour créer du contenu utilisé par <span class="wintitle"> Script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> À propos du filtrage des scripts </a>. </p> <p>Lorsque Index Connector traite des documents XML avec plusieurs accès sur n’importe quel champ de mappage, les valeurs multiples sont concaténées en une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur virgule. Cependant, supposons que la valeur <span class="wintitle"> de champ </span> correspondante soit un champ de métadonnées défini. En outre, ce champ a l’attribut <span class="wintitle"> Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Clé primaire? </span> <p>Une seule définition de mappage est identifiée en tant que clé Principale. Ce champ devient la référence unique qui est présentée lorsque ce document est ajouté à l’index. Cette valeur est utilisée dans l’URL du document dans l’index. </p> <p>Les valeurs <span class="uicontrol"> Clé Principal </span> doivent être uniques dans tous les documents représentés par la configuration du connecteur d’index. Les doublons rencontrés seront ignorés. Si vos documents source ne contiennent pas de valeur unique unique à utiliser comme <span class="uicontrol"> clé de Principal </span>, mais que deux ou plusieurs champs combinés <i>peuvent </i> former un identifiant unique, vous pouvez définir la <span class="uicontrol"> clé de Principal </span> en combinant plusieurs <span class="uicontrol"> définitions de balise </span> avec une barre verticale ("|) . </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC81F"> <span class="uicontrol"> Bande du code HTML ?  </span> <p>Lorsque cette option est cochée, toutes les balises HTML figurant dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_5E829D1D0DBD4BB7AAB5DB983053D248"> <span class="uicontrol"> Utiliser comme suppression ?  </span> <p>Utilisé uniquement pendant les opérations Index incrémentiel. Les enregistrements correspondant à ce modèle XPath identifient les éléments à supprimer. La valeur <span class="uicontrol"> Clé Principal </span> de chaque enregistrement de ce type est utilisée pour construire des requêtes de suppression, comme avec Delete File Path. </p> <p> <b>Remarque</b> : Cette fonction n’est pas activée par défaut. Contactez le support technique pour activer la fonctionnalité à utiliser. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Action  </span> <p>Permet d’ajouter des lignes à la carte ou de supprimer des lignes de la carte. L’ordre des lignes n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : XML</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active la configuration pour analyser et indexer. Vous pouvez également désactiver la configuration pour empêcher l’analyse et l’indexation. </p> <p> <b>Remarque</b> : Les configurations du connecteur d’index désactivées sont ignorées si elles se trouvent dans une liste de points d’entrée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse URL du système hôte sur lequel le fichier de source de données est trouvé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML Principal contenant des liens ( 
      <code>
        &lt;a&gt; 
      </code>) à des documents XML individuels. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Indique le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_EA4EB7953D68483FAD75753B2EE70E74"> 
      <li id="li_537F24C6B2AB435CB7C14117663D7B3F"> HTTP <p>Si nécessaire, vous pouvez saisir des informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_8C13C93C52364FFA8B9B18830CDB223C"> HTTPS <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_2F967B5675254C949B31EAB19910751C"> FTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_C24BE4C1DE79488AA64C7133D78CD3A6"> SFTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_7581C21CFC104986A361F62BD7A370C1"> Fichier </li> 
      </ul> </p> <p> <b>Remarque</b> : Le paramètre Protocole n’est utilisé que lorsque des informations sont spécifiées dans les champs Adresse de l’hôte et/ou Chemin du fichier . Les documents XML individuels sont téléchargés à l’aide de HTTP ou HTTPS, selon leurs spécifications d’URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifie l’élément XML qui définit une "ligne" dans le fichier de source de données que vous avez spécifié. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Permet de définir des mappages colonne/métadonnées à l’aide des numéros de colonne. </p> <p> 
      <ul id="ul_06F50CBA0AA64C7CB1AFAE076E629A64"> 
      <li id="li_0FA2502869BA40DC93D790B79E15A9D2"> <span class="uicontrol"> Baliser </span> <p>Spécifie une représentation XPath des données XML analysées. À l’aide de l’exemple de document XML d’Adobe ci-dessus, sous l’option Itemtag, vous pouvez le mapper à l’aide de la syntaxe suivante : </p> <p> <code> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La syntaxe ci-dessus se traduit comme suit : </p> <p> 
      <ul id="ul_F8C536E6E54546D9AA5B22B879C0AF39"> 
      <li id="li_78A35DFFF1B4496CAC6EDC7B1E991F29"> <code> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>L’attribut <span class="codeph"> display </span> de l’élément <span class="codeph"> enregistrement </span> est mappé au champ de métadonnées <span class="codeph"> page-url </span>. </p> </li> 
      <li id="li_FA7DF3D1942248B98660F3D0C82F4563"> <code> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu à l'intérieur d'un élément <span class="codeph"> de métadonnées </span> contenu à l'intérieur d'un élément <span class="codeph"> d'enregistrement </span> dont l'attribut name est <span class="codeph"> title </span> est associé au champ de métadonnées <span class="codeph"> title &lt;a/&gt;.</span> </p> </li> 
      <li id="li_D8000A116FF84DE59ED19C656DDD3BC1"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu à l'intérieur d'un élément <span class="codeph"> metadata </span> contenu à l'intérieur de l'élément <span class="codeph"> record </span> , dont l'attribut name est <span class="codeph"> description </span> est mappé au champ de métadonnées <span class="codeph"> desc &lt;a11111 1/&gt;.</span> </p> </li> 
      <li id="li_7FA6A53DFD3D42A98B7BA17CC29DDB81"> <code> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu dans un élément <span class="codeph"> metadata </span> contenu dans l'élément <span class="codeph"> record </span> , dont l'attribut name est <span class="codeph"> description </span>, est associé au champ de métadonnées <span class="codeph"> corps </span>. </p> </li> 
      </ul> </p> <p>XPath est une notation relativement compliquée. Vous trouverez plus d’informations à l’emplacement suivant : </p> <p>Voir <a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_84999D07E0AE4265BC7928BBB49957B9"> <span class="uicontrol"> Champ </span> <p>Définit la valeur de l’attribut name utilisée pour chaque balise &lt;meta&gt; générée. </p> </li> 
      <li id="li_E125788D0F5242958BD790E26A675C20"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> </span> devient une liste déroulante à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actif. </p> <p>La valeur <span class="uicontrol"> Champ </span> peut être un champ de métadonnées non défini, si vous le souhaitez. Un champ de métadonnées non défini est parfois utile pour créer du contenu utilisé par <span class="wintitle"> Script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> À propos du filtrage des scripts </a>. </p> <p>Lorsque Index Connector traite des documents XML avec plusieurs accès sur n’importe quel champ de mappage, les valeurs multiples sont concaténées en une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur virgule. Cependant, supposons que la valeur <span class="wintitle"> de champ </span> correspondante soit un champ de métadonnées défini. En outre, ce champ a l’attribut <span class="wintitle"> Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824609F"> <span class="uicontrol"> Clé primaire? </span> <p>Une seule définition de mappage est identifiée en tant que clé Principale. Ce champ devient la référence unique qui est présentée lorsque ce document est ajouté à l’index. Cette valeur est utilisée dans l’URL du document dans l’index. </p> <p>Les valeurs <span class="uicontrol"> Clé Principal </span> doivent être uniques dans tous les documents représentés par la configuration du connecteur d’index. Les doublons rencontrés seront ignorés. Si vos documents source ne contiennent pas de valeur unique unique à utiliser comme <span class="uicontrol"> clé de Principal </span>, mais que deux ou plusieurs champs combinés <i>peuvent </i> former un identifiant unique, vous pouvez définir la <span class="uicontrol"> clé de Principal </span> en combinant plusieurs <span class="uicontrol"> définitions de balise </span> avec une barre verticale ("|) . </p> </li> 
      <li id="li_9F435EFB3EC74B409EC82A851824610G"> <span class="uicontrol"> Bande du code HTML ?  </span> <p>Lorsque cette option est cochée, toutes les balises HTML figurant dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_6302D18971AD439FBECE27742649C56B"> <span class="uicontrol"> Action  </span> <p>Permet d’ajouter des lignes à la carte ou de supprimer des lignes de la carte. L’ordre des lignes n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Cliquez sur **[!UICONTROL Setup Maps]** pour télécharger un exemple de votre source de données. Les données sont examinées pour déterminer l’adéquation de l’indexation. Cette fonctionnalité est disponible uniquement pour les types de texte et de flux.
1. (Facultatif) Cliquez sur **[!UICONTROL Preview]** pour tester le fonctionnement réel de la configuration. Cette fonctionnalité est disponible uniquement pour les types de texte et de flux.
1. Cliquez sur **[!UICONTROL Add]** pour ajouter la configuration à la page [!DNL Index Connector Definitions] et à la liste déroulante [!DNL Index Connector Configurations] de la page [!DNL URL Entrypoints].

   Voir [À propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).
1. Sur la page [!DNL Index Connector Definitions], cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la page [!DNL Index Connector Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une définition de connecteur d’index {#task_DCFC9C6A9964421DB5AB6C25DEE98DE9}

Vous pouvez modifier un connecteur d’index que vous avez défini.

>[!NOTE]
>
>Toutes les options que vous pouvez modifier ne sont pas disponibles, par exemple Nom du connecteur d’index ou Type dans la liste déroulante [!DNL Type].

**Pour modifier une définition de connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la page [!DNL Index Connector], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Edit]** pour un nom de définition du connecteur d’index dont vous souhaitez modifier les paramètres.
1. Sur la page [!DNL Index Connector Edit], définissez les options de votre choix.

   Consultez le tableau des options sous [Ajout d’une définition de connecteur d’index](../c-about-settings-menu/c-about-crawling-menu.md#task_96779B651A654E1F871F55D6DBBC8886).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la page [!DNL Index Connector Definitions], cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la page [!DNL Index Connector Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Affichage des paramètres d’une définition de connecteur d’index {#task_D0B71A7426E54247BDB3468EC576D871}

Vous pouvez consulter les paramètres de configuration d’une définition de connecteur d’index existante.

Une fois qu’une définition de connecteur d’index a été ajoutée à la page [!DNL Index Connector Definitions], vous ne pouvez pas modifier son paramètre Type . Vous devez plutôt supprimer la définition, puis en ajouter une nouvelle.

**Pour afficher les paramètres d’une définition de connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la page [!DNL Index Connector], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Edit]** pour un nom de définition du connecteur d’index dont vous souhaitez modifier les paramètres.

## Copie d’une définition de connecteur d’index {#task_3AD55DF07FC44A748D0EFDAB7B35699B}

Vous pouvez copier une définition de connecteur d’index existante à utiliser comme base pour un nouveau connecteur d’index que vous souhaitez créer.

Lors de la copie d’une définition Connecteur d’index, la définition copiée est désactivée par défaut. Pour activer ou &quot;activer&quot; la définition, vous devez la modifier à partir de la page [!DNL Index Connector Edit] et sélectionner **[!UICONTROL Enable]**.

Voir [Modification d’une définition de connecteur d’index](../c-about-settings-menu/c-about-crawling-menu.md#task_DCFC9C6A9964421DB5AB6C25DEE98DE9).

**Pour copier une définition de connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la page [!DNL Index Connector], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Copy]** pour un nom de définition du connecteur d’index dont vous souhaitez dupliquer les paramètres.
1. Sur la page [!DNL Index Connector Copy], saisissez le nouveau nom de la définition.
1. Cliquez sur **[!UICONTROL Copy]**.
1. (Facultatif) Sur la page [!DNL Index Connector Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Renommer une définition de connecteur d’index {#task_5132118FC21B47D99881E0ED425225D7}

Vous pouvez modifier le nom d’une définition de connecteur d’index existante.

Après avoir renommé la définition, cochez **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Vous souhaitez vous assurer que le nouveau nom de définition est reflété dans la liste déroulante de la page [!DNL URL Entrypoints].

Voir [Ajout de plusieurs points d’entrée d’URL que vous souhaitez indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

**Pour renommer une définition de connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la page [!DNL Index Connector], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Rename]** pour le nom de définition du connecteur d’index que vous souhaitez modifier.
1. Sur la page [!DNL Index Connector Rename] , saisissez le nouveau nom de la définition dans le champ [!DNL Name] .
1. Cliquez sur **[!UICONTROL Rename]**.
1. Cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Si le nom du connecteur d’index précédent figure dans la liste, supprimez-le et ajoutez l’entrée nouvellement renommée.

   Voir [Ajout de plusieurs points d’entrée d’URL que vous souhaitez indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45). 1. (Facultatif) Sur la page [!DNL Index Connector Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’une définition de connecteur d’index {#task_6B0BD5D0C09F4597A401B0F3AC7C7EA7}

Vous pouvez supprimer une définition Connecteur d’index existante dont vous n’avez plus besoin ou que vous n’utilisez plus.

**Pour supprimer une définition de connecteur d’index**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Index Connector]**.
1. Sur la page [!DNL Index Connector Definitions], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Delete]** pour le nom de définition du connecteur d’index à supprimer.
1. Sur la page [!DNL Index Connector Delete], cliquez sur **[!UICONTROL Delete]**.
