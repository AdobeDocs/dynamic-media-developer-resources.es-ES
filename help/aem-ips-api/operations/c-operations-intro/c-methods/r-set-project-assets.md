---
description: Asignar o actualizar recursos en un proyecto.
solution: Experience Manager
title: setProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: b6e6e9bd-5ee2-4750-9182-49e7a3e3486c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 18%

---

# setProjectAssets{#setprojectassets}

Asignar o actualizar recursos en un proyecto.

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
| companyName | `xsd:string` | Sí | Manejo de la compañía. |
| projectHandle | `xsd:string` | Sí | Controlador de proyecto. |
| assetHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de recursos que desea asociar al proyecto. |

**Salida (setProjectAssetsReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| successCount | `xsd:int` | Sí | Número de recursos agregados correctamente. |

## Ejemplos {#section-33c1a909c3dc4aa98da474c23a036596}

Este ejemplo de código asigna un recurso a un proyecto. La solicitud devuelve un recuento de éxito de uno.

**Solicitud**

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
