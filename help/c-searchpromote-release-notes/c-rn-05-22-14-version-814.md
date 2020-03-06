---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 8.14.0 (22/05/2014)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 8.14.0 (22/05/2014)
topic: Release Notes,Site search and merchandising
uuid: 308d84a9-ec38-4fec-b146-e8a353e65be4
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.14.0 Release Notes (05/22/2014){#search-promote-release-notes}

**Correctifs**

* En cas d’échec de [!DNL sqlite_open], l’ancien fichier de base de données sqlite est supprimé et un nouveau fichier est entièrement créé.
* Les résultats principaux d’une recherche étaient incohérents lorsque la même recherche était effectuée à plusieurs reprises.
* Amélioration des performances du traitement des modèles lorsque de nombreux champs s’affichent par résultat de recherche.
* Ajout de notes à l’historique des règles métier.
* Lors des opérations d’indexation, les performances des déclencheurs basés sur les résultats et de la phase de regénération de l’index se dégradaient au fil du temps.
* Modification de l’option de **réinitialisation du cache SPIN** : le booléen no/next-run a été remplacé par un état triple : no/always/next-run.

