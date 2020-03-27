---
description: Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o varias subcarpetas.
seo-description: Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o varias subcarpetas.
seo-title: Carpeta
solution: Experience Manager
title: Carpeta
topic: Scene7 Image Production System API
uuid: 8ba8d9cb-c4e5-423c-b8cb-ba8751952771
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Carpeta{#folder}

Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o varias subcarpetas.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Identificador de carpeta. |
| ` *`ruta`*` | `xsd:string` | Ruta de carpeta. |
| ` *`lastModified`*` | `xsd:dateTime` | Fecha de la última modificación. |
| ` *`childLastModified`*` | `xsd:dateTime` | Fecha de la última modificación para subcarpetas y recursos secundarios de carpetas. |
| ` *`permissionsSetHandle`*` | `xsd:string` | Identificador de permisos de carpetas. |
| ` *`hasSubfolder`*` | `types:Boolean` | Determina si una carpeta tiene subcarpetas. |
| ` *`subfolderArray`*` | `types:FolderArray` | Matriz de subcarpetas de una carpeta. |

