---
description: Establece la pertenencia de un usuario a una o varias compañías.
seo-description: Establece la pertenencia de un usuario a una o varias compañías.
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
topic: Scene7 Image Production System API
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setCompanyMembership{#setcompanymembership}

Establece la pertenencia de un usuario a una o varias compañías.

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
| ` *`userHandle`*` | `xsd:sting` | No | Identificador de usuario. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sí | Matriz de compañías. |

**Output (setCompanyMembershipParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-862c0cc32ce0407ab248028e690a8386}

Este ejemplo de código agrega un usuario a una compañía. Especifique varias compañías en la matriz de control de compañía si es necesario.

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
