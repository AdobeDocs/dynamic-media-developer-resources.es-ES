---
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
title: FlyoutZoomView.zoomfactor
uuid: 8c4e6bf8-0238-470b-9fbe-262eb17f8f3b
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom en línea
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *``*[,[ *``*][, *`primaryFactoryFactorupscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica la ampliación de la imagen para la vista flotante, en relación con la vista principal. Debe ser un número entero o un valor de coma flotante <span class="codeph"> 1.0</span> o mayor. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Se puede especificar un factor secundario opcional al que se puede acceder tocando o haciendo clic en la vista principal cuando el resaltado está activo. Al tocar o hacer clic en una segunda vez se revierte al factor de zoom principal. Un valor de <span class="codeph"> -1</span> desactiva el factor de zoom secundario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> upscale</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica cómo gestiona el componente las imágenes pequeñas. </p> <p>Si se establece en <span class="codeph"> 1</span>, el componente aumenta la imagen principal para que se ajuste a la vista principal. Además, aumenta la imagen de zoom para que ocupe completamente el área configurada de la ventana flotante. </p> <p>Si se establece en <span class="codeph"> 0</span>, las imágenes pequeñas se muestran con la resolución original y se muestran centradas en el área de la vista principal y dentro de la ventana flotante. Puede configurar espacios en blanco adicionales alrededor de la imagen con un fondo o una propiedad CSS similar de las clases CSS <span class="codeph"> s7flyoutzoomview</span> y <span class="codeph"> s7flyoutzoom</span> en la vista principal y la ventana flotante, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
