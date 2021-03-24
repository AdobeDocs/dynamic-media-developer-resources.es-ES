---
description: Una entrada en un archivo ZIP.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '50'
ht-degree: 12%

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

