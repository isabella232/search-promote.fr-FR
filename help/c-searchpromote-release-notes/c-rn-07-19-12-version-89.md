---
description: Search&amp ; amp ; Notes de mise à jour de Promote 8.9.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.9 (19/07/2012)
topic: Release Notes,Site search and merchandising
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 60%

---


# Notes de mise à jour de Search &amp; Promote 8.9 (19/07/2012){#search-promote-release-notes}

**Nouvelles fonctionnalités**

* Améliorations de la gestion des métadonnées - Définition des métadonnées dynamiques à partir des flux client

   Création d’un modèle permettant de reconfigurer dynamiquement votre compte Search&amp;Promote en fonction des métadonnées fournies par le client.
* Amélioration des performances d&#39;indexation - Chargeur d&#39;index

   Le chargeur d’index fournit une nouvelle méthode d’importation du contenu XML directement dans un index Search&amp;Promote. Il s’agit du sous-ensemble de la fonctionnalité Index Connector existante, conçue pour importer rapidement nos fichiers de flux XML standard.

**Correctifs et améliorations**

* Ajout de la prise en charge de la modification de l’option de tri par une règle métier.
* Dans le système d’aide, la balise `<search-description>` affiche le corps lorsque la balise meta de la description est vide.
* Ajout de la capacité d’effectuer un suivi sur les accès aux tables applicables pour les résultats qui ont été ajoutés au moyen des actions basées sur les résultats.
* Ajout de la prise en charge de l’envoi de paramètres de requête au moyen de POST
* Lors de l’analyse, une opération mirror_account finale peut être ignorée dans certains cas.
* Les URL Adobe Analytics n’incluent pas les arguments CGI et le code de Search &amp; Promote qui effectue les recherches Adobe Analytics nécessaires pour supprimer de la même manière les arguments CGI des clés URL.
* Les règles réécrites disparaissaient par intermittence de l’interface utilisateur une fois qu’elles avaient été publiées.
* Les comptes de Search &amp; Promote avec les paramètres Voulez-vous dire qui ont été configurés pour faire des suggestions en raison de résultats faibles peuvent avoir des résultats intermittents.
* La sortie du test de la règle de réécriture n’avait pas de sauts de ligne.
* La page des règles d’URL de recherche et la page d’analyse des règles d’URL de banque de liste pointaient vers une page Historique incorrecte.
* Le fait de cliquer sur Modifier sur certaines bannières n’affichait pas la page Modifier.
* Le reclassement du code de mise à jour était parfois extraordinairement lent.
* Le retrait ou la publication d’un élément de facette ne fonctionnait pas si les lettres du nom de la facette étaient en minuscules et en majuscules.

