---
description: valeur nulle
seo-description: valeur nulle
seo-title: Notes de mise à jour de Search&amp ; amp ; Promote 8.9.3 (01/11/2012)
solution: Target
title: Notes de mise à jour de Search&amp ; amp ; Promote 8.9.3 (01/11/2012)
topic: Release Notes,Site search and merchandising
uuid: 7bc7bcb6-f47f-4e05-94e5-a22a13a187b7
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 84%

---


# Notes de mise à jour de Search &amp; Promote 8.9.3 (01/11/2012){#search-promote-release-notes}

## Notes de mise à jour de la Search &amp; Promote 8.9.3 (01/11/2012) {#concept_85F5B4B4C40C43FEA3AD63E6EA5593CF}

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nouvelles fonctionnalités et améliorations </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Facet Rail (Rampe de facettes) </p> </td> 
   <td colname="col2"> <p> 
     <!--3309390--> Ajout de l’option <span class="uicontrol">Facet Rail</span> afin de vous aider à mieux contrôler l’ordre des gammes et des noms de facettes (par nombre ou ordre alphabétique). </p> <p>Voir <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">A propos de la rampe de facettes</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> Facettes imbriquées </p> </td> 
   <td colname="col2"> <p> Ajout de la prise en charge du tri alternatif des facettes imbriquées. </p> <p>Voir <a href="../c-about-design-menu/c-about-facet-rails.md#concept_1FDC8BCDFFC84A0889DA670F63D5F6DB" format="dita" scope="local">A propos de la rampe de facettes</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Champ Remarques dans les règles de classement </p> </td> 
   <td colname="col2"> <p> 
     <!--3063772--> Ajout d’un champ <span class="wintitle">Remarques</span> de plusieurs lignes à la boîte de dialogue <span class="wintitle">Add Ranking Metric</span> (Ajouter une mesure de classement) et dans la boîte de dialogue <span class="wintitle">Edit Ranking Metric</span> (Modifier la mesure de classement) pour les règles de classement et les définitions des groupes de règles. </p> <p>Les remarques sur les règles de classement s’affichent sur la page <span class="wintitle">Define Ranking Rules</span> (Définir les règles de classement). Les remarques sur les groupes de règles s’affichent lorsque vous modifiez la définition. </p> <p>Voir <a href="../c-about-rules-menu/c-about-ranking-rules.md#concept_F555C076759B4E81B925441CFE707397" format="dita" scope="local">A propos des règles de classement</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Règles de fonctionnement  </p> </td> 
   <td colname="col2"> <p> 
     <!--3331637-->Amélioration de la prise en charge des pages d’entrée en supprimant les résultats naturels dans une règle de fonctionnement à l’aide de la nouvelle option <span class="uicontrol">Remove All Results</span> (Supprimer tous les résultats). </p> <p>Utilisez cette nouvelle option conjointement avec d’autres actions de règles de fonctionnement afin de créer des « pages d’entrée définies ». En d’autres termes, vous créez le contenu d’une page par actions de règles de fonctionnement exclusivement et ignorez les résultats « naturels » de la recherche. </p> <p>Voir <a href="../c-about-rules-menu/c-about-business-rules.md#task_BD3B31ED48BB4B1B8F1DCD3BFA2528E7" format="dita" scope="local">Ajout d’une nouvelle règle de fonctionnement</a> ou <a href="../c-about-rules-menu/c-about-business-rules.md#task_375CFA75D1D94D9E92A35DE1228E5087" format="dita" scope="local">Modification d’une règle de fonctionnement</a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bannières et règles de fonctionnement </p> </td> 
   <td colname="col2"> <p> Ajout d’une option de prise en charge grâce à laquelle vous pouvez éviter sous condition de publier les bannières lorsque la règle de fonctionnement qui référence ladite bannière est publiée. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Correctifs**

* Les règles de fonctionnement ne fonctionnaient pas de manière cohérente en présence d’un indice [!DNL Stage] (phase).
* Les règles de classement automatique s’appliquent désormais aux pages d’entrée définies.

   Voir la table des options dans [Ajouter une règle de classement](../c-about-rules-menu/c-about-ranking-rules.md#task_A132789FD4E5423DAD090DCDA7311E8A).

* [!DNL promosearch.cgi] ne renvoyait aucune promotion.

   Voir [A propos des recherches](../c-about-settings-menu/c-about-searching-menu.md#concept_207105CF26B1448F8A3D223787C56AB8).

* La publication de règles qui faisaient référence à de nombreuses bannières échouait parfois.

   Voir [A propos des bannières](../c-about-design-menu/c-about-banners.md#concept_5BBE01FEC6134393B43CC917C8CC64DA).

* **[!UICONTROL Did You Mean]** la mise en cache des requêtes de recherche est maintenant désactivée.

   Voir [A propos de Vouliez-vous dire](../c-about-linguistics-menu/c-about-did-you-mean.md#concept_7D4F3C29EF184B538B8AE2ECAE0CDC5E)

