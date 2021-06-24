---
description: Archivo jerárquico u objeto de almacenamiento de recursos. Las carpetas pueden contener una o más subcarpetas.
solution: Experience Manager
title: Carpeta
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
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
