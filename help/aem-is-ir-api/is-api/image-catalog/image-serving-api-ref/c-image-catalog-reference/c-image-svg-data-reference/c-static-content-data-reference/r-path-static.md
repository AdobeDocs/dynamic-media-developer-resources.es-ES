---
title: Ruta
description: El servidor utiliza las reglas de resolución de rutas para encontrar el archivo de datos.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9f273f32-1699-4bc3-8dd0-f1dfefaa6e27
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---

# Ruta{#path}

El servidor usa las reglas de resolución de rutas descritas en [Administrar datos de Source](../../../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-configuration-and-administration.md#concept-1ec4d9f0e58a430cae045761f1ff9173) para encontrar el archivo de datos.

## Propiedades {#section-72d9edc532ad43349afcb4df22e1c692}

Cadena de texto. Necesario para registros de imagen y SVG; puede estar vacío para registros de plantilla. Si se especifica, debe ser una ruta de archivo relativa o absoluta del servidor de imágenes válida. attribute::DefaultExt se anexa si no hay ningún sufijo de archivo.

## Formatos de archivo de imagen admitidos {#section-8d6443c883aa48aaa00316fe9661aaa8}

Consulte la descripción de la utilidad Image Converter (IC) para obtener una lista completa de los formatos de archivo de imagen admitidos.

Las aplicaciones que requieren datos de imagen en varias resoluciones diferentes funcionan mejor cuando se utiliza el formato de varias resoluciones del TIFF piramidal de Dynamic Media (PTIFF). La utilidad IC se utiliza para crear imágenes PTIFF a partir de cualquier formato de imagen admitido.

## Predeterminado {#section-82dad83ec3f84ae8bf2f850b4139f63e}

Ninguno.

## Véase también {#section-b36074fae77d49f5bdfd63e9c36aa3ba}

[Utilidad IC](../../../../../../is-api/is-utils/utilities/r-ic.md#reference-de9f43c63a8f48f1a755ff1760af8b7b), [atributo::RootPath](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-rootpath.md#reference-17d57e5967be403b8408fa7214017494), [atributo::DefaultExt](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultext.md#reference-1b96c71a253049ddaeae09892d3484a0), [src=](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-src.md#reference-f6506637778c4c69bf106a7924a91ab1)
