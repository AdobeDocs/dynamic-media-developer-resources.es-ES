---
description: Información del registro de trabajos.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '68'
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

