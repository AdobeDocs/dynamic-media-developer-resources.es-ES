---
description: Segmente para una acción de clic en el explorador.
solution: Experience Manager
title: Mapa de imagen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 13%

---

# Mapa de imagen{#imagemap}

Segmente para una acción de clic en el explorador.

Siempre asociado a una imagen. Puede obtener un `ImageMap` destinatario de `ImageInfo`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| imageMapHandle | `xsd:string` | Control de mapa de imagen. |
| name | `xsd:string` | Nombre del mapa de imagen. |
| región | `xsd:string` | Coordenadas del mapa de imagen. El formato se basa en el HTML `<area>` atributo de etiqueta. |
| action | `xsd:string` | Otros atributos a incluir en el HTML `<area>` , incluido el `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] valor. |
| position | `xsd:string` | Posición en el formato del HTML `<area>` del elemento [!DNL coords] atributo. Por ejemplo: `coords ="0,0,84,128"`. |
| habilitada | `xsd:boolean` | True si el mapa de imagen está habilitado. |
| lastModified | `xsd:dateTime` | Fecha y hora de la última modificación del mapa de imagen. |
