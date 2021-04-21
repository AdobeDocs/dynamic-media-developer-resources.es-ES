---
description: Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.
solution: Experience Manager
title: Anclaje
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 5%

---


# Anclaje{#anchor}

Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.

Define también el punto central predeterminado para la rotación.

## Propiedades {#section-95740f14160744e7bc763094b8be40d8}

Dos números enteros separados por coma. Desplazamiento de píxeles en relación con la esquina superior izquierda de la imagen de resolución completa.

Anulado por `anchor=` (que a su vez se puede sobrescribir con `origin=`).

## Predeterminado {#section-ca3a4cc837d643519eff15951f2b47a1}

El punto central de la imagen se utiliza si este campo no está presente o si está vacío y si es un registro de imagen válido (es decir, si `catalog::Path` es válido).

## Véase también {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) ,  [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
