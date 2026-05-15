---
description: Obtiene los recursos y el número de recursos asociados con una compañía específica.
solution: Experience Manager
title: getAssetCounts
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 21cb8023-d6fe-416a-b16f-636df8a37958
TQID: 'https://experienceleague.adobe.com/gvFs-dqQ8oR38MTKrEYaap31BH-MtSaRtGtJd5FO-MY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 9%

---

# getAssetCounts{#getassetcounts}

Obtiene los recursos y el número de recursos asociados con una compañía específica.

El objeto `countArray` devuelto consiste en una matriz de `assetTypes` (tipo de datos `xsd:string`), cada uno con su propio campo de recuento (tipo de datos `xsd:int`), lo que permite la representación de varios tipos de recursos por elemento de la matriz.
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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía con los recursos que desea contar. |

**Salida (getAssetCountsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| countArray | `types:AssetCountArray` | No | Una matriz de tipos de recursos, cada uno con su propio campo de recuento, lo que permite representar varios tipos de recursos por elemento de la matriz. |

## Ejemplos {#section-6052a503eb3843f6adb99e200fdba280}

Este ejemplo de código utiliza el identificador de la empresa como un campo del `getAssetCountsParam` enviado al servidor de servicios web IPS para obtener los recuentos de recursos.

**Solicitud**

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
