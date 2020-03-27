---
description: Atributo de configuración para el visor de vídeo interactivo.
seo-description: Atributo de configuración para el visor de vídeo interactivo.
seo-title: CallToAction.direction
solution: Experience Manager
title: CallToAction.direction
topic: Dynamic media
uuid: fe182e8f-696d-4515-afdb-49964a374dae
translation-type: tm+mt
source-git-commit: 16838d04b005224fad6df215ab5bf8c25ef86fc7

---


# CallToAction.direction{#calltoaction-direction}

Atributo de configuración para el visor de vídeo interactivo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Especifica la forma en que las miniaturas rellenan la vista. </p> <p>Establezca el valor en <span class="codeph"> left </span> para definir el orden de relleno de izquierda a derecha. </p> <p>Si se define a <span class="codeph"> la derecha, </span> se invierte el orden para que la vista se rellene en una dirección de derecha a izquierda y de arriba abajo. </p> <p>Establezca en <span class="codeph"> auto </span> para que el componente aplique el modo correcto cuando la configuración regional se establezca en <span class="codeph"> "ja" </span>; en caso contrario, se utiliza <span class="codeph"> left </span> . </p> </td> 
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

