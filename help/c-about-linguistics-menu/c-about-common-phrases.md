---
description: Vous pouvez définir des expressions courantes utilisées sur votre site Web de sorte que lorsqu’un client entre dans une requête de recherche, il n’est pas nécessaire qu’il entre des guillemets autour des expressions que vous avez définies.
seo-description: Vous pouvez définir des expressions courantes utilisées sur votre site Web de sorte que lorsqu’un client entre dans une requête de recherche, il n’est pas nécessaire qu’il entre des guillemets autour des expressions que vous avez définies.
seo-title: A propos des expressions courantes
solution: Target
title: A propos des expressions courantes
topic: Linguistics,Site search and merchandising
uuid: 0f980a22-d826-4476-97de-0e9c14549bc8
translation-type: tm+mt
source-git-commit: 8efa90ac2927b263b7d48ccbf25d4b0e917dac79

---


# A propos des expressions courantes{#about-common-phrases}

Vous pouvez définir des expressions courantes utilisées sur votre site Web de sorte que lorsqu’un client entre dans une requête de recherche, il n’est pas nécessaire qu’il entre des guillemets autour des expressions que vous avez définies.

## Utilisation des expressions courantes {#concept_4946E53586DF492EAEB1B7F757FD440F}

>[!NOTE]
>
>La fonction Expression commune n’apparaît pas dans l’interface utilisateur, car elle n’est pas activée par défaut. Contactez le support technique pour activer cette fonctionnalité.

Les expressions courantes sont un ensemble d’expressions de plusieurs mots reconnues au cours de la recherche d’un client. Il traite les expressions comme un groupe combiné de mots plutôt que comme des mots individuels. Lorsqu’un client entre dans une requête de recherche sur votre site Web, il peut identifier des expressions en les entourant de guillemets doubles, tels que &quot;Océan Pacifique&quot;. Toutefois, lorsque vous ajoutez des groupes d’expressions courantes, les étapes de soumission sont exécutées automatiquement pour le client, car il trouve les expressions correspondantes dans la requête de recherche.

Supposons, par exemple, qu’un client de votre site Web entre la requête de recherche suivante :

`hotels near the pacific ocean`

Sans l&#39;ajout de guillemets `pacific ocean`, la recherche du client retourne les résultats pour les hôtels près de n&#39;importe quel océan dans le monde, ce qui n&#39;est pas ce que le client voulait.

Toutefois, lorsque vous ajoutez l’expression courante &quot;Océan Pacifique&quot;, leur requête de recherche est automatiquement convertie en ce qui suit :

`hotels near the "pacific ocean"`

L’utilisation d’expressions courantes n’empêche pas vos clients d’utiliser explicitement des guillemets autour d’expressions de mots. Au lieu de cela, elle ajoute simplement des guillemets lorsque ces expressions définies sont trouvées dans leur requête de recherche.

Cette extension de requête de recherche s&#39;applique aux paramètres CGI de recherche principale `sp_q` et `sp_q_#`,

Voir les lignes 25, 26 et 32 du tableau dans les paramètres [CGI de recherche](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8)principal.

## Ajout d’un groupe d’expressions commun {#task_35C84FABCD9042C5B48C5C788B752871}

Vous pouvez ajouter des groupes d’expressions communs pour vous assurer que les requêtes de recherche renvoient avec précision des pages Web contenant tous les mots, dans l’ordre et la proximité exacts, saisis par un client.

Lorsque vous ajoutez des groupes d’expressions communs, vous pouvez utiliser la fonction Rechercher sur la page principale Groupe d’expressions communs. La fonction Rechercher vous permet de rechercher une expression existante et de savoir dans quel groupe elle réside.

