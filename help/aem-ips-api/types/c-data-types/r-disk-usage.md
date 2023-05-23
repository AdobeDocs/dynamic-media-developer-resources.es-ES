---
description: Estadísticas de espacio en disco de un recurso o una carpeta.
solution: Experience Manager
title: UsoDeDisco
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 14%

---

# [!DNL DiskUsage]{#diskusage}

Estadísticas de espacio en disco de un recurso o una carpeta.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| companyHandle | `xsd:string` | Manejo de la compañía. |
| companyName | `xsd:string` | Nombre de empresa. |
| imageCount | `xsd:int` | Número de imágenes almacenadas. |
| diskSpaceUsage | `xsd:long` | Cara total del archivo en kilobytes. |
| lastModified | `xsd:dateTime` | Fecha, hora y zona horaria de la `DiskUsage` el tipo se modificó por última vez. |
