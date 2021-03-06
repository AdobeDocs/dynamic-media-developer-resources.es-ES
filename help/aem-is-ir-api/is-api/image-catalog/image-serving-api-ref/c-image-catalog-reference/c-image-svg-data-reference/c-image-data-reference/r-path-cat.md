---
description: Ruta del archivo de imagen.
solution: Experience Manager
title: Ruta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 4%

---

# Ruta{#path}

Ruta del archivo de imagen.

Ruta relativa o absoluta y nombre del archivo de imagen de origen asociado con este registro de catálogo. El servidor utiliza las reglas de resolución de rutas descritas en Administración de datos de origen para encontrar el archivo de datos.

## Propiedades {#path-properties}

Cadena de texto. Necesario para registros de imagen, puede estar vacío para registros de plantilla. Si se especifica, debe ser una ruta de archivo válida relativa o absoluta del servidor de imágenes. attribute::DefaultExt se anexa si no hay ningún sufijo de archivo presente.

## Formatos de archivo de imagen compatibles {#path-supported-image-file-formats}

Consulte la descripción de la utilidad Conversor de imágenes (IC) para obtener una lista completa de los formatos de archivo admitidos.

Las aplicaciones que requieran datos de imagen en varias resoluciones diferentes tendrán un mejor rendimiento al usar el formato de varias resoluciones TIFF (PTIFF) piramidal de Dynamic Media. La utilidad IC se utiliza para crear imágenes PTIFF a partir de cualquier formato de imagen admitido.

## Predeterminado {#path-default}

Ninguno.

## Véase también {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) ,  [atributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) ,  [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
