---
description: Utilisez le menu Réécrire les règles pour définir l’analyse et rechercher les règles d’URL et de titre.
solution: Target
subtopic: Rewrite Rules
title: A propos du menu Réécrire les règles
topic: Paramètres, recherche sur le site et marchandisage
uuid: 77ee84dd-fdba-4d34-ae8e-2fe786599800
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '10202'
ht-degree: 0%

---


# A propos du menu Réécrire des règles {#about-the-rewrite-rules-menu}

Utilisez le menu Réécrire les règles pour définir l’analyse et rechercher les règles d’URL et de titre.

## A propos de l&#39;analyse des règles d&#39;URL de stockage de Listes {#concept_B71CF4C8030A4A74A22C3BFE4DE3B865}

Les règles d’analyse des URL spécifient comment les URL qu’il rencontre dans le contenu Web sont réécrites. Vous pouvez spécifier un nombre illimité de règles et de conditions et manipuler n’importe quelle portion des URL rencontrées.

<!-- 

c_about_crawl_list_store_url_rules.xml

 -->

Les règles d’analyse sont particulièrement utiles pour réécrire des parties dynamiques d’une URL, telles qu’un identifiant de session unique pour chaque client qui visite votre site Web. Vous pouvez également utiliser des règles de réécriture pour masquer certaines parties d’une URL, telles que les paramètres de requête, du robot de recherche. Par défaut, aucune règle n’est spécifiée et aucune réécriture d’URL n’est effectuée.

Lorsqu’un site Web est analysé, les URL de contenu incorporées sont stockées dans une liste temporaire de pages Web supplémentaires à analyser. Avant qu’une URL ne soit ajoutée à cette liste, les règles de réécriture du magasin lui sont appliquées. En règle générale, les règles de réécriture du magasin sont utilisées pour supprimer un ID de session d’une URL ou pour appliquer un ID de session spécifique pour l’analyse. Lorsque le robot de recherche récupère une URL de la liste, les règles de récupération de réécriture sont utilisées pour manipuler à nouveau des parties de cette URL. En règle générale, les règles de récupération sont utilisées pour insérer de nouveau des données sensibles au temps dans l’URL. Il s’agit de l’URL finale utilisée pour récupérer la page de votre site Web.

