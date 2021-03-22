---
description: Un usuario de recursos y tipos en el sistema.
seo-description: Un usuario de recursos y tipos en el sistema.
seo-title: Usuario
solution: Experience Manager
title: Usuario
uuid: 37e939ae-dd1a-4550-aa93-b7b091ebc339
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 10%

---


# Usuario{#user}

Un usuario de recursos y tipos en el sistema.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`userHandle`*` | `xsd:string` | Control de usuario. |
| `*`firstName`*` | `xsd:string` | Nombre de usuario. |
| `*`lastName`*` | `xsd:string` | Apellido de usuario. |
| `*`correo electrónico`*` | `xsd:string` | dirección de correo electrónico. |
| `*`defaultRole`*` | `xsd:string` | Establece la función de un usuario en cada empresa a la que pertenece. Sin embargo, la función de usuario `IpsAmin` anula otras funciones de usuario. |
| `*`isValid`*` | `xsd:boolean` | Determina si el usuario es válido. |
| `*`passwordExpires`*` | `xsd:dateTime` | Establece la fecha de caducidad de la contraseña. |

