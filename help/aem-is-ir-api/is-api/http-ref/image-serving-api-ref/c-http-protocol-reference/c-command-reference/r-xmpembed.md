---
title: xmpEmbed
description: Incrustar metadatos de XMP. Especifica si los metadatos de XMP deben incluirse en la imagen de respuesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 353b6ac4-1141-4f17-a3ad-ad48b321b36f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 2%

---

# xmpEmbed{#xmpembed}

Incrustar metadatos de XMP. Especifica si los metadatos de XMP deben incluirse en la imagen de respuesta.

`xmpEmbed=0|1`

>[!NOTE]
>
>Los datos de XMP se pasan de la imagen de origen a la imagen de respuesta sin realizar modificaciones. Esto puede hacer que se incrusten datos incorrectos en la imagen de respuesta.

## Propiedades {#section-27024c4272f44d9a8c264a0629193af2}

Atributo de solicitud. Se ignora si la imagen de origen no contiene datos de XMP. Solo se procesan los datos de XMP de la imagen de origen de `layer=0`. Se omiten los datos de XMP de otras imágenes de capa.

Se ignora si el formato de imagen de salida no admite la incrustación de XMP. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten la incrustación de XMP.

## Predeterminado {#section-aedbedd04d664ba184b2cfe35644b960}

`xmpEmbed=0`, para no incrustar rutas en imágenes de salida.

## Véase también {#section-0b5b7d0a19564101ba7102e667e29828}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
