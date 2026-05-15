---
title: InteractiveSwatches.textpos
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 875d36cc-7372-454e-9a04-32492a2e558e
TQID: 'https://experienceleague.adobe.com/d5HByES5qBKLBHea8F0JMyjhcPfcrAlpS0F5mzWYaYg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 74
ht-degree: 4%

---

# InteractiveSwatches.textpos{#interactiveswatches-textpos}

Atributo de configuración para el visualizador de vídeo interactivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]textpos=bottom|top|left|right|none|tooltip`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> inferior|superior|izquierdo|ninguno|información sobre herramientas</span> </p> </td> 
   <td colname="col2"> <p> Especifica la posición de la etiqueta en relación con la imagen de la muestra. Es decir, la etiqueta se centra en la ubicación especificada en relación con la miniatura. </p> <p>Cuando se especifica <span class="codeph"> tooltip</span>, el texto de la etiqueta se muestra como información de objeto flotante sobre la imagen en miniatura. </p> <p>Establezca <span class="codeph"> none</span> para desactivar la etiqueta. </p> </td> 
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
