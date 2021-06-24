---
description: Asigne o actualice recursos en un proyecto.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Developer,Administrator
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 18%

---

# setProjectAssets{#setprojectassets}

Asigne o actualice recursos en un proyecto.

Sintaxis

## Tipos de usuarios autorizados {#section-8d87939db6d547b48ca6d71771bbefa8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-bd51ef23deaf434ba2efb8cef2a8b4a5}

**Entrada (setProjectAssetsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`projectHandle`*` | `xsd:string` | Sí | Identificador del proyecto. |
| `*`assetHandleArray`*` | `types:HandleArray` | Sí | Matriz de controladores de recursos que desea asociar al proyecto. |

**Salida (setProjectAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sí | El número de recursos agregados correctamente. |

## Ejemplos {#section-33c1a909c3dc4aa98da474c23a036596}

Este ejemplo de código asigna un recurso a un proyecto. La solicitud devuelve un recuento de éxito de uno.

**Solicitar**

```java
<setProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|739|1|537</items>
   </assetHandleArray>
</setProjectAssetsParam>
```

**Respuesta**

```java
<setProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</setProjectAssetsReturn>
```
