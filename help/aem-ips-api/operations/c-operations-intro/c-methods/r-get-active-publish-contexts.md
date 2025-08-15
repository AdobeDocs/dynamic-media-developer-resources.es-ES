---
description: Obtiene una lista de contextos de publicación activos para la compañía especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 11%

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

**Entrada (getActivePublishContextsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía para consultar contextos de publicación activos |

**Salida (getActivePublishContextsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| contextArray | `types:StringArray` | Sí | Matriz de contextos de publicación activos, que pueden incluir cero o más valores del contexto de publicación. |
