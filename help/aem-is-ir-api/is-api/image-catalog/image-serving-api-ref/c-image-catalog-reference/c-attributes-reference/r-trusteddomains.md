---
description: Dominios web de la aplicación Flash. Las aplicaciones Adobe Flash pueden requerir acceso a las propiedades de las imágenes entregadas con fmt=swf o fmt=swf3.
seo-description: Dominios web de la aplicación Flash. Las aplicaciones Adobe Flash pueden requerir acceso a las propiedades de las imágenes entregadas con fmt=swf o fmt=swf3.
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
topic: Scene7 Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TrustedDomains{#trusteddomains}

Dominios web de la aplicación Flash. Las aplicaciones Adobe Flash pueden requerir acceso a las propiedades de las imágenes entregadas con fmt=swf o fmt=swf3.

El swf debe conceder acceso explícitamente registrando el nombre de los dominios de aplicación en los que confía.

## Propiedades {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Cadena que contiene una lista separada por comas de nombres de dominio web. Si están vacías, las aplicaciones deben estar en el mismo dominio que el procesamiento de imágenes para poder acceder a las propiedades de las imágenes en las respuestas con formato swf.

## Predeterminado {#section-5c52ed3c7310488380f5a6f9540bf981}

Se hereda de `default::TrustedDomains` si no está presente.

## Véase también {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
