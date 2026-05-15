---
description: Identificador de registro de catálogo
solution: Experience Manager
title: Id
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 37945115-c93d-4f59-b3d3-a2c4ee7fc990
TQID: 'https://experienceleague.adobe.com/M3stRhM1PHUVUFXTKj-KERQVMOGVolpxUuyNUrRzado'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 99
ht-degree: 7%

---

# Id {#id}

Valor de clave de índice según el cual el [!DNL Platform Server] busca los registros del archivo de datos de imagen.

Normalmente, un identificador de imagen corto y único, como un número SKU, posiblemente con algún tipo de sufijo de imagen, si un SKU tiene varias imágenes. También puede ser una cadena más compleja que se asemeje más a una ruta de archivo, para admitir un ajuste retro sencillo de los sitios web con el servicio de imágenes.

## Propiedades {#id-properties}

Cadena de texto. Obligatorio. Clave de índice principal para la tabla de datos de imagen. Cada valor catalog::Id debe ser único dentro de la tabla.

## Predeterminado {#id-default}

Ninguno.

## Véase también {#id-seealso}

[attribute::RootId](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootid.md)