Voir [A propos de l’analyse des règles d’URL de récupération de Liste](../c-about-settings-menu/c-about-rewrite-rules-menu.md#concept_EC8E2E48B99A458D8567B526C9827CBA).

En règle générale, les règles d’URL de stockage sont utilisées exclusivement. Les règles d’URL de récupération ne sont nécessaires que si les URL contiennent des données dynamiques, comme un ID de session, et si ces données dynamiques changent au fil du temps pour rester valides. Dans ce cas, vous utilisez les règles d’URL de stockage pour obtenir l’état le plus récent des données à partir des URL rencontrées. Vous utilisez ensuite les règles d’URL de récupération pour ajouter ces données à chaque URL lorsque le robot de recherche tente de récupérer la page.

Chaque règle est spécifiée avec une directive de règle de réécriture (RewriteRule) et une ou plusieurs conditions de réécriture facultatives (RewriteCond). L&#39;ordre des règles est important. Le jeu de règles est bouclé règle par règle. Lorsqu’une règle correspond, elle effectue une boucle dans toutes les conditions de réécriture correspondantes. Une règle d’URL d’analyse est spécifiée de la manière suivante :

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Lorsqu’une URL incorporée est rencontrée, le robot de recherche tente de faire correspondre l’URL au Modèle de chaque règle d’analyse. Si le modèle correspond, le moteur de réécriture recherche les directives RewriteCond correspondantes. Si aucune condition n’est présente, l’URL est remplacée par une nouvelle valeur construite à partir de la chaîne de substitution et continue avec la règle suivante dans le jeu de règles. Si des conditions existent, elles sont traitées dans l’ordre dans lequel elles sont répertoriées. Le moteur de réécriture tente de faire correspondre un modèle de condition (CondPattern) à une chaîne de test (TestString). Si les deux correspondent, la condition suivante est traitée jusqu’à ce qu’aucune condition supplémentaire ne soit disponible. Si toutes les conditions correspondent, l’URL est remplacée par la Substitution spécifiée dans la règle. Si la condition n’est pas remplie, l’ensemble complet des conditions et la règle correspondante échoue.

## À propos des directives RewriteRule {#section_162122340BB34F12BB9A36DC9349092B}

Une directive RewriteRule a la forme suivante :

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` peut être une expression régulière POSIX, qui est appliquée à l’URL active. L’&quot;URL active&quot; peut différer de l’URL demandée d’origine, car des règles antérieures ont peut-être déjà correspondu et modifié l’URL.

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Vous ne pouvez pas utiliser le caractère &quot;pas&quot; (&#39;!&#39;) pour préfixer le modèle. Le caractère &quot;pas&quot; vous permet de nier un modèle, c’est-à-dire d’être vrai uniquement si l’URL active ne correspond PAS à ce modèle. Le caractère &quot;pas&quot; peut être utilisé lorsqu’il est préférable de faire correspondre un modèle négatif ou comme règle par défaut finale.

>[!NOTE]
>
>Vous ne pouvez pas utiliser à la fois le caractère &quot;pas&quot; et les caractères génériques groupés dans un modèle. En outre, vous ne pouvez pas utiliser un modèle dégradé lorsque la chaîne de substitution contient $N.

Vous pouvez utiliser des parenthèses pour créer une référence dans le modèle, qui peut être référencée par Substitution et CondPattern.

**** SubstitutionL&#39;URL est remplacée par la chaîne de substitution, qui contient les éléments suivants :

Texte ordinaire : Texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Voici les deux types de références arrière :

* **RéécrireRègle** Références arrière Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0)  &lt;> Par exemple, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* **RéécrireCond** RéférencesRéférencesCes références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et se présentent sous la forme %N (0  &lt;>

Variables : Il s’agit de variables au format %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE est une chaîne pour le nom d’une variable définie. Consultez l&#39;indicateur `*[E]*` pour plus d&#39;informations sur la définition des variables d&#39;environnement.

Fonctions : Il s&#39;agit de fonctions du formulaire ${NAME_OF_FUNCTION:key} dont NAME_OF_FUNCTION est le suivant :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* escape URL code tous les caractères dans *key*.
* Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; ne sont pas modifiés ; les espaces sont convertis en &quot;+&quot; et tous les autres caractères sont convertis en leur équivalent codé URL %xx.
* unescape convertit &#39;+&#39; en espace et tous les caractères codés dans l’URL %xx en caractères uniques.

>[!NOTE]
>
>Il existe une chaîne de substitution spéciale : `'-'` cela signifie &quot;aucune substitution&quot;. La chaîne `'-'` est souvent utilisée avec l&#39;indicateur C (chain), ce qui vous permet de faire correspondre une URL à plusieurs modèles avant qu&#39;une substitution ne se produise.

**Indicateurs**

(Facultatif) Placez les indicateurs entre crochets `[]`. Plusieurs indicateurs sont séparés par des virgules.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Dernière règle. </p> <p>Arrête le processus de réécriture et n’applique aucune règle de réécriture supplémentaire. Utilisez cet indicateur pour empêcher tout traitement ultérieur de l’URL active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Prochain tour. </p> <p> Réexécute le processus de réécriture (en commençant à nouveau par la première règle de réécriture) en utilisant l’URL de la dernière règle de réécriture (et non l’URL d’origine). Attention à ne pas créer de boucle fatale ! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Enchaîné avec la règle suivante. </p> <p>Chaine la règle actuelle à la règle suivante (qui peut également être liée à la règle suivante, etc.). Si une règle correspond, le processus de substitution se poursuit comme d’habitude. Si la règle ne correspond pas, toutes les règles chaînées suivantes sont ignorées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Aucun cas. </p> <p> Rend le modèle non sensible à la casse (c’est-à-dire qu’il n’y a aucune différence entre "A-Z" et "a-z") lorsque le modèle est comparé à l’URL active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignore la ou les règles suivantes. </p> <p> Si la règle actuelle correspond, cet indicateur force le moteur de réécriture à ignorer les règles num suivantes dans le jeu de règles. Utilisez cet indicateur pour faire des constructions pseudo-alors-sinon. La dernière règle de la clause then-clause devient skip=N où N est le nombre de règles de la clause else. </p> <p> <p>Remarque :  Ce drapeau n'est pas le même que le drapeau 'chain|C' !) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Définit la variable environnementale. </p> <p>Crée une variable d’environnement "VAR" définie sur la valeur VAL, où VAL peut contenir des références arrière d’expressions régulières, $N et %N, qui sont développées. Vous pouvez utiliser cet indicateur plusieurs fois pour définir plusieurs variables. Les variables peuvent être ultérieurement déréférencées dans un modèle RewriteCond suivant via %{VAR}. </p> <p>Utilisez cet indicateur pour supprimer et mémoriser les informations des URL. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Les règles de réécriture de magasin et les règles de réécriture de récupération partagent des valeurs de variable. En raison de ce comportement, vous pouvez définir une variable sur une valeur de sessionid sensible au temps lorsqu’une URL incorporée est rencontrée et stockée. Lorsque l’URL suivante est récupérée à partir de la liste d’enregistrement temporaire, la dernière valeur de l’ID de session peut y être ajoutée avant la récupération de cette page.

**Exemple de RewriteRule avec une fonction**

Supposons que vous disposez d’un serveur sensible à la casse, qui gère les chaînes `"www.mydomain.com"` et `"www.MyDomain.com"` différemment. Pour que votre serveur fonctionne correctement, assurez-vous que le domaine est toujours `"www.mydomain.com"` même si certains documents contiennent des liens référençant `"www.MyDomain.com."` Pour ce faire, vous pouvez utiliser la règle suivante :

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Cette règle de réécriture utilise la fonction `tolower` pour réécrire la partie domaine d’une URL afin de s’assurer qu’elle est toujours en minuscules, comme dans l’exemple suivant :

1. Le modèle `(^https://([^/]*)(.*)$)` contient une référence `([^/]*)` qui correspond à tous les caractères compris entre `https://` et le premier `/` de l’URL. Le modèle contient également une deuxième référence `(.*)` qui correspond à tous les caractères restants de l’URL.

1. La Substitution `(https://${tolower:$1}$2)` indique au moteur de recherche de réécrire l&#39;URL en utilisant la fonction `tolower` sur la première référence arrière `(https:// ${tolower:$1}$2)`, en laissant le reste de l&#39;URL intact `(https://${tolower:$1} $2)`.

Par conséquent, une URL du formulaire `https://www.MyDomain.com/INTRO/index.Html` est réécrite en tant que `https://www.mydomain.com/INTRO/index.Html`.

## À propos des directives RewriteCond {#section_CD5A19B2D3204F73B645411931FC34A1}

La directive RewriteCond définit une condition de règle. Lorsqu&#39;un RewriteCond précède un RewriteRule, la règle n&#39;est utilisée que si son modèle correspond au titre actuel et que les conditions supplémentaires s&#39;appliquent. Les conditions de réécriture se présentent comme suit :

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` est une chaîne qui peut contenir les éléments suivants :

Texte ordinaire : Texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Voici les deux types de références arrière :

* **RéécrireRègle** Références arrière Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0)  &lt;> Par exemple, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RéécrireCond** RéférencesRéférencesCes références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et se présentent sous la forme %N (0&lt;>

Variables : Il s’agit de variables au format %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE peut être une chaîne pour le nom d’une variable définie. Voir l&#39;indicateur RewriteRule *`[E]`* pour plus d&#39;informations sur la définition de variables.

Fonctions : Il s&#39;agit de fonctions du formulaire ${NAME_OF_FUNCTION:key} dont NAME_OF_FUNCTION est le suivant :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* L’URL d’échappement code tous les caractères de la clé. Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; ne sont pas modifiés, les espaces sont traduits en &#39;+&#39; et tous les autres caractères sont transformés en équivalents `%xx` codés URL.
* unescape convertit &#39;+&#39; en espace et tous les caractères d&#39;encodage d&#39;URL `%xx` en caractères uniques.

**** CondPatternest une Expression régulière étendue standard avec quelques ajouts. La chaîne de modèle peut être précédée d&#39;un caractère `!` (point d&#39;exclamation) pour spécifier un modèle non-correspondant. Vous pouvez utiliser l’une des variantes spéciales suivantes plutôt que de véritables chaînes d’expression régulières :

>[!NOTE]
>
>Vous pouvez également ajouter un point d’exclamation (&#39;!&#39;) au préfixe de tous ces tests. pour nier leur sens.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexiquement moins. </p> <p> Traite le CondPattern comme une chaîne simple et le compare lexiquement à TestString. True si TestString est lexiquement inférieur à CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexiquement plus grand. </p> <p> Traite le CondPattern comme une chaîne simple et le compare lexiquement à TestString. True si TestString est lexiquement supérieur à CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexiquement égal. </p> <p> Traite le CondPattern comme une chaîne simple et le compare lexiquement à TestString. True si TestString est lexical égal à CondPattern, c'est-à-dire que les deux chaînes sont exactement égales (caractère par caractère). Si CondPattern n'est que "" (deux guillemets), ceci compare TestString à la chaîne vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Indicateurs**
 (facultatifs) Placez les indicateurs entre crochets  `[]`. Plusieurs indicateurs sont séparés par des virgules.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Aucun cas. </p> <p>Cet indicateur rend le test non sensible à la casse, c'est-à-dire qu'il n'y a aucune différence entre "A-Z" et "a-z" à la fois dans TestString développé et dans CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>Ou la condition suivante. </p> <p>Utilisez cet indicateur pour combiner des conditions de règle avec un OU local au lieu de l’ET implicite. Sans cet indicateur, vous devrez écrire le cond/la règle plusieurs fois. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**

Certaines pages Web attribuent une variable CGI &quot;sessionid&quot; la première fois qu’un visiteur arrive sur un site. Cette variable sert à identifier le visiteur et, lorsque le visiteur parcourt le site, elle est transmise. Comme le robot de recherche ressemble à un visiteur de votre site, un numéro &quot;sessionid&quot; lui est attribué. Le robot de recherche conserve cette seule valeur &quot;sessionid&quot;, même si une seconde page du site tente d’attribuer une nouvelle valeur. Pour ce faire, vous devez réécrire deux règles.

La première règle sert à identifier et à stocker la variable sessionid :

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

La règle RewriteRule utilise un indicateur E `([E=sessionid:$1])` pour affecter la valeur actuelle du paramètre CGI sessionid à la variable `sessionid`. `$1` fait référence à la première référence arrière, qui se trouve entre le premier jeu de parenthèses dans le modèle `([^&#]+)` de RewriteRule.

L’expression régulière `^&#]+` correspond à la partie d’une URL située entre le mot `sessionid` et le caractère `**&**or**#**` suivant. Dans la mesure où cette règle RewriteRule est utilisée uniquement pour créer la valeur initiale de la variable sessionid, elle ne réécrit pas. Notez que le champ Substitution de la règle est défini sur `-` pour indiquer qu&#39;aucune réécriture n&#39;est requise.

Le RewriteCond examine la variable `sessionid` ( `%{sessionid}`). S&#39;il n&#39;a même pas un seul caractère (!.+), alors la RewriteRule correspond.

Cette règle permet de lire l’URL en tant que `https://www.domain.com/home/?sessionid=1234&function=start` et d’affecter la valeur `1234` à la variable `sessionid`.

La deuxième règle est utilisée pour réécrire toutes les URL qui correspondent au modèle de règle de réécriture suivant :

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

Le modèle RewriteRule contient deux références arrière : `(.+)` et `(.*)`. La première référence arrière correspond à tous les caractères précédant `sessionid`. La seconde référence correspond à tous les caractères après la fin de `&` ou `#`.

Le modèle de substitution réécrit l&#39;URL à l&#39;aide de la première référence arrière, suivie de la chaîne &quot;sessionid=&quot;, suivie de la valeur de la variable d&#39;ID de session définie par la première règle `%{sessionid}`, suivie de la seconde référence arrière. `($1sessionid=%{sessionid} $2)`

Notez que cette RewriteRule ne contient pas de RewriteCond. De ce fait, elle provoque une réécriture pour toutes les URL qui correspondent à la règle de réécriture *Pattern*. Ainsi, si la valeur de la variable sessionid ( `%{sessionid}`) est `1234`, une URL de la forme `https://www.domain.com/products/?sessionid=5678&function=buy` est réécrite en tant que `https://www.domain.com/products/?sessionid=1234&function=buy`

## Remerciements {#section_B17088EF38244496BC1DDD4ECF75EB5B}

Le logiciel du moteur de réécriture a été développé à l&#39;origine par Apache Group pour être utilisé dans le projet de serveur Apache HTTP (https://www.apache.org/).

## Ajouter une règle URL de banque de listes d’analyse {#task_22DD40DF95584B12BE8E6ECFBF579BCD}

Vous pouvez ajouter des règles d’URL de magasin de listes d’analyse afin de spécifier comment les URL rencontrées dans le contenu Web sont réécrites. Vous pouvez spécifier un nombre illimité de règles et de conditions et manipuler n’importe quelle portion des URL rencontrées.

<!-- 

t_adding_a_crawl_list_store_url_rule.xml

 -->

**Pour ajouter des règles d’URL de banque de listes d’analyse**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Store URL Rules]**.
1. Dans le champ [!DNL Crawl List Store URL Rules], entrez les règles de votre choix.

   Les lignes vierges et les lignes de commentaire commençant par le caractère &quot;#&quot; (hachage) sont autorisées.
1. (Facultatif) Sur la page [!DNL Crawl List Store URL Rules], dans le champ [!DNL Test Crawl List Store URL Rules], saisissez une URL de test dont vous souhaitez tester les règles d’analyse, puis cliquez sur **Test**.
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Crawl List Store URL Rules], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos de l&#39;analyse des règles d&#39;URL de récupération de Liste {#concept_EC8E2E48B99A458D8567B526C9827CBA}

Les règles d’analyse des URL spécifient comment les URL rencontrées dans le contenu Web sont réécrites. Vous pouvez spécifier un nombre illimité de règles et de conditions et manipuler n’importe quelle portion des URL rencontrées.

<!-- 

c_about_crawl_list_retrieve_url_rules.xml

 -->

Avant que les effets des règles ne soient visibles par les clients, veillez à recréer l&#39;index de votre site.

Les règles d’analyse sont particulièrement utiles pour réécrire des parties dynamiques d’une URL, telles qu’un identifiant de session unique pour chaque client qui visite votre site Web. Vous pouvez également utiliser des règles de réécriture pour masquer certaines parties d’une URL, telles que les paramètres de requête, du robot de recherche. Par défaut, aucune règle n’est spécifiée et aucune réécriture d’URL n’est effectuée.

Lorsqu’un site Web est analysé, les URL de contenu incorporées sont stockées dans une liste temporaire de pages Web supplémentaires à analyser. Lorsque le robot de recherche récupère une URL de la liste, les règles de récupération de réécriture sont utilisées pour manipuler des parties de cette URL. En règle générale, les règles de récupération sont utilisées pour insérer des données sensibles au temps dans une URL. Il s’agit de l’URL finale utilisée pour récupérer la page de votre site Web.

Les règles de réécriture ne sont nécessaires que si les URL contiennent des données dynamiques, comme un ID de session, et si ces données dynamiques changent au fil du temps pour rester valides. Dans ce cas, vous utilisez les règles de réécriture du magasin pour obtenir l’état le plus récent des données à partir des URL rencontrées. Ensuite, vous utilisez les règles de récupération des réécritures pour ajouter ces données à chaque URL lorsque les robots de recherche récupèrent la page.

Chaque règle est spécifiée avec une directive de règle de réécriture (RewriteRule) et une ou plusieurs conditions de réécriture facultatives (RewriteCond). L&#39;ordre des règles est important. Le jeu de règles est bouclé règle par règle. Lorsqu’une règle correspond, elle effectue une boucle dans toutes les conditions de réécriture correspondantes. Une règle d’URL d’analyse est spécifiée de la manière suivante :

```
RewriteCond TestString CondPattern [Flags] 
RewriteRule Pattern Substitution [Flags]
```

Lorsqu’une URL incorporée est rencontrée, le robot de recherche tente de faire correspondre l’URL au Modèle de chaque règle d’analyse. Si le modèle correspond, le moteur de réécriture recherche les directives RewriteCond correspondantes. Si aucune condition n’est présente, l’URL est remplacée par une nouvelle valeur construite à partir de la chaîne de substitution et continue avec la règle suivante dans le jeu de règles. Si des conditions existent, elles sont traitées dans l’ordre dans lequel elles sont répertoriées. Le moteur de réécriture tente de faire correspondre un modèle de condition (CondPattern) à une chaîne de test (TestString). Si les deux correspondent, la condition suivante est traitée jusqu’à ce qu’aucune condition supplémentaire ne soit disponible. Si toutes les conditions correspondent, l’URL est remplacée par la Substitution spécifiée dans la règle. Si la condition n’est pas remplie, l’ensemble complet des conditions et la règle correspondante échoue.

## À propos des directives RewriteRule {#section_32B24B29627946398AFBC5F869A610CB}

Une directive RewriteRule a la forme suivante :

```
           
<i>RewriteRule Pattern Substitution [Flags]</i> 
        
```

`Pattern` peut être une expression régulière POSIX, qui est appliquée à l’URL active. L’&quot;URL active&quot; peut différer de l’URL demandée d’origine, car des règles antérieures ont peut-être déjà correspondu et modifié l’URL.

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Vous ne pouvez pas utiliser le caractère &quot;pas&quot; (&#39;!&#39;) pour préfixer le modèle. Le caractère &quot;pas&quot; vous permet de nier un modèle, c’est-à-dire d’être vrai uniquement si l’URL active ne correspond PAS à ce modèle. Le caractère &quot;pas&quot; peut être utilisé lorsqu’il est préférable de faire correspondre un modèle négatif ou comme règle par défaut finale.

>[!NOTE]
>
>Vous ne pouvez pas utiliser à la fois le caractère &quot;pas&quot; et les caractères génériques groupés dans un modèle. En outre, vous ne pouvez pas utiliser un modèle dégradé lorsque la chaîne de substitution contient $N.

Vous pouvez utiliser des parenthèses pour créer une référence dans le modèle, qui peut être référencée par Substitution et CondPattern.

**** SubstitutionL&#39;URL est remplacée par la chaîne de substitution, qui contient les éléments suivants :

Texte ordinaire : Texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Voici les deux types de références arrière :

* **RéécrireRègle** Références arrière Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0)  &lt;> Par exemple, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2.`

* ** Réécrivez les références arrière de Cond** Ces références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et prennent la forme %N (0 &lt;= N &lt;= 9).

Variables : Il s’agit de variables au format %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE est une chaîne pour le nom d’une variable définie. Pour plus d&#39;informations sur la définition des variables d&#39;environnement, consultez l&#39;indicateur *[E]*.

Fonctions : Il s&#39;agit de fonctions du formulaire ${NAME_OF_FUNCTION:key} dont NAME_OF_FUNCTION est le suivant :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* escape URL code tous les caractères dans *key*.
* Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; ne sont pas modifiés ; les espaces sont convertis en &quot;+&quot; et tous les autres caractères sont convertis en leur équivalent codé URL %xx.
* unescape convertit &#39;+&#39; en espace et tous les caractères codés dans l’URL %xx en caractères uniques.

>[!NOTE]
>
>Il existe une chaîne de substitution spéciale : &#39;-&#39; signifie &quot;aucune substitution&quot;. La chaîne &quot;-&quot; est souvent utilisée avec l’indicateur C (chain), ce qui vous permet de faire correspondre une URL à plusieurs modèles avant qu’une substitution ne se produise.

**Indicateurs**

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Dernière règle. </p> <p>Arrête le processus de réécriture et n’applique aucune règle de réécriture supplémentaire. Utilisez cet indicateur pour empêcher tout traitement ultérieur de l’URL active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Prochain tour. </p> <p> Réexécute le processus de réécriture (en commençant à nouveau par la première règle de réécriture) en utilisant l’URL de la dernière règle de réécriture (et non l’URL d’origine). Veillez à ne pas créer de boucle d'arrêt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Enchaîné avec la règle suivante. </p> <p>Chaine la règle actuelle à la règle suivante (qui peut également être liée à la règle suivante, etc.). Si une règle correspond, le processus de substitution se poursuit comme d’habitude. Si la règle ne correspond pas, toutes les règles chaînées suivantes sont ignorées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Aucun cas. </p> <p> Rend le modèle non sensible à la casse (c’est-à-dire qu’il n’y a aucune différence entre "A-Z" et "a-z") lorsque le modèle est comparé à l’URL active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignore la ou les règles suivantes. </p> <p> Si la règle actuelle correspond, cet indicateur force le moteur de réécriture à ignorer les règles num suivantes dans le jeu de règles. Utilisez cet indicateur pour faire des constructions pseudo-alors-sinon. La dernière règle de la clause then-clause devient skip=N où N est le nombre de règles de la clause else. </p> <p> <p>Remarque :  Ce drapeau n'est pas le même que le drapeau 'chain|C' !) </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Définit la variable environnementale. </p> <p>Crée une variable d’environnement "VAR" définie sur la valeur VAL, où VAL peut contenir des références arrière d’expressions régulières, $N et %N, qui sont développées. Vous pouvez utiliser cet indicateur plusieurs fois pour définir plusieurs variables. Les variables peuvent être ultérieurement déréférencées dans un modèle RewriteCond suivant via %{VAR}. </p> <p>Utilisez cet indicateur pour supprimer et mémoriser les informations des URL. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Les règles de réécriture de magasin et les règles de réécriture de récupération partagent des valeurs de variable. En raison de ce comportement, vous pouvez définir une variable sur une valeur de sessionid sensible au temps lorsqu’une URL incorporée est rencontrée et stockée. Lorsque l’URL suivante est récupérée à partir de la liste d’enregistrement temporaire, la dernière valeur de l’ID de session peut y être ajoutée avant la récupération de cette page.

**Exemple de RewriteRule avec une fonction**

Supposons que vous disposez d’un serveur sensible à la casse, qui gère les chaînes &quot;www.mydomain.com&quot; et &quot;www.MyDomain.com&quot; différemment. Pour que votre serveur fonctionne correctement, assurez-vous que le domaine est toujours &quot;www.mydomain.com&quot;, même si certains documents contiennent des liens faisant référence à &quot;www.MyDomain.com&quot;. Pour ce faire, vous pouvez utiliser la règle suivante :

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2
```

Cette règle de réécriture utilise la fonction `tolower` pour réécrire la partie domaine d’une URL afin de s’assurer qu’elle est toujours en minuscules, comme dans l’exemple suivant :

1. Le modèle `(^https://([^/]*)(.*)$)` contient une référence ** `([^/]*)`* qui correspond à tous les caractères entre `https://` et le premier `/` de l’URL. Le modèle contient également une deuxième référence `(.*)` qui correspond à tous les caractères restants de l’URL.
1. La Substitution `(https://${tolower:$1}$2)` indique au moteur de recherche de réécrire l&#39;URL en utilisant la fonction `tolower` sur la première référence arrière `(https:// ${tolower:$1}$2)`, en laissant le reste de l&#39;URL intact `(https://${tolower:$1} $2)`.

Par conséquent, une URL du formulaire `https://www.MyDomain.com/INTRO/index.Html` est réécrite en tant que `https://www.mydomain.com/INTRO/index.Html`.

## À propos des directives RewriteCond {#section_ADD642A24B68452CB98294A0BD687EC3}

La directive RewriteCond définit une condition de règle. Lorsqu&#39;un RewriteCond précède un RewriteRule, la règle n&#39;est utilisée que si son modèle correspond au titre actuel et que les conditions supplémentaires s&#39;appliquent. Les conditions de réécriture se présentent comme suit :

```
           
<i>RewriteCond TestString CondPattern [Flags]</i> 
        
```

`TestString` est une chaîne qui peut contenir les éléments suivants :

Texte ordinaire : Texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Voici les deux types de références arrière :

* **RéécrireRègle** Références arrière Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0)  &lt;> Par exemple, `RewriteRule ^https:// ([^/]*) (.*)$ https://${tolower: $1} $2`.

* **RéécrireCond** RéférencesRéférencesCes références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et se présentent sous la forme %N (0&lt;>

Variables : Il s’agit de variables au format %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE peut être une chaîne pour le nom d’une variable définie. Voir l&#39;indicateur RewriteRule *`[E]`* pour plus d&#39;informations sur la définition de variables.

Fonctions : Il s&#39;agit de fonctions du formulaire ${NAME_OF_FUNCTION:key} dont NAME_OF_FUNCTION est le suivant :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* L’URL d’échappement code tous les caractères de la clé. Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; restent inchangés, les espaces sont traduits en &#39;+&#39; et tous les autres caractères sont transformés en leur équivalent codé URL %xx.
* unescape rétablit &#39;+&#39; dans l&#39;espace et tous les caractères d&#39;encodage de l&#39;URL %xx sont réencodés en caractères uniques.

**** CondPatternest une Expression régulière étendue standard avec quelques ajouts. La chaîne de modèle peut être précédée d&#39;un &#39;!&#39; caractère (point d’exclamation) pour spécifier un modèle qui ne correspond pas. Vous pouvez utiliser l’une des variantes spéciales suivantes plutôt que de véritables chaînes d’expression régulières :

>[!NOTE]
>
>Vous pouvez également ajouter un point d’exclamation (&#39;!&#39;) au préfixe de tous ces tests. pour nier leur sens.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexiquement moins. </p> <p> Traite le CondPattern comme une chaîne simple et le compare lexiquement à TestString. True si TestString est lexiquement inférieur à CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexiquement plus grand. </p> <p> Traite le CondPattern comme une chaîne simple et le compare lexiquement à TestString. True si TestString est lexiquement supérieur à CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Lexiquement égal. </p> <p> Traite le CondPattern comme une chaîne simple et le compare lexiquement à TestString. True si TestString est lexical égal à CondPattern, c'est-à-dire que les deux chaînes sont exactement égales (caractère par caractère). Si CondPattern n'est que "" (deux guillemets), ceci compare TestString à la chaîne vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Indicateurs**
 (facultatifs) Placez les indicateurs entre crochets  `[]`. Plusieurs indicateurs sont séparés par des virgules.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Aucun cas. </p> <p>Cet indicateur rend le test non sensible à la casse, c'est-à-dire qu'il n'y a aucune différence entre "A-Z" et "a-z" à la fois dans TestString développé et dans CondPattern. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p>Ou la condition suivante. </p> <p>Utilisez cet indicateur pour combiner des conditions de règle avec un OU local au lieu de l’ET implicite. Sans cet indicateur, vous devrez écrire le cond/la règle plusieurs fois. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**

Certaines pages Web attribuent une variable CGI &quot;sessionid&quot; la première fois qu’un visiteur arrive sur un site. Cette variable sert à identifier le visiteur et, lorsque le visiteur parcourt le site, elle est transmise. Comme le robot de recherche ressemble à un visiteur de votre site, un numéro &quot;sessionid&quot; lui est attribué. Le robot de recherche conserve cette seule valeur &quot;sessionid&quot;, même si une seconde page du site tente d’attribuer une nouvelle valeur. Pour ce faire, vous devez réécrire deux règles.

La première règle sert à identifier et à stocker la variable sessionid :

```
RewriteCond  %{sessionid}  !.+ 
RewriteRule  ^.+sessionid= 
<b>([^&#]+)</b>.*$  -   
<i>[E=sessionid:$1]</i>
```

La règle RewriteRule utilise un indicateur E `([E=sessionid:$1])` pour affecter la valeur actuelle du paramètre CGI sessionid à la variable `sessionid`. `$1` fait référence à la première référence arrière, qui se trouve entre le premier jeu de parenthèses dans le modèle `([^&#]+)` de RewriteRule.

L’expression régulière `^&#]+` correspond à la partie d’une URL située entre le mot `sessionid` et le caractère suivant**&amp;**ou**#**caractère. Dans la mesure où cette règle RewriteRule est utilisée uniquement pour créer la valeur initiale de la variable sessionid, elle ne réécrit pas. Notez que le champ Substitution de la règle est défini sur `-` pour indiquer qu&#39;aucune réécriture n&#39;est requise.

Le RewriteCond examine la variable `sessionid` ( `%{sessionid}`). S&#39;il n&#39;a même pas un seul caractère (!.+), alors la RewriteRule correspond.

Cette règle permet de lire l’URL en tant que `https://www.domain.com/home/?sessionid=1234&function=start` et d’affecter la valeur `1234` à la variable `sessionid`.

La deuxième règle est utilisée pour réécrire toutes les URL qui correspondent au modèle de règle de réécriture suivant :

```
RewriteRule   
<b>^(.+)</b>sessionid=[^&#]+ 
<i>(.*)$</i>  $1sessionid=%{sessionid}$2
```

Le modèle RewriteRule contient deux références arrière : `(.+)` et `(.*)`. La première référence arrière correspond à tous les caractères précédant `sessionid`. La seconde référence correspond à tous les caractères après la fin de `&` ou `#`.

Le modèle de substitution réécrit l&#39;URL à l&#39;aide de la première référence arrière, suivie de la chaîne &quot;sessionid=&quot;, suivie de la valeur de la variable d&#39;ID de session définie par la première règle `%{sessionid}`, suivie de la seconde référence arrière. `($1sessionid=%{sessionid} $2)`

Notez que cette RewriteRule ne contient pas de RewriteCond. De ce fait, elle provoque une réécriture pour toutes les URL qui correspondent à la règle de réécriture *Pattern*. Ainsi, si la valeur de la variable sessionid ( `%{sessionid}`) est `1234`, une URL de la forme `https://www.domain.com/products/?sessionid=5678&function=buy` est réécrite en tant que `https://www.domain.com/products/?sessionid=1234&function=buy`

## Remerciements {#section_EC3A1DAEB5A54C93A265CB119DF91E9F}

Le logiciel du moteur de réécriture a été développé à l&#39;origine par Apache Group pour être utilisé dans le projet de serveur Apache HTTP (https://www.apache.org/).

## Ajouter les règles d&#39;URL de récupération de la liste d&#39;analyse {#task_94A28ED7DC404BFF9767DBB5ADEE6B7A}

Vous pouvez ajouter des règles de récupération d’URL de la liste d’analyse afin de spécifier comment les URL rencontrées dans le contenu Web sont réécrites. Les règles de réécriture ne sont nécessaires que si les URL contiennent des données dynamiques, telles qu’un ID de session, et si ces données dynamiques changent au fil du temps pour rester valides.

<!-- 

t_adding_crawl_list_retrieve_url_rules.xml

 -->

**Pour ajouter des règles d’URL de récupération de liste d’analyse**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl List Retrieve URL Rules]**.
1. Dans le champ [!DNL Crawl List Retrieve URL Rules], entrez les règles de votre choix.

   Les lignes vierges et les lignes de commentaire commençant par le caractère &quot;#&quot; (hachage) sont autorisées.
1. (Facultatif) Sur la page [!DNL Crawl List Retrieve URL Rules], dans le champ [!DNL Test Crawl List Retrieve URL Rules], saisissez une URL de test dont vous souhaitez tester les règles d’analyse, puis cliquez sur **Test**.
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Crawl List Retrieve URL Rules], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des règles de titre d&#39;analyse {#concept_BD3A576987DA4D93A998B0B9CDDC3C79}

Les règles de titre d&#39;analyse indiquent comment les titres rencontrés dans le contenu Web sont réécrits avant d&#39;être stockés dans l&#39;index de recherche.

<!-- 

c_about_crawl_title_rules.xml

 -->

Par exemple, vous pouvez utiliser une règle de réécriture pour supprimer une partie d’un titre, tel qu’un nom d’organisation. Lorsqu’un site Web est analysé, les titres rencontrés sont stockés dans un tampon temporaire. Toutefois, avant qu’un titre ne soit ajouté à ce tampon, les règles de titre lui sont appliquées. Par défaut, la recherche/marchandisage sur le site ne comporte aucune règle de titre d’analyse et n’apporte aucune modification au titre.

Avant que les effets des règles ne soient visibles par les clients, recréez l’index de votre site.

Vous pouvez rapidement annuler les modifications apportées aux règles de titre d’analyse à l’aide de la fonction Historique.

Les règles peuvent se composer de deux éléments principaux : la RewriteRule et la RewriteCond facultative. Vous pouvez spécifier un nombre illimité de règles et de conditions. L’ordre de ces règles est important car le jeu de règles est bouclé règle par règle. Lorsqu’une règle correspond, elle passe en boucle toutes les conditions de réécriture correspondantes (facultatives). Les règles d’analyse d’URL sont spécifiées de la manière suivante :

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Lorsqu’un titre est rencontré, le robot de recherche tente de faire correspondre le titre au Modèle de chaque règle d’analyse. Si le modèle correspond, le moteur de réécriture recherche les directives RewriteCond correspondantes. Si aucune condition n’est présente, l’URL est remplacée par une nouvelle valeur construite à partir de la chaîne de substitution et continue avec la règle suivante dans le jeu de règles. Si des conditions existent, elles sont traitées dans l’ordre dans lequel elles sont répertoriées. Le moteur de réécriture tente de faire correspondre un modèle de condition (CondPattern) à une chaîne de test (TestString). Si les deux correspondent, la condition suivante est traitée jusqu’à ce qu’aucune condition supplémentaire ne soit disponible. Si toutes les conditions correspondent, l’URL est remplacée par la Substitution spécifiée dans la règle. Si la condition n’est pas remplie, l’ensemble complet des conditions et la règle correspondante échoue.

Saisissez les règles d’URL d’analyse dans la zone de texte, puis cliquez sur Enregistrer les modifications. Les lignes vierges et les lignes de commentaire commençant par le caractère &quot;#&quot; (hachage) sont autorisées. Pour tester les règles de recherche, vous pouvez entrer une URL de test dans la zone de texte &quot;Tester les règles de réécriture&quot;, puis cliquer sur Tester.

## Directive RewriteRule {#section_669445C505754E838E14029D6583D9B6}

Chaque directive RewriteRule définit une règle de réécriture. Les règles sont appliquées dans l’ordre dans lequel elles sont répertoriées. Une règle de réécriture se présente comme suit :

```
RewriteRule Pattern Substitution [Flags]
```

**** Patternpeut être une expression régulière POSIX, qui est appliquée au titre actuel. Le &quot;titre actuel&quot; est différent du titre d’origine, car les règles antérieures l’ont déjà mis en correspondance et modifié.

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Vous pouvez utiliser le caractère &quot;pas&quot; (&#39;!&#39;) pour préfixer le modèle. Le caractère &quot;pas&quot; vous permet de nier un modèle, c’est-à-dire d’être vrai uniquement si le titre actuel ne correspond PAS au modèle. Le caractère &quot;pas&quot; peut être utilisé lorsqu’il est préférable de faire correspondre un modèle négatif ou comme règle par défaut finale. Remarque : Vous ne pouvez pas utiliser à la fois le caractère &quot;pas&quot; et les caractères génériques groupés dans un modèle. En outre, vous ne pouvez pas utiliser un modèle dégradé lorsque la chaîne de substitution contient $N.

Vous pouvez utiliser des parenthèses pour créer une référence arrière, qui peut être référencée par Substitution et CondPattern.

**** SubstitutionLe titre est remplacé par la chaîne de substitution. La chaîne peut contenir les éléments suivants :

Texte ordinaire : texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Voici deux types de références arrière :

* Réécrire les références arrière de règle

   Ces références arrière correspondent dans le modèle RewriteRule correspondant et prennent la forme $N (0 &lt;= N &lt;= 9). Par exemple, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* Réécrire les références arrière de Cond

   Ces références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et prennent la forme %N (0 &lt;= N &lt;= 9).

Variables Il s’agit de variables sous la forme %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE peut être une chaîne pour le nom d’une variable définie. Consultez l&#39;indicateur `[E]` pour plus d&#39;informations sur la définition des variables d&#39;environnement.

Fonctions Il s&#39;agit des fonctions du formulaire ${NAME_OF_FUNCTION : key} où NAME_OF_FUNCTION est :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.

>[!NOTE]
>
>Il existe une chaîne de substitution spéciale : &#39;-&#39; signifie &quot;aucune substitution&quot;. La chaîne &quot;-&quot; est souvent utile avec l&#39;indicateur C (chain), ce qui vous permet de faire correspondre un titre à plusieurs modèles avant qu&#39;une substitution ne se produise.

**Indicateurs**  (facultatif)

Les indicateurs sont placés entre crochets `[]`et plusieurs indicateurs sont séparés par des virgules :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Dernière règle. </p> <p> Arrête le processus de réécriture et n’applique aucune règle de réécriture supplémentaire. Utilisez cet indicateur pour empêcher tout traitement ultérieur du titre actuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Prochain tour. </p> <p> Réexécute le processus de réécriture (en commençant à nouveau par la première règle de réécriture) en utilisant le titre de la dernière règle de réécriture, et non le titre d’origine. Veillez à ne pas créer de boucle morte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Enchaîné avec la règle suivante. </p> <p>Chaine la règle actuelle à la règle suivante (qui peut également être liée à la règle suivante, etc.). Si une règle correspond, le processus de substitution se poursuit comme d’habitude. Si la règle ne correspond pas, toutes les règles chaînées suivantes sont ignorées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Aucun cas. </p> <p>Rend le modèle non sensible à la casse (c’est-à-dire qu’il n’y a aucune différence entre "A-Z" et "a-z") lorsque le modèle est comparé au titre actuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignore la ou les règles suivantes. </p> <p> Si la règle actuelle correspond, cet indicateur force le moteur de réécriture à ignorer les règles num suivantes dans le jeu de règles. Utilisez-le pour faire des constructions pseudo-alors-sinon. La dernière règle de la clause then-clause devient skip=N où N est le nombre de règles de la clause else. (Remarque : Ce n'est pas la même chose que le drapeau 'chain|C' !) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Définissez la variable environnement. </p> <p> Crée une variable d’environnement "VAR" définie sur la valeur VAL, où VAL peut contenir des références arrière d’expressions régulières, $N et %N, qui est développée. Vous pouvez utiliser cet indicateur plusieurs fois pour définir plusieurs variables. Les variables peuvent être référencées ultérieurement dans un modèle RewriteCond suivant via %{VAR}. Utilisez cet indicateur pour retirer et mémoriser les informations des titres. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Directive RewriteCond (facultatif) {#section_D664B71DE3884E0790531804C49A3222}

La directive RewriteCond définit une condition de règle. Lorsqu&#39;un RewriteCond précède un RewriteRule, la règle n&#39;est utilisée que si son modèle correspond au titre actuel et que les conditions supplémentaires s&#39;appliquent.

Les directives de condition de réécriture se présentent comme suit :

```
RewriteCond TestString CondPattern [Flags] 
```

**** TestStringest une chaîne qui peut contenir les éléments suivants :

Texte ordinaire : texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Il existe deux types de références arrière :

* Réécrire les références arrière de règle Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0 &lt;= N &lt;= 9). Par exemple, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`
* RéécrireCond Références de renvoi Ces références de renvoi correspondent dans le dernier CondPattern RewriteCond correspondant et prennent la forme %N (0 &lt;= N &lt;= 9).

Variables Il s’agit de variables sous la forme %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE peut être une chaîne pour le nom d’une variable définie. Pour plus d&#39;informations sur la définition des variables d&#39;environnement, consultez l&#39;indicateur `[E]`.

Fonctions Il s&#39;agit des fonctions du formulaire ${NAME_OF_FUNCTION:key} dont NAME_OF_FUNCTION est :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* L’URL d’échappement code tous les caractères de la clé.
* Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; restent inchangés, les espaces sont traduits en &#39;+&#39; et tous les autres caractères sont transformés en leur équivalent codé URL %xx.
* unescape convertit &#39;+&#39; en espace et tous les caractères codés dans l’URL %xx en caractères uniques.

**** CondPatternest une Expression régulière étendue standard avec quelques ajouts. La chaîne de modèle peut être précédée d&#39;un &#39;!&#39; caractère (point d’exclamation) pour spécifier un modèle qui ne correspond pas. Vous pouvez utiliser l’une des variantes spéciales suivantes plutôt que de vraies chaînes d’expression régulières.

>[!NOTE]
>
>Vous pouvez ajouter un point d’exclamation (&#39;!&#39;) au préfixe de tous ces tests. pour nier leur sens.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Est lexiquement moins. </p> <p>Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexiquement inférieur à <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Est lexiquement plus grand. </p> <p>Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexiquement supérieur à <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p> Est lexiquement égal. </p> <p>Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexiquement égal à <i>CondPattern</i>, c'est-à-dire que les deux chaînes sont exactement égales (caractère par caractère). Si <i>CondPattern</i> n'est que "" (deux guillemets), <i>TestString</i> est comparé à la chaîne vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Indicateurs**  (facultatif)

Les indicateurs sont placés entre crochets `[]`et plusieurs indicateurs sont séparés par des virgules :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Aucun cas. </p> <p> Rend le test non sensible. En d'autres termes, il n'y a aucune différence entre "A-Z" et "a-z" dans le <i>TestString</i> étendu et dans le <i>CondPattern.</i> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' </p> </td> 
   <td colname="col2"> <p> Ou la condition suivante. </p> <p>Utilisez cet indicateur pour combiner des conditions de règle avec un OU local au lieu de l’ET implicite. Sans cet indicateur, vous devrez écrire le cond/la règle plusieurs fois. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Exemple**

Supposons que vous disposez d&#39;un site Web d&#39;entreprise avec un format de titre standard : &quot;Ma Société&quot; suivie d’un trait d’union, puis d’une description spécifique à la page (&quot;Ma Société - Bienvenue&quot; ou &quot;Ma Société - Nouvelles&quot;, par exemple). Vous voulez retirer &quot;Ma Société -&quot; du titre et convertir le titre entier en lettres majuscules lorsqu&#39;il indexe le site.

La règle de réécriture suivante utilise la fonction toupper pour réécrire uniquement la partie descriptive d’un titre en majuscules :

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>}
```

Le modèle de la règle `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` contient une référence arrière `(.*)` qui correspond au contenu du titre qui suit &quot;Ma Société-&quot;. N&#39;oubliez pas que le fait d&#39;entourer une partie d&#39;un modèle avec une parenthèse ( ) crée une référence arrière qui peut être référencée par la Substitution. Dans cet exemple, la Substitution (${toupper:**$1**}) réécrit cette référence arrière (**$1**) à l’aide de la fonction toupper.

Ainsi, le titre du formulaire &quot;Ma Société - Bienvenue&quot; est réécrit en &quot;BIENVENUE&quot;.

**Remerciements**

Le logiciel du moteur de réécriture a été développé à l&#39;origine par Apache Group pour être utilisé dans le projet de serveur Apache HTTP (https://www.apache.org/).

## Ajouter les règles de titre d&#39;analyse {#task_272BB4C603BA4C9ABDBEEB398798B101}

Vous pouvez ajouter des règles de titre d’analyse pour indiquer comment les titres rencontrés dans le contenu Web sont réécrits avant d’être stockés dans l’index de recherche.

<!-- 

t_adding_crawl_title_rules.xml

 -->

**Pour ajouter des règles de titre d’analyse**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Crawl Title Rules]**.
1. Dans le champ [!DNL Crawl Title Rules], entrez les règles de votre choix.

   Les lignes vierges et les lignes de commentaire commençant par le caractère &quot;#&quot; (hachage) sont autorisées.
1. (Facultatif) Sur la page [!DNL Crawl Title Rules], dans le champ [!DNL Test Crawl Title Rules], saisissez une URL de test dont vous souhaitez tester les règles de recherche, puis cliquez sur **Test**.
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Crawl Title Rules], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des règles d&#39;URL de recherche {#concept_017EC95E68844B6C8CC9F874F0EC8D3C}

