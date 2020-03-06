---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp;Promote 8.9 (19/07/2012)
solution: Target
title: Notes de mise à jour de Search&amp;Promote 8.9 (19/07/2012)
topic: Release Notes,Site search and merchandising
uuid: 3853c75d-19ed-4e36-9e81-dcbffe5f5b0c
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Search&amp;Promote 8.9 Release Notes (07/19/2012){#search-promote-release-notes}

**Nouvelles fonctionnalités**

* Améliorations de la gestion des métadonnées - Définition des métadonnées dynamiques à partir des flux client

   Création d’un modèle permettant de reconfigurer dynamiquement votre compte Search&amp;Promote en fonction des métadonnées fournies par le client.
* Amélioration des performances d’indexation - Chargeur d’index

   Le chargeur d’index fournit une nouvelle méthode d’importation du contenu XML directement dans un index Search&amp;Promote. Il s’agit du sous-ensemble de la fonctionnalité Index Connector existante, conçue pour importer rapidement nos fichiers de flux XML standard.

**Correctifs et améliorations**

* Ajout de la prise en charge de la modification de l’option de tri par une règle métier.
* In the Help system `<search-description>` tag shows the body instead when the meta tag for the description has empty content.
* Ajout de la capacité d’effectuer un suivi sur les accès aux tables applicables pour les résultats qui ont été ajoutés au moyen des actions basées sur les résultats.
* Ajout de la prise en charge de l’envoi de paramètres de requête au moyen de POST
* Lors de l’analyse, une opération mirror_account finale peut être ignorée dans certains cas.
* Les URL d’Adobe Analytics n’incluent pas les arguments CGI et le code Search&amp;Promote nécessaire aux recherches d’Adobe Analytics pour dépouiller de la même manière les arguments CGI des clés d’URL.
* Les règles réécrites disparaissaient par intermittence de l’interface utilisateur une fois qu’elles avaient été publiées.
* Les comptes Search&amp;Promote avec les paramètres Voulez-vous dire qui étaient définis pour faire des suggestions en raison de résultats faibles peuvent avoir des résultats intermittents.
* La sortie du test de la règle de réécriture n’avait pas de sauts de ligne.
* La page des règles d’URL de recherche et la page d’analyse des règles d’URL de banque de liste pointaient vers une page Historique incorrecte.
* Le fait de cliquer sur Modifier sur certaines bannières n’affichait pas la page Modifier.
* Le reclassement du code de mise à jour était parfois extraordinairement lent.
* Le retrait ou la publication d’un élément de facette ne fonctionnait pas si les lettres du nom de la facette étaient en minuscules et en majuscules.

