---
description: Elemento de filtro de dirección. Opcional en elementos <rule>. Anula el atributo ClientAddressFilter cuando se aplica la regla.
seo-description: Elemento de filtro de dirección. Opcional en elementos <rule>. Anula el atributo ClientAddressFilter cuando se aplica la regla.
seo-title: direcsfilter
solution: Experience Manager
title: direcsfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# addressfilter{#addressfilter}

Elemento de filtro de dirección. Opcional en elementos `<rule>`. Anula el atributo::ClientAddressFilter cuando se aplica la regla.

## Atributos {#section-e7a0960f7f0045da91de37824aa4aeaa}

Ninguno.

## Datos {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lista separada por comas de las direcciones IP. Cada dirección individual puede incluir un sufijo opcional de máscara de red para permitir la especificación de intervalos de direcciones IP. Consulte ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` para obtener más información.

## Descripción {#section-099b7839c4be40c68cbff29dad14e7d5}

El acceso a este catálogo de imágenes puede restringirse a una o varias direcciones IP específicas especificándolas en un elemento `<addressfilter>`. Se devuelve un error de &quot;solicitud rechazada&quot; al cliente si no coincide la dirección IP del cliente.

El acceso no está restringido si `<addressfilter>` está vacío o no se ha especificado.

Si el `<expression>` del elemento `<rule>` está ausente o vacío, el `<addressfilter>` se aplica a todas las solicitudes.

`localhost` siempre forma parte implícitamente de la  `ClientAddressFilter` definición, aunque no se especifique explícitamente. Las solicitudes provenientes de `localhost` nunca se rechazan, independientemente de la especificación `ClientAddressFilter`.

## SeeaTambién {#section-02056065e0c042e1b155b2f3e5b84ef7}

[atributo::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
