---
description: Chaque fois que votre site Web change, vous pouvez exécuter un script ou un programme demandant au robot de recherche d'exécuter un index à l'aide de la télécommande.
seo-description: Chaque fois que votre site Web change, vous pouvez exécuter un script ou un programme demandant au robot de recherche d'exécuter un index à l'aide de la télécommande.
seo-title: A propos du contrôle à distance pour l'indexation
solution: Target
title: A propos du contrôle à distance pour l'indexation
topic: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# A propos du contrôle à distance pour l&#39;indexation{#about-remote-control-for-indexing}

Chaque fois que votre site Web change, vous pouvez exécuter un script ou un programme demandant au robot de recherche d&#39;exécuter un index à l&#39;aide de la télécommande.

## Utilisation du contrôle à distance pour l&#39;indexation {#concept_C79B322190E84106A434E5C6D4A4118F}

La demande d’indexation de la télécommande provient généralement d’un script ou d’un programme situé sur votre serveur.

Le robot effectue les mêmes étapes d&#39;indexation que si elle avait été lancée manuellement à partir du [!DNL Index] menu. Pour envoyer une demande de contrôle à distance, vous devez configurer le mot de passe et les chaînes de réponse nécessaires.

## Comment effectuer une demande de contrôle à distance {#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

Pour effectuer une demande de contrôle à distance, utilisez les exemples de format suivants en fonction de l’emplacement de votre centre de données :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Emplacement du centre de données </p> </th> 
   <th colname="col2" class="entry"> <p>Exemple </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Londres </p> </td> 
   <td colname="col2"> <p> <code> https://center.lon5.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Amérique du Nord </p> </td> 
   <td colname="col2"> <p> <code> https://center.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Singapour </p> </td> 
   <td colname="col2"> <p> <code> https://center.sin2.atomz.com/search/cgiindex.tk? <b>sp_a=sp99999999&amp;sp_password=xxxxxx&amp;sp_operation=op</b> </code> </p> </td> 
  </tr> 
 </tbody> 
</table>

