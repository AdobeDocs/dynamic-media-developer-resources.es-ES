---
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
title: FlyoutZoomView.preloadtiles
uuid: 8e989ca7-1ef7-4758-b6b9-c447d7647d1d
feature: Dynamic Media Classic,Visualizadores,SDK/API,Zoom en línea
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 7%

---


# FlyoutZoomView.preloadtiles{#flyoutzoomview-preloadtiles}

`[FlyoutZoomView.|<containerId>_flyout.]preloadtiles=0|1`

<table id="table_8E44EC404A1A45C59EA1EF2766613930"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Configúrelo en <span class="codeph"> 1</span> para habilitar la precarga de la imagen ampliada o en <span class="codeph"> 0</span> para cargar la imagen con zoom de forma incremental, según sea necesario. </p> <p> <p>Nota:  Si habilita esta opción, puede aumentar considerablemente el uso del ancho de banda. La imagen ampliada se carga en su totalidad, aunque el usuario no inicie una acción de zoom. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-e6310c8c4e8547689a5b48ceddb3671d}

Opcional.

## Predeterminado {#section-fcb06fd8e7e945e590094efcf9a1d510}

`0`

## Ejemplo {#section-3a188ab955c445bcb2efa3c49722c10d}

`preloadtiles=1`
