---
description: Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.
solution: Experience Manager
title: Anclaje
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c54b8bb2-af4f-4c05-be7b-4326dd08993a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 4%

---

# Anclaje{#anchor}

Anclaje de imagen. Punto de origen cuando esta imagen se utiliza como capa en una plantilla o imagen compuesta.

Define también el punto central por defecto para la rotación.

## Propiedades {#section-95740f14160744e7bc763094b8be40d8}

Dos números enteros, separados por una coma. Desplazamiento de píxel relativo a la esquina superior izquierda de la imagen de resolución completa.

Anulado por `anchor=`(que a su vez se puede anular con `origin=`).

## Predeterminado {#section-ca3a4cc837d643519eff15951f2b47a1}

El punto central de la imagen se utiliza si este campo no está presente o si está vacío, y si se trata de un registro de imagen válido (es decir, si `catalog::Path` es válido).

## Véase también {#section-f605d29c3f5d48ad8e2a374f11886f19}

[anchor=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md) , [origin=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md)
