---
description: Quita un usuario de una o varias empresas.
seo-description: Quita un usuario de una o varias empresas.
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
uuid: af57fde0-2297-41da-87bf-f063fc313264
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 10%

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
| `*`userHandle`*` | `xsd:string` | No | El identificador del usuario con la pertenencia que desea eliminar. |
| `*`companyHandleArray`*` | `types:HandleArray` | Sí | El identificador de la empresa desde la que se va a quitar el usuario. |

**Salida (removeCompanyMembershipReturn)**

La API IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-6b7903195e8647a1bd0502f87387ca62}

Este ejemplo de código elimina a un usuario de una empresa. Omita el identificador de usuario opcional para eliminar todos los usuarios de las empresas especificadas en la matriz de administración de la empresa.

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
