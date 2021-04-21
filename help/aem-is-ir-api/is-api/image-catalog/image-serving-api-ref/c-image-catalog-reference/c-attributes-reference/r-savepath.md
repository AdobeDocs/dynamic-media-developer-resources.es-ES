---
description: Ruta raíz para saveToFile=. Ruta relativa para la carpeta raíz en la que se deben escribir las imágenes generadas con req=saveToFile.
solution: Experience Manager
title: SavePath
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 4%

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
