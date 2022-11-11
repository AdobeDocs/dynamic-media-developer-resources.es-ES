---
description: Una entrada en un archivo ZIP.
solution: Experience Manager
title: ZipEntry
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f71f57db-6717-4a27-b275-19bc4cf59ea4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '42'
ht-degree: 14%

---

# [!DNL ZipEntry]{#zipentry}

Una entrada en un archivo ZIP.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| name | `xsd:string` | Nombre de entrada. |
| isDirectory | `xsd:boolean` | Determina si la entrada es un directorio. |
| lastModified | `xsd:dateTime` | Fecha y hora de la última modificación. |
| zipSize | `xsd:long` | Tamaño comprimido. |
| unzipSize | `xsd:long` | Tamaño sin comprimir. |
