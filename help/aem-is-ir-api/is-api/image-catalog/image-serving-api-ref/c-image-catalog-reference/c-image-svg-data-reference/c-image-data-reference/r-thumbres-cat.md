---
description: Resolución de miniatura. Especifica la resolución del objeto para la imagen en miniatura.
seo-description: Resolución de miniatura. Especifica la resolución del objeto para la imagen en miniatura.
seo-title: ThumbRes
solution: Experience Manager
title: ThumbRes
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 10bbad31-a0fd-4ed3-b708-87822777acdd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# ThumbRes{#thumbres}

Resolución de miniatura. Especifica la resolución del objeto para la imagen en miniatura.

Solo se usa si `catalog::ThumbType=3`.

## Propiedades {#section-ee5cae086a3d4875805fa8a08756a586}

Valor de número real bueno que 0. Debe tener las mismas unidades que `catalog::Resolution`.

## Predeterminado {#section-f0e453fc8a7c451db21961c084eecabd}

`attribute::ThumbRes` se utiliza si el campo no está presente, si el valor es 0 o si el campo está vacío.

## Véase también {#section-eb716bf647614db083020fe8ce453751}

[catálogo:ThumbType](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-thumbtype-cat.md#reference-41149ddffc8749cba2f8d9c8e2611e03) ,  [catálogo::Resolution](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1),  [atributo::ThumbRes](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-thumbres.md#reference-ac36cbbd0c8c433ebf7f515e54846501),  [req=tmb](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76), Escalado de  [miniaturas](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-notes-on-server-behavior/r-thumbnail-scaling.md#reference-0f71817f721d4913b34816758d69b07f)
