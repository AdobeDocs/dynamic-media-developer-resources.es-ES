---
description: Devuelve los miembros de un grupo.
solution: Experience Manager
title: getGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 847e4982-219d-47fd-b94c-f7d520ba1367
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 20%

---

# getGroupMembership{#getgroupmembership}

Devuelve los miembros de un grupo.

Sintaxis

## Tipos de usuarios autorizados {#section-35d070e5c4d74ca69df508368953cfb8}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-2e92f850254e46e48403acaa215341a5}

**Entrada (getGroupMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandle | `xsd:string` | No | El identificador del usuario. |
| companyHandle | `xsd:string` | No | El identificador de la compañía. |

**Salida (getGroupMembershipReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| groupArray | `types:GroupArray` | Sí | Matriz de grupos. |

## Ejemplos {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Este ejemplo de código devuelve todos los miembros de un grupo. Como los identificadores de empresa y usuario son opcionales, la operación puede devolver todos los miembros de todos los grupos.

**Solicitar**

```java
<ns1:getGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getGroupMembershipParam>
```

**Respuesta**

```java
<getGroupMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <groupArray>
      <items>
         <groupHandle>225</groupHandle><companyHandle>47</companyHandle><name>MyGroup</name><isSystemDefined>false</isSystemDefined></items></groupArray></getGroupMembershipReturn>
```
