---
description: La cadena de comandos del servicio de imágenes que se aplica a todas las miniaturas.
seo-description: La cadena de comandos del servicio de imágenes que se aplica a todas las miniaturas.
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
topic: Dynamic media
uuid: 59a25b65-a08f-46e9-a9eb-33672e4a0cb5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# FavoritesView.iscommand{#favoritesview-iscommand}

La cadena de comandos del servicio de imágenes que se aplica a todas las miniaturas.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si se especifica en la dirección URL, todas las ocurrencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben estar codificadas en HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

Ninguno.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Cuando se especifica en la URL del visor.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
