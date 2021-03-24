---
description: dominios web de la aplicación de Flash. Las aplicaciones de Flash de Adobe pueden requerir acceso a las propiedades de las imágenes entregadas con fmt=swf o fmt=swf3.
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 3%

---


# TrustedDomains{#trusteddomains}

dominios web de la aplicación de Flash. Las aplicaciones de Flash de Adobe pueden requerir acceso a las propiedades de las imágenes entregadas con fmt=swf o fmt=swf3.

El swf debe conceder acceso explícitamente registrando el nombre de los dominios de aplicación en los que confía.

## Propiedades {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Cadena que contiene una lista de nombres de dominio web separados por comas. Si está vacío, las aplicaciones deben estar servidas desde el mismo dominio que Image Rendering para poder acceder a las propiedades de las imágenes en respuestas con formato swf.

## Predeterminado {#section-5c52ed3c7310488380f5a6f9540bf981}

Se hereda de `default::TrustedDomains` si no está presente.

## Véase también {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
