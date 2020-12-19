---
description: Atributo de configuración para el visor de carrusel.
seo-description: Atributo de configuración para el visor de carrusel.
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
topic: Dynamic media
uuid: 12730b17-110e-405b-97fe-e70fab89c703
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# CarouselView.autoplay{#carouselview-autoplay}

Atributo de configuración para el visor de carrusel.

`[CarouselView.|<containerId>_carouselView.]autoplay=[0|1][,duration][,direction]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">[0|1][,duración][,dirección]</span> </p> </td> 
   <td colname="col2"> <p> Especifica la activación/desactivación, la duración para mostrar cada letrero en el carrusel y la dirección del bucle automático. </p> <p>Se establece en <span class="codeph"> 0</span> para desactivar el bucle automático. </p> <p>Establezca <span class="codeph"> 1</span> en bucle automático activado con la duración de la transición en segundos controlada por <span class="codeph"> duration</span>. </p> <p>La dirección del bucle automático se controla con <span class="codeph"> dirección</span>. La dirección <span class="codeph"></span> tiene el rango entre <span class="codeph"> 1</span> de derecha a izquierda y <span class="codeph"> 0</span> de izquierda a derecha. </p> </td> 
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

