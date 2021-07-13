---
description: Image Rendering aplica materiales a grupos u objetos en viñetas.
solution: Experience Manager
title: Materiales
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3fe5445e-de85-4f0c-8008-7716226ff966
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# Materiales{#materials}

Image Rendering aplica materiales a grupos u objetos en viñetas.

Un material consiste en un conjunto de *atributos*. Algunos atributos son obligatorios para ciertos materiales, otros son opcionales y algunos se ignoran si están presentes. Muchos atributos tienen valores predeterminados. No todos los materiales se pueden aplicar a todos los objetos (por ejemplo, un material de armario no se puede aplicar a un sofá).

El servidor ignora todos los atributos que se producen dentro de un segmento de especificación de material (MSS) pero que no aparecen enumerados anteriormente ni en las tablas de material específicas que se muestran a continuación.

En las tablas siguientes se enumeran los atributos básicos del material. IR admite atributos adicionales para controlar [efectos de procesamiento avanzados](../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-advanced-render-effects/c-ir-advanced-render-effects.md#concept-bf8b6d8460244b9cacc7f4a3df4c5281).

A menos que se indique lo contrario, todos los atributos de material son opcionales, con los valores predeterminados adecuados.

* [Colores sólidos](r-ir-solid-colors.md)
* [Texturas repetibles](r-ir-repeatable-textures.md)
* [Bordes de muro](r-ir-wall-borders.md)
* [Decretos](r-ir-decals.md)
* [Armarios](r-ir-cabinets.md)
* [Cubiertas de ventana](r-ir-window-coverings.md)
