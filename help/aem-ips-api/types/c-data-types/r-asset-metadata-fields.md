---
description: Devuelve definiciones de campo de metadatos para tipos de recurso especificados.
seo-description: Devuelve definiciones de campo de metadatos para tipos de recurso especificados.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
topic: Dynamic Media Image Production System API
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 8%

---


# AssetMetadataFields{#assetmetadatafields}

Devuelve definiciones de campo de metadatos para tipos de recurso especificados.

Sintaxis

## Parámetros {#section-5ad771540c5f40c187b35e34aac19305}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo de recurso asociado con definiciones de campo (consulte &quot;Tipos de recursos&quot; para conocer los valores). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Matriz de definiciones de campo de metadatos asociadas con el tipo de recurso especificado en `assetType`. |

