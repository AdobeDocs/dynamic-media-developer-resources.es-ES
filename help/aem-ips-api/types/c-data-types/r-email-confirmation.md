---
description: Envía un correo electrónico a un destinatario designado como respuesta a una operación cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---


# EmailConfirmation{#emailconfirmation}

Envía un correo electrónico a un destinatario designado como respuesta a una operación cdnCacheInvalidation.

Sintaxis

## Parámetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`ccOriginator`*` | `xsd:boolean` | Si es true, incluye la cuenta de usuario del servicio Web del usuario, que es una lista de correos electrónicos designados para recibir una confirmación por correo electrónico de la CDN de Dynamic Media. |
| `*`ccOtherArray`*` | `types:EmailArray` | Una matriz de direcciones de correo electrónico (5 como máximo) designada para recibir la notificación de confirmación de la CDN de Dynamic Media. |

