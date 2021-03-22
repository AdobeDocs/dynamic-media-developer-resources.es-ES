---
description: URL para el visualizador de vídeo interactivo.
seo-description: URL para el visualizador de vídeo interactivo.
seo-title: navegación
solution: Experience Manager
title: navegación
uuid: eecc7458-153c-4f36-b29e-97451f275c0c
feature: Dynamic Media Classic,Visualizadores,SDK/API,Vídeos interactivos
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '73'
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

