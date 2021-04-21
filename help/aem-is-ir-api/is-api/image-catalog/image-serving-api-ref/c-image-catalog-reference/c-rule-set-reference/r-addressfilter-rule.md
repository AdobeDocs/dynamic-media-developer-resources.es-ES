---
description: Elemento de filtro de dirección. Opcional en elementos <rule> y <pathrule> .
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 4%

---


# addressfilter{#addressfilter}

Elemento de filtro de dirección. Opcional en elementos `<rule>` y `<pathrule>` .

Anula `attribute::ClientAddressFilter` cuando se aplica la regla.

## Atributos {#section-31e9ad29e9934933ac154bccbc729172}

Ninguno.

## Datos {#section-c762bdfe425140d689ea5abf25e9a48a}

Lista de direcciones IP separadas por comas. Cada dirección individual puede incluir un sufijo de máscara de red opcional para permitir la especificación de intervalos de direcciones IP. Consulte `attribute::ClientAddressFilter` para obtener más información.

## Descripción {#section-d561b2485e004ef8a2085997d0f4bca6}

El acceso a este catálogo de imágenes se puede restringir a una o más direcciones IP de cliente específicas especificándolas en un elemento `<addressfilter>`. Se devuelve al cliente un error &quot;solicitud rechazada&quot; si la dirección IP del cliente no coincide.

El acceso no está restringido si `<addressfilter>` está vacío o no se ha especificado.

Si el `<expression>` del elemento `<rule>` está ausente o vacío, el `<addressfilter>` se aplica a todas las solicitudes.

## Véase también {#section-6f51ec2218d9450bb7642f9fdad1988a}

[atributo::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
