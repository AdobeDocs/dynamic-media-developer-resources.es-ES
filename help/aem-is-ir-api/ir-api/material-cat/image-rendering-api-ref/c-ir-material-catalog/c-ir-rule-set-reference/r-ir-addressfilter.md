---
description: Elemento de filtro de dirección. Opcional en elementos <rule> . Anula el atributo ClientAddressFilter cuando se aplica la regla.
seo-description: Elemento de filtro de dirección. Opcional en elementos <rule> . Anula el atributo ClientAddressFilter cuando se aplica la regla.
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# addressfilter{#addressfilter}

Elemento de filtro de dirección. Opcional en elementos `<rule>`. Overrides attribute::ClientAddressFilter cuando se aplica la regla.

## Atributos {#section-e7a0960f7f0045da91de37824aa4aeaa}

Ninguno.

## Datos {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lista de direcciones IP separadas por comas. Cada dirección individual puede incluir un sufijo de máscara de red opcional para permitir la especificación de intervalos de direcciones IP. Consulte ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` para obtener más información.

## Descripción {#section-099b7839c4be40c68cbff29dad14e7d5}

El acceso a este catálogo de imágenes se puede restringir a una o más direcciones IP específicas especificándolas en un elemento `<addressfilter>` . Se devuelve al cliente un error &quot;solicitud rechazada&quot; si la dirección IP del cliente no coincide.

El acceso no está restringido si `<addressfilter>` está vacío o no se ha especificado.

Si el `<expression>` del elemento `<rule>` está ausente o vacío, el `<addressfilter>` se aplica a todas las solicitudes.

`localhost` siempre forma parte implícita de la  `ClientAddressFilter` definición, incluso si no se especifica explícitamente. Las solicitudes procedentes de `localhost` nunca se rechazan, independientemente de la especificación `ClientAddressFilter`.

## SeeaAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[atributo::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
