---
description: Cadena del modificador de solicitud de prefijo. Ninguno o varios comandos de servicio de imágenes separados por caracteres "&".
seo-description: Cadena del modificador de solicitud de prefijo. Ninguno o varios comandos de servicio de imágenes separados por caracteres "&".
seo-title: Modificador
solution: Experience Manager
title: Modificador
uuid: eb17d115-22ec-4b1b-9039-9bd2bc256f48
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# Modificador{#modifier}

Cadena del modificador de solicitud de prefijo. Ninguno o varios comandos de servicio de imágenes separados por caracteres &quot;&amp;&quot;.

Se utiliza para modificar imágenes de forma persistente y almacenar el cuerpo de las plantillas.

Los comandos de este campo se anulan por los mismos comandos de la solicitud o plantilla desde la que se hace referencia a este registro y por los comandos de `catalog::PostModifier`

Las macros están permitidas en `catalog::Modifier`, siempre que estén definidas en el mismo catálogo o en el catálogo predeterminado. También se pueden usar variables personalizadas.

## Propiedades {#section-6674388f77d644469371a17e8809c45f}

Cadena de texto. Opcional.

## Predeterminado {#section-f4ffe8b75792435c8b1040e75c5fb8a1}

Ninguno.

## Véase también {#section-7a67803d141b442180c418c1f3cff029}

[catálogo::PostModifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-postmodifier-cat.md#reference-4bc3738a812b4e7c8a180e27bfbd770b)
