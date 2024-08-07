---
description: Restaura recursos de la papelera.
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b1cde1a9-d726-4ebc-9d49-ee72a6b56fc9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 11%

---

# restoreAssetsFromTrash{#restoreassetsfromtrash}

Restaura recursos de la papelera.

Sintaxis

## Tipos de usuarios autorizados {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-200a61d040c94e489a85241b29cd499a}

**Entrada (restoreAssetsFromTrashParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de una compañía con los recursos que desea restaurar. |
| assetHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de los recursos que desea restaurar. |

**Salida (restoreAssetsFromTrashReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | Número de recursos eliminados correctamente de la papelera. |
| warningCount | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó restaurar recursos desde la papelera. |
| errorCount | `xsd:int` | Sí | Número de errores generados al intentar restaurar recursos desde la papelera. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó restaurar recursos de la papelera. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó restaurar los recursos de la papelera. |

## Ejemplos {#section-98fe0394b0634ca397c395f14f8a9358}

Este ejemplo de código restaura los recursos de la papelera. La respuesta indica que la operación se ha completado correctamente.

**Solicitud**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Respuesta**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```
