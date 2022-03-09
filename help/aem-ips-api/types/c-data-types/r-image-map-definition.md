---
description: Definición de destino de una acción de clic en el explorador.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 12%

---

# ImageMapDefinition{#imagemapdefinition}

Definición de destino de una acción de clic en el explorador.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| name | `xsd:string` | Nombre de la definición del mapa de imagen. |
| shapeType | `xsd:string` | Uno de los valores de forma de región. |
| región | `xsd:string` | Coordenadas del mapa de imagen. El formato se basa en el HTML `<area>` atributos de etiqueta. |
| action | `xsd:string` | Otros atributos a incluir en el HTML `<area>` , incluido el `href` URL. |
| habilitada | `xsd:boolean` | True si el mapa de imagen está habilitado. |
