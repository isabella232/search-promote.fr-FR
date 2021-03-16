---
description: Avec l'index par script, vous pouvez écrire, mettre à jour et gérer des options d'indexation incrémentielle sans avoir à vous connecter. Le robot de recherche lit les instructions à partir d’un fichier texte hébergé sur votre serveur.
solution: Target
subtopic: Scripted Index
title: A propos de l’index par script
topic: Index, recherche sur le site et marchandisage
uuid: 51e726ad-414b-4cbd-8a68-fefc3cf9b565
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1730'
ht-degree: 1%

---


# A propos de l’index par script{#about-scripted-index}

Avec l&#39;index par script, vous pouvez écrire, mettre à jour et gérer des options d&#39;indexation incrémentielle sans avoir à vous connecter. Le robot de recherche lit les instructions à partir d’un fichier texte hébergé sur votre serveur.

## Utilisation de l’index par script {#concept_34F58D551BC04BFB8ADC294B9DA9199D}

## A propos de la configuration de l&#39;indexation incrémentielle par script {#section_161D254065E143F3A39F3FC09C400090}

Pour utiliser l’index par script, vous utilisez la page Configuration de l’index incrémentiel par script pour spécifier l’URL d’un fichier de script (fichier de texte brut) situé sur votre serveur. Par exemple, `https://www.mysite.com/indexlist.txt`. À mesure que votre site change, vous pouvez ajouter des blocs de commande au fichier texte, manuellement ou automatiquement (avec un script déclenché par l’arrivée d’informations à partir d’un flux d’actualités, d’un télex boursier ou d’un autre fichier modifié).

Lorsque l&#39;index incrémentiel par script commence, le robot de recherche lit le fichier texte et exécute les nouvelles commandes qui se trouvent dans ce fichier. Par défaut, le robot de recherche ne traite que les nouvelles commandes, qui sont déterminées par la date du fichier. A moins que vous ne cochiez **[!UICONTROL Clear Date]** au moment de la configuration de l&#39;index par script, le robot de recherche &quot;mémorise&quot; le spécificateur de date du dernier bloc traité.

## A propos du fichier de script {#section_B312E40539F44C6583B4F9637D428E19}

Le fichier de script que vous spécifiez dans l’URL est un fichier texte brut qui se trouve sur votre serveur. Vous pouvez utiliser des retours chariot, des flux de ligne ou les deux pour la séquence de fin de ligne. Une ligne vide contient zéro ou plusieurs caractères d’espace, suivis d’une séquence de fin de ligne. Toutes les commandes ne sont pas sensibles à la casse.

Le fichier texte est organisé en blocs décrivant les informations utilisées par le robot de recherche lorsqu&#39;il effectue un index incrémentiel par script.

Les blocs sont classés par date, les blocs les plus anciens se trouvant en haut du fichier texte et les blocs les plus récents en bas. Chaque bloc commence par une commande-date sur une seule ligne et une commande de spécificateur de date et se termine par un séparateur de ligne vide, comme dans l&#39;exemple de bloc suivant (entre plusieurs commandes) :

