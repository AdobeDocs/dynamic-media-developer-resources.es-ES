---
description: opciones del archivo PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '68'
ht-degree: 11%

---

# PDFOptions{#pdfoptions}

opciones del archivo PDF.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| proceso | `xsd:string` | Elección de &quot;procesos PDF&quot;. |
| resolution | `xsd:double` | Resolución de archivos. |
| Espacio de color | `xsd:string` | Opción de modo de espacio de color posterior a la secuencia de comandos. |
| pdfCatalog | `xsd:boolean` | Combinar un PDF de varias páginas en un catálogo electrónico después de la renderización (el valor predeterminado es true). |
| extractSearchWords | `xsd:boolean` | Si se extraen palabras de búsqueda del archivo PDF. |
| extractLinks | `xsd:boolean` | Indica si se extraerán vínculos de PDF en mapas de imágenes asignados a las páginas rasterizadas dentro de IPS. |
