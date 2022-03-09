---
title: AssetOperationFault
description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente no por lotes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---

# AssetOperationFault{#assetoperationfault}

Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recursos por lotes. Los campos código y motivo corresponden a los campos de mensaje de error que se habrían generado para la operación equivalente no por lotes.

Sintaxis

## Parámetros {#section-c906f052f43e4785ba46d92b514b0923}

| Nombre | Tipo | Descripción |
|---|---|---|
| assetHandle | `xsd:string` | Identificador de recurso para la operación fallida. |
| código | `xsd:int` | Código de error de la operación. |
| razón | `xsd:string` | Descripción o motivo del error. |
