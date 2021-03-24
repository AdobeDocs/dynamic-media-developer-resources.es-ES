---
description: Imagen de respuesta de error. El procesamiento de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error. atributo ErrorImage permite que la configuración de una imagen se devuelva en caso de error.
solution: Experience Manager
title: ErrorImage *
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 1%

---


# ErrorImage *{#errorimage}

Imagen de respuesta de error. El procesamiento de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error. attribute::ErrorImage permite devolver una imagen de configuración en caso de error.

Cuando se produce un error, el servidor intenta primero interpretar el valor de `ImageRendering::attribute::ErrorImage`como una ruta de archivo de imagen simple. Si el archivo no se puede abrir, envía el valor del atributo y los detalles de error al servicio de imágenes, que procesa como se describe en `ImageServing::attribute::ErrorImage`. Si Image Serving no devuelve una imagen de respuesta válida, el estado de error HTTP estándar y el mensaje de texto se envían al cliente.

Las imágenes de error se devuelven con el estado HTTP 200.

## Propiedades {#section-4a4a7e37ed11483db0b9922dc68ea7db}

Cadena de texto. Si se especifica, debe ser un valor **`ImageServing::catalog::id`**, una ruta relativa (a **`ImageServing::attribute::RootPath`** o **`ImageRendering::attribute::RootPath`**) o una ruta absoluta a un archivo de imagen al que el servidor de imágenes pueda acceder.

## Predeterminado {#section-4c463e369dfb4b43a7b2a3bce9619dd4}

Se hereda de `default::ErrorImage` si no se define. Si está definida pero está vacía, el comportamiento de la imagen de error se desactiva, incluso si `default::ErrorImage` está definido y se devuelve un estado de error HTTP.

## Véase también {#section-3e0308eaf4124451909dacd570e27695}

[atributo::DefaultImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f),  [atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b),  [atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3),  [catálogo::Id](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85)
