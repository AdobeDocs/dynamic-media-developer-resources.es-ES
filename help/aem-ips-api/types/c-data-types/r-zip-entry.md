---
description: Una entrada en un archivo ZIP.
seo-description: Una entrada en un archivo ZIP.
seo-title: ZipEntry
solution: Experience Manager
title: ZipEntry
uuid: 05aac11b-249c-4c44-943d-fa6bf35d3637
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '57'
ht-degree: 10%

---


# ZipEntry{#zipentry}

Una entrada en un archivo ZIP.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`name`*` | `xsd:string` | Nombre de entrada. |
| `*`isDirectory`*` | `xsd:boolean` | Determina si la entrada es un directorio. |
| `*`lastModified`*` | `xsd:dateTime` | Fecha y hora de la última modificación. |
| `*`zipSize`*` | `xsd:long` | Tamaño comprimido. |
| `*`unzipSize`*` | `xsd:long` | Tamaño sin comprimir. |

