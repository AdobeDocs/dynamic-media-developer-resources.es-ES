---
description: Estas operaciones nuevas o modificadas y los tipos de datos disponibles en el WSDL beta no deben utilizarse fuera de las aplicaciones desarrolladas por Dynamic Media.
solution: Experience Manager
title: Uso restringido
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---


# Uso restringido{#restricted-use}

Estas operaciones nuevas o modificadas y los tipos de datos disponibles en el WSDL beta no deben utilizarse fuera de las aplicaciones desarrolladas por Dynamic Media.

Estas operaciones y tipos están sujetos a deshabilitación, cambio o desaprobación con actualizaciones posteriores del sistema.

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

* Se ha cambiado `ActiveJob` para incluir un tipo `createVideoSitemapJob`

* Se ha cambiado `ScheduledJob` para incluir un tipo `createVideoSitemapJob`

* Se ha cambiado `ImageServingPublishJob` para incluir un `contextHandle` opcional

* Se ha cambiado `ImageRenderingPublishJob` para incluir un `contextHandle` opcional

* Se ha cambiado `MetadataField` para incluir un `initialTagField` opcional

* Se ha cambiado `MetadataCondition` para incluir y el parámetro opcional `caseSensitive`

* Se ha cambiado `PropertySet` para incluir un `PermissionArray` opcional como `permissions`

* Se ha cambiado `UploadDirectoryJob` para incluir parámetros opcionales `xmpKeywords`, `xmpTemplateId` y `xmpTemplateOverride`

* Se ha cambiado `VideoPublishJob` para incluir un `contextHandle` opcional

**Operaciones modificadas**

* Se ha cambiado `createAssetSet` para incluir un `thumbAssetHandle` opcional

* Se ha cambiado `createImageSet` para incluir un `thumbAssetHandle` opcional

* Se ha cambiado `createMetadataField` para incluir un parámetro opcional `initialTagValue`

* Se ha cambiado `createPropertySet` para incluir un `PermissionUpdateArray` opcional como `permissionArray`

* Se ha cambiado `getImageServingPublishSettings` para incluir un parámetro opcional `contextHandle`

* Se ha cambiado `getImageRenderingPublishSettings` para incluir un parámetro opcional `contextHandle`

* Se ha cambiado `searchAssetsByFullText` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como  `filters` parámetro

   * `sortBy`
   * `sortDirection`

* Se ha cambiado `searchAssetsByMetadata` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como  `filters` parámetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` secuencia de siete parámetros

* Se ha cambiado `setAssetPublishState` para incluir un `HandleArray` opcional como `contextHandleArray`

* Se ha cambiado `setImageServingPublishSettings` para incluir un parámetro opcional `contextHandle`

* Se ha cambiado `setImageRenderingPublishSettings` para incluir un parámetro `contextHandle`opcional

* Se ha cambiado `submitJob` para incluir un tipo de trabajo opcional `createVideoSitemap`

