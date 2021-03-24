---
description: Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o más subcarpetas.
solution: Experience Manager
title: Carpeta
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 10%

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

