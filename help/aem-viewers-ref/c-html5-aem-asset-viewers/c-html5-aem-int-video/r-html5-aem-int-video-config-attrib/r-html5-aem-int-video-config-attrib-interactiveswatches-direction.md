---
title: InteractiveSwatches.direction
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 6f5ec9e3-9912-4f6a-b848-de0076c4b86f
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 4%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Atributo de configuración para el visualizador de vídeo interactivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|izquierda|derecha </span> </p> </td> 
   <td colname="col2"> <p> Especifica la forma en que la vista se rellena con muestras. </p> <p>Establezca <span class="codeph"> left </span> para establecer el orden de relleno de izquierda a derecha. </p> <p>Definir en <span class="codeph"> right </span> invierte el orden para que se rellene en la dirección de derecha a izquierda, de arriba a abajo. </p> <p>Cuando se establece <span class="codeph"> auto </span>, el componente aplica el modo derecho cuando la configuración regional se establece en "<span class="codeph"> ja </span>"; de lo contrario, se utiliza <span class="codeph"> left </span>. </p> </td> 
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
