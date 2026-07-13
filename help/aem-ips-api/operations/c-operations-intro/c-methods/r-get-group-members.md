---
description: Obtiene los usuarios que pertenecen a una compañía y grupo específicos.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81af79ee-be82-439f-9f42-a1ec09cd8ea0
TQID: 'https://experienceleague.adobe.com/30uti0zOBWTPoFORCa3fTaGznpYjTcSO7oV7M3E-A1c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 16%

---

# getGroupMembers{#getgroupmembers}

Obtiene los usuarios que pertenecen a una compañía y grupo específicos.

Sintaxis

## Tipos de usuarios autorizados {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrada (getGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| companyHandle | `xsd:string` | Sí | El identificador de la compañía. |
| groupHandle | `xsd:string` |  | El identificador del grupo. |

**Salida (getGroupMembersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandleArray | `type:HandleArray` | Sí | Matriz de identificadores de usuario. |

## Ejemplos {#section-aaa340dba6b64cce9bcd8303cf999166}

Este ejemplo de código devuelve una matriz de identificadores de usuario que contiene todos los usuarios que pertenecen a un grupo específico.

**Solicitud**

```java
<ns1:getGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
</ns1:getGroupMembersParam>
```

**Respuesta**

```java
<getGroupMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userHandleArray>
      <items>70|kmagnusson@adobe.com</items>
   </userHandleArray>
</getGroupMembersReturn>
```

