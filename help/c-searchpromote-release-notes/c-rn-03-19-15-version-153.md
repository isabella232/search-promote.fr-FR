---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 15.3.1 (24/03/2015)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 15.3.1 (24/03/2015)
topic: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 15.3.1 Release Notes (03/24/2015){#search-promote-release-notes}

## Nouvelles fonctionnalités et améliorations {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Recherche de numéros de modèle de produit - Ajout d&#39;un nouveau paramètre Linguistique qui vous permet de fractionner éventuellement les jetons sur des  alphanumériques. Cette fonctionnalité permet des correspondances de texte libre plus souples sur les jetons de style de pièce ou de produit.

   Reportez-vous **[!UICONTROL Partial Alphanumeric Matching]** à la section [Configuration de la correspondance des termes de recherche avec votre contenu Web...](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* Ajout de la capacité d’exporter les résultats  des de données.

   Voir [A propos des](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3)de données.

* Plages générées dynamiquement pour les attributs de plage des fonctions de cumul automatique de facettes et de valeurs.

   Pour ce faire, Adobe Systems vous demande actuellement de fournir le contenu identifiant les valeurs de plage. Par exemple, pour un prix de 10, générez une chaîne de plage &quot;Entre 10 et 20 USD&quot;. Adobe Systems vous demande également d’utiliser le filtrage par script. Ajout de nouveaux attributs à une définition de champ de métadonnées, pour `Type=Number` les champs uniquement. Les nouvelles options associent le champ numérique à un `Type=Text` champ et spécifient des informations de configuration décrivant la manière dont la description de la plage est générée.

   Voir [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.

## Correctifs {#section_22D1AFC99F394D569898828A0D3C419D}

* La boîte de dialogue de modification du rail de facettes doit inclure des facettes intermédiaires.
* Résultats de recherche principaux vides pour le mode de recherche &quot;incorporé&quot;, pour une recherche contenant des caractères japonais.
* La conversion Tika des fichiers .docx Word renseigne désormais l’ `title` attribut.
* Correction des messages erronés de la bannière &quot;&quot; dans le **[!UICONTROL Banner]** gestionnaire.
* [!DNL Dynamic Media Classic] les bannières sont maintenant agnostiques du protocole.
* L’attribut de **[!UICONTROL Table Name]** champ était parfois masqué lors de la modification de champs définis par l’utilisateur dans l’interface utilisateur des métadonnées, même lorsque **[!UICONTROL Dynamic Facets]** le compte était activé.
* **[!UICONTROL Recent Searches]** n’encode plus de caractères non ASCII à plusieurs chiffres.
* Les champs MDI peuvent être renseignés sans avoir recours au filtrage par script.
* Codage incorrect dans les suggestions.
* Le déclencheur &quot;autre facette sélectionnée&quot; fonctionne désormais correctement avec les règles de fonctionnement complexes.

