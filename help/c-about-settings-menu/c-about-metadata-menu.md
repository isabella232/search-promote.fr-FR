---
description: Utilisez le menu Métadonnées pour personnaliser les définitions de recherche et les injections d’index.
seo-description: Utilisez le menu Métadonnées pour personnaliser les définitions de recherche et les injections d’index.
seo-title: A propos du menu Métadonnées
solution: Target
subtopic: Metadata
title: A propos du menu Métadonnées
topic: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
translation-type: tm+mt
source-git-commit: cf2707d124bd3f3a864610bcf41dda5e5670fc90

---


# A propos du menu Métadonnées{#about-the-metadata-menu}

Utilisez le menu Métadonnées pour personnaliser les définitions de recherche et les injections d’index.

## A propos des définitions {#concept_AE48035C210145169BE067D396975620}

Vous pouvez utiliser [!DNL Definitions] pour personnaliser le contenu et la pertinence des champs HTML et de métadonnées pris en compte lorsqu’un client envoie une requête de recherche.

Vous pouvez modifier les champs déjà prédéfinis. Vous pouvez également créer des champs définis par l’utilisateur en fonction du contenu des balises de métadonnées. Chaque définition s’affiche sur une seule ligne de la [!DNL Staged Definitions] page.

Voir aussi [A propos des vues](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)de données.

## Ajout d’un nouveau champ de balise meta {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

Vous pouvez définir et ajouter vos propres champs de balise de métadonnées.

Avant que les effets de la nouvelle définition de balise meta ne soient visibles par les clients, vous devez recréer l’index de votre site.

