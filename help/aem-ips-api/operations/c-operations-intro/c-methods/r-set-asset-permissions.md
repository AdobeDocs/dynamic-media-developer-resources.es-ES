---
description: Define los permisos de un solo recurso mediante un recurso de permiso.
seo-description: Define los permisos de un solo recurso mediante un recurso de permiso.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Scene7 Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 8%

---


# setAssetPermissions{#setassetpermissions}

Define los permisos de un solo recurso mediante un recurso de permiso.

Los recursos heredan los permisos de su carpeta principal de forma predeterminada. Una vez configurados los permisos en un recurso, ya no hereda los permisos de su elemento principal a menos que llame a `removeAssetPermissions`.

## Tipos de usuarios autorizados {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-e05abbce6453450fb38747101cb5e228}

**Input (setAssetPermissonsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de la compañía que contiene la carpeta con la que desea trabajar. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador de carpeta. |
| ` *`permissionArray`*` | `types:PermissionsUpdateArray` | Sí | Matriz de permisos. |

**Salida (setAssetPermissonsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-38955bc330bb4909b6b06027ef2b143e}

Este ejemplo de código establece permisos en un recurso. Contiene la compañía, el identificador de recurso y una matriz de permisos.

**Solicitar**

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
