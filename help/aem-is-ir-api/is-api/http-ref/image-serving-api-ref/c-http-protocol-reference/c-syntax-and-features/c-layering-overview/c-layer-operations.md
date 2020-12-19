---
description: Además de cambiar el tamaño (size=) y colocar (pos=) las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden girar (rotate=) y voltear (flip=).
seo-description: Además de cambiar el tamaño (size=) y colocar (pos=) las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden girar (rotate=) y voltear (flip=).
seo-title: Operaciones de capa
solution: Experience Manager
title: Operaciones de capa
topic: Scene7 Image Serving - Image Rendering API
uuid: a9ef4199-cfa2-480e-a4de-8a0b9064a649
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# Operaciones de capa{#layer-operations}

Además de cambiar el tamaño (size=) y colocar (pos=) las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden girar (rotate=) y voltear (flip=).

Los atributos `origin=` y `anchor=` pueden utilizarse para mantener la alineación deseada entre capas cuando las imágenes o el texto se cambian dinámicamente en las plantillas.

El comando `maskUse=` está disponible para que las capas de imagen accedan al área de fondo de las imágenes que tienen máscaras independientes.

`opac=` puede utilizarse para variar la opacidad de la capa y  `hide=` para mostrar u ocultar la capa.
