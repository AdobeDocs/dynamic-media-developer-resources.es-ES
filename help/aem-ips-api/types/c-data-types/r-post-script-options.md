---
description: Opciones de archivo de PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
TQID: 'https://experienceleague.adobe.com/XsIiYor0c-7I34OYazNaSF0Hx3sbZmzpTzAT1u73xxo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 65
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

Opciones de archivo de PostScript.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| proceso | `xsd:string` | Elección de proceso de PostScript. |
| resolution | `xsd:double` | Resolución de archivos. |
| espacio de color | `xsd:string` | Modo de espacio de color PostScript. |
| alfa | `xsd:boolean` | Si se rasteriza el archivo en una imagen. Si es así, crea un fondo transparente si el archivo original si se define de esta manera. Generalmente se utiliza para crear logotipos superpuestos. |
| extractSearchWords | `xsd:boolean` | Si se extraerán las palabras de búsqueda del archivo PostScript. |
