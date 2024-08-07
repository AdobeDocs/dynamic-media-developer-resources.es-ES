---
description: Establece permisos de carpeta.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 13%

---

# setFolderPermissions{#setfolderpermissions}

Establece permisos de carpeta.

Sintaxis

## Tipos de usuarios autorizados {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-2a41135054954396b40f1228f2e63b42}

**Entrada (setFolderPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | Manejo de la compañía. |
| folderHandle | `xsd:string` | Sí | Controlador de carpeta. |
| setChildren | `xsd:boolean` | Sí | Establece permisos en elementos secundarios que pertenecen a la carpeta. |
| permissionArray | `types:PermissionUpdateArray` | Sí | Matriz de permisos. |

**Salida (setFolderPermissionsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-01730da4be874553ab44e3241cdf6357}

Este ejemplo de código especifica un identificador de compañía, un identificador de carpeta y una matriz de permisos con información detallada sobre la carpeta. Aplica los mismos permisos a los elementos secundarios de la carpeta principal.

**Solicitud**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Respuesta**

Ninguno.
