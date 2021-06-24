---
description: Establece la pertenencia de un usuario a una o varias empresas.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# setCompanyMembership{#setcompanymembership}

Establece la pertenencia de un usuario a una o varias empresas.

Sintaxis

## Tipos de usuarios autorizados {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-3930dc6a016140178631083563598104}

**Entrada (setCompanyMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | No | Control de usuario. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sí | Matriz de empresas. |

**Salida (setCompanyMembershipParam)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-862c0cc32ce0407ab248028e690a8386}

Este ejemplo de código agrega un usuario a una empresa. Especifique varias empresas en la matriz de administración de la empresa si es necesario.

**Solicitar**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**Respuesta**

Ninguno.
