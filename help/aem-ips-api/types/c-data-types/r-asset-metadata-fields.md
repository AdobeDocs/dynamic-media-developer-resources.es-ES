---
title: AssetMetadataFields
description: Devuelve definiciones de campos de metadatos para tipos de recursos especificados.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: ad2a45fc-1f30-4b8b-be7c-84cc60c7bd4b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '47'
ht-degree: 10%

---

# [!DNL AssetMetadataFields]{#assetmetadatafields}

Devuelve definiciones de campos de metadatos para tipos de recursos especificados.

Sintaxis

## Parámetros {#section-5ad771540c5f40c187b35e34aac19305}

| Nombre | Tipo | Descripción |
|---|---|---|
| assetType | `xsd:string` | Tipo de recurso asociado a definiciones de campo (consulte &quot;Tipos de recursos&quot; para ver los valores). |
| fieldArray | `types:MetadataFieldArray` | Matriz de definiciones de campos de metadatos asociadas al tipo de recurso especificado en `assetType`. |
