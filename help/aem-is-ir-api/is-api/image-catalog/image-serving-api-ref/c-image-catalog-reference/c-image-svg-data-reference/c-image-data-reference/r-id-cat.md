---
description: Identificador de registro del catálogo
solution: Experience Manager
title: Id
uuid: 9803d754-1f94-4e5d-9a40-3936676c0035
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 7%

---


# Id {#id}

Valor clave de índice mediante el cual Platform Server busca los registros del archivo de datos de imagen.

Normalmente, un identificador de imagen corto y único, como un número SKU, posiblemente con algún tipo de sufijo de imagen, si un SKU tiene varias imágenes. Puede ser también una cadena más compleja que se parezca más a una ruta de archivo, para admitir una fácil adaptación retro de los sitios web con Image Serving.

## Propiedades {#id-properties}

Cadena de texto. Obligatorio. Clave de índice principal para la tabla de datos de imagen. Cada valor de catálogo::Id debe ser único dentro de la tabla.

## Predeterminado {#id-default}

Ninguno.

## Véase también {#id-seealso}

[atributo::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)