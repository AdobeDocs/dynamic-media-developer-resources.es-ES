---
description: Ampliar los datos de destino. Ninguna o más propiedades de destino de zoom, que pueden utilizarse junto con el cliente de visor de zoom.
solution: Experience Manager
title: Objetivos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 2%

---

# Objetivos{#targets}

Ampliar los datos de destino. Ninguna o más propiedades de destino de zoom, que pueden utilizarse junto con el cliente de visor de zoom.

El servidor devuelve el contenido de este campo como respuesta a `req=targets`, después de reemplazar los tokens de terminador de registros &#39; `??`&#39;.

Se pueden asociar hasta cuatro propiedades con cada destino de zoom:

` Target. *``*.frame= *`Numerframe`*`

` Target. *``*.rect= *`numérico,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de destino de zoom (int); los destinos de zoom deben numerarse secuencialmente y consecutivamente, empezando por 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame  </span> </span> </p> </td> 
  <td class="stentry"> <p>Número opcional de cuadro/página para establecer como objetivo un marco/página específico de un conjunto de giros o folletos; el valor predeterminado es 0 si no se especifica para el uso del visor de giros y folletos; ignorado por el visor de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> izquierda, arriba  </span> </span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxeles desde la parte superior izquierda de la imagen hasta la parte superior izquierda del rectángulo de destino del zoom (int, int); debe ser 0 o bueno. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anchura, altura  </span> </span> </p> </td> 
  <td class="stentry"> <p>Tamaño de píxel del rectángulo de destino del zoom (int, int); debe ser bueno que 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> label  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de datos de texto; puede utilizarse como etiqueta de texto para un vínculo de destino de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de datos de texto; se puede usar para pasar al cliente información específica del destino, como un valor SKU o una URL de vínculo activo. </p> </td> 
 </tr> 
</table>

Destino. *`num`*.rect es necesario para cada destino de zoom y debe especificar un rectángulo completamente dentro de la imagen. Todas las demás propiedades son opcionales.

*`label`* y  *`userData`* participar en la localización de cadenas de texto. Consulte [Localización de cadena de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en *Referencia de protocolo HTTP* para obtener más información.

En el caso de aplicaciones que impliquen clientes de espectadores de giros y folletos, los destinos de zoom deben definirse en el mismo registro de catálogo que define el conjunto de imágenes. El visor ignora cualquier definición de objetivo de zoom en los registros de catálogo de los miembros del conjunto de imágenes.

Los visores de Dynamic Media esperan destinos de zoom en las coordenadas de la imagen de resolución completa ya ajustada por los comandos de `catalog::Modifier`.

## Propiedades {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valor de ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) datos de propiedad.

## Predeterminado {#section-feab29f6575e482391086a57f547543c}

Ninguno.

## Véase también {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catálogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catálogo::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), localización de cadenas de  [texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
