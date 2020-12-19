---
description: Establece los atributos del usuario (por ejemplo, nombre, correo electrónico, función, etc.)
seo-description: Establece los atributos del usuario (por ejemplo, nombre, correo electrónico, función, etc.)
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
topic: Scene7 Image Production System API
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# setUserInfo{#setuserinfo}

Establece los atributos del usuario (por ejemplo, nombre, correo electrónico, función, etc.)

Sintaxis

## Tipos de usuarios autorizados {#section-6c28db5d15b3449492a73749e4f981ac}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parámetros {#section-71b457921fe74acb862a1e112e550211}

**Entrada (setUserInfoParam)**

| Nombre | Tipo | Obligatorio | Descripción |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | No | Identificador de usuario. |
| ` *`firstName`*` | `xsd:string` | Sí | Nombre. |
| ` *`lastName`*` | `xsd:string` | Sí | Apellido. |
| ` *`correo electrónico`*` | `xsd:string` | Sí | Correo electrónico del usuario. |
| ` *`defaultRole`*` | `xsd:string` | Sí | Define la función de un usuario en cada compañía a la que pertenece. Sin embargo, tenga en cuenta que la función `IpsAdmin` anula otras configuraciones por compañía. |
| ` *`passwordExpires`*` | `xsd:dateTime` | No | Fecha de caducidad de la contraseña establecida. |
| ` *`isvalid`*` | `xsd:boolean` | Sí | Determina si el usuario es un usuario IPS válido. |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sí | Matriz de controladores de compañía. |

**Salida (setUserInfoReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-272c103076fb4de0a53729e2f6bfb895}

**Solicitar**

```java
<setUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <firstName>test</firstName>
   <lastName>test</lastName>
   <email>test@test.test</email>
   <defaultRole>IpsAdmin</defaultRole>
   <isValid>true</isValid>
</setUserInfoParam>
```

**Respuesta**

Ninguno.
