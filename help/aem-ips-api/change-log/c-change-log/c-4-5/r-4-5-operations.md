---
description: Describe métodos de operaciones nuevos y modificados para la versión 4.5 de la API de IPS.
solution: Experience Manager
title: 'Operaciones: nuevas y modificadas'
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9033328a-d0ce-4ef2-b6ec-c6a81fbedf9d
TQID: 'https://experienceleague.adobe.com/n4U8LW8otIaBBDalW1wRJFaweTAw3-0Sh0ckgIEADAI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 1%

---

# Operaciones: nuevas y modificadas{#operations-new-and-modified}

Describe métodos de operaciones nuevos y modificados para la versión 4.5 de la API de IPS.

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

* `Asset` incluye `animatedGifInfo`, `swcInfo`, `cssInfo` y `javascriptInfo` parámetros.
* `createMetadataField` incluye un parámetro `isHidden` opcional.
* `saveMetadataField` incluye un parámetro `isHidden` opcional.
* `searchAssets`
* El parámetro `renameFiles` ha quedado obsoleto para versiones anteriores y se ha eliminado de la operación `renameAsset`. La ruta del archivo virtual se cambia para que coincida con el nuevo nombre del recurso (conservando la extensión del archivo), mientras que las rutas de archivo físicas no se ven afectadas. Los clientes de API deben quitar las referencias a este parámetro al actualizar a la nueva versión de la API.

