---
title: ClientAddressFilter
description: Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o rangos de direcciones.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# ClientAddressFilter{#clientaddressfilter}

Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o rangos de direcciones.

Cuando se especifica, se rechazan las solicitudes a este catálogo de imágenes que se originan en un cliente con una dirección IP no incluida en la lista. `localhost` siempre es parte implícita de la variable `ClientAddressFilter` definición, incluso si no se especifica explícitamente. Solicitudes procedentes de `localhost` nunca se rechazan, independientemente de la variable `ClientAddressFilter` especificación.

## Propiedades {#section-21a2992f108d42fb8660c0d65aa61e13}

Lista separada por comas de direcciones IP con máscaras de red opcionales ([Anotación CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) ):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Dirección IP en *[!DNL ddd.ddd.ddd.ddd]* format

* *[!DNL netmask]* máscara de red (0...32)

Este atributo se ignora cuando una regla de preprocesamiento con un `<addressfilter>` se aplica.

## Predeterminado {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Heredado de `default::AddressFilter` si no está definida o si está vacío.

## Ejemplos {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Sin restricciones de acceso: `0.0.0.0/0`
* Conceder acceso a todas las direcciones que empiecen por `192: 192.0.0.0/8`
* Conceder acceso a los 512 hosts con direcciones entre `192.168.12.0` y `192.168.13.255: 192.168.12.0/23`

* Conceder acceso a una sola dirección IP: `192.168.2.117` o `192.168.2.117/32`

## Véase también {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
