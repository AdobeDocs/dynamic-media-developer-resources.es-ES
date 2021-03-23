---
description: Segmente para una acción de clic en el explorador.
seo-description: Segmente para una acción de clic en el explorador.
seo-title: Mapa de imagen
solution: Experience Manager
title: Mapa de imagen
uuid: 1a09ab27-7ee1-4162-8047-575f3f5ca8fe
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '113'
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

