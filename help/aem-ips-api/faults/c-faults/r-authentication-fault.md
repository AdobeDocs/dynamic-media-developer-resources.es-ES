---
description: Se desencadena cuando un usuario no se puede autenticar.
solution: Experience Manager
title: authenticationFault
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '37'
ht-degree: 21%

---


# authenticationFault{#authenticationfault}

Se desencadena cuando un usuario no se puede autenticar.

Sintaxis

## Tipos de errores {#section-8ac4519c1dbb4c8b9c46ac9d1f44a054}

| ID | Error |
|---|---|
| 10000 | `AUTHENTICATION_FAULT_CODE_NO_CREDENTIALS` |
| 10001 | `AUTHENTICATION_FAULT_CODE_INVALID_CREDENTIALS` |
| 10002 | `AUTHENTICATION_FAULT_CODE_INVALID_USER` |

## Campos de error {#section-1fe84846a7154b03ab49552810ee9ac3}

| Nombre | Tipo | Descripción |
|---|---|---|
| `code` | `xsd:int` | ID de error |
| `reason` | `xsd:string` | Un mensaje informativo que describe el error. |
