---
description: Obtiene una lista de contextos de publicación activos para la compañía especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.
seo-description: Obtiene una lista de contextos de publicación activos para la compañía especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getActivePublishContext{#getactivepublishcontext}

Obtiene una lista de contextos de publicación activos para la compañía especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.

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

**Entrada (getActivePublishContextParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía a la consulta para los contextos de publicación activos |

**Salida (getActivePublishContextReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | Sí | Matriz de contextos de publicación activos, que puede incluir cero o más valores del contexto de publicación. |

