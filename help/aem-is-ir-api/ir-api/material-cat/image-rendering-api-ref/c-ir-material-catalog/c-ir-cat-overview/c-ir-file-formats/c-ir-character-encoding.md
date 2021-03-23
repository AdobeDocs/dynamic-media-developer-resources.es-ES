---
description: El procesamiento de imágenes admite catálogos de material con codificación ISO-8859-1 y UTF-8.
seo-description: El procesamiento de imágenes admite catálogos de material con codificación ISO-8859-1 y UTF-8.
seo-title: Codificación de caracteres
solution: Experience Manager
title: Codificación de caracteres
uuid: efc3971b-dca1-4b47-a197-c10270ce17c9
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 0%

---


# Codificación de caracteres{#character-encoding}

El procesamiento de imágenes admite catálogos de material con codificación ISO-8859-1 y UTF-8.

Se utiliza una marca de orden de bytes (BOM) para especificar la codificación de cada archivo. Para UTF-8, la BOM es la secuencia de bytes `EF BB BF`. La codificación UTF-8 se asume cuando se detecta esta secuencia de caracteres al principio de cada archivo de catálogo de materiales. Cualquier otra secuencia de bytes hace que el archivo se interprete como codificado con la norma ISO-8859-1.

Muchas aplicaciones contemporáneas, cuando se configuran para UTF-8, insertan la BOM automáticamente.
