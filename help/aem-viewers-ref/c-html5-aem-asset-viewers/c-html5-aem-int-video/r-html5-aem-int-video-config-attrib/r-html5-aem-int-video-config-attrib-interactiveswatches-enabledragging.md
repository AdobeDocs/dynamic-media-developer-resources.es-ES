---
description: Atributo de configuración para el visor de vídeo interactivo.
seo-description: Atributo de configuración para el visor de vídeo interactivo.
seo-title: InteractiveSwatches.enabledragging
solution: Experience Manager
title: InteractiveSwatches.enabledragging
topic: Dynamic media
uuid: 9a93e6b3-3441-4987-b9e6-a964dbf2247d
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---


# InteractiveSwatches.enabledragging{#interactiveswatches-enabledragging}

Atributo de configuración para el visor de vídeo interactivo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]enabledragging=0|1[, *`overdragvalue`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Activa o desactiva la capacidad de un usuario para desplazarse por las muestras con un ratón o mediante gestos táctiles. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> overdragvalue  </span> </span> </p> </td> 
   <td colname="col2"> <p> Está en el rango <span class="codeph"> 0-1 </span> y es un valor porcentual para el movimiento en la dirección incorrecta de la velocidad real. </p> <p>Si se establece en <span class="codeph"> 1 </span> se mueve con el ratón. </p> <p>Si se establece en <span class="codeph"> 0 </span> no le permite moverse en la dirección incorrecta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`1,0.5`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
enabledragging=0
```

