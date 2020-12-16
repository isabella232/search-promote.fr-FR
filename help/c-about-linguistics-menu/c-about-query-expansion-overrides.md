---
description: Vous pouvez remplacer l'extension des résultats de la requête de recherche.
seo-description: Vous pouvez remplacer l'extension des résultats de la requête de recherche.
seo-title: A propos des remplacements d'extension de Requête
solution: Target
title: A propos des remplacements d'extension de Requête
topic: Linguistics,Site search and merchandising
uuid: dfe18004-b8fd-4889-b01c-72a3b0c82b9c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---


# A propos des remplacements d&#39;extension de Requête{#about-query-expansion-overrides}

Vous pouvez remplacer l&#39;extension des résultats de la requête de recherche.

## Utilisation des remplacements d&#39;extension de Requête {#concept_6895B469B0E044299E93361BFA06B554}

Lorsque vous configurez un remplacement d&#39;extension de requête, vous créez un ensemble de &quot;règles&quot;. Chaque règle indique, essentiellement, &quot;Ne pas développer `<this>` en `<that>` au moment de la recherche&quot; où `<this>` est un mot ou une expression de texte simple et `<that>` est un mot ou une expression de texte, ou une classification.

>[!NOTE]
>
>Par défaut, cette fonction n’est pas activée dans Search &amp; Promote. Contactez le support technique pour activer la fonction à utiliser. Une fois la fonction de remplacement de l&#39;extension de Requête activée, vous devez l&#39;activer dans l&#39;interface utilisateur.

**Fonctionnement du remplacement de l&#39;extension de Requête**

Lorsqu’une valeur Texte et Terme est spécifiée dans la page d’Ajoute de remplacement de l’extension de Requête, le code agit sur l’appariement spécifique. Lorsqu’un type de classification est spécifié sous la forme d’un terme (par exemple, un dictionnaire ou un autre mot Forms), la valeur Ne pas développer n’est convertie en aucun formulaire créé par la classification indiquée.

Supposons, par exemple, que vous ayez la définition suivante :

`Do Not Expand = "dog"`

`Type = Text`

`Term = "dogs"`

Une requête de recherche pour &quot;chien&quot;, qui s&#39;étend à &quot;chien&quot; et &quot;chien&quot; par le biais de Word alternatif Forms, n&#39;inclurait pas &quot;chien&quot;.

Toutefois, si la définition était la suivante :

`Do Not Expand = "dog"`

`Type = Alternate Word Forms`

La requête n&#39;inclut pas &quot;chien&quot; ou &quot;chien&quot; (le mot alternatif de Forms disponible pour &quot;chien&quot;).

Vous pouvez spécifier plusieurs termes, plusieurs classifications ou les deux. Cependant, si vous sélectionnez Tous comme type, toute liste à plusieurs termes est réduite en une seule entrée &quot;Tous&quot;.

Si des entrées de texte et de classification sont mélangées dans une règle, elles sont réorganisées dans l’interface utilisateur pour afficher d’abord les valeurs de texte. Cependant, cela n&#39;implique pas ou n&#39;affecte pas l&#39;ordre d&#39;évaluation au moment de la recherche.

Les termes textuels sont validés pour supprimer les références dénuées de sens. En d’autres termes, il compare le terme à la valeur Ne pas développer et supprime le terme en cas de correspondance. En outre, les valeurs Termes de duplicata, texte ou classification, sont supprimées.

Si vous ajoutez une nouvelle règle avec une valeur Ne pas développer qui reproduit une définition antérieure, les termes de la nouvelle définition sont ajoutés à l’original.

## Configuration des remplacements d&#39;extension de Requête {#task_A087354A509D4997BA275186C224160E}

Définition et ajout d&#39;un remplacement d&#39;extension de Requête dans Search &amp; Promote.

<!-- 

t_configuring_query_expansion_overrides.xml

 -->

>[!NOTE]
Par défaut, cette fonction n’est pas activée dans Search &amp; Promote. Contactez le support technique pour activer la fonction à utiliser. Une fois la fonction de remplacement de l&#39;extension de Requête activée, vous devez l&#39;activer dans l&#39;interface utilisateur. Les premières étapes ci-dessous montrent comment faire cela.

**Pour configurer les remplacements d&#39;extension de Requête**

1. Dans le Search &amp; Promote, cliquez sur **Paramètres** > **Utilisateur** > **Rôles de Vue**.
1. Sur la page Rôles de Vue, dans la colonne Actions du tableau, cliquez sur **Modifier** à droite du rôle auquel vous souhaitez donner accès dans le menu Linguistique.
1. Sur la page Modifier le rôle, développez l’arborescence Linguistique.
1. Cochez **Remplacement de l&#39;extension de Requête**, puis cliquez sur **Enregistrer les modifications**.
1. Cliquez sur **Linguistique** > **Remplacements d&#39;extension de Requête**.
1. Cliquez sur **Ajouter les remplacements d&#39;extension de Requête**.
1. Dans la page d&#39;Ajoute de l&#39;extension de Requête, définissez les options de votre choix.

   <!-- 
   
   r_query_expansion_override_definitions.xml
   
   -->

   <table> 
    <thead> 
      <tr> 
      <th colname="col1" class="entry"> <p>Option </p> </th> 
      <th colname="col2" class="entry"> <p>Description </p> </th> 
      </tr> 
    </thead>
    <tbody> 
      <tr> 
      <td colname="col1"> <p>Ne pas développer </p> </td> 
      <td colname="col2"> <p>Indique le mot ou l’expression que vous ne souhaitez pas développer. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Type </p> </td> 
      <td colname="col2"> <p>Sélectionnez <b>Texte</b> pour spécifier un appariement de mots ou d’expressions spécifique. Ou, sélectionnez une classification pour indiquer que le mot ou l'expression ne pas développer n'est pas converti par la classification sélectionnée. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Terme </p> </td> 
      <td colname="col2"> <p>Disponible uniquement si vous avez sélectionné <b>Texte</b> comme Type. Indique le mot ou l’expression à exclure de l’extension de recherche. </p> </td> 
      </tr> 
      <tr> 
      <td colname="col1"> <p>Action </p> </td> 
      <td colname="col2"> <p> Cliquez sur <b>+</b> ou <b>-</b> pour ajouter ou supprimer des termes, respectivement, à la définition. </p> </td> 
      </tr> 
    </tbody> 
    </table>

1. Lorsque vous avez terminé, cliquez sur **Ajouter**.

   Dans la page Définitions des remplacements de l&#39;extension de Requête, vous pouvez modifier ou supprimer les définitions que vous avez ajoutées.
1. Pour prévisualisation les résultats de vos ajouts, cliquez sur **régénérer l&#39;index de votre site intermédiaire** dans la zone bleue pour recréer rapidement l&#39;index de votre site Web intermédiaire.
1. (Facultatif) Effectuez l’une des opérations suivantes :

   * Cliquez sur **Live**.

      Voir [Affichage des paramètres en direct](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F).

   * Cliquez sur **Envoyer en direct**.

      Voir [Activation des paramètres d’étape](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4)

