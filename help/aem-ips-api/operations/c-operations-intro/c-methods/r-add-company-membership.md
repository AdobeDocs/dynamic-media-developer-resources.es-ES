---
description: Agrega un usuario a una o más empresas.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 13%

---

# addCompanyMembership{#addcompanymembership}

Agrega un usuario a una o más empresas.

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
| `*`userHandle`*` | `xsd:string` | No | El identificador del usuario cuya pertenencia desea agregar. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sí | Matriz de empresas a las que va a agregar el usuario. |

**Salida (addCompanyMembershipReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-5469f88bac7047cca131faa6b021e437}

Este ejemplo utiliza `*`companyHandleArray`*` para agregar un usuario a una sola empresa.

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
