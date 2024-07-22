---
description: Cadena de modificador de solicitud de prefijo. Ninguno o más comandos del servicio de imágenes separados por caracteres "&".
solution: Experience Manager
title: Modificador
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6eef3159-c082-469b-b9dc-29acb28560d6
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---

# Modificador{#modifier}

Cadena de modificador de solicitud de prefijo. Ninguno o más comandos del servicio de imágenes separados por caracteres &quot;&amp;&quot;.

Se utiliza para modificar imágenes de forma persistente y almacenar el cuerpo de las plantillas.

Los comandos de este campo son reemplazados por los mismos comandos de la solicitud o plantilla desde la que se hace referencia a este registro, y por comandos de `catalog::PostModifier`

Las macros están permitidas en `catalog::Modifier`, siempre y cuando se definan en el mismo catálogo o en el catálogo predeterminado. También se pueden utilizar variables personalizadas.

## Propiedades {#section-6674388f77d644469371a17e8809c45f}

Cadena de texto. Opcional.

## Predeterminado {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Ninguno.

## Véase también {#section-7a67803d141b442180c418c1f3cff029}

[catalog::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
