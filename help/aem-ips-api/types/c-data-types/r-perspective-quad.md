---
description: Coordenadas de ubicación de imagen devueltas por la operación getPhotoshopPath.
seo-description: Coordenadas de ubicación de imagen devueltas por la operación getPhotoshopPath.
seo-title: PerspectiveQuad
solution: Experience Manager
title: PerspectiveQuad
uuid: e83b7b8c-995b-4ac0-ace5-491f7e98674d
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, administrador
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 15%

---


# PerspectiveQuad{#perspectivequad}

Coordenadas de ubicación de imagen devueltas por la operación getPhotoshopPath.

Sintaxis

## Parámetros {#section-59792c446366456d90de7f5875bad1b0}

| Nombre | Tipo | Descripción |
|---|---|---|
| `*`x0`*` | `xsd:double` | Coordenada del eje x superior izquierdo. |
| `*`y0`*` | `xsd:double` | Coordenada superior izquierda del eje Y. |
| `*`x1`*` | `xsd:double` | Coordenada del eje x superior derecho. |
| `*`y1`*` | `xsd:double` | Coordenada superior derecha del eje Y. |
| `*`x2`*` | `xsd:double` | Coordenada del eje x inferior derecho. |
| `*`y2`*` | `xsd:double` | Coordenada inferior derecha del eje Y. |
| `*`x3`*` | `xsd:double` | Coordenada del eje x inferior izquierdo. |
| `*`y3`*` | `xsd:double` | Coordenada inferior izquierda del eje Y. |

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

