---
description: Obtiene una lista de contextos de publicación activos para la empresa especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.
seo-description: Obtiene una lista de contextos de publicación activos para la empresa especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 8%

---


# getActivePublishContext{#getactivepublishcontext}

Obtiene una lista de contextos de publicación activos para la empresa especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.

Sintaxis

## Tipos de usuarios autorizados {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-a4be4024e55c472fa6728faec9c5e048}

**Entrada (getActivePublishContextsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa para consultar los contextos de publicación activos |

**Salida (getActivePublishContextsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | Sí | Matriz de contextos de publicación activos, que puede incluir cero o más valores de contexto de publicación. |

