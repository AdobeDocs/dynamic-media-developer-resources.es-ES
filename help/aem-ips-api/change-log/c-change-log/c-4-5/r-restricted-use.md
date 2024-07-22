---
description: Estas operaciones y tipos de datos nuevos o modificados disponibles en el WSDL beta no se deben utilizar fuera de las aplicaciones desarrolladas por Dynamic Media.
solution: Experience Manager
title: Uso restringido
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6602c5bc-9f75-4885-ae14-cab14e6afa5e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '232'
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
