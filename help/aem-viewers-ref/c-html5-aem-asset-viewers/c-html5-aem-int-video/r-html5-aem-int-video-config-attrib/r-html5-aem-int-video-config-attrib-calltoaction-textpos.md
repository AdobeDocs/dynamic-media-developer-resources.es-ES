---
title: CallToAction.textpos
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: f2356eb1-2f71-49b6-bb40-6cd332e6785b
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# CallToAction.textpos{#calltoaction-textpos}

Atributo de configuración para el visualizador de vídeo interactivo.

`[CallToAction.|<containerId>_callToAction.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior|superior|izquierdo|ninguno|información sobre herramientas</span> </p> </td> 
   <td colname="col2"> <p> Especifica la posición de la etiqueta en relación con la imagen en miniatura. Es decir, la etiqueta se centra en la ubicación especificada en relación con la miniatura. </p> <p>Cuando se especifica <span class="codeph"> tooltip</span>, el texto de la etiqueta se muestra como información de objeto flotante sobre la imagen en miniatura. </p> <p>Establezca <span class="codeph"> none</span> para desactivar la etiqueta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`bottom`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
textpos=top
```
