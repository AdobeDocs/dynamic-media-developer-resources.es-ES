---
description: La cadena de comando del Servidor de imágenes que se aplica a la imagen de zoom.
seo-description: La cadena de comando del Servidor de imágenes que se aplica a la imagen de zoom.
seo-title: ZoomView.iscommand
solution: Experience Manager
title: ZoomView.iscommand
uuid: 13dc11ed-52a4-45ae-bfae-ca034c8a3c87
feature: Dynamic Media Classic,Visualizadores,SDK/API,Imágenes interactivas
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---


# ZoomView.iscommand{#zoomview-iscommand}

La cadena de comando del Servidor de imágenes que se aplica a la imagen de zoom.

` [ZoomView.|<containerId>_zoomView.]iscommand= *`isCommand`*`

<table id="table_06B5F795889E402FB6BCEA4D882E1422"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> iscommand</span></span> </p> </td> 
   <td colname="col2"> <p> Si se especifica en la dirección URL, todas las ocurrencias de <span class="codeph"> &amp;</span> y <span class="codeph"> =</span> deben codificarse con HTTP como <span class="codeph"> %26</span> y <span class="codeph"> %3D</span>, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

Ninguno.

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

Cuando se especifique en la dirección URL del visor:

`iscommand=op_sharpen%3d1%26op_colorize%3d0xff0000`

Cuando se especifica en los datos de configuración:

`iscommand=op_sharpen=1&op_colorize=0xff0000`
