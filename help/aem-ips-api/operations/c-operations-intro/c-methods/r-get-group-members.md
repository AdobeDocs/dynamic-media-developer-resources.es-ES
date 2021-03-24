---
description: Obtiene los usuarios que pertenecen a una empresa y un grupo específicos.
solution: Experience Manager
title: getGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 17%

---


# getGroupMembers{#getgroupmembers}

Obtiene los usuarios que pertenecen a una empresa y un grupo específicos.

Sintaxis

## Tipos de usuarios autorizados {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrada (getGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sí | El identificador de la empresa. |
| `*`groupHandle`*` | `xsd:string` |  | El identificador del grupo. |

**Salida (getGroupMembersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`userHandleArray`*` | `type:HandleArray` | Sí | Matriz de controles de usuario. |

## Ejemplos {#section-aaa340dba6b64cce9bcd8303cf999166}

Este ejemplo de código devuelve una matriz de gestión de usuario que contiene todos los usuarios que pertenecen a un grupo específico.

**Solicitar**

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

