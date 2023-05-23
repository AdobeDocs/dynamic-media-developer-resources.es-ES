---
description: Ruta del archivo de datos. Ruta relativa y nombre de los archivos de datos que no son imágenes asociados a esta imagen.
solution: Experience Manager
title: AuxPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55f82596-72f0-48c4-9b3a-f10ea5f610f1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 3%

---

# AuxPath{#auxpath}

Ruta del archivo de datos. Ruta relativa y nombre de los archivos de datos que no son imágenes asociados a esta imagen.

El servidor combina este valor con attribute::RootPath para crear la ruta de archivo real. También puede ser una ruta de archivo absoluta.

Se utiliza para especificar un fichero de estilo de armario para un material de armario o un fichero de estilo de recubrimiento de ventana para un material de recubrimiento de ventana. Dejar vacío para el resto de materiales.

## Propiedades {#section-4268350054b7421da0ce0327f0731a52}

Valor de cadena de texto. Si se especifica, debe ser una ruta de archivo relativa o absoluta válida. Necesario para materiales de gabinete y materiales de recubrimiento de ventanas. Debe estar vacío para el resto de materiales.

## Predeterminado {#section-287005c2d8e948fa958f69ba7b90b437}

Ninguno.

## Véase también {#section-e1f7a61c00d04a80af28e2e67481ab92}

[attribute::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) , [catalog::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
