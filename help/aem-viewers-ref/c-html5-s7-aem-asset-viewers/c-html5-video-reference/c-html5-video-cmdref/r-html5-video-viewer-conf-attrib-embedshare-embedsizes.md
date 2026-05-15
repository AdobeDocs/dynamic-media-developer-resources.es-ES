---
title: EmbedShare.embeddedSize
description: Atributo de configuración para el visor de vídeo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: cf075711-1275-4eb2-8cb6-fb2609711c7a
TQID: 'https://experienceleague.adobe.com/hPMm-qxVw7yyttirfoqkgE6Nfr0EyOSRTeMHkQBofIQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 55
ht-degree: 9%

---

# EmbedShare.embeddedSize{#embedshare-embedsizes}

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
