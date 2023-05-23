---
description: Resultados de búsqueda de metadatos que contienen información resumida sobre un recurso.
solution: Experience Manager
title: AssetSummary
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 25f16a2b-6cd8-485f-a6bd-2a9bc9b3243b
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 12%

---

# [!DNL AssetSummary]{#assetsummary}

Resultados de búsqueda de metadatos que contienen información resumida sobre un recurso.

Sintaxis

## Parámetros {#section-ebc75cc024d94c439260d2e71873cc74}

| Nombre | Tipo | Descripción |
|---|---|---|
| assetHandle | `xsd:string` | Controlador de recurso. |
| tipo | `xsd:string` | Tipo de recurso. La constante &quot;Tipos de recursos&quot; define los valores posibles. Opcional. |
| nombre | `xsd:string` | Nombre del recurso. Opcional. |
| carpeta | `xsd:string` | La carpeta que contiene el recurso. |
| filename | `xsd:string` | Nombre de archivo del recurso. |
| creado | `xsd:dateTime` | Fecha de creación del recurso. |
| createUser | `xsd:string` | El usuario que creó el recurso. |
| lastModified | `xsd:dateTime` | Fecha en la que se actualizó el recurso por última vez. |
| lastModifyUser | `xsd:string` | El último usuario que modificó el recurso. |
| metadataArray | `types:MetadataArray` | Matriz de valores de metadatos asociados al recurso. |
| puntaje | `xsd:double` | Define la precisión en caso de búsqueda por similitud (0 = sin coincidencia, 1 = coincidencia exacta). |
| scoreDetail | `xsd:string` | Contiene información detallada sobre áreas similares como resultado de una búsqueda de similitudes. |
