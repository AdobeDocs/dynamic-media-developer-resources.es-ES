---
description: Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.
seo-description: Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.
seo-title: JobLogDetailAux
solution: Experience Manager
title: JobLogDetailAux
topic: Scene7 Image Production System API
uuid: df6f61f2-54f1-4996-938c-c3ea8c27551a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 5%

---


# JobLogDetailAux{#joblogdetailaux}

Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | Un mensaje auxiliar. |
| ` *`logType`*` | `xsd:string` | Tipo de registro: `IPSJobLog.gcUploadWarning` o `IPSJobLog.gcUploadError`. |
| ` *`datecreated`*` | `xsd:dateTime` | Fecha de creación del registro de trabajos auxiliar. |

