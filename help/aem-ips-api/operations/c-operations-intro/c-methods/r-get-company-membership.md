---
description: Obtiene las suscripciones de un usuario a una matriz de compañías.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 18%

---

# getCompanyMembership{#getcompanymembership}

Obtiene las suscripciones de un usuario a una matriz de compañías.

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
| userHandle | `xsd:string` | No | El identificador del usuario cuyas suscripciones desea obtener. |

**Salida (getCompanyMembershipReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| subscriptionArray | `types:CompanyMembershipArray` | Sí | Matriz de miembros de la compañía. |

## Ejemplos {#section-e4958d104ea344a4a79f57d07b46eba7}

Este ejemplo de código toma un identificador de usuario y obtiene todas las suscripciones de compañía del usuario en una matriz. La respuesta se ha truncado para ser breve.

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
