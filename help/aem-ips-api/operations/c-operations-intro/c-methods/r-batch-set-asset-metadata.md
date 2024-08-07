---
description: Establece los metadatos del recurso mediante el modo por lotes.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 12%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

Establece los metadatos del recurso mediante el modo por lotes.

Sintaxis

## Tipos de usuarios autorizados {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Entrada (batchSetAssetMetadataParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Identificador de la compañía cuyos metadatos desea establecer en una operación por lotes. |
| updateArray | `types:BatchMetadataUpdateArray` | Sí | Matriz de actualizaciones de metadatos aplicadas a los recursos. |

**Salida (batchSetAssetMetadataParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | El número de metadatos establecidos correctamente. |
| warningCount | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó establecer metadatos. |
| errorCount | `xsd:int` | Sí | Número de errores generados cuando la operación intentó establecer metadatos. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | La matriz de detalles asociados con los recursos que generan advertencias cuando la operación intentó establecer metadatos por lotes para los recursos. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó establecer metadatos por lotes para los recursos. |

## Ejemplos {#section-2de798ac920e4b47b971b1729a64395b}

**Solicitud**

```java {.line-numbers}
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Respuesta**

```java {.line-numbers}
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
