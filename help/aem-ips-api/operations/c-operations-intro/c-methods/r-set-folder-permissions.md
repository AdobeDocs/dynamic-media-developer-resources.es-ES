---
description: Establece permisos de carpeta.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
TQID: 'https://experienceleague.adobe.com/r-WGRjE263vPSVKsBieklQ79SASbDQOx9hp5IzS0-O0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 91
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

