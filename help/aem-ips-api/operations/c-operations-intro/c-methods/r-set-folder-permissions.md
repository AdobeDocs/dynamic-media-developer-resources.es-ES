---
description: Establece los permisos de carpeta.
seo-description: Establece los permisos de carpeta.
seo-title: setFolderPermissions
solution: Experience Manager
title: setFolderPermissions
uuid: 3a33034e-df2c-48ab-8ade-b76bea444388
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 13%

---


# setFolderPermissions{#setfolderpermissions}

Establece los permisos de carpeta.

Sintaxis

## Tipos de usuarios autorizados {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-2a41135054954396b40f1228f2e63b42}

**Entrada (setFolderPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`folderHandle`*` | `xsd:string` | Sí | Identificador de carpeta. |
| `*`setChildren`*` | `xsd:boolean` | Sí | Establece los permisos de los elementos secundarios que pertenecen a la carpeta. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | Sí | Matriz de permisos. |

**Salida (setFolderPermissionsReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-01730da4be874553ab44e3241cdf6357}

Este ejemplo de código especifica un identificador de empresa, un identificador de carpeta y una matriz de permisos con información detallada sobre la carpeta. Aplica los mismos permisos a los elementos secundarios de la carpeta principal.

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
