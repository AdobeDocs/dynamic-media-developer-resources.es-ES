---
description: Parámetro común a todos los visores.
seo-description: Parámetro común a todos los visores.
seo-title: videoServerUrl
solution: Experience Manager
title: videoServerUrl
topic: Dynamic media
uuid: ef9870f9-599b-449d-b713-66abafb80311
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# videoServerUrl{#videoserverurl}

Parámetro común a todos los visores.

>[!NOTE]
>
>Este comando no se aplica al visor de imágenes de vídeo.

` videoServerUrl= *`videoRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> videoRootPath</span></span> </p> </td> 
   <td colname="col2"> <p> Ruta de acceso raíz del servidor de vídeo. Si no se especifica ningún dominio, se aplica en su lugar el dominio desde el que se proporciona la página. Se aplica la resolución de ruta URI estándar. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Propiedades {#section-10ee45d637134e0fbcd943c62578cb78}

Opcional. No es necesario para el software estándar como uso del servicio.

## Predeterminado {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Ejemplo {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
videoServerUrl=http://s7d1.scene7.com/is/content/
```

