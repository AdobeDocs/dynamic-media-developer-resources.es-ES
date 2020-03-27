---
description: Ruta del archivo de imagen.
solution: Experience Manager
title: Ruta
topic: Scene7 Image Serving - Image Rendering API
uuid: 0fca88bb-de00-4eff-83ad-c0f5e3b8ece0
translation-type: tm+mt
source-git-commit: 7b837020deef888a038a074d0aa826d43e60aeb6

---


# Ruta{#path}

Ruta del archivo de imagen.

Ruta relativa o absoluta y nombre del archivo de imagen de origen asociado a este registro de catálogo. El servidor utiliza las reglas de resolución de rutas descritas en Administración de datos de origen para encontrar el archivo de datos.

## Propiedades {#path-properties}

Cadena de texto. Necesario para los registros de imagen, puede estar vacío para los registros de plantilla. Si se especifica, debe ser una ruta de acceso de archivo relativa o absoluta del servidor de imágenes válida. attribute::DefaultExt se anexa si no hay ningún sufijo de archivo presente.

## Formatos de archivo de imagen admitidos {#path-supported-image-file-formats}

Consulte la descripción de la utilidad Image Converter (IC) para obtener una lista completa de los formatos de archivo admitidos.

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionarán mejor al utilizar el formato de varias resoluciones TIFF (PTIFF) piramidal de Dynamic Media. La utilidad IC se utiliza para crear imágenes PTIFF a partir de cualquier formato de imagen admitido.

## Predeterminado {#path-default}

Ninguno.

## Véase también {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [atributo::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->