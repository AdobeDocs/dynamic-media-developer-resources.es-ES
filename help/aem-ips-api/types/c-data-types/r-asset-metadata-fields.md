---
description: Devuelve definiciones de campos de metadatos para tipos de recursos especificados.
solution: Experience Manager
title: AssetMetadataFields
feature: Dynamic Media Classic,SDK/API,Metadatos,Administración de activos
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '56'
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
