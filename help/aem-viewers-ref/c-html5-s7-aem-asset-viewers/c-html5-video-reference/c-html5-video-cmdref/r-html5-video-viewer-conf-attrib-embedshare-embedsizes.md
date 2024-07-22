---
title: EmbedShare.embedsizes
description: Atributo de configuración para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 5%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Atributo de configuración para el visor de vídeo.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`ancho`*, *`alto`*[,0|1][; *`ancho`*, *`alto`*[,0|1]]`

Especifica una lista de tamaños de incrustación para el cuadro combinado de tamaño en el cuadro de diálogo modal de uso compartido de incrustación.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ancho </span> </span> </p> </td> 
   <td colname="col2"> <p> Anchura de incrustación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> altura </span> </span> </p> </td> 
   <td colname="col2"> <p>Altura de incrustación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Especifica si este elemento de la lista debe preseleccionarse en el cuadro combinado. </p> </td> 
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
