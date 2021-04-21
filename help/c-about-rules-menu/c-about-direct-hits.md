---
description: Les accès directs vous permettent de rediriger un client vers une URL spécifique lorsque le client recherche un terme correspondant. Ce type de fonctionnalité vous permet d'améliorer la navigation dans la recherche de votre site Web.
solution: Target
title: A propos des accès directs
topic-legacy: Rules,Site search and merchandising
uuid: 374d63c8-2b82-4165-b543-05b587757baa
exl-id: 251dfa47-f55a-469c-8fca-e187877b7759
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 1%

---

# A propos des accès directs {#about-direct-hits}

Les accès directs vous permettent de rediriger un client vers une URL spécifique lorsque le client recherche un terme correspondant. Ce type de fonctionnalité vous permet d&#39;améliorer la navigation dans la recherche de votre site Web.

## Utilisation des accès directs {#concept_C5EE074A19FD4D5B8DD21DB575E35565}

Les accès directs se composent de deux éléments principaux : URL de votre site Web et un ou plusieurs termes de recherche délimités par des virgules. Les accès directs sont spécifiés comme suit :

```
    website_URL: term
    website_URL: term, term, term
```

Supposons, par exemple, que votre site Web d’entreprise comporte une page qui spécifie l’ensemble de vos termes et conditions. Lorsqu’un client recherche vos termes et conditions, plutôt que d’afficher les résultats, vous pouvez rediriger le client vers votre page de termes et conditions.

```
    https://www.mycompany.com/policies.asp?article=terms: terms and conditions, terms, conditions, security
    https://www.mycompany.com/press/news.asp: press releases, press
```

Si le terme de requête ne correspond à aucun accès direct, les résultats de la recherche sont renvoyés de la manière habituelle.

## Configuration des accès directs {#task_64DFB8C554874C699FCC0C2F26C3669F}

Vous pouvez spécifier des termes de recherche qui redirigent un navigateur Web vers un URI au lieu de renvoyer les résultats de la recherche.

<!-- 

t_configuring_direct_hits.xml

 -->

Les lignes vierges et les lignes de commentaire commençant par le caractère &quot;#&quot; (hachage) sont autorisées.

**Pour configurer les accès directs**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. Dans le champ [!DNL Direct Hits], saisissez l’URL de votre site Web et un ou plusieurs termes de recherche délimités par des virgules.
1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

## Test des accès directs {#task_1E2EA833BF90423AA0DD8C5BBFE77445}

Avant de publier les règles d’accès direct, vous pouvez tester les accès directs en entrant un terme.

<!-- 

t_testing_direct_hits.xml

 -->

Si vous testez un terme qui n’est pas couvert par une règle d’accès direct, un message s’affiche pour vous informer. Dans un tel scénario, si la règle d’accès direct était activée sur votre site Web, les résultats de la recherche seraient renvoyés comme d’habitude. Si vous testez un terme couvert par une règle d’accès direct, un message s’affiche vous informant qu’une redirection vers l’URL spécifiée s’est produite.

**Pour tester les accès directs**

1. Dans le menu produit, cliquez sur **[!UICONTROL Rules]** > **[!UICONTROL Direct Hits]**.
1. Dans le champ [!DNL Test Direct Hits], entrez un terme de recherche, puis cliquez sur **[!UICONTROL Test]**.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).
