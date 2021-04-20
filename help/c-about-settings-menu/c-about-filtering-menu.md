---
description: Utilisez le menu Filtrage pour utiliser des scripts qui modifient le contenu d’un document Web avant son indexation.
solution: Target
subtopic: Filtering
title: A propos du menu Filtrage
topic: Settings,Site search and merchandising
uuid: ebb08fa8-4e17-417d-868b-11fc2af9f284
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '4008'
ht-degree: 1%

---


# A propos du menu Filtrage{#about-the-filtering-menu}

Utilisez le menu Filtrage pour utiliser des scripts qui modifient le contenu d’un document Web avant son indexation.

## A propos du script de filtrage {#concept_E56B73D625854AB2A899EF2D56CFCB47}

Vous pouvez utiliser [!DNL Filtering Script] pour modifier le contenu d&#39;un document Web avant qu&#39;il ne soit indexé.

Vous pouvez insérer des balises HTML, supprimer du contenu non pertinent et même créer de nouvelles métadonnées HTML basées sur l’URL d’un document, le type MIME et le contenu existant. Le script de filtrage est un script Perl, qui offre une gestion puissante des chaînes et la flexibilité de la mise en correspondance régulière des expressions. Vous utilisez le script de filtrage avec un script d’initialisation, un script de terminaison, un script de masques d’URL et une URL de test.

Le script de filtrage est exécuté chaque fois qu’un document est lu à partir de votre site Web. En d&#39;autres termes, le script s&#39;exécute comme un filtre standard. Il lit les données de STDIN, les transforme d&#39;une certaine façon et écrit les résultats à STDOUT. Vous pouvez utiliser le script de filtrage pour imprimer les messages d’état du script de filtrage vers le journal d’index. Vous imprimez les messages à STDERR ou au moyen de la sous-routine `_search_debug_log()`.

Certaines options de différences GNU que vous pouvez utiliser en mode **[!UICONTROL Expert (diff)]** sur la page Script de filtrage par étapes, incluent les éléments suivants :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Option diff GNU </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b </span> </p> </td> 
   <td colname="col2"> <p> Ignore les modifications apportées à l’espace blanc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B </span> </p> </td> 
   <td colname="col2"> <p> Ignore les modifications qui insèrent ou suppriment des lignes vierges. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie contextuel, avec trois lignes de contexte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C lignes  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie de contexte, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i </span> </p> </td> 
   <td colname="col2"> <p> ignore les modifications de casse ; considérez les lettres en majuscules et en minuscules comme équivalentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Génère une sortie qui ressemble à un script ed mais dont l’ordre d’affichage dans le fichier est modifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n </span> </p> </td> 
   <td colname="col2"> <p> produit des diffusions au format RCS ; comme <span class="codeph"> -f </span>, sauf que chaque commande spécifie le nombre de lignes concernées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie unifié, avec trois lignes de contexte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U lignes  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie unifié, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez utiliser des variables locales, globales ou les deux dans ces scripts. Toutes les variables globales sont préfacées avec l’espace de nommage &quot;main::&quot;. Lorsque le script de filtrage est démarré, son environnement contient les gestionnaires de fichiers standard suivants :

