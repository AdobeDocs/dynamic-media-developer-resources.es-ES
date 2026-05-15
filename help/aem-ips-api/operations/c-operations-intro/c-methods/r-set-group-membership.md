---
description: Establece la pertenencia a grupos de un usuario.
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 11%

---

# setGroupMembership{#setgroupmembership}

Establece la pertenencia a grupos de un usuario.

Sintaxis

## Tipos de usuarios autorizados {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-6aeda13b26af4796aad1306ac7a9ad17}

**Entrada (setGroupMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandle | `xsd:string` | No | El identificador del usuario cuya pertenencia al grupo desea establecer. |
| companyHandle | `xsd:string` | No | Manejo de la compañía. |
| groupHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de grupos a los que pertenece el usuario. |

**Salida (setGroupMembershipReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-67b86d259df24938896fe19061845811}

Este ejemplo de código convierte al usuario en miembro de un grupo. Agregue un usuario a varios grupos con la matriz de identificadores de grupo.

**Solicitud**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**Respuesta**

Ninguno.
