---
description: Establece los permisos de las carpetas.
seo-description: Establece los permisos de las carpetas.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
topic: Scene7 Image Production System API
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setFolderPermissions{#setfolderpermissions}

Establece los permisos de las carpetas.

Sintaxis

## Tipos de usuarios autorizados {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-2a41135054954396b40f1228f2e63b42}

**Entrada (setFolderPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de Compañía. |
| ` *`folderHandle`*` | `xsd:string` | Sí | Identificador de carpeta. |
| ` *`setChildren`*` | `xsd:boolean` | Sí | Establece permisos para los elementos secundarios que pertenecen a la carpeta. |
| ` *`permissionArray`*` | `types:PermissionUpdateArray` | Sí | Matriz de permisos. |

**Output (setFolderPermissionsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-01730da4be874553ab44e3241cdf6357}

Este ejemplo de código especifica un identificador de compañía, un identificador de carpeta y una matriz de permisos con información detallada sobre la carpeta. Aplica los mismos permisos a los elementos secundarios de la carpeta principal.

**Solicitar**

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
