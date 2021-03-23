---
description: Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.
seo-description: Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Un mensaje auxiliar. |
| `*`logType`*` | `xsd:string` | Tipo de registro: `IPSJobLog.gcUploadWarning` o `IPSJobLog.gcUploadError`. |
| `*`dateCreated`*` | `xsd:dateTime` | Fecha de creación del registro de trabajos auxiliar. |

