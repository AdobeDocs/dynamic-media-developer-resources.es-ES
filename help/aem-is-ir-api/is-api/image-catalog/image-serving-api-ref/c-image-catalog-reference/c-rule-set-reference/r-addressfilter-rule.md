---
description: Elemento de filtro de dirección. Opcional en <rule> y <pathrule> elementos.
solution: Experience Manager
title: addressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 5%

---

# addressFilter{#addressfilter}

Elemento de filtro de dirección. Opcional en `<rule>` y `<pathrule>` elementos.

Invalidaciones `attribute::ClientAddressFilter` cuando se aplique la regla.

## Atributos {#section-31e9ad29e9934933ac154bccbc729172}

Ninguno.

## Datos {#section-c762bdfe425140d689ea5abf25e9a48a}

Lista de direcciones IP separadas por comas. Cada dirección individual puede incluir un sufijo de máscara de red opcional para permitir la especificación de intervalos de direcciones IP. Consulte `attribute::ClientAddressFilter` para obtener más información.

## Descripción {#section-d561b2485e004ef8a2085997d0f4bca6}

El acceso a este catálogo de imágenes se puede restringir a una o más direcciones IP de cliente específicas especificándolas en un `<addressfilter>` Elemento. Se devuelve un error &quot;solicitud rechazada&quot; al cliente si la dirección IP del cliente no coincide.

El acceso no está restringido si `<addressfilter>` está vacío o no se ha especificado.

Si la variable `<expression>` en el `<rule>` está ausente o vacío, el elemento `<addressfilter>` se aplica a todas las solicitudes.

## Véase también {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
