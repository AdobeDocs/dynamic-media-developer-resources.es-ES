---
description: Identificador de registro de catálogo
solution: Experience Manager
title: Id
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 8%

---


# Id {#id}

Valor de clave de índice según el cual el servidor de plataforma busca los registros del archivo de datos de imagen.

Normalmente, un identificador de imagen único y corto, como un número de SKU, posiblemente con algún tipo de sufijo de imagen, si un SKU tiene varias imágenes. También puede ser una cadena más compleja que se asemeje más a una ruta de archivo, para admitir la fácil adaptación retro de los sitios web con el servicio de imágenes.

## Propiedades {#id-properties}

Cadena de texto. Obligatorio. Clave de índice principal para la tabla de datos de imagen. Cada valor de catálogo::Id debe ser único dentro de la tabla.

## Predeterminado {#id-default}

Ninguno.

## Véase también {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)