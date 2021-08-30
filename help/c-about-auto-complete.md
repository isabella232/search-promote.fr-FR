---
description: Vous pouvez configurer différentes zones de la saisie semi-automatique pour contrôler la génération du formulaire de recherche activé à saisie automatique et du fichier autocomplete_data.js, qui fait partie du formulaire de recherche activé à saisie automatique.
solution: Target
subtopic: Auto-Complete
title: À propos de la saisie automatique
topic-legacy: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
exl-id: a1d08c0a-6c68-4da2-88d2-fe953d333536
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '1486'
ht-degree: 1%

---

# À propos de la saisie automatique{#about-auto-complete}

Vous pouvez configurer différentes zones de la saisie semi-automatique pour contrôler la génération du formulaire de recherche activé à saisie automatique et du fichier autocomplete_data.js, qui fait partie du formulaire de recherche activé à saisie automatique.

## À propos de la saisie automatique {#concept_093A9CD754864BA79B456FE4BEB64578}

Le fichier [!DNL autocomplete_data.js] est régénéré et publié sur le réseau de contenu de recherche chaque fois que des modifications ont été enregistrées sur la page Configuration de la saisie semi-automatique .

## Configuration du remplissage automatique {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

Vous pouvez configurer et configurer les options qui contrôlent la génération du formulaire de recherche activé à saisie automatique et du fichier.

<!-- 

t_configuring_auto-complete.xml

 -->

Une fois que vous avez configuré la saisie semi-automatique, vous pouvez afficher la source HTML obtenue pour révision. La source HTML est ce que vous copiez et collez dans les pages de votre site web.

