---
description: Incrustar XMP metadatos. Especifica si XMP metadatos deben incluirse en la imagen de respuesta.
seo-description: Incrustar XMP metadatos. Especifica si XMP metadatos deben incluirse en la imagen de respuesta.
seo-title: xmpEmbed
solution: Experience Manager
title: xmpEmbed
uuid: c0dfd0e5-16d1-4a6e-957a-ecc276b9361a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---


# xmpEmbed{#xmpembed}

Incrustar XMP metadatos. Especifica si XMP metadatos deben incluirse en la imagen de respuesta.

`xmpEmbed=0|1`

>[!NOTE]
>
>XMP datos se pasan de la imagen de origen a la imagen de respuesta sin modificación. Esto puede provocar que se incrusten datos incorrectos en la imagen de respuesta.

## Propiedades {#section-27024c4272f44d9a8c264a0629193af2}

Atributo de solicitud. Se omite si la imagen de origen no contiene datos XMP. Solo se procesan XMP datos de la imagen de origen de `layer=0`. XMP datos de otras imágenes de capa se ignoran.

Se omite si el formato de imagen de salida no admite XMP incrustación. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten XMP incrustación.

## Predeterminado {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, para no incrustar rutas en imágenes de salida.

## Véase también {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
