---
description: Lisez les questions fréquentes sur Search&amp;Promote
solution: Target
title: Questions fréquentes
topic-legacy: Appendices,Site search and merchandising
uuid: 4ce454a4-e770-4587-91a0-a25491818ac6
exl-id: 2bb1da04-62f9-4f8c-bee4-5511d8cb2582
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '8643'
ht-degree: 0%

---

# Questions fréquentes{#frequently-asked-questions}

## Flash d&#39;Adobe {#reference_4A25BBDE32214AF5A1A454F38FD51243}

Page de questions fréquentes qui traite de la prise en charge de l’indexation et de la recherche de fichiers SWF sur un site Web.

Voici quelques questions courantes concernant les fichiers SWF :

* [Quand un fichier SWF est-il analysé et indexé ?](#section_01BB5259140D4D5FB04CCB7A1A63DE99)
* [Que dois-je faire pour indexer un SWF...](#section_0A6A52CC70D4495BBE14D91906318F95)
* [Comment les fichiers SWF sont-ils reconnus ?](#section_B36C0536AB544F509601DC6A11A8E656)
* [Comment les fichiers SWF sont-ils indexés ?](#section_36856058A4B54FA5ABF921344F50410C)
* [Un fichier SWF est-il comptabilisé comme une page ?](#section_0158D6DE70BC40D78E2374787B9F58AB)
* [Comment empêcher l&#39;indexation de fichiers SWF individuels...](#section_E38AD37989EF410B97AF5125057BFD22)
* [Comment empêcher l&#39;indexation des fichiers SWF ?](#section_DF2606A50E9A44859CFA0D44D7C5F2E4)
* [Comment se fait-il que je ne puisse pas rechercher les fichiers SWF chinois, japonais ou coréens sur mon site Web ?](#section_EE1A3A705AE74148BD195A0CE513A5C4)

## Quand un fichier SWF est-il analysé et indexé ? {#section_01BB5259140D4D5FB04CCB7A1A63DE99}

Un fichier SWF est analysé et indexé s’il est contenu dans une balise d’objet ou d’incorporation sur une page HTML, comme dans l’exemple suivant :

```
<embed src="Flash-file-URL">  
 
<object>  
<param name=movie value="Flash-file-URL">  
</object> 
```

Un fichier SWF est également reconnu si vous listes l’URL du fichier comme point d’entrée.

Voir [Ajouter plusieurs points d’entrée d’URL que vous souhaitez indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Que dois-je faire pour indexer un fichier SWF ? {#section_0A6A52CC70D4495BBE14D91906318F95}

Pour analyser et indexer des fichiers SWF, sélectionnez le type de contenu **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Tant que votre fichier de Flash est référencé à partir d’une balise `<embed>` ou d’une balise `<object>` dans un document HTML, le texte est indexé et toutes les URL répertoriées dans le fichier sont analysées.

Si votre fichier n’est référencé ni à partir d’une balise `<embed>` ni d’une balise `<object>`, vous pouvez liste le fichier SWF dans une balise `<a href=...>` dans un document HTML ou en tant que point d’entrée d’URL.

Voir [Ajouter plusieurs points d’entrée d’URL que vous souhaitez indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Comment les fichiers SWF sont-ils reconnus ? {#section_B36C0536AB544F509601DC6A11A8E656}

Les fichiers SWF sont identifiés par le type MIME suivant :

`application/x-shockwave-flash`

Les fichiers SWF sont également reconnus avec les types MIME `application/octet-stream`&quot; ou `text/plain`, à condition que l’extension de fichier soit .swf.

Un serveur mal configuré peut utiliser un type MIME différent pour les fichiers SWF. Assurez-vous de vérifier la configuration de votre serveur si vous rencontrez des problèmes d’analyse et d’indexation des fichiers SWF.

## Comment les fichiers SWF sont-ils indexés ? {#section_36856058A4B54FA5ABF921344F50410C}

Le texte contenu dans un fichier SWF est indexé comme s’il s’agissait de `<body>` texte dans la page HTML encadrée. Si un résultat de recherche trouve du texte contenu dans un fichier SWF incorporé, le résultat est en fait lié à la page HTML encadrée et non au fichier SWF. Ainsi, le fichier SWF s’affiche dans le contexte approprié.

Si un fichier SWF contient une URL en tant qu’action &quot;Charger un film&quot;, le texte du fichier SWF référencé est indexé dans le cadre de la page HTML encadrée.

Si un fichier SWF contient une URL en tant qu’action &quot;Get URL&quot;, l’URL est analysée et indexée ultérieurement, tout comme une référence HTML `<a href=...>` est analysée et indexée ultérieurement.

Si un fichier SWF est répertorié comme point d’entrée d’URL, le texte du fichier SWF est indexé en tant que page unique. Résultat de la recherche qui recherche le texte d’un fichier SWF de point d’entrée et qui renvoie directement à la séquence, et non à une page HTML encadrée.

Voir [Ajouter plusieurs points d’entrée d’URL que vous souhaitez indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Un fichier SWF est-il comptabilisé comme une page ? {#section_0158D6DE70BC40D78E2374787B9F58AB}

Non. Un fichier SWF est considéré comme faisant partie de sa page HTML encadrée. Toutes les URL de &quot;chargement de film&quot; contenues dans des fichiers SWF sont également considérées comme faisant partie de la page HTML encadrée. Par conséquent, les fichiers SWF référencés à partir d’une page HTML ne sont pas comptabilisés comme une &quot;page&quot; pour le total de la page du compte.

Si un fichier SWF est répertorié comme point d’entrée d’URL, ce fichier SWF et toutes les URL &quot;Load Movie&quot; répertoriées dans ce fichier SWF sont comptés comme une &quot;page&quot; pour le total de pages du compte.

## Comment empêcher l’indexation de fichiers SWF individuels ? {#section_E38AD37989EF410B97AF5125057BFD22}

Pour empêcher l’indexation d’un fichier SWF, vous pouvez ajouter une balise meta ( `<meta name="ROBOTS" content="NOINDEX">`) ou une balise `<noindex>` robots au document HTML englobant. En d’autres termes, document contenant la balise `<embed>` ou `<object>`.

Vous pouvez également utiliser la balise meta robots ( `<meta name="ROBOTS" content="NOFOLLOW">`) pour empêcher les URL suivantes contenues dans le fichier SWF. Si le document HTML encadré est désactivé, les URL répertoriées comme actions &quot;Get URL&quot; dans le fichier SWF ne sont pas suivies.

## Comment empêcher l’indexation des fichiers SWF sur mon site Web ? {#section_DF2606A50E9A44859CFA0D44D7C5F2E4}

Pour désactiver l’indexation SWF, désélectionnez le type de contenu **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Vous pouvez également choisir d’utiliser [!DNL URL Masks] pour désactiver l’indexation des fichiers SWF.

Voir [Ajouter des masques d&#39;URL pour indexer ou non des parties d&#39;index de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Pour désactiver l’indexation SWF, saisissez l’un des masques d’URL suivants :

* `exclude *.swf` (si vous n’utilisez pas d’expressions régulières)
* `exclude regexp ^.*\.swf$` (si vous utilisez des expressions régulières)

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Comment se fait-il que je ne puisse pas rechercher les fichiers SWF chinois, japonais ou coréens sur mon site Web ? {#section_EE1A3A705AE74148BD195A0CE513A5C4}

La recherche/marchandisage sur site obtient UTF-8 à partir des fichiers SWF créés avec un Flash d’Adobe. L&#39;UTF-8 ne contient aucune indication de langue. Si vous avez sélectionné le type de contenu **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier la langue utilisée par le fichier SWF.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

Les fichiers SWF plus anciens ne spécifient pas non plus de jeu de caractères. Si vous avez sélectionné le type de contenu SWF **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser les injections de métadonnées pour spécifier le jeu de caractères utilisé dans le fichier SWF.

## Recherche générale {#reference_E2C675162789452A9B99C6633B12CBEF}

Page de questions fréquentes qui explique comment la recherche/le marchandisage sur le site aide les clients qui visitent votre site Web à trouver ce qu’ils recherchent.

Les questions courantes relatives à la recherche générale sont les suivantes :

* [Dois-je installer un logiciel pour utiliser le site ?..](#section_02AB2AFF71984F9DAA3AF2B7C0847A22)
* [Que se passe-t-il lorsque mon site dépasse la limite de page ?](#section_ECA5FA01032D4322BABA4E2C7FE498C1)
* [Comment puis-je changer l&#39;adresse e-mail où la semaine...](#section_AE27F63DD13F425B940C8E7D9ED5C614)
* [Quelles sont les informations de mes clients sur la recherche/le marchandisage sur le site ?](#section_5484CB954167412BB7F0480CB0C504B8)
* [Qu&#39;en est-il de la confidentialité de mes informations client ?](#section_8FB493F15E51454BA92A0C83E14C0CC7)
* [Puis-je afficher mes propres bannières publicitaires sur la recherche...](#section_611EB8B32C16418386CB7DC7FB6954B8)

Voici quelques questions courantes concernant les fonctionnalités de recherche :

* [Puis-je personnaliser les résultats de la recherche pour mon site ?](#section_A64B3A621B794DF78D35ED06D9C43D0B)
* [Puis-je voir ce que les clients recherchent sur mon...](#section_73709E1B0E82478DA7B4D15B6C845F33)
* [Comment puis-je contrôler quels types de contenu (PDF, texte, Flash, MP3 et Microsoft Office) sont indexés et recherchés ?](#section_0AB8CB4B6BFA4286AA082055FEBFBE1C)
* [Les pages Web générées de manière dynamique sont-elles prises en charge au moyen de contenu ASP, JSP, PHP, CFM ou Perl ?](#section_E279F004F1C542A2B9773B832E7B013F)
* [Comment puis-je utiliser des synonymes pour améliorer les résultats de la recherche...](#section_E6E36E12514F4D7BAB01F8D1AB61D57B)
* [Ai-je le contrôle sur l&#39;ordre des résultats de la recherche...](#section_C6361048502745779D9749A842C4C370)
* [Puis-je modifier la langue de la page des résultats de la recherche...](#section_6EE41DA8241247D48BBEB061A50599C5)
* [Puis-je avoir plus d&#39;un site sur mon Adobe...](#section_AFA8825182094660A71EEC84B8329D6D)
* [Puis-je rechercher plusieurs domaines ?](#section_BFBB0E9861D942F095B56CF0A8F16596)
* [Puis-je subdiviser mon site en sections distinctes pour que...](#section_52153A9DE9F9493B967A70583848B2A4)
* [Comment puis-je exclure certaines parties de mon site Web de...](#section_D452EDE153654EF398F4A87780C6D43B)
* [Quels jeux de caractères sont pris en charge ?](#section_A62A6F8F15804F968C77F2DEBDE8F8FD)
* [Que se passe-t-il si je modifie ou mets à jour mon site Web ?](#section_489050E0EBC14D0594DBBAA0CCF4F6BA)
* [Mon site peut-il être automatiquement indexé ?](#section_9C7D41636238488691ECDFEE4D4E5103)
* [J&#39;utilise des mots de passe sur mon site web. Puis-je toujours utiliser la recherche/le marchandisage sur le site ?](#section_4618EB5B66704640B5502D1B5CB4B32E)
* [Soutenez-vous l&#39;analyse et l&#39;indexation de https ou...](#section_D5BB8B8FBEA4405583E86B4AEC37151B)
* [Est-ce que la recherche et le marchandisage sur le site respectent le fichier robots.txt sur mon site Web ?](#section_73BBF6FE93C64C109F45CBC2FA394DB2)
* [Certaines parties de mon site Web doivent être mises à jour fréquemment...](#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3)
* [Puis-je utiliser des scripts ou des programmes pour lancer une incrémentation...](#section_0B6BB039557A42AA876D35D748E17DD0)

## Dois-je installer un logiciel pour utiliser la recherche/le marchandisage sur le site ? {#section_02AB2AFF71984F9DAA3AF2B7C0847A22}

Non. Il s&#39;agit de l&#39;avantage Principal de la recherche et du marchandisage sur le site. Le moteur est une application professionnelle hébergée et gérée entièrement sur nos serveurs hautes performances. Cela rend le logiciel plus facile à utiliser que les autres solutions de recherche. La seule chose à faire est d&#39;ajouter une petite quantité de code HTML à vos pages afin que les clients de votre site Web puissent entrer des recherches. La recherche/marchandisage sur site prend en charge tout le reste.

## Que se passe-t-il lorsque mon site dépasse la limite de page ? {#section_ECA5FA01032D4322BABA4E2C7FE498C1}

Nous continuons à effectuer vos recherches afin que vos visiteurs puissent rechercher votre site sans interruption. Pour savoir si votre site Web dépasse la limite de page, vérifiez votre état d’index complet ou votre journal en direct.

Voir [A propos de l&#39;index complet](../c-about-index-menu/c-about-full-index.md#concept_C69BD21863FD4856B49326F35DB570D3).

Voir [Affichage du journal d&#39;index complet d&#39;un fichier actif ou d&#39;un fichier d&#39;évaluation...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

## Comment puis-je modifier l’adresse électronique à laquelle les rapports hebdomadaires sont envoyés ? {#section_AE27F63DD13F425B940C8E7D9ED5C614}

Des rapports hebdomadaires sont envoyés au propriétaire de chaque compte principal. Vous pouvez modifier l’adresse électronique en cliquant sur **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**. Si vous avez plusieurs comptes de recherche principaux, toutes les bulletins d&#39;information sont envoyées à la nouvelle adresse.

Voir [Configuration de vos informations utilisateur personnelles](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

## Quelles sont les informations de mes clients sur la recherche/le marchandisage sur le site ? {#section_5484CB954167412BB7F0480CB0C504B8}

La recherche et le marchandisage sur site sont sécurisés, rapides, stables et faciles à utiliser. Vous n&#39;êtes pas obligé d&#39;utiliser des cookies (même si vous le pouvez si vous le souhaitez) pour utiliser nos produits, et les informations sensibles, telles que les mots de passe, ne sont jamais placées sur un lien URL qui peut être récupéré ultérieurement à partir de votre navigateur.

## Qu&#39;en est-il de la confidentialité de mes informations client ? {#section_8FB493F15E51454BA92A0C83E14C0CC7}

Adobe s&#39;engage à respecter la vie privée de ses clients et visiteurs. Consultez l&#39;Adobe [Centre de traitement des données personnelles](https://www.adobe.com/privacy.html).

## Puis-je afficher mes propres bannières publicitaires dans les pages de résultats de la recherche ? {#section_611EB8B32C16418386CB7DC7FB6954B8}

Oui. Vous contrôlez l&#39;apparence et le contenu des résultats de la recherche. Dans le modèle de résultats de recherche de votre site Web, vous pouvez créer des liens vers votre propre réseau d&#39;échange de bannières, tel que LinkExchange ou SmartClicks. Tous les accès effectués par vos visiteurs sont correctement crédités à votre compte d’échange de bannières.

## Puis-je personnaliser les résultats de la recherche pour mon site ? {#section_A64B3A621B794DF78D35ED06D9C43D0B}

Oui. Il s&#39;agit d&#39;une fonction exclusive de recherche/marchandisage sur le site. Grâce à notre technologie de modèle avancée et à une connaissance limitée du code HTML, vous pouvez contrôler exactement l&#39;apparence des résultats de recherche.

Voir [Rechercher des balises de modèle](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

La transition entre vos propres serveurs et les serveurs de recherche/marchandisage de site est totalement transparente et invisible pour vos clients. Si vous ne connaissez pas HTML ou si vous n&#39;avez pas le temps de créer un modèle personnalisé, vous pouvez choisir parmi un assortiment de modèles attrayants et prêts à l&#39;emploi que l&#39;équipe interne de développeurs Web professionnels du Adobe crée.

## Puis-je identifier les clients qui recherchent sur mon site ? {#section_73709E1B0E82478DA7B4D15B6C845F33}

Oui. Nous conservons les statistiques de recherche pour les recherches effectuées par des visiteurs sur votre site Web au cours des deux derniers mois. Vous pouvez consulter ces statistiques à tout moment sous Rapports dans le menu du produit. Les rapports de recherche vous fournissent des informations essentielles sur ce que les visiteurs recherchent exactement sur votre site Web. Vous pouvez utiliser ces informations pour améliorer la conception ou pour ajuster le moteur de recherche/marchandisage du site afin de mieux servir vos visiteurs.

## Comment puis-je contrôler quels types de contenu (PDF, texte, Flash, MP3 et Microsoft Office) sont indexés et recherchés ? {#section_0AB8CB4B6BFA4286AA082055FEBFBE1C}

Vous pouvez facilement configurer des comptes pour activer ou désactiver l’indexation et la recherche de texte dans les documents PDF, les documents de texte brut, les films de Flash, les fichiers MP3 ou les documents Microsoft Office.

Ces paramètres sont contrôlés sur la page [!DNL Staged Content Types].

Voir [A propos des types de contenu](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Les pages Web générées de manière dynamique sont-elles prises en charge au moyen de contenu ASP, JSP, PHP, CFM ou Perl ? {#section_E279F004F1C542A2B9773B832E7B013F}

Les pages Web HTML statiques ou générées dynamiquement sont indexées, y compris les pages créées à partir de bases de données ou tout autre processus principal. Le code HTML visible par un navigateur étant indexé, vous pouvez utiliser la recherche/marchandisage de site sur les sites Web tant que ces architectures dorsales génèrent des pages HTML.

Le robot de recherche analyse votre site Web en commençant par la première page à l’adresse spécifiée dans [!DNL Account Settings] et suit les liens d’une page à l’autre.

Voir [Configuration des paramètres de votre compte](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Lorsque le robot de recherche analyse et indexe toutes les pages de votre site Web, vous pouvez utiliser le moteur de recherche pour effectuer des recherches sur votre site. En d’autres termes, si des documents générés dynamiquement sont tissés dans votre site Web avec des liens d’autres pages, le robot de recherche peut toujours analyser et indexer le contenu dynamique.

Une fois le contenu de votre site Web analysé et indexé, les clients de votre site Web peuvent rechercher des informations dans le contenu indexé.

## Comment puis-je utiliser des synonymes pour améliorer les résultats de la recherche sur mon site ? {#section_E6E36E12514F4D7BAB01F8D1AB61D57B}

Vous pouvez utiliser des synonymes lorsque vous souhaitez que les visiteurs trouvent des pages qui sont liées à leur requête de recherche.

Supposons, par exemple, que votre page comporte une liste de prix des produits à vendre sur votre site. Cependant, après avoir examiné les rapports de recherche fournis par la recherche/le marchandisage sur le site, vous constatez que les clients recherchent le mot &quot;coût&quot;, &quot;frais&quot;, &quot;frais&quot; ou &quot;frais&quot; dans leurs recherches. Ces mots n&#39;affichent pas votre page de liste de prix dans les résultats de la recherche. Avec la fonction [!DNL Add Synonyms] de [!DNL Dictionaries], vous pouvez spécifier que ces mots sont tous des synonymes et votre client peut trouver votre liste de prix, quel que soit le terme de recherche utilisé.

Voir [A propos des dictionnaires](../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034).

## Ai-je le contrôle sur l&#39;ordre des résultats de la recherche ? {#section_C6361048502745779D9749A842C4C370}

Oui. L&#39;interface de pertinence avancée vous permet de contrôler les pages renvoyées pour une requête de recherche spécifique. Cette fonctionnalité est utile si vous souhaitez vous assurer que les clients voient une page spécifique lorsqu&#39;ils requête certains mots.

Voir [Ajouter un nouveau champ de balise meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Puis-je modifier la langue de la page des résultats de la recherche ? {#section_6EE41DA8241247D48BBEB061A50599C5}

Oui. Le modèle de recherche/marchandisage de site est flexible lorsqu&#39;il s&#39;agit de vous permettre de créer une page de résultats qui utilise la langue de votre choix et correspond à l&#39;apparence de votre site Web.

Le modèle se compose d’une combinaison de texte, de balises HTML standard et de balises spéciales définies pour afficher les résultats de la recherche. Lorsqu’un client effectue une recherche, le robot de recherche lit le modèle, génère le texte à l’aide de balises HTML standard et insère les liens de résultats en fonction des balises de modèle spéciales.

Voir [Rechercher des balises de modèle](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

Si vous souhaitez modifier la langue des résultats, vous pouvez modifier le texte anglais qui s’affiche sur le modèle.

Voir [Modification d&#39;une présentation ou d&#39;un modèle de transport](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3).

## Puis-je avoir plusieurs sites sur mon identifiant de client d&#39;Adobe ? {#section_AFA8825182094660A71EEC84B8329D6D}

Oui. Avec la connexion client d’un seul Adobe, vous pouvez gérer un moteur de recherche différent pour de nombreux sites Web différents. Sélectionnez et gérez des comptes sous &quot;Comptes&quot;.

Voir [Sélection d&#39;un autre compte à utiliser](../c-about-accounts-menu.md#task_03C0FE918E2D44529CDC3B8DB75D1B26).

## Puis-je rechercher plusieurs domaines ? {#section_BFBB0E9861D942F095B56CF0A8F16596}

Oui. Vous pouvez configurer l&#39;accès à plusieurs domaines à l&#39;aide de [!DNL URL Entrypoints]. Fournissez des points d’entrée d’URL pour les domaines supplémentaires que vous détenez. N’oubliez pas que vous devez disposer de l’autorisation d’indexer des domaines que vous ne possédez pas.

Voir [A propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Puis-je subdiviser mon site en sections distinctes afin que les clients puissent effectuer des recherches dans l&#39;une de ces zones individuellement ou sur l&#39;ensemble du site ? {#section_52153A9DE9F9493B967A70583848B2A4}

Oui. Une fonctionnalité &quot;Collections&quot; est incluse, qui permet aux clients de rechercher des zones spécifiques de votre site Web afin de trouver rapidement ce qu’ils recherchent.

Voir [A propos des collections](../c-about-settings-menu/c-about-searching-menu.md#concept_62E42ACE53D54EEE9273433B86259127).

Par exemple, les clients peuvent rechercher une collection d&#39;URL liées aux informations de vente de produits ou une collection d&#39;URL liées aux services d&#39;assistance. Vous pouvez configurer des collections afin que vos clients voient une liste déroulante de collections ou un groupe de cases à cocher.

## Comment puis-je empêcher la recherche de certaines parties de mon site Web ? {#section_D452EDE153654EF398F4A87780C6D43B}

Oui. Spécifiez des masques d’URL pour déterminer les pages de site Web que vous souhaitez inclure ou exclure de l’indexation. Les masques d’URL déterminent si les pages du site Web apparaissent dans les résultats de la recherche.

Voir [A propos des masques d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Voir [A propos du script de masques d’URL](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B).

Pour empêcher la recherche de parties de pages Web individuelles, vous pouvez exclure certaines parties d’une page de l’indexation. Entourez le texte de balises `<noindex>` et `</noindex>`. Cette méthode est utile si vous souhaitez exclure le texte de navigation des recherches.

## Quels jeux de caractères sont pris en charge ? {#section_A62A6F8F15804F968C77F2DEBDE8F8FD}

Les pages Web spécifient généralement le jeu de caractères avec une balise meta semblable à ce qui suit :

`<META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=iso-8859-1">`

Le moteur de recherche/marchandisage du site indexe correctement les pages Web en utilisant tous les jeux de caractères courants utilisés sur Internet aujourd&#39;hui. Voici quelques-uns des jeux de caractères pris en charge :

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Arabe (ISO-8859-6) </p> </td> 
   <td colname="col2"> <p>Chinois (traditionnel); Big5) </p> </td> 
   <td colname="col3"> <p>Japonais (Shift_JIS) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Arabe (Windows-1256) </p> </td> 
   <td colname="col2"> <p>Chinois (traditionnel); EUC-TW) </p> </td> 
   <td colname="col3"> <p>Russe (KOI8-R) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Baltique (ISO-8859-4) </p> </td> 
   <td colname="col2"> <p>Cyrillique (ISO-8859-5) </p> </td> 
   <td colname="col3"> <p>Europe du Sud (ISO-8859-3) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Baltique (Windows-1257) </p> </td> 
   <td colname="col2"> <p>Cyrillique (Windows-1251) </p> </td> 
   <td colname="col3"> <p>Turc (ISO-8859-9) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe centrale (ISO-8859-2) </p> </td> 
   <td colname="col2"> <p>Grec (ISO-8859-7) </p> </td> 
   <td colname="col3"> <p>Turc (Windows-1254) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Europe centrale (Windows-1250) </p> </td> 
   <td colname="col2"> <p>Grec (Windows-1253) </p> </td> 
   <td colname="col3"> <p>Unicode (UTF-8) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (ISO-2022-CN) </p> </td> 
   <td colname="col2"> <p>Hébreu (ISO-8859-8) </p> </td> 
   <td colname="col3"> <p>US-ASCII (us-ascii) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (ISO-2022-CN-EXT) </p> </td> 
   <td colname="col2"> <p>Hébreu (Windows-1255) </p> </td> 
   <td colname="col3"> <p>Europe occidentale (ISO-8859-1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (simplifié); EUC-CN) </p> </td> 
   <td colname="col2"> <p>Japonais (EUC-JP) </p> </td> 
   <td colname="col3"> <p>Europe occidentale (ISO-8859-15) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (simplifié); GB2312) </p> </td> 
   <td colname="col2"> <p>Japonais (ISO-2022-JP) </p> </td> 
   <td colname="col3"> <p>Europe occidentale (Windows-1252) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (simplifié); GBK) </p> </td> 
   <td colname="col2"> <p>Japonais (ISO-2022-JP-1) </p> </td> 
   <td colname="col3"> <p>Europe occidentale (x-mac-roman) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Chinois (simplifié); HZ-GB-2312) </p> </td> 
   <td colname="col2"> <p>Japonais (ISO-2022-JP-2) </p> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

Contactez le support technique pour obtenir des informations sur les jeux de caractères qui ne sont pas répertoriés ci-dessus.

## Que se passe-t-il si je modifie ou mets à jour mon site Web ? {#section_489050E0EBC14D0594DBBAA0CCF4F6BA}

Après avoir modifié le contenu de votre site Web, vous pouvez effectuer un index complet ou incrémentiel. La recherche sur site/le marchandisage télécharge et indexe tout contenu de site Web modifié. Une fois l’indexation terminée, vos clients peuvent rechercher le nouveau contenu. Vous pouvez également programmer une indexation automatique de votre site à un moment donné et un jour donné.

Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Voir [Exécution d’un index incrémentiel d’un site Web dynamique ou d’un site Web intermédiaire..](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Voir [Définition du calendrier complet de l&#39;index pour un site Web actif](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0).

Voir [Définition de la planification de l&#39;index incrémentiel pour un site Web actif](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Mon site peut-il être automatiquement indexé ? {#section_9C7D41636238488691ECDFEE4D4E5103}

Oui. Vous pouvez planifier un index automatique de votre site tous les jours.

Outre l’indexation automatique quotidienne, vous pouvez choisir d’avoir fréquemment modifié des portions de leur site par incréments. Les jours où un index automatique est planifié, vous pouvez contrôler l’heure de la journée où l’index a lieu. De plus, vous pouvez toujours lancer manuellement un index de site lorsque vous le souhaitez.

Voir [Définition du calendrier complet de l&#39;index pour un site Web actif](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0).

Voir [Définition de la planification de l&#39;index incrémentiel pour un site Web actif](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## J&#39;utilise des mots de passe sur mon site web. Puis-je toujours utiliser la recherche/le marchandisage sur le site ? {#section_4618EB5B66704640B5502D1B5CB4B32E}

Si vous utilisez l’authentification de base HTTP pour protéger par mot de passe certaines parties de votre site Web, vous pouvez spécifier les domaines et mots de passe que la recherche/marchandisage du site peut utiliser pour indexer votre site.

Voir [Ajouter des mots de passe pour accéder aux zones de votre site Web qui en ont besoin...](../c-about-settings-menu/c-about-crawling-menu.md#task_DED19D476FF04B48BB6456D5ECB8628A).

## Supportez-vous l&#39;analyse et l&#39;indexation de https ou le contenu sécurisé du serveur ? {#section_D5BB8B8FBEA4405583E86B4AEC37151B}

Oui. Vous pouvez analyser et indexer le contenu sur des serveurs sécurisés (https).

## Est-ce que la recherche et le marchandisage sur le site respectent le fichier robots.txt sur mon site Web ? {#section_73BBF6FE93C64C109F45CBC2FA394DB2}

Oui. Le protocole d&#39;exclusion Robots est conforme. Le robot de recherche examine le fichier robots.txt s&#39;il est présent sur votre site Web. Si votre fichier robots.txt exclut tous les robots de l’analyse de votre site, le robot de recherche/marchandisage du site est également exclu. Pour autoriser uniquement le robot de recherche/marchandisage du site à analyser votre site, définissez le contenu de votre fichier robots.txt sur ce qui suit :

```
User-agent: Atomz/1.0 
Disallow:
```

```
User-agent: * 
Disallow: /
```

Vous pouvez en savoir plus sur les robots Web et le protocole d’exclusion des robots à l’adresse suivante :

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

## Certaines parties de mon site Web doivent être mises à jour fréquemment afin que mes clients obtiennent les résultats de recherche les plus exacts. L’indexation incrémentielle aide-t-elle à résoudre ce problème ? {#section_6D2FB1DE1B8A49729F9CCAE2A2770AB3}

Oui. Ce scénario correspond à la fonction d’indexation incrémentielle créée pour faciliter la recherche/le marchandisage sur le site. L&#39;Principal avantage de l&#39;indexation incrémentielle est qu&#39;elle permet aux sociétés d&#39;indexer fréquemment de manière dynamique des portions de leur site Web qui changent. Cette fonctionnalité garantit que vous affichez les résultats de la recherche avec une précision &quot;jusqu’à la minute&quot;.

Voir [Exécution d’un index incrémentiel d’un site Web dynamique ou d’un site Web intermédiaire..](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

Voir [Définition de la planification de l&#39;index incrémentiel pour un site Web actif](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

## Les pages Web générées de manière dynamique sont-elles prises en charge à partir d’une base de données dorsale, telle que les catalogues de produits ou les systèmes de gestion des stocks ? {#section_26896C556483457E879785E751583B16}

Les pages Web HTML statiques ou générées dynamiquement, y compris les pages créées à partir de bases de données, ou tout autre processus principal, sont indexées. Le code HTML affiché par un navigateur étant indexé, vous pouvez utiliser la recherche/le marchandisage sur les sites Web tant que les informations de la base de données principale génèrent des pages HTML.

Le robot de recherche analyse votre site Web en commençant par la première page à l’adresse spécifiée dans [!DNL Account Settings] et suit les liens d’une page à l’autre.

Voir [Configuration des paramètres de votre compte](../c-about-settings-menu/c-about-account-options-menu.md#task_80A38D0C8E4F453395BD67B81E4B45D9).

Lorsque le robot de recherche analyse et indexe toutes les pages de votre site Web, vous pouvez utiliser le moteur de recherche pour effectuer des recherches sur votre site. En d’autres termes, si des documents générés dynamiquement sont tissés dans votre site Web avec des liens d’autres pages, le robot de recherche peut toujours analyser et indexer le contenu de la base de données dynamique.

Une fois le contenu de votre site Web analysé et indexé, les clients de votre site Web peuvent rechercher des informations dans le contenu indexé.

Vous pouvez facilement activer la recherche de contenu complet ou une recherche thématique plus étroite limitée aux informations contenues dans le titre, la méta-description, les balises de document des mots-clés ou les trois. A l’aide de définitions de métadonnées, vous pouvez également créer des champs d’affichage personnalisés, tels qu’une image de produit, dans les résultats de recherche réels.

Voir [Ajouter un nouveau champ de balise meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Puis-je utiliser des scripts ou des programmes pour lancer un index incrémentiel de mon site ? {#section_0B6BB039557A42AA876D35D748E17DD0}

Oui. Vous pouvez utiliser des scripts ou des programmes pour lancer un index incrémentiel de votre site Web, ainsi que pour effectuer un test ping sur les serveurs pour indexer le site chaque fois que le contenu est modifié ou mis à jour.

Voir [A propos de l’index par script](../c-about-index-menu/c-about-scripted-index.md#concept_34F58D551BC04BFB8ADC294B9DA9199D).

## Implémentations des fonctionnalités {#reference_2D0C4A80B8D64051BA9694D562DCE663}

Page de questions fréquentes qui traite des différentes mises en oeuvre de fonctionnalités dans [!DNL Search&Promote].

Vous trouverez ci-dessous des questions courantes concernant les implémentations de fonctionnalités dans [!DNL Search&Promote] sur un site Web :

* [Pourquoi mes règles de fonctionnement ne s&#39;exécutent-elles pas ?](#section_7FEB60383D8A4B11A60DFF9067274699)
* [Pourquoi ai-je des problèmes de planification de l’indexation, des erreurs de démarrage de l’indexation et des problèmes de démarrage de l’indexation par étapes ?](#section_E05758193DF5436784B0145839989F75)
* [La taille d&#39;index limite dépasse la limite autorisée. Pourquoi cela se produit-il et comment le corriger ?](#section_12E7DA979C4C4B1D8A3A6415FC3DDA70)

## Pourquoi mes règles de fonctionnement ne s&#39;exécutent-elles pas ? {#section_7FEB60383D8A4B11A60DFF9067274699}

Configurez les règles de fonctionnement lors de l&#39;affichage des bannières ou pour vous aider à déterminer quels résultats apparaissent et dans quel ordre. Vous pouvez également configurer la position d’un élément dans votre facette et le modèle utilisé pour une recherche donnée.
Réorganiser les règles de fonctionnement pour modifier l&#39;ordre dans lequel elles s&#39;exécutent sur les modèles de présentation. Les règles de fonctionnement s&#39;exécutent dans l&#39;ordre dans lequel elles ont été définies ; c&#39;est-à-dire que plus le numéro d&#39;ordre d&#39;une règle est élevé, plus elle s&#39;exécute plus tard dans le processus, dépassant les règles antérieures. Vous réorganisez les règles en entrant un nouveau numéro dans la colonne Ordre du tableau de la page Règles métier.

Voir [A propos des règles de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

## Pourquoi ai-je des problèmes de planification de l’indexation, des erreurs de démarrage de l’indexation et des problèmes de démarrage de l’indexation par étapes ? {#section_E05758193DF5436784B0145839989F75}

Lorsque vous générez un index, complet ou incrémentiel, les informations d’état d’analyse de l’index s’affichent en temps réel. Vous pouvez, par exemple, vue l’heure du début, l’heure écoulée et toute erreur survenue au cours du processus d’indexation. Des informations sur l’état de votre dernier index s’affichent également. Utilisez ces informations pour résoudre les erreurs d’indexation que vous rencontrez.

Pour la planification d&#39;un index, voir [Définition de la planification complète de l&#39;index pour un site Web actif](../c-about-index-menu/c-about-full-index.md#task_6760F3256D004A228B38968DF15421F0) et [Définition de la planification de l&#39;index incrémentiel pour un site Web actif](../c-about-index-menu/c-about-incremental-index.md#task_2A46BA189ECC4317A9D5C6E99A336F33).

Pour démarrer un index par étape, voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D) ou [Exécution d’un index incrémentiel d’un site Web dynamique ou d’un site Web intermédiaire...](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## La taille d&#39;index limite dépasse la limite autorisée. Pourquoi cela se produit-il et comment puis-je y remédier ? {#section_12E7DA979C4C4B1D8A3A6415FC3DDA70}

Un site Web peut avoir tendance à se développer et au fil du temps, Search &amp; Promote &quot;découvre&quot; plus de documents et de pages Web qui ont été ajoutés. En fin de compte, votre compte peut dépasser votre limite de taille d&#39;indexation. Dans ce cas, vous pouvez utiliser **[!UICONTROL URL Mask]**. Cette fonctionnalité masque les documents et les pages Web de l’analyse d’index que vous ne souhaitez pas indexer ou dont vous n’avez pas besoin, réduisant ainsi la taille de votre index. Vous pouvez également contacter l’assistance technique pour que votre limite de taille d’indexation soit définie sur un plus grand nombre dans votre compte.

Voir [A propos des masques d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Si vous ne savez pas quoi faire, contactez le support technique. Il peut y avoir de nombreuses autres variables qui affectent la taille de votre index et qui, si elles sont ajustées, peuvent également affecter la facturation de votre compte.

## International {#reference_F017C2968BFB446499EF1D3CE2CAC0FE}

Une page de questions fréquentes qui traite de la prise en charge de l&#39;indexation et de la recherche de plus de 19 langues, y compris les langues asiatiques multioctets comme le chinois (simplifié et traditionnel), le japonais et le coréen.

Voici quelques questions courantes concernant les langues et les jeux de caractères :

* [Ce qui contrôle le codage du jeu de caractères de la requête de recherche...](#section_DF2E8570AFC2480FA199FD26C941A22F)
* [Sont uniquement recherchées les pages dont l&#39;encodage correspond à l&#39;encodage de...](#section_9E544F3DB7DE41618DC1BC8224B32C5A)
* [Quel codage est utilisé pour la page des résultats de la recherche ?](#section_DA68670F35D54EAABF7DBB010F4409BF)
* [Puis-je utiliser la recherche/marchandisage de site sur des pages codées Unicode, UTF-8 ?](#section_130997CB08934A13A5261D85CF88040C)
* [Comment se fait-il que je ne puisse pas rechercher les fichiers PDF chinois, japonais ou coréens sur mon site Web ?](#section_539AFF482F814D28B5929F683D2F2175)
* [Comment se fait-il que je ne puisse pas rechercher les fichiers SWF chinois, japonais ou coréens sur mon site Web ?](#section_9C0849528AFF4C10AA97A2C912992638)
* [Comment se fait-il que je ne puisse pas rechercher les fichiers Microsoft Office chinois, japonais ou coréens sur mon site Web ?](#section_6764BA6863AF492EBA9BE5CCC12CDD1F)
* [Comment se fait-il que je ne puisse pas rechercher les fichiers MP3 chinois, japonais ou coréens sur mon site Web ?](#section_DB6D60CF46F94125BF4E54AF3036DBFC)
* [Est-ce que je dois faire quelque chose de spécial pour avoir...](#section_A8BA6DDD3A6048319D3530BCFD6DA1A5)
* [Comment se fait-il que les polices chinoises, japonaises ou coréennes apparaissent dans les résultats de recherche sous Netscape 4.7 et versions antérieures ?](#section_DF42567063304F918D406AC76529DFB7)

## Qu&#39;est-ce qui contrôle le codage du jeu de caractères de la requête de recherche ? {#section_DF2E8570AFC2480FA199FD26C941A22F}

La section &quot;Formulaires web&quot; de votre compte de recherche contient des exemples de formulaires de recherche que vous utilisez pour ajouter des fonctionnalités de recherche à votre site Web. Si vous observez ce code de formulaire de recherche, vous trouverez une ligne semblable à celle-ci :

`<input type=hidden name="sp_f" value="iso-8859-1">`

Cette ligne de code indique au moteur de recherche que la requête entrante est codée en iso-8859-1, un codage commun pour les langues d&#39;Europe occidentale. Vous pouvez modifier ce paramètre en accédant au menu produit et en cliquant sur **[!UICONTROL Settings]** > **[!UICONTROL My Profile]** > **[!UICONTROL Personal Information]**. Sur la page [!DNL Personal Information], dans la liste déroulante **[!UICONTROL Character Encoding]**, sélectionnez un nouveau codage.

Voir [Configuration de vos informations utilisateur personnelles](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Vous pouvez également modifier manuellement la valeur de codage de vos pages Web en modifiant la ligne `sp_f` du formulaire de recherche. N&#39;oubliez pas que la valeur `sp_f` du formulaire de recherche doit correspondre au codage de jeu de caractères de la page dans laquelle elle apparaît.

## Les seules pages recherchées dont le codage correspond à celui de la requête de recherche sont-elles codées ? {#section_9E544F3DB7DE41618DC1BC8224B32C5A}

Par défaut, non. Tant que les pages de votre site Web identifient correctement leur codage de jeu de caractères, les conversions nécessaires sont effectuées entre le codage de la requête de recherche et celui des pages, même si les pages utilisent plusieurs codages.

## Quel codage est utilisé pour la page des résultats de la recherche ? {#section_DA68670F35D54EAABF7DBB010F4409BF}

Le codage du jeu de caractères de votre compte détermine le codage par défaut pour votre modèle de résultats.

Voir [Configuration de vos informations utilisateur personnelles](../c-about-settings-menu/c-about-my-profile-menu.md#task_A11A3BE2527B4204B896E04303B04AA6).

Vous pouvez en savoir plus sur la spécification d’un jeu de caractères dans un modèle HTML.

Voir [Rechercher des balises de modèle](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

## Puis-je utiliser la recherche/marchandisage de site sur des pages codées Unicode, UTF-8 ? {#section_130997CB08934A13A5261D85CF88040C}

Oui. Cependant, les jeux de caractères Unicode, tels que UTF-8, ne fournissent pas suffisamment d&#39;informations pour déterminer la langue dans laquelle les pages sont écrites. Pour rechercher correctement ces pages, il est nécessaire de spécifier la langue. Pour déterminer la langue du document, les informations sont traitées dans l’ordre suivant :

* En-tête HTTP en langue de contenu fourni pour le document par votre serveur.
* Éléments META (par exemple, `META HTTP-EQUIV="Content-Language" Content="ja_JP"`) dans la section `<HEAD>` du document.

* Attribut LANG de la balise `<HTML>` (par exemple, `<HTML LANG="ja_JP">`).

Si votre serveur n’est pas configuré pour diffuser l’en-tête HTTP Content-Language et que vos documents ne contiennent ni l’élément META de langue, ni l’attribut de langue de la balise `<HTML>`, vous pouvez utiliser des injections de métadonnées pour spécifier la langue appropriée.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Comment se fait-il que je ne puisse pas rechercher les fichiers PDF chinois, japonais ou coréens sur mon site Web ? {#section_539AFF482F814D28B5929F683D2F2175}

La recherche et le marchandisage sur site récupèrent le format UTF-8 des fichiers Adobe PDF sans aucune indication de langue. Si vous avez sélectionné **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier la langue utilisée dans le fichier PDF.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Comment se fait-il que je ne puisse pas rechercher les fichiers SWF chinois, japonais ou coréens sur mon site Web ? {#section_9C0849528AFF4C10AA97A2C912992638}

La recherche et le marchandisage sur site récupèrent l’UTF-8 à partir des fichiers de film Flash d’Adobe qui ont été créés avec un Flash d’Adobe sans aucune indication de langue. Si vous avez sélectionné le type de contenu **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier la langue utilisée dans le fichier SWF.

Pour les versions de Flash 4 ou antérieures des fichiers SWF, le jeu de caractères des caractères du fichier n’est pas spécifié. Si vous avez sélectionné le type de contenu **[!UICONTROL Adobe Flash Movies]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier le jeu de caractères utilisé dans le fichier SWF.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Comment se fait-il que je ne puisse pas rechercher les fichiers Microsoft Office chinois, japonais ou coréens sur mon site Web ? {#section_6764BA6863AF492EBA9BE5CCC12CDD1F}

La recherche et le marchandisage sur site récupèrent le format UTF-8 des fichiers Microsoft Office (Microsoft Word, Microsoft Excel et Microsoft PowerPoint) sans indication de langue. Si vous avez sélectionné le type de contenu **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier la langue utilisée dans les fichiers Microsoft Office.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Comment se fait-il que je ne puisse pas rechercher les fichiers MP3 chinois, japonais ou coréens sur mon site Web ? {#section_DB6D60CF46F94125BF4E54AF3036DBFC}

Si vous sélectionnez le type de contenu **[!UICONTROL Text in MP3 Music Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier le jeu de caractères utilisé pour coder les fichiers MP3.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Dois-je faire quelque chose de spécial pour que les fichiers .txt de mon site Web soient indexés correctement ? {#section_A8BA6DDD3A6048319D3530BCFD6DA1A5}

Si vous avez sélectionné le type de contenu **[!UICONTROL Text Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier le jeu de caractères utilisé pour coder les fichiers .txt.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Comment se fait-il que les polices chinoises, japonaises ou coréennes apparaissent dans les résultats de recherche sous Netscape 4.7 et versions antérieures ? {#section_DF42567063304F918D406AC76529DFB7}

Si votre compte utilise le modèle par défaut, l’un des modèles prêts à l’emploi ou un modèle basé sur l’un de ces modèles, il peut contenir des balises de police qui spécifient Arial ou Helvetica comme polices de caractères. Par exemple, `<font face="arial, helvetica" size="+1">`. Netscape 4.7 et versions antérieures n’affiche pas les caractères chinois, japonais ou coréens lorsque la police Arial ou Helvetica est utilisée. Supprimez l’attribut `face` ou remplacez la face de police par une face plus appropriée pour le chinois, le japonais ou le coréen.

## Nombre de pages faible {#reference_4344E3E3CB2948939860F8C078BD7773}

Page de questions fréquentes qui traite des problèmes courants associés à un faible nombre de pages d’indexation.

Voici quelques questions courantes concernant le nombre de pages à faible indexation :

* [Avez-vous examiné votre journal d&#39;index ?](#section_D6626536DC3D40DDA4A1224F1CB276BF)
* [Avez-vous des fautes de frappe dans votre URL ?](#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676)
* [La page Web du point d&#39;entrée comporte-t-elle des liens vers d&#39;autres pages ?](#section_1C2D6ED54E7249268B555D9DC33352B3)
* [Les liens vers d&#39;autres pages de votre site Web sont-ils incorporés dans...](#section_EE34A67D60A844EBB0921C03544FF63E)
* [Les balises HTML de votre page Web sont-elles placées dans un...](#section_F31A2F5D2C284AC084158A5BD763DC5D)
* [Est-ce que vous avez mal formé les balises de commentaires HTML dans votre...](#section_D1C39D79341845CB9C38579AABDF3A24)
* [Votre page Web contient-elle des liens vers des pages d&#39;une autre page ?..](#section_F8082759184049AAA8FA6342C1F84389)
* [Utilisez-vous un service de domaine virtuel pour votre URL ?..](#section_2861F09EA21A45E6B7E15F032739CDF3)
* [Votre page Web utilise-t-elle une balise meta refresh ?](#section_5A2F544C237C49B8B1A7FE0C45371C0D)
* [Votre page Web utilise-t-elle une balise meta robots ?](#section_36275A33DDFE4620BABA948F8A63DBD2)
* [Votre site Web utilise-t-il un fichier d&#39;exclusion des robots ?](#section_BF7B663347814F58AD736066C86B7D25)

## Avez-vous examiné votre journal d&#39;index ? {#section_D6626536DC3D40DDA4A1224F1CB276BF}

Le journal d&#39;index contient des informations détaillées que le robot de recherche/marchandisage du site collecte lorsqu&#39;il indexe votre site Web. Le journal comprend une liste de liens analysés et d&#39;erreurs survenues. L’examen du journal d’index est le meilleur endroit où le début peut déterminer pourquoi toutes les pages de votre site Web ne sont pas indexées.

Voir [Affichage du journal d&#39;index complet d&#39;un fichier actif ou d&#39;un fichier d&#39;évaluation...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Voir [Affichage du journal d&#39;index incrémentiel d&#39;un fichier actif ou d&#39;un fichier d&#39;évaluation...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

## Avez-vous des fautes de frappe dans votre URL ? {#section_BD2CEABC5D0F4A0DA38F3AD72ABBA676}

Lorsque vous entrez de longues URL dans des formulaires HTML, vous pouvez introduire une ou plusieurs erreurs typographiques. N’oubliez pas que les URL ne doivent pas contenir d’espaces. Sachez également que certains serveurs Web gèrent les URL en respectant la casse.

Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Sur la page [!DNL Staged URL Entrypoints], vérifiez les éléments suivants :

* Vos URL ne comportent aucune erreur typographique.
* Les caractères des URL utilisent tous la casse appropriée.
* Il n’y a pas de caractères d’espace dans les URL.

Pour tester vos points d’entrée d’URL, copiez et collez une URL dans un navigateur Web afin de vérifier si votre site Web s’affiche. S’il n’apparaît pas, vérifiez à nouveau que vous n’avez commis aucune erreur dans le chemin d’accès à l’URL.

Voir [A propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## La page Web d’entrée comporte-t-elle des liens vers d’autres pages de votre site Web ? {#section_1C2D6ED54E7249268B555D9DC33352B3}

Le robot de recherche/marchandisage du site analyse votre site Web comme le font vos clients ; en suivant les liens de page en page. Les liens doivent être présents dans la page Web du point d&#39;entrée pour que le robot de recherche puisse trouver et indexer d&#39;autres pages de votre site.

Voir [Ajouter plusieurs points d’entrée d’URL que vous souhaitez indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Les liens vers d’autres pages de votre site Web sont-ils incorporés dans JavaScript ? {#section_EE34A67D60A844EBB0921C03544FF63E}

Vous pouvez utiliser des techniques de navigation sophistiquées sur votre site Web, telles que des actions de restauration et des menus, qui utilisent JavaScript pour créer des liens vers d’autres pages. Cependant, le robot de recherche/marchandisage du site ne peut pas suivre les liens incorporés dans JavaScript.

Une solution que vous pouvez utiliser pour résoudre ce problème est de placer des liens masqués vers d&#39;autres pages du code HTML qui contient le code JavaScript. Bien que les clients de votre site Web ne voient pas ces liens, le robot de recherche les trouve et les analyse toujours. Vous pouvez placer des balises masquées au bas de la page juste avant la balise `</body>`. Ils peuvent se présenter comme suit :

```
<a href="/mydir/mypag1.html"></a> 
<a href="/mydir/mypag2.html"></a>
```

Une autre solution consiste à liste les URL des pages supplémentaires de votre site Web en tant que points d’entrée à analyser et à indexer. Commencez les URL par `https://`, comme illustré ci-dessous :

```
https://www.mydomain.com/mydir/mypag1.html 
https://www.mydomain.com/mydir/mypag2.html
```

Voir [Ajouter plusieurs points d’entrée d’URL que vous souhaitez indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_2338A47387D74CFDAC4D4EF4A367ED45).

## Les balises HTML de votre page Web sont-elles dans une séquence non valide ? {#section_F31A2F5D2C284AC084158A5BD763DC5D}

La spécification HTML exige que les balises `<html>`, `<head>` et `<body>` suivent une séquence spécifique dans un document HTML. Les balises de toutes vos pages Web doivent avoir la séquence suivante :

```
<html> 
<head> 
...  
<i>head tags go here</i> ... 
</head> 
<body> 
...  
<i>body tags go here</i> ... 
</body> 
</html>
```

Si les balises HTML ne sont pas dans l&#39;ordre approprié, le robot de recherche/marchandisage du site ne peut pas analyser et indexer correctement votre page Web. Voici un exemple de balises qui ne se trouvent pas dans la bonne séquence :

```
<body> 
<head> 
...  
<i>head tags are here</i> ... 
</head> 
...  
<i>body tags are here</i> ... 
</body>
```

Dans ce cas, placez les balises `<html>`, `<head>` et `<body>` dans l’ordre approprié de votre page Web.

## Avez-vous mal formé les balises de commentaires HTML dans votre page Web ? {#section_D1C39D79341845CB9C38579AABDF3A24}

Veillez à examiner attentivement et à corriger les commentaires HTML non valides dans vos pages Web.

La spécification HTML exige qu’un commentaire HTML commence par les caractères `<!--` et se termine par les caractères `-->`. Il est facile d’ignorer les commentaires mal formatés qui provoquent une analyse erronée des balises de votre page Web par le robot de recherche/marchandisage du site. Un commentaire mal formé peut faire que le robot de recherche/marchandisage du site n&#39;a pas accès à d&#39;autres balises importantes qui doivent être analysées. Tenez compte des commentaires juste avant la balise `<body>` dans votre page Web.

Voici un exemple de commentaire correctement formé :

`<!-- This HTML comment is OK. -->`

Voici un exemple de commentaires mal formés :

```
<!- This HTML comment is improperly formed. -> 
<! This HTML comment is also improperly formed. >
```

## Votre page Web contient-elle des liens vers des pages d’un autre domaine ? {#section_F8082759184049AAA8FA6342C1F84389}

Souvent, un site Web peut être constitué de pages qui existent effectivement sur un serveur Web avec une adresse de domaine différente. Par exemple, si l’adresse principale de votre site Web est la suivante :

`https://www.mydomain.com/`

Votre site Web peut également comporter des pages sur un autre domaine, comme les suivantes :

`https://www.otherdomain.com/`

Par défaut, le robot de recherche/marchandisage de site ne suit pas de liens sur un domaine autre que le domaine principal. Cependant, en définissant des points d&#39;entrée supplémentaires pour votre compte de recherche, vous pouvez facilement indexer plusieurs domaines.

Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Ajoutez l’URL du &quot;point d’entrée principal du site Web&quot; de votre site. Ajoutez ensuite des points d’entrée URL supplémentaires à tout autre domaine contenant des pages de site. Par exemple, vous pouvez définir votre point d’entrée d’URL principal sur :

`https://www.mydomain.com/`

et ajoutez le point d’entrée d’URL de site supplémentaire suivant :

`https://www.otherdomain.com/`

## Utilisez-vous un service de domaine virtuel pour votre URL ? {#section_2861F09EA21A45E6B7E15F032739CDF3}

Vous utilisez peut-être un service de domaine virtuel (parfois appelé &quot;service de redirection de domaine&quot;) pour fournir une meilleure URL permettant aux clients d’accéder à votre site Web. Supposons, par exemple, que l’adresse réelle de votre site Web soit la suivante :

`https://www.myispdomain.com/~myname/mywebpages/`

Cependant, vous utilisez un service de domaine virtuel pour que les clients puissent accéder à votre site aux adresses suivantes :

`https://myname.adomain.com/`

ou

`https://adomain.com/myname/`

Par défaut, le robot de recherche/marchandisage de site ne suit pas de liens sur un domaine autre que le domaine principal. Cependant, en définissant des points d&#39;entrée supplémentaires pour votre compte de recherche, vous pouvez facilement indexer plusieurs domaines.

Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Entrypoints]**. Ajoutez le &quot;point d’entrée URL du site Web principal&quot; sur le nom de domaine virtuel de votre site. Ajoutez ensuite des points d’entrée supplémentaires au domaine où réside réellement votre site Web.

Par exemple, vous pouvez définir votre point d’entrée d’URL principal comme suit :

`https://myname.adomain.com/`

Ajoutez le point d’entrée URL de site Web supplémentaire suivant :

`https://www.myispdomain.com/~myname/mywebpages/`

## Votre page Web utilise-t-elle une balise meta refresh ? {#section_5A2F544C237C49B8B1A7FE0C45371C0D}

De nombreux sites Web disposent d’une page d’accueil qui comprend une balise meta refresh entre les balises `<head>...</head>` semblables à ce qui suit :

`<meta http-equiv="Refresh" content="0;URL=https://www.adomain.com/apath/afile.html">`

Dans certains cas, le robot de recherche/marchandisage du site ne peut pas suivre l&#39;URL de mise à jour des métadonnées pour indexer le contenu de votre site Web. Ce problème est facile à résoudre en définissant des points d&#39;entrée supplémentaires.

Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > Analyse > **[!UICONTROL URL Entrypoints]**. Ajoutez un autre point d’entrée à l’URL de la balise meta refresh.

## Votre page Web utilise-t-elle une balise meta robots ? {#section_36275A33DDFE4620BABA948F8A63DBD2}

Parfois, les pages Web utilisent des balises de méta-robots pour contrôler les robots Web qui tentent périodiquement d&#39;analyser un site Web. Les balises Meta-robots apparaissent entre les balises `<head>...</head>` d’une page Web et se ressemblent à la balise suivante :

`<meta name="robots" content="noindex, nofollow">`

Parce que le robot de recherche/marchandisage du site est lui-même un robot web, il suit les instructions de la balise meta robots. En excluant ainsi d&#39;autres robots, vous excluez également le robot de recherche/marchandisage de site.

Vous pouvez en savoir plus sur les robots Web et le protocole d’exclusion des robots à l’adresse suivante :

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Supprimez ou modifiez la balise meta robots sur les pages Web que vous souhaitez indexer sur votre site Web.

## Votre site Web utilise-t-il un fichier d&#39;exclusion des robots ? {#section_BF7B663347814F58AD736066C86B7D25}

Il arrive qu&#39;un site Web ait une page appelée robots.txt qui exclut tous ou certains robots de l&#39;analyse. Pour savoir si votre site Web comporte un fichier robots.txt, recherchez-le juste sous le domaine de niveau supérieur, comme indiqué ci-dessous :

`https://www.yourdomain.com/robots.txt`

Le contenu du fichier robots.txt ressemble au texte suivant :

```
User-agent: * 
Disallow: /
```

Comme le robot de recherche/marchandisage du site est lui-même un robot web, il suit les instructions du fichier robots.txt ; il exclut le robot de recherche/marchandisage du site. Pour contourner ce problème, modifiez le fichier d&#39;exclusion des robots (robots.txt) afin de permettre au robot de recherche/marchandisage du site d&#39;analyser et d&#39;indexer votre site Web comme suit :

```
User-agent: Atomz/1.0 
Disallow: 
 
User-agent: * 
Disallow: /
```

## Microsoft Office {#reference_A85FCC8A96514A7584F4D2A8AC8111D1}

Page de questions fréquentes qui traite de la prise en charge de l’indexation et de la recherche de fichiers Microsoft® Office sur un site Web.

Vous trouverez ci-dessous des questions courantes concernant les fichiers Microsoft Office :

* [Qu&#39;est-ce qui est indexé dans un fichier Microsoft Office ?](#section_8681DADFCFE24B7787B1FC08D431EE28)
* [Ce qui n&#39;est pas indexé dans un fichier Microsoft Office...](#section_BD53BDABFDD94D7EB0E1F55EC18017BB)
* [En quoi les fichiers Microsoft Office sont-ils indexés différemment des pages HTML ?..](#section_C104B44684F340549A6B9EB8F39EDDBB)
* [Comment empêcher l&#39;indexation des fichiers Microsoft Office...](#section_FEBA71274CD14CB99731ADF982087F4C)

## Qu&#39;est-ce qui est indexé dans un fichier Microsoft Office ? {#section_8681DADFCFE24B7787B1FC08D431EE28}

Le contenu complet des fichiers Microsoft Word, Microsoft Excel et Microsoft PowerPoint est indexé.

Les parties suivantes d&#39;un fichier Microsoft Word sont indexées :

* Titre
* Mots-clés
* Objet (description)
* Contenu texte
* Hyperliens vers d’autres documents

Les parties suivantes d&#39;un fichier Microsoft Excel sont indexées :

* Titre
* Mots-clés
* Objet (description)
* Texte dans les cellules
* Valeurs des formules numériques dans les cellules

Les parties suivantes d&#39;un fichier Microsoft PowerPoint sont indexées :

* Titre
* Mots-clés
* Objet (description)
* Texte de chaque diapositive

## Qu&#39;est-ce qui n&#39;est pas indexé dans un fichier Microsoft Office ? {#section_BD53BDABFDD94D7EB0E1F55EC18017BB}

Les graphiques contenus dans des fichiers Microsoft Office ou tout texte faisant partie d&#39;un graphique contenu ne sont pas indexés. Les définitions de propriétés personnalisées ne sont pas indexées en tant que métadonnées. Certains textes des champs spéciaux, tels que les en-têtes et les pieds de page dans un fichier PowerPoint, ne sont pas non plus indexés.

## En quoi les fichiers Microsoft Office sont-ils indexés différemment des pages HTML ? {#section_C104B44684F340549A6B9EB8F39EDDBB}

La différence entre la façon dont le robot de recherche indexe les fichiers Microsoft Office et HTML est que chaque fichier HTML est une page individuelle et qu&#39;un seul fichier Microsoft Office peut représenter des centaines de pages. Pour cette raison, chaque page est comptée dans un fichier Microsoft Office comme une page distincte sous votre compte de recherche.

## Comment empêcher l&#39;indexation des fichiers Microsoft Office sur mon site Web ? {#section_FEBA71274CD14CB99731ADF982087F4C}

Si vous ne souhaitez pas que le robot de recherche analyse et indexe les fichiers Microsoft Office, désélectionnez le type de contenu **[!UICONTROL Microsoft Office Files]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Vous pouvez également utiliser [!DNL URL Masks] pour désactiver l&#39;indexation des fichiers Microsoft Office.

Saisissez les masques d’URL suivants :

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Si vous n’utilisez pas d’expressions régulières </p> </td> 
   <td colname="col2"> 
    <ul id="ul_DFEC911DA11C484C8E4671A0F00E1F88"> 
     <li id="li_2E50374E3869426B97353A5A8CBE09EC">exclure *.doc </li> 
     <li id="li_9089D11161524D90849CA88F703772B6">exclure *.xls </li> 
     <li id="li_7F6CFC6212E64C04AAF38E21A667C763">exclure *.ppt </li> 
    </ul> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Si vous utilisez des expressions régulières </p> </td> 
   <td colname="col2"> 
    <ul id="ul_012A45C3EC04460EA09C0ECFB49A8FA9"> 
     <li id="li_0C239F0A536D465F85A98EBF7B6ADF27">exclure regexp ^.*\.doc$ </li> 
     <li id="li_9F91DA35A2A646ACAFF2BA37F9136E2A">exclure regexp ^.*\.xls$ </li> 
     <li id="li_9D768D9EA2DB44FBB00A1979E21672E2">exclure regexp ^.*\.ppt$ </li> 
    </ul> </td> 
  </tr> 
 </tbody> 
</table>

Voir [Ajouter des masques d&#39;URL pour indexer ou non des parties d&#39;index de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## MP3 {#reference_7614250EE81C4EEFA43E57A6A74E83D7}

Page de questions fréquentes qui traite de la prise en charge de l’indexation et de la recherche de fichiers musicaux MP3 sur un site Web.

Vous trouverez ci-dessous des questions courantes sur les fichiers MP3.

* [Quand un fichier MP3 est-il analysé et indexé ?](#section_538EA1682C9C47E3A62640BB25D84C36)
* [Que dois-je faire pour ramper et indexer...](#section_3CD794446E3545379C14E9F222118665)
* [Comment un fichier MP3 est-il reconnu ?](#section_230E7336965A424F96C5CCF1D3C2D103)
* [Qu&#39;est-ce qui est indexé dans un fichier MP3 ?](#section_E99D252B27CA4946AED3FCD3ABD8779D)
* [Un fichier MP3 est-il comptabilisé comme une page ?](#section_9910BEB6617D4D2090558CDF6C65D16B)
* [Comment empêcher l&#39;indexation de fichiers MP3 individuels...](#section_C989DC1D3D3841B38F683A462195DC05)
* [Comment empêcher l&#39;indexation des fichiers MP3 ?](#section_305D2B28D1124776B6DC0C62A17827C6)
* [Pourquoi ne puis-je pas rechercher les fichiers MP3 chinois, japonais ou coréens sur mon site ?](#section_06A48DA3F9E742CC93CC8B5CCD7382FA)

## Quand un fichier MP3 est-il analysé et indexé ? {#section_538EA1682C9C47E3A62640BB25D84C36}

Les fichiers MP3 sont analysés et indexés de deux manières. La méthode la plus courante consiste à utiliser une balise HREF d’ancrage dans un fichier HTML :

`<a href="MP3-file-URL"></a>`

Une deuxième méthode consiste à entrer l’URL du fichier MP3 en tant que point d’entrée d’URL.

Voir [A propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Que dois-je faire pour analyser et indexer les fichiers MP3 sur mon site ? {#section_3CD794446E3545379C14E9F222118665}

Pour activer l’analyse et l’indexation MP3 pour votre compte, dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**. Sur la page [!DNL Staged Content Types], sélectionnez **[!UICONTROL Text in MP3 Music Files]**.

Voir [A propos des types de contenu](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Comment un fichier MP3 est-il reconnu ? {#section_230E7336965A424F96C5CCF1D3C2D103}

Un fichier MP3 est reconnu par son type MIME qui est &quot;audio/mpeg&quot;.

## Qu&#39;est-ce qui est indexé dans un fichier MP3 ? {#section_E99D252B27CA4946AED3FCD3ABD8779D}

Les fichiers MP3 stockent éventuellement une petite quantité d’informations textuelles. Ces informations peuvent inclure le nom de l’album, le nom de l’artiste, le titre de la chanson, le genre de la chanson, l’année de publication et un commentaire. Ces informations sont stockées à la toute fin du fichier dans ce qu&#39;on appelle la BALISE. Les fichiers MP3 contenant des informations de balise sont indexés de la manière suivante :

* Le titre de la chanson est traité comme le titre d’une page HTML.
* Le commentaire est traité comme une description définie pour une page HTML.
* Le genre est traité comme un mot-clé défini pour une page HTML.
* Le nom de l’artiste, le nom de l’album et l’année de publication sont traités comme le corps d’un document HTML.

## Un fichier MP3 est-il comptabilisé comme une page ? {#section_9910BEB6617D4D2090558CDF6C65D16B}

Oui, chaque fichier MP3 analysé et indexé sur votre site Web est compté comme une page.

## Comment empêcher l&#39;indexation de fichiers MP3 individuels ? {#section_C989DC1D3D3841B38F683A462195DC05}

Entourez les balises d’ancrage qui pointent vers les fichiers MP3 avec les balises `<nofollow>` et `</nofollow>`. Le robot de recherche ne suit pas les liens entre ces balises.

Une autre méthode consiste à ajouter les URL des fichiers MP3 en tant que masques d’exclusion.

Voir [A propos des masques d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Voir [A propos du script de masques d’URL](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B).

## Comment empêcher l&#39;indexation des fichiers MP3 ? {#section_305D2B28D1124776B6DC0C62A17827C6}

Le moyen le plus simple de contrôler l’indexation MP3 pour votre compte consiste à désélectionner **[!UICONTROL Text in MP3 Music Files]** sur la page [!DNL Staged Content Types].

Voir [Sélection des types de contenu à analyser et à indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

Vous pouvez également utiliser la fonction Masques d’URL pour désactiver l’indexation MP3 par extension de fichier. Pour ce faire, dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Saisissez l’un des masques suivants :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Si votre compte... </p> </th> 
   <th colname="col2" class="entry"> <p>Entrez le masque d'URL suivant </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>N'utilise pas d'expressions régulières </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclure *.mp3  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Utilise des expressions régulières </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> exclure regexp ^.*\.mp3$ </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Pourquoi ne puis-je pas rechercher les fichiers MP3 chinois, japonais ou coréens sur mon site ? {#section_06A48DA3F9E742CC93CC8B5CCD7382FA}

Pour rechercher des fichiers MP3 chinois, japonais ou coréens, dans le menu du produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]** > **[!UICONTROL Text in MP3 Music Files]**. Cliquez ensuite sur **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Injections]**, puis spécifiez le jeu de caractères utilisé pour coder les fichiers MP3.

Voir [Sélection des types de contenu à analyser et à indexer](../c-about-settings-menu/c-about-crawling-menu.md#task_CCAC5C67C8BF4AB7B79D34A1495D5EE8).

Voir [A propos des injections](../c-about-settings-menu/c-about-metadata-menu.md#concept_DA091920671948A0A893A26B3A2FAAE5).

## PDF {#reference_F127C4915A0D436DA34E5D75ABFBB21B}

Page de questions fréquentes qui traite de la prise en charge de l’indexation et de la recherche de fichiers PDF sur un site Web.

Voici quelques questions courantes concernant les fichiers PDF :

* [Qu’est-ce qui est indexé dans un fichier PDF ?](#section_62BFCD7158B44F2BB3B1864224B50174)
* [Qu’est-ce qui n’est pas indexé dans un fichier PDF ?](#section_A14B353AE503408896BACBBF3F748FA0)
* [Comment les fichiers PDF indexés sont-ils comptabilisés ?](#section_C35DE36A65D649BD8FF314E9EFD990A6)
* [Les résultats de la recherche peuvent-ils afficher une icône PDF ?](#section_829CE82CC3544502A13D27C4DB820189)
* [Les résultats de la recherche peuvent-ils être liés à une page particulière dans...](#section_A06E7F7017E6441E98209D288EE57BF6)
* [Comment empêcher l’indexation des fichiers PDF ?](#section_96671419A822486AAC654D8DAD819940)
* [Comment se fait-il que je ne puisse pas rechercher les fichiers PDF chinois, japonais ou coréens sur mon site Web ?](#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8)

## Qu’est-ce qui est indexé dans un fichier PDF ? {#section_62BFCD7158B44F2BB3B1864224B50174}

Le contenu complet des fichiers PDF est indexé. Les parties suivantes d’un fichier PDF sont indexées :

* Titre
* Mots-clés
* Objet (description)
* Contenu texte

## Qu’est-ce qui n’est pas indexé dans un fichier PDF ? {#section_A14B353AE503408896BACBBF3F748FA0}

La table des matières PDF, les graphiques du fichier ou tout texte faisant partie d’un graphique contenu ne sont pas indexés.

## Comment les fichiers PDF indexés sont-ils comptabilisés ? {#section_C35DE36A65D649BD8FF314E9EFD990A6}

Chaque fichier PDF est comptabilisé, y compris les fichiers PDF qui contiennent plusieurs pages, en un seul document.

## Les résultats de la recherche peuvent-ils afficher une icône PDF ? {#section_829CE82CC3544502A13D27C4DB820189}

Oui. Utilisez la balise `<search-if-link-extension>` de votre modèle pour inclure une icône PDF, ou d’autres graphiques ou du texte, dans les résultats de la recherche :

```
<search-results> 
  ... 
  <search-if-link-extension value=".pdf"> 
    <img src="/search/i/pdficon.gif"> 
  </search-if-link-extension> 
  ... 
</search-results>
```

Les icônes PDF permettent à vos clients de savoir qu’un résultat de recherche renvoie à un fichier PDF de très grande taille. La taille du fichier peut être importante pour les clients qui accèdent à votre site Web par modem ou sur un périphérique mobile.

## Les résultats de la recherche peuvent-ils renvoyer vers une page spécifique d’un fichier PDF ? {#section_A06E7F7017E6441E98209D288EE57BF6}

Oui. A l’aide de la balise de modèle de liens dynamiques ( `<search-smart-link>...</search-smart-link>`), les clients peuvent cliquer pour ouvrir la première page PDF contenant les résultats de la recherche.

Pour utiliser des liens dynamiques, remplacez les balises `<search-link>...</search-link>` de la section des résultats de recherche de votre modèle par des balises `<search-smart-link>...</search-smart-link>`. Lorsqu’un client clique sur un lien généré par les balises de lien dynamique, il accède à la première page PDF correspondant à sa requête de recherche.

>[!NOTE]
>
>Pour utiliser cette fonctionnalité, le client doit utiliser une version récente de l’Adobe Acrobat, ou Reader Adobe Acrobat, qui doit inclure le module de mise en surbrillance et le module externe de gestion de fenêtres externes (EWH). En outre, leur navigateur Web doit utiliser le module Adobe Acrobat pour Netscape Navigator (vous pouvez utiliser tout navigateur qui accepte ce module Netscape Navigator) ou le contrôle Acrobat ActiveX pour Internet Explorer 4.0 et versions ultérieures.

Voir [Rechercher des balises de modèle](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4).

## Comment empêcher l’indexation des fichiers PDF sur mon site Web ? {#section_96671419A822486AAC654D8DAD819940}

Si vous ne souhaitez pas que le robot de recherche analyse et indexe les fichiers PDF, désélectionnez le type de contenu **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**).

Vous pouvez également choisir d’utiliser [!DNL URL Masks] pour désactiver l’indexation PDF.

Voir [Ajouter des masques d&#39;URL pour indexer ou non des parties d&#39;index de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Pour désactiver l’indexation PDF, saisissez l’un des masques d’URL suivants :

* `exclude *.pdf` (si vous n’utilisez pas d’expressions régulières)
* `exclude regexp ^.*\.pdf$` (si vous utilisez des expressions régulières)

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## Comment se fait-il que je ne puisse pas rechercher les fichiers PDF chinois, japonais ou coréens sur mon site Web ? {#section_D41CA8EFCA0242EA8CF5F8F1924E4CD8}

La recherche/marchandisage sur site obtient UTF-8 à partir de fichiers PDF sans indication de langue. Si vous avez sélectionné le type de contenu **[!UICONTROL PDF Documents]** ( **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**), vous devez utiliser des injections de métadonnées pour spécifier la langue utilisée dans le fichier PDF.

Voir [Ajouter les définitions d&#39;injection de champ](../c-about-settings-menu/c-about-metadata-menu.md#task_E86566FA1FF74CF68115C0ADA05172AE).

## Trop de pages {#reference_48A748BC1ED14844ACAC2735C8388E8A}

Page de questions fréquentes qui explique certaines des raisons pour lesquelles l&#39;indexeur a comptabilisé plus de pages que vous en avez réellement, et quelle est la solution dans chaque cas.

Si vous êtes certain que votre site Web est en dessous de la limite de page, mais que l’indexeur vous indique que la limite est atteinte, vous devez examiner ces questions et réponses courantes pour trouver des solutions possibles.

* [Avez-vous examiné vos différents fichiers de données ?](#section_C929BF9FDA6B4C9A9078C45AFE80EFE8)
* [Les programmes CGI sont-ils indexés sur votre site Web ?](#section_86ED8A641B3841EC80153B4F107548FD)
* [La navigation dans les répertoires est-elle activée sur votre serveur ?](#section_073C88EEE74F4CA0AD2C7145D4810B22)
* [Y a-t-il des forums ou des groupes de discussion sur votre site Web ?](#section_8DCB94F0850A41B9B2EA885F779E2F84)
* [Existe-t-il des fichiers PDF ou Microsoft Office sur votre site Web ?..](#section_455FC5438DF74E68AB9A31D359EAD4D9)
* [Disposez-vous de plusieurs points d’entrée d’URL ?](#section_8C54AFD7DF56472A9364D516482B534C)
* [Avez-vous dépassé les octets internes ou les délais de...](#section_AE1BE61A58864FFE81F0BCEED2EBB15D)

## Avez-vous examiné vos différents fichiers de données ? {#section_C929BF9FDA6B4C9A9078C45AFE80EFE8}

Le journal d&#39;index contient des informations détaillées collectées par le robot de recherche/marchandisage du site lors de l&#39;indexation de votre site Web. Le journal contient une liste de tous les liens analysés et des erreurs survenues. L&#39;examen du journal d&#39;index est le meilleur endroit pour début lorsque vous essayez de déterminer les pages qui sont indexées.

Voir [Affichage du journal d&#39;index complet d&#39;un fichier actif ou d&#39;un fichier d&#39;évaluation...](../c-about-index-menu/c-about-full-index.md#task_02E5E944C56B4EB19CC1FF321F3221B8).

Voir [Affichage du journal d&#39;index incrémentiel d&#39;un fichier actif ou d&#39;un fichier d&#39;évaluation...](../c-about-index-menu/c-about-incremental-index.md#task_E668E1F1240C476DAA1CA783DC728232).

Voir [Affichage du journal d&#39;index incrémentiel par script d&#39;un fichier actif ou...](../c-about-index-menu/c-about-scripted-index.md#task_CBFCE9B9A87B4DF7A2A35A6E83DE93D7).

Voir [Affichage du journal d&#39;index régénéré d&#39;un fichier actif ou d&#39;un fichier d&#39;évaluation...](../c-about-index-menu/c-about-regenerate-index.md#task_61CE8F9E7BF84BA89A8D482B2106BB15).

Voir [Affichage du journal d’index reclassé d’un site Web actif ou d’un site Web intermédiaire](../c-about-index-menu/c-about-re-rank-index.md#task_3C76107DFAC1495FACD3ABB0A688208D).

## Les programmes CGI sont-ils indexés sur votre site Web ? {#section_86ED8A641B3841EC80153B4F107548FD}

Les programmes CGI utilisent des paramètres d’URL qui font parfois que l’indexeur analyse plusieurs &quot;fausses&quot; URL. Si la recherche/le marchandisage du site lit vos programmes CGI et les URL suivantes avec des paramètres CGI, il y a probablement plusieurs multiples de pages analysées et indexées qui ne sont pas utiles pour votre index de recherche. Les paramètres CGI standard apparaissent dans les URL avec des caractères `?` ou `&`.

Vous pouvez masquer l’indexation des programmes CGI à l’aide de la fonction Masques d’URL. Vous pouvez masquer un préfixe d’URL ou utiliser des expressions régulières pour masquer vos scripts CGI.

Voir [A propos des masques d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_8039DFC53FF3410AA494D602F71BA164).

Voir [A propos du script de masques d’URL](../c-about-settings-menu/c-about-filtering-menu.md#concept_384F32EA18F84853A7BA99A04009330B).

Voir [Expressions régulières](../c-appendices/r-regular-expressions.md#reference_B5BA7D61D82E4109A01D2A2D964E3A6A).

## La navigation dans les répertoires est-elle activée sur votre serveur ? {#section_073C88EEE74F4CA0AD2C7145D4810B22}

Lorsqu’une navigation dans les répertoires est activée sur un serveur Web et qu’aucun fichier index.html n’est présent dans un répertoire donné, une visite dans ce répertoire peut afficher la liste des fichiers qu’il contient. En règle générale, il existe des liens en haut de la page qui vous permettent de trier la liste de différentes manières en cliquant simplement sur **[!UICONTROL Name]**, **[!UICONTROL Last modified]**, **[!UICONTROL Size]**, etc. En règle générale, elles apparaissent dans le journal de l&#39;index de recherche/marchandisage du site sous la forme d&#39;URL avec des caractères tels que `?M=A` à la fin. L’indexeur de recherche/marchandisage du site les suit comme des liens, ce qui peut mener à l’indexation de plusieurs &quot;fausses&quot; URL.

En règle générale, un site Web bien conçu contient des fichiers d’index situés dans chaque répertoire, ou bien la navigation dans les répertoires est désactivée pour ces répertoires sans fichiers d’index. Heureusement, il existe un moyen facile de masquer ces &quot;fausses&quot; URL si vous ne pouvez pas modifier vos pages ou désactiver les listes d&#39;annuaires côté serveur.

Pour accomplir cette tâche, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Ajoutez un masque pour masquer toute URL contenant le caractère `?`. Pour ce faire, vous pouvez saisir le masque d’expression normal suivant :

`exclude regexp ^.*\?.*$`

Après avoir créé le masque, veillez à réindexer votre site Web.

Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Voir [Exécution d’un index incrémentiel d’un site Web dynamique ou d’un site Web intermédiaire..](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Y a-t-il des forums ou des groupes de discussion sur votre site Web ? {#section_8DCB94F0850A41B9B2EA885F779E2F84}

Si des forums ou des groupes de discussion sont analysés sur votre site Web, il se peut qu’ils suivent des URL pour connaître différentes options d’affichage ou de tri. Ce comportement signifie que la même page est indexée plusieurs fois.

Habituellement, les forums ou les groupes de discussion sont dotés de leurs propres moteurs de recherche. Dans ce cas, vous pouvez utiliser [!DNL URL Masks] pour masquer les forums à partir de la recherche/du marchandisage sur le site.

Dans le menu produit, cliquez sur **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL URL Masks]**. Sur la page [!DNL Staged URL Masks], masquez vos forums en entrant leurs URL sous forme de masques d’URL exclus.

Voir [Ajouter des masques d&#39;URL pour indexer ou non des parties d&#39;index de...](../c-about-settings-menu/c-about-crawling-menu.md#task_E1AFC17C746048B8843013D979E082C1).

Après avoir créé les masques, veillez à réindexer votre site Web.

Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Voir [Exécution d’un index incrémentiel d’un site Web dynamique ou d’un site Web intermédiaire..](../c-about-index-menu/c-about-incremental-index.md#task_9BFB6157F3884B2FAECB7E0E9CA318CB).

## Existe-t-il des fichiers PDF ou Microsoft Office sur votre site Web ? {#section_455FC5438DF74E68AB9A31D359EAD4D9}

Si votre site Web contient des fichiers PDF ou des fichiers [!DNL Microsoft Office], vous remarquerez peut-être que la taille d’index de quelques fichiers seulement compte de nombreuses pages. La raison pour laquelle il y a plus de pages à indexer que de documents est que chaque page d&#39;un fichier PDF ou Microsoft Office est comptée comme une page distincte.

Dans le menu produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Full Index]** > **[!UICONTROL Live Index]**. Sur la page [!DNL Full Index], sélectionnez **[!UICONTROL Count All Pages]**, puis cliquez sur **[!UICONTROL Full Index Now]** pour afficher le nombre total de pages. Si vous ne souhaitez pas que les fichiers PDF ou les fichiers Microsoft Office soient indexés, vous pouvez désactiver ce type de contenu sous **[!UICONTROL Settings]** > **[!UICONTROL Crawling]** > **[!UICONTROL Content Types]**.

Voir [Exécution d’un index complet d’un site Web en direct ou par étape...](../c-about-index-menu/c-about-full-index.md#task_F7FE04D8A1654A7787FCCA31B45EB42D).

Voir [A propos des types de contenu](../c-about-settings-menu/c-about-crawling-menu.md#concept_6FEA1355C0374500B4C53090C34A8A07).

## Disposez-vous de plusieurs points d’entrée d’URL ? {#section_8C54AFD7DF56472A9364D516482B534C}

Le robot de recherche/marchandisage du site commence à analyser les points d’entrée d’URL spécifiés et suit tous les liens trouvés vers tout le contenu de ce domaine particulier. Si vous avez spécifié de nombreux points d’entrée d’URL, un nombre important de pages peut être analysé.

Utilisez la balise `nofollow` du protocole d&#39;exclusion des robots dans les en-têtes des documents de point d&#39;entrée sur les domaines supplémentaires comme suit :

```
<html> 
<head> 
<meta name="robots" content="nofollow"> 
</head>
```

Le code ci-dessus indique au robot de recherche/marchandisage du site d&#39;indexer le contenu de la page, mais pas de suivre les liens vers d&#39;autres pages.

Vous pouvez en savoir plus sur les robots Web et le protocole d’exclusion des robots à l’adresse suivante :

[https://www.robotstxt.org/orig.html](https://www.robotstxt.org/orig.html)

Si vous n’avez pas accès à la source des pages sur d’autres domaines, vous pouvez supprimer plusieurs points d’entrée d’URL. Cela vous permet de limiter l&#39;activité d&#39;indexation uniquement aux domaines dont vous souhaitez que les clients puissent effectuer des recherches.

Voir [A propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

## Avez-vous dépassé les octets internes ou les délais de recherche/marchandisage sur le site ? {#section_AE1BE61A58864FFE81F0BCEED2EBB15D}

Vérifiez si votre compte a atteint sa limite sur l’écran &quot;État de l’index complet&quot;. Si l’état indique que votre index est supérieur à ce qui est autorisé ou qu’il a pris plus de temps que prévu, votre site Web n’est pas entièrement indexé. Vous pouvez corriger cette erreur afin d’obtenir une couverture et un nombre corrects de pages du site Web.

Pour protéger les serveurs de recherche/marchandisage de site, il existe des limites internes sur les octets et le temps. Ces limites ne sont atteintes que lorsque les fichiers analysés sont très volumineux ou lorsque le serveur que la recherche/marchandisage sur le site tente d&#39;atteindre est lent.

Si vous atteignez une limite de temps, assurez-vous que votre serveur est en ligne et réessayez d’indexer l’index ultérieurement. Si vous atteignez une limite d’octets, vérifiez les fichiers analysés en affichant votre journal d’index. Sont-ils exceptionnellement grands ? Contactez l’assistance technique si vous voyez l’un de ces messages.
