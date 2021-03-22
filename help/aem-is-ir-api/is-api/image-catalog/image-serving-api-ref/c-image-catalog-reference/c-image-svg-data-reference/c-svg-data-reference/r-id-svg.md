---
description: Id
solution: Experience Manager
title: Id
uuid: a700472c-e1eb-4eb0-95ff-7afd4ce27931
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 5%

---


# Id{#id}

Normalmente es un identificador corto y único, como un número de SKU, posiblemente con algún tipo de sufijo, como si un SKU tiene varias imágenes o tiene variaciones específicas de la configuración regional. Puede ser también una cadena más compleja que se asemeja más a una ruta de archivo, para permitir una fácil adaptación de los sitios web con Image Serving.

>[!NOTE]
>
>Las tablas imagen y SVG se combinan en una sola tabla cuando se carga el catálogo de imágenes. Los valores de ID deben ser únicos en ambas tablas. El registro SVG se descarta si la tabla de imágenes contiene un registro con el mismo valor de ID. El contenido estático se administra con una tabla independiente; los elementos de contenido estáticos y los elementos de imagen/SVG pueden tener los mismos valores de Id.

## Propiedades {#section-874a6853f67b4b229341ca76682884ae}

Cadena de texto. Obligatorio. Identificador de registro para la tabla de datos de contenido estático o de imagen/SVG. Cada `catalog::Id` valor dentro de este catálogo de imágenes/catálogo SVG o dentro de este catálogo de contenido estático debe ser único y no debe incluir &#39;,&#39; caracteres.

## Predeterminado {#section-a26e7d83a5ee44b5918baef82ee48e14}

Ninguno.

## Véase también {#section-a258d818487d4ee6b7a99a65d18471a9}

[atributo::RootId](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md#reference-13653312925e4a08b90f99961d53f546)
