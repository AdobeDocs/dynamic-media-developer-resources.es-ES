---
description: Destinatario para una acción de clic en el explorador.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---

# [!DNL ImageMap]{#imagemap}

Destinatario para una acción de clic en el explorador.

Siempre asociado a una imagen. Puede obtener un destino `ImageMap` de `ImageInfo`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| imageMapHandle | `xsd:string` | Controlador de mapa de imagen. |
| [!DNL name] | `xsd:string` | Nombre del mapa de imagen. |
| [!DNL region] | `xsd:string` | Coordenadas de mapa de imagen. El formato se basa en el atributo de etiqueta de HTML `<area>`. |
| [!DNL action] | `xsd:string` | Otros atributos que se incluirán en la etiqueta de HTML `<area>`, incluida la dirección URL `href`. |
| shapeType | `xsd:boolean` | Un valor [!DNL RegionShape]. |
| [!DNL position] | `xsd:string` | Coloque en el formato del atributo `<area>` del elemento [!DNL coords] de HTML. Por ejemplo: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | El valor es True si el mapa de imagen está habilitado. |
| lastModified | `xsd:dateTime` | Fecha y hora de la última modificación del mapa de imagen. |
