---
description: Ruta raíz para saveToFile=. Ruta relativa para la carpeta raíz en la que se deben escribir las imágenes generadas con req=saveToFile.
seo-description: Ruta raíz para saveToFile=. Ruta relativa para la carpeta raíz en la que se deben escribir las imágenes generadas con req=saveToFile.
seo-title: SavePath
solution: Experience Manager
title: SavePath
uuid: 02b88e83-7fee-40d4-95ea-daba9a608e8e
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 3%

---


# SavePath{#savepath}

Ruta raíz para saveToFile=. Ruta relativa para la carpeta raíz en la que se deben escribir las imágenes generadas con req=saveToFile.

`SavePath` es un valor de cadena de texto.

## Propiedades {#section-343d1371e966491c92854a8df14c3c50}

Cadena de texto. Debe estar vacío o tener una ruta de carpeta relativa válida. Siempre se combina con la ruta raíz absoluta configurada con `ImageServer::SaveDirectory`.

## Predeterminado {#section-ae751eea97654f399c6aaee3f3252cbb}

Se hereda de `default::SavePath` si no se define. Guardar en archivos está desactivado si el valor resuelto está vacío.

## Véase también {#section-b38b045bbf084ca5a4b24ea12c4877ae}

[req=saveToFile](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76)
