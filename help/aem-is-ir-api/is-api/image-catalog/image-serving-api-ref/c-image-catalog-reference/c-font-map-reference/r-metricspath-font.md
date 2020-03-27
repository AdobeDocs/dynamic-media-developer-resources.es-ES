---
description: Ruta del archivo de métricas de fuentes. Ruta y nombre de un archivo de métricas de fuente, incluido el sufijo de archivo.
seo-description: Ruta del archivo de métricas de fuentes. Ruta y nombre de un archivo de métricas de fuente, incluido el sufijo de archivo.
seo-title: MetricsPath
solution: Experience Manager
title: MetricsPath
topic: Scene7 Image Serving - Image Rendering API
uuid: b59110bf-330f-4ca4-8b0a-219a61d383f7
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# MetricsPath{#metricspath}

Ruta del archivo de métricas de fuentes. Ruta y nombre de un archivo de métricas de fuente, incluido el sufijo de archivo.

Se utiliza para fuentes Adobe Type 1. Si no se especifica, el servidor intentará encontrar un archivo de métricas de fuente en la misma carpeta en la que se encuentra el archivo de fuente principal. Se producirá un error si no se encuentra un archivo de métricas de fuente requerido en el momento del procesamiento.

## Propiedades {#section-955268c581574875b05253d9e14544f3}

Cadena de texto. Opcional para archivos de Adobe Type 1. Debe estar vacía o ser una ruta de acceso de archivo válida del servidor de imágenes, ya sea absoluta o relativa a `attribute::RootPath`.

## Predeterminado {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Ninguno.

## Véase también {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
