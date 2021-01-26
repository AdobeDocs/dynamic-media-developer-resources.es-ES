---
description: Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.2.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 3%

---


# Tipos de datos: Nuevo y modificado{#data-types-new-and-modified}

Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.2.

Sintaxis

## Nuevos tipos {#section-770a814386a44478881feeff2b6f65f5}

* `AudioInfo`
* `CuePointInfo`
* `PdfSettings`
* `PremeierExpressRemixInfo`

## Tipos modificados {#section-6c42b62dd91c4e9bb3a067b9abe3adee}

**Recurso**

Parámetros agregados:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

Parámetros eliminados:

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

Parámetros agregados:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

Parámetros agregados:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

Parámetros agregados:

* `preservePublishState`
* `preserveCrop`

