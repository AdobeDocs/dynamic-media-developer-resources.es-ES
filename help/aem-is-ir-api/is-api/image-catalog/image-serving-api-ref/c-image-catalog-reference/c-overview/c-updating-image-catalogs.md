---
description: El servidor supervisa continuamente la carpeta del catálogo y vuelve a cargar automáticamente un catálogo de imágenes, incluidos los archivos de datos del catálogo asociados, cuando detecta que se ha cambiado el archivo de atributos del catálogo principal.
solution: Experience Manager
title: Actualización de catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Actualizando catálogos de imágenes{#updating-image-catalogs}

El servidor supervisa continuamente la carpeta del catálogo y vuelve a cargar automáticamente un catálogo de imágenes, incluidos los archivos de datos del catálogo asociados, cuando detecta que se ha cambiado el archivo de atributos del catálogo principal.

Para actualizar los catálogos de imágenes en el servidor, en primer lugar reemplace todos los archivos de datos del catálogo que deban cambiarse y, a continuación, sustituya (o &quot;táctil&quot;, para actualizar la fecha del archivo) el archivo de atributos del catálogo para almacenar en déclencheur la recarga del catálogo.

## Actualizaciones incrementales {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

La carga y el procesamiento de catálogos de imágenes de gran tamaño pueden suponer una carga considerable en el servidor y pueden tener un impacto negativo en las operaciones de servicio en directo. Para minimizar este impacto, se recomienda implementar un mecanismo de actualización de catálogo incremental, que funcione de la siguiente manera:

Un archivo de catálogo principal que contiene todas las imágenes se carga todas las noches durante las horas de poco tráfico. Si es necesario durante el día añadir o cambiar registros en el catálogo de imágenes, se crea otro archivo de datos de imagen que contiene solo los registros nuevos o modificados. Este archivo está registrado como archivo de datos de imagen secundario en `attribute::CatalogFile`. El servidor detecta que el archivo de atributos del catálogo ha cambiado y, a continuación, comprueba qué archivos de datos del catálogo han cambiado. Si no se ha tocado el archivo de datos de imagen principal, el servidor carga o vuelve a cargar únicamente el archivo de datos incremental. Dado que este archivo suele ser mucho menor que el archivo de catálogo principal, el impacto en el servidor es mucho menor que al volver a cargar el catálogo principal.

Las actualizaciones incrementales pueden reducir significativamente el impacto en el servidor durante el tráfico pesado. Se recomienda combinar regularmente el archivo de datos de catálogo incremental con el archivo de datos de catálogo principal durante las horas de poco tráfico para mantener un rendimiento óptimo del servidor.
