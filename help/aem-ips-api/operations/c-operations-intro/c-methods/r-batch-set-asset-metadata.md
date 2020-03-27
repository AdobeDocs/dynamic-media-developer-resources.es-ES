---
description: Establece los metadatos de los recursos mediante el modo por lotes.
seo-description: Establece los metadatos de los recursos mediante el modo por lotes.
seo-title: batchSetAssetMetadata
solution: Experience Manager
title: batchSetAssetMetadata
topic: Scene7 Image Production System API
uuid: 88d8f279-988f-4956-b66f-60fa95cf511c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetAssetMetadata{#batchsetassetmetadata}

Establece los metadatos de los recursos mediante el modo por lotes.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía cuyos metadatos desea definir en una operación por lotes. |
| ` *`updateArray`*` | `types:BatchMetadataUpdateArray` | Sí | Matriz de actualizaciones de metadatos aplicadas a los recursos. |

**Salida (batchSetAssetMetadataParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sí | Número de metadatos establecidos correctamente. |
| ` *`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó establecer metadatos. |
| ` *`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó establecer metadatos. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociada con los recursos que generan advertencias cuando la operación intentó crear lotes de metadatos para los recursos. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociada a los recursos que generan errores cuando la operación intentó crear lotes de metadatos para los recursos. |

## Ejemplos {#section-2de798ac920e4b47b971b1729a64395b}

**Solicitar**

```java
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

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```

