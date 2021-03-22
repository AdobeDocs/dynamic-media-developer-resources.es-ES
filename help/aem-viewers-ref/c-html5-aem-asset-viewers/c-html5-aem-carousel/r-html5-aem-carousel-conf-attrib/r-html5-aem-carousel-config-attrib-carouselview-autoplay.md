---
description: Atributo de configuración para el visor de carrusel.
seo-description: Atributo de configuración para el visor de carrusel.
seo-title: CarouselView.autoplay
solution: Experience Manager
title: CarouselView.autoplay
uuid: 12730b17-110e-405b-97fe-e70fab89c703
feature: Dynamic Media Classic,Visores,SDK/API,Banners de carrusel
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

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

