---
description: Cadena de modificador de solicitud Postfix. Ninguno o más comandos del servicio de imágenes separados por caracteres "&".
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 3%

---

# PostModifier{#postmodifier}

Cadena de modificador de solicitud Postfix. Ninguno o más comandos del servicio de imágenes separados por caracteres &quot;&amp;&quot;.

Los comandos de este campo siempre anulan los comandos de la solicitud HTTP y en `catalog::Modifier`.

`catalog::PostModifier` es útil si determinadas imágenes requieren ajustes especiales que normalmente se controlan desde la dirección URL, como `qlt=` o `resmode=`. `catalog::Modifier` debe utilizarse para configurar la mayoría de los comandos IS en el catálogo de imágenes.

Se permiten macros en `catalog::PostModifier`, siempre que se definan en el mismo catálogo o en el catálogo predeterminado. También se pueden utilizar variables personalizadas.

>[!NOTE]
>
>Si una solicitud incluye varias capas, solo el contenido de `catalog::PostModifier` de la capa 0. `catalog::PostModifier` de todas las demás capas se omite.

## Propiedades {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Cadena de texto. Opcional.

## Predeterminado {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Ninguno.

## Véase también {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