Un zéro de début est requis pour toutes les dates ordinales inférieures au 10e lors de l’utilisation du style HTTP 1.1. Par exemple, le 6 novembre est le 6 novembre, pas le 6 novembre.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Commande </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>date-commande </p> </td> 
   <td colname="col2"> <p>La première ligne de chaque début de bloc comporte l'une des deux commandes de date : </p> <p> 
     <ul id="ul_9C1B229B7F1846C490B853FC34989E77"> 
      <li id="li_31FEF1A7163842BDBB0ABE779D07045A"> <span class="codeph"> date </span> <p>Utilisez la commande "date" pour indiquer que le spécificateur de date se composera d’un jour, d’une date, d’une heure et d’un fuseau horaire. </p> </li> 
      <li id="li_0918D5B090014C1A852CB80BB7C2867C"> <span class="codeph"> secondes</span> <p>Utilisez <span class="codeph"> secondes </span> pour indiquer que le spécificateur de date se composera d’une heure en quelques secondes (par exemple, 784111777). Lorsque vous utilisez <span class="codeph"> secondes </span>, veillez à ce que le nombre de secondes augmente entre les blocs. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>spécificateur de date </p> </td> 
   <td colname="col2"> <p>La commande <span class="codeph"> spécificateur de date </span> enregistre généralement soit la date et l'heure ordinales (commande de date), soit l'heure en secondes (commande de secondes) pendant lesquelles les informations de bloc ont été ajoutées au fichier. Par exemple : </p> <p> <code> date&nbsp;Sun,&nbsp;06&nbsp;Nov&nbsp;1994&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.1&nbsp;style) 
      date&nbsp;Sunday,&nbsp;06-Nov-94&nbsp;08:49:37&nbsp;GMT&nbsp;(HTTP&nbsp;1.0&nbsp;style) 
      date&nbsp;Sun&nbsp;Nov&nbsp;6&nbsp;08:49:37&nbsp;1994&nbsp;(Unix&nbsp;asctime()&nbsp;date&nbsp;style) 
      seconds&nbsp;784111777&nbsp;(Unix&nbsp;epoch-seconds&nbsp;style) </code> </p> <p>Un zéro de début est requis pour toutes les dates ordinales inférieures au 10e lors de l’utilisation du style HTTP 1.1. Par exemple, le 6 novembre est le 6 novembre, pas le 6 novembre. </p> <p>Le robot de recherche "mémorise" le spécificateur de date du dernier bloc traité et n'indexe que les informations qu'il considère comme étant "plus récentes". (Le temps réel n'a pas d'importance pour le robot de recherche. Au lieu de cela, c'est le temps par rapport aux autres heures précédemment traitées qui importe.) </p> <p>Une fois que le robot de recherche lit un bloc avec un spécificateur de date de 22h00, par exemple, il ne lit aucun bloc qui enregistre des heures avant 22h00, indépendamment du moment où l'opération d'indexation s'exécute. Dans le pire des cas, vous pouvez entrer par erreur l’année "2040" au lieu de "2004" dans votre spécificateur de date. Dans un tel cas, le robot de recherche indexe le bloc 2040 lors de la prochaine opération d'indexation, puis refuse de lire d'autres blocs d'informations (à moins qu'un post-date 2040). Si cela se produit, supprimez tous les blocs précédemment traités du fichier texte, cliquez sur <span class="uicontrol"> Effacer la date </span>, puis poussez-le en direct. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ligne de commentaire </p> </td> 
   <td colname="col2"> <p>Commencez les lignes de commentaire par le caractère "#". </p> <p>Chaque ligne de commentaire doit être une ligne qui lui est propre ; vous ne pouvez pas saisir de commentaires de fin de ligne. </p> <p>Une ligne de commentaire n’est pas considérée comme une ligne vide. Il peut également apparaître n’importe où dans un bloc, même avant une commande de date ou de secondes, comme dans l’exemple suivant : </p> <p> <code> &nbsp;&nbsp;&nbsp;&nbsp;#Added&nbsp;by&nbsp;Cathy&nbsp;Read&nbsp;after&nbsp;the&nbsp;Y2K&nbsp;seminar 
      &nbsp;&nbsp;&nbsp;&nbsp;date&nbsp;Mon,&nbsp;29&nbsp;Dec&nbsp;1999&nbsp;09:32:20&nbsp;GMT&nbsp; </code> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>action-commande </p> </td> 
   <td colname="col2"> <p>Chaque bloc de texte peut contenir autant de commandes d'action que vous le souhaitez. Les options de commande-action suivantes correspondent à celles de l’indexation incrémentielle standard : </p> <p> 
     <ul id="ul_8E1435350A0F416BB8F7826CD3886E74"> 
      <li id="li_22181666628C48A28A6A0BA1F7CA8E77"> 
       <code>
         add 
       </code> <p>Utilisation avec l’URL. Le robot de recherche indexe uniquement les URL spécifiées qui ont changé depuis votre dernière opération d'indexation. De plus, le robot de recherche suit les liens contenus dans des documents et index spécifiés uniquement les documents qui ont changé. </p> <p>Vous pouvez suivre l’URL avec 
        <code>
          nofollow 
        </code> ou 
        Mots-clés <code>
          noindex 
        </code> comme dans l'exemple suivant : </p> <p> <code> add&amp;nbsp;https://www.mydomain.com/&amp;nbsp;noindex </code> </p> </li> 
      <li id="li_8E47BF07DB24417083883F5BF40D6B9E"> 
       <code>
         update 
       </code> <p>Utilisation avec masque d’URL. Le robot de recherche trouve et met à jour tous les documents qui correspondent au masque d'URL spécifié. </p> <p>Vous pouvez suivre l’URL avec 
        <code>
          nofollow 
        </code> ou 
        Mots-clés <code>
          noindex 
        </code> comme dans l'exemple suivant : </p> <p> <code> update&amp;nbsp;https://www.mydomain.com/products/ </code> </p> </li> 
      <li id="li_B3EC8B1670D54F66A1D8411A694EF7E4"> 
       <code>
         include 
       </code> ou 
       <code>
         exclude 
       </code> <p>Utilisation avec masque d’URL. Le robot de recherche trouve et indexe ("include") ou ignore ("exclude") les documents en fonction du type de masque spécifié. </p> <p>Par exemple : </p> <p> <code> include&amp;nbsp;https://www.mydomain.com/products/household/lightbulbs*.html </code> </p> <p>ou </p> <p> <code> exclude&amp;nbsp;https://www.mydomain.com/archive/ </code> </p> </li> 
      <li id="li_050B54B735F0475E93806455FA6DC6A5"> 
       <code>
         include-date 
       </code> ou 
       <code>
         exclude-date 
       </code> <p>Utilisation avec masque d’URL. Le robot de recherche trouve et indexe ("include") ou ignore ("exclude") les documents en fonction de l’URL et de la date des documents. Les types de masques suivants sont disponibles : </p> <p> 
        <ul id="ul_23A15CB492214B86BE84D8E6EA1820AE"> 
         <li id="li_0C7051AC3B5A4C57A3E477F7B6246611"> 
          <code>
            include-days NNN 
          </code> <p>Le robot de recherche indexe tous les documents qui correspondent au masque d'URL spécifié et qui sont âgés de NNN ou plus. </p> <p>Vous pouvez suivre le masque d'URL avec les mots-clés 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code> et/ou 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_983A10E2ED5D434EA9031F32143F4EF4"> 
          <code>
            include-date YYYY-MM-DD 
          </code> <p> Le robot de recherche indexe tous les documents qui correspondent au masque d’URL spécifié et qui sont aussi anciens ou plus anciens que la date AAAA-MM-JJ, où "AAAA" correspond à l’année à 4 chiffres, "MM" à un ou deux chiffres (1-12) et "JJ" à un ou deux chiffres (1-31). </p> <p>Vous pouvez suivre le masque d'URL avec les mots-clés 
           <code>
             nofollow 
           </code>, 
           <code>
             noindex 
           </code> et/ou 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_733CE1B748024CECA7FBE00D7BC7B88A"> 
          <code>
            exclude-days NNN 
          </code> <p> Désactive l’indexation de tous les documents qui correspondent au masque d’URL spécifié et qui sont de NNN jours ou plus anciens. </p> <p>Vous pouvez suivre le masque d'URL avec le mot-clé 
           <code>
             server-date 
           </code>. </p> </li> 
         <li id="li_90056A0B96CC4DA3854711860A15CE89"> 
          <code>
            exclude-date YYYY-MM-DD 
          </code> <p>Désactive l’indexation de tous les documents qui correspondent au masque d’URL spécifié et qui sont aussi anciens ou plus anciens que la date AAAA-MM-JJ. </p> <p>Vous pouvez suivre le masque d'URL avec le mot-clé 
           <code>
             server-date 
           </code>. </p> </li> 
        </ul> </p> </li> 
      <li id="li_AA78F22B60FE4535BE73BA87A8992C08"> 
       <code>
         delete 
       </code> <p>Spécifiez les URL. Le robot de recherche supprime les documents de l’index identifiés par l’URL. </p> </li> 
      <li id="li_9C63061568AA4D57A4FEBCF6DB9194EC"> 
       <code>
         deletemask 
       </code> <p>Le robot de recherche supprime des documents de l’index qui correspondent au masque d’URL spécifié. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [A propos des masques d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

## Exemple de fichier de script {#section_9F580F20E7214751B157A28B392BD64E}

Dans l’exemple de fichier de script suivant, le robot de recherche traite les blocs à condition que les spécificateurs de date postdatent le spécificateur de date du dernier bloc traité. Si tel est le cas, les opérations d’indexation suivantes se produisent :

* Supprime `y2k-problems.html` de l&#39;index.
* Ajoute `no-y2k-problems.html` à l&#39;index de recherche et ne suit aucun des liens de `no-y2k-problems.html`.

* Lors de l’analyse, excluez les URL qui correspondent à `housewares.htm` et `lightfixtures.htm`l de l’index de recherche.

* Incluez tous les autres répertoires et documents sous `www.mydomain.com`.
* Mettez à jour tous les documents des répertoires `products` et `information`, en analysant et en indexant tous les liens subsidiaires qui ont changé depuis la dernière opération d&#39;indexation.

* Lors de l’analyse, excluez les URL de la section `archive` du site Web si elles sont datées au plus tard le 1er janvier 1999.
* Exclure les URL qui correspondent à `housewares.html` et `lightfixtures.html` de l&#39;index de recherche.

* Indexez les fichiers dans le répertoire `help`, mais n&#39;analysez ni n&#39;indexez aucun lien à partir de ces fichiers.
* Analyser et indexer tous les autres fichiers rencontrés pour `www.mydomain.com`.

```
# Start of file. 
# Added by John Smith 
date Sat, 01 Jan 2004 16:05:53 PST 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/ 
delete https://www.mydomain.com/y2k-problems.html 
add https://www.mydomain.com/no-y2k-problems.html nofollow 
 
date Sun, 02 Jan 2004 20:19:08 PST 
# Added by the wire service updater 
exclude-date 1999-01-01 https://www.mydomain.com/archive server-date 
exclude https://www.mydomain.com/housewares.html 
exclude https://www.mydomain.com/lightfixtures.html 
include https://www.mydomain.com/help/ nofollow 
include https://www.mydomain.com/ 
# no add files, just update existing files 
# update all files in the "products" directory 
update https://www.mydomain.com/products/ 
# update all files in the "information" directory 
update regexp ^https://www\.mydomain\.com/information/.*$ 
# End of file.
```

## Configuration d’un index incrémentiel par script {#task_05AE040FE75E40FFAA5E10B6B6D4D255}

Vous pouvez spécifier un script que vous avez créé qui écrit, met à jour et maintient un index incrémentiel, sans avoir à vous connecter. Le robot de recherche lit les instructions du fichier texte hébergé sur votre serveur pour exécuter l&#39;index incrémentiel.

**Pour configurer un index incrémentiel par script**

1. Dans le menu produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Configuration]**.
1. Sur la page **[!UICONTROL Scripted Incremental Index Configuration]**, dans **[!UICONTROL Script File URL]**, saisissez l’URL du script de fichier texte situé sur votre serveur.

   Voir [A propos de l’index par script](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D).
