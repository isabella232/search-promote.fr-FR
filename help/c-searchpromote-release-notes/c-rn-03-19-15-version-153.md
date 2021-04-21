---
description: Search&amp ; amp ; Notes de mise à jour de Promote 15.3.1.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 15.3.1 (24/03/2015)
topic-legacy: Release Notes,Site search and merchandising
uuid: f02da5a4-2207-4603-aa05-5cff7be16dd5
exl-id: 2d254275-f777-45e5-a838-b6a35365a6dd
translation-type: tm+mt
source-git-commit: 7559f5f7437d46e3510d4659772308666425ec96
workflow-type: tm+mt
source-wordcount: '254'
ht-degree: 1%

---

# Notes de mise à jour de la Search &amp; Promote 15.3.1 (24/03/2015){#search-promote-release-notes}

## Nouvelles fonctionnalités et améliorations {#section_2A10EF6B40FC4F2CB2381FFA9FFA64BD}

* Recherche de numéros de modèle de produit : Ajoute un nouveau paramètre Linguistique qui vous permet de fractionner les jetons en fonction de transitions alphabétiques et numériques. Cette fonctionnalité permet des correspondances en texte libre plus souples sur les jetons de style article ou produit.

   Voir **[!UICONTROL Partial Alphanumeric Matching]** dans [Configuration de la correspondance des termes de recherche avec votre contenu Web...](../c-about-linguistics-menu/c-about-words-and-language.md#task_351A9144A51F4B41923BDBACDEF3B616).

* Possibilité Ajoutée d’exporter les résultats des vues de données.

   Voir [A propos des Vues de données](../c-about-reports-menu/c-about-data-views.md#concept_DCA897D074464BC1861AA47B40CC86C3).

* Plages générées de manière dynamique pour les attributs de plage, fonctions de regroupement à valeur de facette automatique.

   Adobe Systems exige actuellement que vous fournissiez le contenu identifiant les valeurs de plage pour ce faire. Par exemple, pour un prix de 10, générez une chaîne de plage &quot;Entre 10 et 20 USD&quot;). Ou, Adobe Systems exige que vous utilisiez le filtrage par script. Ajout de nouveaux attributs à une définition de champ de métadonnées, pour les champs `Type=Number` uniquement. Les nouvelles options associent le champ numérique à un champ `Type=Text` et spécifient des informations de configuration décrivant comment la description de la plage est générée.

   Voir [Ajouter un nouveau champ de balise meta](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5).

## Correctifs {#section_22D1AFC99F394D569898828A0D3C419D}

* La boîte de dialogue de modification du rail de facettes doit inclure des facettes intermédiaires.
* Résultats de recherche principaux vides pour le mode de recherche &quot;incorporé&quot;, pour une recherche contenant des caractères japonais.
* La conversion Tika des fichiers .docx Word renseigne désormais l’attribut `title`.
* Correction de messages erronés de &quot;bannière de duplicata&quot; dans le gestionnaire **[!UICONTROL Banner]**.
* [!DNL Dynamic Media Classic] les bannières sont désormais indépendantes du protocole.
* L&#39;attribut de champ **[!UICONTROL Table Name]** était parfois masqué lors de la modification de champs définis par l&#39;utilisateur dans l&#39;interface utilisateur des métadonnées, même si **[!UICONTROL Dynamic Facets]** était activé pour le compte.
* **[!UICONTROL Recent Searches]** n’encode plus de caractères non-ASCII à plusieurs noeuds.
* Les champs MDI peuvent être renseignés sans avoir recours au filtrage par script.
* Codage incorrect dans les suggestions.
* Le déclencheur &quot;autre facette sélectionnée&quot; fonctionne désormais correctement avec les règles métier complexes.
