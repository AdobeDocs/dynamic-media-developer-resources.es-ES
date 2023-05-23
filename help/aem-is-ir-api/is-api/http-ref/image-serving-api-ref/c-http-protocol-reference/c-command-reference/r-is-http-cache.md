---
description: Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en el [!DNL Platform Server] caché.
solution: Experience Manager
title: escondrijo
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8b631836-e5a8-4a56-a09a-35bb2474cc84
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 1%

---

# escondrijo{#cache}

Control de caché. Permite deshabilitar selectivamente el almacenamiento en caché del lado del cliente (explorador, servidores proxy, sistemas de almacenamiento en caché de red) y el almacenamiento en caché en el [!DNL Platform Server] caché.

`cache= *`cacheControl`*`

`cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_70ACECAEA02F400C83B598FA13F1D00B"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> activar|desactivar|validar|actualizar</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activado|desactivado</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> activado|desactivado</span> </p></td> 
 </tr> 
</table>

Si solo hubiera uno `*`cacheControl`*` se especifica, se aplica a las memorias caché del cliente y del servidor.

El `validate` La palabra clave permite actualizar las entradas de caché después de que los archivos de imagen hayan cambiado, sin tener que esperar a que la entrada de caché caduque automáticamente. El almacenamiento en caché de clientes no se ve afectado por este comando.

El `update` La palabra clave se puede utilizar para forzar la actualización de las entradas de caché del lado del servidor. Esto resulta útil después de cambiar recursos que no se rastrean directamente mediante el mecanismo de validación de caché, como cuando se modifica un archivo de fuente sin cambiar su nombre de archivo o el ID de fuente asociado.

Si se especifica en una solicitud anidada, `cache=on` habilita el almacenamiento en caché persistente del lado del servidor de la imagen generada por la solicitud anidada. Se debe tener cuidado para habilitar el almacenamiento en caché para solicitudes anidadas solo cuando se espere que se llame repetidamente a la misma solicitud anidada con exactamente los mismos parámetros.

## Propiedades {#section-dfd0b2f92b3743fc8b9d2c35a786eb81}

Atributo de solicitud. Se aplica independientemente de la configuración de capa actual. Se ignora cuando la solicitud no devuelve una imagen de respuesta. *`clientControl`*se ignora cuando el catálogo de imágenes desactiva el almacenamiento en caché del lado del cliente (si `catalog::Expiration` tiene un valor negativo).

Control de caché del lado del cliente ( `on` y `off` solo ) también está disponible para solicitudes de contenido estático en [!DNL /is/content/].

## Predeterminado {#section-4124b2c836e2491489b9009a92fe4f22}

`cache=on,on` para solicitudes HTTP, `cache=off` para solicitudes anidadas/incrustadas, `cache=on` para solicitudes de contenido estático.

## Véase también {#section-7c2ac171fa0e4aa4a2e9955fd2d2013e}

[catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
