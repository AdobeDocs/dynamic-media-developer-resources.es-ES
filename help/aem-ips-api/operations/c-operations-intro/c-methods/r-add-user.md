---
description: Crea una cuenta de usuario y la agrega a una o varias empresas.
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 11%

---

# addUser{#adduser}

Crea una cuenta de usuario y la agrega a una o varias empresas.

Cuando agregue un usuario a varias empresas, especifique esas empresas por sus identificadores de empresa en `companyHandleArray`. Esta operación devuelve el identificador al usuario que acaba de agregar.

## Tipos de usuarios autorizados {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-40390a512e314b8d80ecffbb7729f6fb}

**Entrada (addUserParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| firstName | `xsd:string` | Sí | El nombre del usuario. |
| lastName | `xsd:string` | Sí | El apellido del usuario. |
| correo electrónico | `xsd:string` | Sí | La dirección de correo electrónico del usuario. |
| defaultRole | `xsd:string` | Sí | Establece la función de un usuario en cada compañía a la que pertenece. Sin embargo, tenga en cuenta que el rol `IpsAdmin` anula otras configuraciones por compañía. |
| contraseña | `xsd:string` | Sí | Establece la contraseña del usuario |
| passwordExpires | `xsd:dateTime` | No | Establece el período de caducidad de la contraseña. Proporcione la zona horaria al pasar la solicitud. Las zonas horarias se ajustan a la Hora central. |
| isValid | `xsd:boolean` | Sí | Determina si el usuario es válido. |
| subscriptionArray | `xsd:CompanyMembershipUpdateArray` | Sí | Una matriz de identificadores de empresa. |

**Salida (addUserParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandle | `xsd:string` | Sí | El identificador del usuario. |

## Ejemplos {#section-2547cef622734b71919eef849960b5cb}

La API de IPS devuelve un elemento de identificador de usuario que especifica el nuevo usuario.

**Solicitud**

```java {.line-numbers}
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**Respuesta**

```java {.line-numbers}
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
