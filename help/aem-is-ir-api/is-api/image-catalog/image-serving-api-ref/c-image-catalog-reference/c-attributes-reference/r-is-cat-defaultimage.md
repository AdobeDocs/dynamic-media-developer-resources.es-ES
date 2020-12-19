---
description: Imagen de respuesta predeterminada. Especifica la imagen o entrada de catálogo que se utilizará en caso de que no se encuentre un archivo de imagen y no se especifique defaultImage= en la solicitud.
seo-description: Imagen de respuesta predeterminada. Especifica la imagen o entrada de catálogo que se utilizará en caso de que no se encuentre un archivo de imagen y no se especifique defaultImage= en la solicitud.
seo-title: DefaultImage
solution: Experience Manager
title: DefaultImage
topic: Scene7 Image Serving - Image Rendering API
uuid: 6f8f50af-15bb-4333-b227-3eba38653a7d
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 2%

---


# DefaultImage{#defaultimage}

Imagen de respuesta predeterminada. Especifica la imagen o entrada de catálogo que se utilizará en caso de que no se encuentre un archivo de imagen y no se especifique defaultImage= en la solicitud.

Puede ser una entrada de catálogo (incluida una plantilla) o una ruta de archivo de imagen relativa (a `attribute::RootPath`) o absoluta. Resulta útil para sustituir las imágenes que faltan por las imágenes predeterminadas.

## Propiedades {#section-b6d8193827c34e5f948792aba8b8daaf}

Cadena de texto. Si se especifica, debe ser un valor `catalog::Id` válido en este catálogo de imágenes o una ruta relativa (a `attribute::RootPath`) o absoluta a un archivo de imagen accesible por el servidor de imágenes.

## Restricciones {#section-5d8ea872f0b0415fbd3a83410bbcf512}

Las fuentes de imagen extranjeras no están cubiertas por el mecanismo de imagen predeterminado; se devuelve un error si un origen de imagen externo no es válido.

## Predeterminado {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Se hereda de `default::DefaultImage` si no se define. Si está definida pero está vacía, el comportamiento de la imagen predeterminada está desactivado, aunque se haya definido `default::DefaultImage`.

## Véase también {#section-dc0fb4e72294442882b33a479fbc2b82}

[atributo::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) ,  [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494),  [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [atributo::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c),  [atributo::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
