---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 8.13.0 (16/04/2014)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 8.13.0 (16/04/2014)
topic: Release Notes,Site search and merchandising
uuid: b3524992-ff00-4a7c-a404-078242456734
translation-type: tm+mt
source-git-commit: 9d5ac055d665b39d09b28063179d74a389d7f830

---


# Search&amp;Promote 8.13.0 Release Notes (04/16/2014){#search-promote-release-notes}

| Nouvelle fonctionnalité et amélioration | Description |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Facettes dynamiques avec prise en charge complète des correspondances de table | Certains clients possédaient de nombreux attributs de &quot;niveau SKU&quot; qu’ils voulaient sélectionner et afficher au moyen de facettes dynamiques. Pour cette raison, vous pouvez désormais associer éventuellement chaque champ de facette dynamique à un nom de table dans une configuration de compte statique. Ces relations de table peuvent ensuite être appliquées au moment de la recherche pour tous les champs de facette dynamique impliqués dans cette dernière. Voir [A propos des faits](../c-about-design-menu/c-about-dynamic-facets.md#concept_E65A70C9C2E04804BF24FBE1B3CAD899)dynamiques. |

**Correctifs**

* Changed the data view description field to use the tag `<search-display-field>` instead of the `<search-description>`.
* Ajout d’une fonctionnalité à Index Connector pour que la clé principale devienne la concaténation de deux champs ou davantage.
* Modification du script AttributeLoader-Regen-Enabled `attributeloader-regen.pl` afin ne pas coder en HTML les valeurs.
* Correspondance du traitement des espaces de durée d’indexation et de durée de recherche pour les demandes de recherche de plage.
* L’ajout d’une règle métier entraînait parfois une erreur lorsque les facettes dynamiques étaient activées.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* A Javascript error prevented adding or editing a definition in **Settings** > **SPIN** > **IndexConnector**.
* Après l&#39;enregistrement d&#39;une règle métier, il s&#39;est avéré que lorsque l&#39;heure était sélectionnée lors de la création d&#39;une règle métier, elle était définie par défaut sur le fuseau horaire GMT. Une fois la règle enregistrée, il est apparu que le fuseau horaire du compte était ensuite pris en compte.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Le tri des règles métier dans un environnement d’évaluation ne fonctionnait pas correctement.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Les rapports sur les performances des recherches ont été améliorés afin de vous permettre de les planifier en vue de leur remise par courrier électronique.
* La planification fixe des règles métier était automatiquement changée lors du passage à l’heure d’été.

   See [About Business Rules](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* Si un grand nombre de champs de facette dynamique ont été définis, les utilisateurs ont connu des temps de réponse de recherche principaux lents.
* De fausses erreurs d’index de plage se produisaient.
* L’accès à Dynamic Media Classic dans les centres de données non nord-américains a été interrompu.
* La fonction de validation XPath SPIN retournait une erreur de faux positif.

* Après une opération d’activation/de désactivation SPIN, l’utilisateur était redirigé vers la page de connexion du centre des membres.

