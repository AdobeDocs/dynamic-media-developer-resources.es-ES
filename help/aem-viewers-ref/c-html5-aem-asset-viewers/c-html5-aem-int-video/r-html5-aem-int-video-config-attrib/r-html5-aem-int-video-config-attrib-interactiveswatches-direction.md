---
description: Atributo de configuración para el visor de vídeo interactivo.
seo-description: Atributo de configuración para el visor de vídeo interactivo.
seo-title: InteractiveSwatches.direction
solution: Experience Manager
title: InteractiveSwatches.direction
topic: Dynamic media
uuid: 08095ab5-f74b-4da6-8f8d-df377995455e
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# InteractiveSwatches.direction{#interactiveswatches-direction}

Atributo de configuración para el visor de vídeo interactivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Especifica la forma en que las muestras rellenan la vista. </p> <p>Establezca el valor en <span class="codeph"> left </span> para definir el orden de relleno de izquierda a derecha. </p> <p>Si se define a <span class="codeph"> la derecha, </span> se invierte el orden para que la vista se rellene en una dirección de derecha a izquierda y de arriba abajo. </p> <p>Cuando <span class="codeph"> auto </span> se configura, el componente aplica el modo correcto cuando la configuración regional se establece en " <span class="codeph"> ja </span>"; en caso contrario, se utiliza <span class="codeph"> left </span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`auto`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
direction=right
```

