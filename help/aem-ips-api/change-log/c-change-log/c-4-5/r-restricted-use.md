---
description: Estas operaciones nuevas o modificadas y los tipos de datos disponibles en el WSDL beta no se utilizarán fuera de las aplicaciones desarrolladas por Scene7.
seo-description: Estas operaciones nuevas o modificadas y los tipos de datos disponibles en el WSDL beta no se utilizarán fuera de las aplicaciones desarrolladas por Scene7.
seo-title: Uso restringido
solution: Experience Manager
title: Uso restringido
topic: Scene7 Image Production System API
uuid: 76a423e5-ff7d-44a3-aba4-af258ea55256
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Uso restringido{#restricted-use}

Estas operaciones nuevas o modificadas y los tipos de datos disponibles en el WSDL beta no se utilizarán fuera de las aplicaciones desarrolladas por Scene7.

Estas operaciones y tipos están sujetos a deshabilitación, cambio o desaprobación con las actualizaciones posteriores del sistema.

**Tipos nuevos**

* AssetPublishContexts
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

* Se ha cambiado `ActiveJob` para incluir un `createVideoSitemapJob` tipo

* Se ha cambiado `ScheduledJob` para incluir un `createVideoSitemapJob` tipo

* Se ha cambiado `ImageServingPublishJob` para incluir un `contextHandle`

* Se ha cambiado `ImageRenderingPublishJob` para incluir un `contextHandle`

* Se ha cambiado `MetadataField` para incluir un `initialTagField`

* Se ha cambiado `MetadataCondition` a incluir y `caseSensitive` parámetro opcional

* Se ha cambiado `PropertySet` para incluir una opción `PermissionArray` como `permissions`

* Se ha cambiado `UploadDirectoryJob` para incluir parámetros opcionales `xmpKeywords`, `xmpTemplateId` y `xmpTemplateOverride`

* Se ha cambiado `VideoPublishJob` para incluir un `contextHandle`

**Operaciones modificadas**

* Se ha cambiado `createAssetSet` para incluir un `thumbAssetHandle`

* Se ha cambiado `createImageSet` para incluir un `thumbAssetHandle`

* Se ha cambiado `createMetadataField` para incluir un `initialTagValue` parámetro opcional

* Se ha cambiado `createPropertySet` para incluir una opción `PermissionUpdateArray` como `permissionArray`

* Se ha cambiado `getImageServingPublishSettings` para incluir un `contextHandle` parámetro opcional

* Se ha cambiado `getImageRenderingPublishSettings` para incluir un `contextHandle` parámetro opcional

* Se ha cambiado `searchAssetsByFullText` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como `filters` parámetro

   * `sortBy`
   * `sortDirection`

* Se ha cambiado `searchAssetsByMetadata` para incluir una serie de parámetros opcionales:

   * `SearchFilter` como `filters` parámetro

   * `sortBy`
   * `sortDirection`
   * `haystackSearch` secuencia de siete parámetros

* Se ha cambiado `setAssetPublishState` para incluir una opción `HandleArray` como `contextHandleArray`

* Se ha cambiado `setImageServingPublishSettings` para incluir un `contextHandle` parámetro opcional

* Se ha cambiado `setImageRenderingPublishSettings` para incluir un `contextHandle`parámetro opcional

* Se ha cambiado `submitJob` para incluir un tipo `createVideoSitemap` de trabajo opcional

