---
description: Estadísticas de espacio en disco para un recurso o carpeta.
solution: Experience Manager
title: Uso del disco
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a3c4c1cd-0fcc-4e7a-a4aa-884d0ce2f208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '51'
ht-degree: 13%

---

# Uso del disco{#diskusage}

Estadísticas de espacio en disco para un recurso o carpeta.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| companyHandle | `xsd:string` | Identificador de la empresa. |
| companyName | `xsd:string` | Nombre de empresa. |
| imageCount | `xsd:int` | Número de imágenes almacenadas. |
| diskSpaceUsage | `xsd:long` | Lado total del archivo en kilobytes. |
| lastModified | `xsd:dateTime` | Fecha, hora y zona horaria de la `DiskUsage` se modificó por última vez. |
