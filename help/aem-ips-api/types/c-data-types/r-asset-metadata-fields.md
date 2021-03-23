---
description: Devuelve definiciones de campos de metadatos para tipos de recursos especificados.
seo-description: Devuelve definiciones de campos de metadatos para tipos de recursos especificados.
seo-title: AssetMetadataFields
solution: Experience Manager
title: AssetMetadataFields
uuid: aefb734c-7609-4227-ae2c-48a1469740ec
feature: Dynamic Media Classic,SDK/API,Metadatos,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 7%

---


# AssetMetadataFields{#assetmetadatafields}

Devuelve definiciones de campos de metadatos para tipos de recursos especificados.

Sintaxis

## Parámetros {#section-5ad771540c5f40c187b35e34aac19305}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`assetType`*` | `xsd:string` | Tipo de recurso asociado a definiciones de campo (consulte &quot;Tipos de recursos&quot; para ver los valores). |
| `*`fieldArray`*` | `types:MetadataFieldArray` | Matriz de definiciones de campo de metadatos asociadas al tipo de recurso especificado en `assetType`. |

