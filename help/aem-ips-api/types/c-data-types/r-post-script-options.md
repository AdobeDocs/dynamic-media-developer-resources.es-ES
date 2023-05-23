---
description: Opciones de archivo PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '66'
ht-degree: 12%

---

# [!DNL PostScriptOptions]{#postscriptoptions}

Opciones de archivo PostScript.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| proceso | `xsd:string` | Opción de proceso PostScript. |
| resolution | `xsd:double` | Resolución de archivos. |
| espacio de color | `xsd:string` | Modo de espacio de color PostScript. |
| alfa | `xsd:boolean` | Si se rasteriza el archivo en una imagen. Si es así, creará un fondo transparente si el archivo original se define de esta manera. Generalmente se utiliza para crear logotipos superpuestos. |
| extractSearchWords | `xsd:boolean` | Si se extraerán las palabras de búsqueda del archivo PostScript. |
