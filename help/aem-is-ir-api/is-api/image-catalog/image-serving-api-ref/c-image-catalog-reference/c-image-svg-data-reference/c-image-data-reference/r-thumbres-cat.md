---
description: Resolución de miniatura. Especifica la resolución de objeto para la imagen en miniatura.
solution: Experience Manager
title: ThumbRes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1b462b7e-076d-433e-a5d2-e254396c4659
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 4%

---

# ThumbRes{#thumbres}

Resolución de miniatura. Especifica la resolución de objeto para la imagen en miniatura.

Solo se usa si `catalog::ThumbType=3`.

## Propiedades {#section-ee5cae086a3d4875805fa8a08756a586}

Valor numérico real mayor que 0. Debe tener las mismas unidades que `catalog::Resolution`.

## Predeterminado {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` se usa si el campo no está presente, si el valor es 0 o si el campo está vacío.

## Véase también {#section-eb716bf647614db083020fe8ce453751}

[catálogo:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) , [catálogo::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1), [atributo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501), [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), [Escala de miniatura](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
