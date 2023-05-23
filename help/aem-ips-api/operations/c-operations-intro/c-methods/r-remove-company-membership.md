---
description: Quita un usuario de una o varias empresas.
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 12%

---

# removeCompanyMembership{#removecompanymembership}

Quita un usuario de una o varias empresas.

Sintaxis

## Tipos de usuarios autorizados {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-6dfce5e44d8a4799afd0c231a0b10463}

**Entrada (removeCompanyMembershipParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandle | `xsd:string` | No | El identificador del usuario con la pertenencia que desea eliminar. |
| companyHandleArray | `types:HandleArray` | Sí | El identificador de la compañía de la que elimina el usuario. |

**Salida (removeCompanyMembershipReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-6b7903195e8647a1bd0502f87387ca62}

Este ejemplo de código quita un usuario de una compañía. Omita el identificador de usuario opcional para quitar todos los usuarios de las empresas especificadas en la matriz de identificadores de la empresa.

**Solicitar**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**Respuesta**

Ninguno.
