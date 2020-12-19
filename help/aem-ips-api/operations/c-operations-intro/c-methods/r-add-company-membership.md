---
description: Añade un usuario en una o varias compañías.
seo-description: Añade un usuario en una o varias compañías.
seo-title: addCompanyMembership
solution: Experience Manager
title: addCompanyMembership
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# addCompanyMembership{#addcompanymembership}

Añade un usuario en una o varias compañías.

Sintaxis

## Tipos de usuarios autorizados {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**Entrada (addCompanyMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | No | Identificador del usuario cuya pertenencia desea agregar. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sí | Matriz de compañías a la que está agregando el usuario. |

**Output (addCompanyMembershipReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-5469f88bac7047cca131faa6b021e437}

Este ejemplo utiliza ` *`companyHandleArray`*` para agregar un usuario a una sola compañía.

**Solicitar**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Respuesta**

Ninguno.
