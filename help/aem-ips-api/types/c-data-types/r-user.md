---
description: Un usuario de recursos y tipos en el sistema.
solution: Experience Manager
title: Usuario
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 11%

---

# Usuario{#user}

Un usuario de recursos y tipos en el sistema.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| userHandle | `xsd:string` | Control de usuario. |
| firstName | `xsd:string` | Nombre de usuario. |
| lastName | `xsd:string` | Apellido de usuario. |
| correo electrónico | `xsd:string` | dirección de correo electrónico. |
| defaultRole | `xsd:string` | Establece la función de un usuario en cada empresa a la que pertenece. Sin embargo, la función de usuario `IpsAmin` anula otras funciones de usuario. |
| isValid | `xsd:boolean` | Determina si el usuario es válido. |
| passwordExpires | `xsd:dateTime` | Establece la fecha de caducidad de la contraseña. |
