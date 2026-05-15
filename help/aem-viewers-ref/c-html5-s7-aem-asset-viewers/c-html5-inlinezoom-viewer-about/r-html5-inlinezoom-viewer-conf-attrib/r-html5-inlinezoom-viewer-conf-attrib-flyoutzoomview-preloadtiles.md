---
title: FlyoutZoomView.preloadtiles
description: FlyoutZoomView.preloadtiles
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: f50ea45a-afd5-4e4f-967d-c45cecc5fb7b
TQID: 'https://experienceleague.adobe.com/-RpyfHGLKLQslkv-Vu3a666L0Z3aLh6I05dzSsAPPqE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 63
ht-degree: 7%

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
