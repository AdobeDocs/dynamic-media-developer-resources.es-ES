---
description: Versión de imagen y metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de las redes de almacenamiento en caché como Akamai, las memorias caché del navegador y las memorias caché del servidor proxy corporativo pueden almacenar respuestas de servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.
seo-description: Versión de imagen y metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de las redes de almacenamiento en caché como Akamai, las memorias caché del navegador y las memorias caché del servidor proxy corporativo pueden almacenar respuestas de servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.
seo-title: id
solution: Experience Manager
title: id
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# id{#id}

Versión de imagen y metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de las redes de almacenamiento en caché como Akamai, las memorias caché del navegador y las memorias caché del servidor proxy corporativo pueden almacenar respuestas de servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena de versión. </p> </td> 
 </tr> 
</table>

El servicio de imágenes incluye un mecanismo de versiones que puede ayudar a reducir la posibilidad de que una aplicación utilice una entrada de caché obsoleta. Este mecanismo implica el uso de `req=props` para obtener cadenas de identificador de versión para datos de imagen y metadatos (como mapa de imagen o datos de destinatario de zoom). La cadena del identificador de versión se agrega a las solicitudes de servicio de imágenes almacenables en caché con el comando `id=`.

Cuando una imagen o metadatos de origen cambian, también cambiará el valor de ID de versión correspondiente. Si se incluye un valor de ID de versión actualizado con el comando `id=`, se garantiza que ya no se tendrá acceso a las entradas de caché antiguas.

La siguiente tabla lista las cadenas del identificador de versión que se utilizarán para cada tipo `req=`:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= type</b> </th> 
   <th class="entry"> <b> identificador de versión de req=props</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> img </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> mapa </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> máscara </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> objetivo </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> tmb </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> userdata </p> </td> 
   <td> <p> metadata.version </p> </td> 
  </tr> 
  <tr> 
   <td> <p> xmp </p> </td> 
   <td> <p> image.version </p> </td> 
  </tr> 
 </tbody> 
</table>

`req=` los tipos no enumerados anteriormente o bien tienen un TTL corto (  `attribute::NonImgExpiration`) o bien sus respuestas no se pueden obtener en absoluto; no hay ninguna ventaja en incluir  `id=` estas solicitudes.

## Propiedades {#section-62e973d0d5884abebbb0679f9278ae2c}

Solicitar atributo. Opcional. Siempre ignorado por el servidor.

## Predeterminado {#section-96136720c82842c89505347ec39e6024}

Ninguno.

## Ejemplo {#section-a5fb871e0ec8485c91c4fca78895d17f}

Consulte la descripción de [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) por ejemplo: uso.

## Véase también {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catálogo::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [atributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
