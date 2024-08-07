---
description: Establece atributos de usuario (por ejemplo, nombre, correo electrónico, función, etc.)
solution: Experience Manager
title: setUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d8f8fe53-a874-4b77-9084-9a369862a672
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 18%

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
| defaultRole | `xsd:string` | Sí | Establece la función de un usuario en cada compañía a la que pertenece. Sin embargo, tenga en cuenta que el rol `IpsAdmin` anula otras configuraciones por compañía. |
| passwordExpires | `xsd:dateTime` | No | Fecha de caducidad de la contraseña del conjunto. |
| isValid | `xsd:boolean` | Sí | Determina si el usuario es un usuario de IPS válido. |
| subscriptionArray | `types:CompanyMembershipUpdateArray` | Sí | Una matriz de identificadores de empresa. |

**Salida (setUserInfoReturn)**

La API de IPS no devuelve una respuesta para esta operación.

## Ejemplos {#section-272c103076fb4de0a53729e2f6bfb895}

**Solicitud**

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
