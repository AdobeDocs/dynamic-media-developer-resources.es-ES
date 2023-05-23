---
description: Describe métodos de operaciones nuevos y modificados para la versión 6 de la API de IPS.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 6%

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

**Agregado**

* Añadido `isHidden` y `initialTagValue` hasta:

   * `saveMetadataField`
   * ` `updateMetadataField&quot;
   * `createMetadataField`

* Añadido `thumbAssetHandle` hasta:

   * `createImageSet`
   * `createAssetSet`

   Añadido `companyHandle` hasta:

   * `getViewerConfigSettings`
   * `setViewerConfigSettings`
   * `updateViewerConfigSettings`
   * `getSearchStrings`

   Añadido `contextHandle` hasta:

   * `getImageServingPublishSettings`
   * `getImageRenderingPublishSettings`
   * `setImageServingPublishSettings`
   * `setImageRenderingPublishSettings`



* Se ha añadido includeInactive a:

   * `getUsers`.
   * `getUserChars`.

* Añadido `permissionArray` hasta `createPropertySet`.

* Añadido `exportJob` hasta `submitJob`.

**Se cambió**

* Entrada `addUser` y `setUser`, cambiado `role` hasta `defaultRole`.

* Entrada `getCompanyMembers`, cambiado `userArray` hasta `memberArray`.

* Entrada `getCompanyMembership`, cambiado `companyArray` hasta `membershipArray`.

* Entrada `addUser`, `setCompanyMembership`, y `addCompanyMembership`, cambiado `membershipArray` hasta `companyHandleArray`.

* Entrada `getCompanyMembership`, cambiado `companyArray` hasta `membershipArray`.

* Entrada `getUserChars`, `includeInvalid` ahora es opcional.

**Eliminado**

* Eliminado `renameFiles` de `renameAsset`.

* Eliminado `getXMPPanelViewDefinition`.
* Eliminado `searchAssetsByFulltext` y `searchAssetsBySimilarity`.
