---
description: Quita los usuarios de la empresa de un grupo específico.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
TQID: 'https://experienceleague.adobe.com/dMEOhQgXQvFvZj2Kozsq6J7qJNiwYpknQQbNkADMsg0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 8%

---

# removeGroupMembers{#removegroupmembers}

Quita los usuarios de la empresa de un grupo específico.

**Diferencias entre los comandos de eliminación**

* `removeGroupMembers`: quita varios usuarios de un grupo.
* `removeGroupMembership`: quita un usuario individual de una matriz de grupos.

## Tipos de usuarios autorizados {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b5596614a3be4ce5962455884e4636af}

**Entrada (removeGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía con los usuarios con los que desea trabajar. |
| groupHandle | `xsd:string` | Sí | Identificador de grupo. |
| userHandleArray | `types:HandleArray` | Sí | Matriz de identificadores de usuarios cuyas pertenencias de grupo desea quitar. |

**Salida (removeGroupMembersParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-9eedac852cea46ec80de6a6928bf97ac}

Este ejemplo de código quita un usuario de la compañía especificada. Quitar varios usuarios de un grupo con la matriz de identificadores de usuario.

**Solicitud**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Respuesta**

Ninguno.
