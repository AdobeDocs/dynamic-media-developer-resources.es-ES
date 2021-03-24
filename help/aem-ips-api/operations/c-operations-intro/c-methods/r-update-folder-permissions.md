---
description: Actualice los permisos de carpeta.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 17%

---


# updateFolderPermissions{#updatefolderpermissions}

Actualice los permisos de carpeta.

Sintaxis

## Tipos de usuarios autorizados {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-339e6e17c5504e1ea79fbdc05f618050}

**Entrada (updateFolderPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | Identificador de la empresa. |
| `*`folderHandle`*` | `xsd:string` | Sí | Identificador de carpeta. |
| `*`updateChildren`*` | `xsd:boolean` | Sí | Determina si se deben actualizar los elementos secundarios con permisos establecidos para la carpeta de nivel superior. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Sí | Matriz de actualizaciones de permisos que desea aplicar a la carpeta. |

**Salida (updateFolderPermissionsReturn)**

La API IPS no devuelve una respuesta para esta operación.

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
