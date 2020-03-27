---
description: Devuelve los miembros de un grupo.
seo-description: Devuelve los miembros de un grupo.
seo-title: getGroupMembership
solution: Experience Manager
title: getGroupMembership
topic: Scene7 Image Production System API
uuid: 5ec48e8c-378b-43a3-b3dc-aa21dbf339b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`userHandle`*` | `xsd:string` | No | El identificador del usuario. |
| ` *`companyHandle`*` | `xsd:string` | No | El identificador de la compañía. |

**Salida (getGroupMembershipReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`groupArray`*` | `types:GroupArray` | Sí | Matriz de grupos. |

## Ejemplos {#section-ebb437369f4f4487b3eb2ef0c078b8ae}

Este ejemplo de código devuelve todos los miembros de un grupo. Dado que los controles de compañía y usuario son opcionales, la operación puede devolver todos los miembros de todos los grupos.

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

