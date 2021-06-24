---
description: Tiempo de vida de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché del cliente y del servidor proxy.
solution: Experience Manager
title: Vencimiento
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5717d568-467e-495b-b963-9b3d42e866a6
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 4%

---

# Vencimiento{#expiration}

Tiempo de vida de la caché del cliente. Número de horas hasta la caducidad. Se utiliza para administrar el almacenamiento en caché del cliente y del servidor proxy.

Consulte ` [catalog::Expiration](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce)` para obtener más información.

## Propiedades {#section-dcdd44cc3f0a4849b968dbd4f1e3768a}

Número real, -2, -1, 0 o bueno. Número de horas hasta la caducidad desde que se generó la imagen de respuesta. Establézcalo en 0 para que siempre caduque la imagen de respuesta inmediatamente, lo que deshabilita efectivamente el almacenamiento en caché del cliente. Configure en -1 para marcar como `never expire`; en este caso, el servidor siempre devuelve el estado 403 en respuesta a solicitudes condicionales `GET` sin comprobar si el archivo ha cambiado realmente. Configúrelo en -2 para utilizar el valor predeterminado proporcionado por `attribute::Expiration`.

## Predeterminado {#section-fb8ea80975034b49af7510764758f123}

`attribute::Expiration` se utiliza si el campo no está presente, si el valor es -2 o si el campo está vacío.

## Véase también {#section-a0d3dab0f6db49b58f1f935d3bdea2fd}

[atributo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-expiration.md#reference-0f68ad8199c64bd4bc8d27dd78b7d996) ,  [catálogo::Caducidad](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce),  [req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
