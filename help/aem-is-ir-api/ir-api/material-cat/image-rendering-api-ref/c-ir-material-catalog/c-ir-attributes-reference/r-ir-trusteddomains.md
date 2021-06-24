---
description: dominios web de la aplicación de Flash. Las aplicaciones de Flash de Adobe pueden requerir acceso a las propiedades de las imágenes entregadas en formato swf. El swf debe conceder acceso explícitamente registrando el nombre de los dominios de aplicación en los que confía.
solution: Experience Manager
title: Dominios de confianza *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# Dominios de confianza *{#trusteddomains}

dominios web de la aplicación de Flash. Las aplicaciones de Flash de Adobe pueden requerir acceso a las propiedades de las imágenes entregadas en formato swf. El swf debe conceder acceso explícitamente registrando el nombre de los dominios de aplicación en los que confía.

## Propiedades {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Cadena que contiene una lista de nombres de dominio web separados por comas. Si está vacío, las aplicaciones deben estar servidas desde el mismo dominio que Image Rendering para poder acceder a las propiedades de las imágenes en respuestas con formato [!DNL swf].

## Predeterminado {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

Se hereda de `default::TrustedDomains` si no está presente.

## Véase también {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [atributo::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
