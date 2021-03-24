---
description: Opciones del archivo PostScript.
solution: Experience Manager
title: PostScriptOptions
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 10%

---


# PostScriptOptions{#postscriptoptions}

Opciones del archivo PostScript.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`proceso`*` | `xsd:string` | Selección del proceso PostScript. |
| `*`resolution`*` | `xsd:double` | Resolución de archivos. |
| `*`Espacio de color`*` | `xsd:string` | Modo de espacio de color PostScript. |
| `*`alpha`*` | `xsd:boolean` | Si se va a rasterizar el archivo en una imagen. Si es así, creará un fondo transparente si el archivo original está definido de esta manera. Generalmente se utiliza para crear logotipos superpuestos. |
| `*`extractSearchWords`*` | `xsd:boolean` | Si se extraen palabras de búsqueda del archivo PostScript. |

