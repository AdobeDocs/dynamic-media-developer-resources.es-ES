---
description: Opciones del archivo PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: fd2093b5-9856-4f31-8853-1027194a71df
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 13%

---

# PostScriptOptions{#postscriptoptions}

Opciones del archivo PostScript.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| proceso | `xsd:string` | Selección del proceso PostScript. |
| resolution | `xsd:double` | Resolución de archivos. |
| Espacio de color | `xsd:string` | Modo de espacio de color PostScript. |
| alfa | `xsd:boolean` | Si se va a rasterizar el archivo en una imagen. Si es así, creará un fondo transparente si el archivo original está definido de esta manera. Generalmente se utiliza para crear logotipos superpuestos. |
| extractSearchWords | `xsd:boolean` | Si se extraen palabras de búsqueda del archivo PostScript. |
