---
description: Ruta raíz de datos de Source. Ruta absoluta o relativa para la carpeta raíz de los datos de origen de este catálogo de imágenes.
solution: Experience Manager
title: RootPath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 06662b27-fb10-41d0-a14c-48025d7e9137
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 2%

---

# RootPath{#rootpath}

Ruta raíz de datos de Source. Ruta absoluta o relativa para la carpeta raíz de los datos de origen de este catálogo de imágenes.

`RootPath` es un valor de cadena de texto. Consulte [Administración de datos de Source](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e) para obtener información adicional sobre las rutas de acceso raíz del servidor.

## Propiedades {#section-b41d7e0ea63143eb8034569706cad0c0}

Cadena de texto. Debe estar vacío, ser una ruta de carpeta relativa válida o una ruta absoluta válida a la que el servidor de imágenes pueda acceder.

## Predeterminado {#section-7d66ff9a3d7a4e3b834769269cb01f4f}

Se hereda de `default::RootPath` si no se define. Si se define pero está vacío, no contribuye a la ruta raíz del archivo de origen.

## Véase también {#section-6bf4ffc4987843a9a2dbe81b43076437}

[catalog::Path](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-path-cat.md) , [catalog::MaskPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-maskpath-cat.md), [ruleset::PathRule](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [Administración de datos de Source](../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-managing-content/r-source-data.md#reference-4eebd51b2db2401c90be771d3382329e)
