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

* Cambiado `ActiveJob` para incluir un `createVideoSitemapJob` type

* Cambiado `ScheduledJob` para incluir un `createVideoSitemapJob` type

* Cambiado `ImageServingPublishJob` para incluir un `contextHandle`

* Cambiado `ImageRenderingPublishJob` para incluir un `contextHandle`

* Cambiado `MetadataField` para incluir un `initialTagField`

* Cambiado `MetadataCondition` para incluir y opcional `caseSensitive` parámetro

* Cambiado `PropertySet` para incluir un `PermissionArray` as `permissions`

* Cambiado `UploadDirectoryJob` para incluir opcional `xmpKeywords`, `xmpTemplateId` y `xmpTemplateOverride` parámetros

* Cambiado `VideoPublishJob` para incluir un `contextHandle`

**Operaciones modificadas**

* Cambiado `createAssetSet` para incluir un `thumbAssetHandle`

* Cambiado `createImageSet` para incluir un `thumbAssetHandle`

* Cambiado `createMetadataField` para incluir un `initialTagValue` parámetro

* Cambiado `createPropertySet` para incluir un `PermissionUpdateArray` as `permissionArray`

* Cambiado `getImageServingPublishSettings` para incluir un `contextHandle` parámetro

* Cambiado `getImageRenderingPublishSettings` para incluir un `contextHandle` parámetro

* Cambiado `searchAssetsByFullText` para incluir una serie de parámetros opcionales:

   * `SearchFilter` as `filters` parámetro

   * `sortBy`
   * `sortDirection`

* Cambiado `searchAssetsByMetadata` para incluir una serie de parámetros opcionales:

   * `SearchFilter` as `filters` parámetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` secuencia de siete parámetros

* Cambiado `setAssetPublishState` para incluir un `HandleArray` as `contextHandleArray`

* Cambiado `setImageServingPublishSettings` para incluir un `contextHandle` parámetro

* Cambiado `setImageRenderingPublishSettings` para incluir un `contextHandle`parámetro

* Cambiado `submitJob` para incluir un `createVideoSitemap` tipo de trabajo
