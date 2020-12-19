---
description: nulo
seo-description: nulo
seo-title: CarouselView.maxloadradius
solution: Experience Manager
title: CarouselView.maxloadradius
topic: Dynamic media
uuid: 0dcebbce-f449-4f5f-acbc-02960e1dbdba
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 9%

---


# CarouselView.maxloadradius{#carouselview-maxloadradius}

` [CarouselView.|<containerId>_carouselView.]maxloadradius=-1|0| *`preloadnbr`*`

<table id="table_B3B03B00DCF0466DB332E851F4DDF610"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> -1|0|<span class="varname"> preloadnbr</span></span> </p> </td> 
   <td> <p>Especifica el comportamiento de precarga del componente. </p> <p>Cuando se establece en <span class="codeph"> -1</span>, el componente carga previamente todos los fotogramas de carrusel cuando se encuentra en estado inactivo. </p> <p>Cuando se establece en <span class="codeph"> 0</span>, el componente carga solo el fotograma que está visible actualmente, anterior y siguiente. </p> <p><span class="codeph"><span class="varname"> </span></span>precarga define cuántos marcos invisibles alrededor del marco mostrado actualmente se cargan previamente cuando se encuentra en estado inactivo. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

`maxloadradius=0`
