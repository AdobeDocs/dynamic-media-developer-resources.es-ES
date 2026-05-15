---
title: CarouselView.autoplay
description: Atributo de configuración para el visualizador de carrusel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
TQID: 'https://experienceleague.adobe.com/LEeJUVIHLhplymrvp9IdNUWcfJz-Tl0kLffkik1GvkY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 3%

---

# CarouselView.autoplay{#carouselview-autoplay}

Atributo de configuración para el visualizador de carrusel.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duración][,dirección]</span> </p> </td> 
   <td colname="col2"> <p> Especifica la activación o desactivación, la duración para mostrar cada titular en el carrusel y la dirección del bucle automático. </p> <p>Establezca en <span class="codeph"> 0</span> para desactivar el bucle automático. </p> <p>Establezca <span class="codeph"> 1</span> en el bucle automático con la duración de la transición en segundos controlada por <span class="codeph"> duration</span>. </p> <p>La dirección del bucle automático se controla con <span class="codeph"> direction</span>. La dirección <span class="codeph"></span> tiene el intervalo entre <span class="codeph"> 1</span> de derecha a izquierda y <span class="codeph"> 0</span> de izquierda a derecha. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,9`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
autoplay=1,2,1
```
