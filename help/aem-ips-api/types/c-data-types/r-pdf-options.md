---
description: Opciones de archivo de PDF.
solution: Experience Manager
title: PDFOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 140c9261-e590-4889-9be4-29afd19ffa86
TQID: 'https://experienceleague.adobe.com/gjd-g7jhWVbLRL3kYnkX96ihjkiK34oCp7Ns1iC89GM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 68
ht-degree: 10%

---

# [!DNL PDFOptions]{#pdfoptions}

Opciones de archivo de PDF.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| proceso | `xsd:string` | Elección de &quot;Procesos de PDF&quot;. |
| resolution | `xsd:double` | Resolución de archivos. |
| espacio de color | `xsd:string` | Opción Modo de espacio de color posterior al script. |
| pdfCatalog | `xsd:boolean` | Si se debe combinar un PDF de varias páginas en un catálogo electrónico después de procesarlo (el valor predeterminado es verdadero). |
| extractSearchWords | `xsd:boolean` | Si se extraerán las palabras de búsqueda del archivo PDF. |
| extractLinks | `xsd:boolean` | Si se extraen vínculos de PDF en mapas de imagen asignados a las páginas rasterizadas en IPS. |
