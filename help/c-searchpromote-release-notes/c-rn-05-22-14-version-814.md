---
description: Search&amp ; amp ; Notes de mise à jour de Promote 8.14.0.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.14.0 (22/05/2014)
topic: Notes de mise à jour, Recherche sur le site et marchandisage
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 63%

---


# Notes de mise à jour de la version 8.14.0 (22/05/2014){#search-promote-release-notes} de la Search &amp; Promote 8.14.0

**Correctifs**

* En cas d’échec de [!DNL sqlite_open], l’ancien fichier de base de données sqlite est supprimé et un nouveau fichier est entièrement créé.
* Les résultats principaux d’une recherche étaient incohérents lorsque la même recherche était effectuée à plusieurs reprises.
* Amélioration des performances du traitement des modèles lorsque de nombreux champs s’affichent par résultat de recherche.
* Notes Ajoutées à **[!UICONTROL Business Rule History]**.
* Lors des opérations d’indexation, les performances des déclencheurs basés sur les résultats et de la phase de regénération de l’index se dégradaient au fil du temps.
* L&#39;option **[!UICONTROL Reset SPIN cache]** booléenne no/next-run a été remplacée par une option à trois états : no/always/next-run.

