---
description: Obtiene los recursos y el número de recursos asociados a una empresa específica.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 10%

---


# getAssetCounts{#getassetcounts}

Obtiene los recursos y el número de recursos asociados a una empresa específica.

El `countArray` devuelto consiste en una matriz de `assetTypes` (tipo de datos `xsd:string`), cada una con su propio campo de recuento (tipo de datos `xsd:int`), que permite la representación de varios tipos de activos por elemento de la matriz.
Sintaxis

## Tipos de usuarios autorizados {#section-6234754722184e828352f10eb18fbce9}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-2a9581315eca427d8a3d26cc3fca7b1f}

**Entrada (getAssetCountsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con los recursos que desea contar. |

**Salida (getAssetCountsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`countArray`*` | `types:AssetCountArray` | No | Matriz de tipos de recurso, cada uno con su propio campo de recuento, que permite la representación de varios tipos de recurso por elemento de la matriz. |

## Ejemplos {#section-6052a503eb3843f6adb99e200fdba280}

Este ejemplo de código utiliza el identificador de la empresa como campo en el `getAssetCountsParam` enviado al servidor de servicios web IPS para obtener los recuentos de recursos.

**Solicitar**

```java
<getAssetCountsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
</getAssetCountsParam>
```

**Respuesta**

```java
<getAssetCountsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <countArray>
      <items>
         <assetType>Image</assetType>
         <count>44</count>
      </items>
      <items>
         <assetType>Flash</assetType>
         <count>3</count>
      </items>
   </countArray>
</getAssetCountsReturn>
```

