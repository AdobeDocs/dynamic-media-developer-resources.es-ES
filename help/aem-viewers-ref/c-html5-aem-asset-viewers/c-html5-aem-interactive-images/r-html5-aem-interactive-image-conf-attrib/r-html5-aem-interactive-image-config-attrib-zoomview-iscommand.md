---
title: ZoomView.iscommand
description: La cadena de comando del servicio de imágenes que se aplica a la imagen de zoom.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 1c24973e-1daf-4d9d-b97c-fb6a18f506ed
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 6%

---

# ZoomView.iscommand{#zoomview-iscommand}

La cadena de comando del servicio de imágenes que se aplica a la imagen de zoom.

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> desmandar</span></span> </p> </td> 
   <td colname="col2"> <p> Si se especifica en la dirección URL, todas las apariciones de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> debe tener la codificación HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

Ninguno.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

Cuando se especifica en la dirección URL del visor:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
