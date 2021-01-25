---
description: Añade uno o varios recursos en un proyecto.
solution: Experience Manager
title: addProjectAssets
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 11%

---


# addProjectAssets{#addprojectassets}

Añade uno o varios recursos en un proyecto.

Sintaxis

## Tipos de usuarios autorizados {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-20d498e971b6466298e60c8a77fc32b2}

**Entrada (addProjectAssetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Gestionar a la compañía asociada con el proyecto actual. |
| `*`projectHandle`*` | `xsd:string` | Sí | Gestionar el proyecto al que está agregando recursos. |
| `*`projectHandleArray`*` | `xsd:HandleArray` | Sí | Matriz de recursos que está agregando al proyecto actual. |

**Salida (addProjectAssetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | Número de recursos agregados correctamente. |
| `*`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó agregar recursos a un proyecto. |
| `*`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó agregar recursos a un proyecto. |
| `*`warningDetailHandle`*` | `xsd:AssetOperationFaultArray` | No | Matriz de advertencias generadas por los recursos cuando la operación intentó agregarlas a un proyecto. |
| `*`companyHandle`*` | `xsd:AssetOperationFaultArray` | No | Matriz de errores generados por los recursos cuando la operación intentó agregarlos a un proyecto. |

## Ejemplos {#section-bee5be2402f54cb9a3a02cc07def4135}

En este ejemplo se agrega un solo recurso (al que hace referencia su identificador) en una matriz de controladores de recursos a un proyecto especificado en la solicitud. La operación se completó correctamente cuando la respuesta `successCount` devuelve `1`.

**Solicitar**

```java
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Respuesta**

```java
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```

