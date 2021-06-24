---
description: Modo de remuestreo predeterminado. Especifica los atributos de remuestreo e interpolación predeterminados que se utilizarán para escalar datos de imagen.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 6%

---

# ResMode{#resmode}

Modo de remuestreo predeterminado. Especifica los atributos de remuestreo e interpolación predeterminados que se utilizarán para escalar datos de imagen.

Se utiliza cuando `resMode=` no se especifica en una solicitud.

## Propiedades {#section-493f900be522486f97710cebdc4460c2}

Enum. Establézcalo en 2 para `bilin`, 3 para `bicub` o 4 para el modo de interpolación `sharp2` (consulte ` [resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)` para obtener más información). `sharp` (1) está en desuso. Utilice `sharp2` (4) en su lugar para obtener los mejores resultados.

## Predeterminado {#section-35f980e745fc4d79a2621e8abacc724d}

Se hereda de `default::ResMode` si no está definido o si está vacío.

## Véase también {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
