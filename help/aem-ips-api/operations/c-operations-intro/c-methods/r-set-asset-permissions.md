---
description: Establece los permisos de un solo recurso mediante un recurso de permiso.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 8%

---

# setAssetPermissions{#setassetpermissions}

Establece los permisos de un solo recurso mediante un recurso de permiso.

Assets hereda los permisos de su carpeta principal de forma predeterminada. Una vez configurados los permisos en un recurso, ya no heredará los permisos de su elemento principal a menos que llame a `removeAssetPermissions`.

## Tipos de usuarios autorizados {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-e05abbce6453450fb38747101cb5e228}

**Entrada (setAssetPermisosParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía que contiene la carpeta con la que desea trabajar. |
| assetHandle | `xsd:string` | Sí | Controlador de carpeta. |
| permissionArray | `types:PermissionsUpdateArray` | Sí | Matriz de permisos. |

**Salida (setAssetPermisosReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-38955bc330bb4909b6b06027ef2b143e}

Este ejemplo de código establece permisos en un recurso. Contiene el identificador de la empresa y el recurso, así como una matriz de permisos.

**Solicitud**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Respuesta**

Ninguno.
