---
description: Tamaño de miniatura predeterminado. Se utiliza en lugar del atributo DefaultPix para solicitudes de miniaturas (req=tmb).
seo-description: Tamaño de miniatura predeterminado. Se utiliza en lugar del atributo DefaultPix para solicitudes de miniaturas (req=tmb).
seo-title: DefaultThumbPix
solution: Experience Manager
title: DefaultThumbPix
uuid: 7b310aab-6d38-45f3-a3e7-b074a8e7a795
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 3%

---


# DefaultThumbPix{#defaultthumbpix}

Tamaño de miniatura predeterminado. Se utiliza en lugar del atributo::DefaultPix para solicitudes de miniatura (req=tmb).

El servidor restringe el tamaño de las imágenes de respuesta para que no superen esta anchura y altura si una solicitud de miniatura ( `req=tmb`) no especifica el tamaño de vista de forma explícita mediante `wid=`, `hei=` o `scl=`.

## Propiedades {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Dos números enteros, 0 o más grandes, separados por coma. Anchura y altura en píxeles. Puede que ambos valores estén establecidos en 0 para mantenerlos sin restricciones.

No se aplica a solicitudes anidadas/incrustadas.

## Predeterminado {#section-2c4a4f14540449638822913513170ff1}

Se hereda de `default::DefaultThumbPix` si no está definido o si está vacío.

## Véase también {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
