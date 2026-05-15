---
description: Usuario de recursos y tipos del sistema.
solution: Experience Manager
title: Usuario
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 5747f5bf-0175-4707-bfcb-1a9b97d7a24a
TQID: 'https://experienceleague.adobe.com/XM-2FjVie-j71W3Sc3-TypNJUFnz5AQuZZuGOx1fePs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
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
