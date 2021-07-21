---
description: Obtiene una lista de contextos de publicación activos para la empresa especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 10%

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
