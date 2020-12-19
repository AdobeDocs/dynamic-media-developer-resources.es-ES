---
description: Estadísticas de espacio en disco para un recurso o una carpeta.
seo-description: Estadísticas de espacio en disco para un recurso o una carpeta.
seo-title: DiskUsage
solution: Experience Manager
title: DiskUsage
topic: Scene7 Image Production System API
uuid: a63f0ed0-c689-43b0-9c3e-9500715d15a5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 11%

---


# DiskUsage{#diskusage}

Estadísticas de espacio en disco para un recurso o una carpeta.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Identificador de compañía. |
| ` *`companyName`*` | `xsd:string` | Nombre de empresa. |
| ` *`imageCount`*` | `xsd:int` | Número de imágenes almacenadas. |
| ` *`diskSpaceUsage`*` | `xsd:long` | Lado total del archivo en kilobytes. |
| ` *`lastModified`*` | `xsd:dateTime` | Fecha, hora y zona horaria en la que se modificó por última vez el tipo `DiskUsage`. |

