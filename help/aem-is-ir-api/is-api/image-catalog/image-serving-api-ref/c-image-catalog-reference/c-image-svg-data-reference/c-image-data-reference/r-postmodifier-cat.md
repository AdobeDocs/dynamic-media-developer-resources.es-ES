---
description: Cadena del modificador de solicitud Postfix. Ninguno o más comandos de servicio de imágenes separados por caracteres '&'.
seo-description: Cadena del modificador de solicitud Postfix. Ninguno o más comandos de servicio de imágenes separados por caracteres '&'.
seo-title: PostModifier
solution: Experience Manager
title: PostModifier
topic: Scene7 Image Serving - Image Rendering API
uuid: 8800a9b2-e9c0-498b-b4e1-37952ba7c842
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# PostModifier{#postmodifier}

Cadena del modificador de solicitud Postfix. Ninguno o más comandos de servicio de imágenes separados por caracteres &#39;&amp;&#39;.

Los comandos de este campo siempre anulan los comandos de la solicitud HTTP y de `catalog::Modifier`.

`catalog::PostModifier` resulta útil si determinadas imágenes requieren una configuración especial que normalmente se controla desde la dirección URL, como  `qlt=` o  `resmode=`. `catalog::Modifier` debe utilizarse para configurar la mayoría de los comandos IS en el catálogo de imágenes.

Las macros están permitidas en `catalog::PostModifier`, siempre que estén definidas en el mismo catálogo o en el catálogo predeterminado. También se pueden usar variables personalizadas.

>[!NOTE]
>
>Si una solicitud incluye varias capas, solo se aplica el contenido de `catalog::PostModifier` de la capa 0. `catalog::PostModifier` del resto de capas se ignora.

## Propiedades {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Cadena de texto. Opcional.

## Predeterminado {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Ninguno.

## Véase también {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catálogo::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
