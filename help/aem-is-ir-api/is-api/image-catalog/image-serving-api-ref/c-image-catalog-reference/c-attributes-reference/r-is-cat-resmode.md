---
description: Modo de remuestreo predeterminado. Especifica los atributos predeterminados de remuestreo e interpolación que se utilizarán para escalar datos de imagen.
seo-description: Modo de remuestreo predeterminado. Especifica los atributos predeterminados de remuestreo e interpolación que se utilizarán para escalar datos de imagen.
seo-title: ResMode
solution: Experience Manager
title: ResMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 14d184bd-6664-4f8f-b551-a92cb92a0d84
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

---


# ResMode{#resmode}

Modo de remuestreo predeterminado. Especifica los atributos predeterminados de remuestreo e interpolación que se utilizarán para escalar datos de imagen.

Se utiliza cuando `resMode=` no se especifica en una solicitud.

## Propiedades {#section-493f900be522486f97710cebdc4460c2}

Enum. Se establece en 2 para `bilin`, 3 para `bicub` o 4 para el modo de interpolación `sharp2` (consulte ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` para obtener más información). `sharp` (1) está en desuso. Utilice `sharp2` (4) en su lugar para obtener los mejores resultados.

## Predeterminado {#section-35f980e745fc4d79a2621e8abacc724d}

Se hereda de `default::ResMode` si no está definida o si está vacía.

## Véase también {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
