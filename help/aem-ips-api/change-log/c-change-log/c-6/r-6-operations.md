---
description: Describe métodos de operaciones nuevos y modificados para la versión 6 de la API de IPS.
solution: Experience Manager
title: Operaciones nuevas y modificadas
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fc7af77e-17fc-453a-8949-78c9c5c33b34
TQID: 'https://experienceleague.adobe.com/DLA26IsxxpZ0TSSfQBrvZSl8mbcJCaTfnpK-bhhmglg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 3%

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

