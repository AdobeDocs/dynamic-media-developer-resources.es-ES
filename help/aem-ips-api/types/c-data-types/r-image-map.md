---
description: Destinatario para una acción de clic en el explorador.
solution: Experience Manager
title: ImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 123eba56-2a59-44c5-93f0-205c362d071d
TQID: 'https://experienceleague.adobe.com/ikMxCQ23L0HzbfmRlcYGL-fRJFK2uhwbZHNzcy1c25k'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: b658a9f9067d2313c1c838c7e157f4070ebc2b50
workflow-type: tm+mt
source-wordcount: 91
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
| [!DNL position] | `xsd:string` | Coloque en el formato del atributo [!DNL coords] del elemento `<area>` de HTML. Por ejemplo: `coords ="0,0,84,128"`. |
| [!DNL enabled] | `xsd:boolean` | El valor es True si el mapa de imagen está habilitado. |
| lastModified | `xsd:dateTime` | Fecha y hora de la última modificación del mapa de imagen. |

