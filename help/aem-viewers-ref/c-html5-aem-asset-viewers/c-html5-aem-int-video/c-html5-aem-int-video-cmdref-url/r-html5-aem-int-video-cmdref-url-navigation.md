---
description: URL para el visualizador de vídeo interactivo.
solution: Experience Manager
title: navegación
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 9852e723-fd1f-4ade-921b-cfb92bf9f2ad
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 12%

---

# navegación{#navigation}

URL para el visualizador de vídeo interactivo.

` navigation= *`archivo`*`

El visor admite la navegación por capítulos de vídeo mediante archivos WebVTT alojados. No se admiten los operadores de posición de señal.

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file</span> </span> </p> </td> 
   <td colname="col2"> <p> Especifica una dirección URL o ruta al contenido de navegación de WebVTT. El servicio de imágenes debe alojar el archivo WebVTT. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

Ninguno.

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
navigation=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.navigation.vtt,1
```
