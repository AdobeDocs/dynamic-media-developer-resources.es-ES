---
description: Obtiene la pertenencia de un usuario a una matriz de compañías.
seo-description: Obtiene la pertenencia de un usuario a una matriz de compañías.
seo-title: getCompanyMembership
solution: Experience Manager
title: getCompanyMembership
topic: Scene7 Image Production System API
uuid: fb3dfe29-4292-4ab2-8015-36c4930a9c05
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# getCompanyMembership{#getcompanymembership}

Obtiene la pertenencia de un usuario a una matriz de compañías.

Sintaxis

## Tipos de usuarios autorizados {#section-f8bba547e1f648648be99dc48fd72b5d}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-8745c360c3e1400a88e9bdb26bcb93de}

**Entrada (getCompanyMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | No | Identificador del usuario cuyas membresías desea obtener. |

**Output (getCompanyMembershipReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`membershipArray`*` | `types:CompanyMembershipArray` | Sí | Matriz de membresías de compañía. |

## Ejemplos {#section-e4958d104ea344a4a79f57d07b46eba7}

Este ejemplo de código toma un control de usuario y obtiene todos los miembros de compañía del usuario en una matriz. La respuesta se ha truncado para la brevedad.

**Solicitar**

```java
<ns1:getCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
</ns1:getCompanyMembershipParam>
```

**Respuesta**

```java
<getCompanyMembershipReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <membershipArray>
      <items>
         <companyHandle>48</companyHandle>
         <name>AIR</name>
         <rootPath>AIR/</rootPath>
         <expires>2101-01-31T23:00:00.485-08:00</expires>
      </items>
      ...
    </membershipArray>
</getCompanyMembershipReturn>
```

