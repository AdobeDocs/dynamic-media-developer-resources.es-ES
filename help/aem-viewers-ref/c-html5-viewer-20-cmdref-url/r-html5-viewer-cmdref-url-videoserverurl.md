---
description: Parámetro común a todos los visualizadores.
solution: Experience Manager
title: videoServerUrl
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Developer,User
exl-id: db0ce8c4-3754-4fef-9430-44ee8e5c5e80
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 5%

---

# videoServerUrl{#videoserverurl}

Parámetro común a todos los visualizadores.

>[!NOTE]
>
>Este comando no se aplica al visualizador de imágenes de vídeo.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p> La ruta raíz del servidor de vídeo. Si no se especifica ningún dominio, se aplica en su lugar el dominio desde el que se sirve la página. Se aplica la resolución de ruta de URI estándar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional. No es necesario para el software estándar como uso de servicio.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Ejemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```
