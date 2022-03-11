---
description: Describe los métodos de operaciones nuevos y modificados para la API IPS versión 4.5.
solution: Experience Manager
title: 'Operaciones: nuevas y modificadas'
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
source-git-commit: 10eb6887663fe335be3abcc311b2d3eb4a241745
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 1%

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

* `Asset` incluye `animatedGifInfo`, `swcInfo`, `cssInfo`y `javascriptInfo` parámetros.
* `createMetadataField` incluye una `isHidden` parámetro.
* `saveMetadataField` incluye una `isHidden` parámetro.
* `searchAssets`
* La variable `renameFiles` se ha desaprobado para versiones anteriores y se ha eliminado del `renameAsset` operación. La ruta del archivo virtual se cambia para que coincida con el nuevo nombre del recurso (conservando la extensión del archivo), mientras que las rutas de archivo físicas no se ven afectadas. Los clientes de API deben eliminar las referencias a este parámetro al actualizar a la nueva versión de API.
