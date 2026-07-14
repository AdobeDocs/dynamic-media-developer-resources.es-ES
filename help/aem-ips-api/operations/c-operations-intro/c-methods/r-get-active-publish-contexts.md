---
description: Obtiene una lista de contextos de publicación activos para la compañía especificada. Un contexto de publicación se considera activo si hay al menos un servidor activo definido para el contexto.
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
TQID: 'https://experienceleague.adobe.com/g337PVX5asvB-o-VQL0XA5XSrgQ0c2vx0xC4-93Dm8E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 108
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

