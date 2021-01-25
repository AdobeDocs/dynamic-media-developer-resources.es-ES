---
description: Id
solution: Experience Manager
title: Id
topic: Dynamic Media Image Serving - Image Rendering API
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 5%

---


# Id{#id}

Normalmente, un identificador corto y único, como un número de SKU, posiblemente con algún tipo de sufijo, como si un SKU tiene varias imágenes o tiene variaciones de configuración regional específica. También puede ser una cadena más compleja que se asemeje más a una ruta de archivo, para facilitar la remodelación de los sitios web con el servicio de imágenes.

>[!NOTE]
>
>Las tablas de imagen y SVG se combinan en una sola tabla cuando se carga el catálogo de imágenes. Los valores de ID deben ser únicos en ambas tablas. El registro SVG se descarta si la tabla de imágenes contiene un registro con el mismo valor de ID. El contenido estático se administra con una tabla independiente; los elementos de contenido estático y los elementos de imagen/SVG pueden tener los mismos valores de Id.

## Propiedades {#section-874a6853f67b4b229341ca76682884ae}

Cadena de texto. Obligatorio. Identificador de registro de la tabla de datos de contenido estático o de imagen/SVG. Cada valor `catalog::Id` de este catálogo de imágenes/catálogo SVG o de este catálogo de contenido estático debe ser único y no debe incluir los caracteres &#39;,&#39;.

## Predeterminado {#section-a26e7d83a5ee44b5918baef82ee48e14}

Ninguno.

## Véase también {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
