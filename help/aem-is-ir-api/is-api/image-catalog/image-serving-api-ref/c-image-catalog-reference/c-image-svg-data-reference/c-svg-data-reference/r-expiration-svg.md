---
description: Vencimiento
solution: Experience Manager
title: Vencimiento
topic: Scene7 Image Serving - Image Rendering API
uuid: f51e45fc-fcea-4df6-8c47-e772a1b70a3a
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 2%

---


# Caducidad{#expiration}

Se utiliza para administrar el almacenamiento en caché de cliente y servidor proxy. El servidor calcula la fecha y hora de caducidad de los datos de respuesta HTTP agregando este valor a la hora y la fecha de transmisión.

Los navegadores administran las memorias caché utilizando los tiempos de caducidad de los archivos. Antes de pasar una solicitud al servidor, el explorador comprueba su caché para ver si el archivo ya se ha descargado. Si es así, y si el archivo aún no ha caducado, el explorador envía una solicitud de GET condicional (por ejemplo, con el campo If-Modified-Since establecido en el encabezado de la solicitud) en lugar de una solicitud de GET normal. El servidor tiene la opción de responder con el estado &#39;304&#39; y no transmitir la imagen. A continuación, el explorador carga el archivo desde su caché. Esto puede aumentar sustancialmente el rendimiento general de los datos a los que se accede con frecuencia.

Se utiliza la caducidad para estos tipos de respuesta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Ciertos tipos de respuestas (por ejemplo, respuestas de error) siempre se marcan para su caducidad inmediata (o se etiquetan como no se pueden almacenar en caché), mientras que otros (por ejemplo, respuestas de propiedades o imágenes predeterminadas) utilizan una configuración de caducidad especial ( `attribute::NonImgExpiration` y `attribute::DefaultExpiration`).

## Propiedades {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Número real, -2, -1, o 0 o bueno. Número de horas hasta la caducidad desde que se generó la imagen de respuesta. Establezca el valor 0 para que la imagen de respuesta caduque siempre inmediatamente, lo que deshabilita el almacenamiento en caché del cliente. Establezca en -1 para marcar como *`never expire`*. En este caso, el servidor siempre devuelve el estado 304 (no modificado) en respuesta a solicitudes de GET condicionales sin comprobar si el archivo ha cambiado realmente. Establezca en -2 para utilizar el valor predeterminado proporcionado por `attribute::Expiration`.

## Predeterminado {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` se utiliza si el campo no está presente, si el valor es -2 o si el campo está vacío.

## Véase también {#section-0e5e8595aad641c689726828712a8902}

[atributo::Expiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7),  [atributo::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf),  [atributo::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d),  [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
