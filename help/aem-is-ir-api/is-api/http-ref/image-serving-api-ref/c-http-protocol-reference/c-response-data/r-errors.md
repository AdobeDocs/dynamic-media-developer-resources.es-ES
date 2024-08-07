---
description: Si una solicitud no se puede completar correctamente, el servidor devuelve una imagen de error o un estado de respuesta HTTP distinto de 200 junto con un mensaje de error.
solution: Experience Manager
title: Errores
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9314782f-703b-4e9c-a026-62970d1c752f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '202'
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
