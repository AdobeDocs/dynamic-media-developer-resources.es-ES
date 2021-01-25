---
description: Quita los permisos de los recursos seleccionados.
seo-description: Quita los permisos de los recursos seleccionados.
seo-title: removeAssetPermissions
solution: Experience Manager
title: removeAssetPermissions
topic: Dynamic Media Image Production System API
uuid: 5a351862-f412-4d89-90b7-9e70a26eacbc
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 16%

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
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |
| `*`assetHandle`*` | `xsd:string` | Sí | Identificador del recurso con permisos que desea quitar. |

**Output (removeAssetPermissionsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

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
