---
description: Ruta del archivo de imagen. Ruta relativa y nombre de un archivo de imagen de textura o calcomanía.
solution: Experience Manager
title: Ruta *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '207'
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

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionan mejor cuando se utiliza el formato de varias resoluciones del TIFF piramidal de Dynamic Media (PTIFF). El servicio de imágenes incluye la utilidad Image Converter (IC) que crea imágenes PTIFF a partir de cualquier formato compatible.

Consulte la descripción de la utilidad IC en la documentación del servicio de imágenes para obtener una lista completa de los formatos de archivo admitidos.

## Predeterminado {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Ninguno.

## Véase también {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[Utilidad IC](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) , [atributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md), [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
