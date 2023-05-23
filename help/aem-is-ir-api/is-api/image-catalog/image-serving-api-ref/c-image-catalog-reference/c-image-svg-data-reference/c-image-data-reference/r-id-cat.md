---
description: Identificador de registro de catálogo
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# Id {#id}

Valor de clave de índice según el cual el usuario busca los registros del archivo de datos de imagen [!DNL Platform Server].

Normalmente, un identificador de imagen corto y único, como un número SKU, posiblemente con algún tipo de sufijo de imagen, si un SKU tiene varias imágenes. También puede ser una cadena más compleja que se asemeje más a una ruta de archivo, para admitir un ajuste retro sencillo de los sitios web con el servicio de imágenes.

## Propiedades {#id-properties}

Cadena de texto. Obligatorio. Clave de índice principal para la tabla de datos de imagen. Cada valor catalog::Id debe ser único dentro de la tabla.

## Predeterminado {#id-default}

Ninguno.

## Véase también {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
