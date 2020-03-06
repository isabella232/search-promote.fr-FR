---
description: Vous pouvez utiliser l’index incrémentiel pour indexer des "morceaux" de votre site Web en direct ou d’évaluation, comme une collection de pages fréquemment modifiées.
seo-description: Vous pouvez utiliser l’index incrémentiel pour indexer des "morceaux" de votre site Web en direct ou d’évaluation, comme une collection de pages fréquemment modifiées.
seo-title: Index incrémentiel
solution: Target
subtopic: Incremental Index
title: Index incrémentiel
topic: Index,Site search and merchandising
uuid: b1ee9b08-dcbe-4ffe-b0b4-d379daaac9b5
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# Index incrémentiel{#about-incremental-index}

Vous pouvez utiliser l’index incrémentiel pour indexer des &quot;morceaux&quot; de votre site Web en direct ou d’évaluation, comme une collection de pages fréquemment modifiées.

## Utilisation de l’index incrémentiel {#concept_A7770F0552D14C47B3DDB65DB78FFFEE}

Un index incrémentiel ne prend que quelques secondes et est utile sur les sites Web de grande capacité qui peuvent prendre plusieurs heures pour complètement indexer.

Lorsque vous générez un index incrémentiel, des informations d’état s’affichent, telles que l’heure de début, l’heure écoulée et les erreurs survenues pendant le processus d’indexation. Des informations sur l’état de votre dernier index s’affichent également.

Vous pouvez arrêter ou redémarrer le processus d’indexation incrémentielle à tout moment.

Pendant que le nouvel index incrémentiel est généré pour votre site Web en ligne, les clients peuvent continuer à rechercher votre site à l’aide de votre dernier index incrémentiel.

## Configuration d’un index incrémentiel d’un site Web intermédiaire {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

Vous pouvez configurer les pages de site Web que vous souhaitez inclure dans votre index incrémentiel en spécifiant les URL de site Web et les masques d’URL.

