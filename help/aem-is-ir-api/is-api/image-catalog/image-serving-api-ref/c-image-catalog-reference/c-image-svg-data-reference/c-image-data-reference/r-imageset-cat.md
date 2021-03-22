---
description: Datos del conjunto de imágenes. Proporciona un mecanismo para definir conjuntos ordenados de imágenes y atributos de control que utilizan los visualizadores de Dynamic Media.
solution: Experience Manager
title: ImageSet
feature: Dynamic Media Classic,SDK/API,Conjuntos de imágenes
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 2%

---


# Conjunto de imágenes{#imageset}

Datos del conjunto de imágenes. Proporciona un mecanismo para definir conjuntos ordenados de imágenes y atributos de control que utilizan los visualizadores de Dynamic Media.

Un conjunto de imágenes consta de una lista de elementos ordenada y separada por comas, cada elemento consta de uno o más subelementos (id de imagen, id de muestra, rutas de archivos multimedia, etiquetas, etc.) separados por punto y coma o dos puntos.

Las llaves `{ }` y los paréntesis `( )` pueden utilizarse para delimitar cierto contenido (como valores de color) o indicar conjuntos anidados. Las llaves o paréntesis utilizados de esta forma no deben codificarse y siempre deben aparecer como pares coincidentes; de lo contrario, se producirá un error de análisis del catálogo.

>[!NOTE]
>
>Los siguientes caracteres se utilizan como delimitadores establecidos y deben tener codificación HTTP cuando aparecen en el conjunto como parte de valores de id o de cadena:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`



Consulte la documentación de Visualizadores de servicio de imágenes para obtener más información sobre la estructura y el uso de los conjuntos de imágenes.

El servidor devuelve el contenido de este campo sin modificación en respuesta a una solicitud `req=imageset`.

## Conjuntos estándar {#section-5ecc8ffee7224668b63f601383665564}

El servicio de imágenes admite de forma nativa las siguientes definiciones de conjuntos, y el acceso a ellas implica el análisis, la validación y el procesamiento del conjunto en el servidor. Cada tipo de conjunto se puede identificar especificando el valor correspondiente en `catalog::AssetType`.

**Conjuntos de muestras básicos**

Cada elemento de un conjunto de muestras básico consiste en una referencia a un registro de imagen y una referencia opcional independiente a un registro de imagen utilizado como muestra.

| `*`basicSwatchSet`*` | `*``*&#42;[',' *`swatchItemswatchItem`*]` |
|---|---|
| `*`swatchItem`*` | `*``*[';' *`imageIndex`*]` |
| `*`muestra`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Referencia de imagen IS (catálogo/id) |
| `*`swatchId`*` | Referencia de imagen IS (catálogo/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *``* [ *`rgbblabel`*]'}'` |
| `*`rrgbb`*` | Valor de color RGB hexadecimal de 6 dígitos empaquetado para muestras de color sólido |
| `*`label`*` | Etiqueta de texto opcional para muestras de color sólido |

**Conjuntos de muestras jerárquicos**

Cada elemento de un conjunto de muestras jerárquicas puede consistir en un elemento de muestra básico o una referencia a un registro de conjunto de muestras (se requieren muestras para dichos elementos).

| `*`hierarchySwatchSet`*` | `*``* &#42;[ ',' *`hierarchySwatchItemhierarchySwatchItem`* ]` |
|---|---|
| `*`hierarchySwatchItem`*` | `*``* | { *``* ';' *`swatchItembasicSwatchSetViewMuestra`* }` |
| `*`basicSwatchSetId`*` | Referencia IS (catálogo/id) a un registro de catálogo que define un conjunto de muestras básico |

**Conjuntos de giros básicos**

Un conjunto de giros básico consta de una lista simple de ID de imagen.

*`basicSpinSet imageId`*  *`[ ';'`  *`imageId`* `]`

**Conjuntos de giros bidimensionales**

Cada elemento de un conjunto de giros bidimensionales puede consistir en una imagen simple, una referencia a un conjunto de giros básico o un conjunto de giros básico en línea delimitado por llaves. Se pueden utilizar paréntesis en lugar de llaves.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*``* | { '{' *``* '}' } | *`imageIdbasicSpinSetbasicSpinSetId`*` |
| `*`basicSpinSetId`*` | Referencia IS (catálogo/id) a un registro de catálogo que define un conjunto de giros básico |

**Conjuntos de páginas**

Cada elemento de un conjunto de páginas puede constar de hasta tres imágenes de página separadas por dos puntos.

| `*`pageSet`*` | `*``* &#42;[ , *`pageItempageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*``* [ : *``* [ : *`imageIdimageIdimageId`* ] ]` |

**Conjuntos de medios**

Cada elemento de un conjunto de medios puede consistir en una imagen, un conjunto de muestras básico, un conjunto de muestras jerárquicas, un conjunto de giros básico, un conjunto de giros bidimensionales, un conjunto de páginas o un recurso de vídeo. Cada elemento del conjunto de medios también puede contener una muestra opcional y un identificador de tipo.

| `*`mediaSet`*` | `*``* &#42;[ , *`elemento de elemento`* ]` |
|---|---|
| `*`elemento`*` | ` { *``* | *``* | *``*}} | *``* } [ ; [ *``* ] [ ; [ *`videoItemrecutItemimageItemsetItemIDreserve`* ] ] ]` |
| `*`videoItem`*` | `*``* ; *`videoswatchId`*` |
| `*`recutItem`*` | `*``* ; *`recutswatchId`*` |
| `*`imageItem`*` | `*``* ; [ *`imageIdMuestraId`* ]` |
| `*`setItem`*` | ` { *``* | { '{' *``* '}' } } ; *`setIdinlineSetswatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | ID de imagen IS |
| `*`video`*` | Ruta del archivo de vídeo/animación o id de catálogo estático |
| `*`recut`*` | Ruta del archivo XML de definición de reedición o id de catálogo estático |
| `*`imageId`*` | ID de imagen IS |
| `*`setId`*` | Referencia IS a imagen, giro o conjunto de catálogos electrónicos |
| `*`inlineSet`*` | Imagen, giro o conjunto de catálogos electrónicos en línea |
| `*`reservado`*` | Reservado para uso futuro |

**Conjuntos de vídeos**

Un conjunto de vídeos consiste en una lista sencilla de ID de vídeo en la que cada id hace referencia a una entrada del catálogo de contenido estático.

*`videoSet videoId`*  *`[ ,`  *`videoId`* `]`

## Propiedades {#section-17c731e5c46646aa90ac21f39bb693ca}

Cadena de texto. Lista separada por comas de valores `catalog::Id`, rutas absolutas de archivo del servidor de imágenes o rutas de archivo relativas a `attribute::RootPath`. Se puede hacer referencia a la misma imagen más de una vez en el conjunto. El registro de catálogo que define puede aparecer en el conjunto en cualquier ubicación.

Este campo participa en la localización de cadenas de texto. Además de las cadenas *`label`* (parte del *`solidColorSpecifier`*), todos los campos delimitados se localizan si incluyen al menos un token de localización &#39; `^loc=…^`&#39;. Consulte [Localización de cadena de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en *Referencia de protocolo HTTP* para obtener más información.

## Predeterminado {#section-c3a60e360393478284f0f2d2da5b963b}

Ninguno.

## Véase también {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) ,  [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), Traducción [ de Id de ](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) Objeto,  [Localización](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)  de Cadena de Texto, Documentación de Visualizadores de Servicio de Imágenes
