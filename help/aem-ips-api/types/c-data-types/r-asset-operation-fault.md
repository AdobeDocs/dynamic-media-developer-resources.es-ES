---
description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente no por lotes.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Developer,Administrator
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente no por lotes.

Sintaxis

## Parámetros {#section-c906f052f43e4785ba46d92b514b0923}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Identificador de recurso para la operación fallida. |
| `*`código`*` | `xsd:int` | Código de error de la operación. |
| `*`razón`*` | `xsd:string` | Descripción o motivo del error. |
