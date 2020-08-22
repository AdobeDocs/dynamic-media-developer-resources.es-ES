---
description: Datos del conjunto de imágenes. Proporciona un mecanismo para definir conjuntos ordenados de imágenes y atributos de control utilizados por los visores de Scene7.
seo-description: Datos del conjunto de imágenes. Proporciona un mecanismo para definir conjuntos ordenados de imágenes y atributos de control utilizados por los visores de Scene7.
seo-title: ImageSet
solution: Experience Manager
title: ImageSet
topic: Scene7 Image Serving - Image Rendering API
uuid: 1a34aaef-4053-4474-abb8-794331898d88
translation-type: tm+mt
source-git-commit: 515fcf8488eba7d9ca501a4182eaa73f1936488b
workflow-type: tm+mt
source-wordcount: '703'
ht-degree: 2%

---


# Conjunto de imágenes{#imageset}

Datos del conjunto de imágenes. Proporciona un mecanismo para definir conjuntos ordenados de imágenes y atributos de control utilizados por los visores de Scene7.

Un conjunto de imágenes consta de una lista de elementos ordenada y separada por comas, cada elemento consta de uno o más subelementos (ID de imagen, ID de muestra, rutas de archivos de medios, etiquetas, etc.), separados por punto y coma y/o dos puntos.

Se pueden utilizar llaves `{ }` y paréntesis `( )` para delimitar cierto contenido (como valores de color) o indicar conjuntos anidados. Las llaves o paréntesis utilizados de esta manera no deben codificarse y siempre deben aparecer como pares coincidentes; de lo contrario, se producirá un error de análisis del catálogo.

>[!NOTE]
>
>Los siguientes caracteres se utilizan como delimitadores establecidos y deben tener codificación HTTP cuando aparecen en el conjunto como parte de los valores de cadena o ID:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Consulte la documentación de los visores de servicio de imágenes para obtener más información sobre la estructura y el uso de conjuntos de imágenes.

El servidor devuelve el contenido de este campo sin modificaciones en respuesta a una `req=imageset` solicitud.

## Conjuntos estándar {#section-5ecc8ffee7224668b63f601383665564}

El servicio de imágenes admite de forma nativa las siguientes definiciones de conjuntos y el acceso a determinados visores implica el análisis, la validación y el procesamiento del conjunto en el lado del servidor. Cada tipo de conjunto se puede identificar especificando el valor correspondiente en `catalog::AssetType`.

**Conjuntos de muestras básicos**

Cada elemento de un conjunto de muestras básico consta de una referencia a un registro de imagen y una referencia independiente opcional a un registro de imagen utilizado como muestra.

| ` *`basicSwatchSet`*` | ` *``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| ` *`swatchItem`*` | ` *``*[';' *`imageIdMuestra`*]` |
| ` *`muestra`*` | ` *`swatchId`*|solidColorSpecifier` |
| ` *`imageId`*` | Referencia de imagen IS (catálogo/id) |
| ` *`swatchId`*` | Referencia de imagen IS (catálogo/id) |
| ` *`solidColorSpecifier`*` | ` '{0x' *``* [ *`rrggblabel`*]'}'` |
| ` *`rrggbb`*` | Valor de color RGB hexadecimal de 6 dígitos empaquetado para muestras de color sólido |
| ` *`label`*` | Etiqueta de texto opcional para muestras de color sólido |

**Conjuntos de muestras jerárquicos**

Cada elemento de un conjunto de muestras jerárquico puede constar de un elemento de muestra básico o una referencia a un registro de conjunto de muestras (se requieren muestras para dichos elementos).

| ` *`hierarchicalSwatchSet`*` | ` *``* &#42;[ ',' *`hierarchicalSwatchItemJerárquicoSwatchItem`* ]` |
|---|---|
| ` *`hierarchicalSwatchItem`*` | ` *``* | { *``* ';' *`swatchItembasicSwatchSetIdswatch`* }` |
| ` *`basicSwatchSetId`*` | Referencia IS (catálogo/id) a un registro de catálogo que define un conjunto de muestras básico |

**Conjuntos de giros básicos**

Un conjunto de giros básico consiste en una simple lista de los ID de imagen.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Conjuntos de giros bidimensionales**

Cada elemento de un conjunto de giros bidimensional puede constar de una imagen simple, una referencia a un conjunto de giros básico o un conjunto de giros básico en línea delimitado por llaves. Se pueden utilizar paréntesis en lugar de llaves.

| ` *`2dSpinItem`*` | ` *`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| ` *`2dSpinItem`*` | ` *``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| ` *`basicSpinSetId`*` | Referencia IS (catálogo/id) a un registro de catálogo que define un conjunto de giros básico |

**Conjuntos de páginas**

Cada elemento de un conjunto de páginas puede constar de hasta tres imágenes de página separadas por dos puntos.

| ` *`pageSet`*` | ` *``* &#42;[ , *`pageItemPageItem`* ]` |
|---|---|
| ` *`pageItem`*` | ` *``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Conjuntos de medios**

Cada elemento de un conjunto de medios puede constar de una imagen, un conjunto de muestras básico, un conjunto de muestras jerárquico, un conjunto de giros básico, un conjunto de giros bidimensional, un conjunto de páginas o un recurso de vídeo. Cada elemento de conjunto de medios también puede contener una muestra opcional y un identificador de tipo.

| ` *`mediaSet`*` | ` *`elemento`* &#42;[ , *`elemento`* ]` |
|---|---|
| ` *`elemento`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemRecutItemimageItemItemIDreserved`* ] ] ]` |
| ` *`videoItem`*` | ` *``* ; *`videoswatchId`*` |
| ` *`recutItem`*` | ` *``* ; *`recutswatchId`*` |
| ` *`imageItem`*` | ` *``* ; [ *`imageIdswatchId`* ]` |
| ` *`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| ` *`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| ` *`swatchId`*` | ID de imagen IS |
| ` *`video`*` | Ruta del archivo de vídeo o animación o identificación del catálogo estático |
| ` *`reedición`*` | Ruta del archivo XML de definición de reedición o id. de catálogo estático |
| ` *`imageId`*` | ID de imagen IS |
| ` *`setId`*` | Referencia IS a un conjunto de imágenes, giros o catálogos electrónicos |
| ` *`inlineSet`*` | Conjunto de imágenes, giros o catálogos electrónicos alineados |
| ` *`reservado`*` | Reservado para uso futuro |

**Conjuntos de vídeos**

Un conjunto de vídeos consiste en una lista sencilla de ID de vídeo en la que cada ID hace referencia a una entrada del catálogo de contenido estático.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Propiedades {#section-17c731e5c46646aa90ac21f39bb693ca}

Cadena de texto. Lista separada por comas de `catalog::Id` valores, rutas absolutas de archivos del servidor de imágenes o rutas de archivos relativas a `attribute::RootPath`. Se puede hacer referencia a la misma imagen más de una vez en el conjunto. El registro de catálogo que define puede aparecer en el conjunto en cualquier ubicación.

Este campo participa en la localización de cadenas de texto. Además de *`label`* las cadenas (parte de *`solidColorSpecifier`*), todos los campos delimitados se localizan si incluyen al menos un token de localización &#39; `^loc=…^`&#39;. Consulte la Localización [de cadena de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texto en la Referencia *del protocolo* HTTP para obtener más información.

## Predeterminado {#section-c3a60e360393478284f0f2d2da5b963b}

Ninguno.

## Véase también {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), Traducción [de ID de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) objeto, Localización [de cadena de](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) texto, Documentación de visores de servicio de imágenes
