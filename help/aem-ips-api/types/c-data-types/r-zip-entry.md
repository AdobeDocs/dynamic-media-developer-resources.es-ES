---
description: Una entrada en un archivo ZIP.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '48'
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
