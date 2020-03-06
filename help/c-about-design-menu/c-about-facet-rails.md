---
description: Utilisez Facet Rail pour réorganiser des groupes de facettes sur une page Web.
seo-description: Utilisez Facet Rail pour réorganiser des groupes de facettes sur une page Web.
seo-title: A propos du rail de facettes
solution: Target
subtopic: Navigation
title: A propos du rail de facettes
topic: Design,Site search and merchandising
uuid: 6da2bd67-8c20-4955-9836-bc8ba88546c5
translation-type: tm+mt
source-git-commit: 6b3aa733b0dfaace956f0ffc25f433fefd21e15f

---


# A propos du rail de facettes{#about-facet-rail}

Utilisez Facet Rail pour réorganiser des groupes de facettes sur une page Web.

## Utilisation du rail de facettes {#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB}

Une facette est une propriété ou une caractéristique, c&#39;est une façon de classer les résultats de la recherche de manière générale. Par exemple, le fabricant, le prix et la couleur peuvent être considérés comme un groupe de facettes. Chaque facette peut comporter plusieurs contraintes ou valeurs. Par exemple, si vous aviez la couleur comme une facette, les &quot;valeurs de facette&quot; peuvent être rouge, orange, jaune, vert, bleu, indigo et violet.

Voir [A propos des facettes](../c-about-design-menu/c-about-facets.md#concept_FA912B3B41EE493DB2F492D188457FF5).

Utilisez Facet Rail pour réorganiser ces groupes de facettes sur une page Web. Supposons, par exemple, que vous disposiez d’une section des résultats de recherche sur le côté gauche d’une page Web. La section répertoriait, de haut en bas, une facette Catégorie, une facette Marque, une facette Prix et une facette La plus populaire. A l’aide d’un rail de facettes, vous pouvez, par exemple, faire apparaître la facette La plus populaire au-dessus ou en dessous de la facette Catégorie.

Le groupe de facettes que vous souhaitez réorganiser ensemble appartient à une balise de rail de facettes. Une facette ne peut appartenir qu’à un seul rail de facettes. Le rail de facettes est une balise de modèle de présentation et renferme une représentation unique d’une facette. Toutes les facettes qui appartiennent à ce rail partagent cette représentation de facettes uniques.

Voir [A propos des modèles](../c-about-design-menu/c-about-templates.md#concept_06EB481B14864E18A8AE2BCD1D6EF0B5) et des facettes dans les balises [de modèle de](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)présentation.

## Configuration d’un rail de facettes {#task_561A8FF1CAD1402B9DD33E276BBC6A0E}

Vous pouvez ajouter un rail de facettes pour personnaliser votre calque de présentation. Les barres de facettes fournissent à vos clients une recherche guidée qui leur permet d’analyser en détail les résultats de leur recherche en fonction de l’ordre des facettes sur votre page Web.

<!-- 

t_configuring_facet_rail.xml

-->

Toute modification apportée aux rails de facettes peut être annulée à l’aide de la fonction Historique.

**Pour configurer un rail de facettes**

1. Avant de pouvoir configurer un rail de facettes, assurez-vous d’avoir déjà ajouté une facette et, dans le cadre de cette tâche, spécifiez un nom de rail de facettes.

   Voir [Ajout d’une nouvelle facette](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B).
1. Dans le menu du produit, cliquez sur **[!UICONTROL Design]** > **[!UICONTROL Navigation]** > **[!UICONTROL Facet Rail.]**
1. Sur la [!DNL Facet Rail] page, sélectionnez les facettes à inclure dans le rail des facettes, puis définissez l’ **[!UICONTROL Sort Facets Method]** option dans la liste déroulante.

   <!-- 
   r_facet_rail_options.xml
   -->

   | Fonctionnalité/Option | Description |
   |--- |--- |
   | Facet Rail (Rampe de facettes) Nom | Identifie le nom du rail de facettes.  Vous créez le nom du rail de facettes au moment où vous ajoutez la facette.  Voir [Ajout d’une nouvelle facette](../c-about-design-menu/c-about-facets.md#task_FC07BFFA62CA4B718D6CBF4F2855C89B) |
   | Facettes incluses | Liste des facettes possibles que vous pouvez sélectionner pour ajouter au rail des facettes.  Si vous choisissez de trier les facettes à l’aide `Custom`, l’ordre dans lequel vous sélectionnez les facettes ici détermine l’ordre dans lequel elles apparaissent dans la `Custom Facet Order` zone de texte. |
   | Méthode de tri des facettes | Choisissez l’une des trois options suivantes dans la liste déroulante :<ul><li>`Alpha` Les facettes sont triées par ordre alphabétique en fonction de leur nom, y compris les caractères de ponctuation.</li><li>`Alpha (not case sensitive)` Les facettes sont triées par ordre alphabétique en fonction de leurs noms, en ignorant la casse des caractères alphabétiques et en incluant les caractères de ponctuation. </li><li>`Alpha (alphanumeric only)` Les facettes sont triées par ordre alphabétique par rapport à leurs noms, en ignorant les caractères de ponctuation. </li><li>`Alpha (not case sensitive, alphanumeric only)` Les facettes sont triées par ordre alphabétique en fonction de leurs noms, en ignorant la casse des caractères alphabétiques et en ignorant les caractères de ponctuation. </li><li>`Count` Les facettes sont triées en fonction du nombre. </li><li>`Custom` Ouvre la `Custom Facet Order` zone de texte qui vous permet de définir l’ordre des facettes en saisissant le nom exact de chaque facette. Les libellés de facettes laissés de côté sont supprimés de la `Custom Facet Order` liste.</li></ul> |
   | Ordre personnalisé des facettes | Cette option est disponible uniquement si vous l’avez sélectionnée `Custom` dans la `Sort Facets Method` liste déroulante.  Vous permet de répertorier les noms des facettes, soit une par ligne, soit sur une ligne et séparés par des virgules. Si des libellés de facette sont définis, ils sont affichés dans la `Facets Included` liste, entre parenthèses.  N’incluez pas d’étiquettes de facettes dans la `Custom Facet Order` zone de texte.  Lorsque vous sélectionnez ou désélectionnez des facettes dans la `Facets Included` liste, la `Custom Facet Order` zone de texte est automatiquement mise à jour. |

1. Cliquez sur **[!UICONTROL Save Changes]**.
1. (Facultatif) Sur la [!DNL Facet Rail] page, effectuez l’une des opérations suivantes :

   * Cliquez sur **[!UICONTROL History]** pour annuler les modifications que vous avez apportées.

      Voir [Utilisation de l’option](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002)Historique.

   * Cliquez sur **[!UICONTROL Live]**.

      Voir [Affichage des paramètres](../c-about-staging.md#task_401A0EBDB5DB4D4CA933CBA7BECDC10F)en direct.

   * Cliquez sur **[!UICONTROL Push Live]**.

      Voir [Pousser les paramètres d’étape en direct](../c-about-staging.md#task_44306783B4C0408AAA58B471DAF2D9A4).

1. Modifiez le modèle de présentation en procédant comme suit :

   * Créez un &quot;modèle de facette&quot; sur le modèle de présentation.
   * Entourez le &quot;modèle de facette&quot; avec les `<guided-facet-rail>` balises.

      Voir Facettes dans les balises [de modèle de](../c-appendices/c-templates.md#reference_F1BBF616BCEC4AD7B2548ECD3CA74C64)présentation.

      Exemple :

      ```
      <guided-facet-rail>
        <guided-facet>
          <guided-facet-display-name/>
          ...
          </guided-facet>
        </guided-facet-rail>
      ```

      Ces balises sculptent une section du modèle de présentation pour devenir un modèle répétable pour chaque facette du rail de facettes. Chaque facette appartenant au rail de facettes utilise cette section découpée pour évaluer sa sortie. Une seule `<guided-facet-rail>` balise peut apparaître sur le modèle de présentation final.

      Les balises suivantes n’ont pas besoin de l’ `gsname` attribut à l’intérieur `<guided-facet-rail>` , car la valeur est déterminée dynamiquement au moment de la recherche et remplacée correctement :

      `<guided-facet>`
      `<guided-facet-display-name>`
      `<guided-facet-total-count>`
      `<guided-facet-undo-link>`
      `<guided-facet-undo-path>`
      `<guided-facet-behavior>`

   * Enregistrez le modèle de présentation et poussez-le en direct.

      Voir [Modification d’une présentation ou d’un modèle](../c-about-design-menu/c-about-templates.md#task_800E0E2265C34C028C92FEB5A1243EC3)de transport.
