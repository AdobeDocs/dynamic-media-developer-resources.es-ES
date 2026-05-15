---
description: Si una solicitud no se puede completar correctamente, el servidor devuelve una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.
solution: Experience Manager
title: Errores
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
TQID: 'https://experienceleague.adobe.com/qqe0JDlFGu08lAe-K3Ww9AtefwQInwBzZswiXsvqryo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 203
ht-degree: 1%

---

# Errores{#errors}

Si una solicitud no se puede completar correctamente, el servidor devuelve una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.

El valor del estado de respuesta depende del tipo de error; para los errores más comunes es &quot;403&quot;. Las respuestas de error para los tipos de solicitud que no son de imagen se ajustan al formato especificado con `req=`. (Es posible que no se implemente de forma coherente en este momento).

La cantidad de detalles incluidos en el mensaje de error se puede configurar con `attribute::ErrorDetail`.

## Imágenes de error {#section-92e9b20b2507433daa96923abc95f777}

El servicio de imágenes se puede configurar para que devuelva los mensajes de error procesados en una imagen.

Consulte [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c) en la referencia del catálogo de imágenes para obtener más información.

Si la imagen de error se genera correctamente, el estado de respuesta HTTP es 200. Si se produce un error al procesar la imagen de error, se devuelve al cliente la respuesta de error HTTP estándar y el mensaje de texto.

## Imagen predeterminada {#section-66bf25fe6b434081bfae96d38d9be25e}

El servicio de imágenes se puede configurar para sustituir una imagen que falta por una imagen predeterminada. La imagen predeterminada se puede especificar con `attribute::DefaultImage` o el comando `defaultImage=`.

## Véase también {#section-e261d7f224ca4546bb64bf8cb909db08}

[attribute::ErrorDetail](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errordetail.md#reference-4987c8cddcba4c88960170e49cafc561) , [attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c), [attribute::DefaultImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-defaultimage.md#reference-8e9900e129f54ed68462a3c2fc3bc433), [defaultImage=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-defaultimage.md#reference-209aa6ce830f490483412eb26af67fd2)
