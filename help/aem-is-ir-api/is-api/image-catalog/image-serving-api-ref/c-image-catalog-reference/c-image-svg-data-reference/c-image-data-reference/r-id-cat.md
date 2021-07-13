---
description: Identificador de registro del catálogo
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
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
