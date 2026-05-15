---
title: Errores
description: Si una solicitud no se puede completar correctamente, el servidor devuelve una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e45e3968-3659-470b-a88a-fe7ba73d8207
TQID: 'https://experienceleague.adobe.com/TSTpmfiuEppAPSUxX1ga5lfQSgWRkI2Wh1CXoalSU9A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
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
