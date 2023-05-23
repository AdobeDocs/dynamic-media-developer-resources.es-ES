---
description: Se produce cuando un usuario no puede autenticarse.
solution: Experience Manager
title: authenticationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fce5c227-9291-4d17-801f-4ef4b8d43eb4
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 21%

---

# authenticationFault{#authenticationfault}

Se produce cuando un usuario no puede autenticarse.

Sintaxis

## Tipos de errores {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Fallo |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Campos de errores {#section-1fe84846a7154b03ab49552810ee9ac3}

| Nombre | Tipo | Descripción |
|---|---|---|
| `code` | `xsd:int` | ID de error |
| `reason` | `xsd:string` | Un mensaje informativo que describe el error. |
