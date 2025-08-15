---
description: Definición de destino para una acción de clic en el explorador.
solution: Experience Manager
title: ImageMapDefinition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 58478e7c-e3a1-4dd5-8ff9-e9752301b93c
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 12%

---

# [!DNL ImageMapDefinition]{#imagemapdefinition}

Definición de destino para una acción de clic en el explorador.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| nombre | `xsd:string` | Nombre de la definición del mapa de imagen. |
| shapeType | `xsd:string` | Uno de los valores de forma de región. |
| región | `xsd:string` | Coordenadas de mapa de imagen. El formato se basa en los atributos de etiquetas de HTML `<area>`. |
| action | `xsd:string` | Otros atributos que se incluirán en la etiqueta de HTML `<area>`, incluida la dirección URL `href`. |
| habilitada | `xsd:boolean` | True si el mapa de imagen está habilitado. |
