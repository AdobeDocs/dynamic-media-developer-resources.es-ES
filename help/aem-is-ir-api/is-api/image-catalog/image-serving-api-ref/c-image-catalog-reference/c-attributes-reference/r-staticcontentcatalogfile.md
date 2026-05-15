---
description: Rutas del archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático para este catálogo.
solution: Experience Manager
title: ArchivoCatálogoContenidoEstático
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ff6f0ad8-189f-4172-89cb-f138d2df8fe4
TQID: 'https://experienceleague.adobe.com/98uNzMz83z3lfa2d3LNixYKZzUWWE9zqrK1fnPo-JNA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 3%

---

# ArchivoCatálogoContenidoEstático{#staticcontentcatalogfile}

Rutas del archivo de datos del catálogo de contenido estático. Especifica los archivos que contienen los datos de contenido estático para este catálogo.

Los archivos de datos del catálogo de contenido estático se cargan en el orden especificado. Si el mismo valor `static::Id` aparece en más de un registro (en el mismo archivo de catálogo o en varios), prevalecerá la última instancia.

## Propiedades {#section-3f8dc8d21fa84fbeb71db6ca1ecbdd8c}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-702edfbc00c54fc29e412a3ff99fef2b}

Vacío, lo que indica que este catálogo de imágenes no incluye datos de contenido estático.

## Véase también {#section-13d78d475fff40e7a4edf9a9c73f3c15}

[Datos de catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
