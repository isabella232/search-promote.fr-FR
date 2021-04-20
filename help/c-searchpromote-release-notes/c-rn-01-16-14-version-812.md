---
description: Search&amp ; amp ; Notes de mise à jour de Promote 8.12.0.
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.12.0 (16/01/2014)
topic: Release Notes,Site search and merchandising
uuid: 4db10eb4-11bf-4483-a7f2-87981d9c7a50
translation-type: tm+mt
source-git-commit: d015154efdccbb4c6a39a56907c0c337ec065c9f
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 72%

---


# Notes de mise à jour de la version 8.12.0 de la Search &amp; Promote (16/01/2014){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nouvelles fonctionnalités et améliorations </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Ajout de dictionnaires de recherche du radical </p> </td> 
   <td colname="col2"> <p> </p> <p> Des dictionnaires de recherche du radical ont été ajoutés pour l’indonésien et le turc. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-dictionaries.md#concept_B8028B71EC8144669614C64578EDB034" format="dita" scope="local"> A propos des dictionnaires</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Rapports d’exportation </p> </td> 
   <td colname="col2"> <p> 
     <!--3683368-->Vous pouvez désormais exporter des données au format CSV à partir des rapports suivants : 
     <ul id="ul_93B619DBB3444F64BD6D7F9E969AB1E1"> 
      <li id="li_96DDE1A196834845A0FA319903C5934B"> <p>Rapport Termes </p> </li> 
      <li id="li_4F1A19DE98C84F8CAD963EEA2B38ED7A"> <p>Rapport Termes de recherche nuls </p> </li> 
      <li id="li_A7716C62C4D44CD69D411C3FEE246D96"> <p>Rapport Requête de recherche </p> </li> 
     </ul> </p> <p>Voir <a href="../c-about-reports-menu/c-about-reports-menu.md#concept_5F901459C7AB461BAB30B305957EB00C" format="dita" scope="local"> A propos du menu Rapports</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Ne pas associer </p> </td> 
   <td colname="col2"> <p>Vous pouvez maintenant contrôler quels sont les deux mots qui ne devraient pas être associés dans les résultats de recherche, par exemple « pull-over » et « pull ». </p> <p> <p>Remarque : cette fonctionnalité n’est pas activée par défaut. Contactez le service d’assistance à la clientèle Adobe pour l’activer dans Search&amp;Promote. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correctifs**

* Vous ne pouvez pas ajouter de résultats à une zone recommandée située en dehors des critères de facettes actuellement sélectionnés.
* Vous ne pouviez pas enregistrer de règles basées sur les résultats pour un compte avec recherche HTTPS uniquement.
* La configuration d’une règle métier pour « n’est pas un appareil mobile » ne fonctionnait pas.

   Voir [A propos des règles de fonctionnement](../c-about-rules-menu/c-about-business-rules.md#concept_2A93D76216754D3D8412CDEA00BD26BD).

* L’exécution d’une recherche avec filtre d’inventaire ne renvoyait aucun résultat.
* La commande de facettes Taille n’était pas mise à jour.
* Ajout de l’option pour une définition de règle « personnalisée » à la page de nettoyage des requêtes.

   Voir [A propos des règles de nettoyage de Requête](../c-about-rules-menu/c-about-query-cleaning-rules.md#concept_17F3CDDC3C8A4128AF092A82B777B86C).

* Le rapport Termes répétait les entrées s’il n’y avait pas suffisamment de données.

   Voir [Affichage du rapport Termes ou du rapport Termes de recherche nuls..](../c-about-reports-menu/c-about-reports-menu.md#task_53B7ED1582DD4B0E8376546A7AFC789A).

* La publication d’une règle métier unique fonctionnait en mode d’évaluation, mais échouait en mode d’activation.
* Les modifications de saisie semi-automatique visant à inclure ou à exclure les listes n’étaient pas enregistrées dans l’historique et, par conséquent, ne pouvaient pas être annulées.

   Voir [À propos de la saisie semi-automatique](../c-about-auto-complete.md#concept_093A9CD754864BA79B456FE4BEB64578).

