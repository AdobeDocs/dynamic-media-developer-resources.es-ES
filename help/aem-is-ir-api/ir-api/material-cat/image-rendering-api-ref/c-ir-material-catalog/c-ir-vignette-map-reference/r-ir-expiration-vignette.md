---
description: Tiempo de espera de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché de cliente y servidor proxy.
seo-description: Tiempo de espera de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché de cliente y servidor proxy.
seo-title: Vencimiento
solution: Experience Manager
title: Vencimiento
topic: Scene7 Image Serving - Image Rendering API
uuid: fa267728-9a36-4705-97d6-d567148fc2d7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 4%

---


# Caducidad{#expiration}

Tiempo de espera de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché de cliente y servidor proxy.

Consulte ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` para obtener más información.

## Propiedades {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Número real, -2, -1, 0 o bueno. Número de horas hasta la caducidad desde que se generó la imagen de respuesta. Establezca el valor 0 para que la imagen de respuesta caduque siempre inmediatamente, lo que deshabilita el almacenamiento en caché del cliente. Establezca en -1 para marcar como `never expire`; en este caso, el servidor siempre devuelve el estado 403 en respuesta a solicitudes condicionales `GET` sin comprobar si el archivo ha cambiado realmente. Establezca en -2 para utilizar el valor predeterminado proporcionado por `attribute::Expiration`.

## Predeterminado {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` se utiliza si el campo no está presente, si el valor es -2 o si el campo está vacío.

## Véase también {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[atributo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catálogo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
