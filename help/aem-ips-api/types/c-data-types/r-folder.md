---
description: Objeto de almacenamiento de recursos o archivos jerárquicos. Las carpetas pueden contener una (o más) subcarpetas.
solution: Experience Manager
title: Carpeta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 8%

---

# [!DNL Folder]{#folder}

Objeto de almacenamiento de recursos o archivos jerárquicos. Las carpetas pueden contener una (o más) subcarpetas.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| folderHandle | `xsd:string` | Controlador de carpeta. |
| [!DNL path] | `xsd:string` | Ruta de carpeta. |
| lastModified | `xsd:dateTime` | Fecha de la última modificación. |
| childLastModified | `xsd:dateTime` | Fecha de la última modificación de las subcarpetas y los recursos secundarios de la carpeta. |
| permissionsSetHandle | `xsd:string` | Controlador de permisos de carpeta. |
| hasSubfolder | `types:Boolean` | Determina si una carpeta tiene subcarpetas. |
| subfolderArray | `types:FolderArray` | Matriz de subcarpetas de una carpeta. |
