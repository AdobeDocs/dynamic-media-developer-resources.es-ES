---
title: EmbedShare.embedsizes
description: Atributo de configuración para el visor de Video360.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 3a6c23dd-5e2c-4149-aa24-37d445128125
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---

# EmbedShare.embedsizes{#embedshare-embedsizes}

Atributo de configuración para el visor de Video360.

` [EmbedShare.|<containerId>_embedShare.]embedsizes= *`anchura`*, *`altura`*[,0|1][; *`anchura`*, *`altura`*[,0|1]]`

Especifica una lista de tamaños de incrustación para el cuadro combinado de tamaño en el cuadro de diálogo modal de uso compartido de incrustación.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
   <td colname="col2"> <p> Anchura de incrustación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> height </span> </span> </p> </td> 
   <td colname="col2"> <p>Altura de incrustación. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
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
