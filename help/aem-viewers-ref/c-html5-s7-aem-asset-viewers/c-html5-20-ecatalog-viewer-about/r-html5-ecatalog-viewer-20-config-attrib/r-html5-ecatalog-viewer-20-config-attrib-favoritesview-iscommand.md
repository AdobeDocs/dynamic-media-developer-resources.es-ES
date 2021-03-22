---
description: La cadena de comando del Servidor de imágenes que se aplica a todas las miniaturas.
seo-description: La cadena de comando del Servidor de imágenes que se aplica a todas las miniaturas.
seo-title: FavoritesView.iscommand
solution: Experience Manager
title: FavoritesView.iscommand
uuid: 59a25b65-a08f-46e9-a9eb-33672e4a0cb5
feature: Dynamic Media Classic,Visualizadores,SDK/API,Catálogo electrónico
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

---


# FavoritesView.iscommand{#favoritesview-iscommand}

La cadena de comando del Servidor de imágenes que se aplica a todas las miniaturas.

` [FavoritesView.|<containerId>_favoritesView.]iscommand= *`isCommand`*`

<table id="table_2B109D2F91E64B5382B31921C3780FA5"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> isCommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si se especifica en la dirección URL, todas las ocurrencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben codificarse con HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

Ninguno.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

Cuando se especifique en la dirección URL del visor.

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifique en los datos de configuración.

`iscommand=op_sharpen=1&op_colorize=0xff0000`
