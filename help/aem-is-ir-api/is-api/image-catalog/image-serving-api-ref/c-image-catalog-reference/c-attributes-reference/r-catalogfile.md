---
description: Rutas del archivo de datos de imagen. Especifica los archivos que contienen los datos de imagen para este catálogo.
solution: Experience Manager
title: CatalogFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 240a3884-68dd-474c-83a6-d79fc5b6c300
TQID: 'https://experienceleague.adobe.com/MhxEBtyw3JIvMg5miQotPPCeoLeWATtXy0fbRtE7ePs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 3%

---

# CatalogFile{#catalogfile}

Rutas del archivo de datos de imagen. Especifica los archivos que contienen los datos de imagen para este catálogo.

Los archivos de datos de imagen se cargan en el orden especificado. Si el mismo valor `catalog::Id` aparece en más de un registro (en el mismo archivo de catálogo o en varios), prevalecerá la última instancia.

## Propiedades {#section-6da55f145ecd4e31a5de52637a436983}

Uno o más valores de cadena de texto, separados por comas. Opcional. Cada valor debe ser una ruta absoluta o una ruta relativa a la carpeta del catálogo.

## Predeterminado {#section-80f91cd7a6b2479ebb310319e9c74da7}

Vacío, lo que indica que este catálogo de imágenes no incluye datos de imagen.

## Véase también {#section-910b67c5041d44d99a105ad43ff63a37}

[Campos de datos de catálogo](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-catalog-data-fields/c-catalog-data-fields.md#concept-b19581028ec44f98b9f5943624403d29)
