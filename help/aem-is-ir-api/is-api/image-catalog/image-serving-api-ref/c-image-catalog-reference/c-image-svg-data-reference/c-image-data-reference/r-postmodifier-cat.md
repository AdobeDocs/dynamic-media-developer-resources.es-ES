---
description: Cadena del modificador de solicitud postfix. Ninguno o varios comandos de servicio de imágenes separados por caracteres "&".
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 4%

---

# PostModifier{#postmodifier}

Cadena del modificador de solicitud postfix. Ninguno o varios comandos de servicio de imágenes separados por caracteres &quot;&amp;&quot;.

Los comandos de este campo siempre anulan los comandos de la solicitud HTTP y de `catalog::Modifier`.

`catalog::PostModifier` es útil si determinadas imágenes requieren ajustes especiales que normalmente se controlan desde la dirección URL, como  `qlt=` o  `resmode=`. `catalog::Modifier` debe utilizarse para configurar la mayoría de los comandos IS en el catálogo de imágenes.

Las macros están permitidas en `catalog::PostModifier`, siempre que estén definidas en el mismo catálogo o en el catálogo predeterminado. También se pueden usar variables personalizadas.

>[!NOTE]
>
>Si una solicitud implica varias capas, solo se aplica el contenido de `catalog::PostModifier` de la capa 0. `catalog::PostModifier` del resto de capas se ignorará.

## Propiedades {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Cadena de texto. Opcional.

## Predeterminado {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Ninguno.

## Véase también {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catálogo::Modifier](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
