---
description: Destinatario de una acción de clic en el explorador.
seo-description: Destinatario de una acción de clic en el explorador.
seo-title: Mapa de imagen
solution: Experience Manager
title: Mapa de imagen
topic: Scene7 Image Production System API
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 13%

---


# Mapa de imagen{#imagemap}

Destinatario de una acción de clic en el explorador.

Siempre asociado a una imagen. Puede obtener un destinatario `ImageMap` de `ImageInfo`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| ` *`imageMapHandle`*` | `xsd:string` | Identificador de mapa de imagen. |
| ` *`name`*` | `xsd:string` | Nombre del mapa de imagen. |
| ` *`región`*` | `xsd:string` | Coordenadas del mapa de imagen. El formato se basa en el atributo de etiqueta HTML `<area>`. |
| ` *`action`*` | `xsd:string` | Otros atributos que se incluirán en la etiqueta HTML `<area>`, incluida la dirección URL `href`. |
| ` *`shapeType`*` | `xsd:boolean` | Un valor [!DNL RegionShape]. |
| ` *`position`*` | `xsd:string` | Posición en el formato del atributo `<area>` del elemento HTML [!DNL coords]. Por ejemplo: `coords ="0,0,84,128"`. |
| ` *`habilitada`*` | `xsd:boolean` | True si el mapa de imagen está activado. |
| ` *`lastModified`*` | `xsd:dateTime` | Fecha y hora de la última modificación del mapa de imagen. |

