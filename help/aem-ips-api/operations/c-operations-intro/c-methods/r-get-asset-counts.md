---
description: Obtiene los recursos y el número de recursos asociados a una compañía específica.
seo-description: Obtiene los recursos y el número de recursos asociados a una compañía específica.
seo-title: getAssetCounts
solution: Experience Manager
title: getAssetCounts
topic: Scene7 Image Production System API
uuid: 92103806-59da-444f-b69c-d045d0ebf42e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getAssetCounts{#getassetcounts}

Obtiene los recursos y el número de recursos asociados a una compañía específica.

El `countArray` devuelto consiste en una matriz de `assetTypes` (tipo de datos `xsd:string`), cada una con su propio campo de recuento (tipo de datos `xsd:int`), lo que permite la representación de varios tipos de recursos por elemento de la matriz.
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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con los recursos que desea contar. |

**Salida (getAssetCountsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`countArray`*` | `types:AssetCountArray` | No | Matriz de tipos de recurso, cada uno con su propio campo de recuento, que permite la representación de varios tipos de recurso por elemento de la matriz. |

## Ejemplos {#section-6052a503eb3843f6adb99e200fdba280}

Este ejemplo de código utiliza el identificador de la compañía como campo en el `getAssetCountsParam` enviado al servidor de servicios Web IPS para obtener los recuentos de recursos.

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

