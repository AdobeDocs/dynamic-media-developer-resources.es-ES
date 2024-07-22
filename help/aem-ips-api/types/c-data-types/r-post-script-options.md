---
description: Opciones de archivo de PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '65'
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
