---
description: Vous pouvez configurer différentes zones de saisie semi-automatique pour contrôler la génération du formulaire de recherche automatique activé et du fichier autocomplete_data.js, inclus dans le formulaire de recherche automatique activé.
seo-description: Vous pouvez configurer différentes zones de saisie semi-automatique pour contrôler la génération du formulaire de recherche automatique activé et du fichier autocomplete_data.js, inclus dans le formulaire de recherche automatique activé.
seo-title: A propos du remplissage automatique
solution: Target
subtopic: Auto-Complete
title: A propos du remplissage automatique
topic: Design,Site search and merchandising
uuid: 3dfdd14d-2044-4f01-a5bc-fcb2eb0d5068
translation-type: tm+mt
source-git-commit: 439100ab96f4b597c55b1c1ae38a5778c208e896

---


# A propos du remplissage automatique{#about-auto-complete}

Vous pouvez configurer différentes zones de saisie semi-automatique pour contrôler la génération du formulaire de recherche automatique activé et du fichier autocomplete_data.js, inclus dans le formulaire de recherche automatique activé.

## A propos du remplissage automatique {#concept_093A9CD754864BA79B456FE4BEB64578}

Le fichier [!DNL autocomplete_data.js] est régénéré et publié sur le réseau de contenu de recherche chaque fois que des modifications ont été enregistrées dans la page de configuration de saisie semi-automatique.

## Configuration du remplissage automatique {#task_F491F2BFC4D24A61BBDC48B9059C11BB}

Vous pouvez configurer et configurer les options qui contrôlent la génération du formulaire de recherche à saisie semi-automatique activé et du fichier.

<!-- 

t_configuring_auto-complete.xml

 -->

Après avoir configuré la saisie semi-automatique, vous pouvez afficher la source HTML résultante pour révision. La source HTML est ce que vous copiez et collez dans les pages de votre site Web.

