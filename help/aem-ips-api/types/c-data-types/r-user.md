---
description: Un usuario de los recursos y tipos del sistema.
seo-description: Un usuario de los recursos y tipos del sistema.
seo-title: Usuario
solution: Experience Manager
title: Usuario
topic: Scene7 Image Production System API
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Usuario{#user}

Un usuario de los recursos y tipos del sistema.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`userHandle`*` | `xsd:string` | Identificador de usuario. |
| ` *`firstName`*` | `xsd:string` | Nombre de usuario. |
| ` *`lastName`*` | `xsd:string` | Apellido del usuario. |
| ` *`correo electrónico`*` | `xsd:string` | dirección de correo electrónico. |
| ` *`defaultRole`*` | `xsd:string` | Define la función de un usuario en cada compañía a la que pertenece. Sin embargo, la función de usuario `IpsAmin` anula otras funciones de usuario. |
| ` *`isvalid`*` | `xsd:boolean` | Determina si el usuario es válido. |
| ` *`passwordExpires`*` | `xsd:dateTime` | Establece la fecha de caducidad de la contraseña. |

