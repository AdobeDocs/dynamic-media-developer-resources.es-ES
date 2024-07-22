---
description: Datos del conjunto de imágenes. Proporciona un mecanismo para definir conjuntos ordenados de imágenes y atributos de control utilizados por los visualizadores de Dynamic Media.
solution: Experience Manager
title: Conjunto de imágenes
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: eacf0553-8cec-4a1d-80a5-6fe37b92b5bf
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 1%

---

# Conjunto de imágenes{#imageset}

Datos del conjunto de imágenes. Proporciona un mecanismo para definir conjuntos ordenados de imágenes y atributos de control utilizados por los visualizadores de Dynamic Media.

Un conjunto de imágenes consta de una lista de elementos ordenada y separada por comas. Cada elemento consta de uno o más subelementos (ID de imagen, ID de muestra, rutas de archivos multimedia, etiquetas, etc.), separados por punto y coma, dos puntos o ambos.

Se pueden usar llaves `{ }` y paréntesis `( )` para delimitar cierto contenido (como valores de color) o indicar conjuntos anidados. Los corchetes o paréntesis utilizados de esta forma no deben codificarse y deben aparecer siempre como pares coincidentes; de lo contrario, se produce un error en el análisis del catálogo.

>[!NOTE]
>
>Los siguientes caracteres se utilizan como delimitadores de conjunto y deben estar codificados en HTTP cuando aparecen en el conjunto como parte de los valores de ID o de cadena:
>
>* `,`
>* `;`
>* `:`
>* `{`
>* `}`
>* `(`
>* `)`


Consulte la documentación de los visualizadores del servicio de imágenes para obtener más información sobre la estructura y el uso de los conjuntos de imágenes.

El servidor devuelve el contenido de este campo sin realizar modificaciones en respuesta a una solicitud `req=imageset`.

## Conjuntos estándar {#section-5ecc8ffee7224668b63f601383665564}

El servicio de imágenes admite de forma nativa las siguientes definiciones de conjuntos, y el acceso con ciertos visores implica el análisis, la validación y el procesamiento del conjunto en el lado del servidor. Cada tipo de conjunto se puede identificar especificando el valor correspondiente en `catalog::AssetType`.

**Conjuntos de muestras básicos**

Cada elemento de un conjunto de muestras básico consta de una referencia a un registro de imagen y una referencia independiente opcional a un registro de imagen utilizado como muestra.

| `*`basicSwatchSet`*` | `*`elementoMuestra`*&#42;[',' *`elementoMuestra`*]` |
|---|---|
| `*`elemento de muestra`*` | `*`imageId`*[';' *`muestra`*]` |
| `*`muestra`*` | `*`swatchId`*|solidColorSpecifier` |
| `*`imageId`*` | Referencia de imagen del servicio de imágenes (catálogo/id) |
| `*`swatchId`*` | Referencia de imagen del servicio de imágenes (catálogo/id) |
| `*`solidColorSpecifier`*` | ` '{0x' *`rrggbb`* [ *`etiqueta`*]'}'` |
| `*`rrggbb`*` | Valor de color de RGB hexadecimal de 6 dígitos empaquetado para muestras de color sólido |
| `*`etiqueta`*` | Etiqueta de texto opcional para muestras de color sólido |

**Conjuntos de muestras jerárquicos**

Cada elemento de un conjunto de muestras jerárquico puede constar de un elemento de muestra básico o una referencia a un registro de conjunto de muestras (se requieren muestras para dichos elementos).

| `*`conjunto de muestras jerárquico`*` | `*`elementoMuestraJerárquico`* &#42;[ ',' *`elementoMuestraJerárquico`* ]` |
|---|---|
| `*`elementoMuestraJerárquico`*` | `*`swatchItem`* | { *`basicSwatchSetId`* ';' *`muestra`* }` |
| `*`basicSwatchSetId`*` | Referencia de IS (catalog/id) a un registro de catálogo que define un conjunto de muestras básico |

**Conjuntos de giros básicos**

Un conjunto de giros básico consiste en una lista simple de ID de imagen.

*`basicSpinSet imageId`*  &#42;`[ ';'`  *`imageId`* `]`

**Conjuntos de giros bidimensionales**

