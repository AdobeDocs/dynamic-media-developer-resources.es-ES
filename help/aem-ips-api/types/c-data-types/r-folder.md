---
description: Objeto de almacenamiento de recursos o archivos jerárquicos. Las carpetas pueden contener una (o más) subcarpetas.
solution: Experience Manager
title: Carpeta
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 74b44b1a-a92e-4c97-a93b-0cd4552f78ec
TQID: 'https://experienceleague.adobe.com/nh6zqOnt-bxAFmsHSHPRCMThKlOwi-9b9fep6ujKZyE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 70
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

