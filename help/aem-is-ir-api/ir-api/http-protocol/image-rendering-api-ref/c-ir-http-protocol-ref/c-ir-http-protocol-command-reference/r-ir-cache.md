---
title: escondrijo
description: Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en el [!DNL Platform Server] caché.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4745197a-9f2d-4e33-8c0e-0067fbd65254
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---

# escondrijo {#cache}

Control de caché. Permite desactivar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en el [!DNL Platform Server] caché.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_CBB5DFBD48B444A4AA806B11299BC43E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> cacheControl</span> </p> </td> 
  <td class="stentry"> <p>el | desactivado | validar </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> clientControl </span> </p> </td> 
  <td class="stentry"> <p>el | desactivado </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> serverControl </span> </p></td> 
  <td class="stentry"> <p>el | desactivado </p></td> 
 </tr> 
</table>

Si solo hubiera uno *`cacheControl`* se especifica, se aplica a las memorias caché del cliente y del servidor.

El &#39; `validate`La palabra clave &#39; permite actualizar las entradas de caché del servidor después de que los archivos de textura o viñeta hayan cambiado, sin tener que esperar a que la entrada de caché caduque automáticamente. El almacenamiento en caché de clientes no se ve afectado por este comando.

Si se especifica en una solicitud anidada, `cache=on` habilita el almacenamiento en caché persistente del lado del servidor de la imagen generada por la solicitud anidada. Tenga cuidado de habilitar el almacenamiento en caché para solicitudes anidadas solo cuando se llame repetidamente a la misma solicitud anidada con los mismos parámetros.

## Propiedades {#section-0dcbd62e1122400e8c347f408f2d937e}

Puede producirse en cualquier lugar de la solicitud. Se ignora cuando la solicitud no devuelve una imagen de respuesta. La propiedad *`clientControl`* se ignora cuando el catálogo de materiales desactiva el almacenamiento en caché del lado del cliente (si `attribute::Expiration` tiene un valor negativo). La propiedad *`serverControl`* se omite si el almacenamiento en caché del servidor está deshabilitado ( `PlatformServer::cache.enable`).

## Predeterminado {#section-9034a1f4d7984c8f8dce3fc1e1803723}

`cache=on,on` Para solicitudes HTTP, `cache=off` para solicitudes anidadas/incrustadas.

## Véase también {#section-2f5853751dab49579e97418fa766bdf9}

[catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
