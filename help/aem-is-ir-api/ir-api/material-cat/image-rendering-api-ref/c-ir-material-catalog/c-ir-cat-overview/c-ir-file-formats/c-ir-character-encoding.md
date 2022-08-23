---
title: Codificación de caracteres
description: El procesamiento de imágenes admite catálogos de material con codificación ISO-8859-1 y UTF-8.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 0%

---

# Codificación de caracteres{#character-encoding}

El procesamiento de imágenes admite catálogos de material con codificación ISO-8859-1 y UTF-8.

Se utiliza una marca de orden de bytes (BOM) para especificar la codificación de cada archivo. Para UTF-8, BOM es la secuencia de bytes `EF BB BF`. La codificación UTF-8 se asume cuando se detecta esta secuencia de caracteres al principio de cada archivo de catálogo de materiales. Cualquier otra secuencia de bytes hace que el archivo se interprete como codificado con la norma ISO-8859-1.

Muchas aplicaciones contemporáneas, cuando se configuran para UTF-8, insertan la BOM automáticamente.
