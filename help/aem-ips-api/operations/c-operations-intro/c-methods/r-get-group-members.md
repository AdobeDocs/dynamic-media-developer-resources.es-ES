---
description: Obtiene los usuarios que pertenecen a una compañía y un grupo específicos.
seo-description: Obtiene los usuarios que pertenecen a una compañía y un grupo específicos.
seo-title: getGroupMembers
solution: Experience Manager
title: getGroupMembers
topic: Scene7 Image Production System API
uuid: 02322b66-1c0c-4d84-a3eb-97a4fb605318
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 16%

---


# getGroupMembers{#getgroupmembers}

Obtiene los usuarios que pertenecen a una compañía y un grupo específicos.

Sintaxis

## Tipos de usuarios autorizados {#section-08a73460d122480292205bb8f2df9220}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-b798b06354c946abbb90fa72cc9c67fd}

**Entrada (getGroupMembersParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sí | El identificador de la compañía. |
| ` *`groupHandle`*` | `xsd:string` |  | El identificador del grupo. |

**Salida (getGroupMembersReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`userHandleArray`*` | `type:HandleArray` | Sí | Matriz de identificadores de usuario. |

## Ejemplos {#section-aaa340dba6b64cce9bcd8303cf999166}

Este ejemplo de código devuelve una matriz de control de usuario que contiene todos los usuarios que pertenecen a un grupo específico.

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

