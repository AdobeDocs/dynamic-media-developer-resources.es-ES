---
description: Información del registro de trabajos.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 7%

---

# JobLogDetail{#joblogdetail}

Información del registro de trabajos.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`logMessage`*` | `xsd:string` | Mensajes en el registro de trabajos. |
| `*`logType`*` | `xsd:string` | Tipo de archivo de registro de trabajo. |
| `*`assetName`*` | `xsd:string` | Nombre del recurso en el registro de trabajos (opcional). |
| `*`assetType`*` | `xsd:string` | Opción del tipo de recurso. |
| `*`assetHandle`*` | `xsd:string` | Identificador de recurso al que se hace referencia en el registro de trabajos. |
| `*`auxArray`*` | `types:JobLogDetailAuxArray` | Proporciona información adicional detallada del registro de trabajos más allá de los cinco tipos de registro de trabajos descritos anteriormente. |
