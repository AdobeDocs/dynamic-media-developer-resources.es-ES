---
description: Zoom de datos de destinatario. Ninguna o más propiedades de destinatario de zoom, que se pueden usar junto con el cliente de visor de zoom.
seo-description: Zoom de datos de destinatario. Ninguna o más propiedades de destinatario de zoom, que se pueden usar junto con el cliente de visor de zoom.
seo-title: Objetivos
solution: Experience Manager
title: Objetivos
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Objetivos{#targets}

Zoom de datos de destinatario. Ninguna o más propiedades de destinatario de zoom, que se pueden usar junto con el cliente de visor de zoom.

El servidor devuelve el contenido de este campo en respuesta a `req=targets`, después de reemplazar los tokens de terminación de registros &#39; `??`&#39;.

Se pueden asociar hasta cuatro propiedades con cada destinatario de zoom:

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numérico,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de destinatario de zoom (int); los destinatarios de zoom deben numerarse secuencialmente y consecutivamente, comenzando por 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de página o marco opcional para dirigir un marco o una página específicos de un conjunto de giros o folletos; el valor predeterminado es 0 si no se especifica para el uso del visor de folletos y giros; omitido por el visor de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> izquierda, arriba  </span> </span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la parte superior izquierda de la imagen hasta la parte superior izquierda del rectángulo del destinatario de zoom (int, int); debe ser 0 o bueno. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anchura, altura  </span> </span> </p> </td> 
  <td class="stentry"> <p>Tamaño de píxel del rectángulo del destinatario de zoom (int, int); debe ser bueno a 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de datos de texto; puede utilizarse como etiqueta de texto para un vínculo de destinatario de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de datos de texto; se puede utilizar para pasar información específica del destinatario al cliente, como un valor de SKU o una dirección URL de enlace en caliente. </p> </td> 
 </tr> 
</table>

Destino. *`num`*.rect es necesario para cada destinatario de zoom y debe especificar un rectángulo completo dentro de la imagen. Todas las demás propiedades son opcionales.

*`label`* y  *`userData`* participar en la localización de cadenas de texto. Consulte [Localización de cadena de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en la *Referencia del protocolo HTTP* para obtener más información.

En el caso de las aplicaciones que involucran los clientes del visor de giros y folletos, los destinatarios de zoom deben definirse en el mismo registro de catálogo que define el conjunto de imágenes. El visor ignora todas las definiciones de destinatario de zoom de los registros de catálogo de los miembros del conjunto de imágenes.

Los visores de Scene7 esperan destinatarios de zoom en las coordenadas de la imagen de resolución completa ya ajustadas por los comandos de `catalog::Modifier`.

## Propiedades {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valor de ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) datos de propiedad.

## Predeterminado {#section-feab29f6575e482391086a57f547543c}

Ninguno.

## Véase también {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catálogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catálogo::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localización de cadena  [de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
