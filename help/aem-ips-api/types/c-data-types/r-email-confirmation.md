---
description: Envía un correo electrónico a un destinatario designado como respuesta a una operación cdnCacheInvalidation .
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 6%

---

# EmailConfirmation{#emailconfirmation}

Envía un correo electrónico a un destinatario designado como respuesta a una operación cdnCacheInvalidation .

Sintaxis

## Parámetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nombre | Tipo | Descripción |
|---|---|---|
| ccOriginator | `xsd:boolean` | Si es true, incluye la cuenta de usuario del servicio web del usuario, que es una lista de correos electrónicos designados para recibir una confirmación por correo electrónico de la CDN de Dynamic Media. |
| ccOthersArray | `types:EmailArray` | Una matriz de direcciones de correo electrónico (5 como máximo) designadas para recibir la notificación de confirmación de la CDN de Dynamic Media. |
