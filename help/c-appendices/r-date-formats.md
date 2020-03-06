---
description: Vous pouvez définir les formats de date utilisés lorsqu’il analyse et indexe un champ avec un type de données "date".
seo-description: Vous pouvez définir les formats de date utilisés lorsqu’il analyse et indexe un champ avec un type de données "date".
seo-title: Formats de date
solution: Target
title: Formats de date
topic: Appendices,Site search and merchandising
uuid: 148914b5-33ef-41db-8404-67c03f6f0832
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# Formats de date{#date-formats}

Vous pouvez définir les formats de date utilisés lorsqu’il analyse et indexe un champ avec un type de données &quot;date&quot;.

Le format de la date et de l’heure est spécifié avec une chaîne de format. La chaîne de format comprend zéro ou plusieurs spécifications de conversion (une spécification de conversion est constituée d’un symbole de pourcentage et d’un autre caractère) et de caractères ordinaires. Une liste par défaut contient des chaînes de format de date pour chaque champ de date.

Vous contrôlez complètement cette liste et pouvez l&#39;ajouter ou la modifier en fonction des besoins de votre site. La chaîne de format supérieure est prioritaire et les chaînes de format suivantes ne sont utilisées que si l’analyse du contenu d’une balise de métadonnées donnée génère une erreur.

Supposons, par exemple, que vous ayez spécifié les formats de date suivants :

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> <p>%b %d %Y %T %Z </p> <p>%A %B %d %Y %T %Z </p> <p>%A %b %d %Y %T %Z </p> <p>%a %B %d %Y %T %Z </p> <p>%a %b %d %Y %T %Z </p> <p>%d %b %Y %T %Z </p> </td> 
  </tr> 
 </tbody> 
</table>

Le premier format, &quot;%B %d, %Y %T %Z&quot;, correspond à des dates du type &quot;20 septembre 2014 13:12:00 PDT&quot;. Si le contenu de la balise de métadonnées ne peut pas être analysé avec cette chaîne de format, le format suivant &quot;%b %d, %Y %T %Z&quot; est essayé. Ce format correspond aux dates suivantes : &quot;20 Septembre 2014 3:12:00 PDT&quot;. Si le contenu de la balise de métadonnées ne peut pas être analysé avec cette chaîne de format, la recherche/marchandisage sur le site déplace la liste des chaînes de format jusqu’à ce qu’elle trouve une chaîne de format qui fonctionne.

Le tableau suivant décrit les chaînes de format de date disponibles :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Format de données </p> </th> 
   <th colname="col2" class="entry"> <p>Description </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%Une </p> </td> 
   <td colname="col2"> <p>Correspond à la représentation nationale du nom complet du jour de la semaine, par exemple "Lundi". La représentation nationale est déterminée à partir du paramètre "Langue" de l’option "Mots et langues". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a </p> </td> 
   <td colname="col2"> <p> correspond à la représentation nationale du nom abrégé du jour de la semaine, où l’abréviation est les trois premiers caractères, p. ex. "Mon." La représentation nationale est déterminée à partir du paramètre "Langue" de l’option "Mots et langues". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%B </p> </td> 
   <td colname="col2"> <p> correspond à la représentation nationale du nom complet du mois, p. ex. "Juin." La représentation nationale est déterminée à partir du paramètre "Langue" de l’option "Mots et langues". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b </p> </td> 
   <td colname="col2"> <p> correspond à la représentation nationale du nom abrégé du mois, où l’abréviation est les trois premiers caractères, p. ex. "Jun." La représentation nationale est déterminée à partir du paramètre "Langue" de l’option "Mots et langues". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%D </p> </td> 
   <td colname="col2"> <p> est équivalent à "%m/%d/%y", par ex. "06/06/01" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d </p> </td> 
   <td colname="col2"> <p> correspond au jour du mois en tant que nombre décimal (01-31) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%e </p> </td> 
   <td colname="col2"> <p> correspond au jour du mois en tant que nombre décimal (1-31) ; les chiffres uniques sont précédés d’un blanc </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%H </p> </td> 
   <td colname="col2"> <p> correspond à l’heure (horloge de 24 heures) comme nombre décimal (00-23) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%h </p> </td> 
   <td colname="col2"> <p> correspond à la représentation nationale du nom abrégé du mois, où l’abréviation est les trois premiers caractères, p. ex. "Jun" (identique à %b) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%I </p> </td> 
   <td colname="col2"> <p> correspond à l’heure (horloge de 12 heures) comme nombre décimal (01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%j </p> </td> 
   <td colname="col2"> <p> correspond au jour de l’année sous forme de nombre décimal (001-366) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%k </p> </td> 
   <td colname="col2"> <p> correspond à l’heure (horloge de 24 heures) comme un nombre décimal (0-23) ; les chiffres uniques sont précédés d’un blanc </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%l </p> </td> 
   <td colname="col2"> <p> correspond à l’heure (horloge de 12 heures) comme nombre décimal (1-12) ; les chiffres uniques sont précédés d’un blanc </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%M </p> </td> 
   <td colname="col2"> <p> correspond à la minute sous forme de nombre décimal (00-59) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%m </p> </td> 
   <td colname="col2"> <p> correspond au mois sous forme de nombre décimal (01-12) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%p </p> </td> 
   <td colname="col2"> <p> correspond à la représentation nationale de "ante meridiem" ou de "post meridiem" selon le cas, p. ex. "PM." La représentation nationale est déterminée à partir du paramètre "Langue" de l’option "Mots et langues". </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%R </p> </td> 
   <td colname="col2"> <p> est équivalent à "%H:%M", par ex. "13:23" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%r </p> </td> 
   <td colname="col2"> <p> est équivalent à "%I:%M:%S %p", par ex. "01:23:45 PM" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%S </p> </td> 
   <td colname="col2"> <p> correspond au deuxième nombre décimal (00-60) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%T </p> </td> 
   <td colname="col2"> <p> est équivalent à "%H:%M:%S", par ex. "13:26:47" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%U </p> </td> 
   <td colname="col2"> <p> correspond au numéro de semaine de l’année (dimanche comme premier jour de la semaine) en tant que nombre décimal (00-53) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%v </p> </td> 
   <td colname="col2"> <p> est équivalent à "%e-%b-%Y", par ex. "6-Jun-2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%O </p> </td> 
   <td colname="col2"> <p> correspond à l’année avec le siècle comme nombre décimal, p. ex. "2001" </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%y </p> </td> 
   <td colname="col2"> <p> correspond à l’année sans siècle comme nombre décimal (00-99) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%Z </p> </td> 
   <td colname="col2"> <p> correspond au nom du fuseau horaire </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%% </p> </td> 
   <td colname="col2"> <p> matches "%" </p> </td> 
  </tr> 
 </tbody> 
</table>

**Chaînes de format par défaut**

Les chaînes de format par défaut suivantes sont utilisées par les modèles. Vous pouvez l’ajouter à cette liste ou la modifier si nécessaire.

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chaîne de format par défaut </p> </th> 
   <th colname="col2" class="entry"> <p>Exemple résultant </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>%B %d, %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 septembre 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%b %d %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 septembre 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %B %d %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Dimanche 5 septembre 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%A %b %d %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Dimanche 5 septembre 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %B %d %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Sun 5 septembre 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%a %b %d %Y %T %Z </p> </td> 
   <td colname="col2"> <p> Sun Sep 5, 1999 13:12:00 PDT </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>%d %b %Y %T %Z </p> </td> 
   <td colname="col2"> <p> 5 Sep 1999 13:12:00 PDT </p> </td> 
  </tr> 
 </tbody> 
</table>

