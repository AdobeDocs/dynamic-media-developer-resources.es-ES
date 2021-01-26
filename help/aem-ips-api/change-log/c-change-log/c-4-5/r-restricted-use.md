---
description: Estas operaciones nuevas o modificadas y los tipos de datos disponibles en el WSDL beta no deben utilizarse fuera de las aplicaciones desarrolladas por Dynamic Media.
solution: Experience Manager
title: Uso restringido
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---


# Uso restringido{#restricted-use}

Estas operaciones nuevas o modificadas y los tipos de datos disponibles en el WSDL beta no deben utilizarse fuera de las aplicaciones desarrolladas por Dynamic Media.

Estas operaciones y tipos están sujetos a deshabilitación, cambio o desaprobación con las actualizaciones posteriores del sistema.

**Tipos nuevos**

* AssetPublishContext
* AssetPublishContextArray
* CompanyMetadataInfo
* CompanyMetadataInfoArray
* CreateVideoSitemapJob
* PublishContext
* PublishContextArray
* SearchFilter
* LongArray

**Nuevas operaciones**

* applyMetadataTemplate
* batchGetAssetPublishContext
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

* Se cambió `ImageServingPublishJob` para incluir un `contextHandle` opcional

* Se cambió `ImageRenderingPublishJob` para incluir un `contextHandle` opcional

* Se cambió `MetadataField` para incluir un `initialTagField` opcional

* Se cambió `MetadataCondition` para incluir y el parámetro opcional `caseSensitive`

* Se cambió `PropertySet` para incluir un `PermissionArray` opcional como `permissions`

* Se ha cambiado `UploadDirectoryJob` para incluir parámetros opcionales `xmpKeywords`, `xmpTemplateId` y `xmpTemplateOverride`

* Se cambió `VideoPublishJob` para incluir un `contextHandle` opcional

**Operaciones modificadas**

* Se cambió `createAssetSet` para incluir un `thumbAssetHandle` opcional

* Se cambió `createImageSet` para incluir un `thumbAssetHandle` opcional

* Se cambió `createMetadataField` para incluir un parámetro `initialTagValue` opcional

* Se cambió `createPropertySet` para incluir un `PermissionUpdateArray` opcional como `permissionArray`

* Se cambió `getImageServingPublishSettings` para incluir un parámetro `contextHandle` opcional

* Se cambió `getImageRenderingPublishSettings` para incluir un parámetro `contextHandle` opcional

* Se ha cambiado `searchAssetsByFullText` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como  `filters` parámetro

   * `sortBy`
   * `sortDirection`

* Se ha cambiado `searchAssetsByMetadata` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como  `filters` parámetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` secuencia de siete parámetros

* Se cambió `setAssetPublishState` para incluir un `HandleArray` opcional como `contextHandleArray`

* Se cambió `setImageServingPublishSettings` para incluir un parámetro `contextHandle` opcional

* Se ha cambiado `setImageRenderingPublishSettings` para incluir un parámetro `contextHandle`opcional

* Se cambió `submitJob` para incluir un tipo de trabajo opcional `createVideoSitemap`

