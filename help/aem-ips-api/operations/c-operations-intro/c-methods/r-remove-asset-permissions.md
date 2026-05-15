---
description: Quita los permisos de los recursos seleccionados.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c47d9853-91b1-45fe-b8ff-aaa1239ca0d1
TQID: 'https://experienceleague.adobe.com/x8k6HwyFQ-U1VHnFmPAPPPuN9pftPorvmXnIWhXfI3k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
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
| companyHandle | `xsd:string` | Sí | El identificador de la compañía. |
| assetHandle | `xsd:string` | Sí | El identificador del recurso con los permisos que desea eliminar. |

**Salida (removeAssetPermissionsReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-238fa7bb091548f5ba72ced11fc92d4f}

Este ejemplo de código elimina los permisos de un recurso.

**Solicitud**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Respuesta**

Ninguno.
