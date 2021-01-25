---
description: Tiempo de espera de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché de cliente y servidor proxy.
seo-description: Tiempo de espera de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché de cliente y servidor proxy.
seo-title: Vencimiento
solution: Experience Manager
title: Vencimiento
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6dbd7d43-727c-42fc-8953-dba112209a45
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 2%

---


# Caducidad{#expiration}

Tiempo de espera de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché de cliente y servidor proxy.

El servidor calcula la fecha y hora de caducidad de los datos de respuesta NTTP agregando este valor a la fecha y hora de transmisión.

Los navegadores administran las memorias caché utilizando los tiempos de caducidad de los archivos. Antes de pasar una solicitud al servidor, el explorador comprobará su caché para ver si el archivo ya se ha descargado. Si es así, y si el archivo aún no ha caducado, el explorador enviará una solicitud de GET condicional (por ejemplo, con el encabezado de solicitud If-Modified-Since HTTP) en lugar de una solicitud de GET normal. El servidor tiene la opción de responder con el estado &#39;304&#39; y no transmitir la imagen. El explorador simplemente cargará el archivo desde su caché. Esto puede aumentar sustancialmente el rendimiento general de los datos a los que se accede con frecuencia.

El servidor establecerá el encabezado de respuesta HTTP expires en la fecha y hora actuales más el valor más pequeño de la viñeta::Caducidad y todo el catálogo::Valores de caducidad para la viñeta y todos los materiales involucrados en la operación de procesamiento.

La caducidad se establece principalmente para las respuestas de datos de imagen. Determinados tipos de respuestas siempre se marcarán para su caducidad inmediata (o se etiquetarán como no procesables), incluidas todas las respuestas de error o las respuestas de propiedad.

## Propiedades {#section-e87e8f6b6d224c6ea2eeaad695c04be8}

Número real, -2, -1, 0 o bueno. Número de horas hasta la caducidad desde que se generó la imagen de respuesta. Establezca el valor 0 para que la imagen de respuesta caduque siempre inmediatamente, lo que deshabilita el almacenamiento en caché del cliente. Establezca en -1 para marcar como `never expire`. En este caso, el servidor siempre devuelve el estado 304 (no modificado) en respuesta a solicitudes condicionales `GET` sin comprobar si el archivo ha cambiado realmente. Establezca en -2 para utilizar el valor predeterminado proporcionado por `attribute::Expiration`.

## Predeterminado {#section-79d71706e12a4493a69d7febc3a1f271}

`attribute::Expiration` se utiliza si el campo no está presente, si el valor es -2 o si el campo está vacío.

## Véase también {#section-9d46a9d346fe42f3911edb3bd79f4121}

[atributo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [viñeta::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