Cada elemento de un conjunto de giros bidimensional puede constar de una imagen simple, una referencia a un conjunto de giros básico o un conjunto de giros básico en línea delimitado por llaves. Se pueden utilizar paréntesis en lugar de llaves.

| `*`2dSpinItem`*` | `*`2dSpinSet`* *`2dSpinItem`* &#42;[ ',' *`2dSpinItem`* ]` |
|---|---|
| `*`2dSpinItem`*` | `*`imageId`* | { '{' *`basicSpinSet`* '}' } | *`basicSpinSetId`*` |
| `*`basicSpinSetId`*` | Referencia de IS (catálogo/id) a un registro de catálogo que define un conjunto de giros básico |

**Conjuntos de páginas**

Cada elemento de un conjunto de páginas puede constar de hasta tres imágenes de página separadas por dos puntos.

| `*`pageSet`*` | `*`pageItem`* &#42;[ , *`pageItem`* ]` |
|---|---|
| `*`pageItem`*` | `*`imageId`* [ : *`imageId`* [ : *`imageId`* ] ]` |

**Conjuntos de medios**

Cada elemento de un conjunto de medios puede constar de una imagen, un conjunto de muestras básico, un conjunto de muestras jerárquico, un conjunto de giros básico, un conjunto de giros bidimensional, un conjunto de páginas o un recurso de vídeo. Cada elemento del conjunto de medios también puede contener una muestra opcional y un identificador de tipo.

| `*`mediaSet`*` | `*`elemento`* &#42;[ , *`elemento`* ]` |
|---|---|
| `*`elemento`*` | ` { *`videoItem`* | *`recutItem`* | *`imageItem`*}} | *`setItem`* } [ ; [ *`ID`* ] [ ; [ *`reservado`* ] ] ]` |
| `*`videoItem`*` | `*`vídeo`* ; *`swatchId`*` |
| `*`recutItem`*` | `*`rehacer`* ; *`swatchId`*` |
| `*`imageItem`*` | `*`imageId`* ; [ *`swatchId`* ]` |
| `*`setItem`*` | ` { *`setId`* | { '{' *`inlineSet`* '}' } } ; *`swatchId`*` |
| `*`ID`*` | `media type identifier [ img | basic | advanced_image | img | img_set | advanced_imageset | advanced_swatchset | spin | video ]` |
| `*`swatchId`*` | ID de imagen IS |
| `*`vídeo`*` | Ruta del archivo de vídeo/animación o ID de catálogo estático |
| `*`rehacer`*` | Ruta del archivo XML de definición de reedición o ID de catálogo estático |
| `*`imageId`*` | ID de imagen IS |
| `*`setId`*` | Referencia IS a imagen, giro o conjunto de catálogo electrónico |
| `*`inlineSet`*` | Conjunto de imagen, giro o catálogo electrónico en línea |
| `*`reservado`*` | Reservado para uso futuro |

**Conjuntos de vídeos**

Un conjunto de vídeos consiste en una sencilla lista de ID de vídeo en la que cada ID hace referencia a una entrada del catálogo de contenido estático.

*`videoSet videoId`*  &#42;`[ ,`  *`videoId`* `]`

## Propiedades {#section-17c731e5c46646aa90ac21f39bb693ca}

Cadena de texto. Lista separada por comas de `catalog::Id` valores, rutas absolutas de archivo del servidor de imágenes o rutas de archivo relativas a `attribute::RootPath`. Se puede hacer referencia a la misma imagen más de una vez en el conjunto. El registro de catálogo que define puede aparecer en el conjunto en cualquier ubicación.

Este campo participa en la localización de cadenas de texto. Además de las cadenas de *`label`* (parte de *`solidColorSpecifier`*), todos los campos delimitados se localizan si incluyen al menos un token de localización de `^loc=…^`. Consulte [Localización de cadenas de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) en la *Referencia de protocolo HTTP* para obtener detalles.

## Predeterminado {#section-c3a60e360393478284f0f2d2da5b963b}

Ninguno.

## Véase también {#section-4c99c44f99074aa0a4ed90ba183bbc25}

[req=imageset](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md), [Traducción de id. de objeto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-object-id-translation.md) , [Localización de cadena de texto](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) , Documentación de visualizadores de Image Serving
