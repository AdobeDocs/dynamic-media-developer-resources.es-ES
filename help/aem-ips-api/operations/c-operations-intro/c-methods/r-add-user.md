---
description: Crea una cuenta de usuario y la agrega a una o varias compañías.
seo-description: Crea una cuenta de usuario y la agrega a una o varias compañías.
seo-title: addUser
solution: Experience Manager
title: addUser
topic: Scene7 Image Production System API
uuid: b8c5ada6-470e-4795-a4f3-20750da709a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# addUser{#adduser}

Crea una cuenta de usuario y la agrega a una o varias compañías.

Al agregar un usuario a varias compañías, especifique dichas compañías mediante sus identificadores de compañía en `companyHandleArray`. Esta operación devuelve el identificador al usuario que acaba de agregar.

## Tipos de usuarios autorizados {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-40390a512e314b8d80ecffbb7729f6fb}

**Input (addUserParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`firstName`*` | `xsd:string` | Sí | El nombre del usuario. |
| ` *`lastName`*` | `xsd:string` | Sí | Apellido del usuario. |
| ` *`correo electrónico`*` | `xsd:string` | Sí | La dirección de correo electrónico del usuario. |
| ` *`defaultRole`*` | `xsd:string` | Sí | Define la función de un usuario en cada compañía a la que pertenece. Sin embargo, tenga en cuenta que la función `IpsAdmin` anula otras configuraciones por compañía. |
| ` *`contraseña`*` | `xsd:string` | Sí | Establece la contraseña del usuario |
| ` *`passwordExpires`*` | `xsd:dateTime` | No | Establece el período de caducidad de la contraseña. Proporcione el huso horario al pasar la solicitud. Los husos horarios se ajustan a la hora central. |
| ` *`isvalid`*` | `xsd:boolean` | Sí | Determina si el usuario es válido. |
| ` *`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | Sí | Matriz de controladores de compañía. |

**Output (addUserParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Sí | El identificador del usuario. |

## Ejemplos {#section-2547cef622734b71919eef849960b5cb}

La API de IPS devuelve un elemento de control de usuario que especifica el nuevo usuario.

**Solicitar**

```java
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

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