Les règles d’URL de recherche spécifient comment les URL des résultats de recherche de votre site Web doivent s’afficher. Les règles fonctionnent sur des URL complètes. Il est possible de manipuler n’importe quelle partie de l’URL, y compris les arguments de requête dans lesquels les informations d’ID de session sont souvent conservées.

<!-- 

c_about_search_url_rules.xml

 -->

En règle générale, les règles d’URL de recherche sont utilisées pour insérer un ID de session dans une URL. Cependant, vous pouvez également utiliser des règles d’URL de recherche pour modifier le nom de domaine affiché avec vos résultats. Par défaut, aucune règle n’est spécifiée et aucune modification d’URL n’est effectuée.

Les règles d’URL de recherche peuvent se composer de deux éléments principaux : la RewriteRule et la RewriteCond facultative. Lorsqu’une URL est incluse dans le résultat d’une recherche, les règles sont utilisées pour la manipuler. Vous pouvez spécifier un nombre illimité de règles et de conditions d’URL de recherche. L’ordre de ces règles est important car le jeu de règles est bouclé par règle. Lorsqu’une règle correspond, le logiciel effectue une boucle dans toutes les conditions de réécriture correspondantes (facultatives). Les règles d’analyse d’URL sont spécifiées de la manière suivante :

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Lors du traitement d’une URL, la recherche/marchandisage sur le site tente de la faire correspondre au Modèle de chaque règle de recherche. Si la correspondance échoue, le moteur de réécriture interrompt immédiatement le traitement de la règle et continue avec la règle suivante dans la visionneuse. Si le modèle correspond, le moteur de réécriture recherche les instructions RewriteCond correspondantes. S’il n’existe aucune condition, l’URL est remplacée par une nouvelle valeur. Cette valeur est construite à partir de la chaîne de substitution et continue avec la règle suivante dans le jeu de règles. S’il existe des conditions, l’ordre dans lequel elles sont répertoriées est leur mode de traitement. Le moteur de réécriture tente de faire correspondre un modèle de condition (CondPattern) à une chaîne de test (TestString). Si les deux correspondent, la condition suivante est traitée jusqu’à ce qu’aucune condition supplémentaire ne soit disponible. Si toutes les conditions correspondent, l’URL est remplacée par la Substitution spécifiée dans la règle. Si la condition n’est pas remplie, l’ensemble complet des conditions et la règle correspondante échoue.

