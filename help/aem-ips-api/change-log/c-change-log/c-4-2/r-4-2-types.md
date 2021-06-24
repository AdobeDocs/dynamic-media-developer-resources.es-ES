---
description: Describe los tipos de datos nuevos y modificados para la API de IPS versión 4.2.
solution: Experience Manager
title: Tipos de datos nuevos y modificados
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 3917e778-bd28-4047-b9f8-3063f136e492
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '56'
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

Parámetros añadidos:

* `readyForPublish`
* `trashState`
* `MaskInfo`
* `RTFInfo`

Parámetros eliminados:

* `ImageSetInfo`
* `RenderSetInfo`

**ReprocessAssetsJob**

Parámetros añadidos:

* `preservePublishState`
* `preserveCrop`
* `readyForPublish`

**UploadDirectoryJob**

Parámetros añadidos:

* `preservePublishState`
* `preserveCrop`
* `videoEncodingPreset`

**UploadUrlsJob**

Parámetros añadidos:

* `preservePublishState`
* `preserveCrop`
