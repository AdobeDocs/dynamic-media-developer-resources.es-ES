---
description: Además de cambiar el tamaño (size=) y la posición (pos=) de las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden rotar (rotate=) y voltear (flip=).
solution: Experience Manager
title: Operaciones de capa
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0b167c74-cb1f-45f1-8b15-cb1fcbc8f734
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 0%

---

# Operaciones de capa{#layer-operations}

Además de cambiar el tamaño (size=) y la posición (pos=) de las capas en relación con la capa 0 y especificar el orden de composición (el orden z) con el comando layer=, las capas se pueden rotar (rotate=) y voltear (flip=).

Los atributos `origin=` y `anchor=` se pueden usar para mantener la alineación deseada entre las capas cuando las imágenes o el texto se cambian dinámicamente en las plantillas.

El comando `maskUse=` está disponible para que las capas de imagen accedan al área de fondo de las imágenes que tienen máscaras independientes.

`opac=` se puede usar para variar la opacidad de la capa, y `hide=` para mostrar u ocultar la capa.
