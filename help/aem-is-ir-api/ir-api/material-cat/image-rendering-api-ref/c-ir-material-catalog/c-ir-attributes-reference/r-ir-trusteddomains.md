---
description: Dominios web de la aplicación Flash. Las aplicaciones Adobe Flash pueden requerir acceso a las propiedades de las imágenes entregadas en formato swf. El archivo swf debe conceder acceso explícitamente registrando el nombre de los dominios de aplicación en los que confía.
seo-description: Dominios web de la aplicación Flash. Las aplicaciones Adobe Flash pueden requerir acceso a las propiedades de las imágenes entregadas en formato swf. El archivo swf debe conceder acceso explícitamente registrando el nombre de los dominios de aplicación en los que confía.
seo-title: TrustedDomains *
solution: Experience Manager
title: TrustedDomains *
topic: Scene7 Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TrustedDomains *{#trusteddomains}

Dominios web de la aplicación Flash. Las aplicaciones Adobe Flash pueden requerir acceso a las propiedades de las imágenes entregadas en formato swf. El archivo swf debe conceder acceso explícitamente registrando el nombre de los dominios de aplicación en los que confía.

## Propiedades {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Cadena que contiene una lista separada por comas de nombres de dominio web. Si están vacías, las aplicaciones deben estar en el mismo dominio que el procesamiento de imágenes para poder acceder a las propiedades de las imágenes en las respuestas con [!DNL swf]formato.

## Predeterminado {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Se hereda de `default::TrustedDomains` si no está presente.

## Véase también {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [atributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
