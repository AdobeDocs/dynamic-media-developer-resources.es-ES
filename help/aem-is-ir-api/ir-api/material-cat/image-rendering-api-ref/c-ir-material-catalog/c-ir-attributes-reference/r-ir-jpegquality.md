---
description: Calidad de codificación JPEG predeterminada. Especifica la configuración de calidad predeterminada para las imágenes de respuesta codificadas con JPEG.
solution: Experience Manager
title: JpegQuality
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1a699a9e-dbf6-4e01-95aa-37a6eb83f4df
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%

---

# JpegQuality{#jpegquality}

Calidad de codificación JPEG predeterminada. Especifica la configuración de calidad predeterminada para las imágenes de respuesta codificadas con JPEG.

## Propiedades {#section-8b1ed3e0acaa4fbfa050b74c00b9d4dc}

Número entero y marca, separados por coma. El primer valor está en el rango 1.100 y define la calidad. El segundo valor puede ser 0 para el comportamiento normal, o 1 para desactivar el muestreo descendente cromático que suelen utilizar los codificadores JPEG.

## Predeterminado {#section-60900c0fb8c54444b2361513232514db}

Se hereda de `default::JpegQuality` si no está definido o si está vacío.

## Véase también {#section-8928a28fcbfe401cad4d4021a7a1c268}

[qlt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-qlt.md#reference-27b91c226eb241d0a14a29af3b3afdbd)
