---
description: Control de caché. Permite desactivar de forma selectiva el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la caché interna de Platform Server.
seo-description: Control de caché. Permite desactivar de forma selectiva el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la caché interna de Platform Server.
seo-title: caché
solution: Experience Manager
title: caché
topic: Scene7 Image Serving - Image Rendering API
uuid: 8af89b67-39d5-43e5-a58d-2cd509a1e373
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# cache{#cache}

Control de caché. Permite desactivar de forma selectiva el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la caché interna de Platform Server.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>on| Desactivado| validate </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>on| Desactivado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>on| Desactivado </p></td> 
 </tr> 
</table>

Si solo se especifica un *`cacheControl`* valor, se aplica a las cachés de cliente y de servidor.

La palabra clave &#39; `validate`&#39; permite actualizar las entradas de caché del servidor después de que se hayan cambiado los archivos de viñeta o textura, sin tener que esperar a que la entrada de caché caduque automáticamente. Este comando no afecta al almacenamiento en caché del cliente.

Si se especifica en una solicitud anidada, `cache=on` habilita el almacenamiento en caché persistente del lado del servidor de la imagen generada por la solicitud anidada. Se debe tener cuidado de habilitar el almacenamiento en caché para solicitudes anidadas solo cuando se espera que la misma solicitud anidada se llame repetidamente con exactamente los mismos parámetros.

## Propiedades {#section-0dcbd62e1122400e8c347f408f2d937e}

Puede ocurrir en cualquier parte de la solicitud. Se omite cuando la solicitud no devuelve una imagen de respuesta. *`clientControl`* se ignora cuando el catálogo de materiales desactiva el almacenamiento en caché del lado del cliente (si `attribute::Expiration` tiene un valor negativo). *`serverControl`* se omite si el almacenamiento en caché del servidor está desactivado ( `PlatformServer::cache.enable`).

## Predeterminado {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` para solicitudes HTTP, `cache=off` para solicitudes anidadas o incrustadas.

## Véase también {#section-2f5853751dab49579e97418fa766bdf9}

[catálogo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
