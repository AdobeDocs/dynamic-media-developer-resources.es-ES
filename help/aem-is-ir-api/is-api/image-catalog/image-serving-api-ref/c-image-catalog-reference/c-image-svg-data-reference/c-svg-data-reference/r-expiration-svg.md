---
description: Vencimiento
solution: Experience Manager
title: Vencimiento
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 62d2368b-ea56-4964-ab9c-07454e19540c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 2%

---

# Vencimiento{#expiration}

Se utiliza para administrar el almacenamiento en caché del cliente y del servidor proxy. El servidor calcula la fecha y hora de caducidad de los datos de respuesta HTTP añadiendo este valor a la hora y la fecha de transmisión.

Los navegadores administran las cachés mediante tiempos de caducidad de los archivos. Antes de pasar una solicitud al servidor, el explorador comprueba su caché para ver si el archivo ya se ha descargado. Si es así, y si el archivo aún no ha caducado, el explorador envía una solicitud de GET condicional (por ejemplo, con el campo If-Modified-Since establecido en el encabezado de la solicitud) en lugar de una solicitud de GET normal. El servidor tiene la opción de responder con un estado &quot;304&quot; y no transmitir la imagen. A continuación, el explorador carga el archivo desde su caché. Esto puede aumentar sustancialmente el rendimiento general de los datos a los que se accede con frecuencia.

La caducidad se utiliza para estos tipos de respuesta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Ciertos tipos de respuestas (por ejemplo, respuestas de error) siempre se marcan para su caducidad inmediata (o se etiquetan como no almacenables en caché), mientras que otros (por ejemplo, respuestas de imagen predeterminadas o propiedades) utilizan una configuración de caducidad especial ( `attribute::NonImgExpiration` y `attribute::DefaultExpiration`).

## Propiedades {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Número real, -2, -1, 0 o bueno. Número de horas hasta la caducidad desde que se generó la imagen de respuesta. Establézcalo en 0 para que siempre caduque la imagen de respuesta inmediatamente, lo que deshabilita efectivamente el almacenamiento en caché del cliente. Configúrelo en -1 para marcar como *`never expire`*. En este caso, el servidor siempre devuelve el estado 304 (no modificado) como respuesta a las solicitudes de GET condicionales sin comprobar si el archivo ha cambiado realmente. Configúrelo en -2 para utilizar el valor predeterminado proporcionado por `attribute::Expiration`.

## Predeterminado {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` se utiliza si el campo no está presente, si el valor es -2 o si el campo está vacío.

## Véase también {#section-0e5e8595aad641c689726828712a8902}

[atributo::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [atributo::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [atributo::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
