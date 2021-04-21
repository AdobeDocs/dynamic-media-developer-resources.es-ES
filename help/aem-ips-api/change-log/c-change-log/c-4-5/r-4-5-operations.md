---
description: Describe los métodos de operaciones nuevos y modificados para la API IPS versión 4.5.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Operaciones: Nuevo y modificado{#operations-new-and-modified}

Describe los métodos de operaciones nuevos y modificados para la API IPS versión 4.5.

Sintaxis

## Nuevas operaciones {#section-a3be679d8e9345aba2e97699c3a537b9}

* `addMediaPortalEvent`
* `addTagFieldValues`
* `cdnCacheInvalidation`
* `deleteTagFieldValues`
* `deleteTagFieldValues`
* `getDistinctMetadataValues`
* `getMediaPortalEvent`
* `getTagFieldValues`
* `getXMPPacket`
* `searchAssetsByFullText`
* `searchAssetsByMetadata`
* `setTagFieldValues`
* `updateTagFieldValues`
* `updateXMPPacket`

## Operaciones modificadas {#section-1c022cc62d274c349837013f1c02ca51}

* `Asset` incluye  `animatedGifInfo`,  `swcInfo`,  `cssInfo` y  `javascriptInfo` parámetros.

* `createMetadataField` incluye un  `isHidden` parámetro opcional.

* `saveMetadataField` incluye un  `isHidden` parámetro opcional.

* `searchAssets`
* 
* El parámetro `renameFiles` ha quedado obsoleto para versiones anteriores y se ha eliminado de la operación `renameAsset`. La ruta del archivo virtual se cambia para que coincida con el nuevo nombre del recurso (conservando la extensión del archivo), mientras que las rutas de archivo físicas no se ven afectadas. Los clientes de API deben eliminar las referencias a este parámetro al actualizar a la nueva versión de API.

