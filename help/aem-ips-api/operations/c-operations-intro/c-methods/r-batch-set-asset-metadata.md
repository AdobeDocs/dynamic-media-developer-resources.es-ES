---
description: Establece los metadatos de los recursos mediante el modo por lotes.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadatos.Administración de recursos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 12%

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa cuyos metadatos desea configurar en una operación por lotes. |
| `*`updateArray`*` | `types:BatchMetadataUpdateArray` | Sí | Matriz de actualizaciones de metadatos aplicadas a los recursos. |

**Salida (batchSetAssetMetadataParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | Número de metadatos establecidos correctamente. |
| `*`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó establecer metadatos. |
| `*`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó establecer metadatos. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generan advertencias cuando la operación intentó establecer metadatos para los recursos por lotes. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados a los recursos que generan errores cuando la operación intentó establecer metadatos para los recursos en lotes. |

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

