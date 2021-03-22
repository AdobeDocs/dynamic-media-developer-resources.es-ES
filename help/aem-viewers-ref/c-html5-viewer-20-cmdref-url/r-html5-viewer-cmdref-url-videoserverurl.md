---
description: Parámetro común a todos los visualizadores.
seo-description: Parámetro común a todos los visualizadores.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
uuid: ef9870f9-599b-449d-b713-66abafb80311
feature: Dynamic Media Classic,Visualizadores,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '78'
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

