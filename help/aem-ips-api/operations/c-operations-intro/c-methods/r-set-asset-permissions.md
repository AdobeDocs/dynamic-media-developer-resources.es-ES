---
description: Establece los permisos de un solo recurso mediante un recurso de permiso.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 1e73c305-cda5-4c30-9380-ec4cd8309933
TQID: 'https://experienceleague.adobe.com/dd96ai2DgoCqZ1NR-2rixSHDEaBSgk6ioQIqmG-1RoE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
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
