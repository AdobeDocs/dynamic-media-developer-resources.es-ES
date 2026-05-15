---
description: Ruta del archivo de imagen. Ruta relativa y nombre de un archivo de imagen de textura o calcomanía.
solution: Experience Manager
title: Ruta *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
TQID: 'https://experienceleague.adobe.com/ndDZ1MOPM1GHqOKFkwwMnJoZHVjaCeVVEHudb-5fPk0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 208
ht-degree: 1%

---

# Ruta *{#path}

Ruta del archivo de imagen. Ruta relativa y nombre de un archivo de imagen de textura o calcomanía.

El servidor combina este valor con `attribute::RootPath` para generar la ruta real del archivo de imagen. También puede ser una ruta absoluta.

Se utiliza para especificar el archivo de imagen de textura para los materiales de revestimiento de textura, gabinete y ventana, y el archivo de imagen RGB o RGBA para los materiales de borde de pared y calcomanía. No todos los materiales de revestimiento de vitrinas y vitrinas requieren una imagen de textura repetible por separado.

## Propiedades {#section-8c12ea24f21d4472be677581893e6681}

Cadena de texto. Necesario para los materiales de textura y calcomanía, opcional para los materiales de revestimiento de vitrinas y vitrinas. Si se especifica, debe ser una ruta de archivo relativa o absoluta válida. Debe estar vacío para los materiales de color sólido.

## Formatos de archivo compatibles {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

El procesamiento de imágenes admite los mismos formatos de imagen de origen que el servicio de imágenes de Dynamic Media.

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionan mejor cuando se utiliza el formato de varias resoluciones Dynamic Media Pyramid TIFF (PTIFF). El servicio de imágenes incluye la utilidad Image Converter (IC) que crea imágenes PTIFF a partir de cualquier formato compatible.

Consulte la descripción de la utilidad IC en la documentación del servicio de imágenes para obtener una lista completa de los formatos de archivo admitidos.

## Predeterminado {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Ninguno.

## Véase también {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilidad IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [atributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
