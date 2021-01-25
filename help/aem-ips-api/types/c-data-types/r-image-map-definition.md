---
description: Definición de destinatario para una acción de clic en el explorador.
seo-description: Definición de destinatario para una acción de clic en el explorador.
seo-title: ImageMapDefinition
solution: Experience Manager
title: ImageMapDefinition
topic: Dynamic Media Image Production System API
uuid: e3b9a304-5c43-46ce-8e87-860b49006a37
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 10%

---


# ImageMapDefinition{#imagemapdefinition}

Definición de destinatario para una acción de clic en el explorador.

Sintaxis

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`name`*` | `xsd:string` | Nombre de la definición del mapa de imagen. |
| `*`shapeType`*` | `xsd:string` | Uno de los valores de forma de región. |
| `*`región`*` | `xsd:string` | Coordenadas del mapa de imagen. El formato se basa en los atributos de etiqueta HTML `<area>`. |
| `*`action`*` | `xsd:string` | Otros atributos que se incluirán en la etiqueta HTML `<area>`, incluida la dirección URL `href`. |
| `*`habilitada`*` | `xsd:boolean` | True si el mapa de imagen está activado. |

