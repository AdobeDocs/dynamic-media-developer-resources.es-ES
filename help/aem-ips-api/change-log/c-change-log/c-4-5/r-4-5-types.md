---
description: Describe tipos de datos nuevos y modificados para la versión 4.5 de la API de IPS.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 45024d75-8058-40f8-b3e3-9b28b4cdc3f7
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

---

# Tipos de datos: nuevos y modificados{#data-types-new-and-modified}

Describe tipos de datos nuevos y modificados para la versión 4.5 de la API de IPS.

Sintaxis

## Nuevos tipos {#section-6941b228cf6747a987e98c3d6e4b6b17}

* `AssetSummary`
* `AssetSummaryArray`
* `JobLogDetailAux`
* `JobLogDetailAuxArray`
* `MPEvent`
* `MPEventArray`
* `OperationFault`
* `OperationFaultArray`
* `PhotoshopOptions`
* `TagCondition`
* `TagConditionArray`
* `TagFieldValues`
* `TagFieldValuesArray`
* `TagValueUpdate`
* `TagValueUpdateArray`
* `TagValueUpdateFault`
* `TagValueUpdateFaultArray`
* `UrlArray`

## Tipos modificados {#section-6ecdf752cc1a4636a583b4c546a0fccf}

* El recurso incluye un nuevo `fileName` que devuelve el nombre del archivo virtual.
* `AssetSummary` devuelve un valor `type` y `name` campo

* `MetadataField` incluye `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` requiere un `urlArray` y añade un `numUrls` count
