---
description: Propiedades del archivo PostScript.
solution: Experience Manager
title: GenerationInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9aac2973-bbcb-4914-9bf9-203f0357527c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 14%

---

# GenerationInfo{#generationinfo}

Propiedades del archivo PostScript.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| motor | `xsd:string` | Motor de generación utilizado (consulte &quot;Información de generación&quot; para conocer los valores). |
| originator | `types:Asset` | Registro de recursos del recurso principal utilizado en la generación. |
| generado | `types:Asset` | Registro de recursos del recurso generado. |
| attributeArray | `types:GenerationAttributeArray` | Matriz de atributos asociados al proceso de generación. |
