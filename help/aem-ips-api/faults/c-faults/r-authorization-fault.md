---
description: Se activa cuando un usuario autenticado no tiene permisos suficientes para realizar una tarea.
solution: Experience Manager
title: authorizationFault
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 76965735-92d8-46be-b589-67cad3b987dc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 25%

---

# authorizationFault{#authorizationfault}

Se activa cuando un usuario autenticado no tiene permisos suficientes para realizar una tarea.

Sintaxis

## Tipos de errores {#section-1f04dec489714ee6bb7256fae6ab7730}

| ID | Fallo |
|---|---|
| 20000 | `AUTHORIZATION_FAULT_CODE_INVALID_COMPANY` |
| 20001 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USERNAME` |
| 20002 | `AUTHORIZATION_FAULT_CODE_INVALID_REQUEST_USER` |
| 2003 | `AUTHORIZATION_FAULT_CODE_NO_OPERATION_PERMISSION` |
| 2004 | `AUTHORIZATION_FAULT_CODE_NO_IMPERSONATION_PERMISSION` |
| 2005 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_PARAMETER_VALUE` |
| 2006 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_COMPANY` |
| 2007 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_REQUEST_USER` |
| 2008 | `AUTHORIZATION_FAULT_CODE_ILLEGAL_ACCESS_GROUP` |
| 2009 | `AUTHORIZATION_FAULT_CODE_MISSING_PERMISSION` |

## Campos predeterminados {#section-4e3e41f41fea402a9ae314bfd05f663e}

| Nombre | Tipo | Descripción |
|---|---|---|
| `code` | `xsd:int` | ID de error |
| `reason` | `xsd:string` | Un mensaje informativo que describe el error. |
