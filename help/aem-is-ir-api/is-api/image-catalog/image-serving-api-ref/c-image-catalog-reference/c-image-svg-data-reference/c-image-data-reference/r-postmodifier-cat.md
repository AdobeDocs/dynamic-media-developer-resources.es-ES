---
description: Cadena de modificador de solicitud Postfix. Ninguno o más comandos del servicio de imágenes separados por caracteres "&".
solution: Experience Manager
title: PostModifier
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7d6c9408-1f09-464d-8a69-eabdf7c0117d
TQID: 'https://experienceleague.adobe.com/hPHoHlBkRN-eXFvLzZ2LpWhmtiT4lGyehTvwFw9ItJo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 128
ht-degree: 3%

---

# PostModifier{#postmodifier}

Cadena de modificador de solicitud Postfix. Ninguno o más comandos del servicio de imágenes separados por caracteres &quot;&amp;&quot;.

Los comandos de este campo siempre anulan los comandos de la solicitud HTTP y de `catalog::Modifier`.

`catalog::PostModifier` resulta útil si determinadas imágenes requieren una configuración especial que normalmente se controla desde la dirección URL, como `qlt=` o `resmode=`. `catalog::Modifier` debe usarse para configurar la mayoría de los comandos IS en el catálogo de imágenes.

Las macros están permitidas en `catalog::PostModifier`, siempre y cuando se definan en el mismo catálogo o en el catálogo predeterminado. También se pueden utilizar variables personalizadas.

>[!NOTE]
>
>Si una solicitud involucra varias capas, solo se aplica el contenido de `catalog::PostModifier` de la capa 0. Se omite `catalog::PostModifier` de todas las demás capas.

## Propiedades {#section-6d5b0462ba1245b8ac3ddfd15c059f42}

Cadena de texto. Opcional.

## Predeterminado {#section-8c83bce7f6c846d48fbe8fd30bedf5d5}

Ninguno.

## Véase también {#section-8942f70e40f44dc48df51b4d8d0a7cde}

[catalog::Modificador](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834)
