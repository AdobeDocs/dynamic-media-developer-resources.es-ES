---
description: Obtiene las suscripciones de un usuario a una matriz de compañías.
solution: Experience Manager
title: getCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 53af8a97-208c-4c44-93d6-aa36a459af51
TQID: 'https://experienceleague.adobe.com/h-fjzt4o5zdyVkWh9pkWDLs6KXTF3--s4koIQv77Zno'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 81
ht-degree: 16%

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

**Solicitud**

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

