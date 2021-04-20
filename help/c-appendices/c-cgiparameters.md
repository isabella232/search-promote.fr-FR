---
description: Découvrez comment utiliser divers paramètres CGI.
solution: Target
title: Paramètres CGI
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1943'
ht-degree: 1%

---


# Paramètres CGI{#cgi-parameters}

## Paramètres CGI {#concept_F395999090FE4926B38BC73D5E612800}

## Rechercher les paramètres CGI {#reference_DA27A8B0728246DA94994885E1353890}

Le code du formulaire de recherche est fourni que vous pouvez copier et coller dans le code HTML de votre site ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**).

Voir [Copie du code HTML du formulaire de recherche dans le...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Vous pouvez également définir les paramètres répertoriés dans le formulaire de recherche lui-même ou à partir d’un script. Outre les paramètres répertoriés ci-dessous, vous pouvez également utiliser les paramètres de recherche d’arrière-plan pour contrôler la recherche.

Voir [Paramètres CGI de recherche dorsale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

Les requêtes de recherche se composent d’une URL de base. L’URL de base indique le compte que le client recherche et un ensemble de paramètres CGI (paires clé-valeur) qui indiquent comment renvoyer les résultats de recherche souhaités pour le compte associé.

L’URL de base est associée à un compte spécifique et à un environnement intermédiaire ou actif. Vous pouvez demander plusieurs alias pour l’URL de base à votre gestionnaire de compte. Par exemple, une société appelée Megacorp peut avoir deux URL de base associées à son compte : `https://search.megacorp.com` et `https://stage.megacorp.com`. La première URL recherche leur index actif et la seconde l’index intermédiaire.

Trois formats de paramètres CGI sont pris en charge. Par défaut, votre compte est configuré pour séparer les paramètres CGI par un point-virgule, comme dans l’exemple suivant :

`https://search.megacorp.com?q=shoes;page=2`

Si vous préférez, votre gestionnaire de compte peut configurer votre compte pour qu’il utilise des esperluettes afin de séparer les paramètres CGI, comme dans l’exemple suivant :

`https://search.megacorp.com?q=shoes&page=2`

Un troisième format, appelé format SEO, est également pris en charge lorsqu’une barre oblique (`/`) est utilisée à la place du séparateur et du signe égal, comme dans l’exemple suivant :

`https://search.megacorp.com/q/shoes/page/2`

Chaque fois que le format d’optimisation du référencement est utilisé pour envoyer une requête, tous les liens de sortie sont renvoyés au même format.

| Paramètre de recherche guidée | Exemple | Description |
|--- |--- |--- |
| q | `q=string` | Indique la chaîne de requête pour la recherche. Ce paramètre correspond au paramètre de recherche principal `sp_q`.  Voir [Paramètres CGI de recherche dorsale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| q# | `q#=string` | Le facettage (recherche dans un champ donné) se fait au moyen des paramètres q et x numérotés.  Le paramètre q définit le terme que vous recherchez dans la facette, comme indiqué par le paramètre x numéroté correspondant.<br>Par exemple, si vous avez deux facettes nommées taille et couleur, vous pouvez avoir un élément du type q1=small;x1=size;q2=red;x2=color.  Ce paramètre correspond aux paramètres de recherche du serveur principal `sp_q_exact_#`.  <br>Voir Paramètres [ CGI de recherche ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)dorsale. |
| x# | `q#=string` | Le facettage (recherche dans un champ donné) se fait au moyen des paramètres q et x numérotés.  Le paramètre q définit le terme que vous recherchez dans la facette, comme indiqué par le paramètre x numéroté correspondant. <br>Par exemple, si vous avez deux facettes nommées taille et couleur, vous pouvez avoir un élément du type q1=small;x1=size;q2=red;x2=color.  Ce paramètre correspond aux paramètres de recherche du serveur principal `sp_x_#`.  <br>Voir Paramètres [ CGI de recherche ](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)dorsale. |
| collecte | `collection=string` | Indique la collection à utiliser pour la recherche.  Ce paramètre correspond au paramètre de recherche principal `sp_k`.  Voir [Paramètres CGI de recherche dorsale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| count | `count=number` | Indique le nombre total de résultats affichés.  La valeur par défaut est définie dans [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Ce paramètre correspond au paramètre de recherche principal `sp_c`.  Voir [Paramètres CGI de recherche dorsale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| page | `page=number` | Indique la page des résultats qui sont renvoyés. |
| rang | `rank=field` | Indique le champ de classement à utiliser pour le classement statique.  Le champ doit être un champ de type Classement dont la pertinence est supérieure à 0.  Ce paramètre correspond au paramètre principal `sp_sr`.  Voir [Paramètres CGI de recherche dorsale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |
| sort | `sort=number` | Indique l’ordre de tri.<br>&quot;0&quot; est la valeur par défaut et est triée par score de pertinence ; &quot;1&quot; est classé par date ; &quot;-1&quot; n’est pas trié.  Les utilisateurs peuvent spécifier un nom de champ pour la valeur du paramètre `sp_s`.  Par exemple, `sp_s=title` trie les résultats en fonction des valeurs contenues dans le champ de titre. Lorsqu’un nom de champ est utilisé pour la valeur d’un paramètre ` sp_s `, les résultats sont triés par ce champ, puis subtriés par pertinence.  Pour activer cette fonction, cliquez sur [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. Sur la page Définitions, cliquez sur [!UICONTROL Add New Field ] ou sur [!UICONTROL Edit ] pour un nom de champ particulier. Dans la liste déroulante [!UICONTROL Sorting ], sélectionnez [!UICONTROL Ascending ] ou [!UICONTROL Descending ]. Ce paramètre correspond au paramètre de recherche principal `sp_s`. <br>Voir Paramètres [ CGI de recherche ]dorsale.(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## Paramètres CGI de recherche principale {#reference_582E85C3886740C98FE88CA9DF7918E8}

En règle générale, les clients interagissent avec une couche de présentation appelée Recherche guidée. Cependant, il est théoriquement possible d’ignorer le calque Recherche guidée et d’interagir avec la recherche principale principale en utilisant directement les paramètres CGI décrits sur cette page.

Vous pouvez sélectionner les paramètres CGI de recherche principale dans le tableau suivant :
<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> </th> 
   <th colname="col2" class="entry"> <p>Prise en charge d’une seule requête </p> </th> 
   <th colname="col03" class="entry"> <p>Prise en charge de plusieurs requêtes </p> </th> 
   <th colname="col3" class="entry"> <p>Exemples </p> </th> 
   <th colname="col4" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>sp_a </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_a= string </code> </p> </td> 
   <td colname="col4"> <p>Indique la chaîne du numéro de compte. Ce paramètre est obligatoire et doit être une chaîne de numéro de compte valide. Vous pouvez trouver la chaîne de votre numéro de compte sous <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Options de compte </span> &gt; <span class="uicontrol"> Paramètres du compte </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_advanced= 0 or 1 </code> </p> </td> 
   <td colname="col4"> <p>Si <code>sp_advanced=1 </code> est envoyé avec une requête, tout le code entre la balise <code>&lt;search-if-advanced&gt; </code> et la balise <code>&lt;/search-if-advanced&gt; </code> dans le modèle de recherche est utilisé pour le formulaire de recherche. Tout le code entre la balise <code>&lt;search-if-not-advanced&gt; </code> et la balise <code>&lt;/search-if-not-advanced&gt; </code> est ignoré. Si <code>sp_advanced=0 </code> (ou toute autre valeur) est envoyé, le bloc de modèle &lt;search-if-advanced&gt; est ignoré et le bloc de modèle &lt;search-if-not-advanced&gt; est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_c= number </code> </p> </td> 
   <td colname="col4"> <p>Indique le nombre total de résultats à afficher. La valeur par défaut est de 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Collecte des informations contextuelles pour le champ donné. Les informations collectées sont générées dans les résultats de la recherche par le biais de la balise de modèle <code>&lt;search-context&gt; </code>. La valeur par défaut est <code>body </code>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_d= type </code> </p> </td> 
   <td colname="col4"> <p>Indique le type de plage de dates à effectuer lors de la recherche. Les valeurs possibles pour le type sont toutes, ce qui signifie ne pas effectuer de recherche de plage de dates, personnalisées, ce qui indique que la valeur de <code>sp_date_range </code> doit être utilisée pour déterminer les dates à rechercher, et spécifiques, ce qui indique que les valeurs de <code>sp_start_day </code>, <code>sp_start_month </code>, <code>sp_start_year </code>, <code>sp_end_day </code>, <code>sp_end_month </code> sont utilisées pour déterminer la plage de dates à rechercher. <code>sp_end_year </code> <code>sp_d </code> n’est requise que si votre formulaire de recherche contient l’option de recherche selon une plage personnalisée (par exemple  <code>sp_date_range </code>) ou selon un début et une plage de dates de fin spécifiques. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <code>sp_d_#= type </code> </p> </td> 
   <td colname="col4"> <p>Spécifie le type de plage de dates à effectuer pour la requête <code>sp_q_# </code> correspondante. Le "#" est remplacé par un nombre compris entre 1 et 16 (par exemple, <code>sp_d_8 </code>, s’applique à la requête numérotée <code>sp_q_8 </code>). </p> <p>Vous pouvez définir <code>type </code> sur n'importe quelle valeur, ce qui signifie qu'il ne faut pas effectuer de recherche de plage de dates, personnalisé, ce qui indique que la valeur de <code>sp_date_range_# </code> est utilisée pour déterminer les dates à rechercher et spécifique, ce qui indique que les valeurs de <code>sp_q_min_day_# </code>, <code>sp_q_min_month_# </code>, <code>sp_q_min_year_# </code>, <code>sp_q_max_day_# </code>, <code>sp_q_max_month_# </code> doivent être utilisées pour déterminer la plage de dates. <code>sp_q_max_year_# </code> L'utilisation de <code>sp_d_# </code> n'est requise que si votre formulaire de recherche contient l'option de recherche soit par une plage personnalisée (par <code>sp_date_range_# </code>), soit par un début et une plage de dates de fin spécifiques. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Spécifie une plage de dates prédéfinie à appliquer à la recherche. Les valeurs supérieures ou égales à zéro spécifient le nombre de jours à rechercher avant aujourd’hui. Par exemple, la valeur "0" indique "aujourd’hui", la valeur "1" indique "aujourd’hui et hier", la valeur "30" indique "au cours des 30 derniers jours", etc. </p> <p>Les valeurs inférieures à zéro définissent une plage personnalisée comme suit : </p> <p>-1 = "Aucun", la même chose que de ne spécifier aucune plage de dates. </p> <p>-2 = "Cette semaine", qui effectue une recherche du dimanche au samedi de la semaine en cours. </p> <p>-3 = "Semaine dernière", qui effectue une recherche du dimanche au samedi de la semaine précédant la semaine en cours. </p> <p>-4 = "Ce mois-ci", qui recherche les dates du mois en cours. </p> <p>-5 = "Dernier mois", qui recherche les dates du mois précédant le mois en cours. </p> <p>-6 = "Cette année", qui recherche les dates de l’année en cours. </p> <p>-7 = "L’année dernière", qui recherche les dates de l’année précédant l’année en cours. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Spécifie une plage de dates prédéfinie à appliquer à la requête <code>sp_q_# </code> correspondante. Le "#" est remplacé par un nombre compris entre 1 et 16 (par exemple, <code>sp_date_range_8 </code>, s’applique à la requête numérotée <code>sp_q_8 </code>). </p> <p>Les valeurs supérieures ou égales à zéro spécifient le nombre de jours de recherche avant aujourd’hui. Par exemple, une valeur de 0 indique aujourd’hui ; une valeur de 1 indique aujourd’hui et hier ; une valeur de 30 indique les 30 derniers jours, etc. </p> <p>Les valeurs inférieures à zéro définissent une plage personnalisée comme suit : </p> <p>-1 = "Aucun", la même chose que de ne spécifier aucune plage de dates. </p> <p>-2 = "Cette semaine", qui effectue une recherche du dimanche au samedi de la semaine en cours. </p> <p>-3 = "Semaine dernière", qui effectue une recherche du dimanche au samedi de la semaine précédant la semaine en cours. </p> <p>-4 = "Ce mois-ci", qui recherche les dates du mois en cours. </p> <p>-5 = "Dernier mois", qui recherche les dates du mois précédant le mois en cours. </p> <p>-6 = "Cette année", qui recherche les dates de l’année en cours. </p> <p>-7 = "L’année dernière", qui recherche les dates de l’année précédant l’année en cours. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Indique un champ unique sur lequel dédupliquer les résultats de la recherche. Tous les résultats de duplicata de ce champ sont supprimés des résultats de la recherche. Par exemple, si pour <code>sp_dedupe_field=title </code>, seul le résultat supérieur d’un titre donné s’affiche dans les résultats de la recherche (aucun résultat n’a le même contenu de champ de titre). Pour les champs de type à plusieurs valeurs (liste autorisée), le contenu entier du champ est utilisé pour la comparaison. Un seul champ peut être spécifié. Un "qualificateur de table" n'est pas autorisé dans le nom du champ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_e= number </code> </p> </td> 
   <td colname="col4"> <p>Indique que l’extension automatique des caractères génériques doit avoir lieu pour tout mot de la chaîne de requête contenant plus de plusieurs caractères numériques. En d'autres termes, <code>sp_e=5 </code> spécifie que les mots de 5 caractères ou plus, tels que "requête" ou "nombre", doivent être développés avec le caractère générique "*", ce qui rend la recherche équivalente à une recherche de "requête*" ou "nombre*". Les mots comportant moins de caractères ne sont pas développés, de sorte qu’une recherche de "mot" ne peut pas être automatiquement étendue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <code>sp_e_#= number </code> </p> </td> 
   <td colname="col4"> <p>Indique que l’extension automatique des caractères génériques a lieu pour tout mot de la chaîne de requête <code>sp_q_# </code> correspondante contenant plus de plusieurs caractères. En d'autres termes, <code>sp_e_2=5 </code> spécifie que les mots contenant cinq caractères ou plus dans la chaîne de requête <code>sp_q_2 </code>, tels que "requête" ou "nombre", doivent être développés avec le caractère générique " <code>* </code>", ce qui rend la recherche équivalente à une recherche de "requête*" ou "nombre*". Les mots comportant moins de caractères ne sont pas développés, de sorte qu’une recherche de "mot" dans <code>sp_q_2 </code> ne peut pas être automatiquement étendue. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>12 </p> </td> 
   <td colname="col2"> <p>sp_end_day, sp_end_month, sp_end_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_end_day= <i>number</i>,sp_end_month= <i>number</i>, sp_end_year= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Ce triplet de valeurs spécifie la plage de dates de fin de la recherche et doit être fourni sous forme de jeu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>13 </p> </td> 
   <td colname="col2"> <p>sp_f </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code>sp_f= string </code> </p> </td> 
   <td colname="col4"> <p>Spécifie le jeu de caractères des chaînes de paramètres de requête (par exemple <code>sp_q </code>). Cette chaîne doit toujours correspondre au jeu de caractères de la page qui contient le formulaire de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Définit un tableau de données logique composé des champs donnés. Par exemple, un tableau nommé "articles" composé des champs "couleur", "taille" et "prix" serait défini comme suit : </p> <p> <code>sp_field_table=items:color,size,price </code> </p> <p>Les tableaux logiques sont particulièrement utiles en conjonction avec les champs dont les "Listes autorisées" sont cochées (sous <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>). Tous les paramètres CGI et les balises de modèle qui utilisent un nom de champ comme valeur peuvent éventuellement spécifier un nom de table suivi d’un "". avant le nom du champ (par exemple, <code>sp_x_1=tablename.fieldname </code>). </p> <p>Par exemple, pour rechercher des documents contenant un ou plusieurs éléments "rouges" de taille "large" (où les éléments sont représentés sous forme de lignes parallèles de métadonnées), vous pouvez utiliser les éléments suivants : </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p></td><td colname="col4"><p></p><p></p><p><code>sp_i=1 </code><code>sp_i=2 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_k= string </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_l= string </code></p></td><td colname="col4"><p><code>sp_q </code><code>string </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_literal= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_literal=1 </code></p><p><code>sp_literal=0 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_m= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_n= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_not_found_page= url </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p= any/all/phrase </code></p></td><td colname="col4"><p><code>any </code><code>all </code><code>phrase </code></p><p><code>phrase </code><code>all </code><code>sp_p </code></p><p></p><p></p><p><code>sp_p </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_p_#= any/all/phrase </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>any </code><code>all </code><code>phrase </code></p><p><code>all </code><code>phrase </code><code>sp_p_# </code><code>any </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>exact </code><code>equivalent </code><code>compatible </code><code>sp_p </code><code>exact </code><code>sp_p </code><code>all </code><code>phrase </code><code>equivalent </code><code>sp_pt </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_pt_#= <i>exact/equivalent/compatible</i> </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_p_8 </code><code>sp_q_8 </code><code>exact </code><code>equivalent </code><code>exact </code><code>compatible </code><code>sp_p_# </code><code>exact </code><code>sp_p_# </code><code>equivalent </code><code>sp_pt_# </code><code>compatible </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q= string </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_#= text </code></p></td><td colname="col4"><p><code>sp_q_# </code><code>sp_q_1 </code><code>sp_q_16 </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_day= integer value </code></p><p><code>sp_q_month= integer value </code></p><p><code>sp_q_year= integer value </code></p><p><code>sp_q_day_#= integer value </code></p><p><code>sp_q_month_#= integer value </code></p><p><code>sp_q_year_#= integer value </code></p></td><td colname="col4"><p><code>sp_q_day </code><code>sp_q_month </code><code>sp_q_year </code><code>sp_q </code></p><p><code># </code><code>sp_q_day_6 </code><code>sp_q_6 </code></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p><p><code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code></p></td><td colname="col4"><p><code>sp_q_location </code><code>sp_q_location_# </code><code># </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_q_max_relevant_distance= <i>value</i> </code></p><p><code> sp_q_max_relevant_distance_#= <i>value</i> </code></p></td><td colname="col4"><p><code>sp_q_max_relevant_distance </code><code>sp_q_max_relevant_distance_# </code><code># </code></p><p><code>sp_q_max_relevant_distance </code></p><p><code>sp_q_max_relevant_distance_# </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p><p></p></td><td colname="col03"><p></p><p></p></td><td colname="col3"><p><code> sp_q_min_day=<i>integer value</i> </code></p><p><code> sp_q_min_month=<i>integer value</i> </code></p><p><code> sp_q_min_year=<i>integer value</i> </code></p><p><code> sp_q_max_day=<i>integer value</i> </code></p><p><code> sp_q_max_month=<i>integer value</i> </code></p><p><code> sp_q_max_year=<i>integer value</i> </code></p><p><code> sp_q_min_day_#=<i>integer value</i> </code></p><p><code> sp_q_min_month_#=<i>integer value</i> </code></p><p><code> sp_q_min_year_#=<i>integer value</i> </code></p><p><code> sp_q_max_day_#=<i>integer value</i> </code></p><p><code> sp_q_max_month_#=<i>integer value</i> </code></p><p><code> sp_q_max_year_#=<i>integer value</i> </code></p></td><td colname="col4"><p><code>sp_q_min_day </code><code>sp_q_min_month </code><code>sp_q_min_year </code><code>sp_q_max_day </code><code>sp_q_max_month </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_day_6 </code><code>sp_q_6 </code></p><p></p><p><code>PublishDate </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_min= value </code></p><p><code>sp_q_max= value </code></p><p><code>sp_q_min_#= value </code></p><p><code>sp_q_max_#= value </code></p><p><code>sp_q_exact_#=value </code></p></td><td colname="col4"><p><code>sp_q_min </code><code>sp_q_max </code><code>sp_q_exact </code><code>sp_q </code></p><p><code># </code><code>sp_q_min_8 </code><code>sp_q_8 </code></p><p><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>sp_q_min_# </code><code>sp_q_max_# </code></p><p><code>sp_q_min_# </code><code>sp_q_max_# </code><code>sp_q_exact_# </code><code>...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_nocp= 1 or 0 </code></p><p><code>sp_q_nocp_#= 1 or 0 </code></p></td><td colname="col4"><p><code>0 </code></p><p><code>1 </code></p><p><code>sp_q_nocp </code><code>sp_q </code><code># </code><code>sp_q_nocp_8 </code><code>sp_q_8 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_q_required= 1 or 0 or -1 </code></p><p><code>sp_q_required_#= 1 or 0 or -1 </code></p></td><td colname="col4"><p></p><p><code>sp_q_required </code><code>sp_q </code></p><p><code># </code><code>sp_q_required_8 </code><code>sp_q_8 </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_referrer= url </code></p></td><td colname="col4"><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>ro </code></p><p></p><p><code>sp_ro=body:10 </code></p><p></p><p><code>sp_ro=body:9|title:9 </code></p><p><p><code>sp_ro=title:10 </code><code>title </code><code>sp_ro </code><code>sp_ro </code></p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_s= number </code></p></td><td colname="col4"><p></p><p><code>sp_s </code><code>sp_s=title </code><code>sp_s </code></p><p></p><p><code>sp_s </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code></p><p><code>sp_field_table </code></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sr= field </code></p></td><td colname="col4"><p><code>sp_sr </code></p><p><code>sp_sr </code><code>&lt;input type="hidden" name="sp_sr" value=""&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_sfvl_field= string </code></p></td><td colname="col4"><p><code>search-field-value-list</code></p><p><code>sp_sfvl_field </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p></td><td colname="col4"><p><code>search-field-value-list </code></p><p><code>dynamic-facet-field-count </code><code>dynamic-facet-field-count </code></p><p><code>sp_sfvl_df_count </code><code>dynamic-facet-field-count </code><code>sp_sfvl_df_count </code><code>sp_sfvl_df_count </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p></p><p></p></td><td colname="col4"><p></p><p><p><code>sp_sfvl_df_count </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_include </code><code>sp_sfvl_df_count </code></p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_staged= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_staged=1 </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_start_day= number </code></p><p><code>sp_start_month= number </code></p><p><code>sp_start_year= number </code></p></td><td colname="col4"><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_suggest_q= number </code></p></td><td colname="col4"><p><code>sp_suggest_q </code><code>sp_q[_#] </code></p><p><code>sp_suggest_q </code><code>sp_q </code></p><p><code>sp_suggest_q=1 </code><code>sp_q_1 </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_t= string </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_trace= 0 or 1 </code></p></td><td colname="col4"><p><code>sp_stage=1 </code></p><p></p><p><p></p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code> sp_w= <i>sound-alike-enable</i> </code></p><p><code> sp_w_control=<i>sound-alike-control</i> </code></p></td><td colname="col4"><p></p><p></p><p></p><p></p><p></p><code>sp_w_control </code></p><p><code>sp_w_control=0 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control=1 </code><code>sp_w </code></p><p><code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code></p><p><code>sp_w_control </code><code>sp_w </code></p><p></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x= field </code></p></td><td colname="col4"><p><code>sp_q </code><code>sp_x </code></p><p></p><p><code>sp_x </code></p><p></p><p><code>sp_x=any </code><code>sp_x </code></p><p><code>sp_x </code></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code></p></td></tr><tr><td colname="col1"><p></p></td><td colname="col2"><p></p></td><td colname="col03"><p></p></td><td colname="col3"><p><code>sp_x_#= field-name </code></p></td><td colname="col4"><p><code>sp_q_# </code><code> # </code><code>sp_x_8 </code></p><p><code>sp_x_# </code></p><p></p><p><code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code></p><p><code>sp_x </code><code>sp_x_# </code></p><p></p><p><code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code></p></td></tr></tbody></table>

## Exemple typique d&#39;utilisation des paramètres CGI de recherche principale {#section_260012BBC2514CC9A8E02E53DE8B41EE}

Les requêtes de liens suivantes début une recherche en utilisant &quot;Musique&quot; comme requête de recherche et utilisent tous les paramètres par défaut. Notez que l’URL est fractionnée sur deux lignes pour plus de lisibilité. Dans votre code HTML, ce lien doit tous se trouver sur une seule ligne.

```
<a href="https://search.atomz.com/search/?sp_q=Music&sp_a=sp99999999"> 
Testing...</a>
```

La même fonctionnalité est généralement définie avec un formulaire :

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q" value="Music"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
</form>
```

En règle générale, vous devez utiliser des paramètres par défaut lorsque vous lancez une recherche. Ainsi, la première page est affichée, triée par pertinence, et permet au client de choisir d&#39;autres pages et d&#39;autres options. Si le formulaire de recherche de votre site comporte des options pour les collections, transmettez le nom de la collection en tant que paramètre.

## Exemple détaillé de l&#39;utilisation des paramètres CGI de recherche principale {#section_5FA3C620D5124FB2AB28857F8D8473F6}

Les requêtes de formulaire suivantes affichent les résultats `25` commençant par le résultat `10`. Les résumés ne sont pas affichés, l’ordre de tri est par date et la collection `support` est utilisée. Seuls les documents datés au cours des 30 derniers jours sont renvoyés.

```
<form action="https://search.atomz.com/search/"> 
<input size=12 name="sp_q"><br> 
<input type=hidden name="sp_a" value="sp99999999"> 
<input type=submit value="Search"><br> 
<input type=hidden name=sp_n value=10> 
<input type=hidden name=sp_c value=25> 
<input type=hidden name=sp_m value=0> 
<input type=hidden name=sp_s value=1> 
<input type=hidden name=sp_k value="support"> 
<input type=hidden name=sp_date_range value=30> 
</form>
```

