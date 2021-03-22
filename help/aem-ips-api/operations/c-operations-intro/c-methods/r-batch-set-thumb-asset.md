---
description: Define la imagen en miniatura de uno o varios recursos.
seo-description: Define la imagen en miniatura de uno o varios recursos.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 12%

---


# batchSetThumbAsset{#batchsetthumbasset}

Define la imagen en miniatura de uno o varios recursos.

Sintaxis

## Tipos de recursos de miniatura {#section-4edc2a6a8f824213b0aaddb1d437268c}

Los tipos de recurso de miniaturas permitidos están formados por lo siguiente:

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
>El usuario debe tener acceso de lectura y escritura al recurso de destino y acceso de lectura al recurso en miniatura.

## Parámetros {#section-9c6efa000b384b3db6c013def20cf40b}

**Entrada (batchSetThumbAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa que contiene los recursos. |
| `*`updateArray`*` | `types:ThumbAssetUpdateArray` | Sí | Matriz de actualizaciones. |

**Salida (batchSetThumbAssetParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | Número de miniaturas establecidas correctamente. |
| `*`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó establecer las miniaturas. |
| `*`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó establecer las miniaturas. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó aplicar las actualizaciones. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó aplicar las actualizaciones. |

## Ejemplos {#section-6de69a8680c24c1486c5f01488393381}

**Solicitar**

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

