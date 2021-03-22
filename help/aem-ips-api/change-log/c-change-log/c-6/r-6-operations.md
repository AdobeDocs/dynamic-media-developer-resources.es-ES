---
description: Describe los métodos de operaciones nuevos y modificados para la versión 6 de la API IPS.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---


# Operaciones: Nuevo y modificado{#operations-new-and-modified}

Describe los métodos de operaciones nuevos y modificados para la versión 6 de la API IPS.

Sintaxis

## Nuevas operaciones {#section-088502a0746945f28a5ea100cd655bc6}

* `batchGetAssetPublishContexts`
* `getPublishContexts`
* `moveFolder`
* `setAssetsContexState`
* `updateAssetSet`
* `updateImageSet`

## Operaciones modificadas {#section-f4e8755527444266ae806e3f4c851ae6}

**Agregado**

* Se agregaron `isHidden` y `initialTagValue` a:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Se ha agregado `thumbAssetHandle` a:

   * `createImageSet`
   * `createAssetSet`

   Se ha agregado `companyHandle` a:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Se ha agregado `contextHandle` a:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* Se ha añadido includeInactive a:

   * `getUsers`.
   * `getUserChars`.

* Se ha agregado `permissionArray` a `createPropertySet`.

* Se ha agregado `exportJob` a `submitJob`.

**Se cambió**

* En `addUser` y `setUser`, cambió `role` a `defaultRole`.

* En `getCompanyMembers`, cambió `userArray` a `memberArray`.

* En `getCompanyMembership`, cambió `companyArray` a `membershipArray`.

* En `addUser`, `setCompanyMembership` y `addCompanyMembership`, se cambió `membershipArray` a `companyHandleArray`.

* En `getCompanyMembership`, cambió `companyArray` a `membershipArray`.

* En `getUserChars`, `includeInvalid` es ahora opcional.

**Eliminado**

* Se ha eliminado `renameFiles` de `renameAsset`.

* Eliminado `getXMPPanelViewDefinition`.
* Se han eliminado `searchAssetsByFulltext` y `searchAssetsBySimilarity`.

