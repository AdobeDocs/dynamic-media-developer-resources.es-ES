---
title: ErrorImage
description: Imagen de respuesta de error. Normalmente, el procesamiento de imágenes devuelve un estado de error con un mensaje de texto cuando se produce un error.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ed48482f-79b0-4c81-b5cd-cf997f27d3ab
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---

# ErrorImage {#errorimage}

Imagen de respuesta de error. Normalmente, el procesamiento de imágenes devuelve un estado de error con un mensaje de texto cuando se produce un error. El `attribute::ErrorImage` permite devolver una imagen configurada si hay un error.

Cuando se produce un error, el servidor intenta interpretar el valor de `ImageRendering::attribute::ErrorImage` como una ruta de acceso de archivo de imagen simple. Si no se puede abrir el archivo, envía el valor del atributo y los detalles del error al servicio de imágenes, que procesa como se describe en `ImageServing::attribute::ErrorImage`. Si el servicio de imágenes no devuelve una imagen de respuesta válida, el estado de error HTTP estándar y el mensaje de texto se envían al cliente.

Las imágenes de error se devuelven con el estado HTTP 200.

## Propiedades {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Cadena de texto. Si se especifica, debe ser un valor **`ImageServing::catalog::id`**, una ruta de acceso relativa (a **`ImageServing::attribute::RootPath`** o **`ImageRendering::attribute::RootPath`**) o una ruta de acceso absoluta a un archivo de imagen al que el servidor de imágenes pueda acceder.

## Predeterminado {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Se hereda de `default::ErrorImage` si no está definido. Si está definida pero vacía, el comportamiento de la imagen de error se deshabilita, incluso si se define `default::ErrorImage` y se devuelve un estado de error HTTP.

## Véase también {#section-3e0308eaf4124451909dacd570e27695}

[attribute::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b), [attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3), [catálogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
