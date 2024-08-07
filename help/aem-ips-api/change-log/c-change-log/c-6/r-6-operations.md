---
description: Describe métodos de operaciones nuevos y modificados para la versión 6 de la API de IPS.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 1%

---

# Operaciones: nuevas y modificadas{#operations-new-and-modified}

Describe métodos de operaciones nuevos y modificados para la versión 6 de la API de IPS.

Sintaxis

## Nuevas operaciones {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Operaciones modificadas {#section-f4e8755527444266ae806e3f4c851ae6}

**Se agregó**

* Se agregaron `isHidden` y `initialTagValue` a:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Se agregó `thumbAssetHandle` a:

   * `createImageSet`
   * `createAssetSet`

  Se agregó `companyHandle` a:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

  Se agregó `contextHandle` a:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`

* Se ha añadido includeInactive a:

   * `getUsers`.
   * `getUserChars`.

* Se agregó `permissionArray` a `createPropertySet`.

* Se agregó `exportJob` a `submitJob`.

**Cambiado**

* En `addUser` y `setUser`, cambió `role` a `defaultRole`.

* En `getCompanyMembers`, cambió `userArray` a `memberArray`.

* En `getCompanyMembership`, cambió `companyArray` a `membershipArray`.

* En `addUser`, `setCompanyMembership` y `addCompanyMembership`, cambió `membershipArray` a `companyHandleArray`.

* En `getCompanyMembership`, cambió `companyArray` a `membershipArray`.

* En `getUserChars`, `includeInvalid` es ahora opcional.

**Eliminado**

* Se eliminó `renameFiles` de `renameAsset`.

* Se eliminó `getXMPPanelViewDefinition`.
* Se eliminaron `searchAssetsByFulltext` y `searchAssetsBySimilarity`.
