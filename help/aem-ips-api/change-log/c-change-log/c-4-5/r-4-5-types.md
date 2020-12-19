---
description: Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.5.
seo-description: Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.5.
seo-title: Tipos de datos nuevos y modificados
solution: Experience Manager
title: Tipos de datos nuevos y modificados
topic: Scene7 Image Production System API
uuid: 2752f9dd-ec47-45d6-a465-6d275ec2b2fb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
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

* El recurso incluye un nuevo campo `fileName` que devuelve el nombre del archivo virtual.
* `AssetSummary` devuelve un  `type` y  `name` campo

* `MetadataField` incluye `isHidden`

* `MetadataUpdate`
* `UploadUrlsJob` requiere un  `urlArray` y agrega un  `numUrls` recuento opcional

