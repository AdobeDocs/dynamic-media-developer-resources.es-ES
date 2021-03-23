---
description: Quita los permisos de los recursos seleccionados.
seo-description: Quita los permisos de los recursos seleccionados.
seo-title: removeAssetPermissions
solution: Experience Manager
title: removeAssetPermissions
uuid: 5a351862-f412-4d89-90b7-9e70a26eacbc
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---


# removeAssetPermissions{#removeassetpermissions}

Quita los permisos de los recursos seleccionados.

Sintaxis

## Tipos de usuarios autorizados {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Entrada (removeAssetPermissionsParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa. |
| `*`assetHandle`*` | `xsd:string` | Sí | El identificador del recurso con los permisos que desea eliminar. |

**Salida (removeAssetPermissionsReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-238fa7bb091548f5ba72ced11fc92d4f}

Este ejemplo de código elimina los permisos de un recurso.

**Solicitar**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Respuesta**

Ninguno.
