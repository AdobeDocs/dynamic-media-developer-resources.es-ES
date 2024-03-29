---
description: Datos de destino de zoom. No hay ninguna o más propiedades de destinos de zoom que se puedan usar junto con el cliente del visor de zoom.
solution: Experience Manager
title: Objetivos
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 2%

---

# Objetivos{#targets}

Datos de destino de zoom. No hay ninguna o más propiedades de destinos de zoom que se puedan usar junto con el cliente del visor de zoom.

El servidor devuelve el contenido de este campo en respuesta a `req=targets`, después de reemplazar &#39; `??`&#39; tokens de terminador de registros.

Se pueden asociar hasta cuatro propiedades a cada destino de zoom:

` Target. *`num`*.frame= *`armazón`*`

` Target. *`num`*.rect= *`izquierda, superior, anchura, altura`*`

` Target. *`num`*.label= *`etiqueta`*`

` Target. *`num`*.userData= *`userData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de destino de zoom (int); los destinos de zoom deben numerarse secuencial y consecutivamente, empezando por 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> armazón </span> </span> </p> </td> 
  <td class="stentry"> <p>Número de página/marco opcional para seleccionar un fotograma o una página específicos de un conjunto de giros o folletos; el valor predeterminado es 0 si no se especifica para el uso del visor de giros y folletos; el visor de zoom lo ignora. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> izquierda, arriba </span> </span> </p> </td> 
  <td class="stentry"> <p>Desplazamiento de píxel desde la parte superior izquierda de la imagen hasta la parte superior izquierda del rectángulo de destino de zoom (int, int); debe ser 0 o bueno. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> anchura, altura </span> </span> </p> </td> 
  <td class="stentry"> <p>Tamaño de píxel del rectángulo de destino de zoom (int, int); debe ser bueno que 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> etiqueta </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de datos de texto; se puede utilizar como etiqueta de texto para un vínculo de destino de zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span> </span> </p> </td> 
  <td class="stentry"> <p>Valor de datos de texto; se puede utilizar para pasar información específica de destinatario al cliente, como un valor SKU o una URL de vínculo activo. </p> </td> 
 </tr> 
</table>

Destino. *`num`*.rect es necesario para cada destino de zoom y debe especificar un rectángulo completamente dentro de la imagen. Todas las demás propiedades son opcionales.

*`label`* y *`userData`* participar en la localización de cadenas de texto. Consulte [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en el *Referencia de protocolo HTTP* para obtener más información.

Para las aplicaciones que impliquen clientes de visualizador de folletos y giros, los destinos de zoom deben definirse en el mismo registro de catálogo que define el conjunto de imágenes. El visor ignora cualquier definición de destinos de zoom en los registros de catálogo de los miembros del conjunto de imágenes.

Los visores de Dynamic Media esperan destinos de zoom en las coordenadas de la imagen de resolución completa ya ajustada por los comandos de `catalog::Modifier`.

## Propiedades {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Datos de propiedad](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) valor.

## Predeterminado {#section-feab29f6575e482391086a57f547543c}

Ninguno.

## Véase también {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalog::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalog::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
