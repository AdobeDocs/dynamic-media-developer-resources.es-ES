---
title: ResMode
description: Modo de remuestreo predeterminado. Especifica los atributos de remuestreo e interpolación predeterminados que se utilizarán para escalar datos de imagen.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a604e61e-be38-4819-b5c3-a79843c1678f
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# ResMode{#resmode}

Modo de remuestreo predeterminado. Especifica los atributos de remuestreo e interpolación predeterminados que se utilizarán para escalar datos de imagen.

Se usa cuando `resMode=` no se ha especificado en una solicitud.

## Propiedades {#section-493f900be522486f97710cebdc4460c2}

Enum. Configure en 2 para `bilin`, 3 para `bicub`o 4 para `sharp2` modo de interpolación (consulte [resMode=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-resmode.md) para obtener más información). `sharp` (1) está en desuso. Uso `sharp2` (4) para obtener los mejores resultados.

## Predeterminado {#section-35f980e745fc4d79a2621e8abacc724d}

Heredado de `default::ResMode` si no está definida o si está vacío.

## Véase también {#section-6c86322b52e9418093d189e9b29dbb75}

[resMode=](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
