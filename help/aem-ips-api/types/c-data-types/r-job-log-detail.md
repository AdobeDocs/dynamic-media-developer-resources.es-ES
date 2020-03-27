---
description: Información del registro de trabajos.
seo-description: Información del registro de trabajos.
seo-title: JobLogDetail
solution: Experience Manager
title: JobLogDetail
topic: Scene7 Image Production System API
uuid: cb1879d7-a554-4ff0-bba0-0758c43f2a99
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# JobLogDetail{#joblogdetail}

Información del registro de trabajos.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`logMessage`*` | `xsd:string` | Mensajes en el registro de trabajos. |
| ` *`logType`*` | `xsd:string` | Tipo de archivo de registro de trabajo. |
| ` *`assetName`*` | `xsd:string` | Nombre del recurso en el registro de trabajos (opcional). |
| ` *`assetType`*` | `xsd:string` | Opción del tipo de recurso. |
| ` *`assetHandle`*` | `xsd:string` | Identificador de recurso al que se hace referencia en el registro de trabajos. |
| ` *`auxArray`*` | `types:JobLogDetailAuxArray` | Proporciona información adicional detallada del registro de trabajos más allá de los cinco tipos de registro de trabajos descritos anteriormente. |

