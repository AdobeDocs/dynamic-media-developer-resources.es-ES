---
description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos de código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente que no es por lotes.
seo-description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos de código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente que no es por lotes.
seo-title: AssetOperationFault
solution: Experience Manager
title: AssetOperationFault
topic: Scene7 Image Production System API
uuid: fb6c5482-6e16-4561-927b-e4daeb7bdd7b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# AssetOperationFault{#assetoperationfault}

Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos de código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente que no es por lotes.

Sintaxis

## Parámetros {#section-c906f052f43e4785ba46d92b514b0923}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Identificador de recurso para la operación fallida. |
| ` *`código`*` | `xsd:int` | Código de error de la operación. |
| ` *`razón`*` | `xsd:string` | Descripción o razón del error. |

