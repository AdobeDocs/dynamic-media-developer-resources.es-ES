---
title: Id
description: Normalmente, un identificador corto y único, como un número SKU, posiblemente con algún tipo de sufijo, como si un SKU tiene varias imágenes o variaciones específicas de la configuración regional.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 818649dd-bcb7-4ff5-9308-6b5dc06f66e1
source-git-commit: c1a4dad7888d31e0b78f0fc5091700ad8104e685
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 3%

---

# Id{#id}

Normalmente, un identificador corto y único, como un número SKU, posiblemente con algún tipo de sufijo, como si un SKU tiene varias imágenes o variaciones específicas de la configuración regional. También puede ser una cadena más compleja que parece más una ruta de archivo, para admitir una fácil reconfiguración de sitios web con el servicio de imágenes.

>[!NOTE]
>
>Las tablas de imagen y SVG se combinan en una sola tabla cuando se carga el catálogo de imágenes. Los valores de ID deben ser únicos en ambas tablas. El registro SVG se descarta si la tabla de imágenes contiene un registro con el mismo valor de ID. El contenido estático se administra con una tabla independiente; los elementos de contenido estático y los elementos de imagen/SVG pueden tener los mismos valores de ID.

## Propiedades {#section-874a6853f67b4b229341ca76682884ae}

Cadena de texto. Obligatorio. Identificador de registro para la imagen/SVG o la tabla de datos de contenido estático. Cada `catalog::Id` el valor dentro de este catálogo de imágenes/catálogo de SVG o dentro de este catálogo de contenido estático debe ser único y no debe incluir los caracteres &quot;,&quot;.

## Predeterminado {#section-a26e7d83a5ee44b5918baef82ee48e14}

Ninguno.

## Véase también {#section-a258d818487d4ee6b7a99a65d18471a9}

[attribute::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
