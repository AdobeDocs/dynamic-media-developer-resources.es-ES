---
description: Devuelve el historial de publicación de un recurso.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Developer,Administrator
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 16%

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
