---
description: Describe los métodos de operaciones nuevos y modificados para la versión 4.5 de la API de IPS.
seo-description: Describe los métodos de operaciones nuevos y modificados para la versión 4.5 de la API de IPS.
seo-title: Operaciones nuevas y modificadas
solution: Experience Manager
title: Operaciones nuevas y modificadas
topic: Scene7 Image Production System API
uuid: c4002670-c830-474e-bb84-343f76b6fb80
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Operaciones: Nuevo y modificado{#operations-new-and-modified}

Describe los métodos de operaciones nuevos y modificados para la versión 4.5 de la API de IPS.

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
* El parámetro `renameFiles` ha quedado obsoleto para versiones anteriores y se ha eliminado de la operación `renameAsset`. La ruta de acceso del archivo virtual se cambia para que coincida con el nuevo nombre del recurso (conservando la extensión del archivo), mientras que las rutas de acceso del archivo físico no se ven afectadas. Los clientes de API deben eliminar las referencias a este parámetro al actualizar a la nueva versión de API.

