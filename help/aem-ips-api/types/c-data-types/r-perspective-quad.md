---
description: Coordenadas de ubicación de la imagen devueltas por la operación getPhotoshopPath.
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 8%

---

# [!DNL PerspectiveQuad]{#perspectivequad}

Coordenadas de ubicación de la imagen devueltas por la operación getPhotoshopPath.

Sintaxis

## Parámetros {#section-59792c446366456d90de7f5875bad1b0}

| Nombre | Tipo | Descripción |
|---|---|---|
| x0 | `xsd:double` | Coordenada superior izquierda del eje X. |
| y0 | `xsd:double` | Coordenada superior izquierda del eje Y. |
| x1 | `xsd:double` | Coordenada superior derecha del eje X. |
| y1 | `xsd:double` | Coordenada superior derecha del eje Y. |
| x2 | `xsd:double` | Coordenada inferior derecha del eje X. |
| y2 | `xsd:double` | Coordenada inferior derecha del eje Y. |
| x3 | `xsd:double` | Coordenada inferior izquierda del eje X. |
| y3 | `xsd:double` | Coordenada inferior izquierda del eje Y. |

## Ejemplo {#section-19ed4409ff3a41c9b52a9c9424612927}

El tipo `PerspectiveQuad` devuelve datos en este orden:

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)