## À propos de la directive RewriteRule {#section_A3473B5B90B74DA1970213113A90591E}

Une règle de réécriture se présente comme suit :

```
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

**Le** modèle peut être une expression régulière POSIX, qui est appliquée à l’URL active. L’&quot;URL active&quot; peut différer de l’URL d’origine, car des règles antérieures ont peut-être déjà fait la correspondance et l’ont modifiée.

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Vous pouvez utiliser le caractère &quot;pas&quot; (&#39;!&#39;) pour préfixer le modèle. Le caractère &quot;pas&quot; vous permet de nier un modèle. En d’autres termes, elle n’est vraie que si l’URL active ne correspond PAS au modèle. Vous pouvez utiliser le caractère &quot;pas&quot; lorsqu’il est préférable de faire correspondre un modèle négatif ou comme règle par défaut finale. Notez que vous ne pouvez pas utiliser à la fois le caractère &quot;pas&quot; et les caractères génériques groupés dans un modèle. En outre, vous ne pouvez pas utiliser un modèle dégradé lorsque la chaîne de substitution contient $N.

Vous pouvez utiliser des parenthèses pour créer une référence arrière, qui peut être référencée par Substitution et CondPattern.

**** SubstitutionL&#39;URL est complètement remplacée par la chaîne de substitution, qui peut contenir les éléments suivants :

Texte ordinaire : texte transmis sans modification.

Références arrière Fournit un accès aux parties groupées (entre parenthèses internes) du modèle ou du modèle de configuration. Il existe deux types de références arrière :

Réécrire les références arrière de règle Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0 &lt;= N &lt;= 9). Par exemple, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

RéécrireCond Références arrière - Ces références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et se présentent sous la forme %N (0 &lt;= N &lt;= 9).

Fonctions : Il s&#39;agit des fonctions du formulaire ${NAME_OF_FUNCTION:key} où NAME_OF_FUNCTION est :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* escape URL code tous les caractères dans *key*.
* Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; ne sont pas modifiés ; les espaces sont traduits en &quot;+&quot;; tous les autres caractères sont transformés en leur équivalent codé URL %xx.
* unescape convertit &#39;+&#39; en espace et tous les caractères codés dans l’URL %xx en caractères uniques.

>[!NOTE]
>
>Il existe une chaîne de substitution spéciale : &#39;-&#39; signifie &quot;aucune substitution&quot;. La chaîne &quot;-&quot; est souvent utile en association avec l&#39;indicateur C (chain). Il vous permet de faire correspondre une URL à plusieurs modèles avant qu’une substitution ne se produise.

**Indicateurs**  (facultatif)

Les indicateurs sont placés entre crochets `[]`et plusieurs indicateurs sont séparés par des virgules :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p>Dernière règle. </p> <p> Arrêtez le processus de réécriture et n’appliquez aucune règle de réécriture supplémentaire. Utilisez cet indicateur pour empêcher tout traitement ultérieur de l’URL active. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p> Prochain tour. </p> <p>Réexécutez le processus de réécriture (en commençant à nouveau par la première règle de réécriture) en utilisant l’URL de la dernière règle de réécriture (et non l’URL d’origine). Attention à ne pas créer une boucle morte ! </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p> Enchaîné avec la règle suivante. </p> <p>Cet indicateur enchaîne la règle actuelle à la règle suivante, qui peut également être liée à la règle suivante, etc. Si une règle correspond, le processus de substitution se poursuit comme d’habitude. Si la règle ne correspond pas, toutes les règles chaînées suivantes sont ignorées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p>Aucun cas. </p> <p>Cet indicateur rend le modèle insensible à la casse. En d’autres termes, il n’y a aucune différence entre "A-Z" et "a-z" lorsque le modèle est comparé à l’URL actuelle. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p>Ignore la ou les règles suivantes. </p> <p> Si la règle actuelle correspond, cet indicateur force le moteur de réécriture à ignorer les règles num suivantes dans le jeu de règles. Utilisez-le pour faire des constructions pseudo-alors-sinon. La dernière règle de la clause then-clause devient skip=N où N est le nombre de règles de la clause else. (Remarque : Ce n'est pas la même chose que le drapeau 'chain|C' !) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Définissez une variable environnementale. </p> <p> Cet indicateur crée une variable d’environnement "VAR" définie sur la valeur VAL. VAL peut contenir des références arrière d'expressions régulières, $N et %N, qui sont développées. Vous pouvez utiliser cet indicateur plusieurs fois pour définir plusieurs variables. Les variables peuvent être ultérieurement déréférencées dans un modèle RewriteCond suivant via %{VAR}. Utilisez cet indicateur pour supprimer et mémoriser les informations des URL. </p> </td> 
  </tr> 
 </tbody> 
</table>

Notez que les règles de réécriture de magasin et les règles de réécriture de récupération partagent des valeurs de variable. C’est pourquoi vous pouvez définir une variable sur une valeur de sessionid sensible au temps lorsqu’une URL incorporée est rencontrée et stockée. Lorsque l’URL suivante est récupérée à partir de la liste d’enregistrement temporaire, la dernière valeur de l’ID de session peut y être ajoutée avant la récupération de cette page.

**Exemple**

Supposons que vous disposez d’un serveur sensible à la casse. Il gère différemment les chaînes &quot;www.mydomain.com&quot; et &quot;www.MyDomain.com&quot;. Pour que votre serveur fonctionne correctement, vous devez vous assurer que le domaine est toujours &quot;www.mydomain.com&quot;, même si certains documents contiennent des liens faisant référence à &quot;www.MyDomain.com&quot;. Pour ce faire, vous pouvez utiliser la règle suivante :

```
RewriteRule  ^https:// 
<b>([^/]*)</b> 
<i>(.*)</i>$  https://${tolower:$1}$2 
```

Cette règle de réécriture utilise la fonction &quot;tolower&quot; pour réécrire la partie domaine d’une URL afin de s’assurer qu’elle est toujours en minuscules :

1. Le modèle `(^https://([^/]*)(.*)$)` contient une référence **`([^/]*)`** qui correspond à tous les caractères entre &quot;https://&quot; et le premier &quot;/&quot; de l&#39;URL. Le modèle contient également une deuxième référence de renvoi **(.*)** qui correspond à tous les caractères restants de l’URL.

1. La Substitution `(https://${tolower:$1}$2)` indique au moteur de recherche de réécrire l&#39;URL en utilisant la fonction **tolower** sur la première référence arrière `(https://**${tolower:$1**}$2)`, en laissant le reste de l&#39;URL intact `(https://${tolower:$1}*$2*)`.

Par conséquent, une URL du formulaire `https://www.MyDomain.com/INTRO/index.Html` est réécrite en tant que `https://www.mydomain.com/INTRO/index.Html`

**Directive**  RewriteCond (facultative)

La directive RewriteCond définit une condition de règle. Lorsqu&#39;un RewriteCond précède un RewriteRule, la règle n&#39;est utilisée que si son modèle correspond au titre actuel et que les conditions supplémentaires s&#39;appliquent.

Les directives de condition de réécriture se présentent comme suit :

```
RewriteCond  
<i>TestString CondPattern [Flags]</i>
```

** TestStringest une chaîne qui peut contenir les éléments suivants :

Texte ordinaire : Texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Il existe deux types de références arrière :

* ** Réécrire les références arrière de règle** Ces références arrière correspondent dans le modèle de règle de réécriture correspondant et prennent la forme $N (0 &lt;= N &lt;= 9). Par exemple, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RéécrireCond** RéférencesRéférencesCes références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et se présentent sous la forme %N (0  &lt;>

Variables Il s’agit de variables sous la forme %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE peut être une chaîne pour le nom d’une variable définie. Voir l&#39;indicateur RewriteRule *`[E]`* pour plus d&#39;informations sur la définition de variables.

>[!NOTE]
>
>Les règles de réécriture utilisent généralement les variables. Tous les paramètres CGI de l’URL active sont automatiquement convertis en variables. Par exemple, l’URL de recherche `"https://search.atomz.com/search/?sp_a=sp00000000&sp_q="Product"&session=1234&id=5678"` fournit automatiquement quatre variables, qui peuvent être référencées dans les règles de réécriture. Dans cet exemple, une variable s’appelle &quot;session&quot; et sa valeur est &quot;1234&quot; tandis qu’une autre variable s’appelle &quot;id&quot; et sa valeur est &quot;5678&quot;. (Les deux autres variables sont `sp_a` et `sp_q`.) Vous devez transmettre toutes les variables nécessaires sous forme de champs masqués dans le formulaire de recherche de votre page Web. Dans cet exemple, vous devez transmettre les valeurs &quot;session&quot; et &quot;id&quot;, qui identifient l&#39;utilisateur du site Web qui effectue la recherche. Pour transmettre un champ masqué au formulaire de recherche, utilisez une balise telle que `<input type=hidden name="session" value="1234">`.

Fonctions Il s&#39;agit des fonctions du formulaire ${NAME_OF_FUNCTION:key} dont NAME_OF_FUNCTION est :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* escape URL code tous les caractères dans *key*. Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; restent inchangés, les espaces sont traduits en &#39;+&#39; et tous les autres caractères sont transformés en leur équivalent codé URL %xx.
* unescape rétablit &#39;+&#39; dans l&#39;espace et tous les caractères d&#39;encodage de l&#39;URL %xx sont réencodés en caractères uniques.

**** CondPatternest une Expression régulière étendue standard avec quelques ajouts. La chaîne de modèle peut être précédée d&#39;un &#39;!&#39; caractère (point d’exclamation) pour spécifier un modèle qui ne correspond pas. Vous pouvez utiliser l’une des variantes spéciales suivantes plutôt que de vraies chaînes d’expression régulières.

Vous pouvez préfixer tous ces tests en utilisant un point d’exclamation (&#39;!&#39;) pour nier leur sens.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Est lexiquement moins. </p> <p> Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexiquement inférieur à <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Est lexiquement plus grand. </p> <p> Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexiquement supérieur à <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Est lexiquement égal. </p> <p> Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexical égal à <i>CondPattern</i>. Autrement dit, les deux chaînes sont exactement égales (caractère par caractère). Si <i>CondPattern</i> n'est que "" (deux guillemets), <i>TestString</i> est comparé à la chaîne vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Indicateurs**  (facultatif)

Les indicateurs sont placés entre crochets `[]`et plusieurs indicateurs sont séparés par des virgules :

&#39;nocase|NC&#39; (aucun cas) : Cela rend le test insensible à la casse. En d&#39;autres termes, il n&#39;y a aucune différence entre &quot;A-Z&quot; et &quot;a-z&quot; à la fois dans la *Chaîne de test* étendue et dans la *CondPattern*.

&#39;ornext|OR&#39; (ou condition suivante) : Utilisez cette option pour combiner des conditions de règle avec un OU local au lieu de l’ET implicite. Sans cet indicateur, vous devrez écrire le cond/la règle plusieurs fois.

**Exemple**

Certaines pages Web attribuent une variable CGI &quot;sessionid&quot; la première fois qu&#39;un client arrive sur un site. Cette variable sert à identifier le client et, lorsque le client parcourt le site, elle est transmise. Comme le robot de recherche ressemble à un client sur votre site, un numéro &quot;sessionid&quot; lui est attribué. Le robot de recherche conserve cette seule valeur &quot;sessionid&quot;, même si une seconde page du site tente d’attribuer une nouvelle valeur. Pour ce faire, vous avez besoin de la règle de réécriture suivante :

```
RewriteCond  %{sessionid}  .+ 
RewriteRule  ^ 
<b>(.+)</b>sessionid=[^&#]+ 
<i>(.*)</i>$   
<b>$1</b>sessionid=%{sessionid} 
<i>$2</i>
```

Le modèle RewriteRule contient deux références arrière : (.+) et (.*). La première référence arrière correspond à tous les caractères précédant &quot;sessionid=&quot;. La seconde référence correspond à tous les caractères après la fin de &quot;&amp;&quot; ou &quot;#&quot; de l&#39;ID de session.

Le modèle de substitution réécrit l’URL à l’aide de la première référence arrière, suivie de la chaîne &quot;sessionid=&quot;, suivie de la valeur de la variable d’ID de session, transmise en tant que paramètre CGI dans l’URL, suivie de la seconde référence arrière. `($1sessionid=%{sessionid}$2)`.

Le **RewriteCond** examine la variable sessionid `(%{sessionid})`. Si elle contient au moins un caractère (.+), alors la RewriteRule correspond.

Ainsi, si la requête de recherche est `"https://search.atomz.com/search/?sp_a=sp99999999&sp_q=word&sessionid=5678"`, toutes les URL de résultats de recherche seront réécrites de sorte que la valeur &quot;sessionid&quot; soit &quot;5678&quot; au lieu de la valeur &quot;sessionid&quot; que le robot de recherche a rencontrée lors de l&#39;analyse de votre site et de l&#39;enregistrement des liens.

**Remerciements**

Le logiciel du moteur de réécriture a été développé à l&#39;origine par Apache Group pour être utilisé dans le projet de serveur Apache HTTP (https://www.apache.org/).

## Ajouter les règles d&#39;URL de recherche {#task_50C77D1B53804AEEB20896F74265BD6F}

Vous pouvez ajouter des règles d’URL de recherche pour indiquer comment s’affichent les URL dans les résultats de recherche de votre site Web. Les règles fonctionnent sur des URL complètes. Vous pouvez manipuler n’importe quelle portion de l’URL, y compris les arguments de requête dans lesquels les informations d’ID de session sont souvent conservées.

<!-- 

t_adding_search_url_rules.xml

 -->

**Pour ajouter des règles d’URL de recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search URL Rules]**.
1. Dans le champ [!DNL Search URL Rules], entrez les règles de votre choix.

   Les lignes vierges et les lignes de commentaire commençant par le caractère &quot;#&quot; (hachage) sont autorisées.
1. (Facultatif) Sur la page [!DNL Search URL Rules], dans le champ [!DNL Test Search URL Rules], saisissez une URL de test dont vous souhaitez tester les règles d’analyse, puis cliquez sur **Test**.
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Search URL Rules], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## À propos des règles de titre de recherche {#concept_C72D20F8DFF64EDE809AF4B72797E858}

Les règles de titre de recherche spécifient comment les titres des résultats de recherche de votre site Web s’affichent. Toute partie du titre peut être manipulée.

<!-- 

c_about_search_title_rules.xml

 -->

Une règle de réécriture peut être utilisée pour supprimer une partie d’un titre, tel qu’un nom d’organisation, par exemple. Par défaut, la recherche/marchandisage sur le site ne comporte aucune règle de titre et n’apporte aucune modification au titre.

Les règles de titre peuvent se composer de deux éléments principaux : RewriteRule et facultative RewriteCond. Un nombre illimité de règles et de conditions peut être spécifié. L’ordre de ces règles est important, car le jeu de règles est bouclé par règle. Lorsqu’une règle correspond, le logiciel effectue une boucle dans toutes les conditions de réécriture correspondantes (facultatives). Les règles de titre de recherche sont spécifiées de la manière suivante :

```
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i> 
 
RewriteCond  
<i>TestString CondPattern [Flags]</i> 
RewriteRule  
<i>Pattern Substitution [Flags]</i>
```

Lorsqu’un titre est rencontré, la recherche/marchandisage sur le site tente de le faire correspondre au Modèle de chaque règle d’analyse. Si le modèle correspond, le moteur de réécriture recherche les directives RewriteCond correspondantes. Si aucune condition n’est présente, le titre est remplacé par une nouvelle valeur construite à partir de la chaîne de substitution et continue avec la règle suivante dans le jeu de règles. Si des conditions existent, elles sont traitées dans l’ordre dans lequel elles sont répertoriées. Le moteur de réécriture tente de faire correspondre un modèle de condition (CondPattern) à une chaîne de test (TestString). Si les deux correspondent, la condition suivante est traitée jusqu’à ce qu’aucune condition supplémentaire ne soit disponible. Si toutes les conditions correspondent, l’URL est remplacée par la Substitution spécifiée dans la règle. Si la condition n’est pas remplie, l’ensemble complet des conditions et la règle correspondante échoue.

## Directive RewriteRule {#section_3BF2B0FF89F74A26AE79D68FA3184B9B}

Chaque directive RewriteRule définit une règle de réécriture. Les règles sont appliquées dans l’ordre dans lequel elles sont répertoriées. Une règle de réécriture se présente comme suit :

```
RewriteRule Pattern Substitution [Flags]
```

**** Modèleexpression régulière POSIX, qui est appliquée au titre actuel. Le &quot;titre actuel&quot; peut différer du titre d’origine, car des règles antérieures peuvent déjà avoir été mises en correspondance et modifiées.

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Vous pouvez utiliser le caractère &quot;non&quot; (&#39;!&#39;) pour préfixer le modèle. Le caractère &quot;pas&quot; vous permet de nier un modèle. C&#39;est-à-dire, pour être vrai uniquement si le titre actuel ne correspond PAS au modèle. Le caractère &quot;pas&quot; peut être utilisé lorsqu’il est préférable de faire correspondre un modèle négatif ou comme règle par défaut finale. Remarque : Vous ne pouvez pas utiliser à la fois le caractère &quot;pas&quot; et les caractères génériques groupés dans un modèle. En outre, vous ne pouvez pas utiliser un modèle dégradé lorsque la chaîne de substitution contient $N.

Vous pouvez utiliser des parenthèses pour créer une référence arrière, qui peut être référencée par Substitution et CondPattern.

**** SubstitutionLe titre est complètement remplacé par la chaîne de substitution, qui peut contenir les éléments suivants :

Texte ordinaire : texte transmis sans modification.

**** Références arrièreFournissez un accès aux parties groupées (entre parenthèses internes) du modèle ou du modèle de suite. Voici deux types de références arrière :

* **RéécrireRègle** Références arrière Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0)  &lt;> Par exemple, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* ** Réécrivez les références arrière de Cond** Ces références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et prennent la forme %N (0 &lt;= N &lt;= 9).

**** VariablesIl s’agit de variables au format %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE peut être une chaîne pour le nom d’une variable définie. Pour plus d&#39;informations sur la définition des variables d&#39;environnement, consultez l&#39;indicateur [E]. Les variables peuvent également être définies dans le formulaire de recherche qui a généré les résultats de la recherche.

**** FonctionsIl s&#39;agit de fonctions du formulaire ${NAME_OF_FUNCTION : key} où NAME_OF_FUNCTION est :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.

Il existe une chaîne de substitution spéciale : &#39;-&#39; signifie &quot;aucune substitution&quot;. La chaîne &quot;-&quot; est souvent utile en association avec l&#39;indicateur C (chain), ce qui vous permet de faire correspondre un titre à plusieurs modèles avant qu&#39;une substitution ne se produise.

**Indicateurs**  (facultatif)

Les indicateurs sont placés entre crochets `[]` et plusieurs indicateurs sont séparés par des virgules :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'last|L' </p> </td> 
   <td colname="col2"> <p> Dernière règle. </p> <p> Arrêtez le processus de réécriture et n’appliquez aucune règle de réécriture supplémentaire. Utilisez cet indicateur pour empêcher tout traitement ultérieur du titre actuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'next|N' </p> </td> 
   <td colname="col2"> <p>Prochain tour. </p> <p> Réexécutez le processus de réécriture (en commençant à nouveau par la première règle de réécriture) en utilisant le titre de la dernière règle de réécriture (et non le titre d’origine !). Veillez à ne pas créer de boucle morte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'chain|C' </p> </td> 
   <td colname="col2"> <p>Enchaîné avec la règle suivante. </p> <p> Cet indicateur enchaîne la règle actuelle à la règle suivante (qui peut également être liée à la règle suivante, etc.). Si une règle correspond, le processus de substitution se poursuit comme d’habitude. Si la règle ne correspond pas, toutes les règles chaînées suivantes sont ignorées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' </p> </td> 
   <td colname="col2"> <p> Aucun cas. </p> <p> Cet indicateur rend le modèle insensible à la casse. En d'autres termes, il n'y a aucune différence entre "A-Z" et "a-z" lorsque le motif est comparé au titre actuel. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'skip|S=num' </p> </td> 
   <td colname="col2"> <p> Ignore la ou les règles suivantes. </p> <p> Si la règle actuelle correspond, cet indicateur force le moteur de réécriture à ignorer les règles num suivantes dans le jeu de règles. Utilisez-le pour faire des constructions pseudo-alors-sinon. La dernière règle de la clause then-clause devient skip=N où N est le nombre de règles de la clause else. (Ce n'est pas la même chose que le drapeau 'chain|C' !) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'env|E=VAR:VAL' </p> </td> 
   <td colname="col2"> <p>Définissez la variable environnement. </p> <p> Cet indicateur crée une variable d'environnement "VAR" définie sur la valeur VAL, où VAL peut contenir des références arrière d'expressions régulières, $N et %N, qui sera développée. Vous pouvez utiliser cet indicateur plusieurs fois pour définir plusieurs variables. Les variables peuvent être référencées ultérieurement dans un modèle RewriteCond suivant via %{VAR}. Utilisez cet indicateur pour retirer et mémoriser les informations des titres. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Directive RewriteCond (facultatif) {#section_9D72B2AB454849A7B681BC39C506AAA3}

La directive RewriteCond définit une condition de règle. Lorsqu&#39;un RewriteCond précède un RewriteRule, la règle n&#39;est utilisée que si son modèle correspond au titre actuel et que les conditions supplémentaires s&#39;appliquent.

Les directives de condition de réécriture se présentent comme suit :

```
RewriteCond TestString CondPattern [Flags]
```

**** TestStringest une chaîne qui peut contenir les éléments suivants :

Texte ordinaire : texte transmis sans modification.

Les références arrière permettent d&#39;accéder aux parties groupées (entre parenthèses internes) du modèle ou du modèle CondPattern. Il existe deux types de références arrière :

* **RéécrireRègle** Références arrière Ces références arrière correspondent dans le modèle RewriteRule correspondant et se présentent sous la forme $N (0)  &lt;> Par exemple, `RewriteRule ^My[[:blank:]] (.*)$ ${toupper: $1}`

* **RéécrireCond** RéférencesRéférencesCes références arrière correspondent dans le dernier CondPattern RewriteCond correspondant et se présentent sous la forme %N (0  &lt;>

**** VariablesIl s’agit de variables au format %{NAME_OF_VARIABLE} où NAME_OF_VARIABLE peut être une chaîne pour le nom d’une variable définie. Consultez l&#39;indicateur `[E]` pour plus d&#39;informations sur la définition des variables d&#39;environnement. Les variables peuvent également être définies dans le formulaire de recherche qui a généré les résultats de la recherche.

**** FonctionsIl s&#39;agit des fonctions du formulaire ${NAME_OF_FUNCTION:key} dont NAME_OF_FUNCTION est :

* tolower fait en minuscule tous les caractères de *key*.
* toupper fait en majuscules tous les caractères de *key*.
* escape URL code tous les caractères dans *key*.
* Les caractères &#39;a&#39;..&#39;z&#39;, &#39;A&#39;..&#39;Z&#39;, &#39;0&#39;..&#39;9&#39;, &#39;*&#39;, &#39;-&#39;, &#39;.&#39;, &#39;/&#39;, &#39;@&#39; et &#39;_&#39; restent inchangés, les espaces sont traduits en &#39;+&#39; et tous les autres caractères sont transformés en leur équivalent codé URL %xx.
* unescape convertit &#39;+&#39; en espace et tous les caractères codés dans l’URL %xx en caractères uniques.

Il existe une chaîne de substitution spéciale : &#39;-&#39; signifie &quot;aucune substitution&quot;. La chaîne &quot;-&quot; est souvent utile en association avec l&#39;indicateur C (chain), ce qui vous permet de faire correspondre une URL à plusieurs modèles avant qu&#39;une substitution ne se produise.

**** CondPatternExpression standard étendue régulière avec quelques ajouts. La chaîne de modèle peut être précédée d&#39;un &#39;!&#39; caractère (point d’exclamation) pour spécifier un modèle qui ne correspond pas. Vous pouvez utiliser l’une des variantes spéciales suivantes plutôt que de vraies chaînes d’expression régulières.

Tous ces tests peuvent également être précédés d&#39;un point d&#39;exclamation (&#39;!&#39;) pour nier leur sens.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne CondPattern </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> '&lt;CondPattern' </p> </td> 
   <td colname="col2"> <p>Est lexiquement moins. </p> <p> Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexiquement inférieur à <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '&gt;CondPattern' </p> </td> 
   <td colname="col2"> <p> Est lexiquement plus grand. </p> <p> Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexiquement supérieur à <i>CondPattern</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> '=CondPattern' </p> </td> 
   <td colname="col2"> <p>Est lexiquement égal. </p> <p> Traite le <i>CondPattern</i> comme une chaîne simple et le compare lexiquement à <i>TestString</i>. True si <i>TestString</i> est lexical égal à <i>CondPattern</i>. Autrement dit, les deux chaînes sont exactement égales (caractère par caractère). Si <i>CondPattern</i> n'est que "" (deux guillemets), <i>TestString</i> est comparé à la chaîne vide. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Indicateurs**  (facultatif)

Les indicateurs sont placés entre crochets`[]` et plusieurs indicateurs sont séparés par des virgules :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Indicateur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> 'nocase|NC' (aucun cas) </p> </td> 
   <td colname="col2"> <p>Rend le test non sensible. En d'autres termes, il n'y a aucune différence entre "A-Z" et "a-z" à la fois dans la <i>chaîne de test</i> développée et dans la <i>configuration de configuration</i>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> 'ornext|OR' (ou condition suivante) </p> </td> 
   <td colname="col2"> <p> Utilisez cette option pour combiner des conditions de règle avec un OU local au lieu de l’ET implicite. Sans cet indicateur, vous devrez écrire le cond/la règle plusieurs fois. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple {#section_E7454FFE169E459AABD9D033651939CB}

Supposons que vous disposez d&#39;un site Web d&#39;entreprise avec un format de titre standard : &quot;Ma Société&quot; suivie d’un trait d’union, puis d’une description spécifique à la page (&quot;Ma Société - Bienvenue&quot; ou &quot;Ma Société - Nouvelles&quot;, par exemple). Vous voulez retirer &quot;Ma Société -&quot; du titre et convertir l&#39;ensemble du titre en lettres majuscules lorsqu&#39;il indexe le site.

La règle de réécriture suivante utilise la fonction toupper pour réécrire uniquement la partie descriptive d’un titre en majuscules :

```
RewriteRule  ^My[[:blank:]]Company[[:blank:]]-[[:blank:]] 
<b>(.*)</b>$  ${toupper: 
<b>$1</b>} 
```

Le modèle de la règle `(^My[[:blank:]]Company[[:blank:]]-[[:blank:]] (.*))` contient une référence arrière **`(.*)`** qui correspond au contenu du titre qui suit &quot;Ma Société-&quot;. N&#39;oubliez pas que le fait d&#39;entourer une partie d&#39;un modèle avec une parenthèse ( ) crée une référence arrière qui peut être référencée par la Substitution. Dans cet exemple, la Substitution (${toupper:**$1**}) réécrit cette référence arrière (**$1**) à l’aide de la fonction toupper.

Ainsi, le titre du formulaire &quot;Ma Société - Bienvenue&quot; est réécrit en &quot;BIENVENUE&quot;.

**Remerciements**

Le logiciel du moteur de réécriture a été développé à l&#39;origine par Apache Group pour être utilisé dans le projet de serveur Apache HTTP (https://www.apache.org/).

## Ajouter les règles de titre de recherche {#task_155CECB74BE3444384EDBBD04F41515E}

Vous pouvez ajouter des règles de titre de recherche pour indiquer comment les titres des résultats de recherche sur votre site Web s’affichent. Vous pouvez manipuler n’importe quelle partie du titre.

<!-- 

t_adding_search_title_rules.xml

 -->

**Pour ajouter des règles de titre de recherche**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Rewrite Rules]** > **[!UICONTROL Search Title Rules]**.
1. Dans le champ [!DNL Search Title Rules], entrez les règles de votre choix.

   Les lignes vierges et les lignes de commentaire commençant par le caractère &quot;#&quot; (hachage) sont autorisées.
1. (Facultatif) Sur la page [!DNL Search Title Rules], dans le champ [!DNL Test Search Title Rules], saisissez un titre de test, puis cliquez sur **Test**.
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Search Title Rules], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

