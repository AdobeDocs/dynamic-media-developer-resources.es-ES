---
description: Tamaño de vista predeterminado.
seo-description: Tamaño de vista predeterminado.
seo-title: DefaultPix
solution: Experience Manager
title: DefaultPix
uuid: f5d2e4f7-f9c5-40a5-8a64-67241fcb0242
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 4%

---


# DefaultPix{#defaultpix}

Tamaño de vista predeterminado.

El servidor restringe el tamaño de las imágenes de respuesta a un tamaño no mayor que este ancho y alto, si la solicitud no especifica el tamaño de vista explícitamente utilizando `wid=`, `hei=` o `scl=`.

## Propiedades {#section-c3e658cf82c540d986b118f74f0fe1b2}

Dos números enteros, 0 o más grandes, separados por coma. Anchura y altura en píxeles. Puede que ambos valores estén establecidos en 0 para mantenerlos sin restricciones.

No se aplica a solicitudes anidadas/incrustadas.

## Predeterminado {#section-b7338b2bf5114fff83b0714a57b20639}

Se hereda de `default::DefaultPix` si no está definido o si está vacío.

## Véase también {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) ,  [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [catálogo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
