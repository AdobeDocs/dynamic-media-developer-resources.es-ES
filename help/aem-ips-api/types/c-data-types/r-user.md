---
description: Usuario de recursos y tipos del sistema.
solution: Experience Manager
title: Usuario
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 9%

---

# [!DNL User]{#user}

Usuario de recursos y tipos del sistema.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| userHandle | `xsd:string` | Controlador de usuario. |
| firstName | `xsd:string` | Nombre del usuario. |
| lastName | `xsd:string` | Apellidos del usuario. |
| correo electrónico | `xsd:string` | dirección de correo electrónico |
| defaultRole | `xsd:string` | Establece la función de un usuario en cada compañía a la que pertenece. Sin embargo, el rol de usuario `IpsAmin` invalida otros roles de usuario. |
| isValid | `xsd:boolean` | Determina si el usuario es válido. |
| passwordExpires | `xsd:dateTime` | Establece fecha de caducidad de contraseña. |
