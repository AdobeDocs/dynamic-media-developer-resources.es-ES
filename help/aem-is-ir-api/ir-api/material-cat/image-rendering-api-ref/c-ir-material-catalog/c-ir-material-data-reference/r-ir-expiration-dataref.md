---
title: Vencimiento
description: Tiempo de vida de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché del cliente y del servidor proxy.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e4f7e5a8-0021-4dd3-be1b-8cb656cabdac
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 1%

---

# Vencimiento{#expiration}

Tiempo de vida de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché del cliente y del servidor proxy.

El servidor calcula la fecha y hora de caducidad de los datos de respuesta NTTP añadiendo este valor a la hora y la fecha de transmisión.

Los navegadores administran las cachés mediante tiempos de caducidad de los archivos. Antes de pasar una solicitud al servidor, el explorador comprobará su caché para ver si el archivo ya se ha descargado. Si es así, y si el archivo aún no ha caducado, el explorador enviará una solicitud de GET condicional (por ejemplo, con el encabezado de solicitud HTTP If-Modified-Since) en lugar de una solicitud de GET normal. El servidor tiene la opción de responder con un estado &quot;304&quot; y no transmitir la imagen. El navegador simplemente cargará el archivo desde su caché. Esto puede aumentar sustancialmente el rendimiento general de los datos a los que se accede con frecuencia.

El servidor establecerá el encabezado de respuesta HTTP expira en la fecha y hora actuales, además del menor de los valores de viñeta::Expiration y all catalog::Expiration para la viñeta y todos los materiales implicados en la operación de renderización.

La caducidad se establece principalmente para las respuestas de datos de imagen. Ciertos tipos de respuestas siempre se marcarán para su caducidad inmediata (o se etiquetarán como no almacenables en caché), incluidas todas las respuestas de error o las respuestas de propiedad.

## Propiedades {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Número real, -2, -1, 0 o bueno. Número de horas hasta la caducidad desde que se generó la imagen de respuesta. Establézcalo en 0 para que siempre caduque la imagen de respuesta inmediatamente, lo que deshabilita efectivamente el almacenamiento en caché del cliente. Configure en -1 para marcar como `never expire`. En este caso, el servidor siempre devuelve el estado 304 (no modificado) como respuesta a las preguntas condicionales `GET` sin comprobar si el archivo ha cambiado realmente. Configúrelo en -2 para utilizar el valor predeterminado proporcionado por `attribute::Expiration`.

## Predeterminado {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` se utiliza si el campo no está presente, si el valor es -2 o si el campo está vacío.

## Véase también {#section-9d46a9d346fe42f3911edb3bd79f4121}

[atributo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) , [viñeta::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c), [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
