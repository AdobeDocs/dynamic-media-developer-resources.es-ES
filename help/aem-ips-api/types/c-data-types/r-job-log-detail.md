---
description: Información del registro de trabajos.
solution: Experience Manager
title: JobLogDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fe41a48a-4671-4179-a128-aadc7bc0683b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '61'
ht-degree: 8%

---

# JobLogDetail{#joblogdetail}

Información del registro de trabajos.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| logMessage | `xsd:string` | Mensajes en el registro de trabajos. |
| logType | `xsd:string` | Tipo de archivo de registro de trabajo. |
| assetName | `xsd:string` | Nombre del recurso en el registro de trabajos (opcional). |
| assetType | `xsd:string` | Opción del tipo de recurso. |
| assetHandle | `xsd:string` | Identificador de recurso al que se hace referencia en el registro de trabajos. |
| auxArray | `types:JobLogDetailAuxArray` | Proporciona información adicional detallada del registro de trabajos más allá de los cinco tipos de registro de trabajos descritos anteriormente. |
