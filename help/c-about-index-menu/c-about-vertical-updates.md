---
description: Vous pouvez utiliser la mise à jour verticale pour mettre rapidement à jour des parties de votre index sans avoir à traiter de grandes quantités de données.
seo-description: Vous pouvez utiliser la mise à jour verticale pour mettre rapidement à jour des parties de votre index sans avoir à traiter de grandes quantités de données.
seo-title: A propos de la mise à jour verticale
solution: Target
subtopic: Vertical Update
title: A propos de la mise à jour verticale
topic: Index,Site search and merchandising
uuid: ded09e89-5a52-4e8c-a6f7-3e25b4191183
translation-type: tm+mt
source-git-commit: f21a3f7fe0aeaab517a5ca36da43594873b3e69a

---


# A propos de la mise à jour verticale{#about-vertical-update}

Vous pouvez utiliser la mise à jour verticale pour mettre rapidement à jour des parties de votre index sans avoir à traiter de grandes quantités de données.

## Utilisation de la mise à jour verticale {#concept_E65A70C9C2E04804BF24FBE1B3CAD899}

Un index vertical ne prend que quelques secondes et est utile sur les sites Web de commerce électronique de grande capacité qui peuvent prendre plusieurs heures pour un index complet ou incrémentiel.

Lorsque vous générez un index vertical, des informations d’état s’affichent, telles que l’heure de début, l’heure écoulée et les erreurs survenues pendant le processus d’indexation.

Vous pouvez arrêter ou redémarrer le processus d’indexation verticale à tout moment.

Tandis que le nouvel index vertical met à jour votre site Web en ligne, les clients peuvent continuer à rechercher votre site à l’aide de l’index actuel.

>[!NOTE]
>
>Par défaut, cette fonction n’est pas activée dans [!DNL Adobe Search&Promote], par défaut. Contactez le support technique pour activer la fonction à utiliser.

Les mises à jour verticales sont spécifiquement destinées à être utilisées sur des [!DNL Adobe Search&Promote] comptes de type commerce électronique qui utilisent IndexConnector pour fournir le contenu de l’index de recherche. Le cas d’utilisation type est celui où l’ [!DNL Adobe Search&Promote] index représente un catalogue de produits pouvant faire l’objet d’une recherche et où il est nécessaire de pouvoir mettre rapidement à jour des valeurs fréquemment modifiées, telles que le stock disponible, la disponibilité et/ou le prix. Une mise à jour verticale est quelque peu similaire à un index incrémentiel, sauf qu’elle ne met à jour que des parties de chaque document, tandis qu’un index incrémentiel remplace des documents entiers par de nouvelles versions.

Le terme &quot;Mise à jour verticale&quot; fait référence à la notion selon laquelle un [!DNL Adobe Search&Promote] index peut être représenté sous la forme d’un tableau à colonnes, chaque colonne correspondant à une définition de champ de [!DNL Adobe Search&Promote] métadonnées et chaque ligne correspondant à un document. Le processus de mise à jour verticale remplace une ou plusieurs colonnes sans avoir à modifier le contenu des autres colonnes.

Lorsque la source principale du contenu, un flux IndexConnector, contient tous les éléments de données requis pour créer l’index, le flux Mise à jour verticale est un sous-ensemble du flux principal, qui utilise le même &quot;schéma&quot; IndexConnector pour définir les éléments de données, mais *ne contenant que* les éléments de données à mettre à jour.

Au minimum, le flux Mise à jour verticale doit contenir l’élément &quot;clé primaire&quot; (identifié par la case à cocher Clé **** principale dans la configuration d’IndexConnector) et au moins un élément de données à mettre à jour.

