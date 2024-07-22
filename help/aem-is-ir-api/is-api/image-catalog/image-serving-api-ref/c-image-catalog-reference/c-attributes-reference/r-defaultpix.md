---
description: Tamaño de vista predeterminado.
solution: Experience Manager
title: DefaultPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 709fb2a1-1b9d-421e-9a65-5f5c74390ce3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 3%

---

# DefaultPix{#defaultpix}

Tamaño de vista predeterminado.

El servidor limita el tamaño de las imágenes de respuesta a esta altura y anchura máximas, a no ser que la solicitud especifique el tamaño de vista explícitamente con `wid=`, `hei=` o `scl=`.

## Propiedades {#section-c3e658cf82c540d986b118f74f0fe1b2}

Dos números enteros, 0 o más, separados por una coma. Ancho y alto en píxeles. Uno o ambos valores pueden establecerse en 0 para mantenerlos sin restricciones.

No se aplica a solicitudes anidadas o incrustadas.

## Predeterminado {#section-b7338b2bf5114fff83b0714a57b20639}

Se hereda de `default::DefaultPix` si no se ha definido o está vacío.

## Véase también {#section-59088cd41da940e8ac0e74e2b049c6e9}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [catálogo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
