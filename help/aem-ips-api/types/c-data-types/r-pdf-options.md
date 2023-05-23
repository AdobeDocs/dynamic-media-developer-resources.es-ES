---
description: Opciones de archivo del PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

Opciones de archivo del PDF.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| proceso | `xsd:string` | Elección de &quot;procesos de PDF&quot;. |
| resolution | `xsd:double` | Resolución de archivos. |
| espacio de color | `xsd:string` | Opción Modo de espacio de color posterior al script. |
| pdfCatalog | `xsd:boolean` | Si se debe combinar un PDF de varias páginas en un catálogo electrónico después de procesarlo (el valor predeterminado es verdadero). |
| extractSearchWords | `xsd:boolean` | Si se extraerán las palabras de búsqueda del archivo del PDF. |
| extractLinks | `xsd:boolean` | Si se extraen vínculos de PDF en mapas de imagen asignados a las páginas rasterizadas en IPS. |
