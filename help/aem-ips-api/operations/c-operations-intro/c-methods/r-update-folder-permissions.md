---
description: Actualice los permisos de la carpeta.
seo-description: Actualice los permisos de la carpeta.
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
topic: Scene7 Image Production System API
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateFolderPermissions{#updatefolderpermissions}

Actualice los permisos de la carpeta.

Sintaxis

## Tipos de usuarios autorizados {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | Identificador de Compañía. |
| ` *`folderHandle`*` | `xsd:string` | Sí | Identificador de carpeta. |
| ` *`updateChildren`*` | `xsd:boolean` | Sí | Determina si se deben actualizar los elementos secundarios con permisos establecidos para la carpeta de nivel superior. |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | Sí | Matriz de actualizaciones de permisos que desea aplicar a la carpeta. |

**Output (updateFolderPermissionsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-c3fe4d4388674870a3856c35ef66b631}

**Solicitar**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Respuesta**

Ninguno.
