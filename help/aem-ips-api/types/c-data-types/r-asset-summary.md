---
description: Resultados de búsqueda de metadatos que contienen información resumida sobre un recurso.
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Administración de activos
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 11%

---


# AssetSummary{#assetsummary}

Resultados de búsqueda de metadatos que contienen información resumida sobre un recurso.

Sintaxis

## Parámetros {#section-ebc75cc024d94c439260d2e71873cc74}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Identificador de recurso. |
| `*`type`*` | `xsd:string` | Tipo de recurso. La constante &quot;Tipos de recursos&quot; define los valores posibles. Opcional. |
| `*`name`*` | `xsd:string` | Nombre del recurso. Opcional. |
| `*`carpeta`*` | `xsd:string` | La carpeta que contiene el recurso. |
| `*`filename`*` | `xsd:string` | Nombre del archivo del recurso. |
| `*`creado`*` | `xsd:dateTime` | Fecha de creación del recurso. |
| `*`createUser`*` | `xsd:string` | El usuario que creó el recurso. |
| `*`lastModified`*` | `xsd:dateTime` | La fecha de la última actualización del recurso. |
| `*`lastModifyUser`*` | `xsd:string` | El último usuario que modificó el recurso. |
| `*`metadataArray`*` | `types:MetadataArray` | Matriz de valores de metadatos asociados al recurso. |
| `*`puntaje`*` | `xsd:double` | Define la precisión en caso de una búsqueda de similitud (0 = sin coincidencia, 1 = coincidencia exacta). |
| `*`scoreDetail`*` | `xsd:string` | Contiene información detallada sobre áreas similares como resultado de una búsqueda por similitudes. |