* STDIN - rien (renvoie immédiatement EOF lorsqu&#39;il est lu)
* STDOUT - HTML de remplacement (si les données sont imprimées sur STDOUT, elles sont utilisées à la place du document d’origine)
* STDERR : les données imprimées sur STDERR sont imprimées dans le journal d&#39;index en tant qu&#39;erreur.

De plus, vous pouvez écrire des messages personnalisés dans le journal d&#39;index à l&#39;aide de la sous-routine `_search_debug_log()`, comme dans l&#39;exemple suivant :

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Ces messages s’affichent avec le mot `DEBUG` comme préface et ne sont pas consignés comme des erreurs.

Voici un exemple de filtrage. Les champs de la page Web `<title>` commencent souvent par le nom de la société. Bien que ces informations soient utiles à la navigation sur le site, elles ne sont pas pertinentes lors de la recherche. Si les titres de toutes les pages Web de MegaCorp sont débuts avec une chaîne commune, telle que :

```
<title>MegaCorp -- meaningful title 
here</title>
```

Vous devez supprimer &quot; `MegaCorp --`&quot; du début de chaque titre de document et compter chaque document traité avec le script de filtrage. Pour ce faire, vous pouvez utiliser le script suivant :

```
# Make sure this is an HTML document. 
if ($main::ws_content_type =~ /^text\/html/) { 
    # Read the entire document into a local scalar variable. 
    my @docarray = <>; 
    my $doc = join("", @docarray); 
 
    # Remove "MegaCorp -- " from the title. 
    $doc =~ s/(<TITLE>)MegaCorp -- /$1/gis; 
 
    # Print the resulting document. 
    print $doc; 
 
    # Count that we've filtered one more document. 
    $main::doc_count++; 
}
```

## Variables globales {#global-variables}

Vous pouvez utiliser les variables suivantes dans tout script de filtrage :

| Variable | Description |
|--- |--- |
| `$main::search_crawl_type` | La valeur `$main::search_crawl_type` indique le type d&#39;opération d&#39;index en cours.  Formulaire obsolète : `$main::ws_crawl_type` Les opérations d&#39;index et les valeurs associées sont les suivantes : <ul><li>Index complet : Manuel - `manual`</li><li>Index complet : Programmé - `auto`</li><li>Index complet : Contrôle à distance : `CGI`</li><li>Index incrémentiel : Manuel - `manual-incremental`</li><li>Index incrémentiel : Programmé - `auto-incremental` </li><li>Index incrémentiel : Contrôle à distance : `CGI-incremental`</li><li>Index par script : Manuel - `manual-indexlist.txt` </li><li>Index par script : Programmé - `auto-indexlist.txt`</li><li>Index par script : Contrôle à distance : `CGI-indexlist.txt`</li><li>Régénérer - `manual-upgrade`</li></ul> |
| `$main::search_clear_cache` | La valeur indique si l’option d’indexation &quot;Effacer le cache d’index&quot; a été demandée pour l’opération d’indexation en cours. Si &quot;Effacer le cache d&#39;index&quot; a été demandé, la valeur de `$main::search_clear_cache` est &quot; `1`&quot;.  Formulaire obsolète :`$main::ws_clear_cache` |
| `$main::search_fields` | La valeur contient une liste séparée par des tabulations des champs de métadonnées définis dans le compte. Par défaut, la valeur est :   `url title desc keys target body alt date charset language` Formulaire obsolète : `$main::ws_fields` |
| `$main::search_collections` | La valeur contient une liste des collections séparées par des tabulations qui sont définies dans le compte.  Formulaire obsolète :`$main::ws_collections` |
| `$main::search_url` | La valeur est l’URL complète du document.  Formulaire obsolète :`$main::ws_url` |
| `$main::search_content_type` | La valeur est le type de contenu du document tel qu’il est extrait de la balise meta http-equiv. La valeur type est &quot;text/html; charset=iso-8859-1&quot;.  Formulaire obsolète :`$main::ws_content_type` |
| `$main::search_content_class` | La valeur est la classe de contenu du document, telle qu’elle est dérivée du champ de type de contenu.  Formulaire obsolète :`$main::ws_content_class` |
| `$main::search_syntax_check` | La valeur reflète l’utilisation du bouton &quot;Vérifier la syntaxe&quot;. Si vous cliquez dessus, la valeur est 1 (un); sinon, sa valeur est 0 (zéro).  Formulaire obsolète :`$main::ws_syntax_check` |
| `$main::search_last_mod_date` | Si elle est fournie par le serveur Web, cette valeur contient la représentation Epoch (secondes depuis le 1er janvier 1970) de la date de dernière modification du document.  Vous pouvez formater cette valeur en utilisant l’appel de bibliothèque Perl localtime(). |

### Conseils rapides {#section_89A5C16911744AF98E232DF608C6A1F5}

* Toutes les variables globales sont préfacées avec l’espace de nommage &quot;main::&quot; : `$main::doc_count = 0;`
* Toutes les variables locales sont déclarées avec &quot;my&quot; : `my $i = 0;`
* Les sous-routines sont définies dans le script d’initialisation. Ils n&#39;ont pas besoin d&#39;un espace de nommage &quot;principal : :&quot; explicite : `sub my_sub {` `...`

   `}`

* Testez `$main::search_content_type` avant d&#39;apporter des modifications à un fichier. Les tests peuvent vous aider à éviter d’apporter des modifications imprudentes aux fichiers binaires, tels que les fichiers SWF ou PDF :

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type` est l&#39;en-tête Content-Type complet fourni par votre serveur. Il peut parfois contenir un type MIME simple, tel que &quot;text/html&quot;. Il peut également contenir un type MIME suivi d’autres informations, telles que le codage du jeu de caractères du document, comme &quot;text/html; charset=iso-8859-1&quot;.
* Pour chaque type de document non HTML, `$main::search_content_type` peut prendre différentes valeurs. Le test de chaque valeur de votre script devient fastidieux. Par exemple, certains documents Word comportent des valeurs de type de contenu &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; ou &quot;application/x-msword&quot;. Dans ce cas, `$main::search_content_class` peut prendre les valeurs suivantes :

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * text

* Dans cet exemple, le test de `$main::search_content_class` pour &quot;word&quot; correspondrait à l’une des trois valeurs de type de contenu possibles.
* Si rien n&#39;est imprimé à STDOUT à partir du script de filtrage, le document est utilisé exactement tel qu&#39;il a été téléchargé. Autrement dit, si vous n&#39;avez pas besoin de changer quoi que ce soit dans un document, vous n&#39;avez pas besoin de copier STDIN dans STDOUT pour ce document.
* Si vous souhaitez supprimer tout le texte d&#39;un document, imprimez un fichier STDOUT valide. Par exemple, pour supprimer complètement tout le texte d’un document HTML, procédez comme suit : `print "<html></html>";`

## Ajouter un script de filtrage {#task_0AB84FD1133F47F9AA069A79BEA13A22}

Le script de filtrage est un script Perl exécuté pour chaque document téléchargé à partir de votre site Web.

Vous utilisez le script de filtrage conjointement avec un script d’initialisation, un script de terminaison et un script de masques d’URL.

Veillez à recréer l’index de votre site afin que les résultats de votre script de filtrage soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Pour ajouter un script de filtrage**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Filtering Script]**.
1. (Facultatif) Sur la page [!DNL Filtering Script], dans le champ [!DNL Test URL], saisissez l’URL d’un document sur votre site Web.

   Cliquez sur une option de test pour afficher les modifications apportées au texte HTML brut.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Champ de l’URL de test </p> </td> 
      <td colname="col2"> <p>Permet de saisir l’URL d’un document sur votre site Web. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test </p> </td> 
      <td colname="col2"> <p>Teste l’URL par rapport aux scripts de filtrage et aux masques d’URL. </p> <p>Le document d’URL de test est téléchargé, puis utilisé comme entrée STDIN dans le script de filtrage. Les scripts d’initialisation, de filtrage et de terminaison sont alors exécutés. S’il existe une sortie STDOUT issue du script de filtrage, cette sortie s’affiche dans une nouvelle fenêtre du navigateur. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test uniquement </p> </td> 
      <td colname="col2"> <p>Teste uniquement l’opération du script. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Aperçu </p> </td> 
      <td colname="col2"> <p>Permet de vue à la page. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Visuel complet </p> </td> 
      <td colname="col2"> <p>Génère une vue complète de table avant et après des documents. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Visuel court </p> </td> 
      <td colname="col2"> <p>Affiche uniquement les différences entre les vues avant et après. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Expert (diff) </p> </td> 
      <td colname="col2"> <p>Affiche la sortie brute de la commande GNU diff utilisée pour comparer les fichiers, à l'aide des options de ligne de commande fournies. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Script de filtrage </p> </td> 
      <td colname="col2"> <p>Permet de coller le script de filtrage dans le champ fourni. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Enregistrer les modifications </p> </td> 
      <td colname="col2"> <p>Enregistre le script de filtrage. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Vérifier la syntaxe </p> </td> 
      <td colname="col2"> <p>Permet de vérifier rapidement la syntaxe de votre script en exécutant les scripts d’initialisation, de filtrage et de terminaison. Il ne met pas à jour et n’enregistre pas votre script. </p> <p>Toutes les erreurs et avertissements du compilateur Perl, ainsi que toutes les sorties de STDERR sont imprimées. </p> <p>Avant que les effets du script ne soient visibles par les clients, vous devez recréer l’index de votre site. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   **Options de ligne de commande GNU diff**

   Certaines options de différences GNU que vous pouvez utiliser en mode **[!UICONTROL Expert (diff)]** sur la page Script de filtrage par étapes, incluent les éléments suivants :

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>GNU diff, option de ligne de commande </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
      <td colname="col2"> <p> Ignore les modifications apportées à l’espace blanc. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
      <td colname="col2"> <p> Ignore les modifications qui insèrent ou suppriment des lignes vierges. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
      <td colname="col2"> <p> Utilise le format de sortie contextuel, avec trois lignes de contexte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -C lignes  </span> </p> </td> 
      <td colname="col2"> <p> Utilise le format de sortie de contexte, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
      <td colname="col2"> <p> ignore les modifications de casse ; considérez les lettres en majuscules et en minuscules comme équivalentes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
      <td colname="col2"> <p> Génère une sortie qui ressemble à un script ed mais dont l’ordre d’affichage dans le fichier est modifié. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
      <td colname="col2"> <p> produit des diffusions au format RCS ; comme <span class="codeph"> -f </span>, sauf que chaque commande spécifie le nombre de lignes concernées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>-u </p> </td> 
      <td colname="col2"> <p> Utilise le format de sortie unifié, avec trois lignes de contexte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <span class="codeph"> -U lignes  </span> </p> </td> 
      <td colname="col2"> <p> Utilise le format de sortie unifié, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Test]** pour tester les scripts de filtrage et les masques d’URL.

   Le fait de cliquer sur **[!UICONTROL Test]** ne met pas à jour et n&#39;enregistre pas votre script de filtrage.
1. Dans le champ [!DNL Filtering Script], collez votre script.
1. (Facultatif) Cliquez sur **[!UICONTROL Check Syntax]** pour vérifier rapidement la syntaxe de votre script en exécutant les scripts de filtrage, d’initialisation et de terminaison.

   **[!UICONTROL Check Syntax]** ne met pas à jour et n’enregistre pas votre script.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Filtering Script], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos du script d&#39;initialisation {#concept_048B4C8BC9F74BE8BB6162C490C201A3}

Vous pouvez utiliser [!DNL Initialization Script] pour modifier le contenu d&#39;un document Web avant qu&#39;il ne soit indexé.

Vous pouvez insérer des balises HTML, supprimer du contenu non pertinent et même créer de nouvelles métadonnées HTML basées sur l’URL d’un document, le type MIME et le contenu existant. Le script d&#39;initialisation est un script Perl, qui permet une gestion puissante des chaînes et la flexibilité de la mise en correspondance régulière des expressions. Vous utilisez le script d’initialisation avec un script de filtrage, un script de terminaison, un script de masques d’URL et une URL de test.

Le script d’initialisation est exécuté une fois avant que l’indexation ne commence. Utilisez ce script pour initialiser toutes les variables globales et sous-routines utilisées par votre script de filtrage. Vous pouvez utiliser le script d’initialisation pour imprimer des messages d’état depuis le script de filtrage vers le journal d’index. Vous imprimez les messages à STDERR ou par l&#39;intermédiaire de la sous-routine `_search_debug_log()`.

Certaines options de différences GNU que vous pouvez utiliser en mode **[!UICONTROL Expert (diff)]** sur la page Script d&#39;initialisation intermédiaire, incluent les éléments suivants :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Option diff GNU </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Ignore les modifications apportées à l’espace blanc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Ignore les modifications qui insèrent ou suppriment des lignes vierges. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie contextuel, avec trois lignes de contexte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C lignes  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie de contexte, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> ignore les modifications de casse ; considérez les lettres en majuscules et en minuscules comme équivalentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Génère une sortie qui ressemble à un script ed mais dont l’ordre d’affichage dans le fichier est modifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> produit des diffusions au format RCS ; comme <span class="codeph"> -f </span>, sauf que chaque commande spécifie le nombre de lignes concernées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie unifié, avec trois lignes de contexte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U lignes  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie unifié, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez utiliser des variables locales, globales ou les deux dans ces scripts. Toutes les variables globales sont préfacées avec l’espace de nommage &quot;main::&quot;. Lorsque le script d’initialisation est démarré, son environnement contient les gestionnaires de fichiers standard suivants :

* STDIN - rien (renvoie immédiatement EOF lorsqu&#39;il est lu)
* STDOUT - rien (si les données sont imprimées sur STDOUT, elles sont ignorées)
* STDERR : les données imprimées sur STDERR sont imprimées dans le journal d&#39;index en tant qu&#39;erreur.

De plus, vous pouvez écrire des messages personnalisés dans le journal d&#39;index à l&#39;aide de la sous-routine `_search_debug_log()`, comme dans l&#39;exemple suivant :

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Ces messages s’affichent avec le mot `DEBUG` comme préface et ne sont pas consignés comme des erreurs.

Voici un exemple de script d’initialisation :

```
# My subroutine to do something. 
sub my_sub_for_the_filtering_script { 
    my ($param1, $param2) = @_; 
    ... 
} 
 
# Initialize the document counter. 
$main::doc_count = 0;
```

Voir [Variables globales](#global-variables).

### Conseils rapides {#section_A2CC0302CAF14135BF8EF6171FB184F1}

* Toutes les variables globales sont préfacées avec l’espace de nommage &quot;main::&quot; : `$main::doc_count = 0;`
* Toutes les variables locales sont déclarées avec &quot;my&quot; : `my $i = 0;`
* Les sous-routines sont définies dans le script d’initialisation. Ils n&#39;ont pas besoin d&#39;un espace de nommage &quot;principal : :&quot; explicite : `sub my_sub {` `...`

   `}`

* Testez `$main::search_content_type` avant d&#39;apporter des modifications à un fichier. Les tests peuvent vous aider à éviter d’apporter des modifications imprudentes aux fichiers binaires, tels que les fichiers SWF ou PDF :

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type` est l&#39;en-tête Content-Type complet fourni par votre serveur. Il peut parfois contenir un type MIME simple, tel que &quot;text/html&quot;. Il peut également contenir un type MIME suivi d’autres informations, telles que le codage du jeu de caractères du document, comme &quot;text/html; charset=iso-8859-1&quot;.
* Pour chaque type de document non HTML, `$main::search_content_type` peut prendre différentes valeurs. Le test de chaque valeur de votre script devient fastidieux. Par exemple, certains documents Word comportent des valeurs de type de contenu &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; ou &quot;application/x-msword&quot;. Dans ce cas, `$main::search_content_class` peut prendre les valeurs suivantes :

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * texte

* Dans cet exemple, le test de `$main::search_content_class` pour &quot;word&quot; correspondrait à l’une des trois valeurs de type de contenu possibles.
* Si rien n&#39;est imprimé à STDOUT à partir du script de filtrage, le document est utilisé exactement tel qu&#39;il a été téléchargé. Autrement dit, si vous n&#39;avez pas besoin de changer quoi que ce soit dans un document, vous n&#39;avez pas besoin de copier STDIN dans STDOUT pour ce document.
* Si vous souhaitez supprimer tout le texte d&#39;un document, imprimez un fichier STDOUT valide. Par exemple, pour supprimer complètement tout le texte d’un document HTML, procédez comme suit : `print "<html></html>";`

## Ajouter un script d&#39;initialisation {#task_5A03B8D0C46E4674B7CE88203515803B}

Le script d’initialisation est un script Perl qui s’exécute une fois avant que les documents ne soient indexés.

Vous utilisez le script d’initialisation conjointement avec un script de filtrage, un script de terminaison et un script de masques d’URL.

Veillez à recréer l’index de votre site afin que les résultats de votre script d’initialisation soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Pour ajouter un script d’initialisation**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Initialization Script]**.
1. (Facultatif) Sur la page [!DNL Initialization Script], dans le champ [!DNL Test URL], saisissez l’URL d’un document sur votre site Web.

   Cliquez sur une option de test pour afficher les modifications apportées au texte HTML brut.

   Voir le tableau des options de filtrage sous **Ajouter un script de filtrage**.

   Cliquez sur **[!UICONTROL Test]** pour tester les scripts de filtrage et les masques d’URL.

   Le fait de cliquer sur **[!UICONTROL Test]** ne met pas à jour et n&#39;enregistre pas votre script d&#39;initialisation.
