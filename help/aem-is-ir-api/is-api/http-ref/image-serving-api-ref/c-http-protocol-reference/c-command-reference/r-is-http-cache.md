---
description: Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la caché interna de Platform Server.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# cache{#cache}

Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en la caché interna de Platform Server.

`cache= *`cacheControl`*`

`cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off|validate|update</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Si solo se especifica un valor `*`cacheControl`*`, se aplica tanto a las cachés de cliente como de servidor.

La palabra clave `validate` permite actualizar las entradas de caché después de que los archivos de imagen hayan cambiado, sin tener que esperar a que la entrada de caché caduque automáticamente. El almacenamiento en caché del cliente no se ve afectado por este comando.

La palabra clave `update` puede utilizarse para forzar la actualización de entradas de caché del lado del servidor. Esto resulta útil después de cambiar los recursos que no están rastreados directamente por el mecanismo de validación de caché, como cuando se modifica un archivo de fuente sin cambiar su nombre de archivo o el id de fuente asociado.

Si se especifica en una solicitud anidada, `cache=on` habilita el almacenamiento en caché persistente del lado del servidor de la imagen generada por la solicitud anidada. Se debe tener cuidado de habilitar el almacenamiento en caché para las solicitudes anidadas solo cuando se espera que la misma solicitud anidada se llame repetidamente con exactamente los mismos parámetros.

## Propiedades {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se omite cuando la solicitud no devuelve una imagen de respuesta. *`clientControl`*se ignora cuando el catálogo de imágenes deshabilita el almacenamiento en caché del lado del cliente (si `catalog::Expiration` tiene un valor negativo).

El control de caché del lado del cliente ( `on` y `off` solamente) también está disponible para solicitudes de contenido estático en [!DNL /is/content/].

## Predeterminado {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` para solicitudes HTTP,  `cache=off` para solicitudes anidadas o incrustadas,  `cache=on` para solicitudes de contenido estático.

## Véase también {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catálogo::Caducidad](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) ,  [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
