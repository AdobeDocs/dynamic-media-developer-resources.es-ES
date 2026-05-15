---
title: FlyoutZoomView.zoomfactor
description: FlyoutZoomView.zoomfactor
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 2a9d4450-a1a0-471c-86bf-105d516b0bd7
TQID: 'https://experienceleague.adobe.com/9J-cksIEU-w-jRL4PN0dklGMWCpu0c74oSMdw-AX2IQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 1%

---

# FlyoutZoomView.zoomfactor{#flyoutzoomview-zoomfactor}

` [FlyoutZoomView.|<containerId>_flyout.]zoomfactor= *`primaryFactor`*[,[ *`secondaryFactor`*][, *`upscale`*]]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> primaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica el aumento de la imagen para la vista flotante, en relación con la vista principal. Debe ser un número entero o un valor de coma flotante <span class="codeph"> 1.0</span> o superior. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> secondaryFactor</span> </span> </p> </td> 
   <td colname="col2"> <p> Se puede especificar un factor secundario opcional al que se puede acceder haciendo clic o pulsando en la vista principal cuando el resaltado está activo. Tocar o hacer clic por segunda vez recupera el factor de zoom principal. Un valor de <span class="codeph"> -1</span> deshabilita el factor de zoom secundario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> de lujo</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica cómo gestiona el componente las imágenes pequeñas. </p> <p>Si se establece en <span class="codeph"> 1</span>, el componente aumenta la escala de la imagen principal para que se ajuste a la vista principal. Además, aumenta la escala de la imagen de zoom para que llene completamente el área de ventana flotante configurada. </p> <p>Si se establece en <span class="codeph"> 0</span>, las imágenes pequeñas se mostrarán con su resolución original y se mostrarán centradas en el área de vista principal y dentro de la ventana flotante. Puede configurar espacio en blanco adicional alrededor de la imagen con un fondo o una propiedad CSS similar de las clases CSS <span class="codeph"> s7flyoutzoomview</span> y <span class="codeph"> s7flyoutzoom</span> en la vista principal y la ventana flotante, respectivamente. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`3,-1,1`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`zoomfactor=2,3,0`
