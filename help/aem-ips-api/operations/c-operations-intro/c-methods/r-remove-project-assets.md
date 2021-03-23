---
description: Quita los recursos de un proyecto. No destruye los recursos.
seo-description: Quita los recursos de un proyecto. No destruye los recursos.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '198'
ht-degree: 10%

---


# removeProjectAssets{#removeprojectassets}

Quita los recursos de un proyecto. No destruye los recursos.

Sintaxis

## Tipos de usuarios autorizados {#section-b0b333a1f3b648ac8cd6bb3d135d2c6f}

* `IpsUser`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-169d8e317417415b87df86242f65710e}

**Entrada (removeProjectAssetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa con los recursos que desea mover. |
| `*`projectHandle`*` | `xsd:string` | Sí | El identificador de los recursos de proyecto que desea mover. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sí | Matriz de controles de los recursos que desea mover. |

**Salida (removeProjectAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | El recuento de recursos se eliminó correctamente. |
| `*`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó quitar recursos del proyecto. |
| `*`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó quitar recursos del proyecto. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó quitarlos del proyecto. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó eliminarlos del proyecto. |

## Ejemplos {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Este ejemplo de código elimina 2 recursos de un proyecto (especificado por el gestor del proyecto).

**Solicitar**

```java
<removeProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
      <items>a|739|1|537</items>
   </assetHandleArray>
</removeProjectAssetsParam>
```

