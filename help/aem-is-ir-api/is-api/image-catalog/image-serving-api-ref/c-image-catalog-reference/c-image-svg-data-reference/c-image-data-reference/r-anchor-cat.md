---
description: Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.
seo-description: Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.
seo-title: Anclaje
solution: Experience Manager
title: Anclaje
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 81069578-8470-4ec0-b755-47b0a8124024
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# Anclaje{#anchor}

Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.

También define el punto central predeterminado para la rotación.

## Propiedades {#section-95740f14160744e7bc763094b8be40d8}

Dos números enteros separados por coma. Desplazamiento de píxeles en relación con la esquina superior izquierda de la imagen de resolución completa.

Sustituido por `anchor=` (que a su vez se puede sobrescribir con `origin=`).

## Predeterminado {#section-ca3a4cc837d643519eff15951f2b47a1}

El punto central de la imagen se utiliza si este campo no está presente o si está vacío y si es un registro de imagen válido (es decir, si `catalog::Path` es válido).

## Véase también {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origen=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
