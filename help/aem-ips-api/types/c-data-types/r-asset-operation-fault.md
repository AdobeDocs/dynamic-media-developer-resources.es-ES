---
title: AssetOperationFault
description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recurso por lotes. Los campos de código y motivo corresponden a los campos de mensaje de error que se habrían producido para la operación equivalente que no es por lotes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 7%

---

# [!DNL AssetOperationFault]{#assetoperationfault}

Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recurso por lotes. Los campos de código y motivo corresponden a los campos de mensaje de error que se habrían producido para la operación equivalente que no es por lotes.

Sintaxis

## Parámetros {#section-c906f052f43e4785ba46d92b514b0923}

| Nombre | Tipo | Descripción |
|---|---|---|
| assetHandle | `xsd:string` | Controlador de recurso para la operación fallida. |
| código | `xsd:int` | Código de fallo de funcionamiento. |
| razón | `xsd:string` | Descripción o motivo del error. |
