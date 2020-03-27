---
description: Envía un correo electrónico a un destinatario designado como respuesta a una operación cdnCacheInvalidation.
seo-description: Envía un correo electrónico a un destinatario designado como respuesta a una operación cdnCacheInvalidation.
seo-title: EmailConfirmation
solution: Experience Manager
title: EmailConfirmation
topic: Scene7 Image Production System API
uuid: c3b7aada-a03a-418d-80b2-31a86a1af786
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# EmailConfirmation{#emailconfirmation}

Envía un correo electrónico a un destinatario designado como respuesta a una operación cdnCacheInvalidation.

Sintaxis

## Parámetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`ccOriginator`*` | `xsd:boolean` | Si el valor es true, incluye la cuenta de usuario del servicio Web del usuario, que es una lista de correos electrónicos designados para recibir una confirmación por correo electrónico de la CDN de Scene7. |
| ` *`ccOtherArray`*` | `types:EmailArray` | Matriz de direcciones de correo electrónico (5 como máximo) designada para recibir la notificación de confirmación de la CDN de Scene7. |

