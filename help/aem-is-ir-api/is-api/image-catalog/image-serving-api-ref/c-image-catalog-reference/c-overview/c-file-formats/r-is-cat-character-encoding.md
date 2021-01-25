---
description: El servicio de imágenes admite catálogos de imágenes con codificación ISO-8859-1 y UTF-8.
seo-description: El servicio de imágenes admite catálogos de imágenes con codificación ISO-8859-1 y UTF-8.
seo-title: Codificación de caracteres
solution: Experience Manager
title: Codificación de caracteres
topic: Dynamic Media Image Serving - Image Rendering API
uuid: dfb56411-40d1-4bac-9213-9104ecba2a02
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 0%

---


# Codificación de caracteres{#character-encoding}

El servicio de imágenes admite catálogos de imágenes con codificación ISO-8859-1 y UTF-8.

Se utiliza una marca de orden de bytes (BOM) para especificar la codificación de cada archivo. Para UTF-8, la L. MAT es la secuencia de bytes `EF BB BF`. La codificación UTF-8 se asume cuando se detecta esta secuencia de caracteres al principio de cada archivo de catálogo de imágenes. Cualquier otra secuencia de bytes hace que el archivo se interprete como codificado según el estándar ISO-8859-1.

Muchas aplicaciones contemporáneas, cuando se configuran para UTF-8, insertan la L. MAT automáticamente.
