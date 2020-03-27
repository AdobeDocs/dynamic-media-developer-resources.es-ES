---
description: nulo
seo-description: nulo
seo-title: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
topic: Dynamic media
uuid: 35c40a49-5b8e-443e-947a-5d91286ae214
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ZoomView.iscommand{#zoomview-iscommand}

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> La cadena de comandos del servicio de imágenes que se aplica para aplicar zoom a la imagen. Si se especifica en la dirección URL, todas las incidencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben estar codificadas en HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> <p> <p>Nota:  No se admiten los comandos de manipulación de tamaño de imagen. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

Ninguno.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

Cuando se especifica en la URL del visor:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