Par exemple, un flux IndexConnector principal peut ressembler à ce qui suit (mais généralement avec beaucoup plus d’éléments de données) :

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <title><![CDATA[Title for product 123]]></title>
  <description><![CDATA[Description for product 123.]]></description>
  <price>3.99</price>
  <link><![CDATA[https://www.somewhere.com/products/123]]></link>
  <image><![CDATA[https://www.somewher.com/images/products/123.jpg]]></image>
  <label><![CDATA[PROD123]]></label>
  <inventory>100</inventory>
  <brand><![CDATA[brand123]]></brand>
  ...
</product>
<product>
...
</product>
</products>
```

Il est nécessaire de pouvoir rapidement mettre à jour uniquement les valeurs `<price>` et `<inventory>` les valeurs, car ces valeurs peuvent changer rapidement sur le site du client. Un flux de mise à jour verticale peut alors ressembler à ce qui suit :

```xml
<?xml version="1.0" encoding="UTF-8"?>
<products>
<product>
  <id><![CDATA[123]]></id>
  <price>3.50</price>
  <inventory>90</inventory>
</product>
<product>
...
</product>
</products>
```

Ces informations sont généralement stockées dans un fichier distinct sur le serveur du client et le paramètre de configuration &quot;Chemin du fichier vertical&quot; d’IndexConnector pointe vers ce fichier. Le processus de mise à jour verticale lit ce nouveau contenu et met à jour l’ [!DNL Adobe Search&Promote] index existant, en mettant uniquement à jour les valeurs de `<price>` et `<inventory>`, dans ce cas, Les recherches suivantes renvoient le contenu nouvellement mis à jour.

>[!NOTE]
Dans cet exemple, les champs `<price>` et `<inventory>` Métadonnées doivent avoir été définis avec l’option Champ **de mise à jour** vertical cochée.

Voir aussi [A propos du contrôle à distance pour l’indexation](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F) et l’ [ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.

## Configuration d’une mise à jour verticale d’un site Web intermédiaire {#task_46A367B0786C4C90BFFA5D3F95FD86C0}

Vous pouvez configurer les sources du connecteur d’index que vous souhaitez inclure dans votre mise à jour verticale en spécifiant des URL.

**Pour configurer une mise à jour verticale d’un site Web intermédiaire**

1. Dans le menu du produit, cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Configuration]**.
1. Sur la **[!UICONTROL Vertical Update Configuration]** page, dans le champ Mettre à jour les URL, spécifiez les URL des pages à indexer.

   Le robot de recherche met uniquement à jour les documents identifiés dans les sources d’Index Connector spécifiées.

   Ce champ ne doit contenir que les URL du connecteur d’index, comme dans l’exemple suivant :

   `index:product_catalog`.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Affichage du journal de mise à jour verticale d’un site Web en direct ou d’un site Web intermédiaire {#task_E668E1F1240C476DAA1CA783DC728232}

Lorsqu’une mise à jour verticale en direct ou une mise à jour verticale par étapes est terminée, vous pouvez afficher le journal associé afin de résoudre les erreurs qui se sont produites.

Vous ne pouvez pas exporter de fichiers journaux de mise à jour verticale, ni les enregistrer. Le fichier journal reste disponible pour affichage jusqu’à ce que l’index suivant se produise.

**Pour afficher le journal des mises à jour verticales d’un site Web en direct ou par étape**

1. Dans le menu du produit, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Live Log]**.

   * Cliquez sur **[!UICONTROL Index]** > **[!UICONTROL Vertical Update]** > **[!UICONTROL Staged Log]**.

1. Dans la page du journal, en haut ou en bas, effectuez l’une des opérations suivantes :

   * Utilisez les options de navigation **[!UICONTROL First]**, **[!UICONTROL Prev]**, **[!UICONTROL Next]**, **[!UICONTROL Last]** ou **[!UICONTROL Go to line]** pour parcourir le journal.

   * Utilisez les options d’affichage **[!UICONTROL Errors only]**, **[!UICONTROL Wrap line]** ou **[!UICONTROL Show]** pour affiner ce que vous voyez.

