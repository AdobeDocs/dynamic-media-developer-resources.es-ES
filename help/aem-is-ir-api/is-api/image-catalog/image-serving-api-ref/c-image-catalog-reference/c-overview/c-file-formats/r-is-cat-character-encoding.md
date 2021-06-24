---
description: El servicio de imágenes admite catálogos de imágenes con codificación ISO-8859-1 y UTF-8.
solution: Experience Manager
title: Codificación de caracteres
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 0%

---

# Codificación de caracteres{#character-encoding}

El servicio de imágenes admite catálogos de imágenes con codificación ISO-8859-1 y UTF-8.

Se utiliza una marca de orden de bytes (BOM) para especificar la codificación de cada archivo. Para UTF-8, la BOM es la secuencia de bytes `EF BB BF`. La codificación UTF-8 se asume cuando se detecta esta secuencia de caracteres al principio de cada archivo de catálogo de imágenes. Cualquier otra secuencia de bytes hace que el archivo se interprete como codificado con la norma ISO-8859-1.

Muchas aplicaciones contemporáneas, cuando se configuran para UTF-8, insertan la BOM automáticamente.
