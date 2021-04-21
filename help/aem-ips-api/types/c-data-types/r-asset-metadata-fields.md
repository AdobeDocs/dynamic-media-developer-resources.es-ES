---
description: Devuelve definiciones de campos de metadatos para tipos de recursos especificados.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '58'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

Devuelve definiciones de campos de metadatos para tipos de recursos especificados.

Sintaxis

## Parámetros {#section-5ad771540c5f40c187b35e34aac19305}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo de recurso asociado a definiciones de campo (consulte &quot;Tipos de recursos&quot; para ver los valores). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Matriz de definiciones de campo de metadatos asociadas al tipo de recurso especificado en `assetType`. |

