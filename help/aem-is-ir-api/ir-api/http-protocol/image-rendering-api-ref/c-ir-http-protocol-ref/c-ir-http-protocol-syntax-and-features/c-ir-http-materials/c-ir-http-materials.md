---
description: El procesamiento de imágenes aplica materiales a grupos u objetos en viñetas.
seo-description: El procesamiento de imágenes aplica materiales a grupos u objetos en viñetas.
seo-title: Materiales
solution: Experience Manager
title: Materiales
topic: Scene7 Image Serving - Image Rendering API
uuid: 82284e25-cfe0-4cf8-b410-b49196cc721c
translation-type: tm+mt
source-git-commit: 7721cccf3f779f258adcdcf886f7e01111e92be0

---


# Materiales{#materials}

El procesamiento de imágenes aplica materiales a grupos u objetos en viñetas.

Un material consiste en un conjunto de *atributos*. Algunos atributos son obligatorios para ciertos materiales, otros son opcionales y algunos se omiten si están presentes. Muchos atributos tienen valores predeterminados. No todos los materiales se pueden aplicar a todos los objetos (por ejemplo, no se puede aplicar un material de armario a un sofá).

El servidor ignora todos los atributos que se producen dentro de un segmento de especificación de material (MSS) pero que no se enumeran arriba ni en las tablas de material específicas a continuación.

Las siguientes tablas lista los atributos básicos del material. IR admite atributos adicionales para controlar los efectos [de procesamiento](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281)avanzados.

A menos que se indique lo contrario, todos los atributos de material son opcionales, con valores predeterminados adecuados.

* [Colores sólidos](r-ir-solid-colors.md)
* [Texturas repetibles](r-ir-repeatable-textures.md)
* [Bordes de pared](r-ir-wall-borders.md)
* [Llamadas](r-ir-decals.md)
* [Armarios](r-ir-cabinets.md)
* [Cubiertas de ventanas](r-ir-window-coverings.md)