1. Dans le champ [!DNL Initialization Script], collez votre script.
1. (Facultatif) Cliquez sur **[!UICONTROL Check Syntax]** pour vérifier rapidement la syntaxe de votre script en exécutant les scripts de filtrage, d’initialisation et de terminaison.

   **[!UICONTROL Check Syntax]** ne met pas à jour et n’enregistre pas votre script.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Initialization Script], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos du script de résiliation {#concept_AAD6B3B0E7124874AD0947096FC42F47}

Vous pouvez utiliser [!DNL Termination Script] pour modifier le contenu d&#39;un document Web avant qu&#39;il ne soit indexé.

Vous pouvez insérer des balises HTML, supprimer du contenu non pertinent et même créer de nouvelles métadonnées HTML basées sur l’URL d’un document, le type MIME et le contenu existant. Le script d&#39;initialisation est un script Perl, qui permet une gestion puissante des chaînes et la flexibilité de la mise en correspondance régulière des expressions. Vous utilisez le script de terminaison avec un script d’initialisation, un script de filtrage, un script de terminaison, un script de masques d’URL et une URL de test.

Le script de terminaison est exécuté une fois que tous les documents sont indexés. Vous pouvez utiliser le script de fin pour imprimer les messages d’état du script de filtrage vers le journal d’index. Vous imprimez les messages à STDERR ou par l&#39;intermédiaire de la sous-routine `_search_debug_log()`.

Certaines options de ligne de commande GNU diff que vous pouvez utiliser en mode **[!UICONTROL Expert (diff)]** sur la page Script d&#39;interruption de service, incluent les éléments suivants :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>GNU diff, option de ligne de commande </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -b  </span> </p> </td> 
   <td colname="col2"> <p> Ignore les modifications apportées à l’espace blanc. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -B  </span> </p> </td> 
   <td colname="col2"> <p> Ignore les modifications qui insèrent ou suppriment des lignes vierges. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -c  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie contextuel, avec trois lignes de contexte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -C lignes  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie de contexte, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -i  </span> </p> </td> 
   <td colname="col2"> <p> ignore les modifications de casse ; considérez les lettres en majuscules et en minuscules comme équivalentes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -f  </span> </p> </td> 
   <td colname="col2"> <p> Génère une sortie qui ressemble à un script ed mais dont l’ordre d’affichage dans le fichier est modifié. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -n  </span> </p> </td> 
   <td colname="col2"> <p> produit des diffusions au format RCS ; comme <span class="codeph"> -f </span>, sauf que chaque commande spécifie le nombre de lignes concernées. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>-u </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie unifié, avec trois lignes de contexte. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -U lignes  </span> </p> </td> 
   <td colname="col2"> <p> Utilise le format de sortie unifié, avec des lignes (un entier) de contexte, ou trois si des lignes ne sont pas données. </p> </td> 
  </tr> 
 </tbody> 
</table>

Vous pouvez utiliser des variables locales, globales ou les deux dans ces scripts. Toutes les variables globales sont préfacées avec l’espace de nommage &quot;main::&quot;. Lorsque le script de terminaison est démarré, son environnement contient les gestionnaires de fichiers standard suivants :

* STDIN - rien (renvoie immédiatement EOF lorsqu&#39;il est lu)
* STDOUT - rien (si les données sont imprimées sur STDOUT, elles sont ignorées)
* STDERR : les données imprimées sur STDERR sont imprimées dans le journal d&#39;index en tant qu&#39;erreur.

De plus, vous pouvez écrire des messages personnalisés dans le journal d&#39;index à l&#39;aide de la sous-routine `_search_debug_log()`, comme dans l&#39;exemple suivant :

```
# Log information to the Index Log 
_search_debug_log("Done processing document: " . $main::search_url);
```

Ces messages s’affichent avec le mot `DEBUG` comme préface et ne sont pas consignés comme des erreurs.

Pour afficher le nombre de documents traités par votre script de filtrage sous forme de ligne d’erreur dans le journal d’index, vous pouvez utiliser le script de terminaison suivant :

```
# Print the value of the document counter. 
print STDERR "Total docs: $main::doc_count\n"; 
# Or, using the log subroutine: 
_search_debug_log("Total docs: " . $main::doc_count);
```

Voir [Variables globales](#global-variables).

### Conseils rapides {#section_5790EA7ACAC046CBA01F759F88E2460F}

* Toutes les variables globales sont préfacées avec l’espace de nommage &quot;main::&quot; : `$main::doc_count = 0;`
* Toutes les variables locales sont déclarées avec &quot;my&quot; : `my $i = 0;`
* Les sous-routines sont définies dans le script d’initialisation. Ils n&#39;ont pas besoin d&#39;un espace de nommage &quot;principal : :&quot; explicite : `sub my_sub {` `...`

   `}`

* Testez `$main::search_content_type` avant d&#39;apporter des modifications à un fichier. Les tests peuvent vous aider à éviter d’apporter des modifications imprudentes aux fichiers binaires, tels que les fichiers SWF ou PDF :

   `if ($main::search_content_type =~ /^text\/html/) { ...`

* `$main::search_content_type` est l&#39;en-tête Content-Type complet fourni par votre serveur. Il peut parfois contenir un type MIME simple, tel que &quot;text/html&quot;. Il peut également contenir un type MIME suivi d’autres informations, telles que le codage du jeu de caractères du document, comme &quot;text/html; charset=iso-8859-1&quot;.
* Pour chaque type de document non HTML, `$main::search_content_type` peut prendre différentes valeurs. Le test de chaque valeur de votre script devient fastidieux. Par exemple, certains documents Word comportent des valeurs de type de contenu &quot;application/msword&quot;, &quot;application/vnd.ms-word&quot; ou &quot;application/x-msword&quot;. Dans ce cas, `$main::search_content_class` peut prendre les valeurs suivantes :

   * html
   * pdf
   * word
   * excel
   * powerpoint
   * mp3
   * texte

* Dans cet exemple, le test de `$main::search_content_class` pour &quot;word&quot; correspondrait à l’une des trois valeurs de type de contenu possibles.
* Si rien n&#39;est imprimé à STDOUT à partir du script de filtrage, le document est utilisé exactement tel qu&#39;il a été téléchargé. Autrement dit, si vous n&#39;avez pas besoin de changer quoi que ce soit dans un document, vous n&#39;avez pas besoin de copier STDIN dans STDOUT pour ce document.
* Si vous souhaitez supprimer tout le texte d&#39;un document, imprimez un fichier STDOUT valide. Par exemple, pour supprimer complètement tout le texte d’un document HTML, procédez comme suit : `print "<html></html>";`

## Ajouter un script de terminaison {#task_F0CFB412871642CFBC88132889C5B6F9}

Le script de terminaison est un script Perl qui est exécuté une fois après l’indexation de tous les documents.

Vous utilisez le script de fin conjointement avec un script de filtrage, un script de fin et un script de masques d’URL.

Veillez à recréer l’index de votre site afin que les résultats de votre script d’initialisation soient visibles par vos clients.

Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).

**Pour ajouter un script de terminaison**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Termination Script]**.
1. (Facultatif) Sur la page [!DNL Termination Script], dans le champ [!DNL Test URL], saisissez l’URL d’un document sur votre site Web.

   Cliquez sur une option de test pour afficher les modifications apportées au texte HTML brut.

   Consultez le tableau des options de filtrage sous **Ajouter un script de filtrage**.

   Cliquez sur **[!UICONTROL Test]** pour tester les scripts de filtrage et les masques d’URL.

   Le fait de cliquer sur **[!UICONTROL Test]** ne met pas à jour et n&#39;enregistre pas votre script de terminaison.
1. Dans le champ [!DNL Termination Script], collez votre script.
1. (Facultatif) Cliquez sur **[!UICONTROL Check Syntax]** pour vérifier rapidement la syntaxe de votre script en exécutant les scripts d’initialisation, de filtrage et de terminaison.

   **[!UICONTROL Check Syntax]** ne met pas à jour et n’enregistre pas votre script.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Termination Script], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos du script de masques d&#39;URL {#concept_384F32EA18F84853A7BA99A04009330B}

