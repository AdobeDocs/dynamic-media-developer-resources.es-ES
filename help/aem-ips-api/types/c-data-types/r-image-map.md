---
description: Segmente para una acción de clic en el explorador.
solution: Experience Manager
title: Mapa de imagen
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 12%

---

# Mapa de imagen{#imagemap}

Segmente para una acción de clic en el explorador.

Siempre asociado a una imagen. Puede obtener un destinatario `ImageMap` de `ImageInfo`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`imageMapHandle`*` | `xsd:string` | Control de mapa de imagen. |
| `*`name`*` | `xsd:string` | Nombre del mapa de imagen. |
| `*`región`*` | `xsd:string` | Coordenadas del mapa de imagen. El formato se basa en el atributo de etiqueta HTML `<area>`. |
| `*`action`*` | `xsd:string` | Otros atributos a incluir en la etiqueta HTML `<area>` , incluida la dirección URL `href`. |
| `*`shapeType`*` | `xsd:boolean` | Un valor [!DNL RegionShape]. |
| `*`position`*` | `xsd:string` | Posición en el formato del atributo `<area>` del elemento HTML [!DNL coords]. Por ejemplo: `coords ="0,0,84,128"`. |
| `*`habilitada`*` | `xsd:boolean` | True si el mapa de imagen está habilitado. |
| `*`lastModified`*` | `xsd:dateTime` | Fecha y hora de la última modificación del mapa de imagen. |