Voir [Aperçu du formulaire de recherche tel qu’il apparaîtra sur votre...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Voir [Configuration de la liste de mots à remplissage automatique](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

Voir [Configuration de la saisie semi-automatique CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Pour configurer la saisie semi-automatique**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. Sur la page [!DNL Auto-Complete Setup], définissez les options de votre choix.

   Voir aussi [Prévisualiser le formulaire de recherche tel qu’il apparaîtra sur votre...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Suggestions maximales </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal d’éléments à afficher dans la liste de suggestions à saisie automatique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caractères d’entrée minimaux </p> </td> 
      <td colname="col2"> <p>Indique le nombre de caractères qu’un client doit entrer dans le formulaire de recherche à saisie automatique avant d’afficher les suggestions. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Entrées de cache maximales </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal de suggestions de saisie semi-automatique précédemment demandées à mettre en cache dans le navigateur du client. En règle générale, vous devez conserver ce paramètre à la valeur par défaut de 1 000. </p> <p>Bien que vous puissiez désactiver complètement la mise en cache du navigateur en définissant cette option sur 0, elle n’est pas recommandée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du formulaire </p> </td> 
      <td colname="col2"> <p>Indique l’attribut "name" de la balise "form" du formulaire de recherche activé à saisie automatique. Par exemple : </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>où <span class="filepath"> SiteSearch </span> est l’attribut name de la balise de formulaire. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Identifiant de balise Div </p> </td> 
      <td colname="col2"> <p>Indique l’attribut ID de la balise "div" du formulaire de recherche activé à saisie automatique. Par exemple : </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>où <span class="filepath"> autocomplete </span> est l’attribut de la balise div. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Identifiant de balise d’entrée </p> </td> 
      <td colname="col2"> <p>Indique l’attribut d’identifiant de la balise "input" du formulaire de recherche activée à saisie automatique. Par exemple : </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>où <span class="filepath"> q </span> est l’attribut id de la balise d’entrée. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Afficher l’ombre </p> </td>
      <td colname="col2"> <p>Ajoute une ombre portée cosmétique à la liste de suggestions à saisie automatique. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Correspondance uniquement au début de l’expression </p> </td>
      <td colname="col2"> <p>Ne suggèrent que des résultats correspondant au début du texte de saisie . </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Prise en charge du jeu de caractères UTF-8 </p> </td>
      <td colname="col2"> <p>Gérez correctement les caractères non ASCII en termes de termes. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** si vous souhaitez annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuration de la liste de mots à remplissage automatique {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Configurez la liste des mots et expressions que le remplissage automatique offre à un client sous la forme de suggestions.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Voir [Configuration de la saisie semi-automatique](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Voir [Configuration de la saisie semi-automatique CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

**Pour configurer la liste de mots à remplissage automatique**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. Sur la page [!DNL Auto-Complete Word List], définissez les options de votre choix.

   Voir [Aperçu du formulaire de recherche tel qu’il apparaîtra sur votre...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Période des recherches les plus consultées </p> </td> 
      <td colname="col2"> <p> Contrôle la période d’inclusion de mots et d’expressions lors des recherches récentes d’un client. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Nombre de recherches maximal </p> </td> 
      <td colname="col2"> <p>Contrôle le nombre maximal de mots et d’expressions recherchés à inclure dans la liste de mots à saisie automatique. Les mots et expressions principaux, qui sont également les plus populaires, sont inclus. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du champ </p> </td> 
      <td colname="col2"> <p>Chaque nom de champ définit le nom d’un champ pour lequel inclure des valeurs indexées. Utilisez + et - pour ajouter ou supprimer des noms de champ. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre de valeurs maximal </p> </td> 
      <td colname="col2"> <p>Définit le nombre maximal de valeurs de champ autorisées pour le nom de champ sélectionné. Les valeurs principales, qui sont également les plus référencées, sont incluses. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajouter ces mots et expressions </p> </td> 
      <td colname="col2"> <p> La liste de mots à saisie automatique est renseignée avec les mots et expressions répertoriés dans cette zone. </p> <p> Cliquez sur <span class="uicontrol"> Modifier </span> pour afficher la liste ou ajouter des mots et des expressions à la liste. Lorsque vous avez terminé, cliquez sur <span class="uicontrol"> Enregistrer les modifications </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer ces mots et expressions </p> </td> 
      <td colname="col2"> <p> Les entrées de cette zone ne s’affichent pas dans la liste de mots à saisie automatique. </p> <p> Cliquez sur <span class="uicontrol"> Modifier </span> pour afficher la liste ou ajouter des mots et des expressions à la liste. Lorsque vous avez terminé, cliquez sur <span class="uicontrol"> Enregistrer les modifications </span>. </p> <p> Les expressions régulières sont autorisées dans cette liste. Pour spécifier une expression régulière dans cette liste, commencez la ligne par <code>regexp</code> suivie d’un espace unique, suivi de l’expression régulière. Toutes les lignes de la liste de mots qui correspondent à l’expression régulière sont supprimées. </p> <p> <b>Important</b> : Vous ne devez utiliser des expressions régulières que si vous avez déjà travaillé avec elles dans d’autres applications. </p> <p>Voir <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorer la casse </p> </td> 
      <td colname="col2"> <p>Les entrées en double dans la liste de mots à saisie automatique qui ne diffèrent que par les majuscules/minuscules alphabétiques sont supprimées ; toutes les entrées de liste de mots sont forcées à être en minuscules. </p> <p>Si vous souhaitez que les suggestions de saisie automatique apparaissent en "majuscule de première lettre" ou "majuscules", ajoutez la variable 
        <code>
          text-transform : capitalize; 
        </code> ou 
        <code>
          text-transform : uppercase; 
        </code> Propriétés de texte CSS au contenu CSS à remplissage automatique, sous "/* styles pour l’élément de résultat */". </p> <p>Voir <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> Configuration de la saisie semi-automatique CSS </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mise à jour lors de la réindexation </p> </td> 
      <td colname="col2"> <p>La liste de mots à saisie automatique est automatiquement régénérée après chaque réindexation de compte réussie. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** si vous souhaitez annuler les modifications que vous avez apportées.
   * Cliquez sur **[!UICONTROL Preview Word List]** pour enregistrer les modifications que vous avez apportées, puis ouvrez la page [!DNL Auto-Complete Word List Preview] où vous pouvez consulter la liste de suggestions à saisie automatique. Utilisez les options de navigation situées en haut de la page pour passer en revue et affiner la liste affichée. Une fois que vous avez terminé, cliquez sur **[!UICONTROL Close]** pour revenir à la page [!DNL Auto-Complete Word List].

      Voir [Utilisation de l’option Historique](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuration du remplissage automatique de CSS {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Utilisez la saisie CSS à saisie automatique pour configurer la feuille de style en cascade à saisie automatique que vous souhaitez utiliser.

<!-- 

t_configuring_auto-complete_css.xml

 -->

La saisie CSS automatique contrôle le contenu de [!DNL autocomplete_styles.css], qui est inclus dans le formulaire de recherche activée à saisie automatique. Le code CSS que vous spécifiez ici contrôle la présentation visuelle de la liste de suggestions à saisie automatique. Pour obtenir un exemple des idées de présentation visuelle possibles, reportez-vous aux sections suivantes :

<!-- 404 DEAD LINK [https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html). -->

[Configuration de la liste de mots à remplissage automatique](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4).

[Configuration de la saisie automatique](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Lorsque vous avez terminé de configurer le remplissage automatique d’une feuille CSS, vous pouvez prévisualiser le formulaire de recherche pour vérifier si le CSS que vous avez spécifié est acceptable en apparence et en mise en page.

Voir [Aperçu du formulaire de recherche tel qu’il apparaîtra sur votre...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Important** : Pour appliquer votre CSS de saisie automatique personnalisé, vous devez supprimer les balises de commentaire de la deuxième ligne qui apparaît dans le code HTML. Vous déplacez ensuite la même ligne vers dans la section head de la page qui contient le formulaire de recherche.

Voir [Copie du code HTML du formulaire de recherche dans le...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Pour configurer le remplissage automatique d’une feuille CSS**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. Dans le champ de texte [!DNL Auto-Complete CSS], collez ou saisissez les informations de feuille de style en cascade que vous souhaitez associer à la liste de suggestions à saisie automatique.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Prévisualiser le formulaire de recherche tel qu’il apparaîtrait sur votre site web {#task_437B35EFA5424603A08AF8E79E6B4714}

Selon votre configuration de saisie semi-automatique et de saisie semi-automatique, vous pouvez prévisualiser l’affichage du formulaire de recherche si vous souhaitez ajouter le code HTML à votre site web.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Voir [Configuration de la saisie semi-automatique](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Voir [Configuration de la saisie semi-automatique CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Voir [Copie du code HTML du formulaire de recherche dans le...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Voir [Utilisation de collections dans les formulaires de recherche](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Voir [Utilisation d’images avec des formulaires](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Voir [Exemple de formulaire de recherche avancée](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Voir [Code HTML du formulaire de recherche avancée](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Voir [Code de modèle de formulaire de recherche avancée](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**Pour prévisualiser le formulaire de recherche tel qu’il apparaîtra sur votre site web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Facultatif) Cliquez sur **[!UICONTROL HTML code]** pour afficher le code HTML que vous copiez et collez dans les pages de votre site Web.

## Copie du code HTML du formulaire de recherche dans les pages de votre site web {#task_A3A01EA800F24C0AA33902387E0362C7}

Selon votre configuration de saisie semi-automatique et de saisie semi-automatique, vous pouvez prévisualiser l’affichage du formulaire de recherche si vous souhaitez ajouter le code HTML à votre site web.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Voir [Configuration de la saisie semi-automatique](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Voir [Configuration de la saisie semi-automatique CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96).

Voir [Copie du code HTML du formulaire de recherche dans le...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Voir [Utilisation de collections dans les formulaires de recherche](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3).

Voir [Utilisation d’images avec des formulaires](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Voir [Exemple de formulaire de recherche avancée](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A).

Voir [Code HTML du formulaire de recherche avancée](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9).

Voir [Code de modèle de formulaire de recherche avancée](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579).

**Pour copier le code HTML du formulaire de recherche dans les pages de votre site web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >Ne modifiez pas la valeur `form name=` dans la source du formulaire.

1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Si vous avez configuré la saisie CSS automatique et que vous souhaitez que les styles soient appliqués au formulaire de recherche, supprimez les balises de commentaire de la deuxième ligne qui apparaît dans le code HTML. Déplacez ensuite la même ligne vers dans la section head de la page qui contient le formulaire de recherche.
   * Pour optimiser les performances, déplacez les balises répertoriées au bas du code HTML et placez-les au bas de la section de corps de chaque page qui contient le formulaire de recherche.

1. Copiez le code et collez-le dans les pages web de votre site web où vous souhaitez que le formulaire de recherche apparaisse.
