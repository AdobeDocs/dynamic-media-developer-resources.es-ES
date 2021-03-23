---
description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente no por lotes.
seo-description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente no por lotes.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 5%

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

