---
description: Actualiza los permisos de recursos.
solution: Experience Manager
title: updateAssetPermisos
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 20%

---


# updateAssetPermisos{#updateassetpermissons}

Actualiza los permisos de recursos.

Sintaxis

## Tipos de usuarios autorizados {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-392cb3076cf84790a32fd913f2b111a3}

**Entrada (updateAssetPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Sí | Permisos que desea aplicar al recurso. |

**Salida (updateAssetPermissionsReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Solicitar**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Respuesta**

Ninguno.
