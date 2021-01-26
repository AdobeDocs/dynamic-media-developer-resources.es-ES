---
description: Ruta del archivo de imagen. Ruta de acceso relativa y nombre de un archivo de imagen de textura o de calcomanía.
seo-description: Ruta del archivo de imagen. Ruta de acceso relativa y nombre de un archivo de imagen de textura o de calcomanía.
seo-title: Ruta *
solution: Experience Manager
title: Ruta *
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9e85a358-3f2f-4b8b-a98f-03de2a1a8a4c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 3%

---


# Ruta *{#path}

Ruta del archivo de imagen. Ruta de acceso relativa y nombre de un archivo de imagen de textura o de calcomanía.

El servidor combina este valor con `attribute::RootPath` para crear la ruta de acceso real del archivo de imagen. También puede ser un camino absoluto.

Se utiliza para especificar el archivo de imagen de textura para los materiales de textura, gabinete y revestimiento de ventanas, y el archivo de imagen RGB o RGBA para los materiales de borde de la pared y el calado. No todos los materiales de revestimiento de gabinete y ventana requieren una imagen de textura repetible independiente.

## Propiedades {#section-8c12ea24f21d4472be677581893e6681}

Cadena de texto. Necesario para los materiales de textura y calado, opcional para los materiales de revestimiento de vitrinas y carcasas. Si se especifica, debe ser una ruta de archivo absoluta o relativa válida. Debe estar vacío para materiales de color sólido.

## Formatos de archivo admitidos {#section-7ef6c9f7c72c4f03ae926d030b6c46d8}

El procesamiento de imágenes admite los mismos formatos de imagen de origen que el servicio de imágenes de Dynamic Media.

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionarán mejor al utilizar el formato de varias resoluciones TIFF (PTIFF) piramidal de Dynamic Media. El servicio de imágenes incluye la utilidad Image Converter (IC) que crea imágenes PTIFF desde cualquier formato admitido.

Consulte la descripción de la utilidad IC en la documentación del servicio de imágenes para obtener una lista completa de los formatos de archivo admitidos.

## Predeterminado {#section-d2e91fcd7d3c45edb34e7d5ae1daadda}

Ninguno.

## Véase también {#section-1bf37fab8e5f4c42a03b785abafc53bd}

[IC Utility](/help/aem-is-ir-api/is-api/is-utils/utilities/r-ic.md) ,  [atributo::RootPath](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md),  [src=](/help/aem-is-ir-api/ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md)
