---
description: Detalles de advertencia o error para una actualización de uso en una operación batchSetAssetMetadata .
seo-description: Detalles de advertencia o error para una actualización de uso en una operación batchSetAssetMetadata .
seo-title: SetMetadataFault
solution: Experience Manager
title: SetMetadataFault
uuid: 22302bb0-914a-4d50-a188-9c3ee58e0481
feature: Dynamic Media Classic,SDK/API,Metadatos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 8%

---


# SetMetadataFault{#setmetadatafault}

Detalles de advertencia o error para una actualización de uso en una operación batchSetAssetMetadata .

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Recurso cuyos metadatos se configuraron de forma incorrecta. |
| `*`fieldHandle`*` | `xsd:string` | El identificador del campo de metadatos cuyo valor se estableció incorrectamente. |
| `*`código`*` | `xsd:int` | Código de error. |
| `*`razón`*` | `xsd:string` | Descripción de error (texto sin formato). |

