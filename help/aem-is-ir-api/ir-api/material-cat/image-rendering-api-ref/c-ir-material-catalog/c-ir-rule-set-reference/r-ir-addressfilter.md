---
description: Elemento de filtro de dirección. Opcional en elementos <rule>. Anula el atributo ClientAddressFilter cuando se aplica la regla.
solution: Experience Manager
title: addressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
TQID: 'https://experienceleague.adobe.com/583zFF80AMZnaF4C-RQpRQI684hRlPRCuwoMPHGJ6eg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 150
ht-degree: 2%

---

# addressFilter{#addressfilter}

Elemento de filtro de dirección. Opcional en `<rule>` elementos. Anula attribute::ClientAddressFilter cuando se aplica la regla.

## Atributos {#section-e7a0960f7f0045da91de37824aa4aeaa}

Ninguno.

## Datos {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Lista de direcciones IP separadas por comas. Cada dirección individual puede incluir un sufijo de máscara de red opcional para permitir la especificación de intervalos de direcciones IP. Consulte [attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) para obtener más información.

## Descripción {#section-099b7839c4be40c68cbff29dad14e7d5}

El acceso a este catálogo de imágenes se puede restringir a una o más direcciones IP específicas especificándolas en un elemento `<addressfilter>`. Se devuelve un error &quot;solicitud rechazada&quot; al cliente si la dirección IP del cliente no coincide.

El acceso no está restringido si `<addressfilter>` está vacío o no se ha especificado.

Si el elemento `<expression>` del elemento `<rule>` está ausente o vacío, el elemento `<addressfilter>` se aplica a todas las solicitudes.

`localhost` siempre forma parte implícitamente de la definición de `ClientAddressFilter`, aunque no se haya especificado explícitamente. Las solicitudes procedentes de `localhost` nunca se rechazan, independientemente de la especificación `ClientAddressFilter`.

## SeeAlso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