**Pour configurer un index incrémentiel d’un site Web intermédiaire**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Configuration]**.
1. Sur la **[!UICONTROL Incremental Index Configuration]** page, utilisez les différents champs pour spécifier les pages à indexer.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Champ </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Ajout ou mise à jour d’URL </p> </td> 
      <td colname="col2"> <p>Spécifiez des URL. </p> <p>Le robot de recherche indexe uniquement les documents spécifiés qui ont changé depuis la dernière indexation. </p> <p>De plus, le robot de recherche suit les liens contenus dans les documents spécifiés et indexe uniquement les documents qui ont changé. </p> <p>Ce champ ne doit contenir que des URL de document et non des masques, comme dans l’exemple suivant : </p> <p> 
        <userinput>
          https://www.mydomain.com/products/new.html 
        </userinput> </p> <p>Vous pouvez utiliser les mots-clés suivants avec l’URL : </p> <p> 
        <ul id="ul_62D1082ACBD547D092B10D72C56A3A1E"> 
          <li id="li_32C2B21DE75C4459908384CC44822F7D"> 
          <userinput>
            noindex 
          </userinput> <p>Si vous ne souhaitez pas indexer le texte de la page qui correspond à une URL spécifiée, mais que vous souhaitez suivre les liens de la page, ajoutez 
            <userinput>
              noindex 
            </userinput> après l’URL, comme dans l’exemple suivant : </p> <p> 
            <userinput>
              https://www.mydomain.com/products/new.html noindex 
            </userinput> </p> <p>Assurez-vous de bien séparer 
            <userinput>
              noindex 
            </userinput> de l’URL avec un espace ; une virgule n’est pas un séparateur valide. </p> </li> 
          <li id="li_33AB62B669084BF7B976F4308715E435"> 
          <userinput>
            nofollow 
          </userinput> <p>Si vous souhaitez indexer le texte de la page qui correspond à l’URL spécifiée, mais que vous ne souhaitez pas suivre les liens de la page, ajoutez 
            <userinput>
              nofollow 
            </userinput> après l’URL, comme dans l’exemple suivant : </p> <p> 
            <userinput>
              https://www.mydomain.com/products/new.html nofollow 
            </userinput> </p> <p> Assurez-vous de bien séparer 
            <userinput>
              nofollow 
            </userinput> de l’URL avec un espace ; une virgule n’est pas un séparateur valide. </p> </li> 
        </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rechercher et mettre à jour des masques d’URL </p> </td> 
      <td colname="col2"> <p>Spécifiez des masques d’URL simples (chemin complet, chemin partiel ou chemins utilisant des caractères génériques ou des expressions régulières). </p> <p>Le robot de recherche ne trouve tous les documents et index correspondants que ceux qui ont changé depuis la dernière indexation. </p> <p>De plus, le robot de recherche suit les liens contenus dans les documents et index correspondants uniquement les pages qui ont changé. Par exemple : </p> <p> 
      <userinput>
        https://www.mydomain.com/products/household/*.html 
      </userinput> </p> <p>Vous pouvez également utiliser des expressions régulières, comme dans l’exemple suivant : </p> <p> 
      <userinput>
        regexp ^https://www\.mondomaine\.com/products/home/.*\.html$ 
      </userinput> </p> <p>Voir Expressions <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"></a>régulières. </p> <p>Vous pouvez également utiliser les mots-clés 
      <userinput>
        nofollow 
      </userinput> et 
      <userinput>
        noindex 
      </userinput> comme décrit dans <span class="uicontrol"> Ajout ou mise à jour d’URL </span> ci-dessus. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure et exclure les masques d’URL </p> </td> 
      <td colname="col2"> <p>Spécifiez des masques d’URL simples à inclure ou à exclure (chemin complet, chemin partiel ou chemins utilisant des caractères génériques ou des expressions régulières). </p> <p>Le robot de recherche trouve et indexe ("include") ou ignore les documents ("exclude") en fonction du type de masque spécifié. </p> <p> Lors de l’indexation d’un site, les directions sont suivies par ordre d’apparence. Par exemple, la liste suivante de masques : </p> <p> 
      <userinput>
        inclure https://www.mydomain.com/products/household/lightbulbs*.html 
      </userinput> </p> <p> 
      <userinput>
        exclure https://www.mydomain.com/products/ 
      </userinput> </p> <p>indexe les pages 
      <userinput>
        lightbulbs1.html 
      </userinput> et 
      <userinput>
        lightbulbs2.html 
      </userinput>. Toutefois, il n’indexe aucune autre page répertoriée sous le répertoire products. </p> <p>Un masque d’URL qui s’affiche en premier prévaut toujours sur un masque qui s’affiche plus loin dans la liste. De plus, si le robot de recherche rencontre un document qui correspond à la fois à un masque d’inclusion et à un masque d’exclusion, le masque répertorié en premier est prioritaire. </p> <p>Vous pouvez également utiliser les mots-clés 
      <userinput>
        nofollow 
      </userinput> et 
      <userinput>
        noindex 
      </userinput> comme décrit dans <span class="uicontrol"> Ajout ou mise à jour d’URL </span> ci-dessus. </p> <p>Voir <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164" type="concept" format="dita" scope="local"> A propos des masques</a>URL. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Inclure et exclure des masques de date </p> </td> 
      <td colname="col2"> <p>Spécifiez des masques de date simples (chemin complet, chemin partiel ou chemins utilisant des caractères génériques ou des expressions régulières) ou incluez-les ou excluez-les. </p> <p>Le robot de recherche trouve et indexe ("inclure") ou ignore les documents ("exclure") en fonction de l’URL et de la date des documents. </p> <p>Vous pouvez utiliser les types de masques de date suivants : </p> <p> 
      <ul id="ul_8958ED54C8EF405AA259236595ED3ABA"> 
      <li id="li_0A7841767E004F088CA6FA42E99B9F32"> 
      <userinput>
        include-days NNN 
      </userinput> <p>Le robot de recherche indexe tous les documents qui correspondent au masque d’URL spécifié et qui datent au moins de plusieurs jours NNN. </p> <p>Vous pouvez suivre le masque d’URL avec un ou plusieurs des mots-clés suivants : 
        <ul id="ul_22A38D5F38B344ABB02B16EB1865813B"> 
        <li id="li_B89CC37DC2A1428185E86FFCB9DDB193">nofollow </li> 
        <li id="li_C2579B3A338D4AF987C3F518806734B0">noindex </li> 
        <li id="li_0527BF7103F34B83AC3E684069B899F7">server-date </li> 
        </ul> </p> <p>Par exemple, le masque suivant inclut tous les documents du dossier /archive/support qui ont 0 jour ou plus : </p> <p> 
        <userinput>
          include-days 0 https://www.mydomain.com/archive/support/ 
        </userinput> </p> </li> 
      <li id="li_7663ABED40DD4E159F746E4F92BB6407"> 
      <userinput>
        include-date AAAA-MM-JJ 
      </userinput> <p>Le robot de recherche indexe tous les documents qui correspondent au masque d’URL spécifié et qui sont antérieurs ou antérieurs à la date AAAA-MM-JJ. </p> <p>Vous pouvez suivre le masque d’URL avec un ou plusieurs des mots-clés suivants : </p> <p> 
        <ul id="ul_57BF37A413BB4A4D962863DACE56F395"> 
        <li id="li_88CAB9AB583B4754A5C53478BD1108FF">nofollow </li> 
        <li id="li_999E1CD34FDE4A1B9C332B4AA8C2887D">noindex </li> 
        <li id="li_05646FACF3524D2A9E201A23770E357F"> server-date </li> 
        </ul> </p> <p>L’exemple de masque suivant inclut tous les documents du dossier /archive/ daté du 25 juillet 2011 ou avant : </p> <p> 
        <userinput>
          include-date 2011-07-25 https://www.mydomain.com/archive/ 
        </userinput> </p> </li> 
      <li id="li_172692DEDA8744B3AA492701D24C2D80"> 
      <userinput>
        exclude-days NNN 
      </userinput> <p>Désactivez l’indexation de tous les documents qui correspondent au masque d’URL spécifié et qui datent de NNN jours ou plus. </p> <p>Vous pouvez éventuellement suivre le masque d’URL en fonction du mot-clé 
        <userinput>
          server-date 
        </userinput>. </p> <p>L’exemple de masque suivant exclut de votre index tous les fichiers PDF âgés de 90 jours ou plus : </p> <p> 
        <userinput>
          exclude-days 90 *.pdf 
        </userinput> </p> </li> 
      <li id="li_26078517744D4AECBE1351008926CBAE"> 
      <userinput>
        exclude-date AAAA-MM-JJ 
      </userinput> <p>Désactivez l’indexation de tous les documents qui correspondent au masque d’URL spécifié et qui sont antérieurs ou antérieurs à la date AAAA-MM-JJ. </p> <p>Vous pouvez éventuellement suivre le masque d’URL en fonction du mot-clé 
        <userinput>
          server-date 
        </userinput>. </p> <p>L’exemple de masque suivant exclut tous les documents du dossier /archive/ daté du 23 avril 2004 ou avant : </p> <p> 
        <userinput>
          exclude-date 2004-04-23 https://www.mydomain.com/archive/ 
        </userinput> </p> </li> 
      </ul> </p> <p>Voir <a href="../c-about-settings-menu/c-about-crawling-menu.md#concept_F4F1F58A646F4A86B8650EC46FDCEF66" type="concept" format="dita" scope="local"> A propos des masques</a>de date. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Suppression d’URL </p> </td> 
      <td colname="col2"> <p>Spécifiez des URL. </p> <p>Le robot de recherche trouve et supprime les documents spécifiés de l'index de recherche. Si une page spécifique figure déjà dans l'index de recherche, le robot la supprime avant d'ajouter ou de mettre à jour d'autres pages. </p> <p>Ce champ ne doit contenir que des URL de document et non des masques. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rechercher et supprimer des masques d’URL </p> </td> 
      <td colname="col2"> <p>Spécifiez des masques d’URL simples (chemin complet, chemin partiel ou utilisant des caractères génériques ou des expressions régulières). </p> <p>Si le masque d’URL spécifié correspond aux pages de votre index de recherche, le robot de recherche supprime les pages avant d’ajouter ou de mettre à jour d’autres pages. Par exemple : </p> <p> 
      <userinput>
        https://www.mydomain.com/products/1998/household/* 
      </userinput> </p> <p>Vous pouvez également utiliser des expressions régulières, comme dans l’exemple suivant : </p> <p> 
      <userinput>
        regexp ^https://www\.mondomaine\.com/products/199[567]/.*$ 
      </userinput> </p> <p>Voir Expressions <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"></a>régulières. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Définition de la planification de l’index incrémentiel pour un site Web en direct {#task_2A46BA189ECC4317A9D5C6E99A336F33}

