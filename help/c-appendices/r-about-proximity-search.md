---
description: La recherche de proximité vous permet d’associer un emplacement unique à une page de votre site Web, puis de rechercher et de trier les résultats par proximité (distance) d’un emplacement donné.
seo-description: La recherche de proximité vous permet d’associer un emplacement unique à une page de votre site Web, puis de rechercher et de trier les résultats par proximité (distance) d’un emplacement donné.
seo-title: A propos de la recherche de proximité
solution: Target
title: A propos de la recherche de proximité
topic: Appendices,Site search and merchandising
uuid: 24fc9265-3400-46a7-b6e0-4de5b049a39a
translation-type: tm+mt
source-git-commit: ef818327e1cdaad79ac47575a8dfba1de3dc5c2e

---


# A propos de la recherche de proximité{#about-proximity-search}

La recherche de proximité vous permet d’associer un emplacement unique à une page de votre site Web, puis de rechercher et de trier les résultats par proximité (distance) d’un emplacement donné.

Supposons, par exemple, que vous ayez renseigné des pages de votre site Web avec des métadonnées de code postal des États-Unis telles que :

```
<meta name="zipcode" content="84057">
```

Configurez ensuite votre compte pour indexer les métadonnées de votre code postal. Dans **[!UICONTROL Settings]** > **[!UICONTROL Metadata]** > **[!UICONTROL Definitions]** > **[!UICONTROL Add New Field]**, sur la [!DNL Add Field] page, définissez les options suivantes :

* Nom du champ: `zip`
* Nom(s) de la balise(s) méta : `zipcode`
* Type de données: **[!UICONTROL Location]**
* Tri: **[!UICONTROL Ascending]**
* Unités par défaut : **[!UICONTROL Miles]**

Après avoir indexé votre site, vous effectuez la recherche suivante :

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_s=zip_proximity
```

Le jeu de résultats contient tous les documents situés à moins de 100 miles du code postal 84057, triés par ordre croissant de distance par rapport à ce code postal.

Vous pouvez également utiliser des codes de zone téléphonique pour les emplacements aux États-Unis. Vous pouvez également utiliser des paires latitude/longitude pour spécifier des emplacements dans les métadonnées de votre site et dans vos critères de recherche. Le type d’emplacement est déterminé automatiquement à partir de la forme des données fournies.

Les valeurs d’emplacement à trois chiffres (&quot;DDD&quot;, où chaque &quot;D&quot; représente un chiffre décimal compris entre 0 et 9) sont traitées comme un indicatif régional des États-Unis.

Les valeurs d’emplacement à cinq ou cinq chiffres (&quot;DDJJ&quot; ou &quot;DJJJ-DJJ&quot;) sont traitées comme un code postal américain.

Les valeurs d’emplacement sous la forme exacte de &quot;±DD.DDDD±DDD.DDDD&quot; sont traitées comme une paire latitude/longitude. La première valeur numérique signée indique la latitude et la seconde valeur numérique signée la longitude.

**Important**: Si vous spécifiez une valeur de latitude positive ou une valeur de longitude positive, ou les deux, le caractère &quot;+&quot; de l’URL doit être codé en tant que `%2b`. Dans le cas contraire, le &quot;+&quot; est interprété comme un espace et la valeur n’est pas reconnue comme un emplacement valide. Supposons, par exemple, que vous disposiez d’une valeur de latitude de +49.2394 et d’une valeur de longitude de -123.1892. La partie emplacement de l’URL, codée &quot;+&quot;, ressemblerait à ce qui suit :

```
...&sp_q_location_1=%2b49.2394-123.1892...
```

* Les valeurs de latitude positive représentent les degrés au nord de l&#39;équateur.
* Les valeurs de latitude négative représentent les degrés au sud de l&#39;équateur.
* Les valeurs de longitude positive représentent les degrés à l&#39;est du premier méridien.
* Les valeurs de longitude négatives représentent les degrés à l&#39;ouest du premier méridien.

Par exemple, la valeur &quot;+48.8577+002.2950&quot; représente 48.857 degrés au nord de l’équateur, 2.295 degrés à l’est du Premier Méridien, l’emplacement exact de la Tour Eiffel à Paris, en France. Les signes numériques et chaque chiffre sont obligatoires, même les zéros de début et de fin. Par exemple, les trois valeurs &quot;48.8577+2.2950&quot;, &quot;+48.8577+2.2950&quot; et &quot;+48.8577+02.295&quot; ne sont pas des emplacements. Il manque le signe de début sur la latitude pour la première valeur. Les deux zéros de début de longitude sont manquants pour la seconde valeur. La troisième valeur ne contient pas le zéro de fin sur la longitude. Assurez-vous d’examiner attentivement votre journal d’index pour déceler tout problème lié à l’emplacement.

Lorsque vous effectuez une recherche par proximité, un &quot;champ de sortie de proximité&quot; spécial est créé pour cette recherche. Le champ est renseigné par la distance relative entre l’emplacement spécifié dans les critères de recherche et l’emplacement associé à chaque résultat de recherche. Ce champ spécial est nommé pour le champ location-type utilisé dans les critères de recherche avec l’ajout de &quot;_close&quot; à la fin.

Dans l’exemple de recherche ci-dessus, les résultats sont triés dans l’ordre croissant de &quot;zip_close&quot;. Autrement dit, la distance entre le code postal spécifié (84057) et l’emplacement du champ &quot;zip&quot; de chaque résultat. Vous pouvez également utiliser ce &quot;champ de sortie de proximité&quot; spécial pour afficher la distance relative de chaque résultat de recherche, en kilomètres ou en milles, à l’aide de la balise de modèle `<Search-Display-Field>` Rechercher.

Voir [Rechercher des balises](../c-appendices/c-templates.md#reference_F7AA3FF602314E42842BBC740D2CA1A4)de modèle.

Vous pouvez également effectuer une recherche sans l&#39;option sp_s. Dans ce cas, les résultats sont triés par score (sp_s=0, qui est la valeur par défaut). Le score est influencé par la distance relative de chaque résultat de l’emplacement de recherche de proximité spécifié par le paramètre sp_q_location[_#] . Un nouveau paramètre cgi sp_q_max_relevant_distance[#] est ajouté afin de contrôler le calcul de pertinence appliqué aux recherches de proximité.

Voici un exemple de recherche de pertinence de proximité :

```
...&sp_q_location_1=84057&sp_x_1=zip&sp_q_max_1=100&sp_q_2=shirt&sp_x_2=title&sp_q_max_relevant_distance_2=50
```

Le jeu de résultats contient tous les documents situés à moins de 100 miles du code postal 84057 et contient le mot &quot;chemise&quot; dans le champ de titre, triés par score influencé par le score de proximité-pertinence. Un score de pertinence parfait pour la composante de proximité représenterait une distance de 0. Un score de pertinence minimal pour la composante de proximité représenterait une distance d&#39;un peu plus de 50 milles.

Vous pouvez en savoir plus sur la recherche de proximité en examinant `sp_location`, `sp_location_#`, `sp_q_min`, `sp_q_min_#`, `sp_q_max``sp_q_max_#``sp_s` , et dans la rubrique de référence Paramètres CGI de recherche.

Voir Paramètres [CGI](../c-appendices/c-cgiparameters.md#reference_DA27A8B0728246DA94994885E1353890)de recherche.

Voir [Ajout d’un nouveau champ](../c-about-settings-menu/c-about-metadata-menu.md#task_6DF188C0FC7F4831A4444CA9AFA615E5)de balise meta.
