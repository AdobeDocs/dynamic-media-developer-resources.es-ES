---
description: Actualiza los permisos de los recursos.
seo-description: Actualiza los permisos de los recursos.
seo-title: updateAssetPermissons
solution: Experience Manager
title: updateAssetPermissons
topic: Scene7 Image Production System API
uuid: feb2faf3-81de-436e-82de-1e41df03508f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateAssetPermissons{#updateassetpermissons}

Actualiza los permisos de los recursos.

Sintaxis

## Tipos de usuarios autorizados {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-392cb3076cf84790a32fd913f2b111a3}

**Input (updateAssetPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de Compañía. |
| ` *`assetHandle`*` | `xsd:string` | Sí | Identificador de recurso. |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | Sí | Permisos que desea aplicar al recurso. |

**Output (updateAssetPermissionsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

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
