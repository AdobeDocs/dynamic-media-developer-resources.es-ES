---
description: Se admiten cuatro tipos de capas.
solution: Experience Manager
title: Tipos de capas
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9819a73d-1108-414a-831f-37ba94c3feb9
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 0%

---

# Tipos de capas{#layer-types}

Se admiten cuatro tipos de capas.

## Capas de imagen {#section-3e53df1437694272aca03f927fc0db07}

Las capas de imagen deben tener un comando `src=` que especifique la imagen que se utilizará como capa. Se puede especificar una imagen independiente con `mask=` para usarla como máscara de capa o la imagen puede tener ya un canal alfa. El tamaño de las capas de imagen siempre se deriva de la imagen, pero a menudo se escala para ajustarse usando el comando `size=`. Se puede aplicar una ruta de recorte con `clipPath=`.

## Capas de texto {#section-dc2aec6416a340bcb20c1f884323c8d0}

Debe tener un comando `text=` o `textPs=` que proporcione el contenido de texto en forma de fragmento de texto con formato de texto enriquecido (RTF). Las capas de texto pueden ajustarse automáticamente al contenido o pueden tener tamaños explícitos. Por ejemplo, si el texto se va a ajustar a un ancho específico, o si el texto debe restringirse dentro de un área específica. `textPs=` admite el flujo de texto en formas arbitrarias definidas con `textFlowPath=` y en rutas arbitrarias definidas con `textPath=`. `textPs=` también admite la representación de texto en el cuadro de texto o forma especificada en ángulos arbitrarios ( `textAngle=`).

## Capas de color sólido {#section-56dfb672756643dda08dc93294809eb0}

Las capas de color sólido suelen utilizarse para la capa 0 en las plantillas, de modo que el tamaño de la imagen compuesta sea fijo e independiente de cualquier contenido de imagen. Las capas de color sólido requieren un atributo `color=` y `size=` o `mask=`, y admiten la mayoría de los demás comandos y atributos para modificar la apariencia. Las capas de color sólido pueden tener formas arbitrarias con `clipPath=`.

## Capas de efectos {#section-dd3b628bc6734077af4c0ddcebcee05f}

Los efectos de capa de estilo Photoshop, como las sombras paralelas y los efectos de resplandor, se implementan mediante IS utilizando subcapas especiales que se pueden adjuntar a las capas de imagen, texto y color sólido. Estas capas de efectos heredan la máscara y la posición de la capa principal y tienen una funcionalidad limitada.
