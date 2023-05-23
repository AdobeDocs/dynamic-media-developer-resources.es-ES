---
description: Establece atributos de usuario (por ejemplo, nombre, correo electrónico, función, etc.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 21%

---

# setUserInfo{#setuserinfo}

Establece atributos de usuario (por ejemplo, nombre, correo electrónico, función, etc.)

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
| userHandle | `xsd:string` | No | Controlador de usuario. |
| firstName | `xsd:string` | Sí | Nombre. |
| lastName | `xsd:string` | Sí | Apellido. |
| correo electrónico | `xsd:string` | Sí | Correo electrónico del usuario. |
| defaultRole | `xsd:string` | Sí | Establece la función de un usuario en cada compañía a la que pertenece. Sin embargo, tenga en cuenta que `IpsAdmin` la función anula otras configuraciones por empresa. |
| passwordExpires | `xsd:dateTime` | No | Fecha de caducidad de la contraseña del conjunto. |
| isValid | `xsd:boolean` | Sí | Determina si el usuario es un usuario de IPS válido. |
| subscriptionArray | `types:CompanyMembershipUpdateArray` | Sí | Una matriz de identificadores de empresa. |

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
