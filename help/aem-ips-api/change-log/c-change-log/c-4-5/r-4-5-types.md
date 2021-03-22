---
description: Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.5.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 2%

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

* Asset incluye un nuevo campo `fileName` que devuelve el nombre del archivo virtual.
* `AssetSummary` devuelve un  `type` campo  `name` y

* `MetadataField` incluye `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` requiere un  `urlArray` y añade un  `numUrls` recuento opcional

