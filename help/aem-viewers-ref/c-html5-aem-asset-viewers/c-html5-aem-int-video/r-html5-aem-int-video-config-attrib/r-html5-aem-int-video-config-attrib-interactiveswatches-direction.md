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
ht-degree: 5%

---

# InteractiveSwatches.direction{#interactiveswatches-direction}

Atributo de configuración para el visualizador de vídeo interactivo.

`[InteractiveSwatches.|<containerId>_interactiveSwatches.]direction=auto|left|right`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> auto|left|right  </span> </p> </td> 
   <td colname="col2"> <p> Especifica la forma en que las muestras rellenan la vista. </p> <p>Configúrelo en <span class="codeph"> izquierda </span> para definir el orden de relleno de izquierda a derecha. </p> <p>Si se establece en <span class="codeph"> derecha </span> , se invierte el orden de modo que la vista se rellene en una dirección de derecha a izquierda, de arriba abajo. </p> <p>Cuando <span class="codeph"> auto </span> está configurado, el componente aplica el modo correcto cuando la configuración regional está configurada en " <span class="codeph"> ja </span>"; de lo contrario, se utiliza <span class="codeph"> izquierda </span>. </p> </td> 
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
