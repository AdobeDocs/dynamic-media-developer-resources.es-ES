---
description: Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.5.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 3%

---


# Tipos de datos: Nuevo y modificado{#data-types-new-and-modified}

Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.5.

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

* El recurso incluye un nuevo campo `fileName` que devuelve el nombre del archivo virtual.
* `AssetSummary` devuelve un  `type` y  `name` campo

* `MetadataField` incluye `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` requiere un  `urlArray` y agrega un  `numUrls` recuento opcional

