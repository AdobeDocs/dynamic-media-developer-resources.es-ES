---
description: El servidor supervisa continuamente la carpeta del catálogo y vuelve a cargar automáticamente un catálogo de imágenes, incluidos los archivos de datos de catálogo asociados, cuando detecta que el archivo de atributos de catálogo principal se ha cambiado.
solution: Experience Manager
title: Actualizando catálogos de imágenes
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b520b4f3-6717-4768-99e2-78a76d1ede24
TQID: 'https://experienceleague.adobe.com/vnAa-SrnEWsyYW3PuGQT-CjlhGBB9nkQ20hZSKCUuUw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 0%

---

# Actualizando catálogos de imágenes{#updating-image-catalogs}

El servidor supervisa continuamente la carpeta del catálogo y vuelve a cargar automáticamente un catálogo de imágenes, incluidos los archivos de datos de catálogo asociados, cuando detecta que el archivo de atributos de catálogo principal se ha cambiado.

Para actualizar los catálogos de imágenes en el servidor, reemplace primero todos los archivos de datos de catálogo que deban cambiarse y, a continuación, reemplace (o &quot;pulse&quot; para actualizar la fecha del archivo) el archivo de atributos de catálogo para almacenar en déclencheur la recarga del catálogo.

## Actualizaciones incrementales {#section-2c0f2c1b8480486d86920b5f2cfe72d2}

La carga y el procesamiento de catálogos de imágenes de gran tamaño pueden suponer una carga considerable en el servidor y tener un impacto negativo en las operaciones de servidor activo. Para minimizar este impacto, se recomienda implementar un mecanismo de actualización de catálogos incrementales, que funcione de la siguiente manera:

Un archivo de catálogo principal que contiene todas las imágenes se carga todas las noches durante las horas de poco tráfico. Si es necesario durante el día añadir o cambiar registros en el catálogo de imágenes, se crea otro archivo de datos de imagen que contiene solo los registros nuevos o modificados. Este archivo está registrado como archivo de datos de imagen secundario en `attribute::CatalogFile`. El servidor detecta que el archivo de atributos de catálogo ha cambiado y, a continuación, comprueba qué archivos de datos de catálogo han cambiado. Si no se ha tocado el archivo de datos de imagen principal, el servidor carga o vuelve a cargar únicamente el archivo de datos incremental. Dado que este archivo suele ser mucho más pequeño que el archivo de catálogo principal, el impacto en el servidor es mucho menor en comparación con la recarga del catálogo principal.

Las actualizaciones incrementales pueden reducir significativamente el impacto en el servidor durante el tráfico intenso. Se recomienda combinar con regularidad el archivo de datos de catálogo incremental en el archivo de datos de catálogo principal durante las horas de poco tráfico para mantener un rendimiento óptimo del servidor.
