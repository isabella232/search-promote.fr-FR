---
description: Chaque fois que votre site Web change, vous pouvez exécuter un script ou un programme demandant au robot de recherche d'exécuter un index à l'aide de la télécommande.
solution: Target
title: A propos du contrôle à distance pour l'indexation
topic-legacy: Index,Site search and merchandising
uuid: 20e230c6-5c1a-4bf4-bff3-b8236d14ab21
exl-id: 1a7689f9-1e3f-48c8-a5f1-abe0efdb7768
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '1037'
ht-degree: 1%

---

# À propos du contrôle à distance pour l&#39;indexation{#about-remote-control-for-indexing}

Chaque fois que votre site Web change, vous pouvez exécuter un script ou un programme demandant au robot de recherche d&#39;exécuter un index à l&#39;aide de la télécommande.

## Utilisation de la commande à distance pour l&#39;indexation {#concept_C79B322190E84106A434E5C6D4A4118F}

La demande d&#39;indexation de contrôle à distance provient généralement d&#39;un script ou d&#39;un programme situé sur votre serveur.

Le robot effectue les mêmes étapes d&#39;indexation que s&#39;il avait été démarré manuellement à partir du menu [!DNL Index]. Pour envoyer une demande de contrôle à distance, vous devez configurer le mot de passe et les chaînes de réponse nécessaires.

## Comment faire une demande de contrôle à distance {#section_42FAB2BAB25A4E24BEA69566C6D1C70F}

Pour effectuer une demande de contrôle à distance, utilisez les exemples de format suivants en fonction de l&#39;emplacement de votre centre de données :

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
   <td colname="col1"> <p> <span class="codeph"> sp_a= sp999999999  </span> </p> </td> 
   <td colname="col2"> <p> Votre numéro de compte. </p> <p>Vous pouvez trouver votre numéro de compte sous <span class="uicontrol"> <b>Paramètres</b> </span> &gt; <span class="uicontrol"> <b>Options de compte</b> </span> &gt; <span class="uicontrol"> <b>Paramètres du compte</b> </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_lines= N  </span> </p> </td> 
   <td colname="col2"> <p>Permet de vérifier l'état d'une analyse d'index en cours d'exécution. </p> <p> <span class="codeph">  N  </span> est un entier positif ou  <span class="codeph"> tout  </span>. S’il s’agit d’une valeur numérique, les dernières lignes <span class="codeph"> N </span> du fichier journal d’index correspondant sont incluses dans la réponse JSON. </p> <p>Si la valeur est <span class="codeph"> all </span>, le fichier entier est renvoyé. </p> <p>Si la valeur est <span class="codeph"> 0 </span>, aucune information de journal n'est renvoyée. Il s’agit de la valeur par défaut d’une requête d’état d’index en cours d’exécution. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= op  </span> </p> </td> 
   <td colname="col2"> <p>Permet de spécifier l’une des opérations d’indexation suivantes à exécuter : </p> <p> 
     <ul id="ul_6CA190AC41694BC293FC7C6BABA629FE"> 
      <li id="li_EFC76E31D47E473F9A56B2EBA8A97CA1"> <span class="codeph"> full_index  </span> <p>Le robot de recherche exécute un index complet de votre site Web. </p> </li> 
      <li id="li_A9ACE21718804A21B3DA7B84AB6729D3"> <span class="codeph"> incremental_index  </span> <p>Le robot de recherche exécute un index incrémentiel en utilisant la configuration définie sous <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Index incrémentiel</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_722FE409AE454AD48ACE95C4CDC7A00B"> <span class="codeph"> vertical_index  </span> <p>Le robot de recherche exécute une mise à jour verticale en utilisant la configuration définie sous <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Mise à jour verticale</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> <p>Voir <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> À propos de la mise à jour verticale</a>. </p> </li> 
      <li id="li_A40B513CE17043A4925CE3D4DE0B48A4"> <span class="codeph"> script_index  </span> <p>Le robot de recherche exécute un index incrémentiel à l’aide du fichier texte spécifié sous <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Index par script</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_A0BC7F1373B14393997BAB7690FD3EF7"> <span class="codeph"> full_staged_index  </span> <p>Le robot de recherche exécute un index complet par étape de votre site Web. </p> </li> 
      <li id="li_47753E358457443A95B384A278FACA83"> <span class="codeph"> incremental_staged_index  </span> <p>Le robot de recherche exécute un index échelonné incrémentiel en utilisant la configuration définie sous <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Index incrémentiel</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
      <li id="li_C8B5F8F1208E438ABEFDF9129A6B14A3"> <span class="codeph"> vertical_staged_index  </span> <p>Le robot de recherche exécute une mise à jour verticale par étapes en utilisant la configuration définie sous <span class="uicontrol"> <b>Index</b> </span> &gt; <span class="uicontrol"> <b>Mise à jour verticale</b> </span> &gt; <span class="uicontrol"> <b>Configuration</b></span>. </p> </li> 
     </ul> </p> <p>Remarque :  Pour utiliser les mises à jour verticales, vous devrez peut-être les activer dans votre compte par le représentant de votre compte d'Adobe ou par l'assistance Adobe. </p> <p>Voir <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> À propos de la mise à jour verticale </a>. </p> <p>Vous pouvez ajouter <span class="codeph"> _save </span> à l'une des valeurs <span class="codeph"> sp_operation </span> ci-dessus pour que le robot de recherche tente d'utiliser le contenu enregistré. Par exemple, vous pouvez spécifier les éléments suivants : </p> <p> <code class="syntax html"> sp_operation=full_index_saved </code> </p> <p>ou </p> <p> <code class="syntax html"> sp_operation=full_staged_index_saved </code> </p> <p>Vous pouvez également ajouter <span class="codeph"> _status </span> à l'une des valeurs <span class="codeph"> sp_operation </span> ci-dessus pour demander un rapport d'état pour l'opération en cours ou la plus récente. Par exemple, vous pouvez spécifier les éléments suivants : </p> <p> <code class="syntax html"> sp_operation=full_index_status </code> </p> <p>ou </p> <p> <code class="syntax html"> sp_operation=full_staged_index_status </code> </p> <p>et les résultats sont renvoyés sous la forme d’un objet JSON. Insérez <span class="codeph"> sp_lines=N </span> pour inclure N lignes dans le fichier journal associé. Si N est négatif, les N dernières lignes sont incluses. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_operation= pushlive  </span> </p> </td> 
   <td colname="col2"> <p> Permet de diffuser à distance un index intermédiaire. </p> <p>Toute tentative d’ajout de <span class="codeph"> _save </span> à l’opération de publication Push est ignorée. </p> <p>Lorsque vous exécutez une opération <span class="codeph"> push </span>, une chaîne de texte de réponse OK, Priorité ou Erreur est renvoyée au serveur. Vous spécifiez ces chaînes de réponse sur la page <span class="wintitle"> Remote Control </span>. </p> <p>Voir <a href="../c-about-index-menu/c-about-remote-control-for-indexing.md#task_57C296258404448DA7A5ADC9B7232391" format="dita" scope="local"> Configuration du contrôle à distance pour l'indexation</a>. </p> <p>Si vous poussez en direct alors qu’il n’existe aucun index intermédiaire, rien ne se produit et la chaîne de réponse OK est renvoyée. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sp_password= xxxxxx  </span> </p> </td> 
   <td colname="col2"> <p>Mot de passe de la télécommande. </p> </td> 
  </tr> 
 </tbody> 
