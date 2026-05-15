---
title: TrustedDomains
description: Dominios web de aplicaciones Flash. Las aplicaciones Flash de Adobe pueden requerir acceso a las propiedades de las imágenes en formato swf. El archivo SWF debe conceder acceso de forma explícita mediante el registro del nombre de los dominios de aplicación en los que confía.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
TQID: 'https://experienceleague.adobe.com/GgLL3XL2Km0RvlfK3fjeD95FkgzO9OEcxNyyTZ8Y738'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Dominios web de aplicaciones Flash. Las aplicaciones Flash de Adobe pueden requerir acceso a las propiedades de las imágenes en formato swf. El archivo SWF debe conceder acceso de forma explícita mediante el registro del nombre de los dominios de aplicación en los que confía.

## Propiedades {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Cadena que contiene una lista de nombres de dominio web separados por comas. Si está vacío, las aplicaciones deben servirse desde el mismo dominio que el procesamiento de imágenes para poder acceder a las propiedades de las imágenes en respuestas con formato [!DNL swf].

## Predeterminado {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Se hereda de `default::TrustedDomains` si no está presente.

## Véase también {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [atributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
