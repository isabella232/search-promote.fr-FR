---
description: valeur nulle
seo-description: valeur nulle
seo-title: Paramètres CGI
solution: Target
title: Paramètres CGI
topic: Appendices,Site search and merchandising
uuid: a5f43547-bc15-44aa-ba23-6b8b573e09d2
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Paramètres CGI{#cgi-parameters}

## Paramètres CGI {#concept_F395999090FE4926B38BC73D5E612800}

## Rechercher des paramètres CGI {#reference_DA27A8B0728246DA94994885E1353890}

Le code du formulaire de recherche est fourni que vous pouvez copier et coller dans le code HTML de votre site ( **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**).

Voir [Copie du code HTML du formulaire de recherche dans le...](../c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Vous pouvez également définir les paramètres répertoriés dans le formulaire de recherche lui-même ou à partir d’un script. Outre les paramètres répertoriés ci-dessous, vous pouvez également utiliser les paramètres de recherche principale pour contrôler la recherche.

Voir Paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal.

Les requêtes de recherche se composent d’une URL de base. L’URL de base indique le compte que le client recherche et un ensemble de paramètres CGI (paires clé-valeur) qui indiquent comment renvoyer les résultats de recherche souhaités pour le compte associé.

L’URL de base est associée à un compte spécifique et à un environnement intermédiaire ou dynamique. Vous pouvez demander plusieurs alias pour l’URL de base à votre gestionnaire de compte. Par exemple, une société appelée Megacorp peut avoir deux URL de base associées à son compte : `https://search.megacorp.com` et `https://stage.megacorp.com`. La première URL effectue une recherche dans son index dynamique et la seconde dans son index intermédiaire.

Trois formats de paramètres CGI sont pris en charge. Par défaut, votre compte est configuré pour séparer les paramètres CGI par un point-virgule, comme dans l’exemple suivant :

`https://search.megacorp.com?q=shoes;page=2`

Si vous le préférez, votre gestionnaire de compte peut configurer votre compte pour qu’il utilise des esperluettes afin de séparer les paramètres CGI, comme dans l’exemple suivant :

`https://search.megacorp.com?q=shoes&page=2`

Un troisième format, appelé format SEO, est également pris en charge lorsqu’une barre oblique `/` est utilisée à la place du séparateur et du signe égal, comme dans l’exemple suivant :

`https://search.megacorp.com/q/shoes/page/2`

Chaque fois que le format d’optimisation du référencement est utilisé pour envoyer une requête, tous les liens de sortie sont renvoyés au même format.

| Paramètre de recherche guidée | Exemple | Description |
|--- |--- |--- |
| q | `q=string` | Spécifie la chaîne de requête pour la recherche. Ce paramètre correspond au paramètre de recherche principal `sp_q` .  Voir Paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal. |
| q# | `q#=string` | La facette (recherche dans un champ donné) est effectuée au moyen des paramètres q et x numérotés.  Le paramètre q définit le terme que vous recherchez dans la facette, comme indiqué par le paramètre x numéroté correspondant.<br>Si, par exemple, vous disposez de deux facettes nommées taille et couleur, vous pouvez avoir un élément du type q1=petite;x1=taille;q2=rouge;x2=couleur.  Ce paramètre correspond aux paramètres de recherche `sp_q_exact_#` principal.  <br>Voir Paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal. |
| x# | `q#=string` | La facette (recherche dans un champ donné) est effectuée au moyen des paramètres q et x numérotés.  Le paramètre q définit le terme que vous recherchez dans la facette, comme indiqué par le paramètre x numéroté correspondant. <br>Par exemple, si vous avez deux facettes appelées taille et couleur, vous pouvez avoir un élément du type q1=petit;x1=taille;q2=rouge;x2=couleur.  Ce paramètre correspond aux paramètres de recherche `sp_x_#` principal.  <br>Voir Paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal. |
| collecte | `collection=string` | Indique la collection à utiliser pour la recherche.  Ce paramètre correspond au paramètre de recherche principal `sp_k` .  Voir Paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal. |
| count | `count=number` | Indique le nombre total de résultats affichés.  La valeur par défaut est définie dans [!UICONTROL Settings ] > [!UICONTROL Searching ] > [!UICONTROL Searches ]. .  Ce paramètre correspond au paramètre de recherche principal `sp_c` .  Voir Paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal. |
| page | `page=number` | Indique la page des résultats qui sont renvoyés. |
| grade | `rank=field` | Indique le champ de classement à utiliser pour le classement statique.  Le champ doit être un champ de type Classement avec une pertinence supérieure à 0.  Ce paramètre correspond au paramètre `sp_sr` principal.  Voir Paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal. |
| sort | `sort=number` | Indique l’ordre de tri.<br>&quot;0&quot; est la valeur par défaut et trie par score de pertinence ; &quot;1&quot; est classé par date ; &quot;-1&quot; n’est pas trié.  Les utilisateurs peuvent spécifier un nom de champ pour la valeur du `sp_s` paramètre.  Par exemple, `sp_s=title` trie les résultats selon les valeurs contenues dans le champ de titre. Lorsqu’un nom de champ est utilisé pour la valeur d’un ` sp_s ` paramètre, les résultats sont triés par ce champ, puis subtriés par pertinence.  To enable this feature, click [!UICONTROL Settings ] > [!UICONTROL Metadata ] > [!UICONTROL Definitions ]. Dans la page Définitions, cliquez sur [!UICONTROL Add New Field ] ou sur [!UICONTROL Edit ] un nom de champ particulier. Dans la liste [!UICONTROL Sorting ] déroulante, sélectionnez [!UICONTROL Ascending ] ou [!UICONTROL Descending ]. Ce paramètre correspond au paramètre de recherche principal `sp_s` . <br>Voir Paramètres [CGI de recherche]principal.(../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8). |

## Paramètres CGI de recherche principale {#reference_582E85C3886740C98FE88CA9DF7918E8}

En règle générale, les clients interagissent avec une couche de présentation appelée Recherche guidée. Cependant, il est théoriquement possible de sauter le calque de recherche guidée et d’interagir avec la recherche principale principale en utilisant directement les paramètres CGI décrits sur cette page.

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
   <td colname="col3"> <p> <span class="codeph"> sp_a= chaîne </span> </p> </td> 
   <td colname="col4"> <p>Indique la chaîne du numéro de compte. Ce paramètre est obligatoire et doit être une chaîne de numéro de compte valide. Vous pouvez trouver la chaîne de votre numéro de compte sous <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Options de compte </span> &gt; <span class="uicontrol"> Paramètres du compte </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>sp_advanced </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_advanced= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p>Si <span class="codeph"> sp_advanced=1 </span> est envoyé avec une requête, tout le code entre la balise <span class="codeph"> &lt;search-if-advanced&gt; </span> et la balise <span class="codeph"> &lt;/search-if-advanced&gt; </span> dans le modèle de recherche est utilisé pour le formulaire de recherche. Tout le code entre la balise <span class="codeph"> &lt;search-if-not-advanced&gt; </span> et la balise <span class="codeph"> &lt;/search-if-not-advanced&gt; </span> est ignoré. Si <span class="codeph"> sp_advanced=0 </span> (ou toute autre valeur) est envoyé, le bloc de modèle &lt;search-if-advanced&gt; est ignoré et le bloc de modèle &lt;search-if-not-advanced&gt; est utilisé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>sp_c </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_c= nombre </span> </p> </td> 
   <td colname="col4"> <p>Indique le nombre total de résultats à afficher. La valeur par défaut est de 10. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>sp_context_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_context_field= <i>field</i> </code> </p> </td> 
   <td colname="col4"> <p>Collecte des informations contextuelles pour le champ donné. Les informations collectées sont générées dans les résultats de la recherche par le biais de la balise de modèle <span class="codeph"> &lt;search-context&gt; </span> . La valeur par défaut est <span class="codeph">body </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>5 </p> </td> 
   <td colname="col2"> <p>sp_d </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d= type </span> </p> </td> 
   <td colname="col4"> <p>Indique le type de plage de dates à effectuer. Les valeurs possibles pour le type sont toutes les valeurs, ce qui signifie qu’il n’est pas possible d’effectuer une recherche de plage de dates, personnalisées, ce qui indique que la valeur de <span class="codeph"> sp_date_range </span> doit être utilisée pour déterminer les dates à rechercher et spécifique, ce qui indique que les valeurs dans <span class="codeph"> sp_start_day </span>, <span class="codeph"> sp_start_month </span>, <span class="codeph"> sp_start_year ,  sp_end_day_month, et sp_end_month_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_year_est utilisé. pour déterminer la plage de dates à rechercher. </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> <span class="codeph"> sp_d </span> n'est requis que si votre formulaire de recherche contient l'option de recherche soit par une plage personnalisée (par <span class="codeph"> sp_date_range </span>), soit par une plage de dates de début et de fin spécifique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>6 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_d_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_d_#= type </span> </p> </td> 
   <td colname="col4"> <p>Indique le type de plage de dates à effectuer pour la requête <span class="codeph"> sp_q_# </span> correspondante. Le "#" est remplacé par un nombre compris entre 1 et 16 (par exemple, <span class="codeph"> sp_d_8 </span>, s’applique à la requête numérotée <span class="codeph"> sp_q_8 </span>). </p> <p>Vous pouvez définir le <span class="codeph"> type </span> sur n’importe quelle valeur, ce qui signifie qu’il ne faut pas effectuer de recherche de plage de dates, personnalisé, ce qui indique que la valeur de <span class="codeph"> sp_date_range_# </span> est utilisée pour déterminer les dates à rechercher et spécifique, ce qui indique que les valeurs dans <span class="codeph"> sp_q_min_day_# </span>, <span class="codeph"> sp_q_min_month_# ,  sp_q_min_year_#_# les sp_q_max_month_# et sp_q_max_year_# doivent être utilisés pour déterminer la plage de dates. </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> L'utilisation de <span class="codeph"> sp_d_# </span> n'est requise que si votre formulaire de recherche contient l'option de recherche soit par une plage personnalisée (au moyen de <span class="codeph"> sp_date_range_# </span>), soit par une plage de dates de début et de fin spécifique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>7 </p> </td> 
   <td colname="col2"> <p>sp_date_range </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Spécifie une plage de dates prédéfinie à appliquer à la recherche. Les valeurs supérieures ou égales à zéro indiquent le nombre de jours avant la date d'aujourd'hui — par exemple, la valeur "0" indique "aujourd’hui", la valeur "1" indique "aujourd’hui et hier", la valeur "30" indique "au cours des 30 derniers jours", etc. </p> <p>Les valeurs inférieures à zéro définissent une plage personnalisée comme suit : </p> <p>-1 = "Aucun", la même chose que de ne spécifier aucune plage de dates. </p> <p>-2 = "Cette semaine", qui effectue une recherche du dimanche au samedi de la semaine en cours. </p> <p>-3 = "Semaine dernière", qui effectue une recherche du dimanche au samedi de la semaine précédant la semaine en cours. </p> <p>-4 = "Ce mois-ci", qui recherche les dates du mois en cours. </p> <p>-5 = "Mois dernier", qui recherche les dates du mois précédant le mois en cours. </p> <p>-6 = "Cette année", qui recherche les dates de l’année en cours. </p> <p>-7 = "L’année dernière", qui recherche les dates dans l’année précédant l’année en cours. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>8 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_date_range_# </p> </td> 
   <td colname="col3"> <p> <code> sp_date_range_#= <i>number</i> </code> </p> </td> 
   <td colname="col4"> <p>Spécifie une plage de dates prédéfinie à appliquer à la requête <span class="codeph"> sp_q_# </span> correspondante. Le "#" est remplacé par un nombre compris entre 1 et 16 (par exemple, <span class="codeph"> sp_date_range_8 </span>, s’applique à la requête numérotée <span class="codeph"> sp_q_8 </span>). </p> <p>Les valeurs supérieures ou égales à zéro indiquent le nombre de jours avant la date d’aujourd’hui. Par exemple, une valeur de 0 indique aujourd’hui ; une valeur de 1 indique aujourd’hui et hier; une valeur de 30 est définie dans les 30 derniers jours, etc. </p> <p>Les valeurs inférieures à zéro définissent une plage personnalisée comme suit : </p> <p>-1 = "Aucun", la même chose que de ne spécifier aucune plage de dates. </p> <p>-2 = "Cette semaine", qui effectue une recherche du dimanche au samedi de la semaine en cours. </p> <p>-3 = "Semaine dernière", qui effectue une recherche du dimanche au samedi de la semaine précédant la semaine en cours. </p> <p>-4 = "Ce mois-ci", qui recherche les dates du mois en cours. </p> <p>-5 = "Mois dernier", qui recherche les dates du mois précédant le mois en cours. </p> <p>-6 = "Cette année", qui recherche les dates de l’année en cours. </p> <p>-7 = "L’année dernière", qui recherche les dates dans l’année précédant l’année en cours. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>9 </p> </td> 
   <td colname="col2"> <p>sp_dedupe_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_dedupe_field= <i>fieldname</i> </code> </p> </td> 
   <td colname="col4"> <p>Spécifie un champ unique sur lequel dédupliquer les résultats de la recherche. Tous les résultats en double de ce champ sont supprimés des résultats de la recherche. Si, par exemple, pour <span class="codeph"> sp_dedupe_field=title </span>, seul le résultat supérieur d’un titre donné s’affiche dans les résultats de la recherche (aucun des deux résultats n’a le même contenu de champ de titre). Pour les champs de type à plusieurs valeurs (liste autorisée), le contenu entier du champ est utilisé pour la comparaison. Un seul champ peut être spécifié. Un "qualificateur de table" n’est pas autorisé dans le nom du champ. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>10 </p> </td> 
   <td colname="col2"> <p>sp_e </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e= nombre </span> </p> </td> 
   <td colname="col4"> <p>Indique que l’extension automatique du caractère générique doit avoir lieu pour tout mot de la chaîne de requête contenant plus de caractères numériques. En d’autres termes, <span class="codeph"> sp_e=5 </span> spécifie que les mots comportant 5 caractères ou plus, tels que "query" ou "number", doivent être développés avec le caractère générique "*", ce qui rend la recherche équivalente à une recherche de "query*" ou "number*". Les mots comportant moins de caractères ne sont pas développés, de sorte qu’une recherche de "mot" n’aurait pas d’extension automatique des caractères génériques. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>11 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_e_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_e_#= nombre </span> </p> </td> 
   <td colname="col4"> <p>Indique que l’extension automatique du caractère générique a lieu pour n’importe quel mot de la chaîne de requête <span class="codeph"> </span> sp_q_# correspondante avec plus de caractères numériques. En d'autres termes, <span class="codeph"> sp_e_2=5 </span> spécifie que les mots comportant cinq caractères ou plus dans la chaîne de requête <span class="codeph"> sp_q_2 </span> , tels que "query" ou "number", doivent être développés avec le caractère générique " <span class="codeph"> * </span>", ce qui rend la recherche équivalente à une recherche de "query*" ou "number*". Les mots comportant moins de caractères ne sont pas développés, de sorte qu’une recherche de "mot" dans <span class="codeph"> sp_q_2 </span> n’aurait pas d’extension automatique de caractères génériques. </p> </td> 
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
   <td colname="col3"> <p> <span class="codeph"> sp_f= chaîne </span> </p> </td> 
   <td colname="col4"> <p>Spécifie le jeu de caractères des chaînes de paramètres de requête (par exemple <span class="codeph"> sp_q </span>). Cette chaîne doit toujours correspondre au jeu de caractères de la page qui contient le formulaire de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>14 </p> </td> 
   <td colname="col2"> <p>sp_field_table </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_field_ table=table: field,field... </code> </p> </td> 
   <td colname="col4"> <p>Définit un tableau de données logique composé des champs donnés. Par exemple, un tableau nommé "articles" composé des champs "couleur", "taille" et "prix" serait défini comme suit : </p> <p> <span class="codeph"> sp_field_table=éléments:couleur,taille,prix </span> </p> <p>Les tableaux logiques sont particulièrement utiles en conjonction avec les champs pour lesquels l’option "Autoriser les listes" est cochée (sous <span class="uicontrol"> Paramètres </span> &gt; <span class="uicontrol"> Métadonnées </span> &gt; <span class="uicontrol"> Définitions </span>). Tous les paramètres CGI et balises de modèle prenant un nom de champ comme valeur peuvent éventuellement spécifier un nom de table suivi d’un "". avant le nom du champ (par exemple, <span class="codeph"> sp_x_1=tablename.fieldname </span>). </p> <p>Par exemple, pour rechercher des documents contenant un ou plusieurs éléments "rouges" de taille "grande" (où les éléments sont représentés sous forme de lignes parallèles de métadonnées), vous pouvez utiliser les éléments suivants : </p> <p> <code> sp_q_exact_1=red&amp;sp_x_1=items.color&amp; sp_q_exact_2=large&amp;sp_x_2=items.size&amp;sp_field_table=items:color,size,price </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>15 </p> </td> 
   <td colname="col2"> sp_i </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_i= <span class="varname"> valeur </span></span> </p> </td> 
   <td colname="col4"> <p>Ignore la recherche lorsque vous générez des rapports. </p> <p>Utilisez cette requête pour masquer certaines recherches en arrière-plan, telles que les recherches générées par le service Voulez-vous dire ou les recherches générées par un administrateur dans le centre des membres. Un utilisateur final ne générant pas ces types de recherches, il n’apparaît pas dans divers rapports Adobe Search&amp;Promote. </p> <p>Les valeurs valides sont <span class="codeph"> sp_i=1 </span> et <span class="codeph"> sp_i=2 </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>16 </p> </td> 
   <td colname="col2"> <p>sp_k </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_k= chaîne </span> </p> </td> 
   <td colname="col4"> <p> Indique la collection à utiliser pour la recherche. La valeur par défaut n’est pas une collection, ce qui signifie que la recherche doit inclure l’ensemble du site. </p> <p>Voir <a href="../c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3" type="reference" format="dita" scope="local"> Utilisation des collections dans les formulaires de recherche </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>17 </p> </td> 
   <td colname="col2"> <p>sp_l </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_l= chaîne </span> </p> </td> 
   <td colname="col4"> <p>Indique la langue des chaînes de paramètres de requête (par exemple <span class="codeph"> sp_q </span>). La <i> chaîne <span class="codeph"> </span></i> doit être un ID de paramètre régional standard contenant un code de langue ISO-639 suivi éventuellement d’un code de pays ISO-3166. Par exemple, "en" ou "en_US" pour l’anglais ou "ja" ou "ja_JP" pour le japonais. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>18 </p> </td> 
   <td colname="col2"> <p>sp_literal </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_literal= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p> La définition de <span class="codeph"> sp_literal=1 </span> désactive temporairement toutes les fonctionnalités susceptibles d’interpréter les mots de la requête. Avec ce paramètre, seuls les mots littéraux de la requête correspondent aux documents, quels que soient les synonymes, les formulaires de remplacement de mots et les correspondances sonores. </p> <p>Notez que <span class="codeph"> sp_literal=0 </span> n’a aucune signification et est ignoré s’il est utilisé. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" type="concept" format="dita" scope="local"> A propos des dictionnaires </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>19 </p> </td> 
   <td colname="col2"> <p>sp_m </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_m= nombre </span> </p> </td> 
   <td colname="col4"> <p> Indique si les résumés sont affichés. 1 est oui, 0 est non. La valeur par défaut est de 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>20 </p> </td> 
   <td colname="col2"> <p>sp_n </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_n= nombre </span> </p> </td> 
   <td colname="col4"> <p> Indique le nombre de résultats qui commencent les résultats de la recherche. La valeur par défaut est de 1. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>21 </p> </td> 
   <td colname="col2"> <p>sp_not_found_page </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_not_found_page= url </span> </p> </td> 
   <td colname="col4"> <p> Indique s’il convient de rediriger vers l’URL spécifiée en l’absence de résultats de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>22 </p> </td> 
   <td colname="col2"> <p>sp_p </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p= any/all/phrase </span> </p> </td> 
   <td colname="col4"> <p> Indique le type de recherche par défaut à effectuer. L’utilisation de <span class="codeph"> n’importe quel </span> signifie rechercher des documents qui contiennent n’importe quel mot de la chaîne de requête. L’utilisation de <span class="codeph"> tous </span> signifie rechercher des documents qui contiennent tous les mots de la chaîne de requête. L’utilisation de <span class="codeph"> phrase </span> signifie que la chaîne de requête est traitée comme s’il s’agissait d’une phrase entre guillemets et que tous les guillemets tapés par l’utilisateur sont ignorés. </p> <p>Pour l’ <span class="codeph"> expression </span> et <span class="codeph"> tous </span>, la spécification de "+" et "-" avant les mots de recherche est désactivée et ces caractères sont ignorés. Si <span class="codeph"> sp_p </span> n'est pas présent, ou s'il est défini sur une chaîne vide ou une autre, les préfixes de mots "+" et "-" standard sont autorisés. </p> <p>Voir la description des conseils de recherche pour plus d’informations sur l’utilisation de plus ("+") et moins ("-") dans les recherches. </p> <p>Voir <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">A propos des recherches </a>. </p> <p>Consultez l’exemple de formulaire de recherche avancée pour obtenir des exemples d’utilisation du paramètre <span class="codeph"> sp_p </span> . </p> <p>Voir <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Exemple de formulaire de recherche avancée </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>23 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p> sp_p_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_p_#= tout/phrase </span> </p> </td> 
   <td colname="col4"> <p>Spécifie le type de recherche par défaut à effectuer avec la requête <span class="codeph"> sp_q_# </span> correspondante. Le "#" est remplacé par un nombre compris entre 1 et 16 (par exemple, <span class="codeph"> sp_p_8 </span> s’applique à la requête numérotée <span class="codeph"> sp_q_8 </span>). L’utilisation de <span class="codeph"> n’importe quel </span> signifie renvoyer des documents qui contiennent n’importe quel mot de la chaîne de requête. L’utilisation de <span class="codeph"> tous </span> signifie renvoyer des documents qui contiennent tous les mots de la chaîne de requête. L’utilisation d’une <span class="codeph"> expression </span> signifie que la chaîne de requête est traitée comme une expression complète (et tous les guillemets tapés par l’utilisateur sont ignorés). </p> <p>Si vous spécifiez <span class="codeph"> tout </span> ou <span class="codeph"> phrase </span>, tous les signes plus et moins avant les mots de recherche sont ignorés. Si <span class="codeph"> sp_p_# </span> est omis, ou s'il est défini sur une chaîne vide ou <span class="codeph"> une autre </span>, les préfixes "+" et "-" standard sont autorisés. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>24 </p> </td> 
   <td colname="col2"> <p>sp_pt </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_pt= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p> Indique le type de correspondance cible à appliquer. L’utilisation de <span class="codeph"> signifie </span> que la cible ne renvoie des correspondances cibles que dans les documents qui correspondent exactement à la chaîne de requête dans le contenu cible. L'utilisation de l' <span class="codeph"> équivalent </span> est exacte, sauf que l'ordre des mots n'est pas important. L’utilisation de <span class="codeph"> compatible </span> définit automatiquement le type de correspondance cible en fonction de la valeur du paramètre <span class="codeph"> sp_p </span> . L'utilisation d' <span class="codeph"> exacte </span> est utilisée si <span class="codeph"> sp_p </span> est <span class="codeph"> tout </span> <span class="codeph"> ou phrase , sinon   équivalent est utilisé. </span><span class="codeph"></span> La valeur par défaut de <span class="codeph"> sp_pt </span> est <span class="codeph"> compatible </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>25 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_pt_# </p> </td> 
   <td colname="col3"> <p> <code> sp_pt_#= <i>exact/equivalent/compatible</i> </code> </p> </td> 
   <td colname="col4"> <p>Spécifie le type de correspondance cible à appliquer avec la requête <span class="codeph"> sp_q_# </span> correspondante. Le "#" est remplacé par un nombre compris entre 1 et 16 (par exemple, <span class="codeph"> sp_p_8 </span> s’applique à la requête numérotée <span class="codeph"> sp_q_8 </span>). L’utilisation de <span class="codeph"> signifie </span> que la cible ne renvoie des correspondances cibles que dans les documents qui correspondent exactement à la chaîne de requête dans le contenu cible. L'utilisation de l' <span class="codeph"> équivalent </span> est comme <span class="codeph"> exact </span>, sauf que l'ordre des mots n'est pas important. L’utilisation de <span class="codeph"> compatible </span> définit automatiquement le type de correspondance cible en fonction de la valeur du paramètre <span class="codeph"> sp_p_# </span> correspondant : <span class="codeph"> exact </span> est utilisé si <span class="codeph"> sp_p_# </span> est tout ou phrase, sinon <span class="codeph"> </span> l'équivalent est utilisé. La valeur par défaut de <span class="codeph"> sp_pt_# </span> est <span class="codeph"> compatible </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>26 </p> </td> 
   <td colname="col2"> <p>sp_q </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q= chaîne </span> </p> </td> 
   <td colname="col4"> <p> Spécifie la chaîne de requête pour la recherche. Une chaîne vide ne donne aucun résultat. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>27 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_q_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_#= texte </span> </p> </td> 
   <td colname="col4"> <p>Ce paramètre permet de créer plusieurs requêtes sur des formulaires de recherche. Le paramètre <span class="codeph"> sp_q_# </span> contient la chaîne de requête à utiliser dans la requête numérotée donnée. Une requête de recherche peut faire référence à 16 requêtes numérotées différentes ( <span class="codeph"> sp_q_1 </span> à <span class="codeph"> sp_q_16 </span>). </p> <p>Par exemple, l’envoi du formulaire suivant renvoie tous les documents qui contiennent les mots "super" et "livres". </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>28 </p> </td> 
   <td colname="col2"> <p>sp_q_day, sp_q_month, sp_q_year </p> </td> 
   <td colname="col03"> <p> sp_q_day_#, sp_q_month_#, sp_q_year_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_day= valeur entière </span> </p> <p> <span class="codeph"> sp_q_month= valeur entière </span> </p> <p> <span class="codeph"> sp_q_year= valeur entière </span> </p> <p> <span class="codeph"> sp_q_day_#= valeur entière </span> </p> <p> <span class="codeph"> sp_q_month_#= valeur entière </span> </p> <p> <span class="codeph"> sp_q_year_#= valeur entière </span> </p> </td> 
   <td colname="col4"> <p>Ces paramètres permettent de spécifier la date exacte d’une requête particulière. Les paramètres <span class="codeph"> sp_q_day </span>, <span class="codeph"> sp_q_month </span>et <span class="codeph"> sp_q_year </span> s'appliquent à la requête principale ( <span class="codeph"> sp_q ).</span> </p> <p>Le <span class="codeph"> # </span>paramètre est remplacé par un nombre compris entre 1 et 16 (par exemple, <span class="codeph"> sp_q_day_6 </span>, qui s’applique à la requête numérotée <span class="codeph"> sp_q_6 </span>). Par défaut, toutes les dates sont recherchées par rapport à l’heure Greenwich. </p> <p>La section suivante du code permet à l’utilisateur de rechercher le mot "orange" dans les documents datés du "janvier". 1st, 2000" dans un champ défini par l’utilisateur et nommé <span class="codeph"> Date de publication </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt; Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;On&nbsp;:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Month &lt;input&nbsp;type="text"&nbsp;name="sp_q_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Year&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>29 </p> </td> 
   <td colname="col2"> <p>sp_q_location </p> </td> 
   <td colname="col03"> <p>sp_q_location_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_location=<i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> <p> <code> sp_q_location_#= <i>latitude/longitude</i> OR <i>areacode</i> OR <i>zipcode</i> </code> </p> </td> 
   <td colname="col4"> <p>Ces paramètres associent un emplacement à la requête principale ou numérotée. L'utilisation de <span class="codeph"> sp_q_location </span> affecte la requête principale, <span class="codeph"> sp_q_location_# </span> (où le <span class="codeph"> # </span> est remplacé par un nombre compris entre 1 et 16), affecte la requête numérotée donnée. Ces paramètres sont utilisés pour effectuer des recherches de proximité à distance minimale et/ou maximale par rapport aux données d’emplacement indexées pour chaque page du site. Le format de la valeur détermine son interprétation. </p> <p>Une valeur sous la forme DDD (trois chiffres) est interprétée comme un code d’aracode téléphonique américain ; une valeur sous la forme DDJJ ou DJJJJ-DJJ est interprétée comme un code postal américain; et une valeur sous la forme ±DD.DDDD±DDD.DDD est interprétée comme une paire latitude/longitude. Les signes sont obligatoires pour chaque valeur. Par exemple, +38.6317+120.5509 indique la latitude 38.6317, la longitude 120.5509. </p> <p>Voir <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> A propos de la recherche de proximité </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>30 </p> </td> 
   <td colname="col2"> <p>sp_q_max_relevant_distance </p> </td> 
   <td colname="col03"> <p>sp_q_max_relevant_distance _# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_max_relevant_distance= <i>value</i> </code> </p> <p> <code> sp_q_max_relevant_distance_#= <i>value</i> </code> </p> </td> 
   <td colname="col4"> <p>Ces paramètres contrôlent le calcul de la pertinence appliqué aux recherches de proximité. L'utilisation de <span class="codeph"> sp_q_max_relevant_distance </span> affecte la requête principale, <span class="codeph"> sp_q_max_relevant_distance_# </span> (où le <span class="codeph"> # </span> est remplacé par un nombre compris entre 1 et 16), affecte la requête numérotée donnée. </p> <p>La valeur par défaut de <span class="codeph"> sp_q_max_relevant_distance </span> est 100. </p> <p>Un score de pertinence parfait pour la composante de proximité représenterait une distance de 0. Un score de pertinence minimum pour le composant de proximité représenterait une distance juste au-dessus de la valeur <span class="codeph"> sp_q_max_relevant_distance_# </span> spécifiée. </p> <p>Voir <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> A propos de la recherche de proximité </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>31 </p> </td> 
   <td colname="col2"> <p>sp_q_min_day, sp_q_min_month, sp_q_min_year </p> <p>sp_q_max_day, sp_q_max_month, sp_q_max_year </p> </td> 
   <td colname="col03"> <p>sp_q_min_day_#, sp_q_min_month_#, sp_q_min_year_# </p> <p> sp_q_max_day_#, sp_q_max_month_#, sp_q_max_year_# </p> </td> 
   <td colname="col3"> <p> <code> sp_q_min_day=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year=<i>integer value</i> </code> </p> <p> <code> sp_q_min_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_min_year_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_day_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_month_#=<i>integer value</i> </code> </p> <p> <code> sp_q_max_year_#=<i>integer value</i> </code> </p> </td> 
   <td colname="col4"> <p>Ces paramètres permettent de définir des plages de dates minimales et maximales pour une requête particulière. Les paramètres <span class="codeph"> sp_q_min_day </span>, <span class="codeph"> sp_q_min_month </span>, <span class="codeph"> sp_q_min_year </span>, <span class="codeph"> sp_q_max_day ,  sp_q_max_month  etsp_q_max_years’appliquent à la requête principale ( sp_q_max).</span><span class="codeph"></span><i></i><span class="codeph"></span> </p> <p>Le <span class="codeph"> # </span>dans le nom du paramètre est remplacé par un nombre compris entre 1 et 16 (par exemple, <span class="codeph"> sp_q_min_day_6 </span> s’applique à la requête numérotée <span class="codeph"> sp_q_6 </span>). </p> <p>Il est légal de spécifier uniquement une date minimale, une date maximale ou à la fois une date minimale et une date maximale. Toutefois, pour un ensemble minimal ou maximal donné, les trois paramètres de date doivent être spécifiés (jour, mois et année). Par défaut, toutes les dates sont recherchées par rapport à l’heure Greenwich. </p> <p>La section de code suivante permet à l’utilisateur de rechercher le mot "orange" dans les documents dont la date est comprise entre le 1er janvier 2000 et le 31 décembre 2000 dans un champ défini par l’utilisateur et appelé <span class="codeph"> Date de publication </span>: </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="PublishDate"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="orange"&gt;Between:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_day_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Day&lt;input&nbsp;type="text"&nbsp;name="sp_q_min_month_1"&nbsp;size="2"&nbsp;value="1"&gt;&nbsp;Start&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_min_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;Start&nbsp;Year 
      And:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_max_day_1"&nbsp;size="2"&nbsp;value="31"&gt;&nbsp;End&nbsp;Day 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_month_1"&nbsp;size="2"&nbsp;value="12"&gt;&nbsp;End&nbsp;Month 
      &lt;input&nbsp;type="text"&nbsp;name="sp_q_max_year_1"&nbsp;size="4"&nbsp;value="2000"&gt;&nbsp;End&nbsp;Year </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>32 </p> </td> 
   <td colname="col2"> <p>sp_q_min, sp_q_max </p> </td> 
   <td colname="col03"> <p>sp_q _min_#, sp_q _max_#, sp_q _exact_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_min= valeur </span> </p> <p> <span class="codeph"> sp_q_max= valeur </span> </p> <p> <span class="codeph"> sp_q_min_#= valeur </span> </p> <p> <span class="codeph"> sp_q_max_#= valeur </span> </p> <p> <span class="codeph"> sp_q_exact_#=value </span> </p> </td> 
   <td colname="col4"> <p>Ces paramètres spécifient une valeur minimale (et/ou maximale) à appliquer à la requête principale ou numérotée. L'utilisation de <span class="codeph"> sp_q_min </span>, <span class="codeph"> sp_q_max </span>et <span class="codeph"> sp_q_exact </span> affecte la requête principale ( <span class="codeph"> sp_q ).</span> </p> <p>Remplacez <span class="codeph"> # </span>dans le nom du paramètre par un nombre compris entre 1 et 16 (par exemple, <span class="codeph"> sp_q_min_8 </span> s'applique à la requête numérotée <span class="codeph"> sp_q_8 </span>). </p> <p>L’utilisation de <span class="codeph"> sp_q_exact_# </span> est abrégée pour spécifier à la fois <span class="codeph"> sp_q_min_# </span> et <span class="codeph"> sp_q_max_# </span> avec la même valeur. Si <span class="codeph"> sp_q_exact_# </span> est spécifié, les paramètres <span class="codeph"> sp_q_min_# </span> ou <span class="codeph"> </span> sp_q_max_# correspondants sont ignorés. </p> <p>Les paramètres <span class="codeph"> sp_q_min_# </span>, <span class="codeph"> sp_q_max_# </span> et <span class="codeph"> </span> sp_q_exact_# peuvent éventuellement spécifier plusieurs valeurs séparées par "|". Par exemple, pour rechercher des documents contenant la valeur vert ou rouge dans le champ "color" : <span class="codeph"> ...&amp;sp_q_exact_1=green|red&amp;sp_x_1=color </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>33 </p> </td> 
   <td colname="col2"> <p>sp_q_nocp </p> </td> 
   <td colname="col03"> <p>sp_q _nocp _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_nocp= 1 ou 0 </span> </p> <p> <span class="codeph"> sp_q_nocp_#= 1 ou 0 </span> </p> </td> 
   <td colname="col4"> <p>La valeur par défaut du paramètre est <span class="codeph"> 0 </span> , ce qui signifie que les extensions Expression commune sont exécutées. </p> <p>Lorsqu'il est défini sur <span class="codeph"> 1 </span> pour la requête de recherche correspondante, les extensions des expressions courantes ne sont pas exécutées. </p> <p>L'utilisation de <span class="codeph"> sp_q_nocp </span> affecte le paramètre de requête de recherche principal <span class="codeph"> sp_q </span>. Pour appliquer ce paramètre à une requête de recherche numérotée, remplacez <span class="codeph"> # </span> dans le nom du paramètre par le numéro correspondant. Par exemple, <span class="codeph"> sp_q_nocp_8 </span> s'applique à la requête de recherche numérotée <span class="codeph"> sp_q_8 </span>. </p> <p> 
     <!--See also <xref href="c_about_common_phrases.xml#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local">About Common Phrases</xref>--> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>34 </p> </td> 
   <td colname="col2"> <p>sp_q_required </p> </td> 
   <td colname="col03"> <p>sp_q _required _# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_q_required= 1 ou 0 ou -1 </span> </p> <p> <span class="codeph"> sp_q_required_#= 1 ou 0 ou -1 </span> </p> </td> 
   <td colname="col4"> <p>Ce paramètre détermine si une correspondance doit (1), (0) ou non (-1) se produire dans la requête correspondante afin qu’un document soit renvoyé sur la page de résultats. </p> <p>L'utilisation de <span class="codeph"> sp_q_required </span> affecte la requête principale ( <span class="codeph"> sp_q </span>). </p> <p>Pour appliquer à une requête numérotée, remplacez le <span class="codeph"> # </span> dans le nom du paramètre par le numéro correspondant (par exemple, <span class="codeph"> sp_q_required_8 </span> s’applique à la requête numérotée <span class="codeph"> sp_q_8 </span>). La valeur par défaut du paramètre est 1 (doit correspondre). </p> <p>Pour rechercher des documents qui contiennent le mot "calc" mais NE contiennent PAS "mac", "win" ou "all" dans le champ "plateforme" défini par l’utilisateur, votre formulaire de recherche HTML peut contenir les lignes suivantes : </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="platform"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="calc"&gt; 
      Exclude:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="mac&nbsp;win&nbsp;all"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_q_required_1"&nbsp;value="-1"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>35 </p> </td> 
   <td colname="col2"> <p>sp_redirect_if_one_result </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_redirect_ 
      if_one_result= <i>0 or 1</i> </code> </p> </td> 
   <td colname="col4"> <p>Indique s’il faut rediriger vers l’URL du résultat de la recherche s’il n’y a qu’un seul résultat de recherche. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>36 </p> </td> 
   <td colname="col2"> <p>sp_referrer </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_referrer= url </span> </p> </td> 
   <td colname="col4"> <p>Indique l’URL du référent pour la recherche. Utile pour les règles de réécriture de recherche dans lesquelles les résultats de la recherche sont liés au même site que le formulaire de recherche. </p> <p>La valeur par défaut est la valeur standard CGI HTTP_REFERRER fournie par le navigateur. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>37 </p> </td> 
   <td colname="col2"> <p>sp_ro </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_ro= <span class="varname"> champ </span>: <span class="varname"> pertinence </span></span> </p> </td> 
   <td colname="col4"> <p>Permet le temps de recherche facultatif, par nom de champ, le contrôle de pertinence. Le <span class="codeph"> ou </span> dans le nom du paramètre signifie "remplacement de la pertinence". Le paramètre accepte un ou plusieurs noms de champ, suivis d’un caractère deux-points, suivis d’une valeur de pertinence comprise entre 0 et 10. </p> <p>Par exemple, pour définir la valeur de pertinence du nom de champ "body" sur 10, au moment où un client effectue une recherche, le paramètre s’affiche comme suit : </p> <p> <span class="codeph"> sp_ro=body:10 </span> </p> <p>Ou, pour spécifier plusieurs valeurs de remplacement de pertinence de champ dans la chaîne de paramètre, vous pouvez utiliser un délimiteur de barre verticale. Par exemple, pour définir la valeur de pertinence des noms de champ "body" et "title" sur 9, le paramètre s’affiche comme suit au moment où un client effectue une recherche : </p> <p> <span class="codeph"> sp_ro=body:9|title:9 </span> </p> <p> <p>Remarque :  La spécification d’un champ qui n’est pas impliqué dans la recherche associée n’a aucun effet. Par exemple, si vous définissez <span class="codeph"> sp_ro=title:10 </span>, mais que le nom du <span class="codeph"> champ de titre </span> n’est pas recherché, le <span class="codeph"> </span> paramètre sp_ro n’a aucun effet. En d'autres termes, la spécification d'un nom de champ à l'aide du paramètre <span class="codeph"> _ro </span> ne recherche pas automatiquement ce champ ; au lieu de cela, il remplace uniquement le paramètre de pertinence associé à ce champ. </p> </p> <p>Voir <a href="../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3" type="task" format="dita" scope="local"> Modification de champs de métadonnées prédéfinis ou définis par l’utilisateur </a>. </p> <p>Voir <a href="../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C" type="concept" format="dita" scope="local"> A propos des règles de nettoyage de requête </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>38 </p> </td> 
   <td colname="col2"> <p>sp_s </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_s= nombre </span> </p> </td> 
   <td colname="col4"> <p>Indique l’ordre de tri. La valeur zéro (0) est la valeur par défaut et permet de trier par score de pertinence. Un (1) signifie trier par date et -1 signifie ne pas trier. </p> <p>Vous pouvez spécifier un nom de champ pour la valeur du paramètre <span class="codeph"> _s </span> . Par exemple, <span class="codeph"> sp_s=title </span> trie les résultats en fonction des valeurs contenues dans le champ de titre. Lorsqu’un nom de champ est utilisé pour la valeur d’un paramètre <span class="codeph"> _s </span> , les résultats sont triés par ce champ, puis subtriés par pertinence. </p> <p>Définissez le tri du champ référencé sur <span class="uicontrol"> Croissant </span> ou <span class="uicontrol"> Décroissant </span> dans <span class="uicontrol"> Paramètres </span> <span class="uicontrol"> &gt;  de métadonnées &gt;  Définitions  pour activer cette fonction.</span><span class="uicontrol"></span> </p> <p>Vous pouvez également affecter plusieurs champs de tri à une seule requête en définissant le paramètre <span class="codeph"> _s </span> plusieurs fois dans le formulaire de recherche. Les lignes de modèle suivantes définissent les résultats de la recherche à trier d’abord par nom d’artiste, puis par nom d’album, puis par nom de piste. </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="artist"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="album"&gt; 
      &lt;input&nbsp;type="hidden"&nbsp;name="sp_s"&nbsp;value="track"&gt; 
      Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Music&nbsp;Search"&gt; </code> </p> <p>Il est également possible de trier sur les données de champ de correspondance de table en spécifiant un qualificateur de nom de table avant le nom du champ, par exemple, items.price. Voir le paramètre <span class="codeph"> sp_field_table </span> pour plus d'informations sur la correspondance des tables. </p> <p>Si vous effectuez une recherche par proximité, vous pouvez trier les résultats en fonction de la proximité en spécifiant un "champ de sortie de proximité". </p> <p>Voir <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> A propos de la recherche de proximité </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>39 </p> </td> 
   <td colname="col2"> <p>sp_sr </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sr= champ </span> </p> </td> 
   <td colname="col4"> <p>Indique le champ de classement à utiliser pour le classement statique. Le champ doit être un champ de type Classement avec une pertinence supérieure à 0. Si aucun paramètre <span class="codeph"> sp_sr </span> n’est fourni pour la requête, un champ de type Classement est automatiquement sélectionné. </p> <p>Pour désactiver le classement statique pour une requête particulière, incluez une valeur NULL pour <span class="codeph"> sp_sr </span> (par exemple, <span class="codeph"> &lt;input type="hidden" name="sp_sr" value=""&gt; </span>). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>40 </p> </td> 
   <td colname="col2"> <p>sp_sfvl_field </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_field= chaîne </span> </p> </td> 
   <td colname="col4"> <p>Indique le nom d’un champ à utiliser conjointement avec la balise <span class="codeph"> &lt;search-field-value-list&gt; </span> dans le modèle de recherche. </p> <p>Vous pouvez spécifier plusieurs paramètres <span class="codeph"> sp_sfvl_field </span> . </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>41 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_count </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_sfvl_df_count= <span class="varname"> &lt;valeur_entière&gt; </span></span> </p> </td> 
   <td colname="col4"> <p> 
     <!--NEW 2/2/2014-->Demande jusqu’à <span class="codeph"><span class="varname"> &lt;valeur_entière&gt; </span></span> <span class="codeph"> </span> les champs de facette dynamique search-field-value-list pour cette recherche. </p> <p>La valeur par défaut est 0. La valeur maximale autorisée est le nombre actuel de champs de facette dynamique, dynamic-facet-field-count défini pour un index donné. Les valeurs entières inférieures à 0 sont traitées comme 0. Les valeurs d’entiers spécifiées ci-dessus <span class="codeph"> sont plafonnées à </span> dynamic-facet-field-count <span class="codeph"> </span>. Les valeurs non entières sont ignorées ; ils sont traités comme la valeur par défaut. </p> <p>La recherche d’une tranche donnée est plafonnée avec une valeur maximale autorisée pour <span class="codeph"> sp_sfvl_df_count </span> de la <span class="codeph"> valeur </span> dynamique facette-champ-nombre de cette tranche. Lors de la fusion des résultats de la tranche, la valeur maximale effective de <span class="codeph"> sp_sfvl_df_count </span> est le nombre maximal réel <span class="codeph"> sp_sfvl_df_count </span> sur toutes les tranches. </p> <p>Voir <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuration des facettes dynamiques </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>42 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_exclude </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_exclude= &lt; <span class="varname"> nom_champ </span>&gt;[|&lt; <span class="varname"> nom_champ </span> </span>&gt;|... </p> </td> 
   <td colname="col4"> <p> Spécifie une liste de champs de facettes dynamiques spécifiques à exclure de la prise en compte pour cette recherche. </p> <p>Par défaut, tous les champs de facette dynamique sont pris en compte. </p> <p>Voir <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuration des facettes dynamiques </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>43 </p> </td> 
   <td colname="col2"> <p> sp_sfvl_df_include </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> </p> <p> <span class="codeph"> sp_sfvl_df_include= &lt; <span class="varname"> nom_champ </span>&gt;[|&lt; <span class="varname"> nom_champ </span> </span>&gt;|... </p> </td> 
   <td colname="col4"> <p> Spécifie une liste de champs de facettes dynamiques spécifiques à inclure dans les résultats de la recherche. </p> <p> <p>Remarque :  Le <span class="codeph"> paramètre </span> sp_sfvl_df_count <span class="codeph"> détermine le nombre total de champs de facette dynamique à renvoyer, y compris tout champ spécifié au moyen de </span>sp_sfvl_df_include. En d’autres termes, l’utilisation de <span class="codeph"> sp_sfvl_df_include </span> ne permet pas au nombre total de champs de facette dynamique renvoyés de dépasser <span class="codeph"> sp_sfvl_df_count </span>. </p> </p> <p>Voir <a href="../c-about-design-menu/c-about-dynamic-facets.md#task_D17F484130E448258100BAC1EEC53F39" format="dita" scope="local"> Configuration des facettes dynamiques </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>44 </p> </td> 
   <td colname="col2"> <p>sp_staged </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_staged= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p>Si <span class="codeph"> sp_staged=1 </span> est envoyé avec une requête, la requête exécutée est une recherche par étapes. </p> <p>Une recherche par étapes utilise tous les composants actuellement mis en scène, y compris l’index et les modèles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>45 </p> </td> 
   <td colname="col2"> <p>sp_start_day, sp_start_month, sp_start_year </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_start_day= nombre </span> </p> <p> <span class="codeph"> sp_start_month= nombre </span> </p> <p> <span class="codeph"> sp_start_year= nombre </span> </p> </td> 
   <td colname="col4"> <p>Ce triplet de valeurs spécifie la plage de dates de début de la recherche et vous le fournissez sous forme de jeu. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>46 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_ sugg _q </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_submit_q= nombre </span> </p> </td> 
   <td colname="col4"> <p>Le paramètre <span class="codeph"> sp_sugg_q </span> détermine le <span class="codeph"> paramètre sp_q[_#] </span> à utiliser avec le service Suggestion. </p> <p>La valeur par défaut de <span class="codeph"> sp_sugg_q </span> est 0, ce qui signifie que le moteur de recherche utilise la valeur de <span class="codeph"> sp_q </span> pour déterminer les suggestions. </p> <p>Définissez <span class="codeph"> sp_sugg_q=1 </span> pour utiliser la valeur de <span class="codeph"> sp_q_1 </span> pour déterminer les suggestions, etc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>47 </p> </td> 
   <td colname="col2"> <p>sp_t </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_t= chaîne </span> </p> </td> 
   <td colname="col4"> <p>Indique le modèle de transport à utiliser. </p> <p>Ce paramètre est utile si vous souhaitez contrôler l’apparence des résultats de recherche de base sur votre site Web en utilisant différents modèles de transport de recherche pour chaque zone de votre compte de recherche. </p> <p>Le modèle de transport par défaut est "search". </p> <p>Voir <a href="../c-appendices/c-templates.md#reference_12AAB3B9F4C74C11956F1DBA95714C2F" type="reference" format="dita" scope="local"> Gestion de plusieurs modèles de transport pour votre site Web </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>48 </p> </td> 
   <td colname="col2"> <p>sp_trace </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_trace= 0 ou 1 </span> </p> </td> 
   <td colname="col4"> <p>Lorsqu'il est défini sur <span class="codeph"> sp_stage=1 </span>, active la fonctionnalité de suivi de recherche principale dans le simulateur. </p> <p>Voir <a href="../c-about-simulator.md#concept_020AA6751E32421A96A3455508364C7E" format="dita" scope="local"> A propos du simulateur </a>. </p> <p> <p>Remarque :  Si ce paramètre n’est pas spécifié, la recherche principale ne collecte pas les informations de suivi et les balises de modèle de recherche principale associées n’ont aucune sortie. </p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>49 </p> </td> 
   <td colname="col2"> <p>sp_w, sp_w_control </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <code> sp_w= <i>sound-alike-enable</i> </code> </p> <p> <code> sp_w_control=<i>sound-alike-control</i> </code> </p> </td> 
   <td colname="col4"> <p>Indique que la correspondance du son doit être activée ou désactivée pour cette requête particulière. </p> <p>Le sp_w_control pour "Exact" est ignoré. La correspondance du son est désactivée. </p><p>Le sp_w_control pour "Alike" est ignoré. La correspondance du son est activée</p><p>Le sp_w_control pour Anything else est 1. La correspondance du son est désactivée. </p><p>Le sp_w_control pour Anything est autre chose. La correspondance du son est activée. </p>Le paramètre <span class="codeph"> sp_w_control </span> permet de créer une case à cocher aux termes négatifs ou positifs pour le contrôle utilisateur final de la correspondance son/son. </p> <p>Si <span class="codeph"> sp_w_control=0 </span> est utilisé, une case à cocher avec un mot négatif est utilisée pour définir le paramètre <span class="codeph"> sp_w </span> comme dans l'exemple suivant : </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="0"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="exact"&gt;No&nbsp;Sound-Alike&nbsp;matching </code> </p> <p>Si <span class="codeph"> sp_w_control=1 </span> est utilisé, une case à cocher avec une formulation positive est utilisée pour définir le <span class="codeph"> paramètre </span> sp_w comme suit : </p> <p> <code class="syntax html"> &lt;input&nbsp;type=hidden&nbsp;name="sp_w_control"&nbsp;value="1"&gt;&lt;input&nbsp;type=checkbox&nbsp;name="sp_w"&nbsp;value="alike"&gt;Sound-Alike&nbsp;matching </code> </p> <p>Voir l'exemple de formulaire de recherche avancée pour plus d'exemples sur l'utilisation des paramètres <span class="codeph"> _w_control </span> et <span class="codeph"> sp_w </span> . </p> <p>Voir <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Exemple de formulaire de recherche avancée </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>50 </p> </td> 
   <td colname="col2"> <p>sp_x </p> </td> 
   <td colname="col03"> <p> </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x= champ </span> </p> </td> 
   <td colname="col4"> <p>Indique les champs à rechercher dans la chaîne de requête. tout signifie rechercher dans tous les champs. title signifie rechercher uniquement les champs de titre. desc signifie rechercher uniquement les champs de description de document. clés signifie rechercher uniquement des mots-clés de document. body signifie rechercher uniquement le texte du corps. alt signifie rechercher uniquement du texte de remplacement. url signifie rechercher uniquement les valeurs d’URL. target signifie que la recherche ne cible que les mots-clés. Dans tous ces cas, les spécifications utilisateur des champs "text:", "desc:", "keys:", "body:", "alt:", "url:" et "target:" sont ignorées dans le paramètre <span class="codeph"> sp_q </span> correspondant. Si <span class="codeph"> sp_x </span> n’est pas présent ou s’il est défini sur une chaîne vide ou une autre chaîne, les préfixes de champ utilisateur standard sont autorisés. Pour plus d’informations sur les préfixes de champ, voir la description des conseils de recherche. </p> <p>Voir <a href="../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8" type="concept" format="dita" scope="local">A propos des recherches </a>. </p> <p>Consultez l’exemple de description du formulaire de recherche avancée pour obtenir des exemples d’utilisation du paramètre <span class="codeph"> sp_x </span> . </p> <p>Voir <a href="../c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A" type="reference" format="dita" scope="local"> Exemple de formulaire de recherche avancée </a>. </p> <p>Vous pouvez créer des requêtes qui recherchent tous les champs définis sur <span class="uicontrol"> Rechercher par défaut </span> sous <span class="uicontrol"> Options </span> &gt; <span class="uicontrol"> Métadonnées </span> <span class="uicontrol"> &gt; Définitions  en définissant  sp_x=n’importe quel . </span><span class="codeph"></span> Les champs prédéfinis et définis par l’utilisateur peuvent être utilisés comme valeur du paramètre <span class="codeph"> sp_x </span> . </p> <p>Vous pouvez également affecter plusieurs champs à une seule requête en définissant le paramètre <span class="codeph"> sp_x </span> plusieurs fois. Les lignes de modèle suivantes permettent aux utilisateurs d’interroger à la fois les champs "titre" et "auteur" pour les "Grands Livres". </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="title"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x"&nbsp;value="author"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="Great&nbsp;Books"&gt; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>51 </p> </td> 
   <td colname="col2"> <p> </p> </td> 
   <td colname="col03"> <p>sp_x_# </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sp_x_#= nom_champ </span> </p> </td> 
   <td colname="col4"> <p>Ce paramètre spécifie le champ à rechercher dans la requête <span class="codeph"> sp_q_# </span> correspondante. Le <span class="codeph"> n° <span class="codeph"> est remplacé par un nombre compris entre 1 et 16 (par exemple, </span> sp_x_8 </span> <span class="codeph"> </span>). Le nom de champ est un champ prédéfini ou défini par l’utilisateur. </p> <p>Si aucun paramètre <span class="codeph"> sp_x_# </span> n’est fourni pour une requête numérotée particulière, tous les champs définis comme <span class="uicontrol"> Rechercher par défaut </span> comme définis sous <span class="uicontrol"> Paramètres </span> <span class="uicontrol"> &gt;  de métadonnées &gt;  Définitions  sont recherchés par cette requête.</span><span class="uicontrol"></span> </p> <p>Par exemple, l’envoi du formulaire suivant renvoie tous les documents qui contiennent le mot "super" qui contient également le mot "Fitzgerald" dans le champ "author" : </p> <p> <code class="syntax html"> Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q"&nbsp;value="great"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="author"&gt;Search&nbsp;only&nbsp;documents&nbsp;written&nbsp;by:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="Fitzgerald"&gt; </code> </p> <p>Vous pouvez associer plusieurs noms de champ à une requête spécifique ou à une requête numérotée en fournissant plusieurs instances du même paramètre <span class="codeph"> _x </span> ou <span class="codeph"> sp_x_# </span> dans une seule requête de recherche. </p> <p>Par exemple, pour rechercher le mot "fleur" dans les champs "corps" et "clés", vous pouvez créer un formulaire de recherche avec les informations suivantes : </p> <p> <code class="syntax html"> &lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="body"&gt;&lt;input&nbsp;type="hidden"&nbsp;name="sp_x_1"&nbsp;value="keys"&gt;Search&nbsp;for:&nbsp;&lt;input&nbsp;type="text"&nbsp;name="sp_q_1"&nbsp;value="flower"&gt; </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exemple typique d’utilisation des paramètres CGI de recherche en arrière-plan {#section_260012BBC2514CC9A8E02E53DE8B41EE}

Les requêtes de lien suivantes lancent une recherche en utilisant &quot;Musique&quot; comme requête de recherche et utilisent tous les paramètres par défaut. Notez que l’URL est fractionnée sur deux lignes pour faciliter la lecture. Dans votre code HTML, ce lien doit tous se trouver sur une seule ligne.

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

Vous devez généralement utiliser les paramètres par défaut lors du lancement d’une recherche. Ainsi, la première page est affichée, triée par pertinence, et permet au client de choisir d’autres pages et d’autres options. Si le formulaire de recherche de votre site comporte des options pour les collections, transmettez le nom de la collection en tant que paramètre.

## Exemple détaillé d’utilisation des paramètres CGI de recherche en arrière-plan {#section_5FA3C620D5124FB2AB28857F8D8473F6}

Les requêtes de formulaire suivantes affichent `25` les résultats en commençant par le résultat `10`. Les résumés ne sont pas affichés, l’ordre de tri est par date et la collection nommée `support` est utilisée. Seuls les documents datant des 30 derniers jours sont renvoyés.

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

