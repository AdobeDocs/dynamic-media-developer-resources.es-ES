---
description: Imagen de respuesta al error. El procesamiento de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error. error de atributoImage permite que se devuelva una imagen en caso de error.
seo-description: Imagen de respuesta al error. El procesamiento de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error. error de atributoImage permite que se devuelva una imagen en caso de error.
seo-title: ErrorImage *
solution: Experience Manager
title: ErrorImage *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6c8801d0-8cd0-4477-9a60-ccbb343a0747
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---


# ErrorImage *{#errorimage}

Imagen de respuesta al error. El procesamiento de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error. attribute::ErrorImage permite que se devuelva una imagen en caso de error.

Cuando se produce un error, el servidor primero intenta interpretar el valor de `ImageRendering::attribute::ErrorImage`como una ruta de archivo de imagen simple. Si el archivo no se puede abrir, envía el valor del atributo y los detalles del error al servicio de imágenes, que se procesa tal como se describe en `ImageServing::attribute::ErrorImage`. Si el servicio de imágenes no devuelve una imagen de respuesta válida, el estado de error HTTP estándar y el mensaje de texto se envían al cliente.

Las imágenes de error se devuelven con el estado HTTP 200.

## Propiedades {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Cadena de texto. Si se especifica, debe ser un valor **`ImageServing::catalog::id`**, una ruta relativa (a **`ImageServing::attribute::RootPath`** o **`ImageRendering::attribute::RootPath`**) o una ruta absoluta a un archivo de imagen al que el servidor de imágenes pueda acceder.

## Predeterminado {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Se hereda de `default::ErrorImage` si no se define. Si está definida pero está vacía, el comportamiento de la imagen de error se desactiva, incluso si se define `default::ErrorImage` y se devuelve un estado de error HTTP.

## Véase también {#section-3e0308eaf4124451909dacd570e27695}

[atributo::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catálogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
