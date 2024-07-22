---
description: Tamaño de miniatura predeterminado. Se utiliza en lugar del atributo DefaultPix para solicitudes de miniaturas (req=tmb).
solution: Experience Manager
title: DefaultThumbPix
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1413da0-a68d-4345-928f-b532991966a8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 2%

---

# DefaultThumbPix{#defaultthumbpix}

Tamaño de miniatura predeterminado. Se utiliza en lugar del atributo::DefaultPix para solicitudes de miniatura (req=tmb).

El servidor limita el tamaño de las imágenes de respuesta a esta altura y anchura máximas, a no ser que una solicitud de miniatura (`req=tmb`) especifique el tamaño explícitamente y no especifique el tamaño de vista explícitamente con `wid=`, `hei=` o `scl=`.

## Propiedades {#section-650d9b1194fb4c47a03c6809e6b4af0e}

Dos números enteros, 0 o más, separados por una coma. Ancho y alto en píxeles. Uno o ambos valores pueden establecerse en 0 para mantenerlos sin restricciones.

No se aplica a solicitudes anidadas o incrustadas.

## Predeterminado {#section-2c4a4f14540449638822913513170ff1}

Se hereda de `default::DefaultThumbPix` si no se ha definido o está vacío.

## Véase también {#section-4ad00963ffa049fcb17ad63e6bbe7ac4}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [atributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)
