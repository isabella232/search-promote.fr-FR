---
description: Actualisation concernant la syntaxe et les règles de construction des expressions régulières.
seo-description: Actualisation concernant la syntaxe et les règles de construction des expressions régulières.
seo-title: Expressions régulières
solution: Target
title: Expressions régulières
topic: Appendices,Site search and merchandising
uuid: 369b54f6-372a-41de-bb5d-3ae0bd640199
translation-type: tm+mt
source-git-commit: 7b883870bb16284d8070a21547cdb62cc79d7632
workflow-type: tm+mt
source-wordcount: '1058'
ht-degree: 1%

---


# Regular Expressions{#regular-expressions}

Actualisation concernant la syntaxe et les règles de construction des expressions régulières.

Voir aussi [Configuration d’un index incrémentiel d’un site Web](../c-about-index-menu/c-about-incremental-index.md#task_46A367B0786C4C90BFFA5D3F95FD86C0)intermédiaire.

**Syntaxe des expressions régulières**

<table> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <b>Texte</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p>N’importe quel caractère </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [caractères] </p> </td> 
   <td colname="col3"> <p> Classe de caractères : Un des caractères </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> [^chars] </p> </td> 
   <td colname="col3"> <p>Classe de caractères : Aucun caractère </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> text1|text2 </p> </td> 
   <td colname="col3"> <p> Autre solution : text1 ou text2 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Quantificateurs</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ? </p> </td> 
   <td colname="col3"> <p> 0 ou 1 du texte précédent </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> * </p> </td> 
   <td colname="col3"> <p> 0 ou N du texte précédent (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> + </p> </td> 
   <td colname="col3"> <p>1 ou N du texte précédent (N &gt; 1) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Groupement</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> (text) </p> </td> 
   <td colname="col3"> <p> Regroupement du texte, soit pour définir les bordures d'une alternative, soit pour faire des références en arrière où le troisième groupe est utilisé sur le RHS d'une RewriteRule avec $N) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Ancrages</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> ^ </p> </td> 
   <td colname="col3"> <p> Début de l’ancre de ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> <p> $ </p> </td> 
   <td colname="col3"> <p> Ancrage de fin de ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <b>Echappement</b> </p> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> </p> </td> 
   <td colname="col2"> <p>\char </p> </td> 
   <td colname="col3"> <p>Echapper à la barre particulière. Par exemple, pour spécifier les caractères ".[]()" etc. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Règles relatives aux expressions régulières**

* Un caractère ordinaire, et non l’un des caractères spéciaux décrits ci-dessous, est une expression régulière à un caractère qui se correspond.
* Une barre oblique inverse (\) suivie d’un caractère spécial est une expression régulière à un caractère qui correspond au caractère spécial lui-même. Les caractères spéciaux sont les suivants :

   * `.` (point), `*` (astérisque), `?` (point d’interrogation), `+` (signe plus), `[` (crochet gauche), `|` (barre verticale) et `\` (barre oblique inverse) sont toujours des caractères spéciaux, sauf lorsqu’ils apparaissent entre crochets.
   * `^` (circonflexe ou circonflexe) est spécial au début d&#39;une expression normale, ou lorsqu&#39;il suit immédiatement la gauche d&#39;une paire de crochets.
   * `$` (signe dollar) est spécial à la fin d&#39;une expression ordinaire.
   * `.` (point) est une expression régulière d’un caractère qui correspond à n’importe quel caractère, y compris les caractères de jeu de codes supplémentaires, à l’exception de la nouvelle ligne.
   * Une chaîne non vide de caractères entre crochets `[ ]` (crochets gauche et droit) est une expression régulière à un caractère qui correspond à un caractère, y compris les caractères de jeu de code supplémentaires, dans cette chaîne.

      Si, toutefois, le premier caractère de la chaîne est un `^` (circumflex), l’expression régulière à un caractère correspond à n’importe quel caractère, y compris les caractères de jeu de code supplémentaires, à l’exception des caractères de nouvelle ligne et des caractères restants de la chaîne.

      Cette signification particulière n’ `^` est définie que si elle se produit en premier dans la chaîne. Vous pouvez utiliser `-` (signe moins) pour indiquer une plage de caractères consécutifs, y compris des caractères de jeu de code supplémentaires. Par exemple, [0-9] équivaut à [0123456789].

      Les caractères spécifiant la plage doivent provenir du même jeu de codes. Lorsque les caractères proviennent de différents jeux de codes, l’un des caractères qui spécifient la plage est mis en correspondance. Cette signification particulière `-` est perdue si elle se produit en premier (après un premier `^`, le cas échéant) ou en dernier dans la chaîne. Le `]` (crochet droit) ne termine pas une telle chaîne lorsqu’il s’agit du premier caractère qu’elle contient, après un premier caractère `^`, le cas échéant. Par exemple, `[]a-f]` correspond à un `]` (crochet droit) ou à l’une des lettres ASCII a à f inclusif. Les quatre caractères répertoriés en tant que caractères spéciaux ci-dessus se trouvent dans une telle chaîne de caractères.

**Règles de construction d’expressions régulières à partir d’expressions régulières à un caractère**

Vous pouvez utiliser les règles suivantes pour construire des expressions régulières à partir d’expressions régulières à un caractère :

* Une expression régulière d’un caractère est une expression régulière qui correspond à l’expression régulière d’un caractère, quelle que soit la nature de celle-ci.
* Une expression régulière d’un caractère suivie d’un `*` (astérisque) est une expression régulière qui correspond à zéro ou plusieurs occurrences de l’expression régulière d’un caractère, qui peut être un caractère de jeu de codes supplémentaire. Si vous avez le choix, la chaîne la plus longue à gauche qui permet une correspondance est choisie.
* Une expression régulière à un caractère suivie d&#39;un `?` (point d&#39;interrogation) est une expression régulière qui correspond à zéro ou à une occurrence de l&#39;expression régulière à un caractère, qui peut être un caractère de jeu de codes supplémentaire. Si vous avez le choix, la chaîne la plus longue à gauche qui permet une correspondance est choisie.
* Une expression régulière d’un caractère suivie d’un signe `+` (plus) est une expression régulière qui correspond à une ou plusieurs occurrences de l’expression régulière d’un caractère, qui peut être un caractère supplémentaire de jeu de codes. Si vous avez le choix, la chaîne la plus longue à gauche qui permet une correspondance est choisie.
* Une expression régulière d’un caractère suivie d’une expression `{m}`, `{m,}`ou `{m,n}` est une  régulière qui correspond à une plage d’occurrences de l’expression régulière d’un caractère. Les valeurs de m et n doivent être des entiers non négatifs inférieurs à 256 ; `{m}` correspond exactement à m occurrences ; `{m,}` correspond au moins à m occurrences ; `{m,n}` correspond à tout nombre d’occurrences entre m et n inclus. Chaque fois qu’un choix existe, l’expression régulière correspond au plus grand nombre d’occurrences possible.
* La concaténation des expressions régulières est une expression régulière qui correspond à la concaténation des chaînes correspondant à chaque composant de l&#39;expression régulière.
* Une expression régulière encadrée entre les séquences de caractères ( et ) est une expression régulière qui correspond à ce que l’expression régulière non ornée correspond.
* Une expression régulière suivie d&#39;une `|` (canalisation verticale) suivie d&#39;une expression régulière est une expression régulière qui correspond soit à la première expression régulière (avant la canalisation verticale), soit à la seconde expression régulière (après la canalisation verticale).

Vous pouvez également contraindre une expression régulière à ne correspondre qu’à un segment initial ou final d’une ligne, ou les deux.

* Un `^` (circonflexe) au début d’une expression régulière limite cette expression régulière pour qu’elle corresponde à un segment initial d’une ligne.
* Un signe `$` (dollar) à la fin d’une expression régulière entière limite cette expression régulière pour qu’elle corresponde à un segment final d’une ligne.
* La construction de ^normal expression$ contraint l&#39;expression régulière à correspondre à la ligne entière.

Il existe des noms de classe de caractères prédéfinis que vous pouvez utiliser à la place d&#39;expressions régulières entre crochets complexes. Par exemple, un chiffre peut être représenté par l’expression régulière à un caractère [0-9] ou par l’expression régulière à un caractère de la classe de caractères [[:chiffre:]].

Les classes de caractères prédéfinies et leur signification sont les suivantes :

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Classe Caractère </p> </th> 
   <th colname="col2" class="entry"> <p>Signification </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:alnum:]] </p> </td> 
   <td colname="col2"> <p> Caractère alphabétique ou chiffre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:alpha:]] </p> </td> 
   <td colname="col2"> <p>Caractère alphabétique. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:vide:]] </p> </td> 
   <td colname="col2"> <p>Espace ou tabulation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:cntrl:]] </p> </td> 
   <td colname="col2"> <p> un code de contrôle ; caractère non imprimable. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:chiffre:]] </p> </td> 
   <td colname="col2"> <p>Chiffre. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:graph:]] </p> </td> 
   <td colname="col2"> <p> N’importe quel caractère d’impression sauf l’espace. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:lower:]] </p> </td> 
   <td colname="col2"> <p>Caractère alphabétique en minuscules. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:print:]] </p> </td> 
   <td colname="col2"> <p> Tout caractère d’impression comprenant un espace. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:punct:]] </p> </td> 
   <td colname="col2"> <p> Ponctuation. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:espace:]] </p> </td> 
   <td colname="col2"> <p> Espace blanc, tel qu’un espace, une tabulation ou une fin de ligne. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:upper:]] </p> </td> 
   <td colname="col2"> <p> Caractère alphabétique en majuscules. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:xnumer:]] </p> </td> 
   <td colname="col2"> <p> Chiffre hexadécimal, majuscule ou minuscule. </p> </td> 
  </tr> 
 </tbody> 
</table>

Deux noms de classe de caractères spéciaux correspondent à l’espace nul au début et à la fin d’un mot. En d’autres termes, elles ne correspondent pas à un caractère réel. Un mot est considéré comme toute séquence de caractères alphabétiques, de chiffres ou de traits de soulignement (_).

<table> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Classe Caractère </p> </th> 
   <th colname="col2" class="entry"> <p>Signification </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> [[:&lt;:]] </p> </td> 
   <td colname="col2"> <p> début d’un mot </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> [[:&gt;:]] </p> </td> 
   <td colname="col2"> <p>fin d’un mot </p> </td> 
  </tr> 
 </tbody> 
</table>

