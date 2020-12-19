---
description: Ruta del archivo de datos. Ruta relativa y nombre para archivos de datos que no son de imagen asociados con esta imagen.
seo-description: Ruta del archivo de datos. Ruta relativa y nombre para archivos de datos que no son de imagen asociados con esta imagen.
seo-title: AuxPath
solution: Experience Manager
title: AuxPath
topic: Scene7 Image Serving - Image Rendering API
uuid: 95d28f8d-27ec-480a-a62a-7e5e8fbfb3fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# AuxPath{#auxpath}

Ruta del archivo de datos. Ruta relativa y nombre para archivos de datos que no son de imagen asociados con esta imagen.

El servidor combina este valor con attribute::RootPath para crear la ruta de acceso real del archivo. También puede ser una ruta absoluta del archivo.

Se utiliza para especificar un fichero de estilo archivador para un material archivador o un fichero de estilo de revestimiento de ventana para un material de revestimiento de ventana. Deje vacío para todos los demás materiales.

## Propiedades {#section-4268350054b7421da0ce0327f0731a52}

Valor de cadena de texto. Si se especifica, debe ser una ruta de archivo absoluta o relativa válida. Necesario para materiales de gabinete y revestimiento de ventanas. Debe estar vacío para todos los demás materiales.

## Predeterminado {#section-287005c2d8e948fa958f69ba7b90b437}

Ninguno.

## Véase también {#section-e1f7a61c00d04a80af28e2e67481ab92}

[atributo::RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3) ,  [catálogo::Path](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590),  [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