**Pour ajouter un nouveau champ de balise meta**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Sur la [!DNL Definitions] page, cliquez sur **[!UICONTROL Add New Field]**.
1. Sur la [!DNL Add Field] page, définissez les options de votre choix.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom du champ </p> </td> 
      <td colname="col2"> <p>Spécifie un nom utilisé pour référencer le champ. </p> <p>Le nom du champ doit respecter les règles suivantes : </p> <p> 
      <ul id="ul_D39D09CD7E7D41A59ECB6C5A6F4F263D"> 
      <li id="li_11CE852BE3C64CEF90FEC7A6E1079E13"> Le nom ne doit contenir que des caractères alphanumériques. </li> 
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> Les tirets sont autorisés dans le nom, mais pas dans les espaces. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> Vous pouvez saisir un nom de 20 caractères maximum. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> Le nom n’est pas sensible à la casse, mais il est affiché et stocké exactement au moment où vous le saisissez. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> Vous ne pouvez pas utiliser les noms qui existent dans les champs prédéfinis comme le montre le tableau de la page <span class="wintitle"> Définitions par étapes </span> . </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> Vous ne pouvez pas utiliser le mot "any" comme valeur d’un nom de champ défini par l’utilisateur. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> Vous ne pouvez pas modifier les noms des champs prédéfinis. </li> 
      </ul> </p> <p> Exemples de noms de champ : </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> Auteur </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> Date de publication </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> quelque chose de sauvage </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom(s) de balise(s) méta </p> </td> 
      <td colname="col2"> <p>Détermine le contenu associé au champ défini. </p> <p>La liste des noms peut comporter jusqu’à 255 caractères. De plus, le nom peut contenir tous les caractères autorisés dans l’attribut name d’une balise meta HTML. </p> <p>Vous pouvez spécifier plusieurs balises meta dans une définition de champ unique. </p> <p>Plusieurs valeurs doivent être séparées par des virgules et le nom de balise meta le plus à gauche trouvé sur une page Web donnée est prioritaire. </p> <p>Supposons, par exemple, que vous ayez défini un champ nommé "auth". Le nom du champ comporte les balises meta associées "author, dc.author". Dans ce cas, le contenu de la balise meta "author" est indexé et recherché sur celui de "dc.author" si les deux balises meta apparaissent sur une page Web. </p> <p>Les champs définis par l’utilisateur doivent avoir au moins un nom de balise meta dans leur définition. Les champs prédéfinis ne doivent pas nécessairement être associés à une balise meta. Toutefois, si une ou plusieurs balises meta sont spécifiées, le contenu des balises meta remplace la source de données actuelle pour chaque balise . </p> <p>Par exemple, si la balise meta "dc.title" est associée au champ prédéfini "title", le contenu de la balise meta "dc.title" est indexé sur celui de la balise meta 
      <userinput>
        &lt;title&gt; 
      </userinput> pour un document particulier. </p> <p>Voici quelques exemples : </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> description </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> proprietarytag </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>Type de données </p> </td> 
      <td colname="col2"> <p>Chaque champ est associé à un type de données tel que texte, nombre, date, version, rang ou emplacement. Ce type de données détermine le mode d’indexation, de recherche et, éventuellement, de tri du contenu du champ. </p> <p>Vous ne pouvez pas modifier le type de données après avoir créé la définition de champ. </p> <p>Utilisez les informations suivantes pour vous aider à sélectionner le type de données approprié aux informations contenues dans le champ. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> Les champs de type </span> de données de texte sont traités comme des chaînes de caractères. </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> Les champs de type </span> de données Nombre sont traités comme des valeurs numériques entières ou à virgule flottante. </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> Les champs </span> de type de données de date sont traités comme des spécificateurs de date et d’heure. Vous pouvez personnaliser les formats de date et d’heure autorisés lorsque vous ajoutez ou modifiez le nouveau champ. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> Les champs de type de données de version </span> sont traités comme des données numériques de forme libre. Par exemple, la version 1.2.3 est triée avant la version 1.2.2. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> Les champs de type </span> de données de classement sont traités de la même manière que les champs de type "Nombre", sauf qu’ils influencent en outre les calculs de classement/pertinence dans les résultats de recherche. <p>Voir <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">A propos des règles de classement </a>. </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> Les champs de type </span> de données d’emplacement sont traités comme un emplacement physique n’importe où dans le monde. Les formats d’emplacement autorisés sont les suivants : <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> Codes postaux à 5 ou 9 chiffres sous la forme de DJJ ou DJJ-DJJ, où chaque "D" est un 0-9 chiffres. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> Codes à trois chiffres sous forme de DDD. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> Paires latitude/longitude sous la forme ±DD.DDDD±DDD.DDD, où le premier nombre spécifie la latitude et le second la longitude. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Autoriser les listes </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Texte </span>ou <span class="uicontrol"> Nombre </span> est sélectionné. </p> <p>Indexez séparément les valeurs délimitées dans le contenu des métadonnées de ce champ. </p> <p>Par exemple, le contenu "Rouge, Jaune, Vert, Bleu" est traité comme quatre valeurs distinctes au lieu d’une seule lorsque l’option "Autoriser les listes" est sélectionnée. Ce traitement est particulièrement utile pour la recherche de plage (à l’aide de 
      <userinput>
        sp_q_min 
      </userinput>, 
      <userinput>
        sp_q_max 
      </userinput> ni 
      <userinput>
        sp_q_exact 
      </userinput>) et avec la variable 
      <userinput>
        &lt;search-field-value-list&gt; 
      </userinput>, 
      <userinput>
        &lt;search-field-values&gt; 
      </userinput>, et 
      <userinput>
        &lt;search-display-field-values&gt; 
      </userinput>. </p> <p>Non disponible si le type de données Version est sélectionné. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Facette dynamique </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>Remarque : cette fonctionnalité n’est pas activée par défaut. Contactez le support technique pour l’activer pour votre utilisation. Une fois activé, il apparaît dans l’interface utilisateur. </p> </p> <p>Définit la facette identifiée comme étant dynamique. </p> <p>Les facettes sont créées au-dessus des champs de balise meta. Un champ de balise meta est une couche de recherche principale de bas niveau d’Adobe Search&amp;Promote. Les facettes, en revanche, font partie de GS (Guided Search), la couche de présentation de haut niveau d’Adobe Search&amp;Promote. Les facettes possèdent des champs de balise meta, mais les champs de balise meta ne connaissent rien aux facettes. </p> <p>Voir <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> A propos des facettes dynamiques </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Autoriser la déduplication </p> </td> 
      <td colname="col2"> <p>Cochez cette option pour activer la déduplication pour ce champ. En d’autres termes, autorisez ce champ à être spécifié au moment de la recherche au moyen de la variable 
        <userinput>
          sp_dedupe_field 
        </userinput> Paramètre CGI de recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Rechercher des paramètres CGI </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du tableau </p> </td> 
      <td colname="col2"> <p>Associe définitivement le champ donné au nom de table donné. </p> <p>Chaque fois qu’un tel champ est mentionné dans un paramètre CGI de recherche principal ou une balise de modèle, le nom de la table est fourni automatiquement. Cette fonctionnalité permet de sélectionner des facettes dynamiques par le biais de correspondances de tableau, mais vous pouvez également l’utiliser pour les champs de facettes non dynamiques, si vous le souhaitez. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Délimiteurs de liste </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> l’option Autoriser les listes </span> est sélectionnée. </p> <p>Indique les caractères qui séparent les valeurs de liste individuelles. Vous pouvez spécifier plusieurs caractères, chacun étant traité comme un séparateur de valeurs. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rechercher par défaut </p> </td> 
      <td colname="col2"> <p>Lorsque cette option est sélectionnée, la recherche porte sur le contenu du champ, même si celui-ci n’est pas explicitement spécifié dans une requête de recherche donnée. Si vous désélectionnez cette option, la recherche du champ n’est effectuée que sur demande. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Champ de mise à jour verticale </p> </td> 
      <td colname="col2"> <p> <p>Remarque : cette fonctionnalité n’est pas activée par défaut. Contactez le support technique pour l’activer pour votre utilisation. Une fois activé, il apparaît dans l’interface utilisateur. </p> </p> <p>Définit le champ identifié comme un champ de mise à jour verticale. </p> <p>Les champs Mise à jour verticale sont des champs pouvant être mis à jour au moyen du processus Mise à jour verticale ( <span class="uicontrol"> Index </span> &gt; <span class="uicontrol"> Mise à jour verticale </span>). En raison de la manière dont les mises à jour verticales sont effectuées, il n’est pas possible de rechercher le contenu de ces champs dans des recherches en texte libre. Si vous cochez cette option, le contenu de ce champ n’est pas ajouté à l’index "word" lors d’une opération d’index quelconque. Il active également la mise à jour de ce champ lors d’une opération de mise à jour verticale. </p> <p>Pour en savoir plus sur les mises à jour verticales, voir <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> A propos des mises à jour verticales </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pertinence </p> </td> 
      <td colname="col2"> <p>Vous pouvez modifier la pertinence des champs prédéfinis et définis par l’utilisateur. </p> <p>La pertinence est spécifiée sur une échelle de 1 à 10. Un paramètre de 1 signifie qu’il est le moins pertinent et 10 qu’il est le plus pertinent. Ces valeurs sont prises en compte lorsque le logiciel considère que la requête correspond à chaque champ. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tri </p> </td> 
      <td colname="col2"> <p>Indique le moment où les résultats sont triés par champ nommé, au moyen de la variable 
        <userinput>
          sp_s 
        </userinput> Paramètre CGI de recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Rechercher des paramètres CGI </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Langue </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span>, <span class="uicontrol"> Nombre </span>ou <span class="uicontrol"> Date </span> est sélectionné. </p> <p>Contrôle les conventions de langue et de paramètres régionaux appliquées lors de l’indexation des valeurs de date, de nombre et de classement pour ce champ. </p> <p>Vous pouvez choisir d’appliquer la langue du compte (Linguistique &gt; Mots et langues). Vous pouvez également appliquer la langue associée au document qui contient chaque numéro ou valeur de date, ou une langue spécifique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format(s) de date </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Date </span> est sélectionné. </p> <p>Contrôle les formats de date reconnus lors de l’indexation des valeurs de date pour ce champ. </p> <p>Une liste par défaut des chaînes de format de date est fournie pour chaque champ de date. Vous pouvez ajouter à la liste ou la modifier en fonction des besoins de votre site. </p> <p>Voir <a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> Formats de date </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formats de date de test </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Date </span> est sélectionné comme type de données. </p> <p>Vous permet de prévisualiser les formats de date que vous avez spécifiés pour vous assurer qu’ils sont correctement formatés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuseau horaire </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Date </span> est sélectionné comme type de données. </p> <p>Contrôle le fuseau horaire supposé appliqué lors de l’indexation des valeurs de date pour ce champ qui ne spécifient pas de fuseau horaire. </p> <p>Si, par exemple, le fuseau horaire de votre compte est défini sur "Amérique/Los Angeles" et que vous sélectionnez <span class="uicontrol"> Utiliser le fuseau horaire du compte </span>, la valeur de date méta suivante, qui n’a pas de fuseau horaire spécifié, est traitée comme s’il s’agissait de l’heure du Pacifique, en tenant compte des économies d’heure d’été : </p> <p>&lt;meta name="dc.date" content="Lun, 05 septembre 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de classement la moins importante </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span> est sélectionné comme Type de données. </p> <p>Contrôle la valeur de classement qui représente le rang minimal d’un document. </p> <p>Si le classement du document est compris entre 0 pour le rang le plus bas et 10 pour le rang le plus élevé, définissez cette valeur sur 0. </p> <p>Si le classement du document est compris entre 1 pour le rang le plus élevé et 10 pour le rang le plus bas, définissez cette valeur sur 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de classement par défaut </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span> est sélectionné comme Type de données. </p> <p>Contrôle la valeur de classement utilisée si un document ne contient aucune balise meta définie pour ce champ de classement. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de classement la plus importante </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span> est sélectionné comme Type de données. </p> <p>Contrôle la valeur de classement qui représente le rang maximal d’un document. </p> <p>Si le classement du document est compris entre 0 pour le rang le plus bas et 10 pour le rang le plus élevé, définissez cette valeur sur 10. </p> <p>Si le classement du document est compris entre 1 pour le rang le plus élevé et 10 pour le rang le plus bas, définissez cette valeur sur 1. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Unités par défaut </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Emplacement </span> est sélectionné en tant que Type de données. </p> <p>Contrôle le traitement des valeurs de distance pour les recherches de proximité. </p> <p>Si vous définissez les unités par défaut sur <span class="uicontrol"> Miles </span>, tous les critères de distance minimale/maximale de la recherche de proximité appliqués à ce champ (au moyen de la variable 
      <userinput>
        sp_q_min[_#] 
      </userinput> ou la variable 
      <userinput>
        sp_q_max[_#] 
      </userinput> Les paramètres CGI de recherche) sont considérés comme des milles, sinon comme des kilomètres. </p> <p>Cette option contrôle également les unités de distance par défaut appliquées à la sortie de la variable 
      <userinput>
        &lt;Search-Display-Field&gt; 
      </userinput> balise de modèle des résultats de recherche lorsqu’elle est appliquée à un champ de sortie de recherche de proximité. </p> <p>Voir <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> A propos de la recherche de proximité </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Créer une description de plage ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Number </span> est sélectionné comme type de données. </p> <p>Contrôle la création automatique de descriptions de plage de champs, à utiliser avec <span class="uicontrol"> Conception </span> &gt; <span class="uicontrol"> Navigation </span> &gt; <span class="uicontrol"> Facettes </span>. </p> <p>Voir <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> A propos des facettes </a>. </p> <p> <p>Remarque :  Si le champ Champ de mise à jour <span class="uicontrol"> verticale </span> est coché dans ce champ, le champ de description de la plage de champs généré est mis à jour lors d’une mise à jour verticale. Toutefois, il est recommandé que le champ identifié dans le champ <span class="uicontrol"> Plage </span> soit <span class="uicontrol"> également contrôlé dans le champ Mise à jour verticale </span> . </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Champ de plage </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée. </p> <p>Le <span class="uicontrol"> champ de texte </span> à mettre à jour avec les descriptions de plage pour le champ actif. Cette liste contient tous les <span class="uicontrol"> champs </span> de texte qui ne sont pas encore utilisés avec d’autres champs pour la génération de plages de champs. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeurs de plage </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Liste de points de données délimités par des champs à utiliser lors de la création des descriptions de plage de champs. Par exemple : </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>Vous pouvez entrer ces valeurs dans n’importe quel ordre. Les valeurs sont triées et les doublons sont supprimés avant d’être enregistrés. Vous pouvez également spécifier des valeurs négatives et non entières. </p> <p>Pour chacune des valeurs de ce champ : 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">si la valeur est inférieure à (&lt;) la valeur la plus petite dans <span class="uicontrol"> les valeurs de plage </span>, le format <span class="uicontrol"> "Inférieur à" </span> est utilisé. </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">si la valeur est supérieure ou égale à (&gt;=) la valeur la plus élevée dans <span class="uicontrol"> les valeurs de plage </span>, le format <span class="uicontrol"> "Supérieur à" </span> est utilisé. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">dans le cas contraire, une "plage" est trouvée lorsque la valeur du champ est comprise entre deux valeurs <span class="uicontrol"> de plage consécutives </span> (supérieures à (&gt;) la valeur la plus petite et inférieure ou égale à (&lt;=) la valeur la plus élevée), et le <span class="uicontrol"> format intermédiaire </span> est utilisé. </li> 
    </ul> </p> <p>Par exemple, l’exemple ci-dessus définit un ensemble de descriptions pour les valeurs : 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">moins de 10 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">supérieur ou égal à 10 et inférieur à 20 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">supérieur ou égal à 20 et inférieur à 50 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">supérieur ou égal à 50 et inférieur à 100 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">supérieur ou égal à 100 et inférieur à 10000 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">supérieur ou égal à 10000 </li> 
      </ul> </p> <p>Voir <span class="uicontrol"> Test à l’aide de l’option Plus grand que ? </span> pour modifier la manière dont ces tests sont effectués. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format "Inférieur à" </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Il s’agit du modèle utilisé pour spécifier la description de la plage pour les valeurs inférieures à la plus petite valeur trouvée dans <span class="uicontrol"> les valeurs de plage </span>. La valeur la plus petite sera représentée à l’aide du jeton d’espace réservé numérique <span class="uicontrol"> ~N~ </span>. Par exemple : </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>ou : </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>Normalement, la valeur sera formatée "telle quelle" - c’est-à-dire pour une <span class="uicontrol"> définition des valeurs de plage </span> de "5 10 20" et une valeur fournie de 1, la description de plage générée serait simplement quelque chose comme "Inférieur à 5". Si vous souhaitez plutôt qu’il soit "4.99 et moins", définissez <span class="uicontrol"> Precision </span> sur <span class="uicontrol"> 2 </span> et utilisez ce format : </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p>Dans <span class="uicontrol"> le format "Inférieur à" </span>, la minuscule <span class="uicontrol"> ~n~ </span> provoquera l’arrondi <i>vers le bas</i> de la valeur selon le paramètre de  de précision <span class="uicontrol"> .</span> </p> <p>Remarque : pour inclure n’importe quel espace réservé numérique dans la description de la plage, en l’état, spécifiez avec un préfixe de barre oblique inverse (\) - par ex. <span class="uicontrol"> \~N~ </span> ou <span class="uicontrol"> \~n~ </span>. Pour inclure une barre oblique inverse, spécifiez-la avec une autre barre oblique inverse (ex. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format intermédiaire </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Il s’agit du modèle utilisé pour spécifier la description de la plage pour les valeurs qui se situent entre les valeurs les plus petites et les plus élevées trouvées dans les <span class="uicontrol"> valeurs de plage </span>. Pour la plage donnée, la valeur de plage inférieure sera représentée à l’aide du jeton d’espace réservé numérique <span class="uicontrol"> ~L~ </span>, et la valeur de plage supérieure sera représentée à l’aide du jeton <span class="uicontrol"> ~H~ </span>. Par exemple : </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>ou : </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>ou : </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>Normalement, les valeurs sont formatées "en l’état" - c’est-à-dire pour une <span class="uicontrol"> définition des valeurs de plage </span> de "5 10 20" et une valeur fournie de 8, la description de plage générée ressemblerait simplement à "Entre 5 et 10". Si vous souhaitez plutôt qu’il s’agisse de "Entre 5 et 9,99", avec la valeur la plus élevée ajustée <i>vers le bas</i>, définissez <span class="uicontrol"> Precision </span> sur <span class="uicontrol"> 2 </span> et utilisez ce format : </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>De même, <span class="uicontrol"> ~L~ </span> peut être remplacé par <span class="uicontrol"> ~l~ </span> pour que la valeur la plus faible soit ajustée <i>vers le haut</i>, également selon le paramètre de  de précision <span class="uicontrol"> . </span> Cela signifie qu’une définition telle que : </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>avec une <span class="uicontrol"> valeur de précision </span> de <span class="uicontrol"> 2 </span> créerait "Entre 5,01 et 10". </p> <p>La minuscule <span class="uicontrol"> ~l~ </span> entraîne l’arrondi <i>vers le haut</i> de la valeur inférieure en fonction du paramètre <span class="uicontrol"> Precision </span> , tandis que la minuscule <span class="uicontrol"> ~h~  entraîne l’arrondi down de la valeur supérieure.</span><i></i> </p> <p>Remarque : pour inclure n’importe quel espace réservé numérique dans la description de la plage, en l’état, spécifiez avec un préfixe de barre oblique inverse (\) - par ex. <span class="uicontrol"> \~L~ </span> ou <span class="uicontrol"> \~h~ </span>. Pour inclure une barre oblique inverse, spécifiez-la avec une autre barre oblique inverse (ex. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format "Supérieur à" </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Il s’agit du modèle utilisé pour spécifier la description de la plage pour les valeurs supérieures à la valeur la plus élevée trouvée dans <span class="uicontrol"> les valeurs de plage </span>. La valeur la plus élevée sera représentée à l’aide du jeton d’espace réservé numérique <span class="uicontrol"> ~N~ </span>. Par exemple : </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>ou : </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>Normalement, la valeur sera formatée "telle quelle" - c’est-à-dire pour une définition des valeurs de <span class="uicontrol"> plage </span> de "5 10 20" et une valeur fournie de 30, la description de plage générée serait simplement un peu comme "Supérieur à 20". Si vous souhaitez plutôt qu’il soit "20.01 et plus", définissez <span class="uicontrol"> Precision </span> sur <span class="uicontrol"> 2 </span> et utilisez ce format : </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p>Dans le format <span class="uicontrol"> "Supérieur à" </span>, la minuscule <span class="uicontrol"> ~n~ </span> provoquera l’arrondi de la valeur <i>vers le haut</i> selon le paramètre de  de précision <span class="uicontrol"> .</span> </p> <p>Remarque : pour inclure n’importe quel espace réservé numérique dans la description de la plage, en l’état, spécifiez avec un préfixe de barre oblique inverse (\) - par ex. <span class="uicontrol"> \~N~ </span> ou <span class="uicontrol"> \~n~ </span>. Pour inclure une barre oblique inverse, spécifiez-la avec une autre barre oblique inverse (ex. <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Précision </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Valeur entière spécifiant le nombre de chiffres à droite d’un point décimal. Cela contrôle également les arrondissements. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Eliminer les zéros de début ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée, un <span class="uicontrol"> </span> <span class="uicontrol"> </span> élément Champ de plage est sélectionné et une valeur de précision non nulle a été définie. </p> <p>Doit-on afficher "0,50" comme ".50" ? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Éliminer les zéros de fin ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée, un <span class="uicontrol"> </span> <span class="uicontrol"> </span> élément Champ de plage est sélectionné et une valeur de précision non nulle a été définie. </p> <p>Doit-on afficher "10.00" comme "10" ? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afficher des milliers de séparateurs ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Devrions-nous afficher "10 000" comme "10 000" ? Des valeurs propres aux paramètres régionaux seront utilisées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajuster les valeurs nulles ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Lorsque des valeurs nulles arrondies sont affichées, doivent-elles être arrondies vers le haut ou vers le bas selon le paramètre <span class="uicontrol"> Précision </span> ? Par exemple, afficher "0.01" ? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Testez en utilisant le paramètre Plus grand que ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Chaque valeur étant comparée aux valeurs des <span class="uicontrol"> valeurs de la plage </span>, traitées dans l’ordre <i><b>décroissant</b></i> , elle est comparée, par défaut, à l’aide de l’opérateur Plus grand que ou égal (&gt;=), en s’arrêtant une fois ce test réussi. Cela signifie qu’avec un ensemble de valeurs de <span class="uicontrol"> plage </span> comme "10 20 50 100 1 000", la valeur 100 tombera dans la plage 100 à 1 000, car 100 est en effet &gt;= 100. Si vous préférez qu’il tombe dans la plage 50 à 100, cochez cette option, ce qui entraînera l’utilisation de l’opérateur Plus grand que (&gt;) par les comparaisons. </p> <p>Par exemple, pour chacune des valeurs de ce champ, lorsque cette option est cochée : 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">si la valeur est inférieure ou égale à (&lt;=) la valeur la plus petite dans <span class="uicontrol"> les valeurs de plage </span>, le format <span class="uicontrol"> "Inférieur à" </span> sera utilisé. </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">si la valeur est supérieure à (&gt;) la valeur la plus élevée dans <span class="uicontrol"> les valeurs de plage </span>, le format <span class="uicontrol"> "Supérieur à" </span> sera utilisé. </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">dans le cas contraire, une plage est trouvée lorsque la valeur du champ est comprise entre deux valeurs <span class="uicontrol"> de plage consécutives </span> (supérieures ou égales à (&gt;=) la valeur la plus petite et inférieure à (&lt;) la valeur la plus élevée), et le <span class="uicontrol"> format intermédiaire </span> est utilisé. </li> 
    </ul> </p> <p>et, lorsqu’elle est désactivée : 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">si la valeur est inférieure à (&lt;) la valeur la plus petite dans <span class="uicontrol"> les valeurs de plage </span>, le format <span class="uicontrol"> "Inférieur à" </span> sera utilisé. </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">si la valeur est supérieure ou égale à (&gt;=) la valeur la plus élevée dans <span class="uicontrol"> les valeurs de plage </span>, le format <span class="uicontrol"> "Supérieur à" </span> sera utilisé. </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">dans le cas contraire, une plage est trouvée lorsque la valeur du champ est comprise entre deux valeurs <span class="uicontrol"> de plage consécutives </span> (supérieures à (&gt;) la valeur la plus petite et inférieure ou égale à (&lt;=) la valeur la plus élevée) et le <span class="uicontrol"> format intermédiaire </span> est utilisé. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer une description de plage </span> est cochée et qu’un <span class="uicontrol"> </span> élément Champ de plage est sélectionné. </p> <p>Fournissez un exemple de valeur numérique et appuyez sur le <span class="uicontrol"> bouton </span> Tester pour voir comment le champ de plage est créé. La description de la plage générée s’affiche dans la fenêtre. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Voir aussi [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.
1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Recréez l’index du site d’évaluation si vous souhaitez prévisualiser les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.
1. (Facultatif) Sur la [!DNL Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification des champs de métadonnées prédéfinis ou définis par l’utilisateur {#task_0A7657B63596421BB6DB3ED44F827AB3}

Vous ne pouvez modifier que certains champs des balises meta prédéfinies ou modifier tous les champs des balises meta définies par l’utilisateur.

Avant que les effets de vos modifications de balise meta ne soient visibles par les clients, vous devez recréer l’index de votre site.

**Pour modifier des champs de métadonnées prédéfinis ou définis par l’utilisateur**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Sur la [!DNL Definitions] page, dans la [!DNL Actions] colonne du tableau, cliquez **[!UICONTROL Edit]** dans la ligne du nom du champ de balise meta que vous souhaitez modifier.
1. Sur la [!DNL Pinned Keyword Results Manager] page, dans le tableau, cliquez **[!UICONTROL Edit]** dans la ligne du mot-clé à modifier.
1. Sur la [!DNL Edit Field] page, définissez les options de votre choix.

   Si vous choisissez d’apporter des modifications à un champ de balise meta prédéfini, sachez que tous les champs ne sont pas modifiables.

   Voir le tableau des options sous [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index du site d’évaluation si vous souhaitez prévisualiser les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.
1. (Facultatif) Sur la [!DNL Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’un champ de balise meta défini par l’utilisateur {#task_9361EF38B5E743038B6672FA6CF70FD3}

Vous pouvez supprimer un champ de balise meta défini par l’utilisateur que vous n’avez plus besoin d’utiliser.

Vous ne pouvez pas supprimer les champs de balise meta prédéfinis. Vous pouvez toutefois modifier certains champs.

Voir [Modification de champs](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3)de balise meta prédéfinis ou définis par l’utilisateur.

Avant que les effets de votre balise meta de suppression ne soient visibles par les clients, vous devez recréer l’index de votre site.

**Pour supprimer un champ de balise meta défini par l’utilisateur**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Sur la [!DNL Definitions] page, dans la [!DNL User-defined fields] section du tableau, cliquez **[!UICONTROL Delete]** sur la ligne du nom du champ de balise meta à supprimer.
1. Dans la boîte de dialogue Confirmation, cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Recréez l’index du site d’évaluation si vous souhaitez prévisualiser les résultats.

   Voir [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.
1. (Facultatif) Sur la [!DNL Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des injections {#concept_DA091920671948A0A893A26B3A2FAAE5}

Vous pouvez les utiliser [!DNL Injections] pour insérer du contenu dans vos pages Web sans avoir à modifier les pages elles-mêmes.

Vous pouvez ajouter du contenu à des champs indexés spécifiques, tels que &quot;target&quot; ou &quot;body&quot;, ou remplacer le contenu indexé par de nouvelles valeurs. Si, par exemple, vous avez inséré un nouveau contenu dans le champ de balise meta &quot;target&quot;, ces informations sont traitées de la même manière que le contenu de la page codée en dur. Vous pouvez modifier le contenu de tout champ de balise meta prédéfini, que les pages de votre site contiennent ou non le contenu correspondant. Par exemple, vous pouvez modifier le contenu des noms de champ de balise meta prédéfinis suivants :

* alt
* body
* charset
* date
* desc
* clés
* language
* cible
* title
* url

## Utilisation des injections de champ de test {#section_74939EA9E6EA4D2A92E8066B3B11CF92}

Vous pouvez éventuellement l’utiliser **[!UICONTROL Test]** sur la [!DNL Staged Injections] page. Vous saisissez un nom de champ de test (par exemple, &quot;titre&quot; ou &quot;corps&quot;), la valeur de champ d’origine (par exemple, &quot;Page d’accueil&quot;) et une URL de test de votre site Web. La valeur résultante est affichée pour votre référence. Les valeurs actuelles ne sont pas modifiées pendant le test.

## Utilisation des définitions d’injection de champ {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

Les définitions d’injection se présentent sous la forme suivante :

```
append|replace field [regexp] URL value
```

The `append|replace`, `field`, `URL`. et `value` les éléments sont obligatoires. Vous entrez une définition d’injection par ligne. L’exemple suivant contient six définitions d’injection différentes.

```
replace title  https://www.yoursite.com/company/contactus.html Adobe: Contact Us 
append body https://www.yoursite.com/products/* On Sale Now! 
append target https://www.yoursite.com/news/bob_white/ Regular Weekly Feature 
append target regexp https://www.yoursite.com/travel/mr_travel/.*\column.html$ Regular Weekly Feature 
replace charset https://www.yoursite.com/japanese/intro.txt shift-jis 
replace language https://www.yoursite.com/japanese/intro.txt ja_JP
```

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Définition d’injection </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> append|replace </span> </p> </td> 
   <td colname="col2"> <p>Choisissez "annexer" pour ajouter la valeur de la définition d’injection ("Adobe : Contactez-nous" ou "En vente maintenant" ! dans les exemples ci-dessus) au contenu des champs existants. Choisissez "Remplacer" pour remplacer le contenu du champ existant par la valeur définie. Si un champ ne comporte actuellement aucun contenu, la valeur définie est ajoutée automatiquement, quelle que soit l’option utilisée (ajouter ou remplacer). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> champ </span> </p> </td> 
   <td colname="col2"> <p>Un nom de champ est requis. Vous trouverez ci-dessous dix noms de champ prédéfinis que vous pouvez utiliser : </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> alt </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> clés </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> cible </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> titre </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>Chaque nom de champ correspond aux éléments des pages de votre site. Si vous spécifiez le nom du champ <span class="codeph"> desc </span> , par exemple, vous pouvez ajouter la valeur de définition de l’injection au champ qui correspond à la description des balises Meta sur les pages de votre site. </p> <p>S’il n’existe aucune balise Meta de description sur vos pages, le contenu défini crée la balise pour vous. Le contenu spécifié dans une injection <span class="codeph"> desc </span> s’affiche sur votre page de résultats tout comme le contenu de la méta-description codée en dur. </p> <p>Vous pouvez également créer plusieurs définitions avec le même nom de champ. Par exemple, supposons que vous ayez les injections suivantes : </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>Toutes les pages du site dans l'exemple ci-dessus reçoivent un titre injecté "Bienvenue sur mon site". Les pages du dossier "/company/" sont injectées avec un nouveau titre "Mon site : Nous contacter" qui remplace la précédente. </p> <p>Les injections sont appliquées dans l’ordre dans lequel elles apparaissent dans la zone de <span class="wintitle"> texte Définitions des injections de champ </span> . Si le même champ ("titre" dans cet exemple) est défini plusieurs fois pour les pages situées au même emplacement, la définition ultérieure est prioritaire. </p> <p> <span class="codeph"> [regexp] </span> - facultatif. Si vous choisissez d’utiliser l’option <span class="codeph"> regexp </span> , l’URL définie est traitée comme une expression régulière. </p> <p>Voir <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> <p>Dans la définition suivante : </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "Informations importantes" est injecté dans le champ "cible" sur toutes les pages qui correspondent à l’expression régulière <span class="codeph"> ^.*/products/.*\.html$ </span>. </p> <p>Par conséquent, vous disposez des éléments suivants : </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>Dans l’exemple suivant : </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>L'injection ajoute "Millennium Science" au contenu "title" de toutes les pages qui se terminent par une extension de nom de fichier ".pdf". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>Une URL est requise et spécifie les documents à injecter. </p> <p>L’URL est l’une des suivantes : </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> Un chemin complet, comme dans https://www.mydomain.com/products.html </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> Un chemin partiel, comme dans https://www.mydomain.com/products </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> URL qui utilise des caractères génériques, comme dans https://www.mydomain.com/*.html </li> 
     </ul> </p> <p>La valeur URL ne doit pas comporter d’espace. Si l’option <span class="codeph"> regexp </span> est utilisée, l’URL est traitée comme une expression régulière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Une valeur est requise et est utilisée pour remplacer ou ajouter du contenu de champ existant. Vous pouvez spécifier plusieurs valeurs pour le même nom de champ. Par exemple : </p> <p>ajouter des <b>clés</b> https://www.mysite.com/travel/ <b>été</b>, <b>plage</b>, <b>sable</b> </p> <p>ajouter des <b>clés</b> https://www.mysite.com/travel/fare/*.html billets <b>bon marché</b> </p> <p>Dans l’exemple ci-dessus, les mots "été, plage, sable" sont ajoutés au champ "clés" sur toutes les pages du répertoire "/travel/". Les mots "billets bon marché" sont également ajoutés au champ "clés" sur toutes les pages du répertoire "/travel/fare/". </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [Sélection de types de contenu à analyser et à indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

## Ajout de définitions d’injection de champ {#task_E86566FA1FF74CF68115C0ADA05172AE}

Vous pouvez les utiliser [!DNL Injections] pour insérer du contenu dans vos pages Web sans avoir à modifier les pages elles-mêmes.

Vous pouvez éventuellement l’utiliser **[!UICONTROL Test]** sur la [!DNL Injections] page. Vous saisissez un nom de champ de test (par exemple, &quot;titre&quot; ou &quot;corps&quot;), la valeur de champ d’origine (par exemple, &quot;Page d’accueil&quot;) et une URL de test de votre site Web. La valeur résultante est affichée pour votre référence. Les valeurs actuelles ne sont pas modifiées pendant le test.

**Pour ajouter des définitions d’injection de champ**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**.
1. (Facultatif) Sur la [!DNL Injections] page, dans la [!DNL Test Field Injections] zone, saisissez le champ de test, la valeur d’origine du test et l’URL du test, puis cliquez sur **[!UICONTROL Test]**.
1. Dans le [!DNL Field Injection Definitions] champ, entrez une définition d’injection par ligne.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos du chargeur d’attributs {#concept_9EF38E98811B42CDA41996432B9AD209}

Utilisez [!DNL Attribute Loader] pour définir d’autres sources d’entrée afin d’augmenter les données analysées à partir d’un site Web.

>[!NOTE]
>
>Pour utiliser Attribute Loader, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe.

Vous pouvez utiliser une source d’entrée de flux de données pour accéder au contenu stocké dans un formulaire différent de ce qui est généralement découvert sur un site Web. Pour ce faire, utilisez l’une des méthodes d’analyse disponibles. Les données provenant de ces sources peuvent ensuite être injectées dans les données issues du contenu analysé.

Après avoir ajouté une définition de chargeur d’attributs à la [!DNL Staged Attribute Loader Definitions] page, vous pouvez modifier n’importe quel paramètre de configuration, à l’exception des valeurs Nom et Type.

La [!DNL Attribute Loader] page affiche les informations suivantes :

* Nom de la configuration du chargeur d’attributs définie que vous avez configurée et ajoutée.
* L’un des types de source de données suivants pour chaque connecteur que vous avez ajouté :

   * **Texte** - Fichiers simples &quot;plats&quot;, délimités par des virgules, délimités par des tabulations ou autres formats délimités de manière cohérente.
   * **Flux** - Flux XML.

* Indique si la configuration est activée ou non pour l’analyse et l’indexation suivantes.
* Adresse de la source de données.

Voir aussi [Comment le processus d’injection d’attributs fonctionne pour le texte et le flux...](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

Voir aussi [A propos de la configuration de plusieurs chargeurs d’attributs](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

Voir aussi [A propos de l’utilisation de l’aperçu lorsque vous ajoutez un attribut...](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## Mode de fonctionnement du processus d’injection d’attributs pour les configurations de texte et de flux dans le chargeur d’attributs {#section_E059A33D61EE4DB0972A37B8A35E9E16}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Étape </p> </th> 
   <th colname="col2" class="entry"> <p>Processus </p> </th> 
   <th colname="col3" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>1 </p> </td> 
   <td colname="col2"> <p>Téléchargez la source de données. </p> </td> 
   <td colname="col3"> <p>Pour les configurations de texte et de flux, il s’agit d’un téléchargement de fichier simple. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Ventilez la source de données téléchargée en pseudo-documents individuels. </p> </td> 
   <td colname="col3"> <p>Pour <span class="uicontrol"> Texte </span>, chaque nouvelle ligne de texte délimité par une ligne correspond à un document individuel et est analysée à l’aide du délimiteur spécifié, tel qu’une virgule ou un tabulation. </p> <p>Pour le <span class="uicontrol"> flux </span>, les données de chaque document sont extraites à l’aide d’un modèle d’expression régulière sous la forme suivante : </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>A l’aide de <span class="uicontrol"> Map </span> sur la page <span class="wintitle"> Attribute Loader Add </span> , créez une copie mise en cache des données, puis créez une liste de liens pour le moteur de recherche. Les données sont stockées dans un cache local et renseignées avec les champs configurés. </p> <p>Les données analysées sont écrites dans le cache local. </p> <p>Cette mémoire cache est lue ultérieurement pour créer les documents HTML simples dont a besoin l’analyseur. Par exemple : </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>L’élément <span class="codeph"> &lt;title&gt; </span> n’est généré que lorsqu’il existe un mappage au champ de métadonnées Titre. De même, l’élément <span class="codeph"> &lt;body&gt; </span> n’est généré que lorsqu’il existe un mappage au champ de métadonnées Body. </p> <p> <b>Important</b>: L’affectation de valeurs à la balise meta d’URL prédéfinie n’est pas prise en charge. </p> <p>Pour tous les autres mappages, <span class="codeph"> &lt;meta&gt; </span> balises sont générées pour chaque champ contenant des données dans le document d’origine. </p> <p>Les champs de chaque document sont ajoutés au cache. Pour chaque document écrit dans le cache, un lien est également généré, comme dans les exemples suivants : </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>Le mappage de la configuration doit comporter un champ identifié comme clé principale. Ce mappage forme la clé utilisée lorsque les données sont extraites du cache. </p> <p>L’analyseur reconnaît l’index d’URL <span class="codeph"> : préfixe </span> de schéma, qui peut ensuite accéder aux données mises en cache localement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Analyse du jeu de documents mis en cache. </p> </td> 
   <td colname="col3"> <p>Index <span class="codeph"> : </span> les liens sont ajoutés à la liste des liens en attente de l’analyseur et sont traités dans la séquence d’analyse normale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>4 </p> </td> 
   <td colname="col2"> <p>Traitez chaque document. </p> </td> 
   <td colname="col3"> <p>La valeur de clé de chaque lien correspond à une entrée dans le cache. L’analyse de chaque lien entraîne la récupération des données de ce document à partir du cache. Il est ensuite "assemblé" dans une image HTML qui est traitée et ajoutée à l’index. </p> </td> 
  </tr> 
 </tbody> 
</table>

## A propos de la configuration de plusieurs chargeurs d’attributs {#section_4CC49C74EF294608A184E233F215ADFF}

Vous pouvez définir plusieurs configurations de chargeur d’attributs pour n’importe quel compte.

Lorsque vous ajoutez un chargeur d’attributs, vous pouvez éventuellement utiliser cette fonction **[!UICONTROL Setup Maps]** pour télécharger un exemple de source de données. Les données sont examinées pour déterminer si elles sont appropriées.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> Type de chargeur d’attributs </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Texte </p> </td> 
   <td colname="col2"> <p>Détermine la valeur du délimiteur en essayant d’abord d’utiliser des tabulations, puis des barres verticales ( <span class="codeph"> | </span>) et enfin des virgules ( <span class="codeph"> , </span>). Si vous avez déjà spécifié une valeur de délimiteur avant de cliquer sur <span class="uicontrol"> Configurer les zones </span>, cette valeur est utilisée à la place. </p> <p>Le modèle adapté permet de remplir les champs de zone cliquable avec des estimations aux valeurs de balise et de champ appropriées. En outre, un échantillon des données analysées s’affiche. Veillez à sélectionner <span class="uicontrol"> En-têtes dans la première rangée </span> si vous savez que le fichier contient une rangée d’en-tête. La fonction de configuration utilise ces informations pour mieux identifier les entrées de mappage résultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flux </p> </td> 
   <td colname="col2"> <p>Télécharge la source de données et effectue une analyse XML simple. </p> <p>Les identifiants XPath résultants s’affichent dans les lignes Balise du tableau de mappage, et des valeurs similaires dans les champs. Ces lignes identifient uniquement les données disponibles et ne génèrent pas les définitions XPath les plus complexes. Cependant, il reste utile car il décrit les données XML et identifie le balisage d’élément. </p> <p> <p>Remarque :  La fonction Setup Maps télécharge la source XML entière pour effectuer son analyse. Si le fichier est volumineux, cette opération peut expirer. </p> </p> <p>En cas de succès, cette fonction identifie tous les éléments XPath possibles, dont beaucoup ne sont pas souhaitables. Vérifiez que vous examinez les définitions de zone cliquable résultantes et supprimez celles dont vous n’avez pas besoin ou que vous ne souhaitez pas. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La fonction Setup Maps (Mappages de configuration) peut ne pas fonctionner pour les jeux de données XML volumineux, car l’analyseur de fichiers tente de lire l’intégralité du fichier en mémoire. Par conséquent, vous pourriez rencontrer une situation de mémoire insuffisante. Cependant, lorsque le même document est traité au moment de l’indexation, il n’est pas lu en mémoire. Au lieu de cela, les documents volumineux sont traités &quot;en déplacement&quot; et ne sont pas lus entièrement en mémoire.

## A propos de l’utilisation de l’aperçu lorsque vous ajoutez un chargeur d’attributs {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

Les données du chargeur d’attributs sont chargées avant une opération d’index.

Lorsque vous ajoutez un chargeur d’attributs, vous pouvez éventuellement utiliser la fonctionnalité **[!UICONTROL Preview]** pour valider les données, comme si vous les aviez enregistrées. Il exécute un test par rapport à la configuration, mais sans enregistrer la configuration dans le compte. Le test accède à la source de données configurée. Toutefois, il écrit le cache de téléchargement à un emplacement temporaire ; il n’est pas en conflit avec le dossier cache principal utilisé par l’analyseur d’indexation.

Aperçu traite uniquement un document par défaut de cinq, comme le contrôle **Acct:IndexConnector-Preview-Max-Documents**. Les documents prévisualisés s’affichent sous forme source, dans la mesure où ils sont présentés au moteur d’indexation. L&#39;affichage est similaire à une fonction &quot;Afficher la source&quot; dans un navigateur Web. Vous pouvez parcourir les documents du jeu d’aperçu à l’aide de liens de navigation standard.

L’aperçu ne prend pas en charge les configurations XML, car ces documents sont traités directement et ne sont pas téléchargés dans le cache.

## Ajout d’une définition de chargeur d’attributs {#task_A735E5EF763343A9B675E1A3B09AFDBC}

Chaque configuration du chargeur d’attributs définit une source de données et des mappages pour relier les éléments de données définis pour cette source aux champs de métadonnées de l’index.

>[!NOTE]
>
>Pour utiliser Attribute Loader, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe.

Avant que les effets de la nouvelle définition activée ne soient visibles par les clients, recréez l’index de votre site.

**Pour ajouter une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Stage Attribute Loader Definitions] page, cliquez sur **[!UICONTROL Add New Attribute Loader]**.
1. Dans la [!DNL Attribute Loader Add] page, définissez les options de configuration de votre choix. Les options disponibles dépendent de l’option **[!UICONTROL Type]** sélectionnée.

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Nom </p> </td> 
      <td colname="col2"> <p>Nom unique de la configuration du chargeur d’attributs. Vous pouvez utiliser des caractères alphanumériques. Les caractères "_" et "-" sont également autorisés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>Source de vos données. Le type de source de données que vous sélectionnez affecte les options résultantes disponibles sur la page Ajouter un chargeur d’ <span class="wintitle"> attributs </span> . Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texte </span> <p>Fichiers de texte aplati simples, formats délimités par des virgules, tabulés ou autres formats délimités de manière cohérente. Chaque ligne de texte délimité par une nouvelle ligne correspond à un document individuel et est analysée à l’aide du délimiteur spécifié. </p> <p>Vous pouvez mapper chaque valeur, ou colonne, à un champ de métadonnées, référencé par le numéro de colonne, en commençant par 1 (un). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Flux </span> <p>Télécharge un document XML maître contenant plusieurs "lignes" d’informations. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Texte</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active la configuration en vue de l’utiliser. Vous pouvez également désactiver la configuration pour empêcher l’utilisation de cette dernière. </p> <p> <b>Remarque</b>: Les configurations du chargeur d’attributs désactivées sont ignorées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse de l’hôte du serveur où se trouvent vos données. </p> <p>Si vous le souhaitez, vous pouvez spécifier un chemin d’accès URI complet (Uniform Resource Identifier) au document de source de données, comme dans les exemples suivants : </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>ou </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>L’URI est ventilé selon les entrées appropriées pour les champs Adresse hôte, Chemin du fichier, Protocole et, éventuellement, Nom d’utilisateur et Mot de passe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Indique le chemin d’accès au fichier de texte plat simple, délimité par des virgules, délimité par des tabulations ou à un autre fichier de format délimité de manière cohérente. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Spécifie le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Si nécessaire, vous pouvez entrer les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Expiration </p> </td> 
      <td colname="col2"> <p>Spécifie le délai d’expiration, en secondes, pour les connexions FTP, SFTP, HTTP ou HTTPS. Cette valeur doit être comprise entre 30 et 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Reprises </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal de tentatives pour les connexions FTP, SFTP, HTTP ou HTTPS ayant échoué. Cette valeur doit être comprise entre 0 et 10. </p> <p>Une valeur nulle (0) empêche les tentatives de nouvelle tentative. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Encodage </p> </td> 
      <td colname="col2"> <p>Spécifie le système de codage de caractères utilisé dans le fichier de source de données spécifié. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Délimiteur </p> </td> 
      <td colname="col2"> <p>Indique le caractère à utiliser pour délimiter chaque champ du fichier de source de données spécifié. </p> <p>La virgule ( <span class="codeph"> , </span>) est un exemple de délimiteur. La virgule agit comme un délimiteur de champ qui permet de séparer les champs de données dans le fichier de source de données spécifié. </p> <p>Sélectionner un <span class="uicontrol"> onglet ? </span> pour utiliser le caractère de tabulation horizontale comme délimiteur. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>En-têtes de première ligne </p> </td> 
      <td colname="col2"> <p>Indique que la première ligne du fichier de source de données contient uniquement des informations d’en-tête et non des données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Jours périmés </p> </td> 
      <td colname="col2"> <p>Définit l’intervalle minimal entre les téléchargements des données du chargeur d’attributs. Les téléchargements déclenchés par index qui se produisent dans l’intervalle de fréquence d’actualisation des téléchargements sont ignorés. Lorsque vous définissez cette valeur sur la valeur par défaut 1, les données du chargeur d’attributs ne sont pas téléchargées plusieurs fois au cours d’une période de 24 heures. Tous les index de recherche qui surviennent dans l’intervalle de fréquence d’actualisation des téléchargements utilisent le dernier jeu de données téléchargé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Indique les mappages colonne/métadonnées, à l’aide des numéros de colonne. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Colonne </span> <p> Spécifie un numéro de colonne, la première colonne étant 1 (un). Pour ajouter de nouvelles lignes de mappage pour chaque colonne, sous <span class="wintitle"> Action </span>, cliquez sur <span class="uicontrol"> + </span>. </p> <p>Il n’est pas nécessaire de référencer chaque colonne de la source de données. Vous pouvez plutôt choisir d’ignorer les valeurs. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Champ </span> <p>Définit la valeur d’attribut name utilisée pour chaque balise &lt;meta&gt; générée. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> devient une liste déroulante </span> à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actuel. </p> <p>La <span class="uicontrol"> valeur </span> de champ peut être un champ de métadonnées non défini, le cas échéant. Un champ de métadonnées non défini est parfois utile pour créer le contenu utilisé par un <span class="wintitle"> script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> A propos du filtrage de script </a>. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Clé primaire? </span> <p>Un seul champ est identifié comme clé principale. Ce champ sera utilisé comme "clé étrangère" pour faire correspondre les données du chargeur d’attributs au document correspondant dans l’index. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> Bande du code HTML ? </span> <p>Lorsque cette option est cochée, toutes les balises HTML trouvées dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Action </span> <p>Permet d’ajouter des lignes au mappage ou de supprimer des lignes du mappage. L’ordre des rangées n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Flux</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active la configuration en vue de l’utiliser. Vous pouvez également désactiver la configuration pour empêcher l’utilisation de cette dernière. </p> <p> <b>Remarque</b>: Les configurations du chargeur d’attributs désactivées sont ignorées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse de l’hôte du serveur où se trouvent vos données. </p> <p>Si vous le souhaitez, vous pouvez spécifier un chemin d’accès URI complet (Uniform Resource Identifier) au document de source de données, comme dans les exemples suivants : </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>ou </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>L’URI est ventilé selon les entrées appropriées pour les champs Adresse hôte, Chemin du fichier, Protocole et, éventuellement, Nom d’utilisateur et Mot de passe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML maître qui contient plusieurs "lignes" d’informations. </p> <p>Le chemin est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Spécifie le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Si nécessaire, vous pouvez entrer les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Vous devez entrer les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifie l’élément XML que vous pouvez utiliser pour identifier des lignes XML individuelles dans le fichier de source de données que vous avez spécifié. </p> <p>Par exemple, dans le fragment Flux suivant d’un document Adobe XML, la valeur Itemtag est <span class="codeph"> record </span>: </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
        &lt;!DOCTYPE&nbsp;gsafeed&nbsp;PUBLIC&nbsp;"-//Google//DTD&nbsp;GSA&nbsp;Feeds//EN"&nbsp;""&gt; 
        &lt;gsafeed&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;datasource&gt;marketplace&lt;/datasource&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;feedtype&gt;incremental&lt;/feedtype&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/header&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;group&nbsp;action="add"&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=1&nbsp;action="add"&nbsp;mimetype="text/html"displayurl="https://www.adobe.com/cfusion/marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=1"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="1"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_air.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;AIR&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Discover&nbsp;new&nbsp;applications&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;AIR&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Discover&nbsp;new&nbsp;applications&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;&lt;/cntent&gt; 
        &lt;/record&gt; 
        &lt;record&nbsp;url=https://www.adobe.com/cfusion/marketplace_gsa/ 
        index.cfm?event=marketplace.home&amp;amp;marketplaceid=2&nbsp;action="add"&nbsp;mimetype="text/html"&nbsp;displayurl="https://www.adobe.com/cfusion/ 
        marketplace/index.cfm?event=marketplace.home&amp;amp;marketplaceid=2"&gt; 
        &lt;metadata&gt; 
        &lt;meta&nbsp;name="mp_mkt"&nbsp;content="2"/&gt; 
        &lt;meta&nbsp;name="mp_logo"&nbsp;content="/images/marketplace/ 
        dbreferenced/marketplaceicons/icn_photoshop.png"/&gt; 
        &lt;meta&nbsp;name="title"&nbsp;content="Adobe&nbsp;Photoshop&nbsp;Marketplace"/&gt; 
        &lt;meta&nbsp;name="description"&nbsp;content="Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;..."/&gt; 
        &lt;/metadata&gt; 
        &lt;content&gt;&lt;![CDATA[&lt;html&gt;&lt;head&gt;&lt;title&gt;Adobe&nbsp;Photoshop&nbsp;Marketplace&lt;/title&gt;&lt;/head&gt;&lt;body&gt;Extend&nbsp;your&nbsp;creative&nbsp;possibilities&nbsp;...&lt;/body&gt;&lt;/html&gt;]]&gt;/content&gt; 
        &lt;/record&gt; 
        ... 
        &lt;record&gt; 
        ... 
        &lt;/record&gt; 
        &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&lt;/group&gt; 
        &lt;/gsafeed&gt; 
        </code> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du champ de référence croisée </p> </td> 
      <td colname="col2"> <p>Spécifie un champ de métadonnées dont les valeurs sont utilisées comme "clés" de recherche dans les données de la configuration du chargeur d’attributs. Si aucune valeur n’est sélectionnée (<b>—Aucun—</b>), les données de cette configuration ne sont pas disponibles pour les calculs de classement (<b>Règles</b> &gt; Règles <b>de</b> classement &gt; <b>Modifier les règles). </b> Lorsque vous sélectionnez une valeur, les valeurs de ce champ sont utilisées pour référencer les documents de recherche/marchandisage de site avec les données de cette configuration. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Jours périmés </p> </td> 
      <td colname="col2"> <p>Définit l’intervalle minimal entre les téléchargements des données du chargeur d’attributs. Les téléchargements déclenchés par index qui se produisent dans l’intervalle de fréquence d’actualisation des téléchargements sont ignorés. Lorsque vous définissez cette valeur sur la valeur par défaut 1, les données du chargeur d’attributs ne sont pas téléchargées plusieurs fois au cours d’une période de 24 heures. Tous les index de recherche qui surviennent dans l’intervalle de fréquence d’actualisation des téléchargements utilisent le dernier jeu de données téléchargé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Permet de spécifier des mappages élément-élément-XML/métadonnées à l’aide d’expressions XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Baliser </span> <p>Spécifie une représentation XPath des données XML analysées. A l’aide de l’exemple de document XML Adobe ci-dessus, sous l’option Itemtag, il peut être mappé à l’aide de la syntaxe suivante : </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La syntaxe ci-dessus se traduit comme suit : </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>L’attribut <span class="codeph"> displayurl </span> de l’ <span class="codeph"> élément d’enregistrement </span> est mappé au champ de métadonnées <span class="codeph"> page-url </span>. </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans un élément de  d’enregistrement, dont l’attribut de nom est  titre , est associé au de titre du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans l’élément de  d’enregistrement, dont l’attribut de nom est  description , correspond au desc du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>L’ <span class="codeph"> attribut </span> de contenu de tout <span class="codeph"> élément </span> de métadonnées contenu contenu dans un <span class="codeph"> </span> <span class="codeph"> élément de métadonnées, contenu dans l’élément de  d’enregistrement, dont l’attribut de nom est  description , correspond au de corps du champ de métadonnées.</span><span class="codeph"></span><span class="codeph"></span> </p> </li> 
        </ul> </p> <p>XPath est une notation relativement compliquée. Pour plus d’informations, consultez l’emplacement suivant : </p> <p>Voir <a href="https://www.w3schools.com/xpath/" scope="external" format="html"> https://www.w3schools.com/xpath/ </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Champ </span> <p>Définit la valeur d’attribut name utilisée pour chaque balise générée <span class="codeph"> &lt;meta&gt; </span> . </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> devient une liste déroulante </span> à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actuel. </p> <p>La <span class="uicontrol"> valeur </span> de champ peut être un champ de métadonnées non défini, le cas échéant. Un champ de métadonnées non défini est parfois utile pour créer le contenu utilisé par <span class="wintitle"> le script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> A propos du filtrage de script </a>. </p> <p>Lorsque le chargeur d’attributs traite des documents XML avec plusieurs accès sur un champ de mappage, les valeurs multiples sont concaténées en une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur de virgule. Cependant, supposons que la <span class="wintitle"> valeur de champ correspondante </span> soit un champ de métadonnées défini. En outre, ce champ a l’ <span class="wintitle"> attribut Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Clé primaire? </span> <p>Un seul champ est identifié comme clé principale. Ce champ sera utilisé comme "clé étrangère" pour faire correspondre les données du chargeur d’attributs au document correspondant dans l’index. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> Bande du code HTML ? </span> <p>Lorsque cette option est cochée, toutes les balises HTML trouvées dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Action </span> <p>Permet d’ajouter des lignes au mappage ou de supprimer des lignes du mappage. L’ordre des rangées n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Cliquez sur **[!UICONTROL Setup Maps]** pour télécharger un exemple de source de données. Les données sont examinées pour déterminer si elles sont appropriées.
1. Cliquez sur **[!UICONTROL Add]** pour ajouter la configuration à la [!DNL Attribute Loader Definitions] page.
1. Sur la [!DNL Attribute Loader Definitions] page, cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la [!DNL Attribute Loader Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une définition de chargeur d’attributs {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

Vous pouvez modifier un chargeur d’attributs existant que vous avez défini.

>[!NOTE]
>
>Pour utiliser Attribute Loader, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe.

Vous ne pouvez pas modifier toutes les options du chargeur d’attributs, telles que le nom du chargeur d’attributs ou le type dans la liste [!DNL Type] déroulante.

**Pour modifier une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Edit]** sur le nom de définition d’un chargeur d’attributs dont vous souhaitez modifier les paramètres.
1. Sur la [!DNL Attribute Loader Edit] page, définissez les options de votre choix.

   Voir le tableau des options sous [Ajout d’une définition](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC)de chargeur d’attributs.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la [!DNL Attribute Loader Definitions] page, cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la [!DNL Attribute Loader Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copie d’une définition de chargeur d’attributs {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

Vous pouvez copier une définition de chargeur d’attributs existante pour l’utiliser comme base d’un nouveau chargeur d’attributs que vous souhaitez créer.

>[!NOTE]
>
>Pour utiliser Attribute Loader, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe.

Lors de la copie d’une définition de chargeur d’attributs, la définition copiée est désactivée par défaut. Pour activer ou &quot;activer&quot; la définition, vous devez la modifier à partir de la [!DNL Attribute Loader Edit] page, puis sélectionner **[!UICONTROL Enable]**.

Voir [Modification d’une définition](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80)de chargeur d’attributs.

**Pour copier une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Copy]** sur le nom de définition d’un chargeur d’attributs dont vous souhaitez dupliquer les paramètres.
1. Sur la [!DNL Attribute Loader Copy] page, saisissez le nouveau nom de la définition.
1. Cliquez sur **[!UICONTROL Copy]**.
1. (Facultatif) Sur la [!DNL Attribute Loader Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification du nom d’une définition de chargeur d’attributs {#task_58D5DFD7EBC04111BCB91118E4440DB4}

Vous pouvez modifier le nom d’une définition existante du chargeur d’attributs.

>[!NOTE]
>
>Pour utiliser Attribute Loader, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe.

**Pour renommer une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Rename]** pour le nom de définition du chargeur d’attributs que vous souhaitez modifier.
1. Sur la [!DNL Attribute Loader Rename] page, saisissez le nouveau nom de la définition dans le [!DNL Name] champ.
1. Cliquez sur **[!UICONTROL Rename]**.
1. (Facultatif) Sur la [!DNL Attribute Loader Definitions] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Chargement des données du chargeur d’attributs {#task_2F3C55189B0A4049AB2113F2291CC181}

Vous pouvez télécharger les données du chargeur d’attributs configuré dans la recherche/marchandisage de site.

La [!DNL Data Load] page affiche les informations suivantes sur l’état de votre dernière opération de chargement des données du chargeur d’attributs :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Champ État </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>État </p> </td> 
   <td colname="col2"> <p>Indique la réussite ou l’échec de la dernière tentative de chargement des données. Il affiche également l’état d’une opération de chargement de données déjà en cours. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Heure de début </p> </td> 
   <td colname="col2"> <p>Affiche la date et l’heure auxquelles la dernière opération de chargement de données a commencé. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Heure d’arrêt </p> </td> 
   <td colname="col2"> <p>Affiche la date et l’heure de fin de la dernière opération de chargement de données. Ou indique que l’opération de chargement de données en cours est toujours en cours. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Pour charger les données du chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader Definitions] page, cliquez sur **[!UICONTROL Load Attribute Loader Data]**.
1. Sur la **[!UICONTROL Attribute Loader Data Load]** page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Start Load]** pour lancer l’opération de chargement.

      Au cours d’une opération de chargement de données,**la ligne Progression** fournit des informations sur sa progression.

   * Cliquez sur **[!UICONTROL Stop Load]** pour arrêter l’opération de chargement.

1. Cliquez sur **[!UICONTROL Close]** pour revenir à la [!DNL Attribute Loader Definitions] page.

## Prévisualisation des données du chargeur d’attributs {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Vous pouvez utiliser la fonction Aperçu pour afficher vos dernières données de chargeur d’attributs chargées.

La colonne Ligne du tableau indique le nombre de chaque ligne de données, indiquant l’ordre initial dans lequel les valeurs du chargeur d’attributs ont été chargées.

Les autres colonnes affichent les valeurs associées à chaque entrée.

Si le tableau est vide, cela signifie que vous n’avez encore chargé aucune donnée de chargeur d’attributs. Vous pouvez fermer la [!DNL Attribute Loader Data Preview] page, puis charger les données du chargeur d’attributs.

Voir [Chargement des données](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)du chargeur d’attributs.

**Pour prévisualiser les données du chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader Definitions] page, sous la [!DNL Actions] colonne, cliquez **[!UICONTROL Preview]** sur la configuration dont vous voulez afficher les données téléchargées.
1. Sur la [!DNL Attribute Loader Data Preview] page, utilisez les options de navigation et d’affichage en haut et en bas de la page pour afficher les données.

   Cliquez sur un en-tête de colonne du tableau pour trier les données par ordre croissant ou décroissant.
1. Utilisez l’une des méthodes suivantes :

   * Cliquez sur **[!UICONTROL Download to Desktop]** pour télécharger et enregistrer le tableau dans un fichier .xlt.
   * Fermez la page lorsque vous avez terminé de prévisualiser les données du chargeur d’attributs et revenez à la page précédemment affichée.

## Affichage des paramètres d’une définition de chargeur d’attributs {#task_EA99A9694FE948ADA82C1DBA0667851B}

Vous pouvez consulter les paramètres de configuration d’une définition existante du chargeur d’attributs.

Une fois la définition du chargeur d’attributs ajoutée à la [!DNL Attribute Loader Definitions] page, vous ne pouvez plus modifier son paramètre Type. Vous devez supprimer la définition, puis en ajouter une nouvelle.

>[!NOTE]
>
>Pour utiliser Attribute Loader, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe.

**Pour afficher les paramètres d’une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Edit]** sur le nom de définition d’un chargeur d’attributs dont vous souhaitez vérifier ou modifier les paramètres.

## Affichage du journal à partir du chargement de données le plus récent du chargeur d’attributs {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Vous pouvez utiliser [!DNL View Log] pour examiner le fichier journal des données du chargeur d’attributs du processus de téléchargement le plus récent. Vous pouvez également utiliser la vue Journal pour surveiller un téléchargement en cours d’exécution.

Voir [Chargement des données](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181)du chargeur d’attributs.

**Pour afficher le journal à partir du chargement de données le plus récent du chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader Definitions] page, cliquez sur **[!UICONTROL View Log]**. Page journal,
1. Sur la [!DNL Attribute Loader Data Log] page, utilisez les options de navigation et d’affichage en haut et en bas de la page pour afficher les informations du journal.
1. Lorsque vous avez terminé, fermez la page pour revenir à la [!DNL Attribute Loader Definitions] page.

## Suppression d’une définition de chargeur d’attributs {#task_E8980F66888B476E98C228C1D307EDF8}

Vous pouvez supprimer une définition existante du chargeur d’attributs dont vous n’avez plus besoin ou que vous n’utilisez plus.

>[!NOTE]
>
>Pour utiliser Attribute Loader, vous devrez peut-être l’activer dans votre compte par votre représentant de compte Adobe ou par l’assistance d’Adobe.

**Pour supprimer une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la [!DNL Attribute Loader Definitions] page, sous l’en-tête de [!DNL Actions] colonne, cliquez **[!UICONTROL Delete]** pour le nom de définition du chargeur d’attributs à supprimer.
1. Sur la [!DNL Attribute Loader Delete] page, cliquez sur **[!UICONTROL Delete]**.