Vous pouvez sélectionner la fréquence d’index incrémentiel et le temps de base utilisé pour analyser et mettre à jour votre index incrémentiel.

L’heure sélectionnée est locale en fonction du fuseau horaire configuré dans les Paramètres du compte.

Voir [Configuration des paramètres](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9)de votre compte.

Les serveurs Web sont souvent programmés pour une maintenance en pleine nuit. Si votre serveur est en panne pendant une heure d’index planifiée, le processus d’indexation échoue. Veillez à sélectionner l’heure de la journée à laquelle votre serveur Web est disponible.

Le calendrier de l&#39;index ne s&#39;applique qu&#39;à votre index en direct ; vous ne pouvez pas planifier des index par étapes.

**Pour définir la planification de l’index incrémentiel pour un site Web en direct**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Schedule]**.
1. Dans la **[!UICONTROL Incremental Index Schedule]** page, dans la liste **[!UICONTROL Incrementally Index]** déroulante, sélectionnez la fréquence d’indexation en heures ou en minutes.
1. Dans la liste **[!UICONTROL Base Time]** déroulante, sélectionnez l’heure de début de la régénération d’un nouvel index incrémentiel.
1. Cliquez sur **[!UICONTROL Save Changes]**.

## Exécution d’un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire {#task_9BFB6157F3884B2FAECB7E0E9CA318CB}

