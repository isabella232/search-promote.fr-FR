---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 8.14.0 (22/05/2014)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 8.14.0 (22/05/2014)
topic: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
translation-type: tm+mt
source-git-commit: ffdec2cfcb30e733c664a7d1ca23868b7a9a9aa5

---


# Search&amp;Promote 8.14.0 Release Notes (05/22/2014){#search-promote-release-notes}

**Correctifs**

* En cas d’échec de [!DNL sqlite_open], l’ancien fichier de base de données sqlite est supprimé et un nouveau fichier est entièrement créé.
* Les résultats principaux d’une recherche étaient incohérents lorsque la même recherche était effectuée à plusieurs reprises.
* Amélioration des performances du traitement des modèles lorsque de nombreux champs s’affichent par résultat de recherche.
* Ajout de notes à **[!UICONTROL Business Rule History]**.
* Lors des opérations d’indexation, les performances des déclencheurs basés sur les résultats et de la phase de regénération de l’index se dégradaient au fil du temps.
* Changed **[!UICONTROL Reset SPIN cache]** option from boolean no/next-run to a tri-state: no/always/next-run.

