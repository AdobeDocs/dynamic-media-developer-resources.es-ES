---
title: Errores
description: Si una solicitud no se puede completar correctamente, el servidor devuelve una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 1%

---

# Errores{#errors}

Si una solicitud no se puede completar correctamente, el servidor devuelve una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.

El valor del estado de respuesta depende del tipo de error; para los errores más comunes, es &quot;403&quot;. Las respuestas de error para los tipos de solicitud que no son de imagen se ajustan al formato especificado con `req=`. (Es posible que no se implemente de forma coherente en este momento).

La cantidad de detalles incluidos en el mensaje de error se puede configurar con `attribute::ErrorDetail`.

**Imágenes de error**

El servicio de imágenes se puede configurar para que devuelva los mensajes de error procesados en una imagen. Consulte `attribute::ErrorImage` en la referencia del catálogo de imágenes para obtener más información. Si la imagen de error se genera correctamente, el estado de respuesta HTTP es 200. Si se produce un error al procesar la imagen de error, se devuelve al cliente la respuesta de error HTTP estándar y el mensaje de texto.

**Ver también**

[attribute::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) , [attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
