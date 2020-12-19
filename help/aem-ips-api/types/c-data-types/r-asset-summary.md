---
description: Resultados de búsqueda de metadatos que contienen información resumida sobre un recurso.
seo-description: Resultados de búsqueda de metadatos que contienen información resumida sobre un recurso.
seo-title: AssetSummary
solution: Experience Manager
title: AssetSummary
topic: Scene7 Image Production System API
uuid: 0ac8f900-c16c-409d-b83c-3bdf0ad28fac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# AssetSummary{#assetsummary}

Resultados de búsqueda de metadatos que contienen información resumida sobre un recurso.

Sintaxis

## Parámetros {#section-ebc75cc024d94c439260d2e71873cc74}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Identificador de recurso. |
| ` *`type`*` | `xsd:string` | Tipo de recurso. La constante &quot;Tipos de recursos&quot; define los valores posibles. Opcional. |
| ` *`name`*` | `xsd:string` | Nombre del recurso. Opcional. |
| ` *`carpeta`*` | `xsd:string` | Carpeta que contiene el recurso. |
| ` *`filename`*` | `xsd:string` | Nombre de archivo del recurso. |
| ` *`creado`*` | `xsd:dateTime` | Fecha de creación de recursos. |
| ` *`createUser`*` | `xsd:string` | El usuario que creó el recurso. |
| ` *`lastModified`*` | `xsd:dateTime` | Fecha en la que se actualizó el recurso por última vez. |
| ` *`lastModifyUser`*` | `xsd:string` | Último usuario que modificó el recurso. |
| ` *`metadataArray`*` | `types:MetadataArray` | Matriz de valores de metadatos asociados al recurso. |
| ` *`puntaje`*` | `xsd:double` | Define la precisión en caso de búsqueda de similitudes (0 = sin coincidencia, 1 = coincidencia exacta). |
| ` *`scoreDetail`*` | `xsd:string` | Contiene información detallada sobre áreas similares como resultado de una búsqueda por similitudes. |

