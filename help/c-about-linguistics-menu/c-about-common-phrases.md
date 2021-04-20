---
description: Vous pouvez définir des expressions courantes utilisées sur votre site Web de sorte que lorsqu’un client entre dans une requête de recherche, il n’est pas nécessaire de saisir des guillemets autour des expressions que vous avez définies.
solution: Target
title: A propos des expressions courantes
topic: Linguistics,Site search and merchandising
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '1183'
ht-degree: 1%

---


# A propos des expressions courantes{#about-common-phrases}

Vous pouvez définir des expressions courantes utilisées sur votre site Web de sorte que lorsqu’un client entre dans une requête de recherche, il n’est pas nécessaire de saisir des guillemets autour des expressions que vous avez définies.

## Utilisation des expressions courantes {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>La fonction Expression commune n’apparaît pas dans l’interface utilisateur, car elle n’est pas activée par défaut. Contactez l’assistance technique pour activer cette fonction.

Les expressions courantes sont un ensemble d’expressions de plusieurs mots qui sont reconnues lors de la recherche d’un client. Il traite les expressions comme un groupe combiné de mots plutôt que comme des mots individuels. Lorsqu’un client entre dans une requête de recherche sur votre site Web, il peut identifier des expressions en les entourant de citations à doublon, telles que &quot;Océan Pacifique&quot;. Cependant, lorsque vous ajoutez des groupes d’expressions courantes, les étapes de citation sont exécutées automatiquement pour le client, car elles détectent les expressions correspondantes dans la requête de recherche.

Supposons, par exemple, qu’un client de votre site Web entre dans la requête de recherche suivante :

`hotels near the pacific ocean`

Sans l&#39;ajout de guillemets autour de `pacific ocean`, la recherche du client retourne les résultats pour les hôtels situés à proximité de n&#39;importe quel océan dans le monde, ce qui n&#39;est pas ce que le client voulait.

Cependant, lorsque vous ajoutez l’expression commune &quot;océan Pacifique&quot;, leur requête de recherche est automatiquement convertie en ce qui suit :

`hotels near the "pacific ocean"`

L’utilisation des expressions courantes n’empêche pas vos clients d’utiliser explicitement des guillemets autour d’expressions de mots. Au lieu de cela, il ajoute simplement des guillemets lorsque ces expressions définies se trouvent dans leur requête de recherche.

Cette extension de requête de recherche s&#39;applique aux paramètres CGI de recherche principale `sp_q` et `sp_q_#`,