Le filtrage vous permet de modifier le contenu d’un document Web avant son indexation. Vous pouvez insérer des balises HTML, supprimer du contenu non pertinent et même créer de nouvelles métadonnées HTML basées sur l’URL d’un document, le type MIME et le contenu existant. Le script de masques d’URL est un script Perl qui permet une gestion puissante des chaînes et la souplesse d’une correspondance d’expression régulière.

Pour modifier le contenu des documents qui n’existent que dans une partie spécifique de votre site Web, vous pouvez spécifier des masques d’URL, exclure des masques d’URL ou les deux pour définir les pages appropriées.

Si vous souhaitez modifier uniquement les documents sous `"https://www.mysite.com/faqs/"`, vous pouvez utiliser l’ensemble de masques suivant :

```
include https://www.mysite.com/faqs/ 
exclude *
```

Vous pouvez également utiliser une expression régulière dans un script de masque d’URL, comme dans l’exemple suivant :

```
include regexp ^https://www\.mysite\.com.*/faqs/.*$ 
exclude *
```

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

Les masques d’URL par script sont pris en compte dans l’ordre dans lequel vous les avez entrés dans le champ [!DNL URL Masks]. Lorsqu’une URL de document correspond à un masque, ce document est inclus ou exclu en fonction du type de masque. Si une URL de document ne correspond à aucun masque d’URL, le document est inclus uniquement si son type MIME est &quot;text/html&quot;. Tous les autres types MIME sont exclus.

