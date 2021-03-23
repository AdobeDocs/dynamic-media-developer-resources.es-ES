---
description: Comando URL para el visualizador de Video360.
seo-description: Comando URL para el visualizador de Video360.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
uuid: b6fa3fc3-9182-4d05-a735-e4cc0e58c3e4
feature: Dynamic Media Classic, visores, SDK/API, vídeo VR 360
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 5%

---


# videoServerUrl{#videoserverurl}

Comando URL para el visualizador de Video360.

` videoServerUrl= *`videoRootPath`*`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> La ruta raíz del servidor de vídeo. Si no se especifica ningún dominio, se aplica en su lugar el dominio desde el que se sirve la página. Se aplica la resolución de ruta de URI estándar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-f42369774e2740dcb399626a0e4e930e}

Opcional. No es necesario para el uso estándar de SaaS.

## Predeterminado {#section-d016470e92a74f98a18c4ab3489410a5}

`/is/content/`

## Ejemplo {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
videoServerUrl=http://s7d9.scene7.com/is/content/
```

