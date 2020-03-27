---
description: Devuelve el historial de publicación de un recurso.
seo-description: Devuelve el historial de publicación de un recurso.
seo-title: getAssetPublishHistory
solution: Experience Manager
title: getAssetPublishHistory
topic: Scene7 Image Production System API
uuid: 15025c3d-eac3-4cb8-9a2a-fd80bd67478f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con el historial de publicación de recursos. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Recurso con el historial de publicación que desea examinar. |

**Salida (getAssetPublishHistoryReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`pubHistoryArray`*` | `types:PublishHistoryArray` | Sí | Historial de publicación del recurso. |

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

