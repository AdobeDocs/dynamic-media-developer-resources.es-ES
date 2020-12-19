---
description: Determina si un lote de recursos está listo para publicarse.
seo-description: Determina si un lote de recursos está listo para publicarse.
seo-title: setAssetsPublishState
solution: Experience Manager
title: setAssetsPublishState
topic: Scene7 Image Production System API
uuid: 2910cd6c-573b-405c-864d-a0136ac5472d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 11%

---


# setAssetsPublishState{#setassetspublishstate}

Determina si un lote de recursos está listo para publicarse.

Esta es la versión por lotes de [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Tipos de usuarios autorizados {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>El usuario debe tener acceso de lectura y escritura al recurso.

## Parámetros {#section-3e49d7859f8647b990d75373cc8dbc24}

**Entrada (setAssetsPublishStateParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de compañía. |
| ` *`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | Sí | Matriz de valores de estado de publicación para los recursos. |

**Salida (setAssetsPublishStateParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sí | Número de recursos actualizados correctamente. |
| ` *`warningCount`*` | `xsd:int` | Sí | Número de recursos que generaron una advertencia cuando la operación intentó actualizarlos. |
| ` *`errorCount`*` | `xsd:int` | Sí | Número de recursos que generaron un error cuando la operación intentó eliminarlos. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Detalles asociados con las actualizaciones de recursos que generaron una advertencia. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Detalles asociados con las actualizaciones de recursos que generaron un error. |

## Ejemplos {#section-38cfdd3436214a06a1bae16875501d51}

Este ejemplo de código establece el estado de publicación de un recurso.

**Solicitar**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Respuesta**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```

