---
description: Obtiene información sobre un usuario. Utilice la dirección de correo electrónico y la contraseña de un usuario del sistema como credenciales para autorizar la solicitud. De lo contrario, la operación obtiene información sobre el usuario predeterminado.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 12%

---

# getUserInfo{#getuserinfo}

Obtiene información sobre un usuario. Utilice la dirección de correo electrónico y la contraseña de un usuario del sistema como credenciales para autorizar la solicitud. De lo contrario, la operación obtiene información sobre el usuario predeterminado.

Sintaxis

## Tipos de usuarios autorizados {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parámetros {#section-e87b3cb743494719925c9458eed433b6}

**Entrada (getUserInfoParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userHandle | `xsd:string` | No | Envíe al usuario cuya información desee devolver. |
| correo electrónico | `xsd:string` | No | Dirección de correo electrónico del usuario |

**Salida (getUserInfoReturn)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| userInfo | `types:User` | Sí | El nombre, apellidos, dirección de correo electrónico y función de un usuario, así como si el usuario es válido y cuándo caduca la contraseña del usuario. |

## Ejemplos {#section-98d77a2e360a438dbe240099bea26a65}

Este ejemplo de código devuelve información para el usuario de IPS predeterminado.

**Solicitar**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Respuesta**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
