---
description: Ruta raíz para saveToFile=. Ruta relativa para la carpeta raíz en la que se deben escribir las imágenes generadas con req=saveToFile.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6e2814b9-898f-4cf4-8e4f-aa972d554213
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# SavePath{#savepath}

Ruta raíz para saveToFile=. Ruta relativa para la carpeta raíz en la que se deben escribir las imágenes generadas con req=saveToFile.

`SavePath` es una cadena de texto.

## Propiedades {#section-343d1371e966491c92854a8df14c3c50}

Cadena de texto. Debe estar vacío o una ruta de carpeta relativa válida. Siempre se combina con la ruta de acceso raíz absoluta configurada con `ImageServer::SaveDirectory`.

## Predeterminado {#section-ae751eea97654f399c6aaee3f3252cbb}

Se hereda de `default::SavePath` si no se define. Guardar en archivos está deshabilitado si el valor resuelto está vacío.

## Véase también {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
