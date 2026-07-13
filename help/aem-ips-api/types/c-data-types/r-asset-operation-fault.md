---
title: AssetOperationFault
description: Contiene información sobre las condiciones de advertencia o error generadas durante una operación de recurso por lotes. Los campos de código y motivo corresponden a los campos de mensaje de error que se habrían producido para la operación equivalente que no es por lotes.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: c97fc35b-76f8-4ff7-a1ae-e5f9749f376c
TQID: 'https://experienceleague.adobe.com/LCiMAp-8grDIfCEGX3sF2kBhDamlxZ8iFHT1BjBLkCY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 92
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