1. (Facultatif) Cochez **[!UICONTROL Clear Date]** si vous ne souhaitez pas que le robot de recherche &quot;se souvienne&quot; du spécificateur de date du dernier bloc traité.

   Par défaut, le robot de recherche ne traite que les nouveaux blocs de commandes qui se trouvent dans le fichier texte, qui est déterminé par la date du fichier. Si vous ne souhaitez pas que la valeur par défaut soit définie, vérifiez **[!UICONTROL Clear Date]**.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Définition de la planification de l&#39;index incrémentiel par script pour un site Web actif {#task_B3A87AC4AC784507859C23B9062BA11C}

Vous pouvez programmer l’indexation incrémentielle par script à intervalles réguliers tout au long de la journée.

L’heure de base sélectionnée est locale en fonction du fuseau horaire configuré dans les Paramètres du compte.

Voir [Configuration des paramètres de votre compte](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Les serveurs Web sont souvent programmés pour une maintenance en pleine nuit. Si votre serveur est hors service pendant une heure d&#39;indexation planifiée, le processus d&#39;indexation échoue. Veillez à sélectionner l’heure de la journée à laquelle votre serveur Web est disponible.

Le calendrier de l&#39;index ne s&#39;applique qu&#39;à votre index de production ; vous ne pouvez pas planifier des index incrémentiels intermédiaires.

**Pour définir la planification de l’index incrémentiel par script pour un site Web actif**

1. Dans le menu produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Schedule]**.
1. Sur la page **[!UICONTROL Scripted Incremental Index Schedule]**, dans la liste déroulante **[!UICONTROL Read the Scripted Incrementally Indexing File]**, sélectionnez la fréquence d’exécution du fichier texte d’index incrémentiel par script, en heures ou en minutes.
1. Dans la liste déroulante **[!UICONTROL Base Time]**, sélectionnez l’heure de début à laquelle vous souhaitez régénérer un nouvel index incrémentiel par script.
1. Cliquez sur **[!UICONTROL Save Changes]**.

