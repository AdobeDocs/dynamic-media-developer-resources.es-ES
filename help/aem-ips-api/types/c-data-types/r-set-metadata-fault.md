---
description: Detalles de advertencia o error para una actualización de uso en una operación batchSetAssetMetadata .
solution: Experience Manager
title: SetMetadataFault
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Admin
exl-id: 49c6f355-4b5f-4b98-9a58-5732d56fdccb
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 12%

---

# SetMetadataFault{#setmetadatafault}

Detalles de advertencia o error para una actualización de uso en una operación batchSetAssetMetadata .

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| assetHandle | `xsd:string` | Recurso cuyos metadatos se configuraron de forma incorrecta. |
| fieldHandle | `xsd:string` | El identificador del campo de metadatos cuyo valor se estableció incorrectamente. |
| código | `xsd:int` | Código de error. |
| razón | `xsd:string` | Descripción de error (texto sin formato). |