ou

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne et valeur </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp99999999 </span> </p> </td> 
   <td colname="col2"> <p> Votre numéro de compte. </p> <p>Vous pouvez trouver votre numéro de compte sous <span class="uicontrol"> Paramètres <b>&gt; Options</b> de </span> <span class="uicontrol"> <b></b> compte &gt;  Paramètres du compte.</span><span class="uicontrol"><b></b></span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N </span> </p> </td> 
   <td colname="col2"> <p>Permet de vérifier l’état d’une analyse d’index en cours d’exécution. </p> <p> <span class="codeph">  N </span> est un entier positif ou <span class="codeph"> tout </span>. S’il s’agit d’une valeur numérique, les N dernières <span class="codeph"> lignes </span> du fichier journal d’index correspondant sont incluses dans la réponse JSON. </p> <p>Si la valeur est <span class="codeph"> all </span>, le fichier entier est renvoyé. </p> <p>Si la valeur est <span class="codeph"> 0 </span>, aucune information de journal n’est renvoyée. Il s’agit de la valeur par défaut d’une requête d’état d’index en cours d’exécution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op </span> </p> </td> 
   <td colname="col2"> <p>Permet de spécifier l’une des opérations d’indexation suivantes à exécuter : </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index </span> <p>Le robot de recherche exécute un index complet de votre site Web. </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incremental_index </span> <p>Le robot de recherche exécute un index incrémentiel à l’aide de la configuration définie sous <span class="uicontrol"> Index <b>&gt; Index</b> </span> incrémentiel <span class="uicontrol"> <b></b> &gt; Configuration.</span><span class="uicontrol"><b></b></span> </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index </span> <p>Le robot de recherche exécute une mise à jour verticale à l’aide de la configuration définie sous <span class="uicontrol"> Index <b>&gt; Mise à jour</b> </span> verticale <span class="uicontrol"> <b></b> &gt; Configuration.</span><span class="uicontrol"><b></b></span> </p> <p>Voir <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> A propos de la mise à jour</a>verticale. </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index </span> <p>Le robot de recherche exécute un index incrémentiel à l’aide du fichier texte spécifié sous <span class="uicontrol"> Index <b>&gt;</b> Index </span> par script &gt; Configuration <span class="uicontrol"> <b></b> .</span><span class="uicontrol"><b></b></span> </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index </span> <p>Le robot de recherche exécute un index complet par étape de votre site Web. </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incremental_staged_index </span> <p>Le robot de recherche exécute un index intermédiaire incrémentiel à l’aide de la configuration définie sous <span class="uicontrol"> Index <b></b> &gt; Index </span> <span class="uicontrol"> incrémentiel <b></b>  &gt;  Configuration.</span><span class="uicontrol"><b></b></span> </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index </span> <p>Le robot de recherche exécute une mise à jour verticale par étapes à l’aide de la configuration définie sous <span class="uicontrol"> Index <b></b> &gt; Mise à jour </span> <span class="uicontrol"> verticale <b></b>  &gt;  Configuration.</span><span class="uicontrol"><b></b></span> </p> </li> 
     </ul> </p> <p>Remarque :  Pour utiliser les mises à jour verticales, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe. </p> <p>Voir <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> A propos de la mise à jour verticale </a>. </p> <p>Vous pouvez ajouter <span class="codeph"> _save </span> à l’une des valeurs <span class="codeph"> _operation ci-dessus </span> pour que le robot de recherche tente d’utiliser du contenu enregistré. Par exemple, vous pouvez spécifier les éléments suivants : </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p>ou </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>Vous pouvez également ajouter <span class="codeph"> _status </span> à l’une des valeurs <span class="codeph"> _operation ci-dessus </span> pour demander un rapport d’état pour l’opération en cours ou la plus récente. Par exemple, vous pouvez spécifier les éléments suivants : </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p>ou </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>et les résultats sont renvoyés sous la forme d’un objet JSON. Incluez <span class="codeph"> sp_lines=N </span> pour inclure N lignes du fichier journal associé. Si N est négatif, les N dernières lignes sont incluses. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= push_live </span> </p> </td> 
   <td colname="col2"> <p> Vous permet de diffuser un index par étapes à distance. </p> <p>Toute tentative d’ajout de <span class="codeph"> _enregistré </span> à l’opération de diffusion en direct est ignorée. </p> <p>Lorsque vous exécutez une opération <span class="codeph"> push-live </span> , une chaîne de texte OK, Priority ou Error est renvoyée au serveur. Vous spécifiez ces chaînes de réponse sur la page <span class="wintitle"> Contrôle à distance </span> . </p> <p>Voir <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> Configuration du contrôle à distance pour l’indexation</a>. </p> <p>Si vous poussez en direct en l’absence d’index d’évaluation, rien ne se passe et la chaîne de réponse OK est renvoyée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxxx </span> </p> </td> 
   <td colname="col2"> <p>Mot de passe de la télécommande. </p> </td> 
  </tr> 
 </tbody> 
</table>

La recherche renvoie des données sous la forme d’une réponse HTTP appropriée. La réponse complète se compose d’un état HTTP, d’en-têtes de réponse HTTP, d’une ligne vide et de la chaîne de réponse.

Supposons, par exemple, que vous exécutiez la demande de contrôle à distance suivante :

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

Voici la réponse du serveur :

```
Status: 200 OK 
Content-type: text/plain 
OK
```

Supposons également que vous exécutiez la demande d’état de contrôle à distance suivante :

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status
```

La réponse du serveur peut se présenter comme suit :

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:58:58-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "status": 1, 
    "message": "ok" 
}
```

Pour obtenir les dix premières lignes de la liste des journaux associées à cette opération d’index, ainsi que son état, la requête suivante est utilisée :

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=10
```

Réponse du serveur :

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T10:59:30-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "offset": 672, 
    "lines": [ 
        "07/25 16:40:07 PST   ======== Starting manual crawl of account sp99999999. ========", 
        "07/25 16:40:08 PST   Loading existing data", 
        "07/25 16:40:08 PST   Downloading entrypoint https://www.atomz.com/", 
        "07/25 16:40:08 PST   Robots.txt exclude mask: https://www.atomz.com/snap", 
        "07/25 16:40:08 PST   Exclude mask: regexp ^https://www.atomz.com/$", 
        "07/25 16:40:08 PST   Include mask: https://www.atomz.com/", 
        "07/25 16:40:08 PST   Downloading https://www.atomz.com/style.css", 
        "07/25 16:40:09 PST   Ignoring https://www.atomz.com/style.css, document type 'text/css'.", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/privacy.html", 
        "07/25 16:40:09 PST   Downloading https://www.atomz.com/terms.html" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Note the `offset` value. Cette valeur identifie la position du décalage de fichier dans le fichier journal où la lecture est laissée en suspens. Pour lire les dix lignes *suivantes* du fichier, vous devez inclure, dans cet exemple, `&sp_offset=672` dans la requête envoyée au serveur.

Grâce `sp_offset`à cette fonctionnalité, vous pouvez parcourir un fichier journal de manière efficace.

Pour obtenir les *dix dernières* lignes du journal, ainsi que l’état, indiquez le nombre comme nombre négatif. Par exemple, spécifiez `sp_lines=` la valeur `-10` comme suit :

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index_status&sp_lines=-10
```

