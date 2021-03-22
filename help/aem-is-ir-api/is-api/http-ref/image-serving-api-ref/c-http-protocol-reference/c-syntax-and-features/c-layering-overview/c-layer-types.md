---
description: Se admiten cuatro tipos de capas.
seo-description: Se admiten cuatro tipos de capas.
seo-title: Tipos de capas
solution: Experience Manager
title: Tipos de capas
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
feature: Dynamic Media Classic,SDK/API
role: Desarrollador, profesional empresarial
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---


# Tipos de capa{#layer-types}

Se admiten cuatro tipos de capas.

## Capas de imagen {#section-3e53df1437694272aca03f927fc0db07}

Las capas de imagen deben tener un comando `src=` que especifique la imagen que se utilizará como capa. Se puede especificar una imagen independiente con `mask=` para utilizarla como máscara de capa o la imagen puede tener ya un canal alfa. El tamaño de las capas de imagen siempre se deriva de la imagen, pero la imagen a menudo se escala para ajustarse al comando `size=`. Se puede aplicar una ruta de clip con `clipPath=`.

## Capas de texto {#section-dc2aec6416a340bcb20c1f884323c8d0}

Debe tener un comando `text=` o `textPs=` que proporcione el contenido del texto en forma de fragmento de texto con formato de texto enriquecido (RTF). Las capas de texto pueden ajustarse al tamaño de su contenido o pueden tener tamaños explícitos (por ejemplo, si el texto se va a ajustar a una anchura específica o si el texto debe restringirse en un área específica). `textPs=` admiten el flujo de texto en formas arbitrarias definidas con  `textFlowPath=` y en rutas arbitrarias definidas con  `textPath=`. `textPs=` también admite el procesamiento de texto en el cuadro de texto o la forma especificada en ángulos arbitrarios (  `textAngle=`).

## Capas de color sólido {#section-56dfb672756643dda08dc93294809eb0}

Las capas de color sólido se utilizan a menudo para la capa 0 de las plantillas, de modo que el tamaño de la imagen compuesta es fijo e independiente del contenido de la imagen. Las capas de color sólido requieren un atributo `color=` y `size=` o `mask=`, y admiten la mayoría de los demás comandos y atributos para modificar el aspecto. Las capas de color sólido pueden recibir formas arbitrarias con `clipPath=`.

## Capas de efecto {#section-dd3b628bc6734077af4c0ddcebcee05f}

Los efectos de capa de estilo Photoshop, como sombras paralelas y efectos de resplandor, se implementan mediante el uso de subcapas especiales que se pueden adjuntar a capas de imagen, texto y color sólido. Estas capas de efecto heredan la máscara de capa principal y la posición de la capa principal, y su funcionalidad es limitada.
