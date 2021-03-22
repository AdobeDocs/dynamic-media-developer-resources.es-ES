---
description: Versión de imagen/metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de las redes de almacenamiento en caché como Akamai, las cachés de los navegadores y las cachés de los servidores proxy corporativos pueden almacenar respuestas de servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.
seo-description: Versión de imagen/metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de las redes de almacenamiento en caché como Akamai, las cachés de los navegadores y las cachés de los servidores proxy corporativos pueden almacenar respuestas de servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.
seo-title: id
solution: Experience Manager
title: id
uuid: 3d526326-c8fa-4aef-95a9-93ccacf08f73
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 4%

---


# id{#id}

Versión de imagen/metadatos. Cuando se trabaja con contenido que cambia con frecuencia, los servidores de las redes de almacenamiento en caché como Akamai, las cachés de los navegadores y las cachés de los servidores proxy corporativos pueden almacenar respuestas de servicio de imágenes que pueden estar desactualizadas durante períodos de tiempo.

` id= *`val`*`

<table id="simpletable_3A6EBDA15B004636804E1ACEF952479A"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> val  </span> </span> </p> </td> 
  <td class="stentry"> <p>Cadena de versión. </p> </td> 
 </tr> 
</table>

El servicio de imágenes incluye un mecanismo de versiones que puede ayudar a reducir las posibilidades de que una aplicación utilice una entrada de caché obsoleta. Este mecanismo implica el uso de `req=props` para obtener cadenas de identificador de versión para datos de imágenes y metadatos (como mapa de imágenes o datos de destino de zoom). A continuación, la cadena del identificador de versión se agrega a las solicitudes almacenables de imágenes almacenables en caché con el comando `id=`.

Cuando una imagen de origen o metadatos cambian, también cambia el valor de id de versión correspondiente. Al incluir un valor de id de versión actualizado con el comando `id=`, se garantiza que ya no se tendrá acceso a las entradas de caché antiguas.

La siguiente tabla enumera las cadenas del identificador de versión que se utilizarán para cada tipo `req=` :

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
   <td> <p> mask </p> </td> 
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

`req=` los tipos no enumerados anteriormente tienen un breve TTL (  `attribute::NonImgExpiration`) o sus respuestas no pueden almacenarse en caché en absoluto; no hay ninguna ventaja en incluir  `id=` esas solicitudes.

## Propiedades {#section-62e973d0d5884abebbb0679f9278ae2c}

Atributo de solicitud. Opcional. El servidor siempre ignora.

## Predeterminado {#section-96136720c82842c89505347ec39e6024}

Ninguno.

## Ejemplo {#section-a5fb871e0ec8485c91c4fca78895d17f}

Consulte la descripción de [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3) para ver ejemplos de uso.

## Véase también {#section-6b4befb47202415195a68516f60e9988}

[req=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76) ,  [rect=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rect.md#reference-520b90d30b4c4b4692a723e4df6adaf3),  [catálogo::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a),  [atributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