Réponse du serveur :

```
Status: 200 OK 
Content-type: application/json; charset=utf-8 
{ 
    "current_time": "2017-08-27T11:01:14-0700", 
    "start_time": "2017-07-25T16:40:07-0800", 
    "end_time": "2017-07-25T16:40:20-0800", 
    "elapsed_seconds": 13, 
    "elapsed_seconds_fmt": "13s", 
    "state": "finished", 
    "docs_indexed": 3, 
    "depth": 0, 
    "errors": 0, 
    "lines": [ 
        "07/25 16:40:20 PST   End Time: 07/25/2017 16:40:20 PST", 
        "07/25 16:40:20 PST   Elapsed Time: 13 seconds", 
        "07/25 16:40:20 PST   Pages Crawled: 3 pages", 
        "07/25 16:40:20 PST   Pages Indexed: 3 pages", 
        "07/25 16:40:20 PST   Words/Bytes Indexed: 2373 words/ 20618 bytes", 
        "07/25 16:40:20 PST   Errors: 0", 
        "07/25 16:40:20 PST   *** Index Summary ***", 
        "07/25 16:40:20 PST   Total Pages: 3", 
        "07/25 16:40:20 PST   --------------------------------------------------------------------", 
        "07/25 16:40:20 PST   ======== Finish manual crawl of account sp99999999: Done. ========" 
    ], 
    "status": 1, 
    "message": "ok" 
}
```

Notez qu’aucune `offset` valeur n’est renvoyée ici, car cette opération s’est terminée à la fin du fichier et qu’il n’y a plus de lignes à lire.

## Configuration du contrôle à distance pour l’indexation {#task_57C296258404448DA7A5ADC9B7232391}

Chaque fois que votre site Web change, vous pouvez utiliser Remote Control pour exécuter un script ou un programme à partir de votre serveur, en demandant au robot de recherche d&#39;exécuter un index.

**Pour configurer Remote Control pour l&#39;indexation**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Remote Control]**.
1. Sur la [!DNL Remote Control] page, définissez chaque option de champ de configuration pour pouvoir envoyer automatiquement une requête d’indexation de votre serveur afin d’indexer votre site Web.

   <table> 
    <thead> 
    <tr> 
    <th colname="col1" class="entry"> <p>Option </p> </th> 
    <th colname="col2" class="entry"> <p>Description </p> </th> 
    </tr> 
    </thead>
    <tbody> 
    <tr> 
    <td colname="col1"> <p>Mot de passe de contrôle à distance </p> </td> 
    <td colname="col2"> <p>Indiquez le mot de passe de la télécommande. </p> <p> Les mots de passe sont sensibles à la casse (au moins six caractères) et doivent comprendre au moins une lettre. Il est recommandé d’inclure également au moins un nombre. </p> <p>N’utilisez pas le mot de passe de connexion de recherche/marchandisage de votre site. </p> <p>Votre mot de passe est utilisé dans chaque demande de contrôle à distance. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Chaîne de réponse OK </p> </td> 
    <td colname="col2"> <p>Permet de spécifier une chaîne de texte de réponse OK si l’opération d’index demandée commence avec succès. Dans ce cas, le robot de recherche renvoie votre chaîne de réponse OK au serveur. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Chaîne de réponse de priorité </p> </td> 
    <td colname="col2"> <p>Si une autre opération d'indexation est en cours lorsque la demande distante est effectuée, le robot de recherche ne peut pas exécuter l'index demandé. Dans ce cas, votre chaîne de texte de réponse de priorité est renvoyée au serveur. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Chaîne de réponse d’erreur </p> </td> 
    <td colname="col2"> <p>Permet de spécifier une chaîne de texte de réponse à une erreur si votre mot de passe est incorrect ou en cas d’erreur. Dans ce cas, le robot de recherche renvoie votre chaîne de réponse d’erreur au serveur. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
