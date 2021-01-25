---
description: Imagen de respuesta al error. El servicio de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error.
seo-description: Imagen de respuesta al error. El servicio de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error.
seo-title: ErrorImage
solution: Experience Manager
title: ErrorImage
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b071c0cd-e7b8-422b-9b23-d93f504d9ce5
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 1%

---


# ErrorImage{#errorimage}

Imagen de respuesta al error. El servicio de imágenes normalmente devuelve un estado de error con un mensaje de texto cuando se produce un error.

`attribute::ErrorImage` permite que se devuelva una imagen, entrada de catálogo o plantilla en caso de error.

>[!NOTE]
>
>Las imágenes que faltan también se pueden gestionar con `attribute::DefaultImage`.

Se puede configurar una plantilla de servicio de imágenes que pueda representar el texto del mensaje de error en la imagen de respuesta. Las siguientes variables predefinidas pueden incluirse en la plantilla `$error.title`, que se sustituye por una breve descripción del error, y `$error.message`, que se sustituye por una descripción del error más detallada (el nivel de detalle se configura con `attribute::ErrorDetail`).

Se devuelve el estado HTTP 200 si la imagen o plantilla de error se puede procesar correctamente. Si se produce un error durante este procesamiento, se devuelve el estado de error HTTP y un mensaje de texto.

## Propiedades {#section-f460c6c2dd1f46b29f9a79b093575f45}

Cadena de texto. Si se especifica, debe ser un valor de catálogo válido::Id en un catálogo de imágenes o una ruta relativa (a `attribute::RootPath`) o absoluta a un archivo de imagen accesible por el servidor de imágenes.

## Predeterminado {#section-2885f289e5714ddca665a6aee401967f}

Se hereda de `default::ErrorImage` si no se define. Si se define pero está vacío, el comportamiento de la imagen de error se desactiva, incluso si se define `default::ErrorImage` y se devuelve un estado de error HTTP y un mensaje de texto.

## Ejemplo {#section-c92090abe1d247529542a8dd4960c2e6}

Para obtener imágenes de respuesta con el mensaje de error procesado en la imagen, primero debemos definir la plantilla en el catálogo de imágenes. En este caso, creamos una entrada en nuestro catálogo de imágenes llamada `onError`, que contiene lo siguiente en `catalog::Modifier`:

`size=300,300&bgc=ffffff&text=$error.message$`

La plantilla está registrada con `attribute::ErrorImage`:

`ErrorImage=myCatalog/onError`

En este ejemplo, el texto se procesará con la fuente predeterminada, el color de fuente y el tamaño de fuente.

## Véase también {#section-bbf1f85fc0a34033bdda1dd3e4e0bbb6}

[atributo::RootPath](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494) ,  [catálogo::Id](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-id-cat.md),  [atributo::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433),  [atributo::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561)
