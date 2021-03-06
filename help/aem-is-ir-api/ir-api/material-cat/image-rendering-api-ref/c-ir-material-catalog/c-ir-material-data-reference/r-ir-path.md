---
description: Ruta del archivo de imagen. Ruta relativa y nombre de un archivo de imagen de textura o calco.
solution: Experience Manager
title: Ruta *
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 28758709-26ae-4261-b11e-34e37b9d1b8c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# Ruta *{#path}

Ruta del archivo de imagen. Ruta relativa y nombre de un archivo de imagen de textura o calco.

El servidor combina este valor con `attribute::RootPath` para crear la ruta real del archivo de imagen. También puede ser un camino absoluto.

Se utiliza para especificar el archivo de imagen de textura para materiales de textura, gabinete y cubierta de ventanas, y el archivo de imagen RGB o RGBA para materiales de borde de calado y pared. No todos los materiales de revestimiento del gabinete y las ventanas requieren una imagen de textura repetible independiente.

## Propiedades {#section-8c12ea24f21d4472be677581893e6681}

Cadena de texto. Necesario para materiales de textura y calzado, optativo para materiales de revestimiento de cartón y ventanilla. Si se especifica, debe ser una ruta de archivo absoluta o relativa válida. Debe estar vacío para materiales de color sólido.

## Formatos de archivo compatibles {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

La representación de imágenes admite los mismos formatos de imagen de origen que Dynamic Media Image Serving.

Las aplicaciones que requieran datos de imagen en varias resoluciones diferentes tendrán un mejor rendimiento al usar el formato de varias resoluciones TIFF (PTIFF) piramidal de Dynamic Media. Image Serving incluye la utilidad Image Converter (IC) que crea imágenes PTIFF a partir de cualquier formato admitido.

Consulte la descripción de la utilidad IC en la documentación de Image Serving para obtener una lista completa de los formatos de archivo admitidos.

## Predeterminado {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Ninguno.

## Véase también {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [atributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
