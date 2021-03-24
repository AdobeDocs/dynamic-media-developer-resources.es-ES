---
description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente no por lotes.
solution: Experience Manager
title: AssetOperationFault
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
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

