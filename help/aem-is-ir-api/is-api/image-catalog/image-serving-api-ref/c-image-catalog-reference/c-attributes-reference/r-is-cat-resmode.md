---
description: Modo de remuestreo predeterminado. Especifica los atributos de remuestreo e interpolación predeterminados que se utilizarán para escalar datos de imagen.
solution: Experience Manager
title: ResMode
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 5%

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
