---
description: Envía un mensaje de correo electrónico a un destinatario designado en respuesta a una operación cdnCacheInvalidation.
solution: Experience Manager
title: EmailConfirmation
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: b4698637-a897-47fa-92d4-4ab400e56962
TQID: 'https://experienceleague.adobe.com/h9ZZRR0zR347mzSifomCmtNW5GorTC6fgGjeSRf52KU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 78
ht-degree: 6%

---

# [!DNL EmailConfirmation]{#emailconfirmation}

Envía un mensaje de correo electrónico a un destinatario designado en respuesta a una operación cdnCacheInvalidation.

Sintaxis

## Parámetros {#section-490717fe96bf40c2a5a2f7ccbfaab3d0}

| Nombre | Tipo | Descripción |
|---|---|---|
| ccOriginator | `xsd:boolean` | Si es true, incluye la cuenta de usuario del servicio web del usuario, que es una lista de correos electrónicos designados para recibir una confirmación por correo electrónico de la CDN de Dynamic Media. |
| ccOthersArray | `types:EmailArray` | Una matriz de direcciones de correo electrónico (5 como máximo) designadas para recibir la notificación de confirmación de la CDN de Dynamic Media. |

