---
title: EmbedShare.embedsizes
description: Atributo de configuración para el visor de vídeo de recorte inteligente.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
source-git-commit: b6ebc938f55117c4144ff921bed7f8742cf3a8a7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Atributo de configuración para el visor de vídeo de recorte inteligente.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`width`*, *`height`*[,0|1][; *`width`*, *`height`*[,0|1]]`

Especifica una lista de tamaños incrustados para el cuadro combinado de tamaño en el cuadro de diálogo modal para compartir incrustación.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Ancho incrustado. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Incrustar altura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica si este elemento de lista debe preseleccionarse inicialmente en el cuadro combinado. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`1280,960;640,480;320,240`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
embedsizes=800,600;640,480,1
```