Voir [Aperçu du formulaire de recherche tel qu’il apparaîtra sur votre...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

Voir [Configuration de la liste](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)de mots à remplissage automatique.

Voir [Configuration d’une page CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)à remplissage automatique.

**Pour configurer le remplissage automatique**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Setup]**.
1. Sur la [!DNL Auto-Complete Setup] page, définissez les options de votre choix.

   Voir aussi [Prévisualisation du formulaire de recherche tel qu’il apparaîtra sur votre...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nombre maximum de suggestions </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal d’éléments à afficher dans la liste de suggestions à saisie semi-automatique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Caractères d’entrée minimaux </p> </td> 
      <td colname="col2"> <p>Indique le nombre de caractères qu’un client doit saisir dans le formulaire de recherche à saisie automatique avant d’afficher les suggestions. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre maximal d’entrées de cache </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal de suggestions de saisie semi-automatique précédemment demandées à mettre en cache dans le navigateur du client. En règle générale, vous devez conserver ce paramètre à la valeur par défaut de 1 000. </p> <p>Bien que vous puissiez désactiver complètement la mise en cache du navigateur en définissant cette option sur 0, elle n’est pas recommandée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du formulaire </p> </td> 
      <td colname="col2"> <p>Spécifie l’attribut "name" de la balise "form" du formulaire de recherche activée à saisie automatique. Par exemple : </p> <p> <span class="filepath"> &lt;form name="SiteSearch" method="get" action="https://sp1004337c.guided.t1.atomz.com" target="_blank"&gt; </span> </p> <p>où <span class="filepath"> SiteSearch </span> est l’attribut name de la balise de formulaire. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID de balise Div </p> </td> 
      <td colname="col2"> <p>Spécifie l’attribut ID de la balise "div" du formulaire de recherche activée à saisie automatique. Par exemple : </p> <p> <span class="filepath"> &lt;div id="autocomplete"&gt; </span> </p> <p>où <span class="filepath"> autocomplete </span> est l’attribut de la balise div. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>ID de balise d’entrée </p> </td> 
      <td colname="col2"> <p>Spécifie l’attribut ID de la balise "input" du formulaire de recherche activée à saisie automatique. Par exemple : </p> <p> <span class="filepath"> &lt;input type="text" id="q" name="q" /&gt; </span> </p> <p>où <span class="filepath"> q </span> est l’attribut id de la balise input. </p> </td> 
      </tr> 
      <tr>
      <td colname="col1"> <p>Ombre affichée </p> </td>
      <td colname="col2"> <p>Ajoute une ombre portée cosmétique à la liste de suggestions à saisie automatique. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Correspondance uniquement au début de l’expression </p> </td>
      <td colname="col2"> <p>N’indiquez que les résultats qui correspondent au début du texte d’entrée. </p> </td>
      </tr>
      <tr>
      <td colname="col1"> <p>Prise en charge du jeu de caractères UTF-8 </p> </td>
      <td colname="col2"> <p>Traitez correctement les caractères non ASCII en termes. </p> </td>
      </tr>
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuration de la liste de mots à remplissage automatique {#task_1F8E0F346263443383F8CFD2C7AB35D4}

Configurez la liste des mots et des expressions que le remplissage automatique affiche pour un client sous forme de suggestions.

<!-- 

t_configuring_auto-complete_word_list.xml

 -->

Voir [Configuration du remplissage](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)automatique.

Voir [Configuration d’une page CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)à remplissage automatique.

**Pour configurer la liste de mots à remplissage automatique**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete Word List]**.
1. Sur la [!DNL Auto-Complete Word List] page, définissez les options de votre choix.

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
      <td colname="col1"> <p>Période des recherches populaires </p> </td> 
      <td colname="col2"> <p> Contrôle la période d’inclusion de mots et d’expressions issus des recherches récentes d’un client. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Nombre maximal de recherches </p> </td> 
      <td colname="col2"> <p>Contrôle le nombre maximal de mots et d’expressions recherchés à inclure dans la liste de mots à saisie automatique. Les mots et expressions les plus utilisés sont inclus. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du champ </p> </td> 
      <td colname="col2"> <p>Chaque nom de champ définit le nom d’un champ pour lequel inclure des valeurs indexées. Utilisez + et - pour ajouter ou supprimer des noms de champ. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nombre maximal de valeurs </p> </td> 
      <td colname="col2"> <p>Définit le nombre maximal de valeurs de champ autorisées pour le nom de champ sélectionné. Les valeurs supérieures, qui sont également les plus référencées, sont incluses. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajouter ces mots et expressions </p> </td> 
      <td colname="col2"> <p> La liste de mots à saisie automatique est renseignée par les mots et les expressions répertoriés dans cette zone. </p> <p> Cliquez sur <span class="uicontrol"> Modifier </span> pour afficher la liste ou ajouter des mots et des expressions à la liste. Lorsque vous avez terminé, cliquez sur <span class="uicontrol"> Enregistrer les modifications </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Supprimer ces mots et expressions </p> </td> 
      <td colname="col2"> <p> Les entrées de cette zone ne s’affichent pas dans la liste de mots à saisie automatique. </p> <p> Cliquez sur <span class="uicontrol"> Modifier </span> pour afficher la liste ou ajouter des mots et des expressions à la liste. Lorsque vous avez terminé, cliquez sur <span class="uicontrol"> Enregistrer les modifications </span>. </p> <p> Les expressions régulières sont autorisées dans cette liste. Pour spécifier une expression régulière dans cette liste, commencez la ligne par 
        <userinput>
          regexp 
        </userinput> suivi d’un espace unique, suivi de l’expression régulière. Toutes les lignes de la liste de mots qui correspondent à l’expression régulière sont supprimées. </p> <p> <b>Important</b>: Vous ne devez utiliser les expressions régulières que si vous avez déjà travaillé avec elles dans d’autres applications. </p> <p>Voir <a href="c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ignorer la casse </p> </td> 
      <td colname="col2"> <p>Les entrées en double dans la liste de mots à saisie automatique qui ne diffèrent que par la majuscule/minuscule alphabétique sont supprimées; toutes les entrées de la liste de mots sont forcées à la minuscule. </p> <p>Si vous souhaitez que les suggestions de saisie semi-automatique apparaissent sous la forme "majuscule de la première lettre" ou "majuscules", ajoutez la variable 
        <userinput>
          text-transform : capitaliser; 
        </userinput> ou 
        <userinput>
          text-transform : majuscule; 
        </userinput> Propriétés de texte CSS au contenu CSS à remplissage automatique, sous "/* styles pour l’élément de résultat */". </p> <p>Voir <a href="c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96" type="task" format="dita" scope="local"> Configuration du remplissage automatique des feuilles de style CSS </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Mise à jour lors du ré-index </p> </td> 
      <td colname="col2"> <p>La liste de mots à saisie automatique est automatiquement régénérée après chaque réindexation réussie du compte. </p> </td> 
      </tr> 
    </tbody> 
   </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.
   * Cliquez sur **[!UICONTROL Preview Word List]** pour enregistrer les modifications que vous avez apportées, puis ouvrez [!DNL Auto-Complete Word List Preview] la page dans laquelle vous pouvez consulter la liste des suggestions de saisie semi-automatique. Utilisez les options de navigation en haut de la page pour revoir et affiner la liste affichée. Lorsque vous avez terminé, cliquez **[!UICONTROL Close]** pour revenir à la [!DNL Auto-Complete Word List] page.

      Voir [Utilisation de l’option](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Configuration du remplissage automatique des feuilles de style CSS {#task_EECE35DEB6C94F4A8A5B42B4DED76D96}

Utilisez le format CSS de saisie semi-automatique pour configurer la feuille de style en cascade de saisie semi-automatique que vous souhaitez utiliser.

<!-- 

t_configuring_auto-complete_css.xml

 -->

Le remplissage automatique du fichier CSS contrôle le contenu de [!DNL autocomplete_styles.css], qui est inclus dans le formulaire de recherche activé à saisie automatique. La page CSS que vous spécifiez ici contrôle la présentation visuelle de la liste de suggestions de saisie semi-automatique. Pour obtenir un exemple des idées de présentation visuelle possibles, reportez-vous aux sections suivantes :

[https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html](https://developer.yahoo.com/yui/examples/autocomplete/ac_skinning.html).

[Configuration de la liste](c-about-auto-complete.md#task_1F8E0F346263443383F8CFD2C7AB35D4)de mots à remplissage automatique.

[Configuration de la saisie semi-automatique](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB).

Lorsque vous avez terminé de configurer le remplissage automatique du fichier CSS, vous pouvez prévisualiser le formulaire de recherche pour vérifier si le fichier CSS que vous avez spécifié est acceptable en termes d’apparence et de disposition.

Voir [Aperçu du formulaire de recherche tel qu’il apparaîtra sur votre...](c-about-auto-complete.md#task_437B35EFA5424603A08AF8E79E6B4714).

**Important**: Pour appliquer votre page CSS de saisie semi-automatique personnalisée, vous devez supprimer les balises de commentaire de la deuxième ligne qui apparaît dans le code HTML. Ensuite, vous déplacez la même ligne dans la section head de la page qui contient le formulaire de recherche.

Voir [Copie du code HTML du formulaire de recherche dans le...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

**Pour configurer le remplissage automatique des feuilles de style CSS**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Auto-Complete CSS]**.
1. Dans le champ de [!DNL Auto-Complete CSS] texte, collez ou saisissez les informations de feuille de style en cascade que vous souhaitez associer à la liste de suggestions de saisie semi-automatique.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Aperçu du formulaire de recherche tel qu’il apparaîtra sur votre site Web {#task_437B35EFA5424603A08AF8E79E6B4714}

Selon votre configuration de saisie semi-automatique et de saisie semi-automatique, vous pouvez prévisualiser l’aspect du formulaire de recherche si vous souhaitez ajouter le code HTML à votre site Web.

<!-- 

t_previewing_the_search_form_as_it_would_appear_on_your_website.xml

 -->

Voir [Configuration du remplissage](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)automatique.

Voir [Configuration d’une page CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)à remplissage automatique.

Voir [Copie du code HTML du formulaire de recherche dans le...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Voir [Utilisation des collections dans les formulaires](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de recherche.

Voir [Utilisation de cadres avec des formulaires](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Voir [Exemple de formulaire](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de recherche avancée.

Voir Code [HTML de formulaire de recherche](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)avancée.

Voir Code [de modèle de formulaire de recherche](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)avancée.

**Pour prévisualiser le formulaire de recherche tel qu’il apparaîtra sur votre site Web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Search Form]**.
1. (Facultatif) Cliquez sur **[!UICONTROL HTML code]** pour afficher le code HTML que vous copiez et collez dans les pages de votre site Web.

## Copie du code HTML du formulaire de recherche dans les pages de votre site Web {#task_A3A01EA800F24C0AA33902387E0362C7}

Selon votre configuration de saisie semi-automatique et de saisie semi-automatique, vous pouvez prévisualiser l’aspect du formulaire de recherche si vous souhaitez ajouter le code HTML à votre site Web.

<!-- 

t_copying_the_html_code_of_the_search_form_into_the_pages_of_your_website.xml

 -->

Voir [Configuration du remplissage](c-about-auto-complete.md#task_F491F2BFC4D24A61BBDC48B9059C11BB)automatique.

Voir [Configuration d’une page CSS](c-about-auto-complete.md#task_EECE35DEB6C94F4A8A5B42B4DED76D96)à remplissage automatique.

Voir [Copie du code HTML du formulaire de recherche dans le...](c-about-auto-complete.md#task_A3A01EA800F24C0AA33902387E0362C7).

Voir [Utilisation des collections dans les formulaires](c-appendices/c-searchforms.md#reference_5A079AEEEFB84457892EF0870D0605C3)de recherche.

Voir [Utilisation de cadres avec des formulaires](c-appendices/c-searchforms.md#reference_82CDDDA1E37042E4849EBF7EA05407C5).

Voir [Exemple de formulaire](c-appendices/c-searchforms.md#reference_82E1051918744EBA88A01E9E6AE42C4A)de recherche avancée.

Voir Code [HTML de formulaire de recherche](c-appendices/c-searchforms.md#reference_9AAD4A46B68D4D48865508982CB86DB9)avancée.

Voir Code [de modèle de formulaire de recherche](c-appendices/c-searchforms.md#reference_D762C22E754E462DBEECD88D2C3FA579)avancée.

**Copie du code HTML du formulaire de recherche dans les pages de votre site Web**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Auto-Complete]** > **[!UICONTROL Form Source]**.

   >[!NOTE]
   >
   >Ne modifiez pas la `form name=` valeur dans la source du formulaire.

1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Si vous avez configuré la saisie semi-automatique du code CSS et souhaitez que les styles soient appliqués au formulaire de recherche, supprimez les balises de commentaire de la deuxième ligne qui apparaît dans le code HTML. Ensuite, déplacez la même ligne dans la section head de la page qui contient le formulaire de recherche.
   * Pour des performances optimales, déplacez les balises répertoriées au bas du code HTML et placez-les au bas de la section body de chaque page qui contient le formulaire de recherche.

1. Copiez le code et collez-le dans les pages Web de votre site Web où vous souhaitez que le formulaire de recherche apparaisse.
