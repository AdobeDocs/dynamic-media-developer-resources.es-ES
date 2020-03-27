---
description: Quita recursos de un proyecto. No destruye los recursos.
seo-description: Quita recursos de un proyecto. No destruye los recursos.
seo-title: removeProjectAssets
solution: Experience Manager
title: removeProjectAssets
topic: Scene7 Image Production System API
uuid: bae09dc3-4328-4264-8fb2-e4f0c53546eb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeProjectAssets{#removeprojectassets}

Quita recursos de un proyecto. No destruye los recursos.

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
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía con los recursos que desea mover. |
| ` *`projectHandle`*` | `xsd:string` | Sí | Identificador de los recursos de proyecto que desea mover. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Sí | Matriz de identificadores a los recursos que desea mover. |

**Output (removeProjectAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sí | Se eliminó correctamente el recuento de recursos. |
| ` *`warningCount`*` | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó quitar recursos del proyecto. |
| ` *`errorCount`*` | `xsd:int` | Sí | Número de errores generados cuando la operación intentó quitar recursos del proyecto. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados a los recursos que generaron advertencias cuando la operación intentó quitarlos del proyecto. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados a los recursos que generaron errores cuando la operación intentó quitarlos del proyecto. |

## Ejemplos {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Este ejemplo de código elimina 2 recursos de un proyecto (especificado por el controlador del proyecto).

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

