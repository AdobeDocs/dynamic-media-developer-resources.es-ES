---
description: Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o intervalos de direcciones.
seo-description: Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o intervalos de direcciones.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ClientAddressFilter{#clientaddressfilter}

Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o intervalos de direcciones.

Cuando se especifique, se rechazarán las solicitudes a este catálogo de imágenes que procedan de un cliente en una dirección IP no incluida en la lista. `localhost` siempre forma parte implícitamente de la `ClientAddressFilter` definición, aunque no se especifique explícitamente. Las solicitudes procedentes de `localhost` nunca se rechazan, independientemente de la `ClientAddressFilter` especificación.

## Propiedades {#section-21a2992f108d42fb8660c0d65aa61e13}

lista separada por comas de direcciones IP con máscaras de red opcionales (se utiliza la notación[](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) CIDR):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Dirección IP en *[!DNL ddd.ddd.ddd.ddd]* formato

* *[!DNL netmask]* máscara de red (0...32)

Este atributo se omite cuando se aplica una regla de preprocesamiento con un `<addressfilter>` elemento.

## Predeterminado {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Se hereda de `default::AddressFilter` si no está definida o si está vacía.

## Ejemplos {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Sin restricciones de acceso: `0.0.0.0/0`
* Conceder acceso a todas las direcciones comenzando con `192: 192.0.0.0/8`
* Conceder acceso a los 512 hosts con direcciones entre `192.168.12.0` y `192.168.13.255: 192.168.12.0/23`

* Conceder acceso a una sola dirección IP: `192.168.2.117` o `192.168.2.117/32`

## Véase también {#section-6198780c7b3045aabd211eefb38bc565}

[direcsfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