Vous pouvez utiliser l’index incrémentiel pour indexer des &quot;morceaux&quot; de votre site Web en direct ou d’évaluation, comme une collection de pages fréquemment modifiées.

**Pour exécuter un index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire**

1. Dans le menu du produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Index]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Index]**.

1. Cliquez sur **[!UICONTROL Incremental Index Now]**.
1. (Facultatif) Si des erreurs d’indexation se sont produites, cliquez sur **[!UICONTROL View Errors]** pour afficher le journal associé.

## Affichage du journal d’index incrémentiel d’un site Web en direct ou d’un site Web intermédiaire {#task_E668E1F1240C476DAA1CA783DC728232}

Lorsqu’un index incrémentiel actif ou un index incrémentiel intermédiaire est terminé, vous pouvez afficher le journal associé afin de résoudre les erreurs qui se sont produites.


Vous ne pouvez pas exporter de journaux ni les enregistrer. Le journal reste disponible jusqu’à ce que le nouvel index se produise.

**Pour afficher le journal d’index incrémentiel d’un site Web en direct ou d’évaluation**

1. Dans le menu du produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Live Log]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Incremental Index]** > **[!UICONTROL Staged Log]**.

1. Dans la page du journal, en haut ou en bas, effectuez l’une des opérations suivantes :

   * Utilisez les options de navigation **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** pour parcourir le journal.

   * Utilisez les options d’affichage **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** pour affiner ce que vous voyez.

