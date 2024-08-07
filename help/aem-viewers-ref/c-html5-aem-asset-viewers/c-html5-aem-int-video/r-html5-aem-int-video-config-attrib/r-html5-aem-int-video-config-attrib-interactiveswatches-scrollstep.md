---
title: InteractiveSwatches.scrollstep
description: Atributo de configuración para el visualizador de vídeo interactivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 15bf7af8-428b-4c1c-b7ad-004563347d7c
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 4%

---

# InteractiveSwatches.scrollstep{#interactiveswatches-scrollstep}

Atributo de configuración para el visualizador de vídeo interactivo.

` [InteractiveSwatches.|<containerId>_interactiveSwatches.]scrollstep= *`paso`*`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> paso</span></span> </p> </td> 
   <td colname="col2"> <p>Especifica el número de muestras que se desplazarán para cada toque el botón de desplazamiento correspondiente. </p> <p>Si el valor especificado es mayor que el número de muestras interactivas visibles, cada toque solo se desplazará según el número de muestras visibles para evitar la omisión de cualquier muestra. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-1e637b22e8a44d759d588e47576891e6}

Opcional.

## Predeterminado {#section-71fb773f814649b2885aefee68073641}

`3`

## Ejemplo {#section-bce98c31f08a4a0ab262fab7f95ba020}

```
scrollstep=1
```
