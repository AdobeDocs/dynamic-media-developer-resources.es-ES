---
description: Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o más subcarpetas.
seo-description: Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o más subcarpetas.
seo-title: Carpeta
solution: Experience Manager
title: Carpeta
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# Carpeta{#folder}

Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o más subcarpetas.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Identificador de carpeta. |
| `*`ruta`*` | `xsd:string` | Ruta de carpeta. |
| `*`lastModified`*` | `xsd:dateTime` | Fecha de la última modificación. |
| `*`childLastModified`*` | `xsd:dateTime` | Fecha de la última modificación para subcarpetas y recursos secundarios de carpeta. |
| `*`permissionsSetHandle`*` | `xsd:string` | Identificador de permisos de carpeta. |
| `*`hasSubfolder`*` | `types:Boolean` | Determina si una carpeta tiene subcarpetas. |
| `*`subfolderArray`*` | `types:FolderArray` | Matriz de subcarpetas de una carpeta. |

