---
description: Atributos de codificación JPEG predeterminados. Especifica los atributos predeterminados para las imágenes de respuesta JPEG.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: c2a7f7f9-0c2c-4421-9dbc-d5c1e936f0f1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 4%

---

# JpegQuality{#jpegquality}

Atributos de codificación JPEG predeterminados. Especifica los atributos predeterminados para las imágenes de respuesta JPEG.

## Propiedades {#section-7a75ebaf11bd4b778d287c2c5c150d0c}

Número entero y marca, separados por coma. El primer valor está en el rango 1.100 y define la calidad. El segundo valor puede ser 0 para el comportamiento normal o 1 para desactivar el muestreo descendente de cromaticidad RGB que suelen utilizar los codificadores JPEG.

## Predeterminado {#section-0b25eddd59bc434abfe38eeea9d45df3}

Se hereda de `default::JpegQuality` si no está definido o si está vacío.

## Véase también {#section-aa994afc02ea4f799655233ea32d36c9}

[qlt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-qlt.md#reference-f69ed0758c784b0385d979820546d352)
