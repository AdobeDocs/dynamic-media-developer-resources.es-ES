---
description: Si una solicitud no se puede completar correctamente, el servidor devolverá una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.
seo-description: Si una solicitud no se puede completar correctamente, el servidor devolverá una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.
seo-title: Errores
solution: Experience Manager
title: Errores
topic: Scene7 Image Serving - Image Rendering API
uuid: 5984fa9e-63c8-426b-be5f-48f66fc918c3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Errores{#errors}

Si una solicitud no se puede completar correctamente, el servidor devolverá una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.

El valor de estado de la respuesta depende del tipo de error; para los errores más comunes es &#39;403&#39;. Las respuestas de error para tipos de solicitudes que no son de imagen se ajustan al formato especificado con `req=`. (Puede que no se implemente de manera consistente en este momento).

La cantidad de detalles incluida en el mensaje de error se puede configurar con `attribute::ErrorDetail`.

**Imágenes de error**

El servicio de imágenes se puede configurar para devolver mensajes de error procesados en una imagen. Consulte `attribute::ErrorImage` en la referencia del catálogo de imágenes para obtener más información. Si la imagen de error se genera correctamente, el estado de respuesta HTTP es 200. Si se produce un error al procesar la imagen de error, se devuelve al cliente la respuesta de error HTTP estándar y el mensaje de texto.

**Véase también**

[atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [atributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
