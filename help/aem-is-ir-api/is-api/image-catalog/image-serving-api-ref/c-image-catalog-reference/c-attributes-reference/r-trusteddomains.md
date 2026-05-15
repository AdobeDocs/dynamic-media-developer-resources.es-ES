---
description: Dominios web de aplicaciones Flash. Las aplicaciones Flash de Adobe pueden requerir acceso a las propiedades de las imágenes suministradas con fmt=swf o fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
TQID: 'https://experienceleague.adobe.com/xGn-usdBOB3NjRaffq6w0SJDlDerpeQJHGhKej-L3Cw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 107
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Dominios web de aplicaciones Flash. Las aplicaciones Flash de Adobe pueden requerir acceso a las propiedades de las imágenes suministradas con fmt=swf o fmt=swf3.

El archivo SWF debe conceder acceso de forma explícita mediante el registro del nombre de los dominios de aplicación en los que confía.

## Propiedades {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Cadena que contiene una lista de nombres de dominio web separados por comas. Si está vacío, las aplicaciones deben servirse desde el mismo dominio que el procesamiento de imágenes para poder acceder a las propiedades de las imágenes en respuestas con formato swf.

## Predeterminado {#section-5c52ed3c7310488380f5a6f9540bf981}

Se hereda de `default::TrustedDomains` si no está presente.

## Véase también {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
