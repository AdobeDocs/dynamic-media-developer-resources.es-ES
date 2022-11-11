---
description: Segmente para una acción de clic en el explorador.
solution: Experience Manager
title: Mapa de imagen
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 7%

---

# [!DNL ImageMap]{#imagemap}

Segmente para una acción de clic en el explorador.

Siempre asociado a una imagen. Puede obtener un `ImageMap` destinatario de `ImageInfo`.

## Parámetros {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nombre | Tipo | Descripción |
|---|---|---|
| imageMapHandle | `xsd:string` | Control de mapa de imagen. |
| [!DNL name] | `xsd:string` | Nombre del mapa de imagen. |
| [!DNL region] | `xsd:string` | Coordenadas del mapa de imagen. El formato se basa en el HTML `<area>` atributo de etiqueta. |
| [!DNL action] | `xsd:string` | Otros atributos a incluir en el HTML `<area>` , incluido el `href` URL. |
| shapeType | `xsd:boolean` | A [!DNL RegionShape] valor. |
| [!DNL position] | `xsd:string` | Posición en el formato del HTML `<area>` del elemento [!DNL coords] atributo. Por ejemplo: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | True si el mapa de imagen está habilitado. |
| lastModified | `xsd:dateTime` | Fecha y hora de la última modificación del mapa de imagen. |
