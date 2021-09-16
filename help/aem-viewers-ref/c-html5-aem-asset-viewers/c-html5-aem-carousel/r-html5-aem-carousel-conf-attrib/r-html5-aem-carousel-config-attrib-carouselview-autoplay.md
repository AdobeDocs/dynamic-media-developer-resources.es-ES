---
title: CarouselView.autoplay
description: Atributo de configuración para el visor de carrusel.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: 43b5c169-0ef6-4a12-a777-d36c1a8d1771
source-git-commit: 5a7af31d6788ded908a5e1630a3b1b0723e6fb4b
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 5%

---

# CarouselView.autoplay{#carouselview-autoplay}

Atributo de configuración para el visor de carrusel.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duración][,dirección]</span> </p> </td> 
   <td colname="col2"> <p> Especifica la activación o desactivación, la duración para mostrar cada banner en el carrusel y la dirección del bucle automático. </p> <p>Establézcalo en <span class="codeph"> 0</span> para desactivar el bucle automático. </p> <p>Establezca <span class="codeph"> 1</span> en bucle automático activado con duración de transición en segundos controlada por <span class="codeph"> duración</span>. </p> <p>La dirección del bucle automático se controla con <span class="codeph"> dirección</span>. La dirección <span class="codeph"></span> tiene el rango entre <span class="codeph"> 1</span> de derecha a izquierda y <span class="codeph"> 0</span> de izquierda a derecha. </p> </td> 
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
