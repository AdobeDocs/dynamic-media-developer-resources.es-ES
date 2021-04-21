---
description: Si una solicitud no se puede completar correctamente, el servidor devolverá una imagen de error o un estado de respuesta HTTP que no sea 200 junto con un mensaje de error.
solution: Experience Manager
title: Errores
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 2%

---


# Errores{#errors}

Si una solicitud no se puede completar correctamente, el servidor devolverá una imagen de error o un estado de respuesta HTTP que no sea 200 junto con un mensaje de error.

El valor del estado de respuesta depende del tipo de error; para los errores más comunes es &quot;403&quot;. Las respuestas de error para los tipos de solicitud que no son de imagen se ajustan al formato especificado con `req=`. (Es posible que no se implemente de manera consistente en este momento).

La cantidad de detalles incluida en el mensaje de error se puede configurar con `attribute::ErrorDetail`.

**Imágenes de error**

El servicio de imágenes se puede configurar para que devuelva mensajes de error procesados en una imagen. Consulte `attribute::ErrorImage` en la referencia del catálogo de imágenes para obtener más información. Si la imagen de error se genera correctamente, el estado de la respuesta HTTP es 200. Si se produce un error al procesar la imagen de error, la respuesta de error HTTP estándar y el mensaje de texto se devuelven al cliente.

**Véase también**

[atributo::ErrorDetail](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errordetail.md#reference-123b56eed6cf49cea6e0490672b7c53b) ,  [atributo::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
