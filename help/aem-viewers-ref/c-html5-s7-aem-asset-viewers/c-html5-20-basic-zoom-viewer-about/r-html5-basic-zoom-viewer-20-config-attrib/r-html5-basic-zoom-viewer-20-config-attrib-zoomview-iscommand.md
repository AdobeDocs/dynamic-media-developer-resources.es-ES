---
description: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: 0befdc0b-dd58-4aae-90e6-8c578f3b6c6f
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> iscommand</span> </span> </p> </td> 
   <td colname="col2"> <p> La cadena de comandos del servicio de imágenes que se aplica para aplicar zoom a la imagen. Si se especifica en la dirección URL, todas las incidencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben estar codificadas en HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Nota:  No se admiten los comandos de manipulación de tamaño de imagen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-50bcd15223174bb79ce08b31ea03d682}

Opcional.

## Predeterminado {#section-7564169749ff4a4996049ea1148cb2a5}

Ninguno.

## Ejemplo {#section-96e69b70365f461dae4399e49044ea2f}

Cuando se especifica en la URL del visor:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