Voir [Recherche de groupes contenant des mots particuliers dans une expression](../c-about-linguistics-menu/c-about-common-phrases.md#task_20714969274740A7BB4DC71E705EA15E).

**Pour ajouter un groupe Expressions courantes**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la [!DNL Common Phrases Groups] page, cliquez sur **Ajouter un groupe** d’expressions.
1. Sur la [!DNL Add Common Phrase Group] page, définissez les options de votre choix et ajoutez toutes les expressions qui composent le groupe.

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
      <td colname="col2"> <p>Requis. </p> <p>Nom unique du groupe d’expressions commun. </p> <p>Si vous modifiez ultérieurement un groupe d’expressions commun, notez que vous ne pouvez pas modifier le nom du groupe. Pour modifier le nom du groupe, utilisez la fonction <span class="uicontrol"> Renommer</span> . </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB" format="dita" scope="local"> Attribution d’un nouveau nom à un groupe</a>d’expressions commun. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Remarques </p> </td> 
      <td colname="col2"> <p>Facultatif. </p> <p>Ajoutez des informations relatives au groupe Expression commune. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Phrases </p> </td> 
      <td colname="col2"> <p>Requis. </p> <p>Vous permet de spécifier une expression jusqu’à cinq mots au maximum. Pour ajuster le paramètre de mot maximum, contactez le support technique. </p> <p>Chaque expression saisie doit être unique dans n’importe quel groupe d’expressions commun. </p> <p>Utilisez les icônes plus (+) et moins (-) de la colonne Action pour ajouter l’expression saisie ou supprimer une expression. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **Ajouter**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Test d’une expression courante {#task_A0C344E051CA45A9A0588242F9DA675D}

Si vous avez sélectionné des champs de métadonnées à associer à un groupe d’expressions, vous pouvez tester l’extension d’une expression particulière.

Lorsque vous testez l’expansion d’une expression, vous recherchez une expression exacte par rapport aux champs de métadonnées que vous avez associés au groupe d’expressions. L’expression est recherchée comme si elle contenait des guillemets. Tous les autres champs de métadonnées recherchent uniquement les mots de l’expression, sans guillemets. Supposons, par exemple, que vous ayez testé l’expression `audi TT`. Les résultats renvoyés peuvent s’afficher comme suit :

`title|body|field3:"Audi TT" url|desc|keys|target|alt:Audi TT`

**Pour tester une expression courante**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la [!DNL Common Phrases Groups] page, dans l’expression **Test qui contient** le champ de texte, saisissez l’expression dont vous souhaitez tester l’extension de métadonnées.
1. Cliquez sur **[!UICONTROL Test]**.

   Les résultats de l’extension s’affichent dans la zone de texte.
1. (Facultatif) Faites glisser le coin inférieur droit de la zone de texte pour développer la zone d’affichage.

## Recherche de groupes contenant des mots particuliers dans une expression {#task_20714969274740A7BB4DC71E705EA15E}

Vous pouvez les utiliser [!DNL Find] pour rechercher des mots spécifiques dans une phrase parmi tous les groupes existants que vous avez ajoutés.

Lorsque vous utilisez Rechercher, il localise les éléments suivants :

* Où la même phrase se trouve exactement parmi tous les groupes.
* Tous les mots de l&#39;expression parmi tous les groupes, indépendamment du mot ordre et proximité dans l&#39;expression.

Voir aussi [Modification d’un groupe](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61)d’expressions commun.

**Pour rechercher des groupes contenant des mots particuliers dans une expression**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la [!DNL Common Phrases Groups] page, dans le champ de **[!UICONTROL Find groups with phrases that contain]** texte, saisissez une expression.
1. Cliquez sur **[!UICONTROL Find]**.

   Les résultats sont affichés dans la zone de texte.
1. (Facultatif) Effectuez une ou plusieurs des opérations suivantes :

   * Faites glisser le coin inférieur droit de la zone de texte pour développer la zone d’affichage.
   * Dans la fenêtre de résultats, cliquez sur une expression hyperliée pour ouvrir la page Modifier le groupe d’expressions commun du groupe associé.

## Modification d’un groupe d’expressions commun {#task_5CAC3A133C5342EEAFE55A7EABCBCD61}

Vous pouvez modifier les champs, notes et expressions existants d’un groupe d’expressions commun que vous avez ajouté. Toutefois, pour modifier le nom du groupe, vous devez utiliser la [!DNL Rename] fonctionnalité.

Voir aussi [Attribution d’un nouveau nom à un groupe](../c-about-linguistics-menu/c-about-common-phrases.md#task_168E07C59C0F40989D43E7010EFF22EB)d’expressions commun.

**Pour modifier un groupe Expressions courantes**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la [!DNL Common Phrases Groups] page, cliquez **[!UICONTROL Edit]** à l’extrémité droite du nom d’un groupe.
1. Sur la [!DNL Edit Common Phrase Group] page, définissez les options de votre choix.

   Voir le tableau des options sous [Ajout d’un groupe](../c-about-linguistics-menu/c-about-common-phrases.md#task_35C84FABCD9042C5B48C5C788B752871)d’expressions commun.
1. Cliquez sur **Enregistrer les modifications**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Changement du nom d’un groupe d’expressions commun {#task_168E07C59C0F40989D43E7010EFF22EB}

Vous pouvez modifier le nom d’un groupe d’expressions communes existant. Cependant, si vous souhaitez modifier les champs, notes et expressions existants d’un groupe d’expressions commun, vous devez utiliser la [!DNL Edit] fonctionnalité.

Voir [Modification d’un groupe](../c-about-linguistics-menu/c-about-common-phrases.md#task_5CAC3A133C5342EEAFE55A7EABCBCD61) d’expressions commun .

**Pour renommer un groupe Expressions courantes**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la [!DNL Common Phrases Groups] page, cliquez **[!UICONTROL Rename]** à l’extrémité droite du nom d’un groupe.
1. Sur la [!DNL Rename Common Phrase Group] page, dans le champ de **[!UICONTROL Group Name]** texte, saisissez le nouveau nom du groupe.
1. Cliquez sur **Renommer**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’un groupe d’expressions commun {#task_4106D282A2ED4A27B09EE5A8CAAEDA36}

Vous pouvez supprimer tout groupe d’expressions commun que vous avez ajouté. Si vous supprimez un groupe par erreur, vous pouvez l&#39;utiliser [!DNL History] pour le restaurer.

Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

**Pour supprimer un groupe Expressions courantes**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Linguistics]** > **[!UICONTROL Common Phrases]**.
1. Sur la [!DNL Common Phrases Groups] page, cliquez **[!UICONTROL Delete]** à l’extrémité droite du nom d’un groupe.
1. Sur la [!DNL Delete Common Phrase Group] page, cliquez sur **[!UICONTROL Delete]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

