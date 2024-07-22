---
title: ClientAddressFilter
description: Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o rangos de direcciones.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# ClientAddressFilter{#clientaddressfilter}

Filtro de dirección IP del cliente. Permite especificar una o más direcciones IP o rangos de direcciones.

Cuando se especifica, se rechazan las solicitudes a este catálogo de imágenes que se originan desde un cliente con una dirección IP no incluida. `localhost` siempre forma parte implícitamente de la definición de `ClientAddressFilter`, aunque no se haya especificado explícitamente. Las solicitudes procedentes de `localhost` nunca se rechazan, independientemente de la especificación `ClientAddressFilter`.

## Propiedades {#section-21a2992f108d42fb8660c0d65aa61e13}

Lista separada por comas de direcciones IP con máscaras de red opcionales ([se usa la notación CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* dirección IP en formato *[!DNL ddd.ddd.ddd.ddd]*

* *[!DNL netmask]* máscara de red (0...32)

Este atributo se omite cuando se aplica una regla de preprocesamiento con un elemento `<addressfilter>`.

## Predeterminado {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Se hereda de `default::AddressFilter` si no se ha definido o está vacío.

## Ejemplos {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Sin restricciones de acceso: `0.0.0.0/0`
* Conceder acceso a todas las direcciones que empiecen por `192: 192.0.0.0/8`
* Conceder acceso a los hosts 512 con direcciones entre `192.168.12.0` y `192.168.13.255: 192.168.12.0/23`

* Conceder acceso a una sola dirección IP: `192.168.2.117` o `192.168.2.117/32`

## Véase también {#section-6198780c7b3045aabd211eefb38bc565}

[addressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
