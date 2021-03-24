---
description: ipsApiFault
solution: Experience Manager
title: ipsApiFault
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '32'
ht-degree: 28%

---


# ipsApiFault{#ipsapifault}

Sintaxis

## Tipos de errores {#section-425697675cac4b2ab5c48bd463956401}

| ID | Fallo |
|---|---|
| 30000 | `IPS_API_FAULT_CODE_EXCEPTION` |
| 30001 | `IPS_API_FAULT_CODE_INVALID_PARAMETER` |
| 30002 | `IPS_API_FAULT_CODE_MISSING_PARAMETER` |
| 30003 | `IPS_API_FAULT_CODE_INVALID_REQUEST_XML` |

## Campos predeterminados {#section-37fe1aef1d5f4ca480071ca933aba826}

| Nombre | Tipo | Descripción |
|---|---|---|
| `code` | `xsd:int` | ID de error |
| `reason` | `xsd:string` | Un mensaje informativo que describe el error. |

