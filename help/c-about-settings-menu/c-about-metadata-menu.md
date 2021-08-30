---
description: Utilisez le menu Métadonnées pour personnaliser les définitions de recherche et les injections d’index.
solution: Target
subtopic: Metadata
title: À propos du menu Métadonnées
topic-legacy: Settings,Site search and merchandising
uuid: f12fc863-a140-45e8-b219-3dbfdef099cd
exl-id: 53d62da9-c5bd-4c4a-bb89-743704f66f7f
source-git-commit: 95bf92df17d7832df72e8d883a22f9063e53a18d
workflow-type: tm+mt
source-wordcount: '8028'
ht-degree: 1%

---

# À propos du menu Métadonnées{#about-the-metadata-menu}

Utilisez le menu Métadonnées pour personnaliser les définitions de recherche et les injections d’index.

## A propos des définitions {#concept_AE48035C210145169BE067D396975620}

Vous pouvez utiliser [!DNL Definitions] pour personnaliser le contenu et la pertinence des champs HTML et de métadonnées pris en compte lorsqu’un client envoie une requête de recherche.

Vous pouvez modifier les champs déjà prédéfinis. Vous pouvez également créer des champs définis par l’utilisateur en fonction du contenu des balises de métadonnées. Chaque définition est affichée sur une seule ligne de la page [!DNL Staged Definitions].

