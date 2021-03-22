---
description: Información del registro de trabajos.
seo-description: Información del registro de trabajos.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 6%

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

