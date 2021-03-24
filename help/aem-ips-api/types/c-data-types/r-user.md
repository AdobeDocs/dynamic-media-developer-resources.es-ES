---
description: Un usuario de recursos y tipos en el sistema.
solution: Experience Manager
title: Usuario
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
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