## Ajouter un script de masque d&#39;URL {#task_D18F2A496C1C45C997B5DA650AAF5D59}

Spécifiez l’URL pour inclure des masques et exclure des masques afin de modifier le contenu des documents qui n’existent que dans une portion spécifique de votre site Web.

Avant que les effets des paramètres Masques d’URL ne soient visibles pour les visiteurs, recréez l’index de votre site.

**Pour ajouter un script de masque d’URL**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL URL Masks]**.
1. (Facultatif) Sur la page [!DNL URL Masks], dans le champ [!DNL Test URL], saisissez l’URL d’un document sur votre site Web, puis cliquez sur **[!UICONTROL Test]** pour tester l’URL par rapport aux scripts de filtrage et aux masques.

   Le document d’URL de test est téléchargé et utilisé comme entrée STDIN dans le script de filtrage. Ensuite, les scripts de filtrage, d’initialisation et de terminaison sont exécutés. S’il existe une sortie STDOUT du script de filtrage, cette sortie s’affiche dans une nouvelle fenêtre du navigateur.

   Le fait de cliquer sur **[!UICONTROL Test]** ne met pas à jour et n&#39;enregistre pas votre script.
1. Dans le champ [!DNL URL Masks], saisissez un masque d’URL par ligne.
1. (Facultatif) Cliquez sur **[!UICONTROL Check Syntax]** pour vérifier rapidement la syntaxe de vos masques d’URL en exécutant les scripts de filtrage, d’initialisation et de terminaison.

   **[!UICONTROL Check Syntax]** ne met pas à jour et n’enregistre pas votre script.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL URL Masks], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des types de contenu dans le filtrage {#concept_E3EFF4A148EA4D21AFD0A5453A00427E}

Permet de sélectionner les types de contenu à filtrer pour ce compte.

Le texte trouvé dans les types de contenu sélectionnés est converti au format HTML, puis traité à l’aide du script spécifié dans le script de filtrage.

Voir [A propos du filtrage de script](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

Les types de contenu que vous pouvez sélectionner sont les suivants :

* DOCUMENTS PDF
* Documents de texte
* Films Flash Adobe
* Fichiers Microsoft Word
* Fichiers Microsoft Office (OpenXML)
* Fichiers Microsoft Excel
* Fichiers Microsoft Powerpoint
* Texte dans les fichiers de musique MP3

Avant que les effets des paramètres Types de contenu ou les modifications apportées aux paramètres ne soient visibles par les clients, vous devez regénérer l&#39;index de votre site.

## Sélection des types de contenu filtrés {#task_C46081FA425A43EC8FDE6EA4A52A170A}

Sélectionnez les types de contenu à transmettre au script spécifié dans le script de filtrage.

Voir [A propos du filtrage de script](../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47).

**Pour sélectionner les types de contenu filtrés**

1. Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Filtering]** > **[!UICONTROL Content Types]**.
1. Sur la page [!DNL Content Types], vérifiez les types de contenu à transmettre au script de filtre.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de votre site d’évaluation si vous souhaitez prévisualisation les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Content Types], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
