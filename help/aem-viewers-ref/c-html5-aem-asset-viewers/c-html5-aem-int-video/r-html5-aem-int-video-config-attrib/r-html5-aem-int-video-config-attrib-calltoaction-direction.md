---
title: CallToAction.direction
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 2cfeeba0-3230-481c-857a-bed3fedc836c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 3%

---

# CallToAction.direction{#calltoaction-direction}

Atributo de configuración para el visualizador de vídeo interactivo.

`[CallToAction.|<containerId>_callToAction.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right </span> </p> </td> 
   <td colname="col2"> <p> Especifica la forma en que la vista se rellena con miniaturas. </p> <p>Configure como. <span class="codeph"> left </span> para establecer el orden de relleno de izquierda a derecha. </p> <p>Configure como. <span class="codeph"> derecha </span> invierte el orden para que la vista se rellene en una dirección de derecha a izquierda, de arriba a abajo. </p> <p>Configure como. <span class="codeph"> auto </span> para que el componente aplique el modo correcto cuando la configuración regional esté configurada como <span class="codeph"> "ja" </span>; de lo contrario, <span class="codeph"> left </span> se utiliza. </p> </td> 
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
