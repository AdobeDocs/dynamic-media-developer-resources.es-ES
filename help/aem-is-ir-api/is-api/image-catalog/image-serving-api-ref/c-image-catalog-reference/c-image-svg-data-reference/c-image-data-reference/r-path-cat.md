---
description: Ruta del archivo de imagen.
solution: Experience Manager
title: Ruta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9d5417df-3aa2-4620-a614-ca71a96e2069
TQID: 'https://experienceleague.adobe.com/dpQY2E7P1LzEhYg05p6C5MQRvx9jgdMB-GrBReIIqig'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 4%

---

# Ruta{#path}

Ruta del archivo de imagen.

Ruta relativa o absoluta y nombre del archivo de imagen de origen asociado a este registro de catálogo. El servidor utiliza las reglas de resolución de rutas descritas en Administración de datos de Source para encontrar el archivo de datos.

## Propiedades {#path-properties}

Cadena de texto. Necesario para registros de imagen; puede estar vacío para registros de plantilla. Si se especifica, debe ser una ruta de archivo relativa o absoluta del servidor de imágenes válida. attribute::DefaultExt se anexa si no hay ningún sufijo de archivo.

## Formatos de archivo de imagen admitidos {#path-supported-image-file-formats}

Consulte la descripción de la utilidad Image Converter (IC) para obtener una lista completa de los formatos de archivo compatibles.

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionan mejor cuando utilizan el formato de varias resoluciones Dynamic Media Pyramid TIFF (PTIFF). La utilidad IC se utiliza para crear imágenes PTIFF a partir de cualquier formato de imagen admitido.

## Predeterminado {#path-default}

Ninguno.

## Véase también {#path-seealso}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [attribute::RootPath](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md) , [attribute::DefaultExt](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md) , [src=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md)

<!-- [attribute::LowerCasePaths]() -->
