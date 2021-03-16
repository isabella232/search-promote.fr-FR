---
description: Vous pouvez configurer le champ Voulez-vous dire pour que les clients reçoivent des suggestions de termes de recherche valides lorsqu'ils ont essayé des recherches qui ont échoué. Les suggestions sont formées en recherchant l’orthographe et en saisissant des corrections dans les termes recherchés qui génèrent une recherche valide.
solution: Target
title: A propos de Voulez-vous dire
topic: Linguistique,Recherche sur le site et marchandisage
uuid: c5973541-3d6b-4fc9-bad4-66d4d3559fe8
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '733'
ht-degree: 2%

---


# A propos de Voulez-vous dire{#about-did-you-mean}

Vous pouvez configurer le champ Voulez-vous dire pour que les clients reçoivent des suggestions de termes de recherche valides lorsqu&#39;ils ont essayé des recherches qui ont échoué. Les suggestions sont formées en recherchant l’orthographe et en saisissant des corrections dans les termes recherchés qui génèrent une recherche valide.

## Configuration de la signification {#task_B539D6A0043547EFB1CA19B67E762371}

Vous pouvez personnaliser la façon dont [!DNL site search/merchandising] fait des suggestions de recherche lorsque la requête d&#39;un client ne renvoie aucun résultat de recherche, ou un résultat minimal.

<!-- 

t_configuring_did_you_mean.xml

 -->

**Pour configurer Voulez-vous dire**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Did You Mean]**.
1. Sur la page [!DNL Did You Mean], dans le champ de texte **Supprimer ces mots des suggestions**, saisissez des mots séparés par des espaces ou des lignes pour filtrer les suggestions indésirables.

   Il s’agit de mots figurant dans votre index de recherche qui ne s’affichent pas en tant que termes de recherche alternative recommandés. Vous pouvez exclure tout mot correspondant à un modèle en utilisant des expressions régulières. Sinon, seul le mot exact est supprimé.

