---
description: Agrega un usuario a una o varias empresas.
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
TQID: 'https://experienceleague.adobe.com/VNnc-lxt0VHsrYBfJHUVTfK7Hqb42u-P-DtxNdQvS8o'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 83
ht-degree: 12%

---

# addCompanyMembership{#addcompanymembership}

Agrega un usuario a una o varias empresas.

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
| userHandle | `xsd:string` | No | El identificador del usuario cuya pertenencia desea agregar. |
| subscriptionArray | `types:CompanyMembershipUpdateArray` | Sí | Una matriz de empresas a las que agrega el usuario. |

**Salida (addCompanyMembershipReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-5469f88bac7047cca131faa6b021e437}

En este ejemplo se utiliza companyHandleArray para agregar un usuario a una sola compañía.

**Solicitud**

```javascript {.line-numbers}
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**Respuesta**

Ninguno.