## Exécution d’un index incrémentiel par script d’un site Web en direct ou par étape {#task_6E6FC76EE1E84A5FADB3B67AD7B1DACB}

Vous pouvez utiliser l’index incrémentiel par script pour indexer des &quot;morceaux&quot; de votre site Web en direct ou d’évaluation, par exemple un ensemble de pages fréquemment modifiées, sans avoir à vous connecter.

Pour utiliser cette fonctionnalité, veillez à configurer un fichier texte d’index incrémentiel par script.

Voir [Configuration d’un index incrémentiel par script](../c-about-index-menu/c-about-scripted-index.md#task_05AE040FE75E40FFAA5E10B6B6D4D255).

**Pour exécuter un index incrémentiel par script d’un site Web en direct ou par étape**

1. Dans le menu produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Index]**.
   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Index]**.

1. Cliquez sur **[!UICONTROL Scripted Index Now]**.
1. (Facultatif) Si des erreurs d’indexation se sont produites, cliquez sur **[!UICONTROL View Errors]** pour vue du journal associé.

## Affichage du journal d&#39;index incrémentiel par script d&#39;un site Web en direct ou d&#39;un site Web intermédiaire {#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7}

Lorsqu’un index par script complet en direct ou un index par script complet par étape est terminé, vous pouvez vue son journal associé pour résoudre les erreurs qui se sont produites.

Vous ne pouvez pas exporter de journaux ni les enregistrer. Cependant, le journal reste disponible pour affichage jusqu’à ce que le nouvel index se produise.

**Pour vue du journal d&#39;index incrémentiel d&#39;un site Web dynamique ou d&#39;un site Web intermédiaire**

1. Dans le menu produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Live Log]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Scripted Index]** > **[!UICONTROL Staged Log]**.

1. Dans la page de journal, en haut ou en bas, effectuez l’une des opérations suivantes :

   * Utilisez les options de navigation **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** pour parcourir le journal.

   * Utilisez les options d&#39;affichage **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** pour affiner ce que vous voyez.

