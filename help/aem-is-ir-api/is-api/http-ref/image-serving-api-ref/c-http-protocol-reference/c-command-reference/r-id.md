---
title: id
description: Versión de imagen/metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de redes de almacenamiento en caché como Akamai, cachés del explorador y cachés del servidor proxy corporativo pueden almacenar respuestas del servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3cdd27e4-14d2-42ef-aedb-9c1f7c39b4c6
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 4%

---

# id{#id}

Versión de imagen/metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de redes de almacenamiento en caché como Akamai, cachés del explorador y cachés del servidor proxy corporativo pueden almacenar respuestas del servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val </span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena de versión. </p> </td> 
 </tr> 
</table>

El servicio de imágenes incluye un mecanismo de versiones que puede ayudar a reducir la posibilidad de que una aplicación utilice una entrada de caché obsoleta. Este mecanismo implica utilizar `req=props` para obtener cadenas de identificador de versión para datos de imagen y metadatos (como datos de mapa de imagen o de destino de zoom). A continuación, la cadena del identificador de versión se agrega a las solicitudes del servicio de imágenes almacenables en caché con `id=` comando.

Cuando cambia una imagen de origen o los metadatos, también cambia el valor del ID de versión correspondiente. Inclusión de un valor de ID de versión actualizado con `id=` garantiza que ya no se pueda acceder a las entradas de caché antiguas.

En la tabla siguiente se enumeran las cadenas de identificador de versión que se deben utilizar para cada una `req=` tipo:

<table id="table_AE39BEBE18864880BBBF1C4F16785E2D"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> req= tipo</b> </th> 
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
   <td> <p> enmascarar </p> </td> 
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

`req=` Los tipos no enumerados anteriormente tienen un TTL corto ( `attribute::NonImgExpiration`) o sus respuestas no se pueden almacenar en caché en absoluto; no tiene ninguna ventaja incluir `id=` con dichas solicitudes.

## Propiedades {#section-62e973d0d5884abebbb0679f9278ae2c}

Atributo de solicitud. Opcional. El servidor siempre lo ignora.

## Predeterminado {#section-96136720c82842c89505347ec39e6024}

Ninguno.

## Ejemplo {#section-a5fb871e0ec8485c91c4fca78895d17f}

Consulte la descripción de [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) por ejemplo, uso.

## Véase también {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) , [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3), [catalog::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a), [attribute::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