Voir les lignes 25, 26 et 32 du tableau dans [Paramètres CGI de recherche principale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

## Ajouter un groupe d&#39;expressions commun {#task_35C84FABCD9042C5B48C5C788B752871}

Vous pouvez ajouter des groupes d’expressions communs pour vous assurer que les requêtes de recherche renvoient avec précision des pages Web contenant tous les mots, dans l’ordre exact et à proximité, saisis par un client.

À mesure que vous ajoutez des groupes d’expressions communs, vous pouvez utiliser la fonction Rechercher sur la page principale Groupe d’expressions communes. La fonction Rechercher permet de rechercher une expression existante et de déterminer dans quel groupe elle réside.

Voir [Recherche de groupes contenant des mots particuliers dans une phrase ](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E).

**Pour ajouter un groupe Expressions courantes**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la page [!DNL Common Phrases Groups], cliquez sur **Ajouter le groupe d&#39;expressions**.
1. Sur la page [!DNL Add Common Phrase Group], définissez les options de votre choix et ajoutez toutes les expressions qui composent le groupe.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom de groupe </p> </td> 
      <td colname="col2"> <p>Requis. </p> <p>Nom unique du groupe d’expressions communes. </p> <p>Si vous modifiez ultérieurement un groupe d’expressions communes, notez que vous ne pouvez pas modifier le nom du groupe. Pour modifier le nom du groupe, utilisez la fonction <span class="uicontrol"> Renommer</span>. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> Changement du nom d'un groupe d'expressions commun</a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remarques </p> </td> 
      <td colname="col2"> <p>Facultatif. </p> <p>Ajoutez les informations relatives au groupe d’expressions communes. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Phrases </p> </td> 
      <td colname="col2"> <p>Requis. </p> <p>Vous permet de spécifier une expression jusqu’à cinq mots. Pour modifier le nombre maximal de mots, contactez le support technique. </p> <p>Chaque expression saisie doit être unique dans tout groupe de expressions commun. </p> <p>Utilisez les icônes plus (+) et moins (-) de la colonne Action pour ajouter l'expression saisie ou pour supprimer une expression. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **Ajouter**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Test d&#39;une expression commune {#task_A0C344E051CA45A9A0588242F9DA675D}

Si vous avez sélectionné des champs de métadonnées à associer à un groupe d’expressions, vous pouvez tester l’extension d’une expression particulière.

Lorsque vous testez l’extension d’une expression, vous recherchez une expression exacte par rapport aux champs de métadonnées que vous avez associés au groupe d’expressions. L’expression est recherchée comme si elle était entourée de guillemets. Tous les autres champs de métadonnées recherchent uniquement les mots de l’expression, sans guillemets. Supposons, par exemple, que vous ayez testé l’expression `audi TT`. Les résultats renvoyés peuvent s’afficher comme suit :

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**Pour tester une expression courante**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la page [!DNL Common Phrases Groups], dans le champ **Expression de test qui contient** texte, saisissez l’expression dont vous souhaitez tester l’extension de métadonnées.
1. Cliquez sur **[!UICONTROL Test]**.

   Les résultats de l’extension s’affichent dans la zone de texte.
1. (Facultatif) Faites glisser le coin inférieur droit de la zone de texte pour développer la zone d’affichage.

## Recherche de groupes contenant des mots particuliers dans une expression {#task_20714969274740A7BB4DC71E705EA15E}

Vous pouvez utiliser [!DNL Find] pour rechercher des mots spécifiques dans une phrase parmi tous les groupes existants que vous avez ajoutés.

Lorsque vous utilisez Rechercher, il localise les éléments suivants :

* Où se trouve exactement la même phrase parmi tous les groupes.
* Tous les mots de l&#39;expression parmi tous les groupes, indépendamment de l&#39;ordre des mots et de la proximité dans l&#39;expression.

Voir aussi [Modification d&#39;un groupe d&#39;expressions commun](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61).

**Pour rechercher des groupes contenant des mots particuliers dans une phrase**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la page [!DNL Common Phrases Groups], dans le champ de texte **[!UICONTROL Find groups with phrases that contain]**, entrez une expression.
1. Cliquez sur **[!UICONTROL Find]**.

   Les résultats s’affichent dans la zone de texte.
1. (Facultatif) Effectuez une ou plusieurs des opérations suivantes :

   * Faites glisser l’angle inférieur droit de la zone de texte pour développer la zone d’affichage.
   * Dans la fenêtre de résultats, cliquez sur une expression liée pour ouvrir la page Modifier un groupe d&#39;expressions commun du groupe associé.

## Modification d&#39;un groupe d&#39;expressions commun {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

Vous pouvez modifier les champs, notes et expressions existants d’un groupe d’expressions commun que vous avez ajouté. Cependant, pour modifier le nom du groupe, vous devez utiliser la fonction [!DNL Rename].

Voir aussi [Changement du nom d&#39;un groupe d&#39;expressions commun](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB).

**Pour modifier un groupe Expressions courantes**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la page [!DNL Common Phrases Groups], cliquez sur **[!UICONTROL Edit]** à l&#39;extrémité droite du nom d&#39;un groupe.
1. Sur la page [!DNL Edit Common Phrase Group], définissez les options de votre choix.

   Consultez le tableau des options sous [Ajouter un groupe d&#39;expressions commun](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871).
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Changement du nom d&#39;un groupe d&#39;expressions commun {#task_168E07C59C0F40989D43E7010EFF22EB}

Vous pouvez modifier le nom d’un groupe d’expressions communes existant. Cependant, si vous souhaitez modifier les champs, notes et expressions existants d’un groupe d’expressions commun, vous devez utiliser la fonction [!DNL Edit].

Voir [Modification d&#39;un groupe de expressions commun](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61) .

**Pour renommer un groupe Expressions courantes**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la page [!DNL Common Phrases Groups], cliquez sur **[!UICONTROL Rename]** à l&#39;extrémité droite du nom d&#39;un groupe.
1. Sur la page [!DNL Rename Common Phrase Group], dans le champ de texte **[!UICONTROL Group Name]**, saisissez le nouveau nom du groupe.
1. Cliquez sur **Renommer**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d&#39;un groupe d&#39;expressions commun {#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

Vous pouvez supprimer tout groupe d’expressions commun que vous avez ajouté. Si vous supprimez un groupe par erreur, vous pouvez utiliser [!DNL History] pour restaurer le groupe.

Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

**Pour supprimer un groupe Expressions courantes**

1. Dans le menu produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la page [!DNL Common Phrases Groups], cliquez sur **[!UICONTROL Delete]** à l&#39;extrémité droite du nom d&#39;un groupe.
1. Sur la page [!DNL Delete Common Phrase Group], cliquez sur **[!UICONTROL Delete]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

