---
description: El servicio de imágenes admite catálogos de imágenes con codificación ISO-8859-1 y UTF-8.
solution: Experience Manager
title: Codificación de caracteres
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e6e50c2a-53d3-4776-a3f6-4a9d3407e562
TQID: 'https://experienceleague.adobe.com/tsIJu-zCT-NlV6SD1I1pPYQ0DfqNcu9jSCBVXCcQ9tE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Codificación de caracteres{#character-encoding}

El servicio de imágenes admite catálogos de imágenes con codificación ISO-8859-1 y UTF-8.

Se utiliza una marca de orden de bytes (BOM) para especificar la codificación de cada archivo. Para UTF-8, la BOM es la secuencia de bytes `EF BB BF`. La codificación UTF-8 se asume cuando esta secuencia de caracteres se detecta al principio de cada archivo de catálogo de imágenes. Cualquier otra secuencia de bytes hace que el archivo se interprete como codificado según el estándar ISO-8859-1.

Muchas aplicaciones contemporáneas, cuando se configuran para UTF-8, insertan la BOM automáticamente.
