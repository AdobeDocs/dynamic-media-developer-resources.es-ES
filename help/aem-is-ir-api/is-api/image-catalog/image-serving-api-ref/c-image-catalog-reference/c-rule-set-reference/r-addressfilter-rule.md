---
description: Elemento de filtro de dirección. Opcional en los elementos <rule> y <pathrule>.
solution: Experience Manager
title: addressFilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
TQID: 'https://experienceleague.adobe.com/NkzpvFZFbluayVtCa7qBVcSgY2aU5N7R2-rZkQCZHkw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 4%

---

# addressFilter{#addressfilter}

Elemento de filtro de dirección. Opcional en `<rule>` y `<pathrule>` elementos.

Anula `attribute::ClientAddressFilter` cuando se aplica la regla.

## Atributos {#section-31e9ad29e9934933ac154bccbc729172}

Ninguno.

## Datos {#section-c762bdfe425140d689ea5abf25e9a48a}

Lista de direcciones IP separadas por comas. Cada dirección individual puede incluir un sufijo de máscara de red opcional para permitir la especificación de intervalos de direcciones IP. Consulte `attribute::ClientAddressFilter` para obtener detalles.

## Descripción {#section-d561b2485e004ef8a2085997d0f4bca6}

El acceso a este catálogo de imágenes se puede restringir a una o más direcciones IP de cliente específicas especificándolas en un elemento `<addressfilter>`. Se devuelve un error &quot;solicitud rechazada&quot; al cliente si la dirección IP del cliente no coincide.

El acceso no está restringido si `<addressfilter>` está vacío o no se ha especificado.

Si el elemento `<expression>` del elemento `<rule>` está ausente o vacío, el elemento `<addressfilter>` se aplica a todas las solicitudes.

## Véase también {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
