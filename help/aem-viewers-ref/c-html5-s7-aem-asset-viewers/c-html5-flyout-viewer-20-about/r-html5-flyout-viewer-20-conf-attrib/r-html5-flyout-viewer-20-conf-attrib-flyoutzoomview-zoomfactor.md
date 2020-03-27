---
description: nulo
seo-description: nulo
seo-title: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
topic: Dynamic media
uuid: 58d49de7-4828-46ae-b2e7-eb9398e98a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`PrimaryFactorsecondaryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primarioFactor</span></span> </p> </td> 
   <td colname="col2"> <p> Especifica la ampliación de la imagen para la vista flotante, en relación con la vista principal. Debe ser un número entero o un valor de coma flotante <span class="codeph"> 1,0</span> o mayor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span></span> </p> </td> 
   <td colname="col2"> <p> Se puede especificar un factor secundario opcional al que se puede acceder haciendo clic o tocando en la vista principal cuando el resaltado está activo. Al tocar o hacer clic una segunda vez se vuelve al factor de zoom principal. Un valor de <span class="codeph"> -1</span> desactiva el factor de zoom secundario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica cómo gestiona el componente imágenes pequeñas. </p> <p>Si se establece en <span class="codeph"> 1</span> , el componente aumenta la escala de la imagen principal para que se ajuste a la vista principal. Además, aumenta la escala de la imagen de zoom para que ocupe completamente el área de la ventana flotante configurada. </p> <p>Si se establece en <span class="codeph"> 0</span> , las imágenes pequeñas se muestran con su resolución original y se muestran centradas en el área de vista principal y dentro de la ventana flotante. Puede configurar espacio en blanco adicional que aparece alrededor de la imagen con una propiedad CSS de fondo o similar de las clases CSS <span class="codeph"> s7flyoutzoomview</span> y <span class="codeph"> s7flyoutzoom</span> en la vista principal y en la ventana flotante, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-5526a5d19e7e4ee2a35b1c4816ed4202}

Opcional.

## Predeterminado {#section-a08032f0fcf041c09e63c0238a339fc9}

`3,-1,1`

## Ejemplo {#section-0338be21edd04ff1a3bed5c8319b61a4}

`zoomfactor=2,3,0`
