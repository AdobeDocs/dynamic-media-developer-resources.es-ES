---
description: Se admiten cuatro tipos de capas.
seo-description: Se admiten cuatro tipos de capas.
seo-title: Tipos de capas
solution: Experience Manager
title: Tipos de capas
topic: Scene7 Image Serving - Image Rendering API
uuid: d88b2163-7c9f-4885-9722-be3339e7127a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Tipos de capas{#layer-types}

Se admiten cuatro tipos de capas.

## Capas de imagen {#section-3e53df1437694272aca03f927fc0db07}

Las capas de imagen deben tener un `src=` comando que especifique la imagen que se utilizará como capa. Se puede especificar una imagen independiente con `mask=` el fin de utilizarla como máscara de capa o la imagen puede tener ya un canal alfa. El tamaño de las capas de imagen siempre se deriva de la imagen, pero la imagen a menudo se escala para ajustarse al `size=` comando. Se puede aplicar un trazado de clip con `clipPath=`.

## Capas de texto {#section-dc2aec6416a340bcb20c1f884323c8d0}

Debe tener un `text=` comando o `textPs=` que proporcione el contenido del texto en forma de fragmento de texto con formato de texto enriquecido (RTF). Las capas de texto pueden ajustarse a su contenido o pueden tener tamaños explícitos (por ejemplo, si el texto se va a ajustar a una anchura específica o si el texto debe restringirse a un área específica). `textPs=` admiten el flujo de texto en formas arbitrarias definidas con `textFlowPath=` y en rutas arbitrarias definidas con `textPath=`. `textPs=` también admite la representación de texto en el cuadro de texto o en la forma especificada en ángulos arbitrarios ( `textAngle=`).

## Capas de color sólidas {#section-56dfb672756643dda08dc93294809eb0}

Las capas de color sólido suelen utilizarse para la capa 0 en las plantillas, de modo que el tamaño de la imagen compuesta es fijo e independiente del contenido de la imagen. Las capas de color sólido requieren un `color=` atributo, ya sea `size=` o `mask=`, y admiten la mayoría de los demás comandos y atributos para modificar el aspecto. Las capas de color sólido pueden recibir formas arbitrarias con `clipPath=`.

## Capas de efecto {#section-dd3b628bc6734077af4c0ddcebcee05f}

Los efectos de capa de estilo Photoshop, como las sombras paralelas y los efectos de resplandor, se implementan mediante IS mediante subcapas especiales que se pueden adjuntar a capas de imagen, texto y color sólido. Estas capas de efecto heredan la máscara de capa principal y la posición de la capa principal, y su funcionalidad es limitada.
