---
title: Vencimiento
description: Se utiliza para administrar el almacenamiento en caché de clientes y servidores proxy. El servidor calcula la fecha y hora de caducidad de los datos de respuesta HTTP agregando este valor a la fecha y hora de la transmisión.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 064dab12-5f58-4e19-a6b1-fbd20182e3aa
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 1%

---

# Vencimiento{#expiration}

Se utiliza para administrar el almacenamiento en caché de clientes y servidores proxy. El servidor calcula la fecha y hora de caducidad de los datos de respuesta HTTP agregando este valor a la fecha y hora de la transmisión.

Los navegadores administran las cachés utilizando los tiempos de caducidad de los archivos. Antes de pasar una solicitud al servidor, el explorador comprueba su caché para ver si el archivo ya se ha descargado. Si es así y si el archivo aún no ha caducado, el explorador envía una solicitud de GET condicional (por ejemplo, con el campo If-Modified-Since configurado en el encabezado de la solicitud) en lugar de una solicitud de GET normal. El servidor tiene la opción de responder con un estado &quot;304&quot; y no transmitir la imagen. A continuación, el explorador carga el archivo desde su caché. Esto puede aumentar sustancialmente el rendimiento general de los datos a los que se accede con frecuencia.

La caducidad se utiliza para estos tipos de respuesta:

* `req=img`
* `req=mask`
* `req=tmb`
* `req=userdata`
* `req=map`

Algunos tipos de respuesta (por ejemplo, respuestas de error) siempre se marcan para su caducidad inmediata (o se etiquetan como no almacenables en caché), mientras que otros (por ejemplo, respuestas de propiedad o de imagen predeterminadas) utilizan configuraciones de caducidad especiales ( `attribute::NonImgExpiration` y `attribute::DefaultExpiration`).

## Propiedades {#section-7f5173d090cf48df8fa1a2c72b8c8c60}

Número real, -2, -1 o 0 o bueno. Número de horas hasta la caducidad desde que se generó la imagen de respuesta. Si se establece en 0, la imagen de respuesta siempre caducará inmediatamente, lo que deshabilita el almacenamiento en caché del cliente. Establezca en -1 para marcar como *`never expire`*. En este caso, el servidor siempre devuelve el estado 304 (sin modificar) en respuesta a solicitudes de GET condicionales sin comprobar si el archivo ha cambiado realmente. Establezca el valor en -2 para utilizar el valor predeterminado proporcionado por `attribute::Expiration`.

## Predeterminado {#section-ec72cc1dfc5e4f278174d37da2e39462}

`attribute::Expiration` se utiliza si el campo no está presente, si el valor es -2 o si el campo está vacío.

## Véase también {#section-0e5e8595aad641c689726828712a8902}

[attribute::Caducidad](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-expiration.md#reference-a0bf4686425d4e00b8014c4950fb62b7), [attribute::DefaultExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attribute::NonImgExpiration](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d), [req=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
