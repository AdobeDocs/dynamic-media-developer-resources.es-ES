---
description: Incrustar datos de rutas. Especifica si las rutas de Photoshop del archivo de imagen de origen de la capa 0 deben incluirse en la imagen de respuesta.
seo-description: Incrustar datos de rutas. Especifica si las rutas de Photoshop del archivo de imagen de origen de la capa 0 deben incluirse en la imagen de respuesta.
seo-title: pathEmbed
solution: Experience Manager
title: pathEmbed
uuid: 93e63c7c-c091-4bb1-baff-45706fd611ea
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 2%

---


# pathEmbed{#pathembed}

Incrustar datos de rutas. Especifica si las rutas de Photoshop del archivo de imagen de origen de la capa 0 deben incluirse en la imagen de respuesta.

`pathEmbed=0|1`

## Propiedades {#section-26eb1c9e13574a0eae39f6d5b92c8995}

Atributo de solicitud. Se omite si la imagen de origen no contiene datos de rutas. Los datos de las rutas se escalan y giran como los datos de la imagen. Solo se procesan las rutas de la imagen de origen de `layer=0`; las rutas de otras imágenes de capa se ignoran.

Se omite si el formato de imagen de salida no admite la incrustación de rutas. Consulte la descripción de `fmt=` para obtener una lista de los formatos de imagen de salida que admiten la incrustación de rutas.

## Restricciones {#section-697cddb79a1542bc8457d2f4f59eec69}

Las rutas de Photoshop abiertas (rutas que no forman bucles cerrados) no son compatibles para incrustar en la imagen de respuesta en este momento.

## Predeterminado {#section-62f113ad71c04517a2741d93319a2b5d}

`pathEmbed=0`, para no incrustar rutas en imágenes de salida.

## Véase también {#section-9c20adb4147e45758ab109a543cc5862}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
