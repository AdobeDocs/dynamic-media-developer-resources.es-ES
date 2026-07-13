---
description: Establece la pertenencia de un usuario a una o varias empresas.
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
TQID: 'https://experienceleague.adobe.com/Nb9XjcAX4NMyne48B9QoVqlhUnhCE5ufIHILopUeAf0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 13%

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
| userHandle | `xsd:sting` | No | Controlador de usuario. |
| subscriptionArray | `types:CompanyMembershipUpdateArray` | Sí | Matriz de empresas. |

**Salida (setCompanyMembershipParam)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-862c0cc32ce0407ab248028e690a8386}

Este ejemplo de código agrega un usuario a una compañía. Especifique varias empresas en la matriz de identificadores de la empresa si es necesario.

**Solicitud**

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

