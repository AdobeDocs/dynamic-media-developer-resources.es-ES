---
description: Elemento de filtro de dirección. Opcional en los elementos <rule> y <pathrule>.
seo-description: Elemento de filtro de dirección. Opcional en los elementos <rule> y <pathrule>.
seo-title: direcsfilter
solution: Experience Manager
title: direcsfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---


# addressfilter{#addressfilter}

Elemento de filtro de dirección. Opcional en elementos `<rule>` y `<pathrule>`.

Anula `attribute::ClientAddressFilter` cuando se aplica la regla.

## Atributos {#section-31e9ad29e9934933ac154bccbc729172}

Ninguno.

## Datos {#section-c762bdfe425140d689ea5abf25e9a48a}

Lista separada por comas de las direcciones IP. Cada dirección individual puede incluir un sufijo opcional de máscara de red para permitir la especificación de intervalos de direcciones IP. Consulte `attribute::ClientAddressFilter` para obtener más información.

## Descripción {#section-d561b2485e004ef8a2085997d0f4bca6}

El acceso a este catálogo de imágenes puede restringirse a una o varias direcciones IP de cliente específicas especificándolas en un elemento `<addressfilter>`. Se devuelve un error de &quot;solicitud rechazada&quot; al cliente si no coincide la dirección IP del cliente.

El acceso no está restringido si `<addressfilter>` está vacío o no se ha especificado.

Si el `<expression>` del elemento `<rule>` está ausente o vacío, el `<addressfilter>` se aplica a todas las solicitudes.

## Véase también {#section-6f51ec2218d9450bb7642f9fdad1988a}

[atributo::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
