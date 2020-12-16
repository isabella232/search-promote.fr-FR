---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp ; amp ; Promote 8.9.8 (23/05/2013)
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.9.8 (23/05/2013)
topic: Release Notes,Site search and merchandising
uuid: ff4bfc53-1d0e-4b7d-83ad-54c81d3f9769
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 57%

---


# Notes de mise à jour de Search &amp; Promote 8.9.8 (23/05/2013){#search-promote-release-notes}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nouvelle fonctionnalité </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> Expressions courantes : prise en charge des correspondances exactes </p> </td> 
   <td colname="col2"> <p> Les expressions courantes contiennent des termes de deux mots ou plus qui font l'objet d'une recherche dans leur ensemble, comme "boot cut" ou "tank top", et non comme des parties distinctes. Une expression courante a une signification unique qui est différente des différents mots qui la compose. </p> <p> Vous gérez un dictionnaire d'expressions courantes liées à votre activité. Lorsqu'un client effectue une requête de recherche qui contient plusieurs mots, le dictionnaire fait l'objet d'une recherche pour déterminer s'il existe une correspondance exacte. </p> <p>Vous pouvez ajouter, modifier ou supprimer des expressions courantes. Vous pouvez également regrouper des expressions courantes dans des dictionnaires de domaine. Vous pouvez par exemple regrouper des expressions courantes par mesures, achats, bijoux, tissus et catégorie générale. </p> <p>Voir <a href="../c-about-linguistics-menu/c-about-common-phrases.md#concept_4946E53586DF492EAEB1B7F757FD440F" format="dita" scope="local"> À propos des expressions courantes </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correctifs et améliorations**

* Le paramètre CGI de recherche principale `sp_date_range_#` ne fonctionnait pas pour les champs définis par l&#39;utilisateur.

   Voir [Paramètres CGI de recherche dorsale](../c-appendices/c-cgiparameters.md#reference_582E85C3886740C98FE88CA9DF7918E8).

* La restauration de la version **[!UICONTROL History]** n&#39;a pas mis à jour le contenu du champ des points d&#39;entrée d&#39;URL.

   Voir [Utilisation de l’option Historique](../t-using-the-history-option.md#task_70DD3F87A67242BBBD2CB27156F43002).

   Voir aussi [A propos des points d’entrée d’URL](../c-about-settings-menu/c-about-crawling-menu.md#concept_5D857E3B5C124E85BC0B5AE77A509573).

* Le codage JSON ne gérait pas les caractères codés de manière incorrecte.
* Une nouvelle prise en charge permet d&#39;activer à distance un index intermédiaire.

   Voir [À propos du contrôle à distance pour l&#39;indexation](../c-about-index-menu/c-about-remote-control-for-indexing.md#concept_C79B322190E84106A434E5C6D4A4118F).

