---
description: Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.
solution: Experience Manager
title: JobLogDetailAux
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 789736c5-d74d-4970-9665-b43e316aca69
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 7%

---

# [!DNL JobLogDetailAux]{#joblogdetailaux}

Contiene mensajes adicionales asociados al mensaje de registro de trabajos principal (JobDetail). Incluye advertencias y otros detalles asociados con el recurso procesado actualmente.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| logMessage | `xsd:string` | Un mensaje auxiliar. |
| logType | `xsd:string` | Tipo de registro: `IPSJobLog.gcUploadWarning` o `IPSJobLog.gcUploadError`. |
| dateCreated | `xsd:dateTime` | Fecha de creación del registro de trabajos auxiliar. |