Voir aussi [À propos des vues de données](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

## Ajout d’un nouveau champ de balise META {#task_6DF188C0FC7F4831A4444CA9AFA615E5}

Vous pouvez définir et ajouter vos propres champs de balise de métadonnées.

Avant que les effets de la nouvelle définition de balise META ne soient visibles par les clients, vous devez reconstruire l’index de votre site.

**Pour ajouter un nouveau champ de balise META**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Sur la page [!DNL Definitions], cliquez sur **[!UICONTROL Add New Field]**.
1. Sur la page [!DNL Add Field], définissez les options de votre choix.

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
      <li id="li_7FC340E7C58545C88CE9AF4AF09AD7AD"> Les tirets sont autorisés dans le nom, mais pas d’espaces. </li> 
      <li id="li_996FF38457AB4C6DB22B15850A0830CC"> Vous pouvez saisir un nom de 20 caractères au maximum. </li> 
      <li id="li_C1019E587995444D9587D5EA495D719E"> Le nom n’est pas sensible à la casse, mais il s’affiche et est stocké exactement au fur et à mesure que vous le saisissez. </li> 
      <li id="li_E55404D6CE354EC89CFFEB1048A11F44"> Vous ne pouvez pas utiliser les noms qui existent dans les champs prédéfinis comme le montre le tableau de la page <span class="wintitle"> Définitions intermédiaires </span>. </li> 
      <li id="li_7CE328AE3B5F45A8A09E2DA7ECB62551"> Vous ne pouvez pas utiliser le mot "any" comme valeur d’un nom de champ défini par l’utilisateur. </li> 
      <li id="li_9B8287EED1784E79BFCBBBA956705CD2"> Vous ne pouvez pas modifier les noms des champs prédéfinis. </li> 
      </ul> </p> <p> Exemples de noms de champ : </p> <p> 
      <ul id="ul_5881669913D04E35A6D4A6D31BEE7DF3"> 
        <li id="li_0AFFB8B516FE40F8A615C2F578F2CEA3"> Auteur </li> 
        <li id="li_7F0ADFBFB21E4B84ACA8A1CEBFE344D1"> PublishDate </li> 
        <li id="li_6D1BEB3D19AC499E9227EC115AEB6296"> quelque chose-sauvage </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom(s) de balise(s) méta </p> </td> 
      <td colname="col2"> <p>Détermine le contenu associé au champ défini. </p> <p>La liste de noms peut contenir jusqu’à 255 caractères. De plus, le nom peut contenir tous les caractères autorisés dans l’attribut name d’une balise meta HTML. </p> <p>Vous pouvez spécifier plusieurs balises META dans une seule définition de champ. </p> <p>Plusieurs valeurs doivent être séparées par des virgules, et le nom de la balise META le plus à gauche figurant sur une page web donnée est prioritaire. </p> <p>Supposons, par exemple, que vous ayez défini un champ nommé "auth". Le nom du champ comporte les balises META associées "author, dc.author". Dans ce cas, le contenu de la balise meta "author" est indexé et recherché sur celui de "dc.author" si les deux balises meta apparaissent sur une page web. </p> <p>Les champs définis par l’utilisateur doivent avoir au moins un nom de balise META dans leur définition. Les champs prédéfinis n’ont pas besoin d’avoir une balise META associée. Toutefois, si une ou plusieurs balises META sont spécifiées, le contenu des balises META remplace la source de données actuelle pour chaque balise. </p> <p>Par exemple, si la balise meta "dc.title" est associée au champ prédéfini "title", le contenu de la balise meta "dc.title" est indexé sur celui du champ 
      Balise <code>
        &lt;title&gt; 
      </code> pour un document particulier. </p> <p>Voici quelques exemples : </p> <p> 
      <ul id="ul_0132E15FC19E4C0CA13CD5A12EA3BBEC"> 
      <li id="li_ECD3B194FECB4C2090CAEC8449320D3F"> dc.date </li> 
      <li id="li_09C76BC7AC7348859D01989697212E31"> Description </li> 
      <li id="li_9230C0450F9D424087D1F127048DA311"> propriétaire </li> 
      </ul> </p> </td> 
    </tr> 
      <tr> 
      <td colname="col1"> <p>Type de données </p> </td> 
      <td colname="col2"> <p>Chaque champ est associé à un type de données tel que texte, nombre, date, version, rang ou emplacement. Ce type de données détermine la manière dont le contenu du champ est indexé, recherché et, éventuellement, trié. </p> <p>Une fois la définition de champ créée, vous ne pouvez pas modifier le type de données. </p> <p>Utilisez les informations suivantes pour vous aider à sélectionner le type de données approprié aux informations contenues dans le champ. </p> <p> 
      <ul id="ul_A3AD5A0CF354410F836311F39151B8A6"> 
      <li id="li_9F412DA7D9EF497BA6E65F9CE10F3046"> <span class="uicontrol"> Les champs de type  </span> de données texte sont traités comme des chaînes de caractères. </li> 
      <li id="li_AD78B75644AE40208F0239311015611F"> <span class="uicontrol"> Les champs de type  </span> de données Nombre sont traités comme des valeurs numériques entières ou à virgule flottante. </li> 
      <li id="li_0B46975C589148E9A7C32A8D250487B7"> <span class="uicontrol"> Les champs de type  </span> de données de date sont traités comme des spécificateurs de date/heure. Vous pouvez personnaliser les formats de date et d’heure autorisés lorsque vous ajoutez ou modifiez le nouveau champ. </li> 
      <li id="li_BB68CB1DBE0543AC9000B3DEDFB28E7E"> <span class="uicontrol"> Les champs de type  </span> de données de version sont traités comme des données numériques de forme libre. Par exemple, la version 1.2.3 trie avant la version 1.2.2. </li> 
      <li id="li_0BA895B4DADA46528A7A4161EEB1521E"> <span class="uicontrol"> Les champs de type  </span> données de classement sont traités de la même manière que les champs de type "Nombre", sauf qu’ils influencent en outre les calculs de classement/pertinence dans les résultats de recherche. <p>Voir <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" type="concept" format="dita" scope="local">A propos des règles de classement </a>. </p> </li> 
      <li id="li_459405DA437049AD88AA1FAC28F04720"> <span class="uicontrol"> Les champs de type  </span> de données de localisation sont traités comme un emplacement physique n’importe où dans le monde. Les formats d’emplacement autorisés sont les suivants : <p> 
      <ul id="ul_D2CEBFA1A5504AA996BA2F7641AFB7F3"> 
      <li id="li_5283A2F2D5D84840B3D920C08D43654C"> Codes postaux à 5 ou 9 chiffres sous la forme de JJJJ ou JJJJ, où chaque "D" est de 0 à 9 chiffres. </li> 
      <li id="li_A5CD4DFC90164BC68183DB7D10603B7C"> Codes à zone à trois chiffres sous la forme de JJ. </li> 
      <li id="li_9DAEAE64BC7F4902B25043D998C8F56D"> Paires latitude/longitude sous la forme ±DD.DDD±DDD.DDD.DDD, où le premier nombre indique la latitude et le second la longitude. </li> 
      </ul> </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>listes autorisées </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Texte </span> ou <span class="uicontrol"> Nombre </span> est sélectionné. </p> <p>Indexez séparément les valeurs délimitées dans le contenu des métadonnées de ce champ. </p> <p>Par exemple, le contenu "Rouge, Jaune, Vert, Bleu" est traité comme quatre valeurs distinctes au lieu d’une valeur lorsque "Listes autorisées" est sélectionné. Ce traitement est plus utile avec la recherche de plage (en utilisant 
      <code>
        sp_q_min 
      </code>, 
      <code>
        sp_q_max 
      </code> ou 
      <code>
        sp_q_exact 
      </code>) et avec la variable 
      <code>
        &lt;search-field-value-list&gt; 
      </code>, 
      <code>
        &lt;search-field-values&gt; 
      </code> et 
      <code>
        &lt;search-display-field-values&gt; 
      </code>. </p> <p>Non disponible si le type de données Version est sélectionné. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> Facette dynamique </p> </td> 
      <td colname="col2"> <p> 
        <!--NEW 2/2/2014--> <p>Remarque : cette fonctionnalité n’est pas activée par défaut. Contactez le support technique pour l’activer afin que vous puissiez l’utiliser. Une fois activé, il apparaît dans l’interface utilisateur. </p> </p> <p>Définit la facette identifiée comme étant dynamique. </p> <p>Les facettes sont construites au-dessus des champs de balise META. Un champ de balise META est une couche de recherche principale de bas niveau de l’Search &amp; Promote d’Adobe. Les facettes, en revanche, font partie de GS (Guided Search) : la couche de présentation de haut niveau du Search &amp; Promote de l’Adobe. Les facettes possèdent des champs de balise meta, cependant, les champs de balise meta ne savent rien des facettes. </p> <p>Voir <a href="../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> À propos des facettes dynamiques </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Autoriser la déduplication </p> </td> 
      <td colname="col2"> <p>Cochez cette option pour activer la déduplication pour ce champ. En d’autres termes, autorisez ce champ à être spécifié au moment de la recherche au moyen de la variable 
        <code>
          sp_dedupe_field 
        </code> Paramètre CGI de recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Paramètres CGI de recherche </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Nom du tableau </p> </td> 
      <td colname="col2"> <p>Associe définitivement le champ donné au nom de la table. </p> <p>Chaque fois qu’un champ de ce type est mentionné dans un paramètre CGI de recherche principal ou une balise de modèle, le nom de la table est fourni automatiquement. Cette fonctionnalité permet de sélectionner des facettes dynamiques par le biais de correspondances de tableau, mais vous pouvez également les utiliser pour les champs de facettes non dynamiques, si vous le souhaitez. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Délimiteurs de liste </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Listes autorisées </span> est sélectionné. </p> <p>Indique les caractères qui séparent des valeurs de liste individuelles. Vous pouvez spécifier plusieurs caractères, chacun étant traité comme un séparateur de valeur. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Rechercher par défaut </p> </td> 
      <td colname="col2"> <p>Lorsque cette option est sélectionnée, la recherche porte sur le contenu du champ même si celui-ci n’est pas explicitement spécifié dans une requête de recherche donnée. Si vous désélectionnez cette option, la recherche du champ se fait uniquement sur demande. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Champ de mise à jour verticale </p> </td> 
      <td colname="col2"> <p> <p>Remarque : cette fonctionnalité n’est pas activée par défaut. Contactez le support technique pour l’activer afin que vous puissiez l’utiliser. Une fois activé, il apparaît dans l’interface utilisateur. </p> </p> <p>Définit le champ identifié comme étant un champ Mise à jour verticale . </p> <p>Les champs Mise à jour verticale peuvent être mis à jour au moyen du processus Mise à jour verticale ( <span class="uicontrol"> Index </span> &gt; <span class="uicontrol"> Mise à jour verticale </span>). En raison de la façon dont les mises à jour verticales sont effectuées, la recherche de contenu de ces champs n’est pas possible dans les recherches en texte libre. Si cette option est cochée, le contenu de ce champ n’est pas ajouté à l’index "word" lors de toute opération d’index. Il permet également la mise à jour de ce champ lors d'une opération de mise à jour verticale. </p> <p>Pour en savoir plus sur les mises à jour verticales, voir <a href="../c-about-index-menu/c-about-vertical-updates.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899" format="dita" scope="local"> À propos de la mise à jour verticale </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Pertinence </p> </td> 
      <td colname="col2"> <p>Vous pouvez modifier la pertinence des champs prédéfinis et définis par l’utilisateur. </p> <p>La pertinence est spécifiée sur une échelle 1-10. Un paramètre de 1 signifie qu’il est le moins pertinent et 10 est le plus pertinent. Ces valeurs sont prises en compte lorsque le logiciel prend en compte les correspondances de la requête dans chaque champ. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Tri </p> </td> 
      <td colname="col2"> <p>Indique le moment où les résultats sont triés par champ nommé, au moyen de la fonction 
        <code>
          sp_s 
        </code> Paramètre CGI de recherche. </p> <p>Voir <a href="../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890" type="reference" format="dita" scope="local"> Paramètres CGI de recherche </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Langue </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span>, <span class="uicontrol"> Nombre </span> ou <span class="uicontrol"> Date </span> est sélectionné. </p> <p>Contrôle les conventions de langue et de paramètres régionaux appliquées lors de l’indexation des valeurs de date, de nombre et de rang pour ce champ. </p> <p>Vous pouvez choisir d'appliquer la langue du compte (Linguistique &gt; Mots et langues). Vous pouvez également appliquer la langue associée au document qui contient chaque nombre ou valeur de date, ou une langue spécifique. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format(s) de date </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Date </span> est sélectionné. </p> <p>Contrôle les formats de date reconnus lors de l’indexation des valeurs de date pour ce champ. </p> <p>Une liste par défaut de chaînes de format de date est fournie pour chaque champ de date. Vous pouvez l’ajouter à la liste ou la modifier en fonction des besoins de votre site. </p> <p>Voir <a href="../c-appendices/r-date-formats.md#reference_4D1FC1F6B9F44857967188496D8D335B" type="reference" format="dita" scope="local"> Formats de date </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Formats de date de test </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Date </span> est sélectionné comme type de données. </p> <p>Permet de prévisualiser les formats de date que vous avez spécifiés pour vous assurer qu’ils sont correctement formatés. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Fuseau horaire </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Date </span> est sélectionné comme type de données. </p> <p>Contrôle le fuseau horaire supposé appliqué lors de l’indexation des valeurs de date pour ce champ qui ne spécifie aucun fuseau horaire. </p> <p>Par exemple, si le fuseau horaire de votre compte est défini sur "Amérique/Los Angeles" et que vous sélectionnez <span class="uicontrol"> Utiliser le fuseau horaire du compte </span>, la méta-valeur de date suivante, qui ne comporte pas de fuseau horaire spécifié, est traitée comme s’il s’agissait de l’heure du Pacifique, en tenant compte de l’heure d’été : </p> <p>&lt;meta name="dc.date" content="Mon, 05 Sep 201213:12:00"&gt; </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de classement la moins importante </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span> est sélectionné comme type de données. </p> <p>Contrôle la valeur rank qui représente le rang minimum de tout document. </p> <p>Si votre classement de document est compris entre 0 pour le rang le plus bas et 10 pour le rang le plus élevé, définissez cette valeur sur 0. </p> <p>Si votre classement de document est compris entre 1 pour le rang le plus élevé et 10 pour le rang le plus bas, vous définissez cette valeur sur 10. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de classement par défaut </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span> est sélectionné comme type de données. </p> <p>Contrôle la valeur de classement utilisée si un document ne contient aucune des balises meta définies pour ce champ de classement. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeur de classement la plus importante </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Classement </span> est sélectionné comme type de données. </p> <p>Contrôle la valeur de rang qui représente le rang maximal de tout document. </p> <p>Si votre classement de document est compris entre 0 pour le rang le plus bas et 10 pour le rang le plus élevé, définissez cette valeur sur 10. </p> <p>Si votre classement de document est compris entre 1 pour le rang le plus élevé et 10 pour le rang le plus bas, définissez cette valeur sur 1. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Unités par défaut </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si le type de données <span class="uicontrol"> Emplacement </span> est sélectionné comme type de données. </p> <p>Contrôle le traitement des valeurs de distance pour les recherches de proximité. </p> <p>Si vous définissez les unités par défaut sur <span class="uicontrol"> Miles </span>, tous les critères de distance minimale/maximale de la recherche de proximité qui sont appliqués à ce champ (au moyen de l’option 
      <code>
        sp_q_min[_#] 
      </code> ou la variable 
      <code>
        sp_q_max[_#] 
      </code> Paramètres CGI de recherche) est traité comme des kilomètres, sinon comme des kilomètres. </p> <p>Cette option contrôle également les unités de distance par défaut qui sont appliquées à la sortie de l’objet 
      <code>
        &lt;Search-Display-Field&gt; 
      </code> balise de modèle de résultats de recherche lorsqu’elle est appliquée à un champ de sortie de recherche de proximité. </p> <p>Voir <a href="../c-appendices/r-about-proximity-search.md#reference_45AC6BB50609431ABD31DA46EE65360D" type="reference" format="dita" scope="local"> À propos de la recherche de proximité </a>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Créer une description de plage ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Nombre </span> est sélectionné comme type de données. </p> <p>Contrôle la création automatique des descriptions de plage de champs, à utiliser avec <span class="uicontrol"> Conception </span> &gt; <span class="uicontrol"> Navigation </span> &gt; <span class="uicontrol"> Facettes </span>. </p> <p>Voir <a href="../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5" format="dita" scope="local"> À propos des facettes </a>. </p> <p> <p>Remarque :  Si <span class="uicontrol"> Champ de mise à jour verticale </span> est coché dans ce champ, le champ de description de la plage de champs généré est mis à jour lors d’une mise à jour verticale. Toutefois, il est recommandé de vérifier également <span class="uicontrol"> le champ identifié dans <span class="uicontrol"> Champ de plage </span>  Champ de mise à jour vertical </span>. </p> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Champ de plage </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché. </p> <p>Le champ <span class="uicontrol"> Texte </span> à mettre à jour avec les descriptions de plage pour le champ actif. Cette liste contient tous les champs <span class="uicontrol"> Texte </span> qui ne sont pas déjà utilisés avec d’autres champs pour la génération de la plage de champs. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Valeurs de plage </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Liste de points de données délimités par des champs à utiliser lors de la création des descriptions de plage de champs. Par exemple : </p> <code> 10&amp;nbsp;20&amp;nbsp;50&amp;nbsp;100&amp;nbsp;1000 </code> <p>Vous pouvez saisir ces valeurs dans n’importe quel ordre. Les valeurs sont triées et les doublons supprimés avant d’être enregistrés. Vous pouvez également spécifier des valeurs négatives et non entières. </p> <p>Pour chacune des valeurs de ce champ : 
      <ul id="ul_C4B41AF5AADF4B84B9C489CE82FF7075"> 
      <li id="li_90736394A5AE4F5CA6B47687BCB627AA">Si la valeur est inférieure à (&lt;) la plus petite valeur de <span class="uicontrol"> Valeurs de plage </span>, le <span class="uicontrol"> format "inférieur à" </span> est utilisé. </li> 
      <li id="li_A5C272B2D26A468CA07EB2046B2EA8A7">Si la valeur est supérieure ou égale à (&gt;=) la valeur la plus grande de <span class="uicontrol"> Valeurs de plage </span>, le <span class="uicontrol"> format "supérieur à" </span> est utilisé. </li> 
      <li id="li_9DDFB70E1E824CF4819C57450C1A6DD2">dans le cas contraire, une "plage" est trouvée lorsque la valeur du champ est comprise entre deux valeurs consécutives <span class="uicontrol"> Valeurs de plage </span> (supérieures à (&gt;) la valeur inférieure et inférieure ou égale à (&lt;=) la valeur la plus élevée), et le <span class="uicontrol"> Format intermédiaire </span> est utilisé. </li> 
    </ul> </p> <p>Par exemple, l’exemple d’ensemble de valeurs ci-dessus définit un ensemble de descriptions de valeurs : 
    <ul id="ul_03ED30D5A19346AB8E6809BDD186A9A9"> 
      <li id="li_F97A6B3763954EFE9B6751F472AF7D20">moins de 10 </li> 
      <li id="li_12B6F636A6444B8292E0BFE4F55032DF">supérieur ou égal à 10 et inférieur à 20 </li> 
      <li id="li_545A2EAF5BD046B5AD59B77DB43DCD14">supérieur ou égal à 20 et inférieur à 50 </li> 
      <li id="li_26A8CD2422524D2CBD36794C6908572A">supérieur ou égal à 50 et inférieur à 100 </li> 
      <li id="li_05EBEEE68DC348E0821F1CC16D04D69C">supérieur ou égal à 100 et inférieur à 10 000 </li> 
      <li id="li_9513A6B519394780A6A41B80762A0370">supérieur ou égal à 10 000 </li> 
      </ul> </p> <p>Voir <span class="uicontrol"> Test à l’aide de Supérieur à ? </span> pour modifier la manière dont ces tests sont effectués. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format "Inférieur à" </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Il s’agit du modèle utilisé pour spécifier la description de la plage pour les valeurs inférieures à la plus petite valeur trouvée dans <span class="uicontrol"> Valeurs de plage </span>. La valeur la plus petite sera représentée à l’aide du jeton d’espace réservé numérique <span class="uicontrol"> ~N~ </span>. Par exemple : </p> <code> Less&amp;nbsp;than&amp;nbsp;~N~ </code> <p>ou : </p> <code> ~N~&amp;nbsp;and&amp;nbsp;below </code> <p>Normalement, la valeur est formatée "en l’état", c’est-à-dire pour une <span class="uicontrol"> définition de valeurs de plage </span> de "5 10 20" et une valeur fournie de 1, la description de plage générée serait simplement de l’ordre de "Moins de 5". Si vous souhaitez qu’il soit "4.99 et inférieur", définissez <span class="uicontrol"> Précision </span> sur <span class="uicontrol"> 2 </span> et utilisez ce format : </p> <code> ~n~&amp;nbsp;and&amp;nbsp;below </code> <p>Dans le <span class="uicontrol"> format "Inférieur à" </span>, la minuscule <span class="uicontrol"> ~n~ </span> arrondit la valeur <i>vers le bas</i> selon le paramètre <span class="uicontrol"> Précision </span> . </p> <p>Remarque : pour inclure n’importe quel espace réservé numérique dans la description de la plage, en l’état, spécifiez avec une barre oblique inverse (\), par exemple : <span class="uicontrol"> \~N~ </span> ou <span class="uicontrol"> \~n~ </span>. Pour inclure une barre oblique inverse, spécifiez-la avec une autre barre oblique inverse, par exemple : <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format intermédiaire </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Il s’agit du modèle utilisé pour spécifier la description de la plage pour les valeurs comprises entre les valeurs les plus petites et les plus grandes trouvées dans <span class="uicontrol"> Valeurs de plage </span>. Pour la plage donnée, la valeur de plage inférieure est représentée à l’aide du jeton d’espace réservé numérique <span class="uicontrol"> ~L~ </span>, et la valeur de plage supérieure est représentée à l’aide du jeton <span class="uicontrol"> ~H~ </span>. Par exemple : </p> <code> ~L~&amp;nbsp;to&amp;nbsp;~H~ </code> <p>ou : </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>ou : </p> <code> Less&amp;nbsp;than&amp;nbsp;~H~&amp;nbsp;and&amp;nbsp;greater&amp;nbsp;than&amp;nbsp;~L~ </code> <p>Normalement, les valeurs seront formatées "en l’état", c’est-à-dire pour une <span class="uicontrol"> définition de valeurs de plage </span> de "5 10 20" et une valeur fournie de 8, la description de plage générée serait simplement de l’ordre de "entre 5 et 10". Si vous souhaitez qu’elle soit "comprise entre 5 et 9.99", avec la valeur la plus élevée ajustée <i>en bas</i>, définissez <span class="uicontrol"> Précision </span> sur <span class="uicontrol"> 2 </span> et utilisez ce format : </p> <code> Between&amp;nbsp;~L~&amp;nbsp;and&amp;nbsp;~h~ </code> <p>De même, <span class="uicontrol"> ~L~ </span> peut être remplacé par <span class="uicontrol"> ~l~ </span> pour que la valeur inférieure soit ajustée <i>à la hausse</i>, également en fonction du paramètre <span class="uicontrol"> Précision </span> . Cela signifie qu’une définition comme : </p> <code> Between&amp;nbsp;~l~&amp;nbsp;and&amp;nbsp;~H~ </code> <p>avec une valeur <span class="uicontrol"> de précision </span> de <span class="uicontrol"> 2 </span> créerait "Entre 5.01 et 10". </p> <p>La minuscule <span class="uicontrol"> ~l~ </span> arrondit la valeur inférieure <i>up</i> selon le paramètre <span class="uicontrol"> Précision </span> et la minuscule <span class="uicontrol"> ~h~ </span> arrondit la valeur supérieure <i>down</i>. </p> <p>Remarque : pour inclure n’importe quel espace réservé numérique dans la description de la plage, en l’état, spécifiez avec une barre oblique inverse (\), par exemple : <span class="uicontrol"> \~L~ </span> ou <span class="uicontrol"> \~h~ </span>. Pour inclure une barre oblique inverse, spécifiez-la avec une autre barre oblique inverse, par exemple : <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Format "Supérieur à" </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Il s’agit du modèle utilisé pour spécifier la description de la plage pour les valeurs supérieures à la valeur la plus élevée trouvée dans <span class="uicontrol"> Valeurs de plage </span>. La valeur la plus élevée sera représentée à l’aide du jeton d’espace réservé numérique <span class="uicontrol"> ~N~ </span>. Par exemple : </p> <code> Greater&amp;nbsp;than&amp;nbsp;~N~ </code> <p>ou : </p> <code> ~N~&amp;nbsp;and&amp;nbsp;above </code> <p>Normalement, la valeur est formatée "en l’état", c’est-à-dire pour une <span class="uicontrol"> définition de valeurs de plage </span> de "5 10 20" et une valeur fournie de 30, la description de plage générée serait simplement "supérieure à 20". Si vous souhaitez qu’il soit "20.01 et supérieur", définissez <span class="uicontrol"> Précision </span> sur <span class="uicontrol"> 2 </span> et utilisez ce format : </p> <code> ~n~&amp;nbsp;and&amp;nbsp;above </code> <p>Dans le <span class="uicontrol"> format "Supérieur à" </span>, la minuscule <span class="uicontrol"> ~n~ </span> arrondit la valeur <i>à </i> selon le paramètre <span class="uicontrol"> Précision </span> . </p> <p>Remarque : pour inclure n’importe quel espace réservé numérique dans la description de la plage, en l’état, spécifiez avec une barre oblique inverse (\), par exemple : <span class="uicontrol"> \~N~ </span> ou <span class="uicontrol"> \~n~ </span>. Pour inclure une barre oblique inverse, spécifiez-la avec une autre barre oblique inverse, par exemple : <span class="uicontrol"> \\ </span>. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Précision </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Valeur entière spécifiant le nombre de chiffres à droite d’un point décimal. Cela contrôle également les opérations d’arrondi. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Bande les zéros au début ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché, un élément <span class="uicontrol"> Champ de plage </span> est sélectionné et une valeur <span class="uicontrol"> de précision </span> non nulle a été définie. </p> <p>Devrions-nous afficher "0,50" comme ".50" ? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Effacer les zéros à la fin ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché, un élément <span class="uicontrol"> Champ de plage </span> est sélectionné et une valeur <span class="uicontrol"> de précision </span> non nulle a été définie. </p> <p>Devrions-nous afficher "10.00" comme "10" ? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Afficher les séparateurs des milliers ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Devrions-nous afficher "10 000" comme "10 000" ? Des valeurs spécifiques aux paramètres régionaux seront utilisées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Ajuster zéro valeur ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Lorsque des valeurs nulles sont arrondies, doivent-elles être arrondies vers le haut ou vers le bas selon le paramètre <span class="uicontrol"> Précision </span> ? c’est-à-dire afficher "0,01" ? </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test à l’aide de Supérieur à ? </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Chaque valeur étant comparée aux valeurs <span class="uicontrol"> Valeurs de plage </span>, traitées dans l’ordre <i><b>descendant</b></i>, elle est comparée, par défaut, à l’aide de l’opérateur Supérieur à ou Égal (&gt;=), s’arrêtant une fois ce test réussi. Cela signifie qu’avec un ensemble de <span class="uicontrol"> valeurs de plage </span> du type "10 20 50 100 1000", la valeur 100 tombe dans la plage 100 à 1000, car 100 est en effet &gt;= 100. Si vous préférez qu’elle tombe dans la plage 50 à 100, cochez cette option, ce qui entraînera des comparaisons utilisant l’opérateur Supérieur à (&gt;) à la place. </p> <p>Par exemple, pour chacune des valeurs de ce champ, lorsque cette option est cochée : 
      <ul id="ul_969621B1BD914FA5BD73ED21F8841010"> 
      <li id="li_157BEFDA7D0E44C481F4E4BC9046EF24">Si la valeur est inférieure ou égale à (&lt;=) la plus petite valeur de <span class="uicontrol"> Valeurs de plage </span>, le <span class="uicontrol"> Format "inférieur à" </span> sera utilisé. </li> 
      <li id="li_737EE666CA6243A8864E17A311CF3ACC">Si la valeur est supérieure à (&gt;) la valeur la plus grande dans <span class="uicontrol"> Valeurs de plage </span>, le <span class="uicontrol"> format "supérieur à" </span> sera utilisé. </li> 
      <li id="li_353A9820F7F74CCCBB3281EC4CB48734">sinon, une plage sera trouvée où la valeur du champ est comprise entre deux valeurs consécutives <span class="uicontrol"> Valeurs de plage </span> (supérieures ou égales à (&gt;=) la valeur la plus petite et inférieure à (&lt;) la valeur la plus grande), et le <span class="uicontrol"> Format intermédiaire </span> sera utilisé. </li> 
    </ul> </p> <p>et, lorsqu’elle est décochée : 
    <ul id="ul_945844C33C2E4D95A598C4876E15F211"> 
      <li id="li_653B6E2934574DA3B4BCEF07D0A84527">Si la valeur est inférieure à (&lt;) la plus petite valeur de <span class="uicontrol"> Valeurs de plage </span>, le <span class="uicontrol"> format "inférieur à" </span> sera utilisé. </li> 
      <li id="li_AECA6880002F40FAB1820B37237550A7">Si la valeur est supérieure ou égale à (&gt;=) la valeur la plus grande de <span class="uicontrol"> Valeurs de plage </span>, le <span class="uicontrol"> format "supérieur à" </span> sera utilisé. </li> 
      <li id="li_ECB2DF7CA592497298E9ADC708220366">sinon, une plage sera trouvée où la valeur du champ est comprise entre deux valeurs consécutives <span class="uicontrol"> Valeurs de plage </span> (supérieures à (&gt;) la valeur inférieure et inférieure ou égale à (&lt;=) la valeur la plus élevée), et le <span class="uicontrol"> Format intermédiaire </span> sera utilisé. </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Test </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si <span class="uicontrol"> Créer la description de la plage </span> est coché et qu’un élément <span class="uicontrol"> Champ de plage </span> est sélectionné. </p> <p>Fournissez un exemple de valeur numérique et appuyez sur le bouton <span class="uicontrol"> Tester </span> pour voir comment le champ de plage est créé. La description de la plage générée s’affiche dans la fenêtre. </p> </td> 
      </tr> 
    </tbody> 
    </table>

   Voir aussi [Ajout d’un nouveau champ de balise META](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Cliquez sur **[!UICONTROL Add]**.
1. (Facultatif) Recréez l’index de site intermédiaire si vous souhaitez prévisualiser les résultats.

   Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification de champs de métadonnées prédéfinis ou définis par l’utilisateur {#task_0A7657B63596421BB6DB3ED44F827AB3}

Vous ne pouvez modifier que certains champs des méta-balises prédéfinies, ou modifier tous les champs des méta-balises définies par l’utilisateur.

Avant que les effets de vos modifications de balises META ne soient visibles par les clients, vous devez reconstruire l’index de votre site.

**Pour modifier des champs de métadonnées prédéfinis ou définis par l’utilisateur**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Sur la page [!DNL Definitions], dans la colonne [!DNL Actions] du tableau, cliquez sur **[!UICONTROL Edit]** dans la ligne du nom du champ de balise meta que vous souhaitez modifier.
1. Sur la page [!DNL Pinned Keyword Results Manager], dans le tableau, cliquez sur **[!UICONTROL Edit]** dans la ligne du mot-clé que vous souhaitez modifier.
1. Sur la page [!DNL Edit Field], définissez les options de votre choix.

   Si vous choisissez d’apporter des modifications à un champ de méta-balise prédéfini, sachez que tous les champs ne sont pas modifiables.

   Consultez le tableau des options sous [Ajout d’un nouveau champ de balise META](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Recréez l’index de site intermédiaire si vous souhaitez prévisualiser les résultats.

   Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Suppression d’un champ de balise META défini par l’utilisateur {#task_9361EF38B5E743038B6672FA6CF70FD3}

Vous pouvez supprimer un champ de méta-balise défini par l’utilisateur dont vous n’avez plus besoin ou que vous n’utilisez plus.

Vous ne pouvez pas supprimer les champs de méta-balise prédéfinis. Vous pouvez toutefois modifier certains champs.

Voir [Modification de champs de balise META prédéfinis ou définis par l’utilisateur](../c-about-settings-menu/c-about-metadata-menu.md#task_0A7657B63596421BB6DB3ED44F827AB3).

Avant que les effets de votre méta-balise de suppression ne soient visibles par les clients, vous devez reconstruire l’index de votre site.

**Pour supprimer un champ de méta-balise défini par l’utilisateur**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]**.
1. Sur la page [!DNL Definitions], dans la section [!DNL User-defined fields] du tableau, cliquez sur **[!UICONTROL Delete]** dans la ligne du nom du champ de balise meta que vous souhaitez supprimer.
1. Dans la boîte de dialogue Confirmation, cliquez sur **[!UICONTROL OK]**.
1. (Facultatif) Recréez l’index de site intermédiaire si vous souhaitez prévisualiser les résultats.

   Voir [Configuration d’un index incrémentiel d’un site web intermédiaire](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0).
1. (Facultatif) Sur la page [!DNL Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos des injections {#concept_DA091920671948A0A893A26B3A2FAAE5}

Vous pouvez utiliser [!DNL Injections] pour insérer du contenu dans vos pages web sans avoir à modifier les pages elles-mêmes.

Vous pouvez ajouter du contenu à des champs indexés spécifiques tels que &quot;target&quot; ou &quot;body&quot;, ou remplacer le contenu indexé par de nouvelles valeurs. Par exemple, si vous avez inséré un nouveau contenu dans le champ de balise meta &quot;cible&quot;, ces informations sont traitées de la même manière que le contenu de la page codé en dur. Vous pouvez modifier le contenu de tout champ de méta-balise prédéfini, que les pages de votre site comportent ou non un contenu correspondant. Par exemple, vous pouvez modifier le contenu des noms de champ de méta-balise prédéfinis suivants :

* Alt
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

Vous pouvez éventuellement utiliser **[!UICONTROL Test]** sur la page [!DNL Staged Injections]. Vous saisissez un nom de champ de test (par exemple, &quot;titre&quot; ou &quot;corps&quot;), la valeur de champ d’origine (par exemple, &quot;Page d’accueil&quot;) et une URL de test de votre site web. La valeur obtenue s’affiche à titre de référence. Les valeurs actives ne sont pas modifiées pendant le test.

## Utilisation des définitions d’injection de champ {#section_C1BBF19DE8EF4A6F8CC3ED691F3953A9}

Les définitions d’injection ont la forme suivante :

```
append|replace field [regexp] URL value
```

`append|replace`, `field`, `URL`. et `value` sont obligatoires. Vous saisissez une définition d’injection par ligne. L’exemple suivant contient six définitions d’injection différentes.

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
   <td colname="col1"> <p> <span class="codeph"> append|replace  </span> </p> </td> 
   <td colname="col2"> <p>Sélectionnez "Ajouter" pour ajouter la valeur de la définition d’injection ("Adobe : Nous contacter" ou "En vente maintenant" dans les exemples ci-dessus) au contenu des champs existants. Sélectionnez "replace" pour remplacer le contenu du champ existant par la valeur définie. Si un champ ne comporte actuellement pas de contenu, la valeur définie est ajoutée automatiquement, quelle que soit l’option utilisée (ajouter ou remplacer). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> field  </span> </p> </td> 
   <td colname="col2"> <p>Un nom de champ est requis. Vous trouverez ci-dessous dix noms de champ prédéfinis que vous pouvez utiliser : </p> <p> 
     <ul id="ul_B9336FA53023474EAEE399116E7FC972"> 
      <li id="li_C621203DCD2B4875A54A1DD19F0B5B90"> <span class="codeph"> Alt </span> </li> 
      <li id="li_9217E6A037254BEDBB8D006B70D7670D"> <span class="codeph"> body </span> </li> 
      <li id="li_DCDC50F93F224F02897419B745E09399"> <span class="codeph"> charset </span> </li> 
      <li id="li_D95668236B6547B99966668C82B302AB"> <span class="codeph"> date </span> </li> 
      <li id="li_D2071681274345C3B97E9ADA6D223271"> <span class="codeph"> desc  </span> </li> 
      <li id="li_26683A9209454A438D811187FB929482"> <span class="codeph"> clés </span> </li> 
      <li id="li_A5E19F81B872402CA62B5AB9497E030D"> <span class="codeph"> language </span> </li> 
      <li id="li_FD0B1CD9E6304B18B9D7F57E61015107"> <span class="codeph"> cible  </span> </li> 
      <li id="li_400D7E3F3E9B47EFB2FF5C0D278DB573"> <span class="codeph"> titre </span> </li> 
      <li id="li_449BCBEE4F64424BB69F780C10F5956C"> <span class="codeph"> url </span> </li> 
     </ul> </p> <p>Chaque nom de champ correspond aux éléments des pages de votre site. Si vous spécifiez le nom du champ <span class="codeph"> desc </span> par exemple, vous pouvez ajouter la valeur de définition d’injection au champ correspondant à la description Les balises META sur les pages de votre site. </p> <p>S’il n’existe pas de balise META de description sur vos pages, le contenu défini crée la balise pour vous. Le contenu spécifié dans une injection <span class="codeph"> desc </span> s’affiche sur votre page de résultats comme le ferait le contenu de métamdescription codé en dur. </p> <p>Vous pouvez également créer plusieurs définitions avec le même nom de champ. Par exemple, supposons que vous ayez les injections suivantes : </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/&nbsp;Welcome&nbsp;to&nbsp;My&nbsp;Site </code> </p> <p> <code> replace&nbsp; <b>title</b>&nbsp;https://www.mysite.com/company/*.html&nbsp;My&nbsp;Site:&nbsp;Contact </code> </p> <p>Toutes les pages du site de l’exemple ci-dessus reçoivent un titre injecté "Bienvenue sur mon site". Les pages du dossier "/company/" sont insérées avec un nouveau titre "My Site : Nous contacter" qui remplace le précédent. </p> <p>Notez que les injections sont appliquées dans l’ordre dans lequel elles apparaissent dans la zone de texte <span class="wintitle"> Définitions d’injection de champ </span> . Si le même champ ("titre" dans cet exemple) est défini plusieurs fois pour les pages situées au même emplacement, la définition ultérieure est prioritaire. </p> <p> <span class="codeph"> [regexp]  </span> - facultatif. Si vous choisissez d’utiliser l’option <span class="codeph"> regexp </span>, l’URL définie est traitée comme une expression régulière. </p> <p>Voir <a href="../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A" type="reference" format="dita" scope="local"> Expressions régulières </a>. </p> <p>Dans la définition suivante : </p> <p> <code> replace&nbsp;target&nbsp; <b>regexp&amp;nbsp;^.*/products/.*\.html$</b>&nbsp;Important&nbsp;information </code> </p> <p> "Informations importantes" est injecté dans le champ "cible" de toutes les pages qui correspondent à l’expression régulière <span class="codeph"> ^.*/products/.*\.html$ </span>. </p> <p>Par conséquent, vous disposez des éléments suivants : </p> <p> <code> https://www.mydomain.com/products/page1.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p> <code> https://www.mydomain.com/product/oldstuff.html 
      &nbsp;&nbsp;&nbsp;&nbsp;(Will&nbsp;not&nbsp;receive&nbsp;"target"&nbsp;content) </code> </p> <p>Dans l’exemple suivant : </p> <p> <code> append&amp;nbsp;title&amp;nbsp;regexp&amp;nbsp;^.*\.pdf$&amp;nbsp;Millennium&amp;nbsp;Science </code> </p> <p>L’injection ajoute "Millennium Science" au contenu "titre" de toutes les pages se terminant par une extension de nom de fichier ".pdf". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> URL </span> </p> </td> 
   <td colname="col2"> <p>Une URL est requise et indique les documents qui sont injectés. </p> <p>L’URL est l’une des suivantes : </p> <p> 
     <ul id="ul_C5C74F6D5EA943B293742989EB822751"> 
      <li id="li_382392DB778D4E14BFFC96D35A861951"> Un chemin complet, comme dans https://www.mydomain.com/products.html </li> 
      <li id="li_EA2BD0FB66A44CD0844613316F6174D4"> Un chemin partiel, comme dans https://www.mydomain.com/products </li> 
      <li id="li_D5E0D6D897C8493ABBFC65517CD4A7DB"> Une URL qui utilise des caractères génériques, comme dans https://www.mydomain.com/*.html </li> 
     </ul> </p> <p>La valeur URL ne doit pas comporter d’espaces. Si l’option <span class="codeph"> regexp </span> est utilisée, l’URL est traitée comme une expression régulière. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> value </span> </p> </td> 
   <td colname="col2"> <p>Une valeur est requise et est utilisée pour remplacer ou ajouter du contenu de champ existant. Vous pouvez spécifier plusieurs valeurs pour le même nom de champ. Par exemple : </p> <p>ajoutez <b>keys</b> https://www.mysite.com/travel/ <b>summer</b>, <b>plage</b>, <b>sable</b> </p> <p>Ajoutez <b>keys</b> https://www.mysite.com/travel/fare/*.html <b>billets bon marché</b> </p> <p>Dans l’exemple ci-dessus, les mots "summer, Beach, sable" sont ajoutés au champ "keys" sur toutes les pages du répertoire "/travel/". Les mots "billets bon marché" sont également ajoutés au champ "clés" de toutes les pages du répertoire "/travel/fare/". </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir aussi [Sélection des types de contenu à analyser et à indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

## Ajout de définitions d’injection de champ {#task_E86566FA1FF74CF68115C0ADA05172AE}

Vous pouvez utiliser [!DNL Injections] pour insérer du contenu dans vos pages web sans avoir à modifier les pages elles-mêmes.

Vous pouvez éventuellement utiliser **[!UICONTROL Test]** sur la page [!DNL Injections]. Vous saisissez un nom de champ de test (par exemple, &quot;titre&quot; ou &quot;corps&quot;), la valeur de champ d’origine (par exemple, &quot;Page d’accueil&quot;) et une URL de test de votre site web. La valeur obtenue s’affiche à titre de référence. Les valeurs actives ne sont pas modifiées pendant le test.

**Pour ajouter des définitions d’injection de champ**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**.
1. (Facultatif) Sur la page [!DNL Injections], dans la zone [!DNL Test Field Injections], saisissez le champ test, la valeur d’origine du test et l’URL du test, puis cliquez sur **[!UICONTROL Test]**.
1. Dans le champ [!DNL Field Injection Definitions] , saisissez une définition d’injection par ligne.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## A propos du chargeur d’attributs {#concept_9EF38E98811B42CDA41996432B9AD209}

Utilisez [!DNL Attribute Loader] pour définir des sources d’entrée supplémentaires afin d’augmenter les données analysées à partir d’un site web.

>[!NOTE]
>
>Pour utiliser le chargeur d’attributs, vous devrez peut-être l’activer dans votre compte par le représentant de votre compte d’Adobe ou par l’assistance Adobe.

Vous pouvez utiliser une source d’entrée de flux de données pour accéder au contenu stocké dans un formulaire différent de ce qui est généralement découvert sur un site web. Pour ce faire, utilisez l’une des méthodes d’analyse disponibles. Les données provenant de ces sources peuvent ensuite être injectées dans des données à partir de contenu analysé.

Après avoir ajouté une définition de chargeur d’attributs à la page [!DNL Staged Attribute Loader Definitions] , vous pouvez modifier tous les paramètres de configuration, à l’exception des valeurs Nom et Type .

La page [!DNL Attribute Loader] présente les informations suivantes :

* Nom de la configuration de chargeur d’attributs définie que vous avez configurée et ajoutée.
* L’un des types de source de données suivants pour chaque connecteur que vous avez ajouté :

   * **Texte**  : fichiers &quot;plats&quot; simples, délimités par des virgules, délimités par des tabulations ou autres formats délimités de manière cohérente.
   * **Flux**  : flux XML.

* Si la configuration est activée ou non pour l’analyse et l’indexation suivantes.
* Adresse de la source de données.

Voir aussi [Comment fonctionne le processus d’injection d’attributs pour le texte et le flux...](../c-about-settings-menu/c-about-metadata-menu.md#section_E059A33D61EE4DB0972A37B8A35E9E16)

Voir aussi [A propos de la configuration de plusieurs chargeurs d’attributs](../c-about-settings-menu/c-about-metadata-menu.md#section_4CC49C74EF294608A184E233F215ADFF)

Voir aussi [À propos de l’utilisation de l’aperçu lorsque vous ajoutez un attribut...](../c-about-settings-menu/c-about-metadata-menu.md#section_E9CAB000A94C4D9189786C1EDB1CDB46)

## Fonctionnement du processus d’injection d’attributs pour les configurations de texte et de flux dans le chargeur d’attributs {#section_E059A33D61EE4DB0972A37B8A35E9E16}

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
   <td colname="col3"> <p>Pour les configurations Texte et Flux , il s’agit d’un simple téléchargement de fichier. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>2 </p> </td> 
   <td colname="col2"> <p>Ventilez la source de données téléchargée en pseudo-documents individuels. </p> </td> 
   <td colname="col3"> <p>Pour <span class="uicontrol"> Texte </span>, chaque nouvelle ligne de texte délimitée par des lignes correspond à un document individuel et est analysée à l’aide du délimiteur spécifié, tel qu’une virgule ou un onglet. </p> <p>Pour le flux <span class="uicontrol"> </span>, les données de chaque document sont extraites à l’aide d’un modèle d’expression régulière sous la forme suivante : </p> <p> <code class="syntax js"> &lt;${Itemtag}&gt;(.*?)&lt;/${Itemtag}&gt; </code> </p> <p>En utilisant <span class="uicontrol"> Carte </span> sur la page <span class="wintitle"> Chargeur d’attributs Ajoutez </span> , créez une copie mise en cache des données, puis créez une liste de liens pour le moteur de recherche. Les données sont stockées dans un cache local et sont renseignées avec les champs configurés. </p> <p>Les données analysées sont écrites dans le cache local. </p> <p>Ce cache est lu ultérieurement pour créer les documents HTML simples nécessaires au robot d’indexation. Par exemple : </p> <p> <code class="syntax html"> &lt;html&gt;&lt;head&gt; 
      &lt;title&gt;{title}&lt;/title&gt; 
      &lt;meta&nbsp;name="{field}"&nbsp;content="{data}"&nbsp;/&gt; 
      ... 
      &lt;/head&gt;&lt;body&gt; 
      {body} 
      &lt;/body&gt;&lt;/html&gt; </code> </p> <p>L’élément <span class="codeph"> &lt;title&gt; </span> n’est généré que lorsqu’il existe un mappage sur le champ de métadonnées Titre. De même, l’élément <span class="codeph"> &lt;body&gt; </span> n’est généré que lorsqu’il existe un mappage sur le champ de métadonnées Body. </p> <p> <b>Important</b> : L’affectation de valeurs à la balise meta d’URL prédéfinie n’est pas prise en charge. </p> <p>Pour tous les autres mappages, les balises <span class="codeph"> &lt;meta&gt; </span> sont générées pour chaque champ contenant des données présentes dans le document d’origine. </p> <p>Les champs de chaque document sont ajoutés au cache. Pour chaque document écrit dans le cache, un lien est également généré, comme dans les exemples suivants : </p> <p> <code class="syntax html"> &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      &lt;a&nbsp;href="index:Adobe?key=&lt;primary&nbsp;key&nbsp;field&gt;\"&nbsp;/&gt; 
      .... </code> </p> <p>Le mappage de la configuration doit comporter un champ identifié comme Clé Principal. Ce mappage forme la clé utilisée lorsque les données sont extraites du cache. </p> <p>Le robot reconnaît l’index <span class="codeph"> de l’URL : </span> préfixe de schéma, qui peut ensuite accéder aux données mises en cache localement. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>3 </p> </td> 
   <td colname="col2"> <p>Analyse du jeu de documents mis en cache. </p> </td> 
   <td colname="col3"> <p>Index <span class="codeph"> : Les liens </span> sont ajoutés à la liste en attente du moteur de recherche et sont traités dans l’ordre d’analyse normal. </p> </td> 
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

Lorsque vous ajoutez un chargeur d’attributs, vous pouvez éventuellement utiliser la fonction **[!UICONTROL Setup Maps]** pour télécharger un exemple de votre source de données. Les données sont examinées pour en déterminer la compatibilité.

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
   <td colname="col2"> <p>Détermine la valeur du délimiteur en commençant par essayer les onglets, puis les barres verticales ( <span class="codeph"> | </span>), et enfin des virgules ( <span class="codeph"> , </span>). Si vous avez déjà spécifié une valeur de délimiteur avant de cliquer sur <span class="uicontrol"> Mappages de configuration </span>, cette valeur est utilisée à la place. </p> <p>Le modèle le mieux adapté entraîne le remplissage des champs de mappage avec des estimations aux valeurs de balise et de champ appropriées. De plus, un échantillonnage des données analysées s’affiche. Veillez à sélectionner <span class="uicontrol"> En-têtes dans la première ligne </span> si vous savez que le fichier contient une ligne d’en-tête. La fonction de configuration utilise ces informations pour mieux identifier les entrées de mappage résultantes. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Flux </p> </td> 
   <td colname="col2"> <p>Télécharge la source de données et effectue une analyse XML simple. </p> <p>Les identifiants XPath résultants sont affichés dans les lignes Balises du tableau Carte et les valeurs similaires dans Champs. Ces lignes identifient uniquement les données disponibles et ne génèrent pas les définitions XPath les plus complexes. Cependant, il reste utile, car il décrit les données XML et identifie l’élément . </p> <p> <p>Remarque :  La fonction Setup Maps télécharge l’intégralité de la source XML pour effectuer son analyse. Si le fichier est volumineux, cette opération peut expirer. </p> </p> <p>En cas de réussite, cette fonction identifie tous les éléments XPath possibles, dont la plupart ne sont pas souhaitables. Veillez à examiner les définitions de mappage qui en résultent et à supprimer celles dont vous n’avez pas besoin ou que vous souhaitez. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>La fonction Setup Maps (Mappages de configuration) peut ne pas fonctionner pour les jeux de données XML volumineux, car l’analyseur de fichiers tente de lire l’intégralité du fichier en mémoire. Par conséquent, vous pourriez rencontrer une condition de mémoire insuffisante. Cependant, lorsque le même document est traité au moment de l’indexation, il n’est pas lu en mémoire. Au lieu de cela, les documents volumineux sont traités &quot;en déplacement&quot; et ne sont pas lus entièrement en mémoire.

## À propos de l’utilisation de l’aperçu lorsque vous ajoutez un chargeur d’attributs {#section_E9CAB000A94C4D9189786C1EDB1CDB46}

Les données de chargeur d’attributs sont chargées avant une opération Index.

Au moment où vous ajoutez un chargeur d’attributs, vous pouvez éventuellement utiliser la fonction **[!UICONTROL Preview]** pour valider les données, comme si vous l’enregistriez. Il exécute un test par rapport à la configuration, mais sans enregistrer la configuration dans le compte. Le test accède à la source de données configurée. Cependant, il écrit le cache de téléchargement dans un emplacement temporaire. il n’entre pas en conflit avec le dossier cache principal utilisé par l’analyseur d’indexation.

L’aperçu traite uniquement une valeur par défaut de cinq documents, comme contrôlé par **Acct:IndexConnector-Preview-Max-Documents**. Les documents prévisualisés sont affichés sous forme source, dans la mesure où ils sont présentés au moteur de recherche d&#39;indexation. L’affichage est similaire à la fonction &quot;Afficher la source&quot; d’un navigateur Web. Vous pouvez parcourir les documents de l’ensemble d’aperçu à l’aide de liens de navigation standard.

L’aperçu ne prend pas en charge les configurations XML, car ces documents sont traités directement et ne sont pas téléchargés dans le cache.

## Ajout d’une définition de chargeur d’attributs {#task_A735E5EF763343A9B675E1A3B09AFDBC}

Chaque configuration de chargeur d’attributs définit une source de données et des mappages afin de mettre en relation les éléments de données définis pour cette source avec les champs de métadonnées de l’index.

>[!NOTE]
>
>Pour utiliser le chargeur d’attributs, vous devrez peut-être l’activer dans votre compte par le représentant de votre compte d’Adobe ou par l’assistance Adobe.

Avant que les effets de la nouvelle définition activée ne soient visibles par les clients, reconstruisez l’index de votre site.

**Pour ajouter une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Stage Attribute Loader Definitions], cliquez sur **[!UICONTROL Add New Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader Add], définissez les options de configuration de votre choix. Les options disponibles dépendent de la balise **[!UICONTROL Type]** sélectionnée.

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
      <td colname="col2"> <p>Source de vos données. Le type de source de données que vous sélectionnez affecte les options résultantes disponibles sur la page <span class="wintitle"> Chargeur d’attributs Ajouter </span> . Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_1ADC3DFBC929467385F7465BE8E13635"> 
      <li id="li_64FCD749F55442BAB316BD474128D4F9"> <span class="uicontrol"> Texte </span> <p>Fichiers texte plats simples, délimités par des virgules, délimités par des tabulations ou autres formats délimités de manière cohérente. Chaque nouvelle ligne de texte délimitée par des lignes correspond à un document individuel et est analysée à l’aide du délimiteur spécifié. </p> <p>Vous pouvez associer chaque valeur, ou colonne, à un champ de métadonnées, référencé par le numéro de colonne, en commençant à 1 (un). </p> </li> 
      <li id="li_2A4F16CE6DCE4114B7F8E4FE156252BB"> <span class="uicontrol"> Flux </span> <p>Télécharge un Principal document XML contenant plusieurs "lignes" d’informations. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Texte</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active la configuration pour utilisation. Vous pouvez également désactiver la configuration pour empêcher l’utilisation de si . </p> <p> <b>Remarque</b> : Les configurations du chargeur d’attributs désactivées sont ignorées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse de l’hôte du serveur où se trouvent vos données. </p> <p>Si vous le souhaitez, vous pouvez spécifier un chemin d’accès URI (Uniform Resource Identifier) complet au document de source de données, comme dans les exemples suivants : </p> <p> <code otherprops="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>ou </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>L’URI est ventilé en entrées appropriées pour les champs Adresse de l’hôte, Chemin du fichier, Protocole et, éventuellement, Nom d’utilisateur et Mot de passe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au fichier de texte simple, délimité par des virgules, délimité par des tabulations ou à tout autre fichier de format délimité de manière cohérente. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Indique le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_F6BC10FD51CA4A1D855B2B3212838A9C"> 
      <li id="li_79FB7DC65E774ABBB23E57BF98AD9738"> HTTP <p>Si nécessaire, vous pouvez saisir des informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_BAA9AD5E4B014E09B3A66C94022B7225"> HTTPS <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_E716ABB169DD408BA91F1CA27F445A16"> FTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_FD7143019C5244C3B8A5B1B5AA84859A"> SFTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_38E0036C1365419F9D00083CACA34AFB"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Expiration </p> </td> 
      <td colname="col2"> <p>Indique le délai d’expiration, en secondes, pour les connexions FTP, SFTP, HTTP ou HTTPS. Cette valeur doit être comprise entre 30 et 300. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Reprises </p> </td> 
      <td colname="col2"> <p>Indique le nombre maximal de tentatives pour les connexions FTP, SFTP, HTTP ou HTTPS en échec. Cette valeur doit être comprise entre 0 et 10. </p> <p>Une valeur de zéro (0) permet d’empêcher les tentatives de nouvelle tentative. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Encodage </p> </td> 
      <td colname="col2"> <p>Spécifie le système de codage des caractères utilisé dans le fichier de source de données spécifié. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Délimiteur </p> </td> 
      <td colname="col2"> <p>Indique le caractère à utiliser pour délimiter chaque champ du fichier de source de données spécifié. </p> <p>La virgule ( <span class="codeph"> , </span>) est un exemple de délimiteur. La virgule agit comme un délimiteur de champ qui permet de séparer les champs de données dans le fichier de source de données spécifié. </p> <p>Sélectionnez l’onglet <span class="uicontrol"> ? </span> pour utiliser le caractère de tabulation horizontale comme délimiteur. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>En-têtes de première ligne </p> </td> 
      <td colname="col2"> <p>Indique que la première ligne du fichier de source de données contient des informations d’en-tête uniquement, et non des données. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Jours périmés </p> </td> 
      <td colname="col2"> <p>Définit l’intervalle minimum entre les téléchargements des données de chargeur d’attributs. Les téléchargements déclenchés par un index qui se produisent dans l’intervalle de fréquence d’actualisation des téléchargements sont ignorés. Lorsque vous définissez cette valeur sur la valeur par défaut de 1, les données du chargeur d’attributs ne se téléchargent pas plus d’une fois dans une période de 24 heures. Tous les index de recherche qui se produisent dans l’intervalle de fréquence d’actualisation des téléchargements utilisent le dernier jeu de données téléchargé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Indique les mappages colonne/métadonnées à l’aide des numéros de colonne. </p> <p> 
      <ul id="ul_981AE2C6D30443BDBFC6575D413732A2"> 
      <li id="li_A42CB9DFFF8C45A7BAC2D471FE96CEBE"> <span class="uicontrol"> Colonne </span> <p> Spécifie un numéro de colonne, la première colonne étant 1 (une). Pour ajouter de nouvelles lignes de mappage pour chaque colonne, sous <span class="wintitle"> Action </span>, cliquez sur <span class="uicontrol"> + </span>. </p> <p>Il n’est pas nécessaire de référencer chaque colonne de la source de données. Vous pouvez plutôt choisir d’ignorer les valeurs. </p> </li> 
      <li id="li_26E8C9554A5D4BC5A5073D6385E3626F"> <span class="uicontrol"> Champ </span> <p>Définit la valeur de l’attribut name utilisée pour chaque balise &lt;meta&gt; générée. </p> </li> 
      <li id="li_5DFA514B7F9549B98D6CBC095A66033C"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> </span> devient une liste déroulante à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actif. </p> <p>La valeur <span class="uicontrol"> Champ </span> peut être un champ de métadonnées non défini, si vous le souhaitez. Un champ de métadonnées non défini est parfois utile pour créer du contenu utilisé par un <span class="wintitle"> script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> À propos du filtrage des scripts </a>. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892C95"> <span class="uicontrol"> Clé primaire? </span> <p>Un seul champ est identifié comme clé Principale. Ce champ sera utilisé comme "clé étrangère" pour faire correspondre les données du chargeur d’attributs au document correspondant dans l’index. </p> </li> 
      <li id="li_80DB205525094CE1AA6762BFC7892D96"> <span class="uicontrol"> Bande du code HTML ?  </span> <p>Lorsque cette option est cochée, toutes les balises HTML figurant dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_359D2902859B4C5BADB0BA26F0BA4DC0"> <span class="uicontrol"> Action </span> <p>Permet d’ajouter des lignes à la carte ou de supprimer des lignes de la carte. L’ordre des lignes n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p> <b>Type de source de données : Flux</b> </p> </td> 
      <td colname="col2"> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Activé </p> </td> 
      <td colname="col2"> <p>Active la configuration pour utilisation. Vous pouvez également désactiver la configuration pour empêcher l’utilisation de si . </p> <p> <b>Remarque</b> : Les configurations du chargeur d’attributs désactivées sont ignorées. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Adresse de l’hôte </p> </td> 
      <td colname="col2"> <p>Indique l’adresse de l’hôte du serveur où se trouvent vos données. </p> <p>Si vous le souhaitez, vous pouvez spécifier un chemin d’accès URI (Uniform Resource Identifier) complet au document de source de données, comme dans les exemples suivants : </p> <p> <code class="syntax html"> https://www.somewhere.com/some_path/some_file.tsv </code> </p> <p>ou </p> <p> <code class="syntax html"> ftp://user:password@ftpserver.somewhere.com/some_path/some_file.csv </code> </p> <p>L’URI est ventilé en entrées appropriées pour les champs Adresse de l’hôte, Chemin du fichier, Protocole et, éventuellement, Nom d’utilisateur et Mot de passe. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Chemin du fichier </p> </td> 
      <td colname="col2"> <p>Spécifie le chemin d’accès au document XML Principal qui contient plusieurs "lignes" d’informations. </p> <p>Le chemin d’accès est relatif à la racine de l’adresse hôte. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Protocole </p> </td> 
      <td colname="col2"> <p>Indique le protocole utilisé pour accéder au fichier. Vous pouvez choisir parmi les options suivantes : </p> <p> 
      <ul id="ul_976A34FD14A841F2B610C1C0CCBB82B9"> 
      <li id="li_05BBA0F670F14431A89AE4178F1A6F94"> HTTP <p>Si nécessaire, vous pouvez saisir des informations d’identification d’authentification appropriées pour accéder au serveur HTTP. </p> </li> 
      <li id="li_100446691F304572B8FC3F083F86A2CB"> HTTPS <p>Si nécessaire, vous pouvez saisir les informations d’identification d’authentification appropriées pour accéder au serveur HTTPS. </p> </li> 
      <li id="li_027088A8E30444DAA8CCCC5B0BAA74C1"> FTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur FTP. </p> </li> 
      <li id="li_DCEF9D5C99354990B03E29083C2ED8DC"> SFTP <p>Vous devez saisir les informations d’identification d’authentification appropriées pour accéder au serveur SFTP. </p> </li> 
      <li id="li_44E34FF2AB0D429EB3408106E6FCF780"> Fichier </li> 
      </ul> </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Itemtag </p> </td> 
      <td colname="col2"> <p>Identifie l’élément XML que vous pouvez utiliser pour identifier les lignes XML individuelles dans le fichier de source de données que vous avez spécifié. </p> <p>Par exemple, dans le fragment de flux suivant d’un document XML d’Adobe, la valeur de l’élément est <span class="codeph"> enregistrement </span> : </p> <p> <code class="syntax xml"> &lt;?xml&nbsp;version="1.0"&nbsp;encoding="utf-8"?&gt; 
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
      <td colname="col2"> <p>Spécifie un champ de métadonnées dont les valeurs sont utilisées comme "clés" de recherche dans les données de la configuration du chargeur d’attributs. Si aucune valeur n’est sélectionnée (<b>—None—</b>), les données de cette configuration ne sont pas disponibles pour une utilisation dans les calculs de classement (<b>Règles</b> &gt; <b>Règles de classement</b> &gt; <b>Modifier les règles</b>). Lorsque vous sélectionnez une valeur, les valeurs de ce champ sont utilisées pour effectuer des références croisées dans des documents de recherche/marchandisage de site avec les données de cette configuration. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Jours périmés </p> </td> 
      <td colname="col2"> <p>Définit l’intervalle minimum entre les téléchargements des données de chargeur d’attributs. Les téléchargements déclenchés par un index qui se produisent dans l’intervalle de fréquence d’actualisation des téléchargements sont ignorés. Lorsque vous définissez cette valeur sur la valeur par défaut de 1, les données du chargeur d’attributs ne se téléchargent pas plus d’une fois dans une période de 24 heures. Tous les index de recherche qui se produisent dans l’intervalle de fréquence d’actualisation des téléchargements utilisent le dernier jeu de données téléchargé. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Carte </p> </td> 
      <td colname="col2"> <p>Permet de spécifier des mappages XML-élément-vers-métadonnées à l’aide d’expressions XPath. </p> <p> 
      <ul id="ul_604108C0277C4892AE8A40CA39889ABD"> 
      <li id="li_0AF92270AE9F4BA8B2C7EE41FABC0F34"> <span class="uicontrol"> Baliser </span> <p>Spécifie une représentation XPath des données XML analysées. En utilisant l’exemple de document XML d’Adobe ci-dessus, sous l’option Itemtag, il peut être mappé à l’aide de la syntaxe suivante : </p> <p> <code class="syntax xml"> /record/@displayurl&nbsp;-&gt;&nbsp;page-url 
        /record/metadata/meta[@name='title']/@content&nbsp;-&gt;&nbsp;title 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;desc 
        /record/metadata/meta[@name='description']/@content&nbsp;-&gt;&nbsp;body </code> </p> <p>La syntaxe ci-dessus se traduit comme suit : </p> <p> 
        <ul id="ul_6400EBD08D424EADA1612FE4F7EFB640"> 
        <li id="li_9958F9B40D42434195597DBA9F2AF28F"> <code class="syntax xml"> /record/@displayurl&amp;nbsp;-&gt;&amp;nbsp;page-url </code> <p>L’attribut <span class="codeph"> display </span> de l’élément <span class="codeph"> enregistrement </span> est mappé au champ de métadonnées <span class="codeph"> page-url </span>. </p> </li> 
        <li id="li_759013EA02CD48BE971A55B0A6A11424"> <code class="syntax xml"> /record/metadata/meta[@name='title']/@content&amp;nbsp;-&gt;&amp;nbsp;title </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu à l'intérieur d'un élément <span class="codeph"> de métadonnées </span> contenu à l'intérieur d'un élément <span class="codeph"> d'enregistrement </span> dont l'attribut name est <span class="codeph"> title </span> est associé au champ de métadonnées <span class="codeph"> title &lt;a/&gt;.</span> </p> </li> 
        <li id="li_E741CA59197D462EB2946EDE874AFDC8"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;desc </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu à l'intérieur d'un élément <span class="codeph"> metadata </span> contenu à l'intérieur de l'élément <span class="codeph"> record </span> , dont l'attribut name est <span class="codeph"> description </span> est mappé au champ de métadonnées <span class="codeph"> desc &lt;a11111 1/&gt;.</span> </p> </li> 
        <li id="li_E35EAE3D284D46D485D9064D7BB6AB13"> <code class="syntax xml"> /record/metadata/meta[@name='description']/@content&amp;nbsp;-&gt;&amp;nbsp;body </code> <p>L'attribut <span class="codeph"> content </span> de tout élément <span class="codeph"> meta </span> contenu dans un élément <span class="codeph"> metadata </span> contenu dans l'élément <span class="codeph"> record </span> , dont l'attribut name est <span class="codeph"> description </span>, est associé au champ de métadonnées <span class="codeph"> corps </span>. </p> </li> 
        </ul> </p> <p>XPath est une notation relativement compliquée. Vous trouverez plus d’informations à l’emplacement suivant : </p> <p>Voir <a href="https://www.w3schools.com/xml/xpath_intro.asp" scope="external" format="html"> https://www.w3schools.com/xml/xpath_intro.asp </a> </p> </li> 
      <li id="li_8147075D7ACD4811A7ED335F23FE62A6"> <span class="uicontrol"> Champ </span> <p>Définit la valeur de l’attribut name utilisée pour chaque balise <span class="codeph"> &lt;meta&gt; </span> générée. </p> </li> 
      <li id="li_2380199D63BF425A919606D8232FA6E2"> <span class="uicontrol"> Métadonnées? </span> <p>Le champ <span class="uicontrol"> </span> devient une liste déroulante à partir de laquelle vous pouvez sélectionner des champs de métadonnées définis pour le compte actif. </p> <p>La valeur <span class="uicontrol"> Champ </span> peut être un champ de métadonnées non défini, si vous le souhaitez. Un champ de métadonnées non défini est parfois utile pour créer du contenu utilisé par <span class="wintitle"> Script de filtrage </span>. </p> <p>Voir <a href="../c-about-settings-menu/c-about-filtering-menu.md#concept_E56B73D625854AB2A899EF2D56CFCB47" type="concept" format="dita" scope="local"> À propos du filtrage des scripts </a>. </p> <p>Lorsque Attribute Loader traite des documents XML avec plusieurs accès sur n’importe quel champ de mappage, les valeurs multiples sont concaténées en une seule valeur dans le document mis en cache résultant. Par défaut, ces valeurs sont combinées à l’aide d’un délimiteur virgule. Cependant, supposons que la valeur <span class="wintitle"> de champ </span> correspondante soit un champ de métadonnées défini. En outre, ce champ a l’attribut <span class="wintitle"> Listes autorisées </span> . Dans ce cas, la valeur Délimiteurs de liste du champ, qui est le premier délimiteur défini, est utilisée dans la concaténation. </p> </li> 
      <li id="li_DEA24003E97E406DA2510C43CCFDC70E"> <span class="uicontrol"> Clé primaire? </span> <p>Un seul champ est identifié comme clé Principale. Ce champ sera utilisé comme "clé étrangère" pour faire correspondre les données du chargeur d’attributs au document correspondant dans l’index. </p> </li> 
      <li id="li_80D6AF130FCE40AC972FE4B605B86BF6"> <span class="uicontrol"> Bande du code HTML ?  </span> <p>Lorsque cette option est cochée, toutes les balises HTML figurant dans les données de ce champ sont supprimées. </p> </li> 
      <li id="li_D40E2F9AD8AD49FC9AC4B8C75BA31E28"> <span class="uicontrol"> Action  </span> <p>Permet d’ajouter des lignes à la carte ou de supprimer des lignes de la carte. L’ordre des lignes n’est pas important. </p> </li> 
      </ul> </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. (Facultatif) Cliquez sur **[!UICONTROL Setup Maps]** pour télécharger un exemple de votre source de données. Les données sont examinées pour en déterminer la compatibilité.
1. Cliquez sur **[!UICONTROL Add]** pour ajouter la configuration à la page [!DNL Attribute Loader Definitions].
1. Sur la page [!DNL Attribute Loader Definitions], cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la page [!DNL Attribute Loader Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Modification d’une définition de chargeur d’attributs {#task_AA2D1B2BCAFA44A6A0C59A0318274E80}

Vous pouvez modifier un chargeur d’attributs existant que vous avez défini.

>[!NOTE]
>
>Pour utiliser le chargeur d’attributs, vous devrez peut-être l’activer dans votre compte par le représentant de votre compte d’Adobe ou par l’assistance Adobe.

Toutes les options de chargeur d’attributs ne sont pas disponibles pour que vous puissiez les modifier, comme le nom ou le type du chargeur d’attributs dans la liste déroulante [!DNL Type].

**Pour modifier une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Edit]** pour un nom de définition de chargeur d’attributs dont vous souhaitez modifier les paramètres.
1. Sur la page [!DNL Attribute Loader Edit], définissez les options de votre choix.

   Consultez le tableau des options sous [Ajout d’une définition de chargeur d’attributs](../c-about-settings-menu/c-about-metadata-menu.md#task_A735E5EF763343A9B675E1A3B09AFDBC).
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la page [!DNL Attribute Loader Definitions], cliquez sur **[!UICONTROL rebuild your staged site index]**.
1. (Facultatif) Sur la page [!DNL Attribute Loader Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Copie d’une définition de chargeur d’attributs {#task_9B40D5ECFC81411E9480F62A0FD5F2E0}

Vous pouvez copier une définition de chargeur d’attributs existante à utiliser comme base d’un nouveau chargeur d’attributs que vous souhaitez créer.

>[!NOTE]
>
>Pour utiliser le chargeur d’attributs, vous devrez peut-être l’activer dans votre compte par le représentant de votre compte d’Adobe ou par l’assistance Adobe.

Lors de la copie d’une définition de chargeur d’attributs, la définition copiée est désactivée par défaut. Pour activer ou &quot;activer&quot; la définition, vous devez la modifier à partir de la page [!DNL Attribute Loader Edit] et sélectionner **[!UICONTROL Enable]**.

Voir [Modification d’une définition de chargeur d’attributs](../c-about-settings-menu/c-about-metadata-menu.md#task_AA2D1B2BCAFA44A6A0C59A0318274E80).

**Pour copier une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Copy]** pour un nom de définition de chargeur d’attributs dont vous souhaitez dupliquer les paramètres.
1. Sur la page [!DNL Attribute Loader Copy], saisissez le nouveau nom de la définition.
1. Cliquez sur **[!UICONTROL Copy]**.
1. (Facultatif) Sur la page [!DNL Attribute Loader Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Changement du nom d’une définition de chargeur d’attributs {#task_58D5DFD7EBC04111BCB91118E4440DB4}

Vous pouvez modifier le nom d’une définition de chargeur d’attributs existante.

>[!NOTE]
>
>Pour utiliser le chargeur d’attributs, vous devrez peut-être l’activer dans votre compte par le représentant de votre compte d’Adobe ou par l’assistance Adobe.

**Pour renommer une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Rename]** pour le nom de définition du chargeur d’attributs que vous souhaitez modifier.
1. Sur la page [!DNL Attribute Loader Rename] , saisissez le nouveau nom de la définition dans le champ [!DNL Name] .
1. Cliquez sur **[!UICONTROL Rename]**.
1. (Facultatif) Sur la page [!DNL Attribute Loader Definitions], effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Publication des paramètres de l’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Chargement des données du chargeur d’attributs {#task_2F3C55189B0A4049AB2113F2291CC181}

Vous pouvez télécharger les données configurées du chargeur d’attributs dans la recherche/le marchandisage sur site.

La page [!DNL Data Load] affiche les informations suivantes sur l’état de votre dernière opération de chargement de données de chargeur d’attributs :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Champ d’état </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>État </p> </td> 
   <td colname="col2"> <p>Indique la réussite ou l’échec de la dernière tentative de chargement de données. Ou, il affiche l’état d’une opération de chargement de données déjà en cours. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Heure de début </p> </td> 
   <td colname="col2"> <p>Affiche la date et l’heure de début de la dernière opération de chargement de données. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Heure d’arrêt </p> </td> 
   <td colname="col2"> <p>Affiche la date et l’heure de fin de la dernière opération de chargement de données. Il indique également que l’opération de chargement des données en cours est toujours en cours. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Pour charger les données de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader Definitions], cliquez sur **[!UICONTROL Load Attribute Loader Data]**.
1. Sur la page **[!UICONTROL Attribute Loader Data Load]**, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Start Load]** pour lancer l’opération de chargement.

      Lors d’une opération de chargement de données, la ligne **Progression** fournit des informations sur sa progression.

   * Cliquez sur **[!UICONTROL Stop Load]** pour arrêter l’opération de chargement.

1. Cliquez sur **[!UICONTROL Close]** pour revenir à la page [!DNL Attribute Loader Definitions].

## Aperçu des données de chargeur d’attributs {#task_735CDCC1D8174B7B9F5B8E0AFA5F0CA0}

Vous pouvez utiliser l’aperçu pour afficher vos données de chargeur d’attributs les plus récemment chargées.

La colonne Ligne du tableau indique le numéro de chaque ligne de données, indiquant l’ordre d’origine du chargement des valeurs du chargeur d’attributs.

Les autres colonnes affichent les valeurs associées à chaque entrée.

Si la table est vide, cela signifie que vous n’avez pas encore chargé de données de chargeur d’attributs. Vous pouvez fermer la page [!DNL Attribute Loader Data Preview], puis charger les données du chargeur d’attributs.

Voir [Chargement des données du chargeur d’attributs](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Pour prévisualiser les données de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader Definitions], sous la colonne [!DNL Actions], cliquez sur **[!UICONTROL Preview]** pour la configuration dont vous souhaitez afficher les données téléchargées.
1. Sur la page [!DNL Attribute Loader Data Preview] , utilisez les options de navigation et d’affichage en haut et en bas de la page pour afficher les données.

   Cliquez sur un en-tête de colonne du tableau pour trier les données par ordre croissant ou décroissant.
1. Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Download to Desktop]** pour télécharger et enregistrer la table sous la forme d’un fichier .xlt.
   * Fermez la page lorsque vous avez terminé de prévisualiser les données du chargeur d’attributs et revenez à la page précédemment consultée.

## Affichage des paramètres d’une définition de chargeur d’attributs {#task_EA99A9694FE948ADA82C1DBA0667851B}

Vous pouvez consulter les paramètres de configuration d’une définition de chargeur d’attributs existante.

Une fois qu’une définition de chargeur d’attributs est ajoutée à la page [!DNL Attribute Loader Definitions] , vous ne pouvez pas modifier son paramètre Type . Vous devez plutôt supprimer la définition, puis en ajouter une nouvelle.

>[!NOTE]
>
>Pour utiliser le chargeur d’attributs, vous devrez peut-être l’activer dans votre compte par le représentant de votre compte d’Adobe ou par l’assistance Adobe.

**Pour afficher les paramètres d’une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Edit]** pour un nom de définition de chargeur d’attributs dont vous souhaitez modifier les paramètres.

## Affichage du journal à partir de la charge de données la plus récente d’Attribute Loader {#task_9C7D6E34BB6C4A40B7CA3EE36ACB0837}

Vous pouvez utiliser [!DNL View Log] pour examiner le fichier de log de données Attribute Loader du processus de téléchargement le plus récent. Vous pouvez également utiliser la vue Journal pour surveiller un téléchargement en cours d’exécution.

Voir [Chargement des données du chargeur d’attributs](../c-about-settings-menu/c-about-metadata-menu.md#task_2F3C55189B0A4049AB2113F2291CC181).

**Pour afficher le journal à partir de la charge de données la plus récente d’Attribute Loader**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader Definitions], cliquez sur **[!UICONTROL View Log]**. Page Journal,
1. Sur la page [!DNL Attribute Loader Data Log] , utilisez les options de navigation et d’affichage en haut et en bas de la page pour afficher les informations du journal.
1. Une fois que vous avez terminé, fermez la page pour revenir à la page [!DNL Attribute Loader Definitions].

## Suppression d’une définition de chargeur d’attributs {#task_E8980F66888B476E98C228C1D307EDF8}

Vous pouvez supprimer une définition de chargeur d’attributs existante dont vous n’avez plus besoin ou que vous n’utilisez plus.

>[!NOTE]
>
>Pour utiliser le chargeur d’attributs, vous devrez peut-être l’activer dans votre compte par le représentant de votre compte d’Adobe ou par l’assistance Adobe.

**Pour supprimer une définition de chargeur d’attributs**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Attribute Loader]**.
1. Sur la page [!DNL Attribute Loader Definitions], sous l’en-tête de colonne [!DNL Actions], cliquez sur **[!UICONTROL Delete]** pour le nom de définition du chargeur d’attributs à supprimer.
1. Sur la page [!DNL Attribute Loader Delete], cliquez sur **[!UICONTROL Delete]**.
