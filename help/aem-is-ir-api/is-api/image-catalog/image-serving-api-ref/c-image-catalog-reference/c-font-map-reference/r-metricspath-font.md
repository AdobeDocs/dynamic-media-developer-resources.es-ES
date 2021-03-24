---
description: Ruta del archivo de métricas de fuente. Ruta y nombre de un archivo de métricas de fuente, incluido el sufijo de archivo.
solution: Experience Manager
title: MetricsPath
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---


# MetricsPath{#metricspath}

Ruta del archivo de métricas de fuente. Ruta y nombre de un archivo de métricas de fuente, incluido el sufijo de archivo.

Se utiliza para las fuentes de Adobe Type 1. Si no se especifica, el servidor intentará encontrar un archivo de métricas de fuente en la misma carpeta en la que se encuentra el archivo de fuente principal. Se producirá un error si no se encuentra un archivo de métricas de fuente requerido en el momento del procesamiento.

## Propiedades {#section-955268c581574875b05253d9e14544f3}

Cadena de texto. Opcional para archivos de Adobe Type 1. Debe estar vacía o tener una ruta de acceso de archivo del servidor de imágenes válida, ya sea absoluta o relativa a `attribute::RootPath`.

## Predeterminado {#section-a6ffbd6879c642caa5a2fd4ed14a3a85}

Ninguno.

## Véase también {#section-a3a87a03d8e14876b7dbc2d4ad45c5ef}

[atributo::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md)
