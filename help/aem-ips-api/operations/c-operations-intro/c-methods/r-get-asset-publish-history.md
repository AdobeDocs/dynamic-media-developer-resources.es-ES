---
description: Devuelve el historial de publicación de un recurso.
seo-description: Devuelve el historial de publicación de un recurso.
seo-title: getAssetPublishHistory
solution: Experience Manager
title: getAssetPublishHistory
uuid: 15025c3d-eac3-4cb8-9a2a-fd80bd67478f
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 15%

---


# getAssetPublishHistory{#getassetpublishhistory}

Devuelve el historial de publicación de un recurso.

Sintaxis

## Tipos de usuarios autorizados {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-3541bd9914a44b89acfc1d419b560ee6}

**Entrada (getAssetPublishHistoryParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con el historial de publicación de recursos. |
| `*`assetHandle`*` | `xsd:string` | Sí | El recurso con el historial de publicación que desea examinar. |

**Salida (getAssetPublishHistoryReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | Sí | El historial de publicación del recurso. |

## Ejemplos {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Este ejemplo de código devuelve el historial de publicación de un recurso. Nunca se ha publicado un recurso si el servidor devuelve una matriz vacía.

**Solicitar**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Respuesta**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```