</table>

La recherche renvoie des données sous la forme d’une réponse HTTP appropriée. La réponse complète est composée d’un état HTTP, d’en-têtes de réponse HTTP, d’une ligne vide et de la chaîne de réponse.

Par exemple, supposons que vous effectuiez la demande de contrôle à distance suivante :

```
https://center.atomz.com/search/cgiindex.tk?sp_a=sp99999999&sp_password=my-password&sp_operation=full_index
```

Voici la réponse du serveur :

```
Status: 200 OK 
Content-type: text/plain 
OK
```

Ou supposons que vous effectuiez la demande d&#39;état de contrôle à distance suivante :

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

Pour obtenir les dix premières lignes de la liste des journaux associées à cette opération d&#39;index, ainsi que son état, la requête suivante est utilisée :

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

Notez la valeur `offset`. Cette valeur identifie la position de décalage de fichier dans le fichier journal où la lecture est laissée en arrière. Pour lire les dix lignes *next* du fichier, vous devez inclure, dans cet exemple, `&sp_offset=672` dans la requête envoyée au serveur.

`sp_offset` permet de parcourir efficacement un fichier journal.

Pour obtenir les *dernières* lignes du journal, ainsi que l’état, indiquez le nombre comme nombre négatif. Par exemple, spécifiez `sp_lines=` avec la valeur `-10` comme dans l’exemple suivant :

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

Notez qu’aucune valeur `offset` n’est renvoyée ici, car cette opération s’est terminée à la fin du fichier et qu’il n’y a plus de lignes à lire.

## Configuration du contrôle à distance pour l&#39;indexation {#task_57C296258404448DA7A5ADC9B7232391}

Chaque fois que votre site Web change, vous pouvez utiliser la télécommande pour exécuter un script ou un programme à partir de votre serveur, en demandant au robot de recherche d&#39;exécuter un index.

**Pour configurer le contrôle à distance pour l&#39;indexation**

1. Dans le menu produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Remote Control]**.
1. Sur la page [!DNL Remote Control], définissez chaque option de champ de configuration pour pouvoir envoyer automatiquement une demande d&#39;indexation de votre serveur afin d&#39;indexer votre site Web.

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
    <td colname="col2"> <p>Indiquez le mot de passe de la télécommande. </p> <p> Les mots de passe sont sensibles à la casse (au moins six caractères) et doivent contenir au moins une lettre. Il est recommandé d’inclure également au moins un nombre. </p> <p>N’utilisez pas le mot de passe de connexion de recherche/marchandisage de votre site. </p> <p>Votre mot de passe est utilisé dans chaque demande de contrôle à distance. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Chaîne de réponse OK </p> </td> 
    <td colname="col2"> <p>Permet de spécifier une chaîne de texte de réponse OK si l’opération d’index demandée commence avec succès. Dans ce cas, le robot de recherche renvoie au serveur votre chaîne de réponse OK. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Chaîne de réponse prioritaire </p> </td> 
    <td colname="col2"> <p>Si une autre opération d'indexation est en cours lorsque la demande distante est effectuée, le robot de recherche ne peut pas exécuter l'index demandé. Dans ce cas, votre chaîne de texte de réponse Priorité est renvoyée au serveur. </p> </td> 
    </tr> 
    <tr> 
    <td colname="col1"> <p>Chaîne de réponse d’erreur </p> </td> 
    <td colname="col2"> <p>Permet de spécifier une chaîne de texte de réponse d’erreur Si votre mot de passe est incorrect ou si une autre erreur se produit. Dans ce cas, le robot de recherche renvoie à nouveau au serveur votre chaîne de réponse d’erreur. </p> </td> 
    </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
