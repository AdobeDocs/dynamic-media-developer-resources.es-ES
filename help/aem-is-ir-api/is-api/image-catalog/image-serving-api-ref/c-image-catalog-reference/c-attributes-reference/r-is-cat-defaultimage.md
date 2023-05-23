---
description: Imagen de respuesta predeterminada. Especifica la imagen o la entrada de catálogo que se utilizará en caso de que no se encuentre un archivo de imagen y defaultImage= no se especifique en la solicitud.
solution: Experience Manager
title: DefaultImage
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2044b447-0ee1-4964-b751-8637c5e115d1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# DefaultImage{#defaultimage}

Imagen de respuesta predeterminada. Especifica la imagen o la entrada de catálogo que se utilizará en caso de que no se encuentre un archivo de imagen y defaultImage= no se especifique en la solicitud.

Puede ser una entrada de catálogo (incluida una plantilla) o un relativo (a `attribute::RootPath`) o ruta absoluta del archivo de imagen. Útil para sustituir imágenes que faltan por imágenes predeterminadas.

## Propiedades {#section-b6d8193827c34e5f948792aba8b8daaf}

Cadena de texto. Si se especifica, debe ser un válido `catalog::Id` en este catálogo de imágenes o un relativo (a `attribute::RootPath`) o ruta absoluta a un archivo de imagen accesible mediante el servidor de imágenes.

## Restricciones {#section-5d8ea872f0b0415fbd3a83410bbcf512}

El mecanismo de imagen predeterminado no cubre los orígenes de imagen externos; se devuelve un error si un origen de imagen externo no es válido.

## Predeterminado {#section-d88bc8fc71bd413e8f70281d57e1ba1c}

Heredado de `default::DefaultImage` si no está definido. Si se define pero está vacío, el comportamiento predeterminado de la imagen se desactiva, incluso si `default::DefaultImage` está definida.

## Véase también {#section-dc0fb4e72294442882b33a479fbc2b82}

[attribute::DefaultImageMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultimagemode.md#reference-8a996af162f84e46bbe9e6e0d4e26782) , [defaultImage=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [attribute::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [catalog::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md), [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf)
