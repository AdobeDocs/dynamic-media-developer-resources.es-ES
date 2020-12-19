---
description: Quita un usuario de una o varias compañías.
seo-description: Quita un usuario de una o varias compañías.
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
topic: Scene7 Image Production System API
uuid: af57fde0-2297-41da-87bf-f063fc313264
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# removeCompanyMembership{#removecompanymembership}

Quita un usuario de una o varias compañías.

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
| ` *`userHandle`*` | `xsd:string` | No | Identificador del usuario con la pertenencia que desea eliminar. |
| ` *`companyHandleArray`*` | `types:HandleArray` | Sí | Identificador de la compañía desde la que se está quitando al usuario. |

**Output (removeCompanyMembershipReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-6b7903195e8647a1bd0502f87387ca62}

Este ejemplo de código elimina a un usuario de una compañía. Omita el identificador de usuario opcional para eliminar a todos los usuarios de las compañías especificadas en la matriz del identificador de compañía.

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
