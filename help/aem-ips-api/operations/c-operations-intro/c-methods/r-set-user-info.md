---
description: Establece los atributos de usuario (por ejemplo, nombre, correo electrónico, función, etc.)
seo-description: Establece los atributos de usuario (por ejemplo, nombre, correo electrónico, función, etc.)
seo-title: setUserInfo
solution: Experience Manager
title: setUserInfo
uuid: 52e3a21e-1dd5-4f9d-b460-506d280fff47
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 18%

---


# setUserInfo{#setuserinfo}

Establece los atributos de usuario (por ejemplo, nombre, correo electrónico, función, etc.)

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
| `*`userHandle`*` | `xsd:string` | No | Control de usuario. |
| `*`firstName`*` | `xsd:string` | Sí | Nombre. |
| `*`lastName`*` | `xsd:string` | Sí | Apellido. |
| `*`correo electrónico`*` | `xsd:string` | Sí | Correo electrónico del usuario. |
| `*`defaultRole`*` | `xsd:string` | Sí | Establece la función de un usuario en cada empresa a la que pertenece. No obstante, tenga en cuenta que la función `IpsAdmin` anula otras configuraciones por empresa. |
| `*`passwordExpires`*` | `xsd:dateTime` | No | Establezca la fecha de caducidad de la contraseña. |
| `*`isValid`*` | `xsd:boolean` | Sí | Determina si el usuario es un usuario IPS válido. |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | Sí | Matriz de controladores de empresa. |

**Salida (setUserInfoReturn)**

La API IPS no devuelve una respuesta para esta operación.

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
