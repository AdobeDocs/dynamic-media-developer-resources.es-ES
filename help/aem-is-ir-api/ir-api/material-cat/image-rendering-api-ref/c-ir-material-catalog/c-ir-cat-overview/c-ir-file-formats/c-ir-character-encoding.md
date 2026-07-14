---
title: Codificación de caracteres
description: El procesamiento de imágenes admite catálogos de materiales con codificación ISO-8859-1 y UTF-8.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ee7b33fd-7607-4bff-867b-6e7a837a9ed4
TQID: 'https://experienceleague.adobe.com/1ITLimvCUD8hrdfeyyod6nE0sMmfIJ3ySx5HCFa2ZQk'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 104
ht-degree: 0%

---

# Codificación de caracteres{#character-encoding}

El procesamiento de imágenes admite catálogos de materiales con codificación ISO-8859-1 y UTF-8.

Se utiliza una marca de orden de bytes (BOM) para especificar la codificación de cada archivo. Para UTF-8, la BOM es la secuencia de bytes `EF BB BF`. La codificación UTF-8 se asume cuando esta secuencia de caracteres se detecta al principio de cada fichero de catálogo de materiales. Cualquier otra secuencia de bytes dará como resultado que el archivo se interprete como codificado según el estándar ISO-8859-1.

Muchas aplicaciones contemporáneas, cuando se configuran para UTF-8, insertan la BOM automáticamente.

