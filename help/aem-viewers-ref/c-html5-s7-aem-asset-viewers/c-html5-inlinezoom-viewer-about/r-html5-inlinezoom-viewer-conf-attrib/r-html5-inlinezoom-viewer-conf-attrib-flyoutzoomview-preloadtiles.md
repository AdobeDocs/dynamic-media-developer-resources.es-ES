---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Establezca en <span class="codeph"> 1</span> para habilitar la carga previa de la imagen a la que se ha aplicado el zoom, o establezca en <span class="codeph"> 0</span> para cargar la imagen de zoom de forma incremental, según sea necesario. </p> <p> <p>Nota: Si activa esta opción, puede aumentar considerablemente el uso del ancho de banda. La imagen ampliada se carga en su totalidad, incluso si el usuario no inicia una acción de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
