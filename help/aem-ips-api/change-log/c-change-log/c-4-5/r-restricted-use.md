---
description: Estas operaciones y tipos de datos nuevos o modificados disponibles en el WSDL beta no se deben utilizar fuera de las aplicaciones desarrolladas por Dynamic Media.
solution: Experience Manager
title: Uso restringido
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
TQID: 'https://experienceleague.adobe.com/X-Q28iVTM95SDSwlSy3yhmJcfJv0TC3LtxXPRv8RCpg'
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
source-wordcount: 232
ht-degree: 0%

---

# Uso restringido{#restricted-use}

Estas operaciones y tipos de datos nuevos o modificados disponibles en el WSDL beta no se deben utilizar fuera de las aplicaciones desarrolladas por Dynamic Media.

Estas operaciones y tipos están sujetos a la desactivación, el cambio o la desaprobación con actualizaciones posteriores del sistema.

**Nuevos tipos**

* AssetPublishContexts
* AssetPublishContextsArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Nuevas operaciones**

* applyMetadataTemplate
* batchGetAssetPublishContexts
* createCompanyMetadata
* deleteCompanyMetadata
* getCompanyMetadata
* getPublishContexts
* listCompanyMetadata
* removeMask
* removePropertySetPermissions
* searchAssetsBySimilarity
* searchAssetsByFulltext
* setAssetPublishState
* setPropertySetPermissions
* updateAssetSet
* updateCompanyMetadata
* updateImageSet
* updatePropertySetPermissions

**Tipos modificados**

* Se cambió `ActiveJob` para incluir un tipo `createVideoSitemapJob`

* Se cambió `ScheduledJob` para incluir un tipo `createVideoSitemapJob`

* Se cambió `ImageServingPublishJob` para incluir un(a) `contextHandle` opcional

* Se cambió `ImageRenderingPublishJob` para incluir un(a) `contextHandle` opcional

* Se cambió `MetadataField` para incluir un(a) `initialTagField` opcional

* Se cambió `MetadataCondition` para incluir el parámetro `caseSensitive` opcional

* Se cambió `PropertySet` para incluir un(a) `PermissionArray` opcional como `permissions`

* Se cambió `UploadDirectoryJob` para incluir los parámetros `xmpKeywords`, `xmpTemplateId` y `xmpTemplateOverride` opcionales

* Se cambió `VideoPublishJob` para incluir un(a) `contextHandle` opcional

**Operaciones modificadas**

* Se cambió `createAssetSet` para incluir un(a) `thumbAssetHandle` opcional

* Se cambió `createImageSet` para incluir un(a) `thumbAssetHandle` opcional

* Se cambió `createMetadataField` para incluir un parámetro `initialTagValue` opcional

* Se cambió `createPropertySet` para incluir un(a) `PermissionUpdateArray` opcional como `permissionArray`

* Se cambió `getImageServingPublishSettings` para incluir un parámetro `contextHandle` opcional

* Se cambió `getImageRenderingPublishSettings` para incluir un parámetro `contextHandle` opcional

* Se cambió `searchAssetsByFullText` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como parámetro `filters`

   * `sortBy`
   * `sortDirection`

* Se cambió `searchAssetsByMetadata` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como parámetro `filters`

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` secuencia de siete parámetros

* Se cambió `setAssetPublishState` para incluir un(a) `HandleArray` opcional como `contextHandleArray`

* Se cambió `setImageServingPublishSettings` para incluir un parámetro `contextHandle` opcional

* Se cambió `setImageRenderingPublishSettings` para incluir un parámetro `contextHandle` opcional

* Se ha cambiado `submitJob` para incluir un tipo de trabajo `createVideoSitemap` opcional

