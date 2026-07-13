---
description: Establece la imagen en miniatura de uno o varios recursos.
solution: Experience Manager
title: batchSetThumbAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: f7d7ddd9-a3c3-47c4-8da6-d693851d0d7f
TQID: 'https://experienceleague.adobe.com/bANJIeE9iNsdm0RevvIgeU--faqAqmUyeZRJn09Oieg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 171
ht-degree: 11%

---

# batchSetThumbAsset{#batchsetthumbasset}

Establece la imagen en miniatura de uno o varios recursos.

Sintaxis

## Tipos de recursos de miniaturas {#section-4edc2a6a8f824213b0aaddb1d437268c}

Los tipos de recursos de miniaturas permitidos son los siguientes:

* Imagen
* Vista ajustada
* Máscara
* Plantilla
* PsdTemplate

## Tipos de usuarios autorizados {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso de destino y acceso de lectura al recurso de la miniatura.

## Parámetros {#section-9c6efa000b384b3db6c013def20cf40b}

**Entrada (batchSetThumbAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene los recursos. |
| updateArray | `types:ThumbAssetUpdateArray` | Sí | La matriz de actualizaciones. |

**Salida (batchSetThumbAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | El número de miniaturas configuradas correctamente. |
| warningCount | `xsd:int` | Sí | El número de advertencias generadas cuando la operación intentó establecer las miniaturas. |
| errorCount | `xsd:int` | Sí | El número de errores generados cuando la operación intentó establecer las miniaturas. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó aplicar las actualizaciones. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó aplicar las actualizaciones. |

## Ejemplos {#section-6de69a8680c24c1486c5f01488393381}

**Solicitud**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Respuesta**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```

