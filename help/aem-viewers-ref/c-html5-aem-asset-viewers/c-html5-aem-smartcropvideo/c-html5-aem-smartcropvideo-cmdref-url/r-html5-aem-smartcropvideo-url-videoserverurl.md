---
description: URL para el visor de vídeo de recorte inteligente.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 945c32e0-a67b-4c27-b661-26510615d757
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '55'
ht-degree: 7%

---

# videoServerUrl{#videoserverurl}

URL para el visor de vídeo de recorte inteligente.

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
videoServerUrl=http://s7d1.scene7.com/is/content/
```
