---
description: Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la caché interna de Platform Server.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# cache{#cache}

Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la caché interna de Platform Server.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>en | off | validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl  </span> </p> </td> 
  <td class="stentry"> <p>en | off </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl  </span> </p></td> 
  <td class="stentry"> <p>en | off </p></td> 
 </tr> 
</table>

Si solo se especifica un valor *`cacheControl`* , se aplica tanto a las cachés de cliente como de servidor.

La palabra clave &#39; `validate`&#39; permite actualizar las entradas de caché del servidor después de que los archivos de viñeta o textura hayan cambiado, sin tener que esperar a que la entrada de caché caduque automáticamente. El almacenamiento en caché del cliente no se ve afectado por este comando.

Si se especifica en una solicitud anidada, `cache=on` habilita el almacenamiento en caché persistente del lado del servidor de la imagen generada por la solicitud anidada. Se debe tener cuidado de habilitar el almacenamiento en caché para las solicitudes anidadas solo cuando se espera que la misma solicitud anidada se llame repetidamente con exactamente los mismos parámetros.

## Propiedades {#section-0dcbd62e1122400e8c347f408f2d937e}

Puede ocurrir en cualquier parte de la solicitud. Se omite cuando la solicitud no devuelve una imagen de respuesta. *`clientControl`* se ignora cuando el catálogo de materiales desactiva el almacenamiento en caché del lado del cliente (si  `attribute::Expiration` tiene un valor negativo). *`serverControl`* se ignora si el almacenamiento en caché del servidor está deshabilitado (  `PlatformServer::cache.enable`).

## Predeterminado {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` para solicitudes HTTP,  `cache=off` para solicitudes anidadas/incrustadas.

## Véase también {#section-2f5853751dab49579e97418fa766bdf9}

[catálogo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
