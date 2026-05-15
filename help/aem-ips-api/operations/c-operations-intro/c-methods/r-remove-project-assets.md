---
description: Quita recursos de un proyecto. No destruye los recursos.
solution: Experience Manager
title: removeProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 6bf169ec-c724-4ac0-a2bf-67af2ebba21a
TQID: 'https://experienceleague.adobe.com/GHGyYEF5H3Me5jKtkfd15Ok8KEk2hrRuVxrKCF7cZ-E'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 179
ht-degree: 10%

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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía con los recursos que desea mover. |
| projectHandle | `xsd:string` | Sí | El identificador de los recursos del proyecto que desea mover. |
| assetHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de los recursos que desea mover. |

**Salida (removeProjectAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | El recuento de recursos se eliminó correctamente. |
| warningCount | `xsd:int` | Sí | Número de advertencias generadas cuando la operación intentó quitar recursos del proyecto. |
| errorCount | `xsd:int` | Sí | Número de errores generados cuando la operación intentó quitar recursos del proyecto. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron advertencias cuando la operación intentó quitarlos del proyecto. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Matriz de detalles asociados con los recursos que generaron errores cuando la operación intentó quitarlos del proyecto. |

## Ejemplos {#section-13546cf0a98e4e1b91b8b7cd5724ced8}

Este ejemplo de código quita dos recursos de un proyecto (especificados por el identificador del proyecto).

**Solicitud**

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