1. Définissez les options **Voulez-vous dire** que vous souhaitez.

   <!-- 
   
   r_did_you_mean_options.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Algorithme de suggestion </p> </td> 
      <td colname="col2"> <p>Ajuste le chemin parcouru par le logiciel pour trouver des suggestions. Si un utilisateur commet une erreur d’une lettre, tous les algorithmes proposent les mêmes suggestions. La raison en est qu'il suffit d'une modification pour obtenir une suggestion de travail et que tous les algorithmes trouvent des mots proches de l'original. Mais lorsque les termes de recherche d’origine ne sont pas similaires aux termes existants dans l’index, les algorithmes de suggestion <b>Profond</b> et <b>Mauvais orthographes</b> continuent de rechercher des suggestions possibles. Ce scénario est utile si un client tente de saisir un nom correct difficile à saisir et qu’il recherche les noms. Cependant, si vous souhaitez uniquement que des suggestions similaires apparaissent, vous pouvez choisir l’algorithme <b>Quick</b>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre par défaut de suggestions à afficher </p> </td> 
      <td colname="col2"> <p>Indique le nombre de suggestions de termes Voulez-vous dire (0 à 20) que vous souhaitez afficher lorsque la recherche d’un client ne renvoie aucun résultat. La valeur par défaut est de 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Longueur minimale du mot de suggestion </p> </td> 
      <td colname="col2"> <p>Prunes Voulez-vous dire des termes en spécifiant le nombre minimal de lettres pour un mot suggéré. </p> <p>Par exemple, si vous définissez la valeur sur 4, le logiciel ne suggère pas un mot de 1, 2 ou 3 caractères. Si vous spécifiez la valeur 0, aucun mot court n’est supprimé des suggestions de termes. Si vous spécifiez une valeur élevée, il n’y a généralement aucune suggestion de terme. La valeur par défaut est 3. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fréquence d'index minimale </p> </td> 
      <td colname="col2"> <p> Indique le nombre minimum de fois où un mot doit apparaître dans l’index avant d’être inclus dans le dictionnaire Voulez-vous dire. </p> <p>Vous ne pouvez pas spécifier un nombre négatif dans le champ. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rechercher un terme suggéré si aucun résultat </p> </td> 
      <td colname="col2"> <p>Cherche automatiquement de nouveau le premier terme suggéré lorsqu’une recherche d’un client ne donne aucun résultat et qu’il existe au moins une suggestion de terme Voulez-vous dire. </p> <p>Vous pouvez utiliser les balises suivantes dans votre modèle de présentation pour indiquer que la recherche/marchandisage sur le site recherche automatiquement un autre terme : </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search&nbsp;for&nbsp;&lt;guided-param&nbsp;gsname="q"&nbsp;/&gt;&nbsp;instead&nbsp;of&nbsp;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> <p>Vous pouvez également faire d'autres suggestions ici. </p> <p> <code>&nbsp;&lt;guided-if-suggestion-autosearch&gt;&nbsp;&nbsp;There&nbsp;was&nbsp;0&nbsp;matches&nbsp;for&nbsp;&lt;guided-suggestion-original-query&nbsp;/&gt;&nbsp;&nbsp;&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&lt;guided-param&nbsp;gsname="q"&gt;?&nbsp;Here&nbsp;are&nbsp;the&nbsp;results&nbsp;for&nbsp;that&nbsp;search.&nbsp;&nbsp;&nbsp;Or&nbsp;Did&nbsp;You&nbsp;Mean&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestions&gt;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-autosearch&gt;</code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Faire des suggestions en raison de résultats médiocres </p> </td> 
      <td colname="col2"> <p>Si un client recherche un terme qui donne moins de dix résultats, le moteur de recherche vérifie s’il a une suggestion qui peut générer plus de 100 résultats. Si tel est le cas, vous pouvez utiliser les balises suivantes pour indiquer à l’utilisateur que, même s’ils ont des résultats, ils ont peut-être voulu rechercher autre chose : </p> <p> <code>&nbsp;&lt;guided-if-suggestion-low-results&gt; &nbsp;&nbsp;You&nbsp;have&nbsp;a&nbsp;low&nbsp;result&nbsp;count&nbsp;for&nbsp;&lt;Search&nbsp;for&nbsp;guided-param&nbsp;gsname="q"&gt;.&nbsp;&nbsp;Did&nbsp;you&nbsp;mean:&nbsp;&lt;guided-suggestion&gt;&lt;guided-suggestion-link&gt;&lt;guided-suggestion&nbsp;/&gt;&lt;/guided-suggestion-link&gt;&lt;guided-if-not-last&gt;,&nbsp;&lt;/guided-if-not-last&gt;&lt;/guided-suggestions&gt;&nbsp;&lt;/guided-if-suggestion-low-results&gt;</code> </p> <p> Dans le scénario ci-dessus, le nombre de suggestions est contrôlé par la valeur spécifiée dans <span class="uicontrol"> Nombre par défaut de suggestions à afficher </span>. Les seuils inférieur et supérieur peuvent être configurés selon les options ci-dessous. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Faire des suggestions lorsque les résultats initiaux sont inférieurs à </p> </td> 
      <td colname="col2"> <p>Contrôle le nombre de résultats lorsque le système début à des suggestions d’offre. </p> <p>Cette option apparaît uniquement lorsque vous cochez <span class="uicontrol"> Faire des suggestions en raison de résultats faibles</span>. </p> <p>La valeur par défaut est de 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Une suggestion doit générer au moins autant de résultats </p> </td> 
      <td colname="col2"> <p>Filtres des suggestions qui sont faites en raison de résultats faibles dans la recherche Principale par leur nombre de résultats. </p> <p>Cette option apparaît uniquement lorsque vous cochez <span class="uicontrol"> Faire des suggestions en raison de résultats faibles</span>. </p> <p>La valeur par défaut est de 100. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

